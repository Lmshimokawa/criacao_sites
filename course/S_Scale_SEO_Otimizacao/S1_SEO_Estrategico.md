# Lição S1 — SEO Estratégico

> **Fase**: S — Scale, SEO & Otimização Contínua  
> **Status**: ✅ Concluída  
> **Data de conclusão**: 2026-02-01

---

## 🎯 Objetivo da Lição

Definir a **estrutura editorial** e a **estratégia de SEO** do site Verde Barro para aparecer no Google e em assistentes/LLMs quando o usuário buscar por workshops de cerâmica em São Paulo, mantendo o blog em papel secundário (SEO only, fora do menu principal).

---

## 📚 Camada 1: Conceitos

### SEO em uma frase

**SEO (Search Engine Optimization)** é o conjunto de práticas para que seu site seja encontrado pelo Google (e outros buscadores) quando alguém pesquisa termos relacionados ao seu negócio — sem pagar por anúncios.

### Por que importa para a Verde Barro

- **Objetivo declarado (R3):** “Ser top of mind no Google e em chats de LLM como referência de workshops de cerâmica em São Paulo.”
- **Blog:** Mantido para SEO (conteúdo que responde buscas), escondido do menu principal (público entra por redes, não por blog).
- **Páginas principais:** Home, Experiências, Peças, Contato — todas devem ter meta tags e conteúdo que o Google entenda.

### Pilares do SEO on-page

| Pilar | O que é | Exemplo Verde Barro |
|-------|---------|---------------------|
| **Título (title)** | Frase que aparece na aba e no resultado do Google | “Workshops de Cerâmica em São Paulo \| Verde Barro” |
| **Meta description** | Resumo de 1–2 linhas no resultado do Google | “Experiências de modelagem e pintura em cerâmica na sua casa. Grupos de 2 a 8 pessoas em SP.” |
| **URLs amigáveis** | Links curtos e legíveis | `/experiencias`, `/pecas`, `/legal/privacidade` |
| **Headings (H1, H2)** | Títulos que estruturam a página | Um H1 por página; H2 para seções |
| **Conteúdo relevante** | Texto que responde à intenção de busca | Palavras-chave naturais: “workshop cerâmica São Paulo”, “experiência cerâmica em casa” |
| **Estrutura técnica** | Sitemap, robots, performance | `sitemap.xml`, `robots.txt`, Core Web Vitals |

### Estrutura editorial

É o **plano de conteúdo** que sustenta o SEO: quais páginas existem, o que cada uma responde e quais termos (keywords) cada uma “cobre”. Inclui:

- **Páginas principais:** tema e foco de cada URL.
- **Blog (SEO only):** lista de temas de artigos que respondem a buscas (ex.: “como funciona workshop de cerâmica”, “cerâmica em São Paulo”).
- **Palavras-chave por página:** termos que você quer ranquear em cada URL.

---

## 📄 Camada 2: Aplicação — Verde Barro

### Regra 80/20 (Pareto) para Verde Barro

**O 20% de esforço que gera ~80% do resultado (priorizar agora):**

- **Local SEO:** título e meta description em todas as páginas principais com “São Paulo” / “SP” e termos de oferta (workshop cerâmica, experiência na sua casa). Uma única fonte de verdade para nome, endereço e contato (ex.: footer ou página Contato).
- **Páginas transacionais:** Home, Experiências, Peças e Contato com conteúdo claro, um H1 por página e URLs amigáveis (`/`, `/experiencias`, `/pecas`, `/contato`).
- **Sitemap.xml** e **robots.txt** corretos para o Google indexar as páginas certas.
- **Open Graph básico** (og:title, og:description, og:image, og:url) para quando o link for compartilhado no WhatsApp, Instagram ou redes — melhora clique e percepção de qualidade.

**O que NÃO priorizar agora (perfumaria para um site novo):**

- Schema.org (LocalBusiness, Service): traz rich results, mas exige manutenção e validação; pode vir depois.
- Blog em volume alto: 1–2 posts por mês já atendem; não criar dezenas de posts antes de medir tráfego.
- Keywords long-tail em páginas específicas para cada variação: uma página Experiências bem escrita cobre “workshop cerâmica São Paulo”, “cerâmica na sua casa”, “experiência cerâmica SP”.
- Otimização avançada de Core Web Vitals (além do básico: imagens com next/image, evitar layout shift): refinamentos podem esperar dados reais do Search Console.

