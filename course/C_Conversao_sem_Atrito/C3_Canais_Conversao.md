# Lição C3 — Canais de Conversão

> **Fase**: C — Conversão sem Atrito  
> **Status**: ✅ Concluída  
> **Data de início**: 2025-01-29  
> **Data de conclusão**: 2025-01-29

---

## 🎯 Objetivo da Lição

Definir os **canais de conversão** completos para Verde Barro, especificando fluxos, integrações técnicas, automações e experiência do usuário em cada ponto de contato.

---

## 📚 Conceitos-Chave (3 Camadas)

### Camada 1: Definição Simples

**Canal de Conversão** é o meio pelo qual o cliente completa uma ação desejada (compra, agendamento, contato).

**Tipos de canais**:
- **WhatsApp**: Conversacional, pessoal, instantâneo
- **Checkout no site**: Autoatendimento, escalável, 24/7
- **Agendamento**: Calendário integrado
- **Email**: Follow-up, nutrição, automação

**Princípios de conversão sem atrito**:
- Menos cliques possível
- Informação clara em cada etapa
- Múltiplas opções (não forçar um caminho)
- Feedback imediato
- Recuperação de erros fácil

---

### Camada 2: Aplicação no Caso Verde Barro

**Contexto** (das Fases A e R):
- **Público**: Mulheres 25-35, mobile-first, preferem WhatsApp
- **Ofertas**: Modelagem, Pintura, Peças Autorais
- **Diferencial**: Checkout compartilhável para grupos
- **Abrangência**: Experiências apenas SP, Peças todo Brasil

---

## 📦 Entregáveis

### 1. Mapa de Canais de Conversão

```
┌─────────────────────────────────────────────────────────────────┐
│                    CANAIS DE CONVERSÃO                          │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  EXPERIÊNCIAS (Modelagem/Pintura)                               │
│  ─────────────────────────────────                              │
│                                                                 │
│  ┌─────────────┐    ┌─────────────┐    ┌─────────────┐          │
│  │  WhatsApp   │    │  Checkout   │    │  Checkout   │          │
│  │  (dúvidas)  │    │  Individual │    │  Compartilh.│          │
│  └──────┬──────┘    └──────┬──────┘    └──────┬──────┘          │
│         │                  │                  │                 │
│         ▼                  ▼                  ▼                 │
│  ┌─────────────────────────────────────────────────┐            │
│  │              AGENDAMENTO                        │            │
│  │         (após pagamento confirmado)             │            │
│  └─────────────────────────────────────────────────┘            │
│                                                                 │
│  PEÇAS AUTORAIS                                                 │
│  ──────────────                                                 │
│                                                                 │
│  ┌─────────────┐    ┌─────────────┐                             │
│  │  WhatsApp   │    │  Checkout   │                             │
│  │  (dúvidas)  │    │  E-commerce │                             │
│  └──────┬──────┘    └──────┬──────┘                             │
│         │                  │                                    │
│         ▼                  ▼                                    │
│  ┌─────────────────────────────────────────────────┐            │
│  │              ENTREGA                            │            │
│  │         (+ cupom 20% experiência)               │            │
│  └─────────────────────────────────────────────────┘            │
│                                                                 │
│  CONTATO GERAL                                                  │
│  ─────────────                                                  │
│                                                                 │
│  ┌─────────────┐    ┌─────────────┐    ┌─────────────┐          │
│  │  WhatsApp   │    │  Chamada    │    │  Email      │          │
│  │  (principal)│    │  de Vídeo   │    │  (backup)   │          │
│  └─────────────┘    └─────────────┘    └─────────────┘          │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

---

### 2. Canal: WhatsApp

#### Especificações

**Tipo**: WhatsApp Business API ou Click-to-Chat

**Uso**:
- Canal principal de dúvidas
- Atendimento humanizado
- Fechamento de vendas complexas
- Suporte pós-venda

**Implementação**:

```
OPÇÃO A: Click-to-Chat (Simples)
─────────────────────────────────
- Link direto: wa.me/5511XXXXXXXXX
- Mensagem pré-preenchida por contexto
- Sem custo adicional
- Atendimento manual

