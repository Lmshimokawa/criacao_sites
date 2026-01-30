# Lição O1 — Como um Site Funciona

> **Fase**: O — Operação & Infraestrutura  
> **Status**: ✅ Concluída  
> **Data de início**: 2025-01-28  
> **Data de conclusão**: 2025-01-28

---

## 🎯 Objetivo da Lição

Entender os **fundamentos técnicos** de como um site funciona, desde a requisição do navegador até a renderização da página, para tomar decisões informadas sobre stack e infraestrutura.

---

## 📚 Conceitos-Chave (3 Camadas)

### Camada 1: Definição Simples

#### O que acontece quando você acessa um site?

```
1. Você digita "verdebarro.com.br" no navegador
         ↓
2. DNS traduz o nome para um IP (ex: 76.76.21.21)
         ↓
3. Navegador faz requisição HTTP/HTTPS para esse IP
         ↓
4. Servidor recebe a requisição
         ↓
5. Servidor processa e retorna HTML, CSS, JS
         ↓
6. Navegador renderiza a página
         ↓
7. Você vê o site
```

---

#### Componentes Principais

**1. DOMÍNIO**
```
O "nome" do site (verdebarro.com.br)
- Registrado em um registrador (Registro.br, GoDaddy, etc.)
- Aponta para servidores DNS
- Custo: ~R$ 40-80/ano para .com.br
```

**2. DNS (Domain Name System)**
```
"Agenda telefônica" da internet
- Traduz nomes em IPs
- Configurado no registrador ou serviço separado
- Cloudflare DNS é gratuito e rápido
```

**3. HOSPEDAGEM (Hosting)**
```
Onde os arquivos do site ficam
- Servidor que responde às requisições
- Pode ser: VPS, Cloud, Serverless
- Custo: R$ 0 (free tier) a R$ 500+/mês
```

**4. FRONT-END**
```
O que o usuário vê e interage
- HTML: Estrutura
- CSS: Estilo
- JavaScript: Interatividade
- Roda no navegador do usuário
```

**5. BACK-END**
```
O que acontece "por trás"
- Processa lógica de negócio
- Acessa banco de dados
- Autentica usuários
- Roda no servidor
```

**6. BANCO DE DADOS**
```
Onde os dados são armazenados
- Pedidos, usuários, produtos
- SQL (PostgreSQL, MySQL) ou NoSQL (MongoDB)
- Pode ser gerenciado (Supabase, PlanetScale) ou próprio
```

**7. APIs**
```
Comunicação entre sistemas
- Front-end ↔ Back-end
- Seu site ↔ Stripe (pagamentos)
- Seu site ↔ WhatsApp (mensagens)
- Geralmente REST ou GraphQL
```

---

#### Tipos de Sites

**1. SITE ESTÁTICO**
```
Arquivos HTML/CSS/JS pré-gerados
- Não muda baseado no usuário
- Muito rápido
- Fácil de hospedar (gratuito)
- Exemplo: Landing page simples

Prós: Rápido, barato, seguro
Contras: Não tem lógica dinâmica
```

**2. SITE DINÂMICO (SSR - Server-Side Rendering)**
```
HTML gerado no servidor a cada requisição
- Pode mudar baseado no usuário
- Acessa banco de dados em tempo real
- Exemplo: E-commerce tradicional

Prós: SEO bom, dados sempre atualizados
Contras: Mais lento, servidor necessário
```

**3. SPA (Single Page Application)**
```
JavaScript carrega tudo no cliente
- Navegação sem recarregar página
- Dados via API
- Exemplo: Apps como Gmail, Trello

Prós: UX fluida, interativo
Contras: SEO ruim, carregamento inicial lento
```

**4. HÍBRIDO (SSG + CSR)**
```
Páginas estáticas pré-geradas + hidratação no cliente
- Melhor dos dois mundos
- Exemplo: Next.js, Astro

Prós: Rápido, bom SEO, interativo
Contras: Mais complexo
```

---

### Camada 2: Aplicação no Caso Verde Barro

#### O que Verde Barro precisa?

**Requisitos do site**:
- Páginas institucionais (Home, Experiências, Peças, Contato)
- Blog para SEO (artigos)
- Catálogo de peças (pode mudar)
- Checkout customizado (compartilhável)
- Integração com pagamentos
- Integração com WhatsApp
- Integração com agendamento
- Newsletter/email capture
- Mobile-first
- Carregamento rápido

**Análise por tipo de site**:

```
ESTÁTICO PURO?
- ✅ Páginas institucionais
- ✅ Blog (pode ser gerado)
- ❌ Checkout dinâmico
- ❌ Catálogo que muda
→ Não serve sozinho

SSR PURO?
- ✅ Tudo funciona
- ❌ Mais lento que necessário
- ❌ Custo de servidor
→ Overkill para páginas simples

SPA PURA?
- ❌ SEO ruim (blog não indexa bem)
- ❌ Carregamento inicial lento
→ Não serve

HÍBRIDO?
- ✅ Páginas estáticas para institucional
- ✅ Blog estático (gerado no build)
- ✅ Checkout dinâmico onde precisa
- ✅ APIs para pagamentos
- ✅ Bom SEO
- ✅ Rápido
→ IDEAL para Verde Barro
```

