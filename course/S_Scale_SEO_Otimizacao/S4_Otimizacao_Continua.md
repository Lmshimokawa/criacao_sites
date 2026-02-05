# Lição S4 — Otimização Contínua

> **Fase**: S — Scale, SEO & Otimização Contínua  
> **Status**: 🔄 Em andamento  
> **Data de início**: 2026-01-28

---

## Objetivo da Lição

Estabelecer uma **rotina mensal de evolução** do site Verde Barro: usar as métricas (S3) para priorizar melhorias, aplicar ciclos de melhoria e, quando fizer sentido, testes guiados por dados — para que o site evolua de forma consciente e não fique parado após o lançamento.

---

## Camada 1: Conceitos

### Ciclos de melhoria

- **O que é:** repetir, em intervalo fixo (ex.: mensal), a sequência: **olhar dados → decidir o que melhorar → implementar → medir de novo**.
- **Por que importa:** sem rotina, o site tende a ficar “congelado”; com ciclo definido, cada mês há um passo concreto (uma página, um CTA, um texto, uma métrica).
- **Para Verde Barro:** revisão mensal do painel (S3) + uma a três ações por ciclo (ex.: melhorar título de uma página que ranqueia, ajustar CTA do blog, corrigir página com erro no GSC).

### Iteração guiada por dados

- **Decisões com base em números:** priorizar o que os dados mostram (ex.: “página X tem impressões mas poucos cliques” → melhorar title/description; “blog post Y traz tráfego” → criar mais conteúdo na mesma linha).
- **Evitar:** mudar tudo por intuição; ignorar Search Console e analytics.
- **Fonte de verdade (S3):** Search Console (impressões, cliques, consultas, erros) + Vercel Analytics (visitantes, páginas) + Supabase (newsletter, solicitações).

### Testes A/B (quando faz sentido)

- **O que é:** testar duas versões (ex.: título A vs B, texto do botão) com parte do tráfego e comparar resultado (cliques, conversão).
- **Quando priorizar:** quando já houver tráfego suficiente e uma dúvida clara (ex.: “este CTA converte mais?”). No início, muitas vezes basta **iterar e medir** (mudar, esperar 2–4 semanas, ver no GSC/analytics) em vez de A/B formal.
- **Ferramentas:** GA4 (experimentos), Vercel Edge (rewrites), ou ferramentas dedicadas (Optimizely, etc.). Para Verde Barro no início: foco em **uma versão por vez + métricas**; A/B pode entrar depois.

### O que NÃO priorizar

- Refazer o site inteiro a cada ciclo.
- Métricas sem ação (só olhar e não mudar nada).
- A/B sem volume de tráfego ou sem hipótese clara.

---

## Camada 2: Aplicação — Verde Barro

### Rotina mensal sugerida

| Passo | Ação | Onde |
|-------|------|------|
| 1 | Revisar impressões, cliques e top páginas | Search Console |
| 2 | Ver top consultas (keywords) e erros de indexação | Search Console |
| 3 | Ver Core Web Vitals (mobile/desktop) | Search Console > Experiência |
| 4 | Ver visitantes e páginas mais vistas | Vercel Analytics |
| 5 | Contar inscrições newsletter e solicitações de experiência | Supabase |
| 6 | Escolher 1–3 melhorias para o próximo ciclo | — |
| 7 | Implementar (copy, SEO, CTA, performance) e anotar | — |
| 8 | Na próxima revisão, conferir se as métricas evoluíram | — |

### Exemplos de ações por ciclo

- **SEO:** Ajustar title/description de uma página com muitas impressões e poucos cliques; corrigir página com erro de cobertura; adicionar um post no blog alinhado a uma keyword que já ranqueia.
- **Conversão:** Melhorar texto do CTA do blog (“Agende uma experiência”); testar posição do formulário na página de contato.
- **Experiência:** Corrigir página lenta (Core Web Vitals); melhorar texto de uma seção com alta rejeição (se os dados indicarem).

### Prompt de evolução (Vibe Coding)

Usar um prompt de **otimização** na biblioteca (ou criar um) que inclua:

- **Contexto:** Verde Barro, site de workshops de cerâmica, objetivos (tráfego orgânico, conversão em experiência/newsletter).
- **Input:** resumo das métricas do mês (impressões, cliques, top páginas, erros, conversões).
- **Output esperado:** lista priorizada de 1–3 ações concretas (o que mudar, onde, por quê) para o próximo ciclo.

---

## Checklist de implementação

- [ ] **Definir data da primeira revisão mensal** (ex.: 30 dias após go-live ou após concluir S3).
- [ ] **Realizar primeira revisão:** abrir Search Console + Vercel Analytics + Supabase; preencher (em doc ou planilha) os números do painel (S3).
- [ ] **Escolher 1–3 ações** para o primeiro ciclo de melhoria e anotar.
- [ ] **Implementar** as ações (copy, SEO, CTA ou performance).
- [ ] **Documentar ou criar prompt** de “revisão mensal” (template de métricas + decisões) para reutilizar nos próximos ciclos.
- (Opcional) **Introduzir teste A/B** quando houver tráfego e uma hipótese clara (ex.: via GA4 ou ferramenta dedicada).

---

## Entregável

- **Rotina mensal de evolução do site:** data fixa (ex.: primeiro dia útil do mês) + checklist de revisão (painel S3) + 1–3 ações por ciclo + registro do que foi feito e do resultado na próxima revisão.

---

## Próximos passos

1. Agendar primeira revisão mensal.
2. Ao final da fase S: conferir checklist final do framework (proposta de valor, funil, métricas ativas, rotina de otimização definida).

---

**Status**: 🔄 Em andamento  
**Última atualização**: 2026-01-28
