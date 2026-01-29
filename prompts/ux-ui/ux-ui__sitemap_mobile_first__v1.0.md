# UX-UI — Sitemap Mobile-First (v1.0)

## Objetivo

Definir arquitetura de informação (sitemap) para sites modernos com foco em mobile-first, entrada via redes sociais e conversão simplificada, adaptado ao comportamento digital atual.

## Quando Usar

- Após mapear jornada do usuário e funil de conversão (Fase R)
- Quando público-alvo é majoritariamente mobile (redes sociais)
- Para negócios com foco em experiências ou produtos premium
- Quando simplicidade e conversão rápida são prioridades

## Inputs Necessários

- **Nome do negócio**
- **Público-alvo** (perfil demográfico e comportamental)
- **Canais de entrada** (Instagram, TikTok, Google, etc.)
- **Ofertas** (produtos, serviços, experiências)
- **Canais de conversão** (WhatsApp, checkout, agendamento)
- **Referências visuais** (sites de inspiração)

## Prompt

```
Você é um especialista em arquitetura de informação para sites mobile-first, focado em comportamento digital moderno e conversão simplificada.

CONTEXTO DO NEGÓCIO:
- Nome: [NOME DO NEGÓCIO]
- Público-alvo: [PERFIL DEMOGRÁFICO E COMPORTAMENTAL]
- Canais de entrada: [INSTAGRAM, TIKTOK, GOOGLE, ETC.]
- Ofertas: [PRODUTOS, SERVIÇOS, EXPERIÊNCIAS]
- Canais de conversão: [WHATSAPP, CHECKOUT, AGENDAMENTO]
- Referências visuais: [SITES DE INSPIRAÇÃO]

TAREFA:
Defina a arquitetura de informação seguindo estes princípios:

1. ANÁLISE DE COMPORTAMENTO DIGITAL
   - Como o público-alvo consome conteúdo?
   - Quais canais de entrada são principais?
   - Qual a tolerância a fricção?
   - Blog tradicional é relevante para esse público?

2. ESTRUTURA SIMPLIFICADA
   - Máximo 5 páginas no menu principal
   - Cada página com propósito claro
   - Fluxos de conversão em 2-3 cliques
   - Sem páginas desnecessárias

3. NAVEGAÇÃO MOBILE-FIRST
   - Menu hambúrguer para mobile
   - CTAs acessíveis com polegar
   - Touch targets adequados
   - Carregamento rápido

4. ESTRATÉGIA DE AUTORIDADE
   - Blog tradicional é eficiente para esse público?
   - Alternativas: prova social, redes sociais, newsletter
   - SEO pode ser feito com blog escondido?

5. CANAIS DE CONVERSÃO
   - WhatsApp como canal principal (se aplicável)
   - Formulários são necessários?
   - Agendamento de chamadas (se aplicável)

6. ENTREGÁVEIS
   Crie os seguintes artefatos:

   a) SITEMAP COMPLETO
      - Estrutura hierárquica de páginas
      - Propósito de cada página
      - O que aparece no menu vs escondido

   b) NAVEGAÇÃO
      - Header (mobile e desktop)
      - Footer
      - Elementos fixos (sticky)

   c) CONTEÚDO MÍNIMO POR PÁGINA
      - O que cada página deve conter
      - CTAs por página

   d) FLUXOS DE CONVERSÃO
      - Do canal de entrada até conversão
      - Máximo 2-3 cliques

RESTRIÇÕES:
- Mobile-first obrigatório
- Máximo 5 páginas no menu principal
- Evitar formulários se público prefere WhatsApp
- Blog apenas se realmente necessário para público
- Simplicidade radical sobre completude

OUTPUT ESPERADO:
- Sitemap completo e simplificado
- Navegação mobile-first
- Conteúdo mínimo por página
- Fluxos de conversão em 2-3 cliques
- Estratégia de autoridade adaptada ao público
```

## Output Esperado

### Critérios de Sucesso

1. **Estrutura simplificada**
   - Máximo 5 páginas no menu
   - Propósito claro por página
   - Sem páginas desnecessárias

2. **Mobile-first**
   - Navegação intuitiva no celular
   - CTAs acessíveis
   - Carregamento rápido

3. **Fluxos curtos**
   - Conversão em 2-3 cliques
   - Sem fricção desnecessária

4. **Autoridade adaptada**
   - Estratégia que funciona para o público
   - Blog apenas se necessário (pode ser escondido)

### Formato de Saída

```markdown
# Arquitetura de Informação — [NOME DO NEGÓCIO]

## Análise de Comportamento
- Público: [...]
- Canais de entrada: [...]
- Decisão sobre blog: [...]

## Sitemap
/
├── / (Home)
├── /[pagina-1]
├── /[pagina-2]
└── /[pagina-n]

## Navegação
- Header: [...]
- Footer: [...]
- Elementos fixos: [...]

## Conteúdo por Página
- Home: [...]
- [Página 1]: [...]
[...]

## Fluxos de Conversão
1. [Entrada] → [Página] → [Conversão]
[...]
```

## Versões

- **v1.0** (2025-01-26): Versão inicial criada durante Lição R3 do curso ARCOS™
  - Baseado em caso piloto: Verde Barro Cerâmica
  - Foco em público jovem (25-35), redes sociais, mobile-first
  - Referência: meubenza.com.br
  - Inclui estratégia de autoridade sem blog tradicional

---

## Notas de Uso

- Este prompt é para públicos mobile-first com entrada via redes sociais
- Para públicos mais tradicionais, considerar blog no menu principal
- Para B2B, formulários podem ser necessários
- Sempre testar com usuários reais após implementação

---

**Criado em**: 2025-01-26  
**Última atualização**: 2025-01-26  
**Próxima revisão**: Após uso em 3+ projetos
