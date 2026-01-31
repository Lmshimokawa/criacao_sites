# Changelog — Curso Completo de Criação de Sites

Todas as mudanças relevantes neste projeto serão documentadas aqui.

O formato é baseado em [Keep a Changelog](https://keepachangelog.com/pt-BR/1.0.0/),
e este projeto adere ao [Semantic Versioning](https://semver.org/lang/pt-BR/).

---

## [Unreleased]

### Modificado
- **Lição A1 — Proposta de Valor** (revisão 2025-01-25):
  - Posicionamento 1-linha revisado: removido "premium" explícito, escolhida versão mais autêntica e poética (Opção D)
  - Incorporada dimensão de presente/experiência compartilhada como proposta de valor SECUNDÁRIA (core permanece experiência pessoal)
  - Parágrafo institucional atualizado (remove "premium", mantém foco em experiência pessoal, não menciona presente explicitamente)
  - Tagline de presente removida (não queremos tagline explícita sobre presente)
  - 3 novas objeções/respostas adicionadas (presente), ajustadas para não mencionar "presente que vale mais que dinheiro" explicitamente
  - Análise da proposta de valor expandida (dois perfis: experiência pessoal CORE + presente compartilhado SECUNDÁRIO)
  - Mensagem de presente será transmitida através de copy emocional e exemplos, não texto explícito
  - Documento de referência criado: `A1_Copy_Emocional_Presente.md` com exemplos de copy emocional para presente

### Modificado
- **Lição A2 — Posicionamento** (ajuste 2025-01-25):
  - Ajustado anticompetidor "NÃO é loja de peças" para refletir estratégia inicial
  - Adicionada estratégia inicial: venda de peças como entrada (secundária)
  - Adicionado combo obrigatório: peça autoral = cupom 20% desconto no workshop (válido 2 meses)
  - Decisão registrada: DEC-010

### Concluído
- ✅ Lição A1 — Proposta de Valor (finalizada)
- ✅ Lição A2 — Posicionamento e Categoria Mental:
  - Conceitos explicados (3 camadas)
  - Declaração clara de posicionamento criada
  - 6 anticompetidores mapeados (o que NÃO é)
  - Território simbólico definido
  - Prompt reutilizável: `strategy__posicionamento__v1.0.md`
  - Documentação completa em `course/A_Arquitetura_de_Valor/A2_Posicionamento_Categoria_Mental.md`
  - Auditoria realizada (AUD-002: Consistência A1/A2)
- ✅ Lição A3 — Definição da Oferta:
  - Conceitos explicados (3 camadas)
  - Escopo da oferta (workshop) definido
  - Escopo da oferta (peças autorais) definido
  - Regras da oferta criadas
  - Expectativas do cliente mapeadas
  - Precificação psicológica estruturada
  - Prompt reutilizável: `strategy__definicao_oferta__v1.0.md`
  - Documentação completa em `course/A_Arquitetura_de_Valor/A3_Definicao_da_Oferta.md`
- ✅ CHECKPOINT da Fase A criado:
  - Resumo de decisões das 3 lições
  - Riscos e trade-offs identificados
  - Itens a revisar antes/durante implementação
  - Lista de prompts aprovados (3 prompts)
  - Validações e consistências verificadas
  - Documento: `course/A_Arquitetura_de_Valor/CHECKPOINT.md`

### Concluído
- ✅ Lição R1 — Jornada do Usuário:
  - Conceitos explicados (3 camadas)
  - Mapa da jornada completa criado (6 etapas)
  - Pontos de fricção identificados
  - Oportunidades mapeadas
  - Microdecisões listadas
  - Prompt reutilizável: `ux-ui__jornada_usuario__v1.0.md`
  - Documentação completa: `course/R_Ritual_do_Usuario/R1_Jornada_do_Usuario.md`

### Concluído
- ✅ Lição R2 — Funil de Conversão:
  - Conceitos explicados (3 camadas)
  - Funil desenhado (TOFU, MOFU, BOFU, Pós-conversão)
  - CTA principal e CTAs contextuais definidos
  - Canais de entrada mapeados
  - Dois funis paralelos documentados (experiência pessoal + presente)
  - Estratégia de conversão entre funis (peça → workshop via combo)
  - Prompt reutilizável: `ux-ui__funil_conversao__v1.0.md`
  - Documentação completa: `course/R_Ritual_do_Usuario/R2_Funil_de_Conversao.md`

### Concluído
- ✅ Lição R3 — Arquitetura de Informação:
  - Conceitos explicados (3 camadas) com foco em mobile-first e comportamento digital moderno
  - Público-alvo refinado: mulheres jovens (25-35), SP, redes sociais (Instagram/TikTok)
  - Sitemap ultra-simplificado: 4 páginas no menu (Home, Experiências, Peças, Contato)
  - Blog escondido (SEO only) — não no menu principal
  - Contato sem formulário (WhatsApp + chamada de vídeo)
  - Newsletter para comunidade e lista de espera
  - Referência: meubenza.com.br (estrutura simples, narrativa, CTAs claros)
  - Fluxos de conversão em 2-3 cliques
  - Especificações mobile-first
  - Prompt reutilizável: `ux-ui__sitemap_mobile_first__v1.0.md`
  - 5 novas decisões registradas (DEC-011 a DEC-015)

### Concluído
- ✅ Auditoria da Fase R (AUD-003, AUD-004)
  - Verificada consistência entre R1, R2, R3 e Fase A
  - R3 definido como fonte de verdade para arquitetura
  - Todas as 18 decisões verificadas e alinhadas
- ✅ CHECKPOINT da Fase R criado
  - Sitemap final documentado (4 páginas principais)
  - Ofertas refinadas (Modelagem + Pintura + Peças)
  - Público-alvo definido (mulheres 25-35, SP, redes sociais)
  - Checkout compartilhável documentado
  - 3 prompts de UX-UI aprovados

### Concluído
- ✅ Lição C1 — Wireframes / Layout:
  - Wireframes mobile-first para todas as páginas (HOME, EXPERIÊNCIAS, PEÇAS, CONTATO)
  - Fluxo completo de checkout compartilhável wireframado
  - Prompt reutilizável: `ux-ui__wireframes_mobile_first__v1.0.md`

- ✅ Lição C2 — Copy das Páginas:
  - Copy completo para HOME (hero, sobre, ofertas, como funciona, prova social, newsletter)
  - Copy completo para EXPERIÊNCIAS (tipos, formatos, incluso, FAQ)
  - Copy completo para CHECKOUT COMPARTILHÁVEL (todas as telas do fluxo)
  - Copy completo para PEÇAS AUTORAIS (história, catálogo, combo)
  - Copy completo para CONTATO (WhatsApp, chamada de vídeo, redes)
  - Elementos globais (header, footer, meta tags SEO)
  - Prompt reutilizável: `copy__paginas_experiencias__v1.0.md`

### Concluído
- ✅ Lição C3 — Canais de Conversão:
  - Mapa completo de todos os canais
  - WhatsApp: click-to-chat, mensagens pré-preenchidas, horários
  - Checkout individual: fluxo de 7 etapas
  - Checkout compartilhável: fluxo organizador + convidado + regras de negócio
  - Checkout e-commerce: peças autorais com cupom
  - Agendamento: opções Cal.com/Calendly, campos
  - Email: automações welcome, carrinho abandonado, pós-compra
  - Chamada de vídeo: script e configuração
  - Integrações técnicas: stack recomendada (Next.js, Stripe, Resend, Cal.com)
  - Prompt reutilizável: `ux-ui__canais_conversao__v1.0.md`

### Concluído
- ✅ CHECKPOINT Fase C criado
  - Resumo de wireframes, copy e canais
  - Checkout compartilhável especificado
  - Stack técnica recomendada
  - 3 prompts aprovados (wireframes, copy, canais)

### Concluído
- ✅ Lição O1 — Como um Site Funciona:
  - Fluxo de requisição web (DNS → servidor → resposta)
  - Tipos de sites (estático, SSR, SPA, híbrido)
  - Arquitetura proposta: híbrido com serverless
  - Glossário técnico (DNS, CDN, API, SSG, etc.)
  - Checklist de infraestrutura (domínio, hospedagem, banco, pagamentos)
  - Estimativa de custos: R$ 7-60/mês (início)

### Concluído
- ✅ Lição O2 — Stack Tecnológica:
  - 2 opções propostas: Simples (Next.js) vs Robusta (Astro)
  - Decisão: Opção A com arquitetura híbrida
  - **Notion**: CMS para peças, blog, depoimentos
  - **Supabase**: Banco para checkout, pagamentos, grupos
  - Stack: Next.js 14 + Tailwind + Stripe + Resend + Cal.com + Vercel
  - DEC-019 registrada

- ✅ Ajustes no fluxo e schema (O2):
  - **DEC-020**: Fluxo de experiências alterado — agendamento ANTES do pagamento
    - Cliente solicita → Você confirma → Link de pagamento gerado
  - **DEC-021**: Schema revisado com 8 tabelas
  - **DEC-022**: Gestão de cupons centralizada
    - Tabela `cupons` para todos os tipos (peça, influenciadora, promocional)
    - Tabela `cupons_uso` para rastreamento
    - Cupom de peça autoral: 20% off, validade 2 meses
    - Suporte a parcerias com influenciadoras

### Em Andamento
- 🔄 Lição O3 — Infraestrutura Básica:
  - Guia completo de setup em 10 etapas
  - Checklist de contas: GitHub, Vercel, Supabase, Stripe, Resend, Cal.com
  - Script SQL pronto para criar 8 tabelas no Supabase
  - Código base para clientes (Supabase, Stripe, Resend)
  - Página Home básica em React/Next.js
  - Instruções de deploy na Vercel
  - **Pendente**: Execução prática do setup

### Adicionado
- Estrutura completa do repositório (docs/, prompts/, course/, src/, assets/)
- Arquivos núcleo em `docs/`:
  - `00_README.md` — Visão geral do projeto
  - `01_ARCOS_Framework.md` — Documentação completa do framework
  - `02_Course_Roadmap.md` — Roteiro completo do curso
  - `03_Decisions_Log.md` — Log de decisões
  - `04_Audit_Log.md` — Log de auditoria
  - `05_State.md` — Estado atual do projeto
  - `06_Backlog.md` — Pendências e melhorias
  - `07_Definitions_Glossary.md` — Glossário de termos
- Estrutura de `prompts/` com categorias (strategy, ux-ui, copy, seo, analytics, infra-deploy)
- Estrutura de `course/` com todas as fases ARCOS
- Estrutura de `assets/` (brand, images, references)
- `prompts/README.md` — Documentação da biblioteca de prompts
- Caso piloto definido: Verde Barro Cerâmica
- **Lição A1 — Proposta de Valor**:
  - Conceitos explicados (3 camadas)
  - Posicionamento 1-linha criado
  - Parágrafo institucional premium criado
  - 3 taglines criadas
  - Objeções e respostas mapeadas
  - Prompt reutilizável: `strategy__proposta_valor__v1.0.md`
  - Documentação completa em `course/A_Arquitetura_de_Valor/A1_Proposta_de_Valor.md`

### Concluído
- ✅ Lição A1 — Proposta de Valor

---

## [0.1.0] - 2025-01-25

### Adicionado
- Setup inicial do repositório
- Estrutura base conforme especificação

---

**Legenda**:
- `[Unreleased]`: Mudanças em desenvolvimento
- `[X.Y.Z]`: Versões lançadas (data)
