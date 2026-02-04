# Lição S2 — Conteúdo de Autoridade

> **Fase**: S — Scale, SEO & Otimização Contínua  
> **Status**: ✅ Concluída  
> **Data de conclusão**: 2026-02-04

---

## Objetivo da Lição

Definir o **conteúdo de autoridade** do site Verde Barro: primeiros artigos do blog (SEO only) que respondem às buscas do público e reforçam a marca como referência em workshops de cerâmica em São Paulo, sem virar o foco do site (blog fora do menu principal).

---

## Camada 1: Conceitos

### Conteúdo de autoridade em uma frase

**Conteúdo de autoridade** é o conjunto de textos (artigos, guias, FAQs) que demonstram expertise e respondem às dúvidas reais do seu público — gerando confiança e melhorando o posicionamento em buscas.

### Por que importa para a Verde Barro

- **Objetivo (R3/S1):** Ser referência no Google e em assistentes para "workshop cerâmica São Paulo" e termos relacionados.
- **Blog como ferramenta SEO:** Conteúdo que responde buscas informacionais ("como funciona", "quanto custa", "onde fazer") atrai tráfego qualificado e reforça autoridade.
- **Tom e posicionamento:** Cada artigo deve manter o tom da marca (íntimo, autêntico, acolhedor) e, quando natural, conectar com a oferta (experiências e peças).

### Pilares do conteúdo de autoridade

| Pilar | O que é | Exemplo Verde Barro |
|-------|---------|---------------------|
| **Intenção de busca** | O que a pessoa quer ao pesquisar | "O que é um workshop de cerâmica?" — informacional |
| **Estrutura clara** | H1, H2, parágrafos curtos, lista quando fizer sentido | Um H1 por artigo; seções com H2 |
| **Resposta direta** | Responder a pergunta no início (ou perto) | Primeiro parágrafo já responde |
| **Tom da marca** | Voz consistente em todo o site | Conversacional, acolhedor, sem jargão |
| **CTA contextual** | Convite natural à ação (não forçado) | "Se quiser vivenciar, veja nossas experiências" |
| **SEO básico** | Title, description, URL amigável, palavra-chave no texto | Slug: /blog/o-que-e-workshop-ceramica |

### O que NÃO é conteúdo de autoridade (evitar)

- Textos genéricos de "cerâmica no mundo" sem conexão com a oferta ou a região.
- Artigos só para "encher" o blog sem responder uma busca real.
- Tom corporativo ou técnico demais (perde a voz da marca).
- CTAs agressivos em todo o texto ("Compre agora!" em cada parágrafo).

---

## Camada 2: Aplicação — Verde Barro

### Papel do blog no site

- **Onde aparece:** URL /blog (lista) e /blog/[slug] (post). Fora do menu principal (público entra por redes e páginas principais; o blog atende quem já busca no Google).
- **Frequência sugerida:** 1–2 posts por mês para começar; priorizar qualidade e intenção de busca.
- **Fonte de verdade:** Estrutura editorial e temas já definidos na S1 (SEO Estratégico).

### Temas dos primeiros artigos (estrutura editorial S1)

| # | Tema / pergunta | Intenção de busca | Slug sugerido |
|---|-----------------|-------------------|---------------|
| 1 | O que é um workshop de cerâmica? | Informacional | o-que-e-workshop-ceramica |
| 2 | Modelagem vs pintura em cerâmica: qual escolher? | Informacional + decisão | modelagem-vs-pintura-ceramica |
| 3 | Como presentear com experiência em vez de objeto? | Informacional + presente | presentear-com-experiencia |
| 4 | Cerâmica em São Paulo: onde fazer? | Transacional (local) | ceramica-sao-paulo-onde-fazer |
| 5 | Quantas pessoas cabem em um workshop de cerâmica? | Informacional | quantas-pessoas-workshop-ceramica |
| 6 | Quanto tempo dura um workshop de cerâmica? | Informacional | quanto-tempo-workshop-ceramica |

### Critérios de qualidade por artigo

