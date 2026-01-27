# Strategy — Definição da Oferta (v1.0)

## Objetivo

Definir o escopo exato da oferta, estabelecendo limites operacionais claros, expectativas do cliente e estrutura de precificação psicológica.

## Quando Usar

- Após definir proposta de valor e posicionamento (Fase A — Arquitetura de Valor, Lição A3)
- Antes de criar copy de venda e precificação
- Quando há confusão sobre o que está incluso na oferta
- Para evitar expectativas desalinhadas

## Inputs Necessários

- **Nome do negócio**
- **Proposta de valor** (da Lição A1)
- **Posicionamento** (da Lição A2)
- **Serviço/produto oferecido**
- **Limitações operacionais** (o que não pode ser oferecido)
- **Estratégia de precificação** (se houver)

## Prompt

```
Você é um estrategista de negócios especializado em definir ofertas claras e operacionais.

CONTEXTO DO NEGÓCIO:
- Nome: [NOME DO NEGÓCIO]
- Proposta de valor: [PROPOSTA DE VALOR DA LIÇÃO A1]
- Posicionamento: [POSICIONAMENTO DA LIÇÃO A2]
- Serviço/Produto: [DESCRIÇÃO]
- Limitações operacionais: [O QUE NÃO PODE SER OFERECIDO]
- Estratégia de precificação: [SE HOUVER]

TAREFA:
Defina a oferta deste negócio seguindo estas etapas:

1. ESCOPO DA OFERTA (O que está incluso)
   - Liste tudo que está incluso na oferta
   - Seja específico e claro
   - Alinhe com proposta de valor e posicionamento

2. LIMITES OPERACIONAIS (O que NÃO está incluso)
   - Liste o que NÃO está incluso
   - Explique por quê (limitações operacionais)
   - Evite expectativas desalinhadas

3. EXPECTATIVAS DO CLIENTE
   - O que o cliente PODE esperar receber
   - O que o cliente NÃO deve esperar
   - Seja realista e claro

4. REGRAS DA OFERTA
   - Regras operacionais claras
   - Condições e restrições
   - Políticas (se aplicável)

5. PRECIFICAÇÃO PSICOLÓGICA
   - Como o preço será apresentado
   - Estrutura de precificação (se houver múltiplas ofertas)
   - Justificativa psicológica (como transmite valor)

6. ENTREGÁVEIS
   Crie os seguintes artefatos:

   a) ESCOPO DA OFERTA
      - Lista clara do que está incluso
      - Lista clara do que NÃO está incluso
      - Específico e operacional

   b) REGRAS DA OFERTA
      - Regras operacionais claras
      - Condições e restrições
      - Políticas (se aplicável)

   c) EXPECTATIVAS DO CLIENTE
      - O que PODE esperar
      - O que NÃO deve esperar
      - Realista e claro

   d) PRECIFICAÇÃO PSICOLÓGICA
      - Estrutura de precificação
      - Como transmite valor
      - Justificativa psicológica

RESTRIÇÕES:
- Não simplifique conceitos importantes
- Profundidade é obrigatória em definição de oferta
- Seja específico sobre limites operacionais
- Evite prometer mais do que pode entregar
- Alinhe com proposta de valor e posicionamento

OUTPUT ESPERADO:
- Escopo completo da oferta (incluso e não incluso)
- Regras operacionais claras
- Expectativas do cliente mapeadas
- Precificação psicológica estruturada
- Justificativa para cada escolha
```

## Output Esperado

### Critérios de Sucesso

1. **Escopo claro**
   - Lista completa do que está incluso
   - Lista completa do que NÃO está incluso
   - Específico e operacional

2. **Regras operacionais**
   - Regras claras e práticas
   - Condições e restrições definidas
   - Políticas estabelecidas (se aplicável)

3. **Expectativas alinhadas**
   - Cliente sabe o que pode esperar
   - Cliente sabe o que NÃO deve esperar
   - Realista e claro

4. **Precificação psicológica**
   - Estrutura de precificação definida
   - Transmite valor, não apenas preço
   - Alinha com proposta de valor

### Formato de Saída

```markdown
# Definição da Oferta — [NOME DO NEGÓCIO]

## Escopo da Oferta

### O que está incluso
- [...]
- [...]

### O que NÃO está incluso
- [...]
- [...]

## Regras da Oferta
1. [...]
2. [...]
[...]

## Expectativas do Cliente

### O que PODE esperar
- [...]
- [...]

### O que NÃO deve esperar
- [...]
- [...]

## Precificação Psicológica
- Estrutura: [...]
- Apresentação: [...]
- Justificativa: [...]
```

## Versões

- **v1.0** (2025-01-25): Versão inicial criada durante Lição A3 do curso ARCOS™
  - Baseado em caso piloto: Verde Barro Cerâmica
  - Inclui escopo, limites, expectativas, regras e precificação psicológica
  - Testado e validado no contexto de serviços premium e experiências

---

## Notas de Uso

- Este prompt deve ser usado APÓS definir proposta de valor (Lição A1) e posicionamento (Lição A2)
- Para produtos físicos, ajustar foco em "escopo do produto" e "limites de produção"
- Para B2B, focar mais em "escopo do serviço" e "limites contratuais"
- Sempre validar oferta com público-alvo antes de usar em produção

---

**Criado em**: 2025-01-25  
**Última atualização**: 2025-01-25  
**Próxima revisão**: Após uso em 3+ projetos