### Intenção de busca do público

| Busca típica | Intenção | Onde atender no site |
|--------------|----------|----------------------|
| “workshop de cerâmica São Paulo” | Encontrar experiência em SP | Home, Experiências |
| “cerâmica na sua casa” / “workshop em casa” | Experiência no local do cliente | Experiências, Home |
| “curso de cerâmica SP” | Aprender cerâmica | Experiências (esclarecer: experiência, não curso longo) |
| “presente experiência São Paulo” | Presentear com vivência | Home, Experiências |
| “peças de cerâmica autorais” | Comprar peça | Peças autorais |
| “Verde Barro” | Conhecer a marca | Home, todas as páginas |

### Estrutura editorial (páginas + blog)

**Páginas principais (já existentes):**

| Página | URL | Foco SEO | Palavras-chave principais |
|--------|-----|----------|----------------------------|
| Home | `/` | Workshops de cerâmica em São Paulo, experiência na sua casa | workshop cerâmica São Paulo, cerâmica na sua casa, experiência cerâmica SP |
| Experiências | `/experiencias` | O que é, como funciona, modelagem e pintura, grupos | workshop modelagem cerâmica, pintura cerâmica, experiência cerâmica em casa SP |
| Peças autorais | `/pecas` | Peças autorais, entrega Brasil, combo com workshop | peças cerâmica autorais, cerâmica artesanal, presente cerâmica |
| Contato | `/contato` | Fale conosco, WhatsApp, agendar | contato Verde Barro, agendar workshop cerâmica |
| Política de privacidade | `/legal/privacidade` | Transparência (LGPD) | — (não foco de tráfego) |

**Blog (SEO only, fora do menu):**

- **Objetivo:** Conteúdo que responde a dúvidas e buscas (informacional) e reforça autoridade.
- **URL sugerida:** `/blog` (lista) e `/blog/[slug]` (post).
- **Temas sugeridos (estrutura editorial do blog):**
  - O que é um workshop de cerâmica?
  - Modelagem vs pintura em cerâmica: qual escolher?
  - Como presentear com experiência em vez de objeto?
  - Cerâmica em São Paulo: onde fazer?
  - Quantas pessoas cabem em um workshop de cerâmica?
  - Quanto tempo dura um workshop de cerâmica?
- **Frequência:** 1–2 posts por mês é suficiente para começar.

### Meta tags por página (recomendações)

Use a tabela abaixo como referência para **title** e **meta description** de cada página. Os valores já seguem as boas práticas (termo principal no início, marca no final, até ~60 e ~155 caracteres).

| Página | Title (até ~60 caracteres) | Meta description (até ~155 caracteres) |
|--------|----------------------------|----------------------------------------|
| Home | Workshops de Cerâmica em São Paulo \| Verde Barro | Experiências de modelagem e pintura em cerâmica na sua casa. Grupos de 2 a 8 pessoas em São Paulo. Agende ou presenteie. |
| Experiências | Experiências de Cerâmica na Sua Casa \| Verde Barro | Workshop de modelagem e pintura em cerâmica em SP. Na sua casa, com sua turma. Veja como funciona e agende sua experiência. |
| Peças autorais | Peças de Cerâmica Autorais \| Verde Barro | Cerâmica artesanal e peças autorais. Entrega para todo o Brasil. Compre uma peça e ganhe 20% de desconto na próxima experiência. |
| Contato | Contato \| Verde Barro Cerâmica | Fale conosco por WhatsApp ou agende uma chamada de vídeo. Dúvidas sobre workshops e peças em São Paulo. |
| Blog (lista) | Blog \| Verde Barro Cerâmica | Textos sobre cerâmica, workshops em São Paulo e experiências na sua casa. |
| Post (exemplo) | [Título do post] \| Verde Barro | [Resumo em 1–2 linhas do post] |

**Outras tags a implementar (além de title e description):** **canonical** — URL absoluta da página em todas as páginas públicas (evita duplicado). **robots** (meta tag) — use `noindex, nofollow` só em páginas de obrigado, checkout ou fluxos internos (ver regra abaixo). **Open Graph** (og:title, og:description, og:image, og:url, og:type) e **Twitter** (twitter:card, twitter:title, twitter:description, twitter:image) — para compartilhamento em redes; em geral repita os mesmos title e description da tabela; og:image em 1200×630 px (ex.: `public/og-image.jpg`). No Next.js (App Router): exportar `metadata` em `layout.tsx` ou em cada `page.tsx`; usar `metadataBase` e `openGraph`/`twitter` no layout para valores padrão.