1. **Título (H1):** Frase que resume a pergunta ou o tema; pode ser a pergunta literal ou uma variação natural.
2. **Abertura:** Nos primeiros 1–2 parágrafos, responder de forma clara e direta (ideal para snippet no Google).
3. **Estrutura:** H2 para cada bloco de ideia; parágrafos curtos (2–4 linhas); listas quando facilitar a leitura.
4. **Tom:** Conversacional, acolhedor, autêntico — alinhado ao copy das páginas principais (Verde Barro).
5. **Conexão com a oferta:** Onde fizer sentido, mencionar experiências na sua casa, grupos pequenos, São Paulo; CTA único e suave (ex.: link para Experiências ou Contato), não repetido em todo o texto.
6. **Meta tags:** Title e description únicos por post; palavras-chave naturais; até ~60 caracteres no title, ~155 na description.

### Checklist de implementação (conteúdo)

- [x] Definir **ordem de publicação** dos primeiros artigos: 1) O que é um workshop de cerâmica?, 2) Modelagem vs pintura, 3) Presentear com experiência, 4) Cerâmica em São Paulo: onde fazer?, 5) Quantas pessoas cabem?, 6) Quanto tempo dura? (conforme tabela de temas).
- [x] Escrever **copy** dos 6 artigos (tom Verde Barro, resposta direta no primeiro parágrafo) e inserir no Notion via API — script `verde-barro-site/scripts/create-blog-posts.mjs`.
- [x] Revisar **tom** e **resposta direta**: cada post abre com definição/resposta clara; H2 para seções; CTA suave no fechamento quando aplicável.
- [x] **Meta tags** (title, description) e **URL/slug** por post: preenchidos na database (Titulo, Slug, Descricao); o site gera metadata dinâmica e canonical por slug.
- [x] **Blog** no sitemap e em **robots** (S1); páginas de post com canonical (implementado em `/blog/[slug]`).

### Checklist de implementação (site)

- [x] Criar rota **/blog** (lista de posts) e **/blog/[slug]** (post individual) no verde-barro-site.
- [x] Fonte de conteúdo: **Notion API (CMS)** — database "Blog Site Verde Barro" com propriedades: Titulo, Slug, Descricao, Publicado, Data Publicacao, Capa Post, Autor; corpo do post = blocos da página (cada linha da database é uma página).
- [x] Cada post: **metadata** (title, description, canonical, openGraph, twitter) dinâmica por slug.
- [x] **Sitemap** atualizado para incluir /blog e todos os slugs de posts (gerado dinamicamente).

### Implementação Notion API (referência)

- **Variáveis de ambiente:** `NOTION_API_KEY`, `NOTION_DATABASE_BLOG` (ID da database).
- **SDK:** `@notionhq/client` (API 2025-09-03: usa `databases.retrieve` para obter `data_sources[0].id` e `dataSources.query` para listar/filtrar posts; criação de páginas com `parent.data_source_id`).
- **Blocos renderizados:** parágrafo, heading_1/2/3, listas (bulleted, numbered), quote, code, image, divider; rich text com negrito, itálico, link, code.
- **Imagens:** Notion (e S3) usadas com `unoptimized` ou `<img>`; capa do post e imagens no corpo exibidas diretamente do Notion.
- **Revalidação:** 60 s (`revalidate = 60`) para lista e post.
- **Script de criação de posts:** `verde-barro-site/scripts/create-blog-posts.mjs` — cria os 6 posts iniciais no Notion via API (executar com `node --env-file=.env.local scripts/create-blog-posts.mjs`).

---

## Próximos passos

1. Usar o prompt **copy__conteudo_autoridade__v1.0.md** para gerar o copy dos próximos artigos (temas da tabela acima).
2. Publicar no Notion (marcar **Publicado** e preencher Slug, Data Publicacao, etc.); o site atualiza em até 1 minuto.
3. Avançar para **S3 — Métricas e Analytics** (painel e Search Console).

---

**Status**: ✅ Concluída  
**Última atualização**: 2026-02-04
