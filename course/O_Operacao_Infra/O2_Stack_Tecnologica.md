# Lição O2 — Stack Tecnológica

> **Fase**: O — Operação & Infraestrutura  
> **Status**: ✅ Concluída  
> **Data de início**: 2025-01-30  
> **Data de conclusão**: 2025-01-30

---

## 🎯 Objetivo da Lição

Escolher a **stack tecnológica** ideal para Verde Barro, comparando opções com base em requisitos do projeto, complexidade, custo e escalabilidade.

---

## 📚 Conceitos-Chave (3 Camadas)

### Camada 1: Definição Simples

**Stack Tecnológica** é o conjunto de tecnologias usadas para construir e operar um sistema.

**Componentes típicos de uma stack web**:
```
FRONTEND          BACKEND           BANCO DE DADOS
(o que usuário    (lógica do        (onde dados
vê e interage)    servidor)         são guardados)
     │                │                   │
     ▼                ▼                   ▼
React, Vue,      Node.js,          PostgreSQL,
Next.js, Astro   Python, Go        MongoDB, MySQL
     │                │                   │
     └────────────────┴───────────────────┘
                      │
                      ▼
               INFRAESTRUTURA
               (onde tudo roda)
                      │
                      ▼
            Vercel, AWS, Netlify
```

**Critérios para escolher stack**:
1. **Requisitos do projeto**: O que precisa fazer?
2. **Conhecimento da equipe**: O que já sabem?
3. **Velocidade de desenvolvimento**: Quão rápido precisa entregar?
4. **Escalabilidade**: Vai crescer muito?
5. **Custo**: Quanto pode gastar?
6. **Comunidade**: Tem suporte e documentação?

---

### Camada 2: Aplicação no Caso Verde Barro

#### Requisitos Técnicos (recap)

**Páginas**:
- Home (estática)
- Experiências (estática + checkout dinâmico)
- Peças Autorais (catálogo dinâmico + checkout)
- Contato (estática)
- Blog (estático, gerado)

**Funcionalidades dinâmicas**:
- Checkout individual
- Checkout compartilhável (diferencial!)
- Integração Stripe (pagamentos)
- Integração email (Resend)
- Integração agendamento (Cal.com)
- Newsletter capture
- Catálogo de peças (admin simples)

**Requisitos não-funcionais**:
- Mobile-first
- Carregamento < 3 segundos
- SEO excelente (blog indexável)
- HTTPS obrigatório
- LGPD compliance

---

## 📦 Duas Opções de Stack

### OPÇÃO A: Simples e Rápida

**Filosofia**: Menor complexidade, deploy mais rápido, menos código customizado.

```
┌─────────────────────────────────────────────────────────────┐
│                    OPÇÃO A: SIMPLES                         │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  FRONTEND + BACKEND                                         │
│  ─────────────────                                          │
│  Next.js 14 (App Router)                                    │
│  • React para UI                                            │
│  • Server Components                                        │
│  • API Routes para backend                                  │
│  • SSG para páginas estáticas                               │
│                                                             │
│  ESTILIZAÇÃO                                                │
│  ───────────                                                │
│  Tailwind CSS                                               │
│  • Utility-first                                            │
│  • Mobile-first nativo                                      │
│  • Shadcn/ui para componentes                               │
│                                                             │
│  BANCO DE DADOS                                             │
│  ──────────────                                             │
│  Supabase                                                   │
│  • PostgreSQL gerenciado                                    │
│  • Auth built-in (se precisar)                              │
│  • Storage para imagens                                     │
│  • Free tier generoso                                       │
│                                                             │
│  PAGAMENTOS                                                 │
│  ──────────                                                 │
│  Stripe                                                     │
│  • Checkout hosted ou embedded                              │
│  • Webhooks para confirmação                                │
│  • Dashboard completo                                       │
│                                                             │
│  EMAIL                                                      │
│  ─────                                                      │
│  Resend                                                     │
│  • API simples                                              │
│  • React Email para templates                               │
│  • Free tier: 3k emails/mês                                 │
│                                                             │
│  HOSPEDAGEM                                                 │
│  ──────────                                                 │
│  Vercel                                                     │
│  • Deploy automático (GitHub)                               │
│  • Edge functions                                           │
│  • Analytics básico                                         │
│  • Free tier generoso                                       │
│                                                             │
│  AGENDAMENTO                                                │
│  ───────────                                                │
│  Cal.com (embed)                                            │
│  • Widget embeddável                                        │
│  • Sync com Google Calendar                                 │
│  • Self-hosted ou cloud                                     │
│                                                             │
│  CMS (para peças e blog)                                    │
│  ───                                                        │
│  Notion API ou Markdown + GitHub                            │
│  • Simples de editar                                        │
│  • Sem custo adicional                                      │
│  • Build regenera conteúdo                                  │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

**Prós**:
- ✅ Setup rápido (1-2 semanas para MVP)
- ✅ Menos código para manter
- ✅ Deploy simples (git push)
- ✅ Custo inicial zero
- ✅ Comunidade enorme (Next.js)
- ✅ Documentação excelente

**Contras**:
- ⚠️ Menos controle sobre performance
- ⚠️ Vendor lock-in parcial (Vercel)
- ⚠️ Pode ficar caro se escalar muito

**Custo estimado**:
- Início: R$ 0-50/mês
- Crescimento: R$ 200-400/mês

**Ideal para**: Lançar rápido, validar, iterar

---

### OPÇÃO B: Robusta e Escalável

**Filosofia**: Mais controle, otimização de performance, preparado para escala.

```
┌─────────────────────────────────────────────────────────────┐
│                    OPÇÃO B: ROBUSTA                         │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  FRONTEND                                                   │
│  ────────                                                   │
│  Astro                                                      │
│  • Zero JS por padrão                                       │
│  • Islands architecture                                     │
│  • Integra React onde precisa                               │
│  • Performance extrema                                      │
│                                                             │
│  INTERATIVIDADE                                             │
│  ─────────────                                              │
│  React (islands apenas onde necessário)                     │
│  • Checkout                                                 │
│  • Formulários                                              │
│  • Componentes interativos                                  │
│                                                             │
│  ESTILIZAÇÃO                                                │
│  ───────────                                                │
│  Tailwind CSS                                               │
│  • Mesmo que Opção A                                        │
│                                                             │
│  BACKEND (APIs)                                             │
│  ──────────────                                             │
│  Hono (ou Express)                                          │
│  • Lightweight                                              │
│  • TypeScript nativo                                        │
│  • Roda em Edge (Cloudflare Workers)                        │
│                                                             │
│  BANCO DE DADOS                                             │
│  ──────────────                                             │
│  Turso (SQLite distribuído)                                 │
│  • Réplicas globais                                         │
│  • Latência baixíssima                                      │
│  • Custo menor que PostgreSQL                               │
│  OU                                                         │
│  PlanetScale (MySQL serverless)                             │
│  • Branching de banco                                       │
│  • Escala automática                                        │
│                                                             │
│  PAGAMENTOS                                                 │
│  ──────────                                                 │
│  Stripe (mesmo)                                             │
│                                                             │
│  EMAIL                                                      │
│  ─────                                                      │
│  Resend (mesmo)                                             │
│                                                             │
│  HOSPEDAGEM                                                 │
│  ──────────                                                 │
│  Cloudflare Pages + Workers                                 │
│  • CDN global gratuito                                      │
│  • Workers para APIs (edge)                                 │
│  • Mais barato em escala                                    │
│  • Sem cold starts                                          │
│                                                             │
│  CMS                                                        │
│  ───                                                        │
│  Sanity ou Payload CMS                                      │
│  • Interface visual                                         │
│  • Preview em tempo real                                    │
│  • Mais profissional                                        │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

