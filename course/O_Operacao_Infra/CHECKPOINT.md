# CHECKPOINT — Fase O: Operação & Infraestrutura

> **Data**: 2025-02-01
> **Status**: ✅ Concluída  
> **Próxima fase**: S — Scale, SEO & Otimização Contínua

---

## 📋 Resumo das Decisões

### Lição O1 — Como um Site Funciona

**Entregáveis**:
- Fluxo de requisição web explicado (DNS → servidor → resposta)
- Tipos de sites comparados (estático, SSR, SPA, híbrido)
- Arquitetura proposta para Verde Barro: híbrido + serverless
- Glossário técnico (10 termos)
- Checklist de infraestrutura
- Estimativa de custos (início: R$ 7–60/mês)

**Princípios**:
- Verde Barro precisa de conteúdo dinâmico (peças, blog) + transações (checkout, pagamentos)
- Híbrido permite SEO, performance e interatividade

---

### Lição O2 — Stack Tecnológica

**Decisões principais**:
- **DEC-019**: Opção A (Next.js + Vercel) com arquitetura híbrida
- **DEC-020**: Fluxo de experiências — agendamento ANTES do pagamento (solicitação → confirmação → link de pagamento)
- **DEC-021**: Schema Supabase com 8 tabelas
- **DEC-022**: Gestão de cupons centralizada (tabelas `cupons` e `cupons_uso`)

**Stack final**:
- **Frontend:** Next.js 14 (App Router) + Tailwind + shadcn
- **CMS:** Notion API (peças, blog, depoimentos)
- **Banco transacional:** Supabase (solicitações, pedidos, grupos, newsletter, cupons)
- **Pagamentos:** Stripe
- **Email:** Resend
- **Agendamento:** Cal.com
- **Hospedagem:** Vercel

**Tabelas Supabase**:
- `solicitacoes_experiencias` — pré-pagamento
- `pedidos_experiencias` — pós-pagamento
- `pedidos_pecas` — peças autorais
- `grupos` e `grupo_participantes` — checkout compartilhável
- `newsletter` — inscritos (com `aceite_privacidade`)
- `cupons` e `cupons_uso` — cupons (peça 20%, influenciadora, promocional)

---

### Lição O3 — Infraestrutura Básica

**Entregáveis**:
- Guia completo de configuração (10 etapas)
- Estrutura base do projeto executada no repositório `verde-barro-site`
- Clientes: Supabase (client + server), Stripe, Resend
- Páginas: Home, Experiências, Peças, Contato
- API routes: `/api/solicitacao`, `/api/checkout`, `/api/webhooks/stripe`, `/api/newsletter`
- Componentes: Header, Footer, NewsletterForm
- Página Home com hero + seção newsletter
- Webhook Stripe testado

**Estrutura de pastas**:
- `src/app/(site)/` — páginas públicas
- `src/app/api/` — API routes
- `src/components/layout/` — Header, Footer
- `src/components/forms/` — NewsletterForm
- `src/lib/supabase/`, `stripe.ts`, `resend.ts`
- `src/emails/` — template confirmacao.tsx

---

### Lição O4 — Segurança e LGPD

**Entregáveis**:
- Política de privacidade publicada em `/legal/privacidade`
- Link “Política de privacidade” no footer
- Checkbox de consentimento no formulário de newsletter (obrigatório)
- API newsletter exige `aceite_privacidade: true` e persiste na tabela `newsletter`
- Coluna `aceite_privacidade` no schema (O2/O3) e migração documentada para projetos existentes

**Bases legais**:
- Newsletter: consentimento (checkbox)
- Pedidos/solicitações: execução de contrato
- Dados de pagamento: Stripe (não armazenados no site)

**Pendente (opcional)**:
- Banner de cookies (se usar analytics/cookies de terceiros)
- Menção + link à Política na solicitação de experiência e checkout (quando implementar formulários)

---

## 🔗 Fluxo de Dados Consolidado

```
CONTEÚDO        → Notion API (peças, blog, depoimentos)
TRANSAÇÕES      → Supabase (solicitações, pedidos, grupos, newsletter, cupons)
PAGAMENTOS      → Stripe (checkout, webhooks)
EMAIL           → Resend (transacional + newsletter)
AGENDAMENTO     → Cal.com
HOSPEDAGEM      → Vercel
```

---

## 📱 Sitemap Atual (verde-barro-site)

```
/
├── / (Home) — hero, newsletter
├── /experiencias
├── /pecas
├── /contato
└── /legal/privacidade — Política de privacidade
```

---

## ✅ Validações Antes da Fase S

- [x] Stack definida e documentada
- [x] Schema do banco definido (8 tabelas + migração newsletter)
- [x] Projeto base rodando (Next.js, Supabase, Stripe, Resend)
- [x] Política de privacidade publicada e link no footer
- [x] Consentimento na newsletter configurado
- [ ] Deploy na Vercel (quando fizer)
- [ ] Domínio e SSL (quando configurar)

---

## 🎯 Próximos Passos (Fase S)

1. **S1 — SEO Estratégico:** estrutura editorial, meta tags, sitemap
2. **S2 — Conteúdo de Autoridade:** primeiros artigos (blog para SEO)
3. **S3 — Métricas e Analytics:** painel, eventos, conversões
4. **S4 — Otimização Contínua:** rotina mensal de evolução

---

**Última atualização**: 2025-02-01
