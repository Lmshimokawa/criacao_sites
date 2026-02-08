# CHECKPOINT — Fase C: Conversão sem Atrito

> **Data**: 2025-01-29  
> **Status**: ✅ Concluída  
> **Próxima fase**: O — Operação & Infraestrutura (após O: Fase I — Implementação de site completo; wireframes e copy desta fase são aplicados nas páginas na Fase I)

---

## 📋 Resumo das Decisões

### Lição C1 — Wireframes / Layout

**Entregáveis**:
- Wireframes mobile-first para todas as páginas (HOME, EXPERIÊNCIAS, PEÇAS, CONTATO)
- Fluxo completo do checkout compartilhável (organizador + convidado)
- Estrutura de seções por página
- Posicionamento de CTAs

**Princípios aplicados**:
- Mobile-first (375px referência)
- Touch targets 44x44px mínimo
- CTAs distribuídos ao longo da página
- Scroll vertical apenas
- WhatsApp flutuante sempre visível

---

### Lição C2 — Copy das Páginas

**Entregáveis**:
- Copy completo HOME (hero, sobre, ofertas, como funciona, prova social, newsletter, CTA final)
- Copy completo EXPERIÊNCIAS (tipos, formatos, incluso, FAQ, CTA)
- Copy completo CHECKOUT COMPARTILHÁVEL (todas as telas do fluxo)
- Copy completo PEÇAS AUTORAIS (hero, história, combo, catálogo, FAQ)
- Copy completo CONTATO (WhatsApp, chamada de vídeo, redes, email)
- Elementos globais (header, footer, meta tags SEO)

**Tom de voz definido**:
- Íntimo: como conversa entre amigas
- Autêntico: sem jargões corporativos
- Acolhedor: convite, não pressão
- Poético mas acessível

**Headlines principais**:
- HOME: "Cerâmica que vira memória"
- EXPERIÊNCIAS: "Experiências de Cerâmica — Na sua casa, em São Paulo"
- PEÇAS: "Peças Autorais — Arte única para sua casa"
- CONTATO: "Vamos conversar?"

---

### Lição C3 — Canais de Conversão

**Canais definidos**:

| Canal | Uso | Status |
|-------|-----|--------|
| WhatsApp | Dúvidas, atendimento, vendas complexas | Click-to-chat inicial |
| Checkout Individual | Experiências (pagar por todos) | Fluxo 7 etapas |
| Checkout Compartilhável | Experiências (dividir pagamento) | Fluxo completo |
| Checkout E-commerce | Peças autorais | Carrinho + checkout |
| Agendamento | Marcar data da experiência | Cal.com/Calendly |
| Email | Automações e marketing | ConvertKit/Resend |
| Chamada de Vídeo | Conhecer o trabalho | Calendly + Meet |

**Automações de email definidas**:
- Welcome sequence (3 emails)
- Carrinho abandonado (3 emails)
- Pós-compra experiência (4 emails)
- Pós-compra peça (3 emails)

**Stack técnica recomendada**:
- Frontend: Next.js / Astro
- Hospedagem: Vercel / Netlify
- Pagamentos: Stripe / Mercado Pago
- Email transacional: Resend
- Email marketing: ConvertKit
- Agendamento: Cal.com
- Analytics: Plausible / GA4

---

## 🔗 Checkout Compartilhável — Especificação Completa

**Fluxo do Organizador**:
1. Seleciona experiência e número de pessoas
2. Escolhe "Vamos dividir"
3. Preenche dados e paga sua parte (opcional)
4. Recebe link único
5. Compartilha via WhatsApp/Instagram
6. Acompanha confirmações
7. Quando completo, agenda data

**Fluxo do Convidado**:
1. Recebe link do organizador
2. Vê quem convidou e detalhes
3. Vê barra de progresso (X/Y confirmados)
4. Paga sua parte
5. Recebe confirmação
6. Aguarda data ser agendada

**Regras de negócio**:
- Link válido por 7 dias
- Lembretes automáticos: dia 3, 5, 7
- Mínimo 2 pessoas para agendar
- Organizador pode agendar com vagas abertas
- Cancelamento individual: crédito para futura experiência

---

## ⚠️ Riscos e Trade-offs Identificados

### Riscos

**1. Checkout compartilhável não funciona**
- **Risco**: Grupos não fecham, links expiram
- **Mitigação**: Lembretes, opção de pagar diferença, timeout claro
- **Status**: A monitorar na implementação

**2. WhatsApp sobrecarregado**
- **Risco**: Demanda maior que capacidade de atendimento
- **Mitigação**: FAQ completo, mensagens automáticas, horários claros
- **Status**: Começar com click-to-chat, migrar para API se necessário