**Prós**:
- ✅ Performance máxima (100 Lighthouse)
- ✅ Menor custo em escala
- ✅ Sem vendor lock-in
- ✅ Mais controle
- ✅ Edge computing (mais rápido globalmente)

**Contras**:
- ⚠️ Setup mais complexo (3-4 semanas para MVP)
- ⚠️ Mais código para manter
- ⚠️ Comunidade menor (Astro)
- ⚠️ Curva de aprendizado maior

**Custo estimado**:
- Início: R$ 0-30/mês
- Crescimento: R$ 100-200/mês

**Ideal para**: Otimização de performance, controle total, escala

---

## 📊 Comparação Detalhada

### Tabela Comparativa

| Critério | Opção A (Next.js) | Opção B (Astro) |
|----------|-------------------|-----------------|
| **Tempo para MVP** | 1-2 semanas | 3-4 semanas |
| **Complexidade** | Média | Alta |
| **Performance** | Muito boa | Excelente |
| **SEO** | Excelente | Excelente |
| **Custo inicial** | R$ 0-50 | R$ 0-30 |
| **Custo em escala** | R$ 200-400 | R$ 100-200 |
| **Comunidade** | Enorme | Grande |
| **Documentação** | Excelente | Muito boa |
| **Flexibilidade** | Alta | Muito alta |
| **Manutenção** | Fácil | Média |
| **Vendor lock-in** | Parcial (Vercel) | Mínimo |

---

### Performance Esperada

| Métrica | Opção A | Opção B |
|---------|---------|---------|
| **LCP** (Largest Contentful Paint) | < 2.5s | < 1.5s |
| **FID** (First Input Delay) | < 100ms | < 50ms |
| **CLS** (Cumulative Layout Shift) | < 0.1 | < 0.05 |
| **Lighthouse Score** | 85-95 | 95-100 |
| **Bundle Size** | ~100-200KB | ~20-50KB |

---

### Curva de Aprendizado

| Tecnologia | Opção A | Opção B |
|------------|---------|---------|
| React | ✅ Usa | ✅ Usa (parcial) |
| Next.js | ✅ Core | ❌ Não usa |
| Astro | ❌ Não usa | ✅ Core |
| Tailwind | ✅ Usa | ✅ Usa |
| Supabase | ✅ Usa | ❌ Não usa |
| Turso/PlanetScale | ❌ Não usa | ✅ Usa |
| Vercel | ✅ Usa | ❌ Não usa |
| Cloudflare | ❌ Não usa | ✅ Usa |

---

## 🎯 Recomendação para Verde Barro

### Recomendo: **OPÇÃO A (Next.js + Vercel + Supabase)**

**Justificativa**:

1. **Velocidade de lançamento**
   - Verde Barro está começando
   - Validar produto é prioridade
   - 1-2 semanas vs 3-4 semanas faz diferença

2. **Checkout compartilhável**
   - É o diferencial do projeto
   - Next.js API Routes facilitam implementação
   - Server Components ajudam na UX

3. **Comunidade e suporte**
   - Mais tutoriais, exemplos, ajuda
   - Problemas são mais fáceis de resolver
   - Stripe + Next.js tem documentação oficial

4. **Custo-benefício**
   - Free tier cobre fase inicial
   - Escala bem para volume esperado
   - Custo só sobe se negócio crescer (bom problema)

5. **Simplicidade operacional**
   - Uma pessoa consegue manter
   - Deploy é git push
   - Menos coisas para dar errado

**Quando migrar para Opção B?**
- Se tiver > 10.000 visitas/mês
- Se custo de Vercel ficar proibitivo
- Se precisar de performance extrema
- Se quiser sair de vendor lock-in

---

## 📦 Stack Final Detalhada (Opção A)

