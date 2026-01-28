# UX-UI — Jornada do Usuário (v1.0)

## Objetivo

Mapear a jornada emocional e funcional completa do usuário, do primeiro contato até a conversão e além, identificando microdecisões, pontos de fricção e oportunidades de conexão.

## Quando Usar

- Após definir proposta de valor, posicionamento e oferta (Fase R — Ritual do Usuário, Lição R1)
- Antes de criar funil de conversão e sitemap
- Quando há necessidade de entender comportamento do cliente
- Para identificar pontos de fricção e oportunidades de melhoria

## Inputs Necessários

- **Nome do negócio**
- **Proposta de valor** (da Fase A)
- **Posicionamento** (da Fase A)
- **Oferta** (da Fase A)
- **Perfis de cliente** (se houver múltiplos)
- **Canais de entrada** (redes sociais, busca, indicação, etc.)

## Prompt

```
Você é um especialista em UX e jornada do usuário, focado em mapear trajetórias emocionais e funcionais.

CONTEXTO DO NEGÓCIO:
- Nome: [NOME DO NEGÓCIO]
- Proposta de valor: [PROPOSTA DE VALOR]
- Posicionamento: [POSICIONAMENTO]
- Oferta: [OFERTA]
- Perfis de cliente: [PERFIS, SE HOUVER]
- Canais de entrada: [CANAIS]

TAREFA:
Mapeie a jornada completa do usuário seguindo estas etapas:

1. IDENTIFICAÇÃO DE ETAPAS
   - Divida a jornada em 5-7 etapas principais
   - Do primeiro contato até pós-experiência
   - Considere múltiplos pontos de entrada

2. JORNADA EMOCIONAL (Por etapa)
   - Estado emocional inicial
   - Emoções durante a etapa
   - Necessidades emocionais
   - Como o cliente se sente

3. JORNADA FUNCIONAL (Por etapa)
   - Ações que o cliente realiza
   - Microdecisões que precisa tomar
   - Passos práticos
   - Canais utilizados

4. MICRODECISÕES
   - Liste todas as microdecisões por etapa
   - Identifique decisões críticas para conversão
   - Mapeie pontos de hesitação

5. PONTOS DE FRICÇÃO
   - Onde o cliente pode desistir?
   - Onde há dúvidas ou confusão?
   - Onde há atrito no processo?
   - Priorize por impacto na conversão

6. OPORTUNIDADES DE CONEXÃO
   - Onde podemos conectar emocionalmente?
   - Onde podemos facilitar a decisão?
   - Onde podemos reduzir fricção?
   - Onde podemos criar valor?

7. ENTREGÁVEIS
   Crie os seguintes artefatos:

   a) MAPA DA JORNADA COMPLETA
      - Todas as etapas mapeadas
      - Jornada emocional e funcional por etapa
      - Microdecisões identificadas
      - Pontos de fricção e oportunidades

   b) PONTOS DE FRICÇÃO E OPORTUNIDADES
      - Lista priorizada de fricções
      - Lista priorizada de oportunidades
      - Recomendações de ação

   c) MICRODECISÕES MAPEADAS
      - Lista completa de microdecisões
      - Identificação de decisões críticas
      - Sugestões de facilitação

RESTRIÇÕES:
- Não simplifique conceitos importantes
- Profundidade é obrigatória em jornada do usuário
- Considere jornada emocional E funcional
- Mapeie múltiplos pontos de entrada
- Não assuma jornada linear

OUTPUT ESPERADO:
- Mapa completo da jornada (5-7 etapas)
- Jornada emocional e funcional por etapa
- Microdecisões mapeadas
- Pontos de fricção identificados e priorizados
- Oportunidades de conexão mapeadas
- Recomendações de ação
```

## Output Esperado

### Critérios de Sucesso

1. **Jornada completa mapeada**
   - 5-7 etapas principais identificadas
   - Cobre do primeiro contato até pós-experiência
   - Considera múltiplos pontos de entrada

2. **Jornada emocional clara**
   - Estados emocionais por etapa
   - Necessidades emocionais identificadas
   - Oportunidades de conexão mapeadas

3. **Jornada funcional clara**
   - Ações por etapa
   - Microdecisões identificadas
   - Canais utilizados mapeados

4. **Pontos de fricção identificados**
   - Lista completa de fricções
   - Priorização por impacto
   - Recomendações de redução

5. **Oportunidades mapeadas**
   - Oportunidades de conexão emocional
   - Oportunidades de facilitação
   - Recomendações de ação

### Formato de Saída

```markdown
# Jornada do Usuário — [NOME DO NEGÓCIO]

## Mapa da Jornada Completa

### ETAPA 1: [Nome da Etapa]
- **Emocional**: [Estado emocional, emoções, necessidades]
- **Funcional**: [Ações, microdecisões, canais]
- **Microdecisões**: [...]
- **Fricção**: [...]
- **Oportunidade**: [...]

### ETAPA 2: [Nome da Etapa]
[...]

## Pontos de Fricção e Oportunidades

### Fricções Críticas (Prioridade Alta)
1. [...]
2. [...]

### Oportunidades de Conexão (Prioridade Alta)
1. [...]
2. [...]

## Microdecisões Mapeadas

### Por Etapa
- **Etapa 1**: [...]
- **Etapa 2**: [...]
[...]
```

## Versões

- **v1.0** (2025-01-26): Versão inicial criada durante Lição R1 do curso ARCOS™
  - Baseado em caso piloto: Verde Barro Cerâmica
  - Inclui mapeamento de jornada emocional e funcional, microdecisões, fricções e oportunidades
  - Testado e validado no contexto de serviços premium e experiências

---

## Notas de Uso

- Este prompt deve ser usado APÓS definir proposta de valor, posicionamento e oferta (Fase A)
- Para produtos físicos, ajustar foco em "jornada de compra" e "pós-compra"
- Para B2B, focar mais em "jornada de decisão" e "processo de aprovação"
- Sempre validar jornada com usuários reais antes de usar em produção

---

**Criado em**: 2025-01-26  
**Última atualização**: 2025-01-26  
**Próxima revisão**: Após uso em 3+ projetos