OPÇÃO B: WhatsApp Business API (Escalável)
──────────────────────────────────────────
- Integração via provedor (Twilio, Z-API, etc.)
- Mensagens automáticas
- Chatbot para triagem
- Custo mensal por mensagem
```

**Mensagens pré-preenchidas por contexto**:

```
HOME:
"Olá! Vim pelo site e quero saber mais sobre as experiências de cerâmica 🏺"

EXPERIÊNCIAS:
"Olá! Tenho interesse em agendar uma experiência de [modelagem/pintura]. 
Somos [X] pessoas. Pode me ajudar?"

PEÇAS:
"Olá! Vi as peças autorais no site e tenho uma dúvida sobre [peça específica]"

CHECKOUT (dúvida):
"Olá! Estou no checkout e preciso de ajuda para finalizar minha compra"

CONTATO:
"Olá! Quero falar com a Verde Barro"
```

**Horário de atendimento**:
- Segunda a sexta: 9h às 18h
- Sábado: 9h às 13h
- Fora do horário: Mensagem automática com expectativa de resposta

**Mensagem automática fora do horário**:
```
Olá! 👋

Obrigada por entrar em contato com a Verde Barro.

Nosso horário de atendimento é:
📅 Segunda a sexta: 9h às 18h
📅 Sábado: 9h às 13h

Deixe sua mensagem que respondemos assim que possível!

Enquanto isso, você pode explorar nosso site:
🔗 verdebarro.com.br
```

---

### 3. Canal: Checkout Individual (Experiências)

#### Fluxo Completo

```
ETAPA 1: SELEÇÃO
────────────────
Página: /experiencias

Usuário escolhe:
- Tipo (Modelagem / Pintura / Ambos)
- Número de pessoas (2-8)

↓

ETAPA 2: FORMA DE PAGAMENTO
───────────────────────────
Modal ou página dedicada

Opções:
- "Vou pagar por todos" → Checkout individual
- "Vamos dividir" → Checkout compartilhável

↓ (se individual)

ETAPA 3: DADOS DO COMPRADOR
───────────────────────────
Campos:
- Nome completo *
- Email *
- WhatsApp *
- CEP (para validar SP) *

↓

ETAPA 4: PAGAMENTO
──────────────────
Métodos:
- Cartão de crédito (parcelado)
- Pix (desconto 5%?)

Gateway: Stripe / Mercado Pago / PagSeguro

↓

ETAPA 5: CONFIRMAÇÃO
────────────────────
- Resumo do pedido
- Número do pedido
- Próximos passos

Email automático:
- Confirmação de pagamento
- Instruções para agendamento
- Link para agendar

↓

ETAPA 6: AGENDAMENTO
────────────────────
Opção A: Calendly / Cal.com integrado
Opção B: WhatsApp para combinar

Campos:
- Data preferida (calendário)
- Horário preferido
- Endereço completo (SP)
- Observações

↓

ETAPA 7: CONFIRMAÇÃO FINAL
──────────────────────────
Email com:
- Data e horário confirmados
- Endereço
- O que preparar
- Contato de emergência
```

---

### 4. Canal: Checkout Compartilhável (Experiências)

#### Fluxo do Organizador

```
ETAPA 1: SELEÇÃO
────────────────
(igual ao individual)

↓

ETAPA 2: CRIAR GRUPO
────────────────────
Campos:
- Nome do organizador *
- Email *
- WhatsApp *
- ☑ Já quero garantir minha vaga (pagar agora)

↓

ETAPA 3: LINK GERADO
────────────────────
Sistema gera:
- URL única: verdebarro.com.br/grupo/{hash}
- Validade: 7 dias
- Status: 1/X confirmados (se pagou)

Ações disponíveis:
- Copiar link
- Compartilhar WhatsApp
- Compartilhar Instagram