**3. Copy não ressoa**
- **Risco**: Tom de voz não conecta com público
- **Mitigação**: Testar com público real, iterar
- **Status**: A validar

### Trade-offs Aceitos

**1. Click-to-chat vs WhatsApp API**
- **Escolha**: Click-to-chat inicial
- **Trade-off**: Não escala, manual
- **Justificativa**: Validar demanda antes de investir em automação

**2. Agendamento externo vs Próprio**
- **Escolha**: Cal.com/Calendly
- **Trade-off**: Menos controle, custo
- **Justificativa**: Rápido de implementar, validar primeiro

**3. Checkout próprio vs Plataforma**
- **Escolha**: Próprio (para checkout compartilhável)
- **Trade-off**: Desenvolvimento complexo
- **Justificativa**: Funcionalidade é diferencial do produto

---

## 📝 Itens a Revisar

### Antes de Implementar

1. **Valores de preços**
   - Preço por pessoa para modelagem
   - Preço por pessoa para pintura
   - Preços das peças autorais

2. **Políticas**
   - Política de cancelamento detalhada
   - Política de reembolso
   - Termos de uso do checkout compartilhável

3. **Logística de agendamento**
   - Horários disponíveis
   - Antecedência mínima
   - Região de atendimento (Grande SP)

### Durante Implementação

1. **Testar fluxos**
   - Checkout individual funciona?
   - Checkout compartilhável funciona?
   - Links compartilhados funcionam?

2. **Testar copy**
   - Tom ressoa com público?
   - Informações estão claras?
   - CTAs convertem?

3. **Testar integrações**
   - Pagamentos processam?
   - Emails enviam?
   - Agendamento sincroniza?

---

## 📚 Lista Final de Prompts Aprovados

### UX-UI

1. **`ux-ui__wireframes_mobile_first__v1.0.md`**
   - **Criado em**: 2025-01-28
   - **Status**: ✅ Aprovado
   - **Uso**: Criar wireframes mobile-first para sites de experiências

2. **`ux-ui__canais_conversao__v1.0.md`**
   - **Criado em**: 2025-01-28
   - **Status**: ✅ Aprovado
   - **Uso**: Definir canais de conversão e integrações

### Copy

1. **`copy__paginas_experiencias__v1.0.md`**
   - **Criado em**: 2025-01-28
   - **Status**: ✅ Aprovado
   - **Uso**: Criar copy para sites de experiências premium

---

## ✅ Validações Realizadas

### Consistências Verificadas

- ✅ Wireframes seguem sitemap da Fase R
- ✅ Copy alinha com proposta de valor da Fase A
- ✅ Tom de voz consistente em todas as páginas
- ✅ Canais de conversão cobrem todos os fluxos mapeados
- ✅ Checkout compartilhável alinha com DEC-018
- ✅ Experiências para grupos (2-8) alinha com DEC-017
- ✅ Ofertas (modelagem + pintura) alinham com DEC-016

---

## 🎯 Próximos Passos

1. **Fase O — Operação & Infraestrutura**
   - Lição O1: Como um Site Funciona
   - Lição O2: Escolha de Stack
   - Lição O3: Implementação

2. **Decisões pendentes para Fase O**:
   - Stack definitiva (Next.js vs Astro vs outro)
   - Gateway de pagamento (Stripe vs Mercado Pago)
   - Hospedagem (Vercel vs Netlify vs outro)
   - CMS para peças e blog (se necessário)

---

## 📊 Métricas da Fase C

- **Lições concluídas**: 3/3 (100%)
- **Prompts criados**: 3 (total: 9)
- **Wireframes criados**: 5 páginas + 1 fluxo
- **Copy criado**: 5 páginas + elementos globais
- **Canais definidos**: 7
- **Automações de email**: 4 sequences

---

## 🔄 Notas Finais

A Fase C entregou todos os artefatos de conversão:

**Wireframes**: Estrutura visual mobile-first para todas as páginas, com foco em conversão e usabilidade.

**Copy**: Texto completo com tom íntimo e conversacional, alinhado com proposta de valor. Cada página conta uma história que guia para a conversão.

**Canais**: Sistema completo de conversão com múltiplas opções (WhatsApp, checkout, agendamento), destacando o checkout compartilhável como diferencial.

A Fase O irá transformar esses artefatos em um site funcional, definindo stack, implementando código e preparando para deploy.

---

**Última atualização**: 2025-01-28  
**Próxima revisão**: Após conclusão da Fase O
