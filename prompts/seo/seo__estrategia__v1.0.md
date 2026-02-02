# SEO — Estratégia e Estrutura Editorial (v1.0)

## Objetivo

Definir a estratégia de SEO e a estrutura editorial de um site de negócio: páginas principais, foco por URL, palavras-chave por página, meta tags recomendadas e (quando aplicável) plano de conteúdo para blog ou seção de autoridade.

## Quando Usar

- Fase S — Scale, SEO & Otimização Contínua (Lição S1)
- Lançamento ou relançamento de site
- Revisão de posicionamento no Google
- Planejamento de blog ou conteúdo para SEO

## Inputs Necessários

- **Nome do negócio**
- **Oferta principal** (serviço ou produto)
- **Público-alvo** (quem compra, onde está)
- **Cidade/região de atuação** (se relevante)
- **Lista de páginas do site** (URLs existentes ou planejadas)
- **Blog ou seção de conteúdo?** (sim/não; se sim, papel: menu principal ou “SEO only”)
- **Objetivo de busca** (ex.: “ser referência em [termo] em [cidade]”)

## Prompt

```
Você é um especialista em SEO para negócios locais e de serviços.

CONTEXTO DO NEGÓCIO:
- Nome: [NOME DO NEGÓCIO]
- Oferta principal: [SERVIÇO OU PRODUTO]
- Público-alvo: [QUEM COMPRA, ONDE ESTÁ]
- Cidade/região: [CIDADE OU REGIÃO]
- Páginas do site: [LISTA DE URLs OU PÁGINAS]
- Blog ou seção de conteúdo: [SIM/NÃO; SE SIM, PAPEL: MENU PRINCIPAL OU "SEO ONLY"]
- Objetivo de busca: [EX.: "ser referência em workshops de cerâmica em São Paulo"]

TAREFA:
Defina a estratégia de SEO e a estrutura editorial seguindo estas etapas:

1. INTENÇÃO DE BUSCA
   - Liste 5–10 buscas típicas que o público faria para encontrar este negócio.
   - Classifique por intenção (informacional, transacional, navegacional).
   - Indique em qual página do site cada busca deve ser atendida.

2. ESTRUTURA EDITORIAL (PÁGINAS PRINCIPAIS)
   - Para cada página do site: foco de conteúdo, palavras-chave principais (3–5) e secundárias (opcional).
   - Garanta que termos de cidade/região e oferta apareçam de forma natural nas páginas relevantes.

3. META TAGS RECOMENDADAS
   - Para cada página: title (até ~60 caracteres) e meta description (até ~155 caracteres).
   - Inclua termos principais e call-to-action quando fizer sentido.

4. BLOG OU CONTEÚDO (SE APLICÁVEL)
   - Se houver blog ou seção de conteúdo: liste 5–10 temas de artigos que respondam a buscas informacionais e reforcem autoridade.
   - Indique palavras-chave alvo por tema.
   - Sugira frequência mínima de publicação (ex.: 1–2 posts/mês).

5. SITEMAP E ROBOTS
   - Quais URLs devem aparecer no sitemap (páginas públicas).
   - Alguma URL que deva ser bloqueada no robots.txt? (ex.: admin, APIs).

6. RESUMO EXECUTIVO
   - 3–5 prioridades de implementação (ex.: meta tags em todas as páginas, sitemap.xml, primeiro lote de posts).
```

## Output Esperado

- Documento com: intenção de busca, estrutura editorial por página, meta tags por URL, temas de blog (se aplicável), orientações para sitemap/robots e prioridades de implementação.
- Títulos e descrições prontos para uso ou adaptação no site.
- Lista de palavras-chave por página para guiar copy e conteúdo.

## Versões

- v1.0 (2026-02-01): Versão inicial — estratégia, estrutura editorial, meta tags, blog (opcional), sitemap/robots.