```
┌─────────────────────────────────────────────────────────────┐
│              STACK VERDE BARRO (RECOMENDADA)                │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  FRAMEWORK                                                  │
│  ─────────                                                  │
│  Next.js 14 (App Router)                                    │
│  • TypeScript                                               │
│  • Server Components                                        │
│  • Server Actions                                           │
│  • API Routes                                               │
│                                                             │
│  UI / ESTILIZAÇÃO                                           │
│  ────────────────                                           │
│  • Tailwind CSS                                             │
│  • shadcn/ui (componentes)                                  │
│  • Framer Motion (animações)                                │
│  • Lucide Icons                                             │
│                                                             │
│  BANCO DE DADOS                                             │
│  ──────────────                                             │
│  Supabase                                                   │
│  • PostgreSQL                                               │
│  • Prisma como ORM                                          │
│  • Supabase Storage (imagens)                               │
│                                                             │
│  AUTENTICAÇÃO (se precisar admin)                           │
│  ─────────────                                              │
│  Supabase Auth                                              │
│  • Email/senha                                              │
│  • Magic link                                               │
│                                                             │
│  PAGAMENTOS                                                 │
│  ──────────                                                 │
│  Stripe                                                     │
│  • Checkout embedded                                        │
│  • Webhooks                                                 │
│  • stripe-js + @stripe/stripe-js                            │
│                                                             │
│  EMAIL                                                      │
│  ─────                                                      │
│  Resend                                                     │
│  • @react-email/components                                  │
│  • Templates em React                                       │
│                                                             │
│  AGENDAMENTO                                                │
│  ───────────                                                │
│  Cal.com                                                    │
│  • Embed widget                                             │
│  • API para integração                                      │
│                                                             │
│  ANALYTICS                                                  │
│  ─────────                                                  │
│  Vercel Analytics + Plausible                               │
│  • Web Vitals                                               │
│  • Pageviews                                                │
│  • Eventos customizados                                     │
│                                                             │
│  HOSPEDAGEM                                                 │
│  ──────────                                                 │
│  Vercel                                                     │
│  • Deploy automático                                        │
│  • Preview deployments                                      │
│  • Edge functions                                           │
│  • Domain + SSL                                             │
│                                                             │
│  CONTROLE DE VERSÃO                                         │
│  ──────────────────                                         │
│  GitHub                                                     │
│  • Repositório privado                                      │
│  • CI/CD com Vercel                                         │
│                                                             │
│  CMS (conteúdo)                                             │
│  ────                                                       │
│  Markdown + MDX (blog)                                      │
│  Supabase (peças autorais)                                  │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

---

## 📁 Estrutura de Pastas Sugerida

```
verde-barro/
├── app/                          # Next.js App Router
│   ├── (site)/                   # Grupo de rotas públicas
│   │   ├── page.tsx              # Home
│   │   ├── experiencias/
│   │   │   └── page.tsx
│   │   ├── pecas/
│   │   │   ├── page.tsx          # Catálogo
│   │   │   └── [slug]/
│   │   │       └── page.tsx      # Página da peça
│   │   ├── contato/
│   │   │   └── page.tsx
│   │   └── blog/
│   │       ├── page.tsx          # Lista de posts
│   │       └── [slug]/
│   │           └── page.tsx      # Post individual
│   │
│   ├── checkout/                 # Fluxo de checkout
│   │   ├── page.tsx              # Checkout individual
│   │   └── grupo/
│   │       └── [id]/
│   │           └── page.tsx      # Checkout compartilhável
│   │
│   ├── confirmacao/
│   │   └── [id]/
│   │       └── page.tsx          # Confirmação de pedido
│   │
│   ├── api/                      # API Routes
│   │   ├── checkout/
│   │   │   └── route.ts
│   │   ├── grupo/
│   │   │   ├── criar/
│   │   │   │   └── route.ts
│   │   │   └── [id]/
│   │   │       └── route.ts
│   │   ├── webhooks/
│   │   │   └── stripe/
│   │   │       └── route.ts
│   │   └── newsletter/
│   │       └── route.ts
│   │
│   ├── layout.tsx                # Layout raiz
│   └── globals.css               # Estilos globais
│
├── components/                   # Componentes React
│   ├── ui/                       # shadcn/ui
│   ├── layout/
│   │   ├── header.tsx
│   │   ├── footer.tsx
│   │   └── mobile-nav.tsx
│   ├── home/
│   ├── experiencias/
│   ├── checkout/
│   └── shared/
│
├── lib/                          # Utilitários
│   ├── supabase/
│   │   ├── client.ts
│   │   └── server.ts
│   ├── stripe.ts
│   ├── resend.ts
│   └── utils.ts
│
├── emails/                       # Templates de email
│   ├── confirmacao.tsx
│   ├── lembrete-grupo.tsx
│   └── pos-compra.tsx
│
├── content/                      # Conteúdo MDX (blog)
│   └── blog/
│       └── primeiro-post.mdx
│
├── public/                       # Assets estáticos
│   ├── images/
│   └── favicon.ico
│
├── prisma/                       # Schema do banco
│   └── schema.prisma
│
├── .env.local                    # Variáveis de ambiente
├── next.config.js
├── tailwind.config.js
├── tsconfig.json
└── package.json
```

---

## 💰 Orçamento Detalhado

### Fase 1: MVP (0-3 meses)

| Serviço | Plano | Custo/mês |
|---------|-------|-----------|
| Domínio | .com.br (anual) | ~R$ 7 |
| Vercel | Hobby (Free) | R$ 0 |
| Supabase | Free | R$ 0 |
| Stripe | Pay as you go | ~3.99% + R$ 0.39/tx |
| Resend | Free (3k/mês) | R$ 0 |
| Cal.com | Free | R$ 0 |
| Plausible | - | (usar Vercel Analytics free) |
| **Total fixo** | | **~R$ 7/mês** |

### Fase 2: Crescimento (3-12 meses)

| Serviço | Plano | Custo/mês |
|---------|-------|-----------|
| Domínio | .com.br | ~R$ 7 |
| Vercel | Pro | ~R$ 100 |
| Supabase | Pro | ~R$ 130 |
| Stripe | Pay as you go | ~3.99% + R$ 0.39/tx |
| Resend | Pro | ~R$ 100 |
| Cal.com | Team | ~R$ 60 |
| Plausible | Growth | ~R$ 50 |
| **Total fixo** | | **~R$ 450/mês** |

---

## 🔧 Configurações Iniciais

### Variáveis de Ambiente (.env.local)

```env
# App
NEXT_PUBLIC_APP_URL=https://verdebarro.com.br

