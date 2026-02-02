# Lição S2 — Conteúdo de Autoridade

> **Fase**: S — Scale, SEO & Otimização Contínua  
> **Status**: Em andamento  
> **Data de início**: 2026-02-01

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

- [ ] Definir **ordem de publicação** dos primeiros artigos (sugestão: começar pelo "O que é um workshop de cerâmica?").
- [ ] Escrever ou encomendar **copy** de cada artigo usando o prompt copy__conteudo_autoridade__v1.0.md.
- [ ] Revisar **tom** e **resposta direta** (primeiro parágrafo) em cada texto.
- [ ] Garantir **meta tags** (title, description) e **URL/slug** por post no site.
- [ ] Incluir **blog** no sitemap e em **robots** (já previsto na S1); páginas de post com canonical.

### Checklist de implementação (site)

- [ ] Criar rota **/blog** (lista de posts) e **/blog/[slug]** (post individual) no verde-barro-site.
- [ ] Fonte de conteúdo: Notion API (CMS) ou arquivos estáticos/MDX — conforme decisão na O2/O3.
- [ ] Cada post: **metadata** (title, description, canonical, openGraph) dinâmica por slug.
- [ ] Atualizar **sitemap** para incluir /blog e todos os slugs de posts quando existirem.

---

## Próximos passos

1. Usar o prompt **copy__conteudo_autoridade__v1.0.md** para gerar o copy do primeiro artigo ("O que é um workshop de cerâmica?").
2. Implementar as rotas **/blog** e **/blog/[slug]** no site (ou documentar dependência ao CMS).
3. Publicar o primeiro artigo e revisar meta tags e snippet.
4. Avançar para **S3 — Métricas e Analytics** (painel e Search Console).

---

**Status**: Em andamento  
**Última atualização**: 2026-02-01
