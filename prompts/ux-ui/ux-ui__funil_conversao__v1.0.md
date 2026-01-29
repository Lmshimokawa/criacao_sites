# UX-UI — Funil de Conversão (v1.0)

## Objetivo

Definir o funil de conversão do negócio, organizando os estágios do relacionamento com o cliente (topo, meio e fundo de funil), identificando canais de entrada, conversões primárias e secundárias, e definindo CTAs contextuais.

## Quando Usar

- Após mapear jornada do usuário (Fase R — Ritual do Usuário, Lição R2)
- Antes de criar sitemap e arquitetura de informação
- Quando há necessidade de estruturar processo de conversão
- Para definir CTAs e canais de entrada

## Inputs Necessários

- **Nome do negócio**
- **Proposta de valor** (da Fase A)
- **Posicionamento** (da Fase A)
- **Oferta** (da Fase A)
- **Jornada do usuário** (da Lição R1)
- **Perfis de cliente** (se houver múltiplos)
- **Canais disponíveis** (WhatsApp, formulário, etc.)

## Prompt

```
Você é um especialista em funil de conversão e estratégia de marketing digital.

CONTEXTO DO NEGÓCIO:
- Nome: [NOME DO NEGÓCIO]
- Proposta de valor: [PROPOSTA DE VALOR]
- Posicionamento: [POSICIONAMENTO]
- Oferta: [OFERTA]
- Jornada do usuário: [RESUMO DA JORNADA]
- Perfis de cliente: [PERFIS, SE HOUVER]
- Canais disponíveis: [CANAIS]

TAREFA:
Defina o funil de conversão seguindo estas etapas:

1. ESTRUTURA DO FUNIL
   - Defina estágios do funil (TOFU, MOFU, BOFU, Pós-conversão)
   - Identifique objetivo de cada estágio
   - Mapeie ações do cliente por estágio

2. CANAIS DE ENTRADA
   - Liste canais de entrada (redes sociais, busca, indicação, etc.)
   - Defina estratégia para cada canal
   - Mapeie fluxo de conversão por canal

3. CONVERSÕES
   - Identifique conversões primárias (venda final)
   - Identifique conversões secundárias (leads, interesse)
   - Mapeie fluxo entre conversões secundárias e primárias

4. CTAs (Call-to-Action)
   - Defina CTA principal (fundo de funil)
   - Defina CTAs contextuais por estágio
   - Garanta clareza e alinhamento com proposta de valor

5. MÚLTIPLOS FUNIS (se aplicável)
   - Identifique funis paralelos (se houver múltiplos perfis/ofertas)
   - Defina estratégia de conversão entre funis
   - Mapeie caminhos de conversão

6. ENTREGÁVEIS
   Crie os seguintes artefatos:

   a) FUNIL DESENHADO
      - Estrutura completa (TOFU, MOFU, BOFU, Pós)
      - Objetivo, ações e conversões por estágio
      - Canais de entrada mapeados

   b) CTA PRINCIPAL E CONTEXTUAIS
      - CTA principal (fundo de funil)
      - CTAs contextuais por estágio
      - Alinhamento com proposta de valor

   c) CANAIS DE ENTRADA
      - Lista de canais com estratégia
      - Fluxo de conversão por canal

RESTRIÇÕES:
- Não simplifique conceitos importantes
- Considere múltiplos pontos de entrada
- Defina CTAs claros e contextuais
- Não assuma funil linear rígido
- Considere pós-conversão (retenção, advocacy)

OUTPUT ESPERADO:
- Funil completo desenhado (4 estágios)
- Canais de entrada mapeados
- CTA principal e contextuais definidos
- Conversões primárias e secundárias identificadas
- Múltiplos funis (se aplicável)
```

## Output Esperado

### Critérios de Sucesso

1. **Funil completo desenhado**
   - 4 estágios (TOFU, MOFU, BOFU, Pós-conversão)
   - Objetivo claro por estágio
   - Ações e conversões mapeadas

2. **Canais de entrada claros**
   - Lista completa de canais
   - Estratégia por canal
   - Fluxo de conversão mapeado

3. **CTAs definidos**
   - CTA principal claro
   - CTAs contextuais por estágio
   - Alinhamento com proposta de valor

4. **Conversões mapeadas**
   - Conversões primárias identificadas
   - Conversões secundárias identificadas
   - Fluxo entre elas claro

### Formato de Saída

```markdown
# Funil de Conversão — [NOME DO NEGÓCIO]

## Funil Desenhado

### TOPO DE FUNIL (TOFU) — Consciência
- **Objetivo**: [...]
- **Canais**: [...]
- **Ações do cliente**: [...]
- **Conversões secundárias**: [...]
- **CTA**: [...]

### MEIO DE FUNIL (MOFU) — Consideração
[...]

### FUNDO DE FUNIL (BOFU) — Decisão
[...]

### PÓS-CONVERSÃO — Retenção
[...]

## CTA Principal e Contextuais

### CTA Principal
[...]

### CTAs por Estágio
- TOFU: [...]
- MOFU: [...]
- BOFU: [...]
- Pós: [...]

## Canais de Entrada
1. [Canal]: [Estratégia]
2. [Canal]: [Estratégia]
[...]
```

## Versões

- **v1.0** (2025-01-26): Versão inicial criada durante Lição R2 do curso ARCOS™
  - Baseado em caso piloto: Verde Barro Cerâmica
  - Inclui funil de 4 estágios, CTAs contextuais, canais de entrada e múltiplos funis
  - Testado e validado no contexto de serviços premium e experiências

---

## Notas de Uso

- Este prompt deve ser usado APÓS mapear jornada do usuário (Lição R1)
- Para e-commerce, ajustar foco em "carrinho" e "checkout"
- Para B2B, focar mais em "qualificação de leads" e "proposta comercial"
- Sempre validar funil com dados reais após implementação

---

**Criado em**: 2025-01-26  
**Última atualização**: 2025-01-26  
**Próxima revisão**: Após uso em 3+ projetos