**Conclusão**: Site híbrido com páginas estáticas e funcionalidades dinâmicas onde necessário.

---

#### Arquitetura Proposta

```
┌─────────────────────────────────────────────────────────────┐
│                        USUÁRIO                              │
│                     (navegador mobile)                      │
└────────────────────────────┬────────────────────────────────┘
                             │
                             ▼
┌─────────────────────────────────────────────────────────────┐
│                         CDN                                 │
│              (Vercel Edge / Cloudflare)                     │
│         Cache de páginas estáticas no mundo todo            │
└────────────────────────────┬────────────────────────────────┘
                             │
              ┌──────────────┴──────────────┐
              │                             │
              ▼                             ▼
┌─────────────────────────┐   ┌─────────────────────────┐
│    PÁGINAS ESTÁTICAS    │   │    FUNÇÕES SERVERLESS   │
│                         │   │                         │
│  • Home                 │   │  • API checkout         │
│  • Experiências         │   │  • API links grupo      │
│  • Peças                │   │  • Webhooks Stripe      │
│  • Contato              │   │  • Webhooks email       │
│  • Blog                 │   │                         │
│                         │   │                         │
│  (HTML pré-gerado)      │   │  (Node.js on-demand)    │
└─────────────────────────┘   └───────────┬─────────────┘
                                          │
                              ┌───────────┴───────────┐
                              │                       │
                              ▼                       ▼
                   ┌─────────────────┐     ┌─────────────────┐
                   │   BANCO DADOS   │     │    SERVIÇOS     │
                   │                 │     │    EXTERNOS     │
                   │  • Pedidos      │     │                 │
                   │  • Links grupo  │     │  • Stripe       │
                   │  • Newsletter   │     │  • Resend       │
                   │                 │     │  • Cal.com      │
                   │  (Supabase/     │     │  • WhatsApp     │
                   │   PlanetScale)  │     │                 │
                   └─────────────────┘     └─────────────────┘
```

---

#### Fluxo de uma Compra

```
1. USUÁRIO ACESSA /experiencias
   └─→ CDN serve HTML estático (< 100ms)

2. USUÁRIO CLICA "AGENDAR"
   └─→ JavaScript abre modal de checkout

3. USUÁRIO PREENCHE DADOS
   └─→ Validação no cliente

4. USUÁRIO CLICA "PAGAR"
   └─→ API Route: POST /api/checkout
   └─→ Serverless function processa
   └─→ Cria sessão no Stripe
   └─→ Salva pedido no banco
   └─→ Retorna URL do Stripe

5. USUÁRIO PAGA NO STRIPE
   └─→ Stripe processa pagamento
   └─→ Webhook: POST /api/webhooks/stripe
   └─→ Atualiza status do pedido
   └─→ Envia email de confirmação

6. USUÁRIO RECEBE CONFIRMAÇÃO
   └─→ Redirect para /confirmacao/[id]
   └─→ Página com detalhes do pedido
```

---

### Camada 3: Trade-offs, Riscos e Validação

#### Trade-offs de Arquitetura

**1. Serverless vs Servidor Dedicado**
```
SERVERLESS (Vercel, Netlify)
Prós:
- Escala automaticamente
- Paga só pelo uso
- Zero manutenção de servidor
- Deploy simples

Contras:
- Cold starts (primeira requisição lenta)
- Limite de tempo de execução
- Menos controle

SERVIDOR DEDICADO (VPS, EC2)
Prós:
- Controle total
- Sem cold starts
- Mais barato em alto volume

Contras:
- Manutenção necessária
- Escala manual
- Precisa de DevOps
```

**Escolha para Verde Barro**: Serverless
- Volume inicial baixo
- Não precisa de DevOps
- Escala se viralizar

---

**2. Banco de Dados Gerenciado vs Próprio**
```
GERENCIADO (Supabase, PlanetScale)
Prós:
- Backups automáticos
- Escala automática
- Interface amigável
- Menos trabalho

Contras:
- Custo maior em volume alto
- Vendor lock-in
- Limites do plano

PRÓPRIO (PostgreSQL em VPS)
Prós:
- Controle total
- Mais barato em volume
- Sem limites

Contras:
- Manutenção necessária
- Backups manuais
- Precisa de conhecimento
```

**Escolha para Verde Barro**: Gerenciado (Supabase)
- Começar rápido
- Não precisa de DBA
- Free tier generoso

---

**3. Framework Pesado vs Leve**
```
PESADO (Next.js)
Prós:
- Tudo incluso
- Comunidade grande
- Flexível

Contras:
- Bundle maior
- Mais complexo
- Pode ser overkill

LEVE (Astro)
Prós:
- Muito rápido
- Bundle pequeno
- Simples

Contras:
- Menos flexível
- Comunidade menor
- Menos recursos built-in
```

