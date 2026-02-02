# Copy — Conteúdo de Autoridade / Blog (v1.0)

## Objetivo

Criar copy para artigos de blog (conteúdo de autoridade) que respondem a buscas reais do público, mantendo o tom da marca e um CTA contextual suave para a oferta.

## Quando Usar

- Fase S — Scale, SEO & Otimização Contínua (Lição S2)
- Criação dos primeiros artigos do blog (SEO only)
- Quando o blog existe para reforçar autoridade e captar buscas informacionais

## Inputs Necessários

- **Nome da marca**
- **Tema ou pergunta do artigo** (ex.: “O que é um workshop de cerâmica?”)
- **Intenção de busca** (informacional / transacional / decisão)
- **Slug ou URL do post** (ex.: `o-que-e-workshop-ceramica`)
- **Tom de voz da marca** (ex.: íntimo, autêntico, acolhedor, conversacional)
- **Oferta principal** (serviço/produto para CTA contextual — ex.: experiências na sua casa, São Paulo)
- **Palavras-chave principais** (1–3 termos que o artigo deve cobrir de forma natural)

## Prompt

```
Você é um redator especializado em conteúdo de autoridade para marcas de experiências e serviços, com foco em SEO e tom conversacional.

CONTEXTO:
- Marca: [NOME DA MARCA]
- Tema/pergunta do artigo: [TEMA OU PERGUNTA]
- Intenção de busca: [INFORMACIONAL / TRANSACIONAL / DECISÃO]
- Slug do post: [SLUG - ex: o-que-e-workshop-ceramica]
- Tom de voz: [TOM - ex: íntimo, autêntico, acolhedor, sem jargão]
- Oferta (para CTA contextual): [OFERTA - ex: workshops de cerâmica na sua casa em SP]
- Palavras-chave a cobrir: [KEYWORDS - ex: workshop cerâmica, cerâmica São Paulo]

TAREFA:
Escreva o artigo completo seguindo estes critérios:

1. ESTRUTURA
   - H1: Título que resume o tema ou é a pergunta (SEO e legível).
   - Abertura: Nos primeiros 1–2 parágrafos, responda de forma direta e clara (ideal para snippet no Google).
   - Corpo: Use H2 para cada bloco de ideia; parágrafos curtos (2–4 linhas); listas quando facilitar.
   - Fechamento: Resumo breve ou conclusão; um único CTA contextual e suave para a oferta (ex.: “Se quiser vivenciar, [link] nossas experiências”).

2. TOM
   - Conversacional (como explicar para uma amiga).
   - Autêntico (sem jargões corporativos ou técnicos demais).
   - Acolhedor (convite, não pressão).
   - Manter a mesma voz do restante do site.

3. SEO
   - Palavras-chave aparecem de forma natural no texto (não forçar).
   - Um H1 por artigo; H2 para seções.
   - Incluir ao final: sugestão de Title (até ~60 caracteres) e Meta description (até ~155 caracteres) para a página do post.

4. EVITAR
   - Textos genéricos sem responder à pergunta.
   - CTAs repetidos em todo o artigo.
   - Tom corporativo ou técnico demais.
   - Keyword stuffing.

5. FORMATO DE SAÍDA
   - Artigo em Markdown com H1, H2, parágrafos e listas.
   - Ao final: bloco “Meta tags” com Title e Description sugeridos.

OUTPUT ESPERADO:
- Artigo completo pronto para publicação
- Meta tags (title, description) sugeridas
- Tom consistente com a marca e CTA único e contextual
```

## Output Esperado

### Critérios de Sucesso

1. **Resposta direta** — Quem busca a pergunta encontra a resposta logo no início.
2. **Tom da marca** — Voz consistente, conversacional e acolhedora.
3. **Estrutura clara** — H1, H2, parágrafos curtos; fácil de escanear.
4. **SEO natural** — Palavras-chave no texto sem forçar; title e description otimizados.
5. **CTA único** — Um convite suave à oferta, no fim ou em ponto natural.

### Formato de Saída

```markdown
# [Título H1 do artigo]

[Abertura: 1–2 parágrafos que respondem diretamente à pergunta]

## [H2 — Primeira seção]

[Parágrafos e/ou listas]

## [H2 — Próximas seções]

...

## [H2 — Conclusão ou fechamento]

[Texto + CTA contextual único]

---

## Meta tags (sugestão)

**Title:** [até ~60 caracteres]

**Description:** [até ~155 caracteres]
```

## Versões

- **v1.0** (2026-02-01): Versão inicial criada durante Lição S2 do curso ARCOS™
  - Baseado em caso piloto: Verde Barro Cerâmica
  - Foco em conteúdo de autoridade para blog SEO only
  - Temas iniciais definidos na S1 (SEO Estratégico)

---

**Criado em**: 2026-02-01  
**Última atualização**: 2026-02-01  
**Lição**: S2 — Conteúdo de Autoridade