### Meta robots e noindex (robots.txt vs meta robots)

- **robots.txt:** Diz ao buscador quais *caminhos* ele *pode* ou *não* rastrear (ex.: “não acesse /api”). Não remove páginas do índice; só controla o acesso do crawler.
- **Meta tag robots (noindex):** Diz ao buscador “não indexe esta página”. A página pode ser rastreada, mas não aparece nos resultados. Use em páginas que não devem ser encontradas por busca.

**Regra para o site Verde Barro:**

- **Indexar (não usar noindex):** Home, Experiências, Peças, Contato, Legal/privacidade, Blog (lista), cada post do blog. São páginas que você quer no Google.
- **Noindex (usar `noindex, nofollow`):** Página de obrigado/confirmação após envio (ex.: `/obrigado`), páginas de checkout ou carrinho (ex.: `/checkout`, `/pagamento`), páginas internas de fluxo que não têm valor de busca (ex.: passo 2 de um wizard). Assim você evita que o usuário caia direto em “Obrigado” ou em meio a um checkout.

No Next.js: em cada `page.tsx` dessas telas, definir `metadata = { robots: 'noindex, nofollow' }` (ou equivalente no layout da rota).

### Open Graph e Twitter Cards

**O que são:** Tags que redes sociais e mensageiros (WhatsApp, Instagram, Facebook, Twitter/X) usam para montar o “card” do link (título, descrição, imagem). Sem elas, o link pode aparecer sem imagem ou com texto genérico.

**Por que importam para a Verde Barro:** Muito do tráfego vem de redes; um link bem apresentado aumenta cliques e credibilidade. É alta alavancagem com pouco esforço.

**Tags essenciais:** `og:title`, `og:description`, `og:image`, `og:url`, `og:type`; `twitter:card`, `twitter:title`, `twitter:description`, `twitter:image`. No Next.js 14+ (App Router), isso sai do objeto `metadata` com `openGraph` e `twitter`.

**Recomendações para a imagem OG:** Tamanho 1200×630 px (proporção 1.91:1). Pode ser uma arte com logo + frase (ex.: “Workshops de cerâmica na sua casa — São Paulo”) ou uma foto de qualidade da experiência. Salvar em `public/og-image.jpg` (ou `.png`) e referenciar com URL absoluta (ex.: `https://verdebarro.com.br/og-image.jpg`). Evitar texto pequeno na imagem (fica ilegível em miniatura). Não é obrigatório usar ferramenta externa; um Canva ou export do Figma já resolve.

### Sitemap e robots (como criar e implementar)

- **O que é o sitemap:** Arquivo (em geral `sitemap.xml`) que lista as URLs que o site quer que o buscador descubra e indexe. Ajuda o Google a encontrar páginas novas ou pouco linkadas.

- **Por que é importante:** Para um site novo, o sitemap acelera a descoberta das páginas principais e do blog. É uma boa prática e fácil de implementar no Next.js.

- **Como implementar no Next.js (App Router):** Criar `app/sitemap.ts` (ou `sitemap.js`) na raiz do `app`. Exportar uma função que retorne um array de objetos com `url`, `lastModified` (opcional) e `changeFrequency` (opcional). Usar a URL base do site (ex.: `process.env.NEXT_PUBLIC_APP_URL` ou variável de ambiente). Incluir: `/`, `/experiencias`, `/pecas`, `/contato`, `/legal/privacidade`, `/blog` e, se houver, cada URL de post (ex.: buscando slugs do CMS ou de arquivos). O Next.js gera a rota `/sitemap.xml` automaticamente.

- **robots.txt:** Criar `app/robots.ts` (ou `robots.js`) exportando um objeto com `rules` (para User-Agent e allow/disallow) e opcionalmente `sitemap` com a URL do sitemap (ex.: `https://verdebarro.com.br/sitemap.xml`). Permitir crawling de `/` e bloquear apenas rotas sensíveis, por exemplo `/api`, se não quiser que sejam rastreadas. Não bloquear páginas que você queira no índice.