↓

ETAPA 4: ACOMPANHAMENTO
───────────────────────
Dashboard do organizador:
- Quem confirmou
- Quem falta
- Prazo restante
- Reenviar convite

Notificações:
- Email a cada nova confirmação
- WhatsApp (opcional)

↓

ETAPA 5: GRUPO COMPLETO
───────────────────────
Quando todas as vagas preenchidas:
- Email para organizador: "Grupo completo! Agende agora"
- Link para agendamento

↓

ETAPA 6-7: AGENDAMENTO E CONFIRMAÇÃO
────────────────────────────────────
(igual ao individual)
```

#### Fluxo do Convidado

```
ETAPA 1: RECEBER LINK
─────────────────────
Via WhatsApp/Instagram/Email do organizador

↓

ETAPA 2: PÁGINA DO CONVITE
──────────────────────────
URL: verdebarro.com.br/grupo/{hash}

Exibe:
- Quem convidou (nome + foto opcional)
- Qual experiência
- Preço por pessoa
- Quem já confirmou (barra de progresso)
- Vagas restantes

↓

ETAPA 3: CONFIRMAR PRESENÇA
───────────────────────────
Campos:
- Nome *
- Email *
- WhatsApp *

↓

ETAPA 4: PAGAMENTO
──────────────────
Paga apenas sua parte

↓

ETAPA 5: CONFIRMAÇÃO
────────────────────
- "Você está dentro!"
- Aguardar organizador agendar
- Adicionar ao calendário (placeholder)
```

#### Regras de Negócio

```
TIMEOUT:
- Link expira em 7 dias
- Lembretes automáticos: dia 3, dia 5, dia 7
- Após expirar: organizador pode estender ou cancelar

MÍNIMO PARA AGENDAR:
- Precisa de pelo menos 2 pessoas confirmadas
- Organizador pode agendar com vagas abertas 
  (responsabilidade de preencher ou pagar diferença)

CANCELAMENTO INDIVIDUAL:
- Participante pode cancelar em até 48h antes
- Reembolso: crédito para futura experiência
- Vaga reabre no link

CANCELAMENTO DO GRUPO:
- Apenas organizador pode cancelar
- Reembolso proporcional para todos
- Ou reagendamento
```

---

### 5. Canal: Checkout E-commerce (Peças)

#### Fluxo

```
ETAPA 1: CATÁLOGO
─────────────────
Página: /pecas

Grid de produtos com:
- Foto/video
- Nome
- Preço
- Badge "Única" (se aplicável)

↓

ETAPA 2: PÁGINA DO PRODUTO
──────────────────────────
- Galeria de fotos
- Descrição
- Dimensões
- Preço
- [Adicionar ao carrinho]

↓

ETAPA 3: CARRINHO
─────────────────
- Lista de itens
- Subtotal
- Calcular frete (CEP)
- Cupom de desconto
- [Finalizar compra]

↓

ETAPA 4: CHECKOUT
─────────────────
Campos:
- Dados pessoais (nome, email, WhatsApp)
- Endereço de entrega
- Método de pagamento

↓

ETAPA 5: CONFIRMAÇÃO
────────────────────
- Pedido confirmado
- Número do pedido
- Prazo de entrega
- Código de rastreio (após envio)

↓

ETAPA 6: PÓS-VENDA
──────────────────
Email automático:
- Confirmação do pedido
- Nota fiscal
- Código de rastreio
- CUPOM 20% EXPERIÊNCIA (válido 2 meses)
```

---

### 6. Canal: Agendamento

#### Opções de Implementação

```
OPÇÃO A: CALENDLY / CAL.COM
───────────────────────────
Prós:
- Fácil de configurar
- Sincroniza com Google Calendar
- Notificações automáticas
- Embed no site

Contras:
- Menos personalização
- Custo mensal
- Dependência externa