# Supabase
NEXT_PUBLIC_SUPABASE_URL=https://xxx.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=xxx
SUPABASE_SERVICE_ROLE_KEY=xxx

# Stripe
STRIPE_SECRET_KEY=sk_live_xxx
NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY=pk_live_xxx
STRIPE_WEBHOOK_SECRET=whsec_xxx

# Resend
RESEND_API_KEY=re_xxx

# Cal.com
CAL_API_KEY=xxx
```

---

### Camada 3: Trade-offs e Validação

#### Trade-offs Aceitos

**1. Vercel vendor lock-in**
- **Aceitamos**: Facilidade > liberdade total
- **Mitigação**: Next.js roda em outras plataformas se necessário

**2. Supabase vs banco próprio**
- **Aceitamos**: Velocidade > controle total
- **Mitigação**: PostgreSQL é padrão, migração possível

**3. Custo em escala**
- **Aceitamos**: Pagar mais se crescer é bom problema
- **Mitigação**: Monitorar custos, migrar se necessário

#### Validação

**Checklist pré-implementação**:
- [ ] Criar conta Vercel
- [ ] Criar conta Supabase
- [ ] Criar conta Stripe (com documentos)
- [ ] Criar conta Resend
- [ ] Registrar domínio
- [ ] Criar repositório GitHub

---

## ✅ Checklist da Lição

- [x] Conceitos de stack explicados
- [x] Requisitos do projeto mapeados
- [x] Opção A (simples) detalhada
- [x] Opção B (robusta) detalhada
- [x] Comparação entre opções
- [x] Recomendação justificada
- [x] Stack final detalhada
- [x] Estrutura de pastas definida
- [x] Orçamento detalhado
- [x] Configurações iniciais listadas
- [x] Decisão do usuário registrada (DEC-019)
- [x] Arquitetura híbrida documentada
- [x] Schema do banco definido
- [x] Logs atualizados

---

## ✅ Decisão Tomada

**Escolha**: **Opção A com Arquitetura Híbrida (Notion + Supabase)**

**Stack final**:
- **Framework**: Next.js 14 + Vercel
- **Banco de dados**: Supabase (operações críticas)
- **CMS**: Notion API (conteúdo)
- **Pagamentos**: Stripe
- **Email**: Resend

---

## 📦 Stack Final — Arquitetura Híbrida

```
┌─────────────────────────────────────────────────────────────┐
│            STACK VERDE BARRO (HÍBRIDA)                      │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  FRAMEWORK                                                  │
│  ─────────                                                  │
│  Next.js 14 (App Router)                                    │
│  • TypeScript                                               │
│  • Server Components                                        │
│  • API Routes                                               │
│                                                             │
│  UI / ESTILIZAÇÃO                                           │
│  ────────────────                                           │
│  • Tailwind CSS                                             │
│  • shadcn/ui (componentes)                                  │
│  • Framer Motion (animações)                                │
│  • Lucide Icons                                             │
│                                                             │
│  NOTION (CMS — conteúdo)                                    │
│  ──────────────────────                                     │
│  ✅ Catálogo de peças autorais                              │
│  ✅ Posts do blog                                           │
│  ✅ Depoimentos de clientes                                 │
│  ✅ FAQ                                                     │
│  ❌ NÃO usar para: checkout, pagamentos, dados tempo real   │
│                                                             │
│  SUPABASE (Banco — operações críticas)                      │
│  ─────────────────────────────────────                      │
│  ✅ Pedidos de experiências                                 │
│  ✅ Links de checkout compartilhável                        │
│  ✅ Status de pagamentos                                    │
│  ✅ Newsletter subscribers                                  │
│  ✅ Logs de webhooks                                        │
│                                                             │
│  SYNC: Supabase → Notion (opcional)                         │
│  ─────────────────────────────────                          │
│  • Webhook Stripe confirma pagamento                        │
│  • Supabase salva pedido                                    │
│  • Função cria registro no Notion (seu controle)            │
│                                                             │
│  PAGAMENTOS                                                 │
│  ──────────                                                 │
│  Stripe                                                     │
│  • Checkout embedded                                        │
│  • Webhooks → Supabase                                      │
│                                                             │
│  EMAIL                                                      │
│  ─────                                                      │
│  Resend                                                     │
│  • Templates em React                                       │
│                                                             │
│  AGENDAMENTO                                                │
│  ───────────                                                │
│  Cal.com (embed)                                            │
│                                                             │
│  HOSPEDAGEM                                                 │
│  ──────────                                                 │
│  Vercel                                                     │
│  • Deploy automático                                        │
│  • Edge functions                                           │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

---

## 📁 Estrutura de Pastas Atualizada

