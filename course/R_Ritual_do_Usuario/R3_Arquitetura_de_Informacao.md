# Lição R3 — Arquitetura de Informação (Sitemap)

> **Fase**: R — Ritual do Usuário  
> **Status**: ✅ Concluída  
> **Data de início**: 2025-01-28  
> **Data de conclusão**: 2025-01-28

---

## 🎯 Objetivo da Lição

Definir a **arquitetura de informação** (sitemap) do site Verde Barro, estabelecendo uma estrutura **mobile-first**, **simplificada** e **orientada a conversão**, adaptada ao comportamento digital do público-alvo e às dinâmicas atuais de creator economy e redes sociais.

---

## 📚 Conceitos-Chave (3 Camadas)

### Camada 1: Definição Simples

**Arquitetura de Informação Moderna** é a estrutura de páginas do site pensada para o comportamento digital atual: mobile-first, atenção fragmentada, entrada via redes sociais e conversão rápida.

**Princípios fundamentais**:
- **Mobile-first**: 90%+ do tráfego virá de celular via redes sociais
- **Simplicidade radical**: Menos páginas, mais foco, sem confundir
- **Funil direto**: Cada página guia para conversão clara
- **Prova social nativa**: Autoridade via redes sociais, não via blog tradicional
- **Conversão sem atrito**: WhatsApp como canal principal, sem formulários complexos

**Componentes**:
- **Sitemap enxuto**: Apenas páginas essenciais
- **Navegação intuitiva**: Máximo 5 itens no menu
- **CTAs claros**: Um CTA principal por página
- **Fluxos curtos**: Máximo 2-3 cliques até conversão

**Por que é crítico**:
- Define experiência de navegação
- Guia desenvolvimento do site
- Impacta SEO (estrutura de URLs)
- Facilita conversão (fluxos claros)

---

### Camada 2: Aplicação no Caso Verde Barro

**Contexto do público-alvo**:
- Mulheres jovens (25-35 anos)
- Moradoras de São Paulo
- Médio a alto poder aquisitivo
- Acostumadas a cultura e luxuosidade
- Alta propensão a redes sociais (Instagram e TikTok)
- Antenadas em trends comportamentais, moda e novas experiências
- Consomem conteúdo em vídeos curtos, não em blogs
- Tomam decisões rápidas quando algo ressoa emocionalmente

**Comportamento digital**:
- Entrada principal via Instagram e TikTok (stories, reels, tiktoks)
- Navegação 90% mobile
- Baixa tolerância a fricção ou confusão
- Valorizam estética, narrativa e autenticidade
- Confiam em prova social (depoimentos, UGC, influencers)
- Preferem WhatsApp a formulários de contato

**Contexto de negócio**:
- Core: Workshops de cerâmica na casa do cliente (apenas São Paulo)
- Secundário: Peças autorais (entrega para todo Brasil)
- Combo: Peça = cupom 20% desconto no workshop
- Autoridade: Blog (conceitos de cerâmica, workshop e pintura) para SEO/confiança
- Conversão: WhatsApp + agendamento + checkout
- Funil: TOFU → MOFU → BOFU → Pós-conversão
- Newsletter para comunidade e lista de espera

---

**Objetivos do site**:
1. **Institucional**: Apresentar Verde Barro, proposta de valor, posicionamento
2. **Venda**: Converter workshops e peças autorais
3. **Autoridade**: Redes sociais e prova social no site.
4. **Conversão**: Múltiplos canais (WhatsApp, agendamento, checkout)

**Análise Estratégica da Arquitetura**:

**Sobre Blog tradicional**:
- ❌ Público-alvo não consome blog (consome reels, stories, tiktoks)
- ❌ Tempo de produção alto, retorno incerto para esse perfil
- ✅ Pode funcionar para SEO/Google (mas escondido, não no menu principal)
- ✅ Pode funcionar para LLMs (indexação de conteúdo)
- **Decisão**: Blog existe apenas para SEO, fora da navegação principal. Autoridade é construída via redes sociais e prova social no site.

