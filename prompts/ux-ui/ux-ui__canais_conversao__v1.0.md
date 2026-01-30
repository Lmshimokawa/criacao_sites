# UX-UI — Canais de Conversão (v1.0)

## Objetivo

Definir canais de conversão completos para sites de experiências/serviços, incluindo fluxos, integrações técnicas, automações e especificações por canal.

## Quando Usar

- Após definir copy das páginas
- Antes de implementar o site
- Para mapear toda a infraestrutura de conversão
- Quando há múltiplos canais (WhatsApp, checkout, email)

## Inputs Necessários

- **Ofertas** (produtos/serviços com preços)
- **Público-alvo** (preferências de canal)
- **Fluxos de conversão** (da Fase R)
- **Wireframes** (pontos de conversão)
- **Requisitos especiais** (checkout compartilhável, agendamento, etc.)

## Prompt

```
Você é um especialista em UX e sistemas de conversão para 
negócios de experiências/serviços premium.

CONTEXTO:
- Negócio: [NOME]
- Ofertas: [LISTA COM PREÇOS]
- Público-alvo: [PERFIL E PREFERÊNCIAS]
- Canais desejados: [WHATSAPP, CHECKOUT, EMAIL, ETC.]
- Requisitos especiais: [EX: CHECKOUT COMPARTILHÁVEL]

TAREFA:
Defina todos os canais de conversão seguindo esta estrutura:

1. MAPA DE CANAIS
   - Diagrama visual de todos os canais
   - Como se conectam
   - Qual canal para qual finalidade

2. PARA CADA CANAL, ESPECIFIQUE:
   
   a) WHATSAPP
   - Tipo: Click-to-chat ou API
   - Mensagens pré-preenchidas por contexto
   - Horário de atendimento
   - Mensagens automáticas fora do horário
   
   b) CHECKOUT
   - Fluxo completo (etapas)
   - Campos por etapa
   - Métodos de pagamento
   - Gateway recomendado
   - Emails automáticos
   
   c) AGENDAMENTO
   - Ferramenta (Calendly, Cal.com, próprio)
   - Campos necessários
   - Disponibilidade
   - Confirmações
   
   d) EMAIL/NEWSLETTER
   - Ferramenta
   - Listas/segmentos
   - Automações (welcome, carrinho abandonado, pós-compra)
   - Timing de cada email

3. REGRAS DE NEGÓCIO
   - Timeouts e expirações
   - Cancelamentos e reembolsos
   - Casos especiais

4. INTEGRAÇÕES TÉCNICAS
   - Stack recomendada
   - Fluxo de dados
   - Webhooks necessários

5. TRADE-OFFS E RISCOS
   - O que pode dar errado
   - Como mitigar

OUTPUT ESPERADO:
- Mapa visual de canais
- Especificação detalhada de cada canal
- Fluxos completos com todas as etapas
- Regras de negócio
- Stack técnica recomendada
```

## Output Esperado

### Critérios de Sucesso

1. **Cobertura completa**
   - Todos os canais mapeados
   - Todas as etapas documentadas
   - Casos de erro considerados

2. **Praticidade**
   - Especificações implementáveis
   - Stack realista
   - Ferramentas disponíveis

3. **Experiência do usuário**
   - Fluxos curtos
   - Feedback em cada etapa
   - Múltiplas opções

4. **Escalabilidade**
   - Começar simples
   - Caminho para crescer
   - Automações planejadas

### Formato de Saída

```markdown
# Canais de Conversão — [NOME]

## Mapa de Canais
[Diagrama ASCII]

## Canal: [NOME]

### Especificações
[Detalhes técnicos]

### Fluxo
[Etapas]

### Mensagens/Emails
[Templates]

---

## Regras de Negócio
[Lista]

## Integrações
[Stack e fluxo de dados]
```

## Versões

- **v1.0** (2025-01-28): Versão inicial criada durante Lição C3 do curso ARCOS™
  - Baseado em caso piloto: Verde Barro Cerâmica
  - Inclui checkout compartilhável para grupos
  - Automações de email detalhadas

---

**Criado em**: 2025-01-28  
**Última atualização**: 2025-01-28