```
verde-barro/
├── app/
│   ├── (site)/
│   │   ├── page.tsx              # Home
│   │   ├── experiencias/
│   │   ├── pecas/
│   │   │   ├── page.tsx          # Lista (dados do Notion)
│   │   │   └── [slug]/page.tsx   # Detalhe (dados do Notion)
│   │   ├── contato/
│   │   └── blog/
│   │       ├── page.tsx          # Lista (dados do Notion)
│   │       └── [slug]/page.tsx   # Post (dados do Notion)
│   │
│   ├── checkout/
│   │   ├── page.tsx              # Checkout individual
│   │   └── grupo/[id]/page.tsx   # Checkout compartilhável
│   │
│   ├── api/
│   │   ├── checkout/route.ts           # Cria sessão Stripe
│   │   ├── grupo/
│   │   │   ├── criar/route.ts          # Cria link grupo
│   │   │   └── [id]/route.ts           # Status do grupo
│   │   ├── webhooks/
│   │   │   └── stripe/route.ts         # Recebe confirmação
│   │   └── newsletter/route.ts         # Inscrição
│   │
│   ├── layout.tsx
│   └── globals.css
│
├── lib/
│   ├── notion.ts                 # Cliente Notion API
│   ├── supabase/
│   │   ├── client.ts             # Cliente browser
│   │   └── server.ts             # Cliente servidor
│   ├── stripe.ts
│   └── resend.ts
│
├── components/
├── emails/
└── public/
```

---

## 🔗 Fluxos de Dados

### Conteúdo (Notion → Site)
```
1. Build do site (ou request)
2. Next.js chama Notion API
3. Notion retorna dados (peças, posts, depoimentos)
4. Site renderiza

Latência aceitável: Conteúdo pode cachear
```

### Experiências (Agendamento → Confirmação → Pagamento)

```
ETAPA 1: CLIENTE SOLICITA
─────────────────────────
[Cliente]                           [Site]                      [Supabase]
    │                                  │                             │
    │ Preenche formulário:             │                             │
    │ • Experiência                    │                             │
    │ • Data desejada                  │                             │
    │ • Nº pessoas                     │                             │
    │ • Endereço                       │                             │
    │ • Dados contato                  │                             │
    │ • Tipo pagamento                 │                             │
    │                                  │                             │
    │ ─────────────────────────────────►                             │
    │                                  │ API Route                   │
    │                                  │ ──────────────────────────► │
    │                                  │                             │ INSERT
    │                                  │                             │ solicitacoes_experiencias
    │                                  │                             │ (status: 'pendente')
    │                                  │                             │
    │ ◄─────────────────────────────────                             │
    │ "Obrigada! Entraremos em         │                             │
    │  contato em breve."              │                             │
    │                                  │                             │
    │                    [Email para você: nova solicitação!]        │


ETAPA 2: VOCÊ CONFIRMA (manual ou via admin)
────────────────────────────────────────────
[Você]                              [Admin/WhatsApp]            [Supabase]
    │                                  │                             │
    │ Analisa solicitação:             │                             │
    │ • Disponibilidade ok?            │                             │
    │ • Região atendida?               │                             │
    │ • Dados corretos?                │                             │
    │                                  │                             │
    │ Confirma e define valor          │                             │
    │ ─────────────────────────────────►                             │
    │                                  │                             │ UPDATE
    │                                  │                             │ status = 'confirmado'
    │                                  │                             │ valor_total = X
    │                                  │                             │
    │                                  │                             │ Se compartilhado:
    │                                  │                             │ INSERT grupos
    │                                  │                             │
    │                    [Email para cliente: link de pagamento]     │


ETAPA 3: CLIENTE PAGA
─────────────────────
[Cliente]                           [Site]                      [Stripe]
    │                                  │                             │
    │ Clica no link do email           │                             │
    │ ─────────────────────────────────►                             │
    │                                  │ Exibe resumo + botão pagar  │
    │                                  │                             │
    │ Clica "Pagar"                    │                             │
    │ ─────────────────────────────────►                             │
    │                                  │ Cria Checkout Session ─────►│
    │                                  │                             │
    │ ◄───────────────────────────────────────────────────────────────
    │ Redirect para Stripe             │                             │
    │                                  │                             │
    │ Paga no Stripe                   │                             │
    │ ──────────────────────────────────────────────────────────────►│
    │                                  │                             │
    │                                  │         Webhook ◄───────────│
    │                                  │                             │
    │                                  │ [Supabase]                  │
    │                                  │ UPDATE status = 'pago'      │
    │                                  │ INSERT pedidos_experiencias │
    │                                  │                             │
    │ ◄─────────────────────────────────                             │
    │ "Pagamento confirmado!"          │                             │
    │                                  │                             │
    │                    [Email: confirmação final]                  │
```

### Experiências com Pagamento Compartilhado

```
APÓS CONFIRMAÇÃO (você):
────────────────────────
→ Sistema cria registro em `grupos`
→ Email para organizador com link: /pagar/grupo/{id}

ORGANIZADOR COMPARTILHA LINK:
─────────────────────────────
→ WhatsApp, Instagram, etc.

CADA PARTICIPANTE ACESSA:
─────────────────────────
→ Vê: quem organizou, experiência, valor, quem já pagou
→ Paga sua parte
→ Webhook atualiza `grupo_participantes`
→ Página atualiza em tempo real (Supabase Realtime)

GRUPO COMPLETO:
───────────────
→ Todos pagaram
→ Email para você: "Grupo completo, experiência confirmada!"
→ INSERT em `pedidos_experiencias`
```

### Peças Autorais (Checkout Direto)

```
[Cliente]                           [Site]                      [Stripe]
    │                                  │                             │
    │ Adiciona peça ao carrinho        │                             │
    │ Preenche dados + endereço        │                             │
    │ Clica "Pagar"                    │                             │
    │ ─────────────────────────────────►                             │
    │                                  │ [Supabase]                  │
    │                                  │ INSERT pedidos_pecas        │
    │                                  │ (status: 'pendente')        │
    │                                  │                             │
    │                                  │ Cria Checkout Session ─────►│
    │                                  │                             │
    │ Redirect para Stripe             │                             │
    │ Paga                             │                             │
    │                                  │         Webhook ◄───────────│
    │                                  │ UPDATE status = 'pago'      │
    │                                  │ Gera cupom 20%              │
    │                                  │                             │
    │                    [Email: confirmação + cupom]                │
```

---

## 🔧 Variáveis de Ambiente