OPÇÃO B: AGENDAMENTO VIA WHATSAPP
─────────────────────────────────
Prós:
- Mais pessoal
- Flexibilidade total
- Sem custo adicional

Contras:
- Manual
- Não escala
- Risco de erros

OPÇÃO C: SISTEMA PRÓPRIO
────────────────────────
Prós:
- Total controle
- Integração perfeita
- Sem custos recorrentes

Contras:
- Desenvolvimento complexo
- Manutenção

RECOMENDAÇÃO: Começar com Calendly/Cal.com
         Migrar para sistema próprio quando escalar
```

#### Campos do Agendamento

```
OBRIGATÓRIOS:
- Data (calendário com disponibilidade)
- Horário (slots definidos)
- Endereço completo
  - CEP
  - Rua + número
  - Complemento
  - Bairro
  - Cidade (apenas Grande SP)
- Número de participantes confirmados

OPCIONAIS:
- Observações (alergias, preferências, etc.)
- Tem pet em casa?
- Tem estacionamento?
```

---

### 7. Canal: Newsletter / Email Marketing

#### Especificações

**Ferramenta**: Mailchimp / ConvertKit / Brevo

**Listas**:
1. **Comunidade geral**: Todos os inscritos
2. **Clientes**: Quem já comprou
3. **Leads quentes**: Carrinho abandonado, checkout incompleto

**Automações**:

```
WELCOME SEQUENCE (novos inscritos)
──────────────────────────────────
Email 1 (imediato): 
  "Bem-vinda à comunidade Verde Barro"
  - Quem somos
  - O que esperar
  - Link para experiências

Email 2 (dia 3):
  "Como nasceu a Verde Barro"
  - História da fundadora
  - Bastidores

Email 3 (dia 7):
  "Tem novidade!"
  - Próximas datas disponíveis
  - Ou peças novas

─────────────────────────────────

CARRINHO ABANDONADO
───────────────────
Email 1 (1 hora):
  "Esqueceu algo?"
  - Resumo do carrinho
  - Link para retomar

Email 2 (24 horas):
  "Ainda pensando?"
  - Depoimento de cliente
  - Link para retomar

Email 3 (48 horas):
  "Última chance"
  - Cupom de desconto? (opcional)
  - Link para retomar

─────────────────────────────────

PÓS-COMPRA (Experiência)
────────────────────────
Email 1 (dia seguinte):
  "Obrigada por escolher Verde Barro!"
  - Resumo do pedido
  - Próximos passos

Email 2 (1 dia antes):
  "Amanhã é o grande dia!"
  - O que preparar
  - Contato de emergência

Email 3 (1 dia depois):
  "Como foi?"
  - Pedido de feedback/depoimento
  - Compartilhar nas redes

Email 4 (2 semanas depois, se modelagem):
  "Suas peças estão prontas!"
  - Fotos das peças queimadas
  - Logística de entrega

─────────────────────────────────

PÓS-COMPRA (Peça)
─────────────────
Email 1 (imediato):
  "Pedido confirmado!"
  - Resumo
  - Prazo de entrega

Email 2 (envio):
  "Sua peça está a caminho!"
  - Código de rastreio
  - CUPOM 20% EXPERIÊNCIA

Email 3 (entrega):
  "Chegou?"
  - Feedback
  - Lembrete do cupom
```

---

### 8. Canal: Chamada de Vídeo

#### Especificações

**Ferramenta**: Calendly + Google Meet / Zoom

**Objetivo**: Conhecer o trabalho, tirar dúvidas, criar conexão

**Configuração**:
- Duração: 15 minutos
- Disponibilidade: 2-3 slots por semana
- Confirmação automática
- Lembrete 1h antes

**Script sugerido**:
```
1. Apresentação (2 min)
   - "Oi! Sou [Nome], criadora da Verde Barro"
   
2. Entender necessidade (5 min)
   - "O que te trouxe aqui?"
   - "É para você ou para presentear?"
   - "Quantas pessoas seriam?"

