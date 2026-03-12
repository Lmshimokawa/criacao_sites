# Lição I2 — Referências de Site e Direção de Design

> **Fase**: I — Implementação de Site Completo e Go-Live  
> **Status**: 🔄 Em andamento  
> **Pré-requisito**: I1 (critérios e checklist internalizados)

---

## Objetivo da Lição

Definir a **direção de design** do site com base em **1–3 sites de referência** indicados pelo aluno. O objetivo é **copiar literalmente** formato, UX, UI e estilo de branding dessas referências e **adaptar** às características específicas do negócio e da marca do aluno — para que o site final seja ultra-específico, escalável e **nunca pareça genérico, feito por IA ou por desenvolvedores preguiçosos**. A implementação (I3) segue essa direção.

---

## Camada 1: Conceitos

### Por que usar referências de site

- **Escalável:** Qualquer aluno pode trazer seus próprios exemplos (concorrentes, agências, marcas que admira) e obter um resultado alinhado ao que considera "nível agência".
- **Ultra-específico:** O formato, a UX e a UI vêm de sites reais que o aluno escolheu — não de um template padrão do curso.
- **Anti-genérico:** Evita o "look de IA" ou de template único: tipografia, grid, ritmo de seções e componentes espelham referências de qualidade, adaptados à marca.

### Copiar formato, UX, UI e estilo — depois adaptar

- **Copiar (como molde):** Estrutura de layout (hero full-width ou contido, número de colunas, blocos de seção), padrões de navegação (header fixo, menu, footer), posição e estilo de CTAs, tipo de cards e listagens, uso de imagens e espaçamento, hierarquia tipográfica (tamanhos, pesos), estilo de botões e inputs.
- **Adaptar:** Conteúdo (copy do aluno), cores e tipografia da marca do aluno, oferta específica (ex.: workshops em vez de e-commerce), tom e atmosfera da marca. O resultado é **inspirado na referência**, não uma cópia literal de conteúdo.

### O que extrair das referências

| Dimensão | O que observar e documentar |
|----------|----------------------------|
| **Layout** | Hero (altura, texto à esquerda/direita/centro, CTA), grid (1/2/3 colunas), largura máxima de conteúdo, ritmo de seções (alternância fundo branco/cinza, bordas) |
| **Navegação** | Header (logo, itens, CTA no header?), footer (colunas, links, redes), mobile (hamburger, drawer) |
| **Componentes** | Botões (filled, outline, tamanhos), cards (sombra, borda, padding), formulários (labels, placeholders, erro), listas e tabelas |
| **Tipografia** | Família para títulos e corpo, escalas (H1, H2, body, small), peso e line-height |
| **Cores e fundos** | Paleta (primária, secundária, neutros), uso de imagens de fundo, overlays |
| **Visual e mídia (protagonistas)** | Uso de **fotos, vídeos, animações e imagens de background** como protagonistas: hero com vídeo/imagem forte, seções com mídia em destaque, backgrounds que criam atmosfera, animações dinâmicas. Documentar o que será replicado/adaptado (ex.: "hero full-bleed com vídeo; seção sobre com foto grande à esquerda"). |
| **Copy / texto** | Se as referências usam **textos simples e enxutos** (frases curtas, poucos blocos longos, copy que apoia o visual); adotar esse critério na direção. |
| **Espaçamento** | Padding de seções, gap entre elementos, margens consistentes (ex.: escala 8px) |
| **Microinterações** | Hover em links e botões, transições, estados de foco (acessibilidade) |

---

## Camada 2: Aplicação — Passos para o Aluno e para a Implementação

### Passo 1: Aluno fornece 1–3 referências

O aluno deve indicar **URLs de sites** que admira (mesmo setor ou outro) e, se possível, descrever em uma frase o que quer "copiar" de cada um (ex.: "o hero minimalista do X", "a grid de serviços do Y", "as cores e o tom do Z"). Opcional: screenshots ou anotações (hero, uma página interna, footer).

**Entregável do aluno:** Lista de 1–3 URLs + frases curtas do que extrair de cada uma (layout, estilo, UX).

### Passo 2: Documentar a direção de design

Quem implementa (ou o próprio aluno, com prompt) produz um **documento de direção de design** que contém:

1. **Resumo das referências:** URL, o que foi extraído (layout, UX, estilo).
2. **Padrões adotados:** Escolha de estrutura de hero, grid, componentes (ex.: "hero centralizado com H1 + subtexto + 2 CTAs, como no site X"; "cards com borda sutil e sombra leve, como no site Y"). Incluir **visual como protagonista**: onde usar fotos, vídeos, animações e backgrounds em destaque (hero, seções, atmosfera).
3. **Copy:** Adotar **textos simples e enxutos** (frases curtas, poucos blocos longos; texto apoia o visual, não compete).
4. **Adaptação à marca:** Como a paleta, tipografia e tom da marca do aluno serão aplicados sobre esses padrões (ex.: "manter estrutura do X; cores = terracota e verde da marca; fonte títulos = Playfair, corpo = Geist").
5. **Checklist de consistência:** Lista curta de regras (ex.: "espaçamento em múltiplos de 8px"; "hero com imagem/vídeo full-bleed"; "textos enxutos em todas as seções") para a implementação em I3 seguir.

### Passo 3: Usar a direção na implementação (I3)

Na lição I3 (Páginas, Conteúdo e Branding), cada página é implementada **seguindo** esse documento: mesma estrutura de seções, mesmo tipo de componentes e mesmo nível de refinamento (espaçamento, hierarquia, estados) das referências, com conteúdo e identidade visual do aluno.

---

## Entregáveis

- [ ] **Aluno:** 1–3 URLs de referência + descrição curta do que copiar/adaptar de cada uma.
- [ ] **Curso/implementação:** Documento (ou prompt reutilizável) de **direção de design**: padrões extraídos (layout, UX, UI, estilo) + especificação de adaptação à marca e ao negócio. Arquivo sugerido: `docs/direcao_design_[projeto].md` ou seção em `INFORMACOES_PARA_O_USUARIO.md`.
- [ ] Compromisso de que I3 (e I4) seguem essa direção para atingir qualidade nível agência e evitar resultado genérico.

---

## Exemplo (Verde Barro)

- **Referência 1:** Site de ateliê de cerâmica (hero com imagem em destaque, tipografia serif, tons terrosos). Copiar: estrutura hero + seção "sobre" em duas colunas; estilo de cards de serviços.
- **Referência 2:** Site de agência de experiências (formulário em etapa única, botões grandes). Copiar: padrão de formulário e CTAs.
- **Adaptação:** Cores = paleta Verde Barro (terracota, verde suave); copy = C2; oferta = workshops e peças; manter grid e ritmo das referências.

---

## Próximos passos

Seguir para **I3 — Páginas, Conteúdo e Branding (Seguindo a Direção de Design)** e implementar cada página alinhada ao documento de direção.