```env
# App
NEXT_PUBLIC_APP_URL=https://verdebarro.com.br

# Notion
NOTION_API_KEY=secret_xxx
NOTION_DATABASE_PECAS=xxx
NOTION_DATABASE_BLOG=xxx
NOTION_DATABASE_DEPOIMENTOS=xxx

# Supabase
NEXT_PUBLIC_SUPABASE_URL=https://xxx.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=xxx
SUPABASE_SERVICE_ROLE_KEY=xxx

# Stripe
STRIPE_SECRET_KEY=sk_live_xxx
NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY=pk_live_xxx
STRIPE_WEBHOOK_SECRET=whsec_xxx

# Resend
RESEND_API_KEY=re_xxx

# Cal.com
NEXT_PUBLIC_CAL_LINK=verdebarro
```

---

## 💾 Schema do Banco (Supabase)

### Visão Geral das Tabelas

| Tabela | Propósito |
|--------|-----------|
| `solicitacoes_experiencias` | Agendamentos de experiências (pré-pagamento) |
| `pedidos_experiencias` | Experiências confirmadas e pagas |
| `pedidos_pecas` | Compras de peças autorais |
| `grupos` | Links de checkout compartilhável |
| `grupo_participantes` | Participantes de cada grupo |
| `newsletter` | Inscritos na newsletter |
| `cupons` | Cupons de desconto (automáticos e promocionais) |
| `cupons_uso` | Histórico de uso de cupons |

### Fluxo de Venda de Experiências (ATUALIZADO)

```
┌─────────────────────────────────────────────────────────────┐
│     FLUXO: EXPERIÊNCIA (Agendamento antes do pagamento)     │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  1. CLIENTE SOLICITA                                        │
│     ─────────────────                                       │
│     • Escolhe experiência (modelagem/pintura)               │
│     • Seleciona data desejada (agenda disponível)           │
│     • Informa número de participantes (2-8)                 │
│     • Informa endereço do workshop                          │
│     • Escolhe: "vou pagar por todos" ou "dividir"           │
│     • Preenche dados de contato                             │
│                                                             │
│     → Cria registro em `solicitacoes_experiencias`          │
│       (status: 'pendente')                                  │
│                                                             │
│  2. VOCÊ RECEBE E ANALISA                                   │
│     ──────────────────────                                  │
│     • Notificação por email/WhatsApp                        │
│     • Verifica disponibilidade real                         │
│     • Verifica se atende a região                           │
│     • Entra em contato com cliente se necessário            │
│                                                             │
│  3. VOCÊ CONFIRMA                                           │
│     ─────────────────                                       │
│     • Atualiza `solicitacoes_experiencias`                  │
│       (status: 'confirmado')                                │
│     • Sistema gera link de pagamento                        │
│     • Email automático para cliente com link                │
│                                                             │
│  4. CLIENTE PAGA                                            │
│     ─────────────                                           │
│     • Acessa link de pagamento                              │
│     • Stripe processa                                       │
│     • Webhook atualiza (status: 'pago')                     │
│     • Cria registro em `pedidos_experiencias`               │
│                                                             │
│  5. PÓS-PAGAMENTO                                           │
│     ──────────────                                          │
│     • Email de confirmação final                            │
│     • (Opcional) Sync para Notion                           │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

### Schema SQL

```sql
-- ============================================================
-- SOLICITAÇÕES DE EXPERIÊNCIAS (antes do pagamento)
-- ============================================================
CREATE TABLE solicitacoes_experiencias (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  
  -- Experiência
  experiencia TEXT NOT NULL, -- 'modelagem' | 'pintura' | 'ambos'
  num_pessoas INTEGER NOT NULL CHECK (num_pessoas >= 2 AND num_pessoas <= 8),
  
  -- Agendamento desejado
  data_desejada DATE NOT NULL,
  horario_desejado TEXT, -- 'manha' | 'tarde' | 'noite' | horário específico
  
  -- Local
  endereco_cep TEXT NOT NULL,
  endereco_rua TEXT NOT NULL,
  endereco_numero TEXT NOT NULL,
  endereco_complemento TEXT,
  endereco_bairro TEXT NOT NULL,
  endereco_cidade TEXT NOT NULL,
  
  -- Dados do solicitante
  nome TEXT NOT NULL,
  email TEXT NOT NULL,
  whatsapp TEXT NOT NULL,
  
  -- Forma de pagamento escolhida
  tipo_pagamento TEXT NOT NULL, -- 'individual' | 'compartilhado'
  
  -- Observações do cliente
  observacoes TEXT,
  
  -- Status do fluxo
  status TEXT DEFAULT 'pendente', 
  -- 'pendente' → aguardando sua análise
  -- 'confirmado' → você confirmou, link de pagamento enviado
  -- 'pago' → cliente pagou (vira pedido)
  -- 'recusado' → você recusou (fora de área, sem disponibilidade)
  -- 'expirado' → cliente não pagou no prazo
  -- 'cancelado' → cancelado por qualquer motivo
  
  -- Valor calculado (preenchido por você na confirmação)
  valor_total DECIMAL(10,2),
  valor_por_pessoa DECIMAL(10,2),
  
  -- Link de pagamento (gerado após confirmação)
  link_pagamento_id UUID, -- referência para grupos (se compartilhado)
  stripe_session_id TEXT, -- se pagamento individual
  
  -- Motivo (se recusado)
  motivo_recusa TEXT,
  
  -- Metadata
  created_at TIMESTAMP DEFAULT NOW(),
  updated_at TIMESTAMP DEFAULT NOW(),
  confirmado_em TIMESTAMP,
  pago_em TIMESTAMP
);

