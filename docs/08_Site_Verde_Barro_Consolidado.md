# Site Verde Barro — Documento Consolidado (Fonte Única da Verdade)

> **Objetivo**: Consolidar em um único documento todo o direcionamento, conteúdo trabalhado, definições, estratégia, estrutura, implementações realizadas e pendências do site Verde Barro Cerâmica. Este documento serve como **fonte única da verdade** para contexto, referência e otimizações futuras.  
> **Última atualização**: 2026-02-08

---

## 1. Visão geral do negócio e do site

### Negócio
- **Nome**: Verde Barro Cerâmica
- **O que é**: Workshops de cerâmica (modelagem e pintura) na casa do cliente, em São Paulo. Grupos pequenos; foco em memória, conexão e experiência íntima, não apenas técnica.
- **Oferta principal**: Experiências (família e amigos; eventos corporativos).
- **Oferta secundária**: Peças autorais (feitas à mão por Camila; cupom 20% na experiência por 2 meses).
- **Onde atende**: Grande São Paulo (presencial). Experiência virtual em planejamento.

### Objetivo do site
- Institucional + conversão (solicitação de cotação, WhatsApp, newsletter).
- Autoridade (blog, FAQ, Nossa história).
- Peças autorais como extensão de marca e entrada para a experiência.

### Posicionamento em uma linha
*Verde Barro: Experiências de cerâmica na sua casa. Transformamos encontros em memórias que duram para sempre.*

---

## 2. Referências de design e estratégia

| Referência | Uso no site |
|------------|-------------|
| **Benza** (meubenza.com.br) | Hero com headline em destaque, copy enxuto, visual protagonista, CTAs arredondados, newsletter. |
| **Lóv** (azeitelov.com) | Blocos alternados texto/imagem, frases impactantes, **header dinâmico** (transição no scroll). |
| **Pottery with a Purpose** (potterywithapurpose.com) | Modelo de negócio próximo; **Como funciona** visual (4 passos); formulário de cotação simplificado; FAQ em página dedicada colapsável; separação Família e Amigos vs Corporativo; "Where we host" → "Onde atendemos". |

Documentos detalhados no repositório:
- **Direção de design**: `verde-barro-site/docs/direcao_design_verde_barro.md`
- **Diagnóstico PWAP**: `verde-barro-site/docs/REFERENCIA_POTTERY_WITH_A_PURPOSE.md`
- **Sitemap e estrutura**: `verde-barro-site/docs/SITEMAP_ESTRUTURA.md`
- **Guia de marca**: `verde-barro-site/assets/brand/Verde_Barro_Guia_de_Marca_v3.md`

---

## 3. Direção de design e identidade

### Paleta (Guia de Marca v3)
- **Primária**: Verde Oliva `#888F5D`
- **Fundos**: Off-white Areia `#F3F0EA`
- **Acentos**: Terracota `#CFA585`
- **Textos escuros**: Verde Musgo `#4E5633`, Grafite `#3B3B3B`

### Tipografia
- Títulos: Playfair Display (serifa)
- Corpo e UI: Geist (sans-serif)

### Tom de voz
- Simples, afetuoso, "quem sabe, sabe". Sem "premium" ou "exclusivo" na copy. Cool e under the radar pela contenção, não por autopromoção.

### Padrões de UI
- Hero full-bleed com overlay para legibilidade; H1 + subtexto + 1–2 CTAs.
- Botões primários `rounded-full`; secundário outline.
- Espaçamento em múltiplos de 8px; alternância de fundos (muted/40 e branco).
- Design **mobile-first**.

---

## 4. Sitemap e rotas

| Rota | Descrição |
|------|------------|
| `/` | Home |
| `/familia-e-amigos` | Experiências privadas família e amigos (conteúdo principal de conversão) |
| `/eventos-corporativos` | Eventos corporativos (team building, wellness) |
| `/pecas` | Peças autorais |
| `/nossa-historia` | História da Verde Barro e da fundadora Camila |
| `/blog` | Blog (Notion) |
| `/faq` | Perguntas frequentes (colapsáveis) |
| `/contato` | WhatsApp primário + Colabore/Parcerias + formulário de mensagem |
| `/experiencias` | Redirect 308 para `/familia-e-amigos` |
| `/legal/privacidade` | Política de privacidade |
| `/obrigado` | Agradecimento pós-formulário (se usado) |

---

## 5. Estrutura por página (resumo)

### Home (ordem das seções)
1. Hero (full-bleed, H1 "Cerâmica que vira memória", 2 CTAs)
2. Quem leva a cerâmica até você (foto fundadora + texto + CTA Nossa história)
3. **Carrossel de ofertas** (Família e amigos, Eventos corporativos, Peças autorais) — scroll horizontal, dots, snap
4. **Como funciona** — 4 passos visuais em grid
5. Oferta experiências + CTAs (Família e amigos, Eventos corporativos)
6. **Onde realizamos** — área para mapa + banner "Atendemos apenas Grande SP"
7. **Newsletter virtual** — "Experiência virtual em breve"; avise-me
8. CTA Nossa história
9. **Quem já viveu** — depoimentos (reviews)
10. **Faça parte da comunidade** — copy sedutor (ofertas secretas, preferência, lançamentos, bastidores) + newsletter com nome opcional e checkbox aceite **marcado por padrão**
11. CTA final (Agendar experiência, Peças autorais, Fale no WhatsApp)