**Decisão**: Avaliar na Lição O2

---

#### Riscos Técnicos

**1. Performance**
- **Risco**: Site lento, usuário desiste
- **Mitigação**: CDN global, páginas estáticas, imagens otimizadas
- **Meta**: < 3 segundos de carregamento

**2. Disponibilidade**
- **Risco**: Site fora do ar
- **Mitigação**: Hospedagem confiável (Vercel tem 99.99% uptime)
- **Meta**: < 1h de downtime/mês

**3. Segurança**
- **Risco**: Dados vazados, pagamentos fraudulentos
- **Mitigação**: HTTPS, Stripe (PCI compliant), LGPD
- **Status**: A detalhar na Lição O4

**4. Custos**
- **Risco**: Custos explodirem
- **Mitigação**: Free tiers, monitoramento, limites
- **Estimativa**: R$ 0-100/mês no início

---

#### Validação Técnica

**Perguntas para validar arquitetura**:

1. ✅ As páginas institucionais carregam rápido? (< 1s)
2. ✅ O checkout funciona no mobile?
3. ✅ Os pagamentos são processados corretamente?
4. ✅ Os emails são enviados?
5. ✅ O SEO está funcionando? (Google indexa)
6. ✅ Os dados estão seguros?

---

## 📦 Entregáveis

### 1. Glossário Técnico

| Termo | Definição |
|-------|-----------|
| **DNS** | Sistema que traduz nomes de domínio em IPs |
| **CDN** | Rede de servidores que distribui conteúdo globalmente |
| **SSL/TLS** | Protocolo de segurança (o "S" do HTTPS) |
| **API** | Interface para comunicação entre sistemas |
| **REST** | Padrão de API usando HTTP (GET, POST, PUT, DELETE) |
| **Serverless** | Funções que rodam sob demanda, sem servidor fixo |
| **SSG** | Static Site Generation - páginas geradas no build |
| **SSR** | Server-Side Rendering - páginas geradas por requisição |
| **Webhook** | Notificação automática de um sistema para outro |
| **Edge** | Servidores próximos do usuário geograficamente |

---

### 2. Checklist de Infraestrutura

**Domínio**:
- [ ] Domínio registrado (verdebarro.com.br)
- [ ] DNS configurado
- [ ] SSL/HTTPS ativo

**Hospedagem**:
- [ ] Plataforma escolhida (Vercel/Netlify)
- [ ] Projeto criado
- [ ] Deploy automático configurado (GitHub)

**Banco de Dados**:
- [ ] Serviço escolhido (Supabase)
- [ ] Projeto criado
- [ ] Tabelas definidas
- [ ] Conexão configurada

**Pagamentos**:
- [ ] Conta Stripe criada
- [ ] Chaves de API configuradas
- [ ] Webhooks configurados
- [ ] Teste em sandbox

**Email**:
- [ ] Serviço escolhido (Resend)
- [ ] Domínio verificado
- [ ] Templates criados
- [ ] Teste de envio

**Analytics**:
- [ ] Serviço escolhido (Plausible/GA4)
- [ ] Script instalado
- [ ] Eventos configurados

---

### 3. Estimativa de Custos

**Cenário: Início (0-100 pedidos/mês)**

| Serviço | Plano | Custo/mês |
|---------|-------|-----------|
| Domínio | .com.br | ~R$ 7/mês (anual) |
| Hospedagem | Vercel Free | R$ 0 |
| Banco de Dados | Supabase Free | R$ 0 |
| Pagamentos | Stripe | 3.99% + R$ 0.39/transação |
| Email | Resend Free | R$ 0 (3k emails/mês) |
| Analytics | Plausible | €9/mês (~R$ 50) ou GA4 grátis |
| **Total fixo** | | **~R$ 7-60/mês** |

**Cenário: Crescimento (100-500 pedidos/mês)**

| Serviço | Plano | Custo/mês |
|---------|-------|-----------|
| Domínio | .com.br | ~R$ 7/mês |
| Hospedagem | Vercel Pro | $20 (~R$ 100) |
| Banco de Dados | Supabase Pro | $25 (~R$ 130) |
| Pagamentos | Stripe | 3.99% + R$ 0.39/transação |
| Email | Resend Pro | $20 (~R$ 100) |
| Analytics | Plausible | €9/mês (~R$ 50) |
| **Total fixo** | | **~R$ 400/mês** |

---

## ✅ Checklist da Lição

- [x] Conceitos explicados (3 camadas)
- [x] Fluxo de requisição web explicado
- [x] Tipos de sites comparados
- [x] Arquitetura para Verde Barro proposta
- [x] Trade-offs analisados
- [x] Glossário técnico criado
- [x] Checklist de infraestrutura criado
- [x] Estimativa de custos criada
- [x] Logs atualizados

---

**Última atualização**: 2025-01-28