**Sobre página de Contato com formulário**:
- ❌ Público-alvo não preenche formulários
- ❌ Email é canal secundário para esse perfil
- ✅ WhatsApp é o canal natural de conversação
- ✅ Chamada de vídeo demonstra premium e personalização
- **Decisão**: Contato via WhatsApp e agendamento de chamada de vídeo. Sem formulário tradicional.

**Sobre FAQ separado**:
- ❌ Público-alvo não navega até página de FAQ
- ❌ Fragmenta informação necessária
- ✅ FAQ deve estar integrado nas páginas de Experiências e Peças
- **Decisão**: FAQ integrado nas páginas relevantes, não separado.

**Sobre autoridade e validação**:
- ❌ Blog não é eficiente para esse público
- ✅ Prova social nativa (depoimentos, fotos, vídeos de clientes)
- ✅ Destaque para redes sociais (seguidores, engajamento)
- ✅ UGC (User Generated Content)
- ✅ Newsletter como canal de relacionamento e comunidade
- **Decisão**: Autoridade via prova social, redes sociais e newsletter. Blog apenas para SEO.

---

**Referência de Estrutura: [meubenza.com.br](https://meubenza.com.br/)**

Aprendizados da referência:
- Estrutura ultra-simples (Home + Produto + Comprar)
- Narrativa cativante no hero ("o seu novo jeito de usar azeite")
- CTAs claros e diretos
- Foco no funil (não distrai)
- Design mobile-first
- Newsletter para comunidade
- Prova social integrada (não em página separada)
- Sem blog no menu principal
- Contato simplificado (footer, sem página dedicada complexa)

**Adaptação para Verde Barro**:
- Diferença: Verde Barro vende experiência (serviço) + produto
- Diferença: Experiências apenas em São Paulo
- Diferença: Peças autorais para todo Brasil
- Diferença: Precisa de agendamento (não apenas checkout de produto)
- Mantém: Estrutura simples, narrativa, CTAs claros, mobile-first

---

**SITEMAP FINAL — Verde Barro**:

```
/
├── / (Home)
│   └── Narrativa completa, sobre fundadora, história, proposta de valor,
│       direcionamento para ofertas, CTAs principais, newsletter
│
├── /experiencias (Experiências)
│   └── Workshops de cerâmica em casa (apenas SP), como funciona,
│       o que está incluso, FAQ integrado, preços, agendamento,
│       prova social, CTA principal
│
├── /pecas (Peças Autorais)
│   └── Catálogo de peças, história das peças, combo com workshop,
│       FAQ integrado, compra, entrega para todo Brasil
│
├── /contato (Contato)
│   └── WhatsApp direto, agendamento de chamada de vídeo,
│       direcionamento para redes sociais (Instagram, TikTok),
│       sem formulário, sem FAQ
│
├── /blog (Blog — SEO only, fora do menu - footer only)
│   └── Artigos para SEO e indexação em LLMs,
│       não aparece na navegação principal
│
└── /legal (Páginas Utilitárias — footer only)
    ├── /politica-privacidade
    └── /termos-uso
```

**Total de páginas no menu principal**: 4 (Home, Experiências, Peças, Contato)

---

**Navegação Principal (Header)**:
```
Logo | Experiências | Peças Autorais | Contato | [CTA: Agendar/WhatsApp]
```

**Navegação Secundária (Footer)**:
```
Links:              Redes:              Legal:
- Experiências      - Instagram         - Política Privacidade
- Peças Autorais    - TikTok            - Termos de Uso
- Contato           
- Blog (SEO)        Newsletter: [input email]
```

---

**Fluxos de Conversão Simplificados**:

**Fluxo 1: Workshop (Core)**
```
Instagram/TikTok → Home (narrativa) → Experiências → Agendar (WhatsApp)
```

**Fluxo 2: Presente**
```
Instagram/TikTok → Home → Experiências (seção presentear) → Agendar (WhatsApp)
```

**Fluxo 3: Peça Autoral → Workshop**
```
Instagram/TikTok → Home → Peças Autorais → Comprar → Cupom 20% → Experiências
```

**Fluxo 4: SEO/LLM (secundário)**
```
Google/ChatGPT → Blog (artigo) → CTA → Experiências ou Peças
```

---

### Camada 3: Trade-offs, Riscos, Anti-padrões e Validação

#### Trade-offs

**1. Estrutura ultra-simples vs Estrutura completa**
- **Escolha**: Ultra-simples (4 páginas principais)
- **Trade-off**: Menos conteúdo detalhado
- **Justificativa**: Público-alvo tem atenção fragmentada, prefere simplicidade

**2. Blog escondido vs Blog no menu**
- **Escolha**: Blog apenas para SEO, fora do menu
- **Trade-off**: Menos visibilidade para conteúdo
- **Justificativa**: Público não consome blog; autoridade vem de redes sociais

**3. Sem formulário de contato vs Com formulário**
- **Escolha**: WhatsApp + chamada de vídeo, sem formulário
- **Trade-off**: Pode perder leads que preferem email
- **Justificativa**: Público-alvo prefere WhatsApp; formulário cria fricção

**4. FAQ integrado vs FAQ separado**
- **Escolha**: FAQ integrado nas páginas de Experiências e Peças
- **Trade-off**: Páginas mais longas
- **Justificativa**: Informação onde o cliente precisa, sem navegação extra

**5. Newsletter como comunidade vs Apenas marketing**
- **Escolha**: Newsletter para comunidade e lista de espera
- **Trade-off**: Requer investimento em conteúdo de email
- **Justificativa**: Cria relacionamento, antecipa demanda, constrói comunidade

#### Riscos

**1. SEO fraco sem blog visível**
- **Risco**: Menor visibilidade no Google
- **Mitigação**: Blog existe (apenas não no menu), páginas principais otimizadas para SEO

**2. Perda de leads que preferem email**
- **Risco**: Pequena parcela que prefere formulário
- **Mitigação**: Email disponível no Contato (texto, não formulário)

**3. Páginas muito longas**
- **Risco**: Scroll infinito, fadiga do usuário
- **Mitigação**: Design com seções claras, CTAs ao longo da página

**4. Dependência de redes sociais**
- **Risco**: Algoritmos mudam, alcance cai
- **Mitigação**: Newsletter como canal próprio, SEO como backup

#### Anti-padrões a Evitar

**1. ❌ Menu com muitas opções**
- Confunde usuário mobile
- Máximo 5 itens no menu

**2. ❌ Blog tradicional como estratégia principal de autoridade**
- Público não consome
- Autoridade via redes sociais e prova social

**3. ❌ Formulário de contato como canal principal**
- Cria fricção
- WhatsApp é mais natural para público-alvo

**4. ❌ FAQ em página separada**
- Fragmenta informação
- Integrar nas páginas relevantes

**5. ❌ Desktop-first design**
- 90%+ do tráfego é mobile
- Mobile-first obrigatório

#### Validação

**Como validar a arquitetura**:

1. **Teste mobile**:
   - Site funciona perfeitamente no celular?
   - Navegação é intuitiva com polegar?
   - CTAs são clicáveis facilmente?

2. **Teste de fluxo**:
   - Usuário consegue converter em 2-3 cliques?
   - Fluxos são claros e diretos?

3. **Teste de entrada via redes**:
   - Link do Instagram/TikTok funciona?
   - Página de destino é relevante?

4. **Teste de conversão**:
   - WhatsApp funciona corretamente?
   - Agendamento de chamada funciona?

---

## 📦 Entregáveis

### 1. Sitemap Completo

**Estrutura final**:

```
SITEMAP — Verde Barro Cerâmica (Mobile-First)

/
├── / (Home)
│   ├── Hero com narrativa e proposta de valor
│   ├── Sobre a fundadora e história
│   ├── O que oferecemos (experiências + peças)
│   ├── Prova social (depoimentos, fotos, UGC)
│   ├── Newsletter (comunidade + lista de espera)
│   └── CTAs principais
│
├── /experiencias (Experiências)
│   ├── Hero com proposta de valor de workshops
│   ├── Como funciona (passo a passo visual)
│   ├── O que está incluso / não incluso
│   ├── Tipos de experiência (pessoal, compartilhada, presente)
│   ├── Preços (estrutura psicológica)
│   ├── FAQ integrado (perguntas frequentes)
│   ├── Prova social (depoimentos específicos)
│   ├── Agendamento (WhatsApp ou calendário)
│   └── Nota: Apenas São Paulo
│
├── /pecas (Peças Autorais)
│   ├── Hero com proposta de valor de peças
│   ├── História das peças autorais
│   ├── Catálogo de peças
│   ├── Combo: compre peça, ganhe 20% desconto no workshop
│   ├── FAQ integrado
│   ├── Checkout/compra
│   └── Nota: Entrega para todo Brasil
│
├── /contato (Contato)
│   ├── WhatsApp (link direto, CTA principal)
│   ├── Agendar chamada de vídeo (conhecer melhor o trabalho)
│   ├── Redes sociais (Instagram, TikTok — CTAs para seguir)
│   └── Sem formulário, sem FAQ
│
├── /blog (Blog — SEO only)
│   ├── Artigos otimizados para SEO e LLMs
│   ├── Foco: "workshop cerâmica São Paulo", "presente criativo", etc.
│   └── Não aparece no menu principal (apenas footer)
│
└── /legal (Páginas Utilitárias)
    ├── /politica-privacidade
    └── /termos-uso
```

---

### 2. Hierarquia de Páginas

**Menu Principal** (4 páginas):
| Página | URL | Propósito |
|--------|-----|-----------|
| Home | / | Narrativa, história, proposta de valor, direcionamento |
| Experiências | /experiencias | Workshops, como funciona, preços, agendamento |
| Peças Autorais | /pecas | Catálogo, compra, combo com workshop |
| Contato | /contato | WhatsApp, chamada de vídeo, redes sociais |

**Páginas Ocultas** (SEO/Legal):
| Página | URL | Propósito |
|--------|-----|-----------|
| Blog | /blog | SEO e indexação em LLMs |
| Artigo | /blog/[slug] | Artigo específico para SEO |
| Política | /legal/politica-privacidade | LGPD |
| Termos | /legal/termos-uso | Termos de uso |

---

### 3. Navegação e Menus

**Header (Mobile)**:
```
[Logo] [Menu Hambúrguer]

Menu aberto:
- Experiências
- Peças Autorais
- Contato
- [CTA: Fale no WhatsApp]
```

**Header (Desktop)**:
```
[Logo] | Experiências | Peças Autorais | Contato | [CTA: Agendar Experiência]
```

**Footer**:
```
┌─────────────────────────────────────────────────────────────┐
│  [Logo]                                                     │
│                                                             │
│  Experiências    Peças Autorais    Contato    Blog          │
│                                                             │
│  ─────────────────────────────────────────────────────────  │
│                                                             │
│  Newsletter: Faça parte da comunidade Verde Barro           │
│  [Email] [Quero participar]                                 │
│                                                             │
│  ─────────────────────────────────────────────────────────  │
│                                                             │
│  Instagram    TikTok    WhatsApp                            │
│                                                             │
│  Política de Privacidade | Termos de Uso                    │
│                                                             │
│  © 2026 Verde Barro Cerâmica                                │
└─────────────────────────────────────────────────────────────┘
```

**Elemento Fixo (Sticky)**:
- WhatsApp flutuante (canto inferior direito) — sempre visível

---

### 4. Conteúdo Mínimo por Página

**HOME**:

*Hero*:
- Headline com proposta de valor (inspirado em "o seu novo jeito de...")
- Subheadline emocional
- CTA principal ("Conheça as Experiências" ou "Fale no WhatsApp")
- Visual impactante (foto/vídeo de workshop)

*Sobre a Fundadora*:
- História pessoal e autêntica
- Por que Verde Barro existe
- Conexão emocional

*O que Oferecemos*:
- Card: Experiências (workshops na sua casa) — CTA
- Card: Peças Autorais (arte para sua casa) — CTA

*Prova Social*:
- Depoimentos de clientes (com foto/vídeo)
- Fotos de experiências reais
- UGC (se houver)
- Números (se relevante: "X workshops realizados")

*Newsletter*:
- Headline: "Faça parte da comunidade Verde Barro"
- Subheadline: "Receba novidades, inspirações e acesso antecipado"
- Input de email + CTA

*CTAs Finais*:
- "Agende sua experiência"
- "Conheça as peças"

---

**EXPERIÊNCIAS**:

*Hero*:
- Headline: Proposta de valor de workshops
- Subheadline: "Workshops de cerâmica na sua casa, em São Paulo"
- Visual impactante

*Como Funciona*:
- Passo 1: Você agenda
- Passo 2: Vamos até você
- Passo 3: Criamos juntos
- Passo 4: Você leva sua peça
- (Visual: ícones ou fotos)

*O que Está Incluso*:
- Lista clara do que está incluso
- Lista do que NÃO está incluso

*Tipos de Experiência*:
- Experiência pessoal (para você)
- Experiência compartilhada (com amigos/família)
- Presentear alguém (experiência como presente)

*Preços*:
- Estrutura de preços clara
- O que cada opção inclui
- (Sem esconder preço — transparência)

*FAQ Integrado*:
- "Preciso ter experiência?" — Não...
- "Quanto tempo dura?" — 3-4 horas...
- "Como funciona o agendamento?" — Via WhatsApp...
- (Apenas perguntas mais frequentes)

*Prova Social*:
- Depoimentos específicos de workshops
- Fotos de experiências

*CTA Final*:
- "Agende sua experiência" (WhatsApp ou calendário)
- Nota: "Experiências disponíveis apenas em São Paulo"

---

**PEÇAS AUTORAIS**:

*Hero*:
- Headline: Proposta de valor de peças
- Subheadline: "Peças únicas criadas por [nome da fundadora]"
- Visual das peças

*História das Peças*:
- Por que peças autorais
- Processo de criação
- Conexão com a marca

*Catálogo*:
- Grid de peças disponíveis
- Preço por peça
- CTA: Comprar

*Combo*:
- Destaque: "Compre uma peça e ganhe 20% de desconto no workshop"
- Explicação do combo
- CTA: Ver experiências

*FAQ Integrado*:
- "Como funciona a entrega?" — Entregamos para todo Brasil...
- "As peças são únicas?" — Sim, cada peça...
- (Apenas perguntas mais frequentes)

*CTA Final*:
- "Comprar peça" (checkout)
- Nota: "Entrega para todo o Brasil"

---

**CONTATO**:

*Hero*:
- Headline: "Vamos conversar?"
- Subheadline: "Tire suas dúvidas ou agende sua experiência"

*WhatsApp*:
- CTA principal: "Fale no WhatsApp"
- Link direto para WhatsApp
- (Maior destaque da página)

*Chamada de Vídeo*:
- "Quer conhecer melhor nosso trabalho?"
- "Agende uma chamada de vídeo com [nome da fundadora]"
- Link para agendamento (Calendly ou similar)

*Redes Sociais*:
- "Acompanhe nosso dia a dia"
- Instagram (link + CTA "Seguir")
- TikTok (link + CTA "Seguir")

*Sem formulário de email* — Se precisar, email disponível como texto: "Ou envie um email para: contato@verdebarro.com.br"

---

**BLOG (SEO only)**:

*Propósito*:
- Indexação no Google
- Indexação em LLMs (ChatGPT, etc.)
- Ranking para: "workshop cerâmica São Paulo", "presente criativo", "experiência de cerâmica", etc.

*Estrutura*:
- Listagem de artigos
- Artigos otimizados para SEO
- CTA em cada artigo direcionando para Experiências ou Peças

*Não aparece no menu principal* — Apenas no footer

---

### 5. Fluxos de Conversão

**Fluxo Principal: Instagram/TikTok → Workshop**
```
[Reel/Story no Instagram/TikTok]
    ↓
[Link na bio ou swipe up]
    ↓
[Home — narrativa, identifica-se]
    ↓
[Experiências — entende como funciona]
    ↓
[WhatsApp — agenda]
    ↓
CONVERSÃO: Workshop agendado
```

**Fluxo Secundário: Peça → Workshop**
```
[Instagram/TikTok]
    ↓
[Home ou Peças Autorais]
    ↓
[Compra peça — checkout]
    ↓
CONVERSÃO 1: Peça comprada + Cupom 20%
    ↓
[Experiências — usa cupom]
    ↓
[WhatsApp — agenda com desconto]
    ↓
CONVERSÃO 2: Workshop agendado
```

**Fluxo SEO/LLM (backup)**
```
[Google: "workshop cerâmica São Paulo"]
    ↓
[Blog — artigo relevante]
    ↓
[CTA no artigo → Experiências]
    ↓
[WhatsApp — agenda]
    ↓
CONVERSÃO: Workshop agendado
```

---

### 6. Estratégia de Autoridade (sem blog tradicional)

**Construção de autoridade para público-alvo**:

1. **Prova social no site**:
   - Depoimentos com foto/vídeo
   - Fotos de experiências reais
   - UGC (reposts de clientes)
   - Números (se relevante)

2. **Redes sociais como vitrine de autoridade**:
   - Feed curado (Instagram)
   - Vídeos de processo e experiências (TikTok)
   - Stories do dia a dia
   - Reels mostrando workshops

3. **Newsletter como canal de relacionamento**:
   - Conteúdo exclusivo
   - Acesso antecipado a novas peças
   - Lista de espera para workshops
   - Comunidade

4. **SEO/LLM (backup)**:
   - Blog escondido com artigos otimizados
   - Objetivo: Ranking no Google para buscas relevantes
   - Objetivo: Indexação em LLMs como referência de workshops em SP

---

### 7. Especificações Mobile-First

**Princípios de design**:
- Touch targets mínimo 44x44px
- Texto legível sem zoom (mínimo 16px)
- CTAs em posição de fácil acesso (parte inferior da tela)
- Navegação com menu hambúrguer
- Scroll vertical (evitar scroll horizontal)
- Imagens otimizadas para mobile
- Carregamento rápido (< 3 segundos)

**Elementos fixos**:
- Header com logo e menu
- WhatsApp flutuante (canto inferior direito)

**Adaptações para desktop**:
- Menu expandido (não hambúrguer)
- Layout em grid (2-3 colunas)
- Imagens maiores
- Mais espaço em branco

---

## 🎯 Próximos Passos

Após completar esta lição:
1. Criar prompt reutilizável em `prompts/ux-ui/`
2. Atualizar logs (Decisions, State, Changelog)
3. Realizar auditoria da Fase R
4. Criar CHECKPOINT da Fase R
5. Iniciar Fase C — Conversão sem Atrito

---

## ✅ Checklist da Lição

- [x] Conceitos explicados (3 camadas)
- [x] Análise de público-alvo e comportamento digital
- [x] Sitemap completo criado (estrutura simplificada)
- [x] Hierarquia de páginas definida
- [x] Navegação principal e secundária definida
- [x] Fluxos de conversão mapeados
- [x] Conteúdo mínimo por página definido
- [x] Estratégia de autoridade sem blog tradicional
- [x] Especificações mobile-first
- [x] Prompt reutilizável criado (`ux-ui__sitemap_mobile_first__v1.0.md`)
- [x] Logs atualizados
- [ ] Auditoria realizada

---

**Última atualização**: 2025-01-26