### Família e Amigos
- Hero oferta + CTA "Quero agendar"
- Escolha como criar: 3 ofertas (Modelagem, Pintura, Modelagem + Pintura) com **seleção dinâmica**; para cada uma: "Como funciona" (passos + inclusos)
- Por que vivenciar a experiência (4 cards)
- FAQ colapsável
- Formulário de cotação

### Eventos Corporativos
- Hero + CTA "Solicitar cotação"
- Por que times amam (4 cards)
- Como funciona (4 passos)
- Ideal para (lista)
- Formulário de cotação

### Nossa história
- Hero + storytelling: origem do nome, Camila (fundadora), por que existimos. CTAs para experiências e WhatsApp.

### FAQ
- "Como funciona" em 4 passos (resumo)
- Perguntas frequentes em accordion (workshop, prazos, local, presente, queima, cancelamento, etc.)

### Contato
- Hero "Prefere WhatsApp?"
- WhatsApp (CTA primário)
- Colabore conosco / Parcerias (dois blocos)
- Formulário de mensagem

---

## 6. Formulário único de cotação

- **Onde é usado**: Família e Amigos, Eventos Corporativos.
- **Campos obrigatórios (\*)**: experiência, número de pessoas (inteiro), nome, e-mail, localização (cidade e bairro), como chegou até nós.
- **Opcionais**: nome da empresa, WhatsApp (formatação dinâmica `(XX) XXXXX-XXXX`), agendar chamada de vídeo com Camila, observações.
- **Tipos de experiência**: Evento Corporativo | Família e Amigos: Modelagem | Família e Amigos: Pintura | Família e Amigos: Modelagem + Pintura.
- **Localização**: um único campo (cidade e bairro); sem CEP/endereço completo.
- **API**: `POST /api/solicitacao`; grava em `solicitacoes_experiencias` (Supabase). Payload novo usa `localizacao`; dados extras em `observacoes` (como_chegou, nome_empresa, chamada vídeo).

---

## 7. Header e navegação

- **Scroll**: Após ~40px, header ganha fundo arredondado e sombra; logo deixa de ser invertido (no topo, logo claro sobre fundo verde).
- **Desktop**: (1) **Layer 1** (some no scroll): grid de 3 colunas — esquerda "Acompanhe nos bastidores" + redes, **logo centralizado**, direita espaçador; centralização horizontal real. (2) **Layer 2**: logo à esquerda + nav centralizado com dropdowns.
- **Nav**: Uma linha apenas (`whitespace-nowrap`); espaçamento horizontal maior (gap-4/6). **Página ativa**: negrito + sublinhado (mesma fonte). EXPERIÊNCIAS PRIVADAS (dropdown) · PEÇAS AUTORAIS · PRESENTEIE · APRENDA (dropdown) · CONTATO.
- **Mobile**: Logo + menu hamburger; painel do menu com **font-serif** (branding); mesmo menu em lista; sem redes no header.

---

## 8. Footer e elemento global

- **Footer**: 3 colunas — marca + texto + CTAs Instagram e TikTok; links (Família e amigos, Eventos corporativos, Peças, Nossa história, Blog, FAQ, Contato, Privacidade).
- **WhatsApp flutuante**: Botão fixo canto inferior direito em **todas** as páginas (layout do site).

---

## 9. Implementações realizadas (histórico)

