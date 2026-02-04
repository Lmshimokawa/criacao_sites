# Analytics — Setup de Métricas e Painel (v1.0)

## Objetivo

Definir a stack de métricas (Search Console, analytics de tráfego, conversões) e o painel de indicadores que o negócio vai acompanhar para evoluir o site com base em dados.

## Quando Usar

- Fase S — Scale, SEO & Otimização Contínua (Lição S3)
- Após o site estar no ar (mesmo que em homolog)
- Antes de definir rotina de otimização contínua (S4)

## Inputs Necessários

- **URL do site** (produção ou homolog)
- **Objetivo de negócio** (ex.: tráfego orgânico, conversões em newsletter/solicitação)
- **Ferramentas já em uso** (ex.: Vercel, Supabase, Resend)
- **Restrições** (ex.: evitar cookies / LGPD; orçamento para ferramentas pagas)

## Prompt

```
Você é um consultor de métricas e analytics para sites de negócio (pequeno/médio porte).

CONTEXTO:
- Site: [URL DO SITE]
- Objetivo principal: [EX.: "tráfego orgânico para workshop cerâmica em SP" / "conversões em newsletter e solicitação de experiência"]
- Stack atual: [EX.: Next.js, Vercel, Supabase, Resend]
- Restrições: [EX.: minimizar cookies / LGPD; só ferramentas gratuitas]

TAREFA:
1. STACK DE MÉTRICAS
   - Recomende obrigatoriamente: Google Search Console (verificação + sitemap). Explique em 2 linhas por que é prioritário.
   - Recomende uma opção de analytics de tráfego: (a) Vercel Analytics, (b) Google Analytics 4, (c) Plausible ou similar. Justifique em 1 linha considerando privacidade, custo e simplicidade.
   - Indique onde as conversões serão vistas (ex.: Supabase, GA4 eventos, planilha).

2. PAINEL MÍNIMO (o que acompanhar)
   - Liste 5 a 8 indicadores que o dono do site deve olhar (ex.: impressões/cliques no Search Console, pageviews, inscrições newsletter, solicitações).
   - Para cada um: nome da métrica, onde ver (ferramenta + onde clicar), frequência sugerida (ex.: mensal).

3. PASSOS DE SETUP (resumidos)
   - Search Console: como verificar a propriedade (método mais simples para o stack) e onde enviar o sitemap.
   - Analytics escolhido: como ativar (ex.: variável de ambiente, script no layout, link de documentação).

4. LGPD/COOKIES
   - Se a opção de analytics usar cookies de terceiros: mencione que é recomendável aviso/banner e link para política de privacidade. Se for apenas Vercel Analytics (sem cookies identificáveis): mencione que em muitos casos não exige banner, mas que a política de privacidade deve listar as ferramentas usadas.

OUTPUT: texto em tópicos, pronto para colar em doc ou checklist do projeto.
```

## Output Esperado

- Recomendação clara: Search Console + uma ferramenta de tráfego + onde ver conversões.
- Lista de indicadores (painel mínimo) com “onde ver” e “frequência”.
- Passos de setup resumidos (verificação Search Console, ativação do analytics).
- Nota sobre cookies/LGPD conforme a escolha.

## Versões

- **v1.0** (2026-02-04): Versão inicial criada durante Lição S3 do curso ARCOS™. Caso piloto: Verde Barro Cerâmica.

---

**Criado em**: 2026-02-04  
**Lição**: S3 — Métricas e Analytics