3. Apresentar (5 min)
   - Mostrar fotos/vídeos de experiências
   - Explicar como funciona
   - Responder dúvidas

4. Próximos passos (3 min)
   - "Posso te mandar o link para agendar?"
   - "Quer que eu reserve a data?"
```

---

### 9. Integrações Técnicas

#### Stack Recomendada

```
SITE:
- Next.js / Astro (frontend)
- Vercel / Netlify (hospedagem)

PAGAMENTOS:
- Stripe (internacional, fácil)
- ou Mercado Pago (BR, familiar)

EMAIL:
- Resend (transacional)
- ConvertKit (marketing)

AGENDAMENTO:
- Cal.com (open source)
- ou Calendly (mais fácil)

WHATSAPP:
- Click-to-chat (início)
- Z-API / Twilio (escalar)

ANALYTICS:
- Plausible / Fathom (privacidade)
- ou Google Analytics 4

CRM (futuro):
- Notion (simples)
- ou HubSpot (robusto)
```

#### Fluxo de Dados

```
┌─────────────┐
│   SITE      │
└──────┬──────┘
       │
       ▼
┌─────────────┐     ┌─────────────┐
│  CHECKOUT   │────▶│   STRIPE    │
└──────┬──────┘     └──────┬──────┘
       │                   │
       │                   ▼
       │           ┌─────────────┐
       │           │  WEBHOOK    │
       │           └──────┬──────┘
       │                  │
       ▼                  ▼
┌─────────────┐     ┌─────────────┐
│  DATABASE   │◀────│   EMAIL     │
│  (pedidos)  │     │  (Resend)   │
└──────┬──────┘     └─────────────┘
       │
       ▼
┌─────────────┐
│ AGENDAMENTO │
│  (Cal.com)  │
└─────────────┘
```

---

### Camada 3: Trade-offs, Riscos, Anti-padrões e Validação

#### Trade-offs

**1. WhatsApp manual vs API**
- **Escolha inicial**: Click-to-chat manual
- **Trade-off**: Não escala, depende de disponibilidade
- **Justificativa**: Começar simples, validar demanda, depois automatizar

**2. Checkout próprio vs Plataforma**
- **Escolha**: Checkout próprio (compartilhável é diferencial)
- **Trade-off**: Desenvolvimento complexo
- **Justificativa**: Funcionalidade core do produto

**3. Agendamento integrado vs Ferramenta externa**
- **Escolha inicial**: Cal.com/Calendly
- **Trade-off**: Menos controle, custo
- **Justificativa**: Rápido de implementar, validar primeiro

#### Riscos

**1. Checkout compartilhável não funciona**
- **Risco**: Grupos não fecham, links expiram
- **Mitigação**: Lembretes, opção de pagar diferença, timeout claro

**2. WhatsApp sobrecarregado**
- **Risco**: Não conseguir atender demanda
- **Mitigação**: Mensagens automáticas, FAQ no site, horários claros

**3. Pagamentos não processam**
- **Risco**: Falhas técnicas, perda de vendas
- **Mitigação**: Gateway confiável, fallback (Pix manual)

#### Anti-padrões Evitados

- ❌ Forçar único canal de conversão
- ❌ Checkout longo demais
- ❌ Sem feedback em cada etapa
- ❌ Esconder informações de contato
- ❌ Não ter plano B para falhas

---

## ✅ Checklist da Lição

- [x] Conceitos explicados (3 camadas)
- [x] Mapa de canais definido
- [x] Canal WhatsApp especificado
- [x] Checkout individual detalhado
- [x] Checkout compartilhável detalhado
- [x] Checkout e-commerce (peças) detalhado
- [x] Agendamento especificado
- [x] Newsletter/Email automações definidas
- [x] Chamada de vídeo especificada
- [x] Integrações técnicas mapeadas
- [x] Prompt reutilizável criado (`ux-ui__canais_conversao__v1.0.md`)
- [x] Logs atualizados

---

**Última atualização**: 2025-01-29
