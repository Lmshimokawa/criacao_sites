# Lição S3 — Métricas e Analytics

> **Fase**: S — Scale, SEO & Otimização Contínua  
> **Status**: 🔄 Em andamento  
> **Data de início**: 2026-02-04

---

## Objetivo da Lição

Configurar o **painel de métricas** do site Verde Barro: conectar Google Search Console (SEO), definir analytics de tráfego e conversão, e estabelecer o que acompanhar mensalmente para evoluir com base em dados reais.

---

## Camada 1: Conceitos

### Por que métricas importam

- **Sem dados:** decisões por intuição; não dá para saber se o blog traz visitas, se o formulário converte ou se uma página trava no mobile.
- **Com dados:** priorizar o que funciona (ex.: qual post ranqueia), corrigir o que falha (ex.: página lenta) e repetir o que converte.

### Três pilares para um site de negócio

| Pilar | O que responde | Ferramenta típica |
|-------|----------------|-------------------|
| **SEO** | Como o site aparece no Google (busca orgânica)? Quais páginas ranqueiam? | Google Search Console |
| **Tráfego e comportamento** | Quantas visitas? De onde? Quais páginas? | Google Analytics 4 ou Vercel Analytics / Plausible |
| **Conversão** | Quantos preencheram formulário, assinaram newsletter, iniciaram checkout? | Eventos no analytics + Supabase (dados transacionais) |

### O que NÃO priorizar no início

- Dashboards complexos com dezenas de gráficos.
- Métricas de “vanidade” (ex.: só pageviews sem contexto).
- Analytics antes de ter Search Console e domínio verificado (SEO primeiro).

---

## Camada 2: Aplicação — Verde Barro

### 1. Google Search Console (obrigatório para SEO)

- **O que é:** ferramenta gratuita do Google que mostra como o site aparece na busca (impressões, cliques, posição média, páginas indexadas, Core Web Vitals).
- **Por que primeiro:** o objetivo (S1/R3) é “ser referência no Google”; o Search Console é a fonte de verdade para isso.
- **Passos resumidos:**
  1. Acessar [search.google.com/search-console](https://search.google.com/search-console).
  2. Adicionar “recurso” (property): URL do site (ex.: `https://verdebarro.com.br` ou a URL de homolog na Vercel).
  3. Verificar propriedade: método recomendado = **tag HTML** ou **arquivo HTML** no site; alternativa = **DNS** (registro TXT no domínio). No Next.js, colocar a meta tag em `layout.tsx` ou usar a opção de arquivo em `public/`.
  4. Enviar sitemap: em “Sitemaps”, informar `https://seu-dominio.com/sitemap.xml`.
- **O que acompanhar (mensal):** impressões e cliques totais; páginas com mais cliques; consultas (keywords) que trazem tráfego; erros de cobertura/indexação; Core Web Vitals (experiência).

### 2. Analytics de tráfego (escolha uma opção)

- **Google Analytics 4 (GA4):** gratuito, poderoso, eventos e conversões customizáveis; exige banner/cookies se houver uso de cookies não essenciais (LGPD). Integração via script ou `@next/third-parties/google`.
- **Vercel Analytics:** simples, privacidade-friendly, métricas básicas (pageviews, top páginas) para projetos na Vercel; menos detalhe que GA4.
- **Plausible (ou similar):** foco em privacidade, sem cookies; pago; dashboard enxuto.

Para Verde Barro, **recomendação inicial:** Search Console + **Vercel Analytics** (se o site estiver na Vercel) para não precisar de banner no lançamento; depois, se quiser funil e eventos detalhados, adicionar GA4 e tratar cookies (O4).

### 3. Painel de métricas (o que acompanhar)

Definir um “painel” = lista de indicadores que você olha com frequência (ex.: mensal), não necessariamente um app. Pode ser um doc ou planilha.

**Sugestão para Verde Barro:**

| Métrica | Onde ver | Frequência |
|---------|----------|------------|
| Impressões e cliques (busca) | Search Console | Mensal |
| Top 5 páginas por cliques | Search Console | Mensal |
| Top consultas (keywords) | Search Console | Mensal |
| Erros de indexação | Search Console > Cobertura | Mensal |
| Core Web Vitals (mobile/desktop) | Search Console > Experiência | Mensal |
| Visitantes / pageviews | Vercel Analytics ou GA4 | Mensal |
| Inscrições newsletter | Supabase (tabela `newsletter`) ou email Resend | Mensal |
| Solicitações de experiência | Supabase (`solicitacoes_experiencias`) | Mensal |

**Conversões:** hoje o “fundo do funil” são: newsletter, solicitação de experiência, (futuro) checkout. Contar registros no Supabase já é um painel mínimo; depois dá para enviar eventos para GA4 (ex.: “newsletter_signup”) para ver no mesmo lugar.

### 4. Cookies e LGPD (O4)

- Se usar **apenas** Vercel Analytics (sem cookies identificáveis), muitas vezes não exige banner, mas confira a documentação e sua política de privacidade.
- Se usar **GA4** ou ferramentas com cookies de terceiros: aviso/banner de cookies e opção de aceitar/recusar é recomendável (conforme O4).

---

## Checklist de implementação

- [ ] **Verificar site no Google Search Console** (propriedade + sitemap).
- [ ] **Decidir analytics:** Vercel Analytics e/ou GA4 (ou Plausible).
- [ ] **Implementar** o script/tag no site (ex.: Vercel Analytics no projeto Vercel; GA4 em `layout.tsx` ou via `@next/third-parties`).
- [ ] **Documentar o “painel”** (lista de métricas + onde ver) em um doc interno ou na lição.
- [ ] (Opcional) **Eventos de conversão** (newsletter, solicitação) no GA4, se usar GA4.
- [ ] (Se GA4/cookies) **Revisar política de privacidade e banner** (O4).

---

## Próximos passos

1. Verificar o site no Search Console e enviar o sitemap.
2. Ativar Vercel Analytics (ou configurar GA4) conforme decisão.
3. Definir data para primeira revisão mensal (ex.: 30 dias após go-live).
4. Avançar para **S4 — Otimização Contínua** (rotina mensal e prompt de evolução).

---

**Status**: 🔄 Em andamento  
**Última atualização**: 2026-02-04