-- ============================================================
-- PEDIDOS DE EXPERIÊNCIAS (após pagamento confirmado)
-- ============================================================
CREATE TABLE pedidos_experiencias (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  
  -- Referência à solicitação original
  solicitacao_id UUID REFERENCES solicitacoes_experiencias(id),
  
  -- Dados da experiência (copiados para histórico)
  experiencia TEXT NOT NULL,
  num_pessoas INTEGER NOT NULL,
  data_agendada DATE NOT NULL,
  horario TEXT,
  endereco JSONB NOT NULL,
  
  -- Dados do comprador
  nome TEXT NOT NULL,
  email TEXT NOT NULL,
  whatsapp TEXT NOT NULL,
  
  -- Pagamento
  tipo_pagamento TEXT NOT NULL, -- 'individual' | 'compartilhado'
  valor_total DECIMAL(10,2) NOT NULL,
  stripe_payment_intent TEXT,
  
  -- Status
  status TEXT DEFAULT 'confirmado',
  -- 'confirmado' → pago, aguardando realização
  -- 'realizado' → experiência aconteceu
  -- 'cancelado' → cancelado após pagamento (reembolso)
  
  -- Metadata
  created_at TIMESTAMP DEFAULT NOW(),
  realizado_em TIMESTAMP
);

-- ============================================================
-- PEDIDOS DE PEÇAS AUTORAIS
-- ============================================================
CREATE TABLE pedidos_pecas (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  
  -- Itens (pode ser mais de uma peça)
  itens JSONB NOT NULL, -- [{peca_id, nome, preco, quantidade}]
  valor_subtotal DECIMAL(10,2) NOT NULL,
  valor_frete DECIMAL(10,2) NOT NULL,
  valor_total DECIMAL(10,2) NOT NULL,
  
  -- Dados do comprador
  nome TEXT NOT NULL,
  email TEXT NOT NULL,
  whatsapp TEXT,
  
  -- Endereço de entrega
  endereco_cep TEXT NOT NULL,
  endereco_rua TEXT NOT NULL,
  endereco_numero TEXT NOT NULL,
  endereco_complemento TEXT,
  endereco_bairro TEXT NOT NULL,
  endereco_cidade TEXT NOT NULL,
  endereco_estado TEXT NOT NULL,
  
  -- Pagamento
  stripe_session_id TEXT,
  stripe_payment_intent TEXT,
  
  -- Status
  status TEXT DEFAULT 'pendente',
  -- 'pendente' → aguardando pagamento
  -- 'pago' → pago, preparando envio
  -- 'enviado' → enviado (tem código de rastreio)
  -- 'entregue' → entregue
  -- 'cancelado' → cancelado
  
  -- Envio
  codigo_rastreio TEXT,
  enviado_em TIMESTAMP,
  
  -- Metadata
  created_at TIMESTAMP DEFAULT NOW(),
  pago_em TIMESTAMP
);

-- ============================================================
-- GRUPOS (checkout compartilhável)
-- ============================================================
CREATE TABLE grupos (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  
  -- Referência à solicitação
  solicitacao_id UUID REFERENCES solicitacoes_experiencias(id),
  
  -- Config do grupo
  num_vagas INTEGER NOT NULL,
  valor_por_pessoa DECIMAL(10,2) NOT NULL,
  
  -- Validade
  expira_em TIMESTAMP NOT NULL,
  
  -- Status
  status TEXT DEFAULT 'aberto',
  -- 'aberto' → aguardando participantes
  -- 'completo' → todos pagaram
  -- 'parcial_pago' → alguns pagaram, organizador finalizou
  -- 'expirado' → prazo expirou
  -- 'cancelado' → cancelado
  
  created_at TIMESTAMP DEFAULT NOW()
);

-- ============================================================
-- PARTICIPANTES DO GRUPO
-- ============================================================
CREATE TABLE grupo_participantes (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  grupo_id UUID REFERENCES grupos(id),
  
  -- Dados do participante
  nome TEXT NOT NULL,
  email TEXT NOT NULL,
  whatsapp TEXT,
  
  -- Pagamento
  stripe_payment_intent TEXT,
  pago BOOLEAN DEFAULT FALSE,
  pago_em TIMESTAMP,
  
  -- É o organizador?
  is_organizador BOOLEAN DEFAULT FALSE,
  
  created_at TIMESTAMP DEFAULT NOW()
);

-- ============================================================
-- NEWSLETTER
-- ============================================================
CREATE TABLE newsletter (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  email TEXT UNIQUE NOT NULL,
  nome TEXT,
  origem TEXT, -- 'home' | 'footer' | 'blog' | 'checkout'
  created_at TIMESTAMP DEFAULT NOW()
);

-- ============================================================
-- CUPONS (gestão centralizada)
-- ============================================================
CREATE TABLE cupons (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  codigo TEXT UNIQUE NOT NULL, -- ex: 'PECA-A1B2C3' ou 'INFLUENCER-MARIA'
  
  -- Tipo e origem
  tipo TEXT NOT NULL,
  -- 'peca_autoral' → gerado automaticamente na compra de peça
  -- 'promocional' → campanha sazonal (Dia das Mães, Natal)
  -- 'influenciadora' → parceria com influenciadoras
  -- 'indicacao' → programa de indicação (futuro)
  
  -- Referência de origem (se aplicável)
  pedido_peca_id UUID REFERENCES pedidos_pecas(id), -- se veio de compra de peça
  influenciadora_nome TEXT, -- se for parceria
  campanha_nome TEXT, -- se for promocional
  
  -- Desconto
  desconto_tipo TEXT NOT NULL DEFAULT 'percentual', -- 'percentual' | 'valor_fixo'
  desconto_valor DECIMAL(10,2) NOT NULL, -- 20 (%) ou 50.00 (R$)
  
  -- Onde pode usar
  aplica_em TEXT NOT NULL, 
  -- 'experiencias' | 'pecas' | 'tudo'
  
  -- Restrições
  valor_minimo DECIMAL(10,2), -- valor mínimo do pedido (NULL = sem mínimo)
  
  -- Validade
  valido_de TIMESTAMP DEFAULT NOW(),
  valido_ate TIMESTAMP NOT NULL, -- OBRIGATÓRIO: sempre ter data de expiração
  
  -- Limite de uso
  uso_maximo INTEGER DEFAULT 1, -- 1 = uso único, NULL = ilimitado
  uso_atual INTEGER DEFAULT 0,
  
  -- Status
  status TEXT DEFAULT 'ativo',
  -- 'ativo' → pode ser usado
  -- 'usado' → atingiu uso_maximo
  -- 'expirado' → passou da valido_ate
  -- 'cancelado' → cancelado manualmente
  
  -- Metadata
  created_at TIMESTAMP DEFAULT NOW(),
  updated_at TIMESTAMP DEFAULT NOW()
);