| Data | Escopo | Detalhe |
|------|--------|---------|
| 2026-02-08 | **Documentação** | Criados `REFERENCIA_POTTERY_WITH_A_PURPOSE.md`, `SITEMAP_ESTRUTURA.md`; atualizado `direcao_design_verde_barro.md` com PWAP e novo sitemap. |
| 2026-02-08 | **Formulário** | Formulário único de cotação (`CotacaoForm`): localização única, como chegou obrigatório, pessoas numérico, experiência com 4 opções, WhatsApp formatado, opcional empresa e chamada vídeo; API aceita payload novo e legado. |
| 2026-02-08 | **Páginas novas** | `/nossa-historia`, `/eventos-corporativos`, `/familia-e-amigos`, `/faq`. Redirect `/experiencias` → `/familia-e-amigos`. |
| 2026-02-08 | **Família e Amigos** | Hero; 3 ofertas (Modelagem, Pintura, Modelagem+Pintura) com seleção dinâmica; "Como funciona" e "Incluso" por oferta; "Por que vivenciar"; FAQ colapsável; cotação. |
| 2026-02-08 | **Home** | Carrossel de ofertas; "Como funciona" visual (4 passos); oferta experiências + CTA; "Onde realizamos" (placeholder mapa + banner SP); newsletter virtual; CTA Nossa história; Quem já viveu; comunidade (newsletter com defaultChecked e nome opcional); CTA final. |
| 2026-02-08 | **Contato** | Hero "Prefere WhatsApp?"; blocos Colabore conosco e Parcerias; formulário de mensagem. |
| 2026-02-08 | **Header** | Dinâmico no scroll; duas camadas no desktop (logo+redes que some + nav fixa); dropdowns Experiências Privadas e Aprenda; mobile com hamburger. |
| 2026-02-08 | **Footer** | Redesign com colunas, CTAs Instagram/TikTok, links atualizados. |
| 2026-02-08 | **Global** | Componente `WhatsAppFloat` no layout do site. |
| 2026-02-08 | **Newsletter** | `NewsletterForm` com props `defaultChecked`, `showName`, `submitLabel`; uso na comunidade (defaultChecked + showName) e na newsletter virtual. |
| 2026-02-08 | **Sitemap** | `sitemap.ts` atualizado com novas rotas. |
| 2026-02-08 | **Documento consolidado** | Criado `docs/08_Site_Verde_Barro_Consolidado.md` (este documento). |
| 2026-02-08 | **Header** | Layer 1 em grid 3 colunas (logo centralizado); página ativa em negrito+sublinhado; nav em 1 linha; maior espaçamento; menu mobile com font-serif. |
| 2026-02-08 | **Footer newsletter** | Layout responsivo: botão "Entrar na comunidade" abaixo do campo email em telas &lt; md para evitar truncar "Seu email". |
| 2026-02-08 | **Família e Amigos** | Grid 2 colunas fixo: ofertas à esquerda, "Como funciona" à direita no mesmo bloco vertical. |
| 2026-02-08 | **Carrossel Home** | Arraste mouse/touch com threshold 10px (CTA permanece clicável); auto-advance em loop com indexRef (0→1→2→0); dots com aria-label; removido texto "Xs · Nome da oferta". |

---

## 10. Pendências e melhorias futuras

- **Mapa "Onde atendemos"**: Substituir placeholder por mapa real (Grande SP) ou lista de cidades/regiões, mantendo visual claro e útil.
- **Prova social**: Reforçar com reviews reais (nome, contexto, foto quando autorizado); boas práticas para negócios em início.
- **Banco de dados**: Se for necessário filtrar/relatar por "como chegou" ou "nome empresa", adicionar colunas `como_chegou` e `nome_empresa` em `solicitacoes_experiencias` e preenchê-las na API.
- **reCAPTCHA**: Avaliar inclusão no formulário de cotação e no de contato se houver spam.
- **Experiência virtual**: Quando lançada, atualizar copy, FAQ e possivelmente formulário (opção "virtual" em localização).
- **Workshops públicos / Gift card / Kits / Estúdio**: Não estão no escopo atual; documentados como evolução futura no diagnóstico PWAP.

---

## 11. Documentos e arquivos de referência

| Documento | Caminho | Uso |
|------------|---------|-----|
| Guia de Marca v3 | `verde-barro-site/assets/brand/Verde_Barro_Guia_de_Marca_v3.md` | Essência, história, posicionamento, tom, identidade visual, fotografia. |
| Direção de design | `verde-barro-site/docs/direcao_design_verde_barro.md` | Referências (Benza, Lóv, PWAP), padrões de UI, checklist. |
| Referência PWAP | `verde-barro-site/docs/REFERENCIA_POTTERY_WITH_A_PURPOSE.md` | Diagnóstico estratégico do site de referência. |
| Sitemap e estrutura | `verde-barro-site/docs/SITEMAP_ESTRUTURA.md` | Rotas, formulário, header, footer, elemento global. |
| Brief fotos e vídeos | `verde-barro-site/docs/BRIEF_FOTOS_VIDEOS.md` | Assets por seção/página. |
| Log de decisões | `docs/03_Decisions_Log.md` | Decisões estratégicas e técnicas do projeto. |
| Backlog | `docs/06_Backlog.md` | Pendências e melhorias. |

---

## 12. Histórico de atualizações deste documento

| Data | Alteração |
|------|------------|
| 2026-02-08 | Criação do documento consolidado; inclusão de visão geral, referências, sitemap, estrutura por página, formulário, header/footer, implementações realizadas e pendências. |
| 2026-02-08 | Refino UX/UI: sec. 7 (Header) atualizada (grid Layer 1, ativo negrito+sublinhado, 1 linha, font-serif mobile); sec. 9 (Implementações) com entradas header, footer newsletter, Família e Amigos, carrossel; diagnóstico das interações de implementação documentado no Decisions Log (DEC-025). |

---

**Manutenção**: Este documento deve ser atualizado sempre que houver mudanças de direção, estrutura, implementação ou pendências no site Verde Barro. Use-o como contexto principal para otimizações e melhorias futuras.