### LLM e assistentes

- Conteúdo bem estruturado (títulos, parágrafos claros, dados concretos) ajuda respostas em ChatGPT, Perplexity etc.
- Ter uma página “Sobre” / “Como funciona” com nome da marca, cidade, oferta e contato aumenta a chance de ser citada como referência de “workshops de cerâmica em São Paulo”.

---

## 🛠️ Camada 3: Entregáveis e Checklist

### Entregáveis da Lição S1

| Entregável | Status | Observação |
|------------|--------|------------|
| Estrutura editorial documentada | ✅ | Páginas principais + blog (temas e foco por URL) |
| Palavras-chave por página | ✅ | Tabela nesta lição |
| Meta tags recomendadas | ✅ | Title e description por página |
| Prompt reutilizável `seo__estrategia__v1.0.md` | ✅ | Para replicar estratégia em outros projetos |

### Core Web Vitals e performance

**O que são:** Métricas que o Google usa para avaliar experiência do usuário (carregamento, interatividade, estabilidade visual). Influenciam ranqueamento e são reportadas no Search Console.

- **LCP (Largest Contentful Paint):** Tempo até o maior elemento visível (ex.: hero, imagem principal) carregar. Boa: < 2,5 s. **Prática:** Usar `next/image` para imagens; priorizar imagens acima da dobra; evitar bloqueio por JS/CSS pesado.
- **INP (Interaction to Next Paint):** Tempo até a resposta à primeira interação (ex.: clique). Boa: < 200 ms. **Prática:** Evitar JS pesado no carregamento inicial; não bloquear o main thread.
- **CLS (Cumulative Layout Shift):** Instabilidade visual (elementos que “pulam” ao carregar). Boa: < 0,1. **Prática:** Definir largura/altura em imagens e embeds (ou aspect-ratio); reservar espaço para conteúdo dinâmico; evitar inserir conteúdo acima do conteúdo já visível.

**Instruções práticas para o site Verde Barro:**

- **Imagens:** Usar sempre o componente `next/image` do Next.js (lazy load, tamanhos responsivos, formato moderno quando suportado). Definir `width` e `height` (ou `fill` com container com aspect-ratio) para evitar layout shift.
- **Evitar layout shift:** Não carregar blocos de texto ou botões sem espaço reservado; usar skeleton ou altura mínima se o conteúdo vier dinâmico.
- **Reduzir JS desnecessário:** Não importar bibliotecas pesadas acima da dobra; usar dynamic import para componentes abaixo da dobra ou modais quando fizer sentido.

Não é necessário otimizar além disso no lançamento; depois de ter dados reais (Search Console, PageSpeed Insights), priorize as páginas com pior LCP ou CLS.

### Checklist de implementação (site)

- [x] Incluir **meta tags** (title, description, canonical) em todas as páginas públicas (layout ou por página).
- [x] Definir **meta robots** `noindex, nofollow` em páginas de obrigado, checkout e fluxos internos que não devem ser indexados (a implementar quando houver páginas de obrigado/checkout).
- [x] Incluir **Open Graph** e **Twitter Cards** (og:title, og:description, og:image, og:url, og:type; twitter:card, twitter:title, twitter:description, twitter:image).
- [x] Garantir **um H1 por página** e H2 para seções.
- [x] Implementar **sitemap.xml** via `app/sitemap.ts` (incluir Home, Experiências, Peças, Contato, Legal/privacidade, Blog e posts).
- [x] Configurar **robots.txt** via `app/robots.ts` (permitir /; sitemap apontando para a URL do sitemap).
- [x] Usar **next/image** para imagens e evitar layout shift (width/height ou fill + aspect-ratio).

---

## 📌 Próximos passos

1. Avançar para **S2 — Conteúdo de Autoridade** (primeiros artigos do blog). (Opcional: avaliar trocar a imagem OG por outra no futuro.)

**Implementado no `verde-barro-site`:** meta tags (title, description, canonical, openGraph) em Home (layout), Experiências, Peças, Contato e Legal/privacidade; `app/sitemap.ts`; `app/robots.ts`; metadata base com openGraph e twitter no layout raiz; **imagem OG** em `public/og-image.png` (1200×630 px — logo Verde Barro em fundo verde, referência inicial).

---

**Status**: ✅ Concluída  
**Última atualização**: 2026-02-01