-- ============================================================
-- HISTÓRICO DE USO DE CUPONS
-- ============================================================
CREATE TABLE cupons_uso (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  cupom_id UUID REFERENCES cupons(id) NOT NULL,
  
  -- Onde foi usado (um dos dois)
  solicitacao_id UUID REFERENCES solicitacoes_experiencias(id),
  pedido_peca_id UUID REFERENCES pedidos_pecas(id),
  
  -- Detalhes do uso
  valor_original DECIMAL(10,2) NOT NULL, -- valor antes do desconto
  valor_desconto DECIMAL(10,2) NOT NULL, -- quanto descontou
  valor_final DECIMAL(10,2) NOT NULL, -- valor após desconto
  
  -- Metadata
  usado_em TIMESTAMP DEFAULT NOW()
);

-- ============================================================
-- ÍNDICES
-- ============================================================
CREATE INDEX idx_solicitacoes_status ON solicitacoes_experiencias(status);
CREATE INDEX idx_solicitacoes_email ON solicitacoes_experiencias(email);
CREATE INDEX idx_solicitacoes_data ON solicitacoes_experiencias(data_desejada);

CREATE INDEX idx_pedidos_exp_status ON pedidos_experiencias(status);
CREATE INDEX idx_pedidos_exp_email ON pedidos_experiencias(email);

CREATE INDEX idx_pedidos_pecas_status ON pedidos_pecas(status);
CREATE INDEX idx_pedidos_pecas_email ON pedidos_pecas(email);

CREATE INDEX idx_grupos_status ON grupos(status);
CREATE INDEX idx_grupos_expira ON grupos(expira_em);

CREATE INDEX idx_cupons_codigo ON cupons(codigo);
CREATE INDEX idx_cupons_status ON cupons(status);
CREATE INDEX idx_cupons_tipo ON cupons(tipo);
CREATE INDEX idx_cupons_validade ON cupons(valido_ate);
```

---

## 🎟️ Regras de Negócio: Cupons

### Cupom Automático (Compra de Peça)

| Regra | Valor |
|-------|-------|
| **Gatilho** | Cliente paga por peça autoral |
| **Desconto** | 20% |
| **Aplica em** | Experiências |
| **Validade** | 2 meses a partir da compra |
| **Uso máximo** | 1 vez |
| **Código** | `PECA-{6 chars aleatórios}` |

**Fluxo automático**:
```
1. Webhook Stripe confirma pagamento de peça
2. Sistema gera código único
3. INSERT em `cupons`:
   - tipo: 'peca_autoral'
   - desconto_valor: 20
   - valido_ate: NOW() + 2 meses
   - pedido_peca_id: {id do pedido}
4. Email para cliente com código do cupom
```

### Cupom de Influenciadora

| Regra | Valor |
|-------|-------|
| **Criação** | Manual (você cria) |
| **Desconto** | Definido por parceria (ex: 15%) |
| **Aplica em** | Experiências ou Peças |
| **Validade** | Definido por parceria |
| **Uso máximo** | Ilimitado ou limitado |
| **Código** | `{NOME}-{SUFIXO}` (ex: MARIA15) |

**Exemplo de criação**:
```sql
INSERT INTO cupons (
  codigo, tipo, desconto_tipo, desconto_valor,
  aplica_em, valido_ate, uso_maximo, influenciadora_nome
) VALUES (
  'MARIA15', 
  'influenciadora', 
  'percentual', 
  15,
  'experiencias',
  '2025-06-30', -- validade da parceria
  NULL, -- ilimitado
  'Maria Influenciadora'
);
```

### Cupom Promocional (Campanhas)

| Regra | Valor |
|-------|-------|
| **Criação** | Manual (você cria) |
| **Desconto** | Variável |
| **Aplica em** | Definido por campanha |
| **Validade** | Período da campanha |
| **Uso máximo** | Variável |
| **Código** | Temático (ex: MAES2025, NATAL10) |

---

## 🔄 Fluxo: Aplicar Cupom no Checkout

```
[Cliente]                      [Site]                        [Supabase]
    │                            │                               │
    │ Digita código "MARIA15"    │                               │
    │ ──────────────────────────►│                               │
    │                            │ SELECT * FROM cupons          │
    │                            │ WHERE codigo = 'MARIA15'      │
    │                            │ ─────────────────────────────►│
    │                            │                               │
    │                            │ Valida:                       │
    │                            │ • status = 'ativo'?           │
    │                            │ • valido_ate > NOW()?         │
    │                            │ • uso_atual < uso_maximo?     │
    │                            │ • aplica_em compatível?       │
    │                            │ • valor >= valor_minimo?      │
    │                            │                               │
    │ ◄────────────────────────────────────────────────────────────
    │ "Cupom válido! -15%"       │                               │
    │                            │                               │
    │ Finaliza compra            │                               │
    │ ──────────────────────────►│                               │
    │                            │ INSERT cupons_uso             │
    │                            │ UPDATE cupons SET uso_atual++ │
    │                            │ ─────────────────────────────►│
```

---

**Última atualização**: 2025-01-30
