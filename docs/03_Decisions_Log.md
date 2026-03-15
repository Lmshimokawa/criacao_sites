# Log de Decisões — Verde Barro Cerâmica

> **Objetivo**: Registrar todas as decisões estratégicas, técnicas e operacionais com justificativa e contexto.

---

## 📋 Formato de Registro

Cada decisão deve conter:
- **Data**: Quando foi tomada
- **Fase/Lição**: Contexto no framework ARCOS™
- **Decisão**: O que foi decidido
- **Alternativas consideradas**: O que foi rejeitado e por quê
- **Justificativa**: Motivo da escolha
- **Impacto**: O que isso afeta no projeto
- **Riscos/Trade-offs**: Limitações ou custos

---

## 🗓️ Histórico de Decisões

### DEC-001: Estrutura do Repositório
**Data**: 2025-01-25  
**Fase**: Setup inicial  
**Decisão**: Estrutura de pastas conforme especificação (docs/, prompts/, course/, src/, assets/)

**Alternativas consideradas**:
- Estrutura flat (todos os arquivos na raiz) — rejeitada por falta de organização
- Estrutura monorepo — rejeitada por complexidade desnecessária

**Justificativa**: 
- Separação clara de responsabilidades
- Facilita navegação e manutenção
- Alinha com padrões de documentação técnica

**Impacto**: 
- Organização do projeto
- Facilita onboarding
- Permite escalabilidade

**Riscos/Trade-offs**: Nenhum significativo

---

### DEC-002: Caso Piloto — Verde Barro Cerâmica
**Data**: 2025-01-25  
**Fase**: Setup inicial  
**Decisão**: Usar Verde Barro Cerâmica como caso piloto

**Contexto**:
- Negócio: Workshops premium de cerâmica (modelagem e pintura) na casa do cliente
- Objetivo do site: Institucional premium + venda de experiências
- Conversão: WhatsApp + formulário + agendamento automatizado + checkout no site
- Autoridade: Blog (conceitos de cerâmica e pintura) para SEO/confiança
- Página secundária: "Peças autorais" (extensão de marca; não pode competir com a experiência)

**Justificativa**: 
- Caso real permite profundidade prática
- Combina múltiplos elementos (experiência, autoridade, conversão)
- Desafios interessantes (premium, autoridade, extensão de marca)

**Impacto**: 
- Define todo o contexto do curso
- Influencia decisões de design, copy e estratégia

**Riscos/Trade-offs**: Nenhum

---

### DEC-003: Profundidade Obrigatória em Conceitos Estruturais
**Data**: 2025-01-25  
**Fase**: Setup inicial  
**Decisão**: Explicar conceitos estruturais em 3 camadas (definição simples, aplicação, trade-offs)

**Justificativa**: 
- Garante compreensão real, não superficial
- Permite reutilização do conhecimento
- Alinha com princípio de "não simplificar para economizar token"

**Impacto**: 
- Qualidade do curso
- Capacidade de aplicação em outros projetos

**Riscos/Trade-offs**: 
- Mais tempo/documentação por lição
- Trade-off aceito pela qualidade

---

### DEC-004: Sistema de Versionamento de Prompts
**Data**: 2025-01-25  
**Fase**: Setup inicial  
**Decisão**: Prompts versionados com formato `<categoria>__<tema>__vX.Y.md`

**Justificativa**: 
- Permite evolução sem quebrar referências
- Facilita rastreabilidade
- Padrão claro e consistente

**Impacto**: 
- Biblioteca de prompts reutilizável
- Histórico de mudanças

**Riscos/Trade-offs**: Nenhum

---

### DEC-005: Proposta de Valor — Verde Barro
**Data**: 2025-01-25  
**Fase**: A — Arquitetura de Valor (Lição A1)  
**Decisão**: Proposta de valor focada em experiência íntima, memória compartilhada e identidade autêntica, não apenas ensino técnico

**Alternativas consideradas**:
- Foco apenas em ensino técnico — rejeitada por ser genérica
- Foco apenas na peça final — rejeitada por ignorar processo emocional
- Múltiplas propostas de valor — rejeitada por criar confusão

**Justificativa**: 
- Alinha com posicionamento premium (casa do cliente, intimidade)
- Diferencia de competidores genéricos
- Conecta emocionalmente com público-alvo (busca autenticidade, slow living)
- Valor está no processo e memória, não apenas resultado técnico

**Impacto**: 
- Define toda a comunicação do site
- Influencia copy, design e CTAs
- Base para próximas lições (posicionamento, oferta, jornada)

**Riscos/Trade-offs**: 
- Risco: Expectativas desalinhadas (cliente espera "curso completo")
- Mitigação: Definição clara do escopo na Lição A3
- Trade-off: Menor volume, maior ticket (aceito por alinhar com premium)

---

### DEC-006: Posicionamento 1-linha — Verde Barro (REVISADO)
**Data**: 2025-01-25 (revisão: 2025-01-25)  
**Fase**: A — Arquitetura de Valor (Lição A1)  
**Decisão**: "Verde Barro: Workshops de cerâmica na sua casa, onde cada gesto se torna memória e cada peça carrega uma história."

**Alternativas consideradas**:
- Versão anterior com "premium" explícito — rejeitada por passar imagem elitista incompatível com conexão autêntica
- "Workshops de cerâmica em casa" — rejeitada por ser muito genérica
- "Experiências de cerâmica premium" — rejeitada por falta de especificidade e "premium" explícito
- 6 alternativas novas avaliadas (A a F) — escolhida Opção D

**Justificativa**: 
- Remove "premium" explícito, mas transmite exclusividade através de "cada gesto", "cada peça"
- Foco em memória e história (valor emocional)
- Autêntico e poético, não comercial demais
- Funciona tanto para experiência pessoal quanto presente compartilhado
- Clara sobre o que é (workshops de cerâmica) e onde (sua casa)
- Diferencia pela intimidade e pela narrativa (história, memória)

**Impacto**: 
- Usada em comunicação principal
- Base para taglines e copy
- Alinha com posicionamento autêntico (não elitista)

**Riscos/Trade-offs**: 
- Risco: Perder percepção de qualidade/exclusividade
- Mitigação: "Cada gesto", "cada peça" e "história" transmitem exclusividade implicitamente
- Trade-off aceito: Autenticidade sobre marketing explícito

---

### DEC-007: Incorporação de Dimensão Presente/Experiência Compartilhada (REVISADO)
**Data**: 2025-01-25 (revisão: 2025-01-25)  
**Fase**: A — Arquitetura de Valor (Lição A1)  
**Decisão**: Incorporar Verde Barro como solução para presente autêntico e experiência compartilhada, mas como proposta de valor SECUNDÁRIA. Core permanece experiência pessoal.

**Contexto**:
- Clientes têm dor de: pensar em presente legal, escolher presente para quem foge da materialidade fútil, dar presente que vale mais que dinheiro (momentos e memórias)
- **NOVO**: Presente é secundário, não primário. Não queremos direcionar posicionamento especialmente para presente.

**Alternativas consideradas**:
- Focar apenas em experiência pessoal — rejeitada por limitar mercado
- Focar apenas em presente — rejeitada por excluir experiência pessoal e não ser o core
- Focar principalmente em presente — rejeitada por não ser o core do negócio
- Escolhida: Experiência pessoal (CORE) + presente compartilhado (SECUNDÁRIO)

**Justificativa**: 
- Expande mercado sem diluir proposta de valor principal
- Resolve dor real de clientes (presente autêntico) sem competir com core
- Alinha com proposta de valor (memória compartilhada, experiência)
- Presente é extensão natural, não competição

**Impacto**: 
- Parágrafo institucional mantém foco em experiência pessoal (não menciona presente explicitamente)
- Tagline de presente removida (não queremos tagline explícita)
- 3 novas objeções/respostas adicionadas (presente), mas ajustadas para não mencionar "presente que vale mais que dinheiro" explicitamente
- Mensagem de presente será transmitida através de copy emocional e exemplos, não texto explícito
- Página dedicada a presentes pode existir, mas não compete com core

**Riscos/Trade-offs**: 
- Risco: Confundir proposta de valor (experiência vs presente)
- Mitigação: Comunicação clara que presente = experiência compartilhada, não objeto. Presente é secundário, não primário.
- Risco: Mensagem de presente não ficar clara
- Mitigação: Copy emocional e exemplos na página dedicada, não texto explícito
- Trade-off: Menor explícito sobre presente, mas mantém foco no core (aceito)

---

## 🔄 Decisões Pendentes

### PEND-001: Stack Tecnológica
**Fase**: O — Operação & Infraestrutura (Lição O2)  
**Status**: Aguardando proposta de 2 opções + decisão do usuário

---

### DEC-008: Posicionamento — Verde Barro
**Data**: 2025-01-25  
**Fase**: A — Arquitetura de Valor (Lição A2)  
**Decisão**: Posicionamento como "experiência íntima de cerâmica na casa do cliente", não curso, ateliê ou loja

**Alternativas consideradas**:
- Posicionar como "curso de cerâmica" — rejeitada por criar expectativa de ensino formal
- Posicionar como "ateliê de cerâmica" — rejeitada por não transmitir intimidade
- Posicionar como "loja de peças" — rejeitada por foco errado (produto vs experiência)
- Posicionar como "workshop genérico" — rejeitada por não diferenciar

**Justificativa**: 
- Alinha com proposta de valor (intimidade, experiência, memória)
- Diferencia de competidores (curso, ateliê, loja)
- Define categoria mental desejada (experiência íntima, não genérica)
- Estabelece território simbólico claro (autenticidade, intimidade, memória)

**Impacto**: 
- Define toda a comunicação do site
- Influencia copy, design e CTAs
- Base para próximas lições (oferta, jornada, funil)

**Riscos/Trade-offs**: 
- Risco: Confusão com curso/ateliê/loja
- Mitigação: Comunicação clara sobre o que NÃO é (anticompetidores)
- Trade-off: Menor volume, maior ticket (aceito por alinhar com intimidade)

---

### DEC-009: Anticompetidores — Verde Barro
**Data**: 2025-01-25  
**Fase**: A — Arquitetura de Valor (Lição A2)  
**Decisão**: Definir 6 anticompetidores claros (curso, ateliê, loja, workshop genérico, digital, produção comercial)

**Justificativa**: 
- Evita confusão com competidores
- Clareza sobre o que Verde Barro NÃO é
- Alinha com proposta de valor e posicionamento

**Impacto**: 
- Comunicação mais clara
- Expectativas alinhadas
- Diferenciação reforçada

**Riscos/Trade-offs**: Nenhum significativo

---

### DEC-010: Estratégia Inicial — Venda de Peças como Entrada
**Data**: 2025-01-25  
**Fase**: A — Arquitetura de Valor (Lição A2 - ajuste)  
**Decisão**: No início do negócio, vender peças autorais de forma secundária como estratégia de entrada, com combo obrigatório (peça = cupom 20% desconto no workshop)

**Contexto**:
- Core do negócio: Workshops de cerâmica na casa do cliente
- Estratégia inicial: Venda de peças autorais como entrada
- Objetivos: Ganhar confiança do cliente na marca, cativar com ticket menor

**Alternativas consideradas**:
- Focar apenas em workshops desde o início — rejeitada por ser mais difícil ganhar confiança inicial
- Vender peças como modelo principal — rejeitada por não ser o core do negócio
- Escolhida: Peças como estratégia secundária de entrada, com combo para converter para workshops

**Justificativa**: 
- Permite ganhar confiança do cliente com ticket menor (peça)
- Cria oportunidade de conversão para workshop (combo)
- Alinha com posicionamento (core é workshop, peças são estratégia)
- Combo obrigatório cria incentivo claro para experimentar workshop

**Impacto**: 
- Ajuste no posicionamento (peças não são core, mas são estratégia inicial)
- Define modelo de combo (peça + cupom workshop)
- Influencia precificação e estratégia de conversão

**Riscos/Trade-offs**: 
- Risco: Confundir posicionamento (parecer loja de peças)
- Mitigação: Comunicação clara que peças são estratégia de entrada, core é workshop
- Risco: Cliente comprar peça mas não usar cupom
- Mitigação: Combo obrigatório, validade de 2 meses, comunicação clara do valor
- Trade-off: Maior complexidade operacional (aceito pela estratégia de entrada)

---

### DEC-011: Público-Alvo Refinado — Verde Barro
**Data**: 2025-01-26  
**Fase**: R — Ritual do Usuário (Lição R3)  
**Decisão**: Definir público-alvo como mulheres jovens (25-35 anos), São Paulo, médio-alto poder aquisitivo, alta propensão a redes sociais (Instagram/TikTok), antenadas em trends e novas experiências

**Contexto**:
- Perfil comportamental: Consomem conteúdo em vídeos curtos, não em blogs
- Entrada principal: Instagram e TikTok
- Dispositivo: Mobile (90%+ do tráfego)
- Preferência de contato: WhatsApp (não formulários)

**Justificativa**: 
- Define todas as decisões de arquitetura e design
- Guia estratégia de autoridade (redes sociais, não blog)
- Determina mobile-first como obrigatório

**Impacto**: 
- Toda arquitetura do site
- Estratégia de conteúdo
- Canais de conversão

**Riscos/Trade-offs**: 
- Risco: Excluir públicos fora do perfil
- Mitigação: Aceito — foco é melhor que generalização

---

### DEC-012: Arquitetura Mobile-First Simplificada
**Data**: 2025-01-26  
**Fase**: R — Ritual do Usuário (Lição R3)  
**Decisão**: Estrutura ultra-simplificada com apenas 4 páginas no menu principal (Home, Experiências, Peças Autorais, Contato)

**Alternativas consideradas**:
- Estrutura completa (8+ páginas) — rejeitada por confundir público mobile
- One-page — rejeitada por limitar SEO e organização
- Escolhida: 4 páginas principais + blog escondido para SEO

**Justificativa**: 
- Público tem atenção fragmentada
- Mobile-first exige simplicidade
- Conversão em 2-3 cliques
- Referência: meubenza.com.br (estrutura simples, foco no funil)

**Impacto**: 
- Site mais simples e focado
- Melhor experiência mobile
- Conversão mais rápida

**Riscos/Trade-offs**: 
- Trade-off: Menos conteúdo detalhado
- Mitigação: Conteúdo integrado nas páginas principais

---

### DEC-013: Blog Escondido (SEO Only)
**Data**: 2025-01-26  
**Fase**: R — Ritual do Usuário (Lição R3)  
**Decisão**: Blog existe apenas para SEO e indexação em LLMs, não aparece no menu principal (apenas footer)

**Alternativas consideradas**:
- Blog no menu principal — rejeitada por público não consumir blog
- Sem blog — rejeitada por perder SEO e indexação em LLMs
- Escolhida: Blog escondido (SEO only)

**Justificativa**: 
- Público-alvo não consome blog (consome reels, stories, tiktoks)
- SEO ainda é relevante para visibilidade no Google
- Indexação em LLMs (ChatGPT, etc.) como referência de workshops em SP
- Autoridade construída via redes sociais e prova social no site

**Impacto**: 
- Blog não compete por atenção no menu
- SEO mantido como canal secundário
- Autoridade via redes sociais (Instagram, TikTok)

**Riscos/Trade-offs**: 
- Risco: SEO mais fraco sem blog visível
- Mitigação: Páginas principais otimizadas para SEO, blog existe no footer

---

### DEC-014: Contato sem Formulário — WhatsApp + Chamada de Vídeo
**Data**: 2025-01-26  
**Fase**: R — Ritual do Usuário (Lição R3)  
**Decisão**: Página de Contato com WhatsApp direto e agendamento de chamada de vídeo, sem formulário tradicional

**Alternativas consideradas**:
- Formulário de contato tradicional — rejeitada por público não usar
- Apenas email — rejeitada por criar fricção
- Escolhida: WhatsApp + chamada de vídeo + redes sociais

**Justificativa**: 
- Público-alvo prefere WhatsApp a formulários
- WhatsApp é mais natural para conversação
- Chamada de vídeo demonstra premium e personalização
- Direcionamento para redes sociais reforça comunidade

**Impacto**: 
- Conversão mais rápida (menos fricção)
- Melhor experiência para público-alvo
- Canal de atendimento mais pessoal

**Riscos/Trade-offs**: 
- Risco: Perder leads que preferem email
- Mitigação: Email disponível como texto (não formulário)

---

### DEC-015: Newsletter para Comunidade e Lista de Espera
**Data**: 2025-01-26  
**Fase**: R — Ritual do Usuário (Lição R3)  
**Decisão**: Newsletter como canal de comunidade e lista de espera, integrada na Home e Footer

**Justificativa**: 
- Canal próprio (não depende de algoritmos de redes sociais)
- Cria relacionamento com público
- Lista de espera para workshops
- Antecipa demanda

**Impacto**: 
- Canal de comunicação direta
- Construção de comunidade
- Base de leads para futuras ações

**Riscos/Trade-offs**: 
- Risco: Baixa taxa de inscrição
- Mitigação: Oferecer valor (conteúdo exclusivo, acesso antecipado)

---

### DEC-016: Ofertas Refinadas — Modelagem e Pintura
**Data**: 2025-01-28  
**Fase**: R — Ritual do Usuário (Lição R3 - ajuste)  
**Decisão**: Definir duas experiências distintas: (1) Modelagem em Cerâmica, (2) Pintura em Cerâmica, além de Peças Autorais

**Contexto**:
- Modelagem: criar peças do zero com argila
- Pintura: personalizar peças já modeladas
- Públicos e preferências diferentes

**Justificativa**: 
- Oferece opções claras para diferentes perfis
- Pintura pode ter barreira de entrada menor
- Modelagem atrai quem quer experiência mais imersiva

**Impacto**: 
- Página de experiências com dois cards de oferta
- Checkout diferenciado por tipo

**Riscos/Trade-offs**: 
- Trade-off: Mais complexidade operacional
- Mitigação: Estrutura de preços e logística alinhadas

---

### DEC-017: Experiências para Grupos Pequenos — Não 1:1
**Data**: 2025-01-28  
**Fase**: R — Ritual do Usuário (Lição R3 - ajuste)  
**Decisão**: Experiências são pensadas para grupos pequenos (não turmas grandes). O número de participantes não é fixo no site: combina-se no contato (formulário/WhatsApp) para evitar fricção. Comunicação usa "pequenos grupos", não "2 a 8 pessoas". Não haverá oferta 1:1 como padrão.

**Contexto**:
- Experiência compartilhada é o core do valor (memórias juntos)
- Operacionalmente mais eficiente
- Reforça posicionamento de experiência social

**Justificativa**: 
- Alinha com proposta de valor (criar memórias compartilhadas)
- Ticket médio maior por sessão
- Diferenciação de cursos/ateliês individuais

**Impacto**: 
- Copy e comunicação focam em grupo
- Checkout exige mínimo 2 pessoas
- FAQ esclarece regra

**Riscos/Trade-offs**: 
- Risco: Perder clientes que querem experiência solo
- Mitigação: Aceito — foco em experiência compartilhada é diferencial

---

### DEC-018: Checkout com Link Compartilhável — Pagamento Dividido
**Data**: 2025-01-28  
**Fase**: R — Ritual do Usuário (Lição R3 - ajuste)  
**Decisão**: Implementar funcionalidade de checkout com link compartilhável, permitindo que múltiplas pessoas paguem e confirmem presença de forma interativa

**Conceito**:
- Organizador gera link único da experiência
- Compartilha via WhatsApp/Instagram
- Cada convidado acessa, paga sua parte, confirma presença
- Barra de progresso visual ("3/6 confirmados")
- Quando completo, organiza agenda

**Justificativa**: 
- Facilita divisão de custos (barreira comum em grupos)
- Cria viralização orgânica (cada link = exposição da marca)
- Experiência de checkout social e interativa
- Alinhado com comportamento do público (compartilhar no WhatsApp/Instagram)

**Impacto**: 
- Desenvolvimento de funcionalidade específica no checkout
- Mini landing pages para cada link
- Potencial viral significativo

**Riscos/Trade-offs**: 
- Risco: Complexidade técnica de implementação
- Risco: Links não completados (grupos que não fecham)
- Mitigação: Timeout para links, lembretes automáticos, opção de pagar por todos

---

### DEC-019: Stack Tecnológica — Arquitetura Híbrida
**Data**: 2025-01-28  
**Fase**: O — Operação & Infraestrutura (Lição O2)  
**Decisão**: Adotar Opção A (Next.js + Vercel) com arquitetura híbrida de backend (Notion + Supabase)

**Stack escolhida**:
- **Framework**: Next.js 14 (App Router) + TypeScript
- **Estilização**: Tailwind CSS + shadcn/ui
- **CMS (conteúdo)**: Notion API
- **Banco (operações)**: Supabase (PostgreSQL)
- **Pagamentos**: Stripe
- **Email**: Resend
- **Agendamento**: Cal.com
- **Hospedagem**: Vercel

**Arquitetura híbrida**:
- **Notion**: Catálogo de peças, blog, depoimentos, FAQ (conteúdo que já é gerenciado lá)
- **Supabase**: Pedidos, checkout compartilhável, pagamentos, newsletter (operações críticas)
- **Sync opcional**: Webhook Stripe → Supabase → Notion (para controle interno)

**Justificativa**: 
- Usuário já usa Notion para gestão do negócio
- Notion API tem limitações para checkout (rate limits, latência)
- Supabase garante performance para operações críticas
- Melhor dos dois mundos: familiaridade + robustez

**Impacto**: 
- Duas fontes de dados (Notion + Supabase)
- Código para integrar ambos
- Possibilidade de sincronizar vendas para Notion

**Riscos/Trade-offs**: 
- Risco: Complexidade de duas integrações
- Mitigação: Separação clara de responsabilidades
- Trade-off: Notion para conteúdo, Supabase para operações

---

### DEC-020: Fluxo de Experiências — Agendamento antes do Pagamento
**Data**: 2025-01-28  
**Fase**: O — Operação & Infraestrutura (Lição O2 - ajuste)  
**Decisão**: Cliente primeiro agenda e solicita, você confirma, depois gera link de pagamento

**Fluxo anterior** (descartado):
1. Cliente escolhe experiência
2. Cliente paga direto no checkout
3. Depois agenda

**Fluxo novo** (aprovado):
1. Cliente preenche formulário de solicitação:
   - Experiência desejada
   - Data desejada (baseada em agenda disponível)
   - Número de participantes
   - Endereço do workshop
   - Tipo de pagamento (individual ou compartilhado)
   - Dados de contato
2. Mensagem: "Entraremos em contato para confirmar"
3. Você analisa e confirma (ou recusa se fora de área)
4. Sistema gera link de pagamento
5. Email para cliente com link
6. Cliente paga pelo link

**Justificativa**: 
- Negócio de experiências premium requer relacionamento antes do pagamento
- Permite verificar disponibilidade real
- Permite validar se atende a região
- Evita cancelamentos/reembolsos
- Cria conexão mais humanizada com cliente

**Impacto no banco de dados**:
- Nova tabela: `solicitacoes_experiencias` (pré-pagamento)
- Tabela `pedidos_experiencias` só recebe após pagamento confirmado
- Fluxo mais longo mas mais controlado

**Impacto na UX**:
- Formulário de solicitação ao invés de checkout direto
- Mensagem de "aguarde confirmação"
- Email com link de pagamento após confirmação

---

### DEC-021: Schema do Banco — Tabelas Essenciais
**Data**: 2025-01-28  
**Fase**: O — Operação & Infraestrutura (Lição O2 - ajuste)  
**Decisão**: Definir 6 tabelas essenciais no Supabase

**Tabelas**:
1. `solicitacoes_experiencias` — Agendamentos pré-pagamento
2. `pedidos_experiencias` — Experiências pagas e confirmadas
3. `pedidos_pecas` — Compras de peças autorais
4. `grupos` — Links de checkout compartilhável
5. `grupo_participantes` — Participantes de cada grupo
6. `newsletter` — Inscritos na newsletter

**Justificativa**: 
- Separação clara entre solicitação (pré) e pedido (pós pagamento)
- Tabela específica para peças (faltava)
- Newsletter mantida no Supabase para simplicidade

---

### DEC-022: Gestão de Cupons — Tabela Centralizada
**Data**: 2025-01-28  
**Fase**: O — Operação & Infraestrutura (Lição O2 - ajuste)  
**Decisão**: Criar tabela dedicada `cupons` + `cupons_uso` para gestão centralizada

**Justificativa**: 
- Parcerias com influenciadoras planejadas para próximos 6 meses
- Cupom automático de peça precisa de validade de 2 meses
- Estrutura escalável para campanhas sazonais futuras

**Tipos de cupons suportados**:
| Tipo | Origem | Exemplo |
|------|--------|---------|
| `peca_autoral` | Automático (compra peça) | PECA-A1B2C3 |
| `influenciadora` | Manual (parceria) | MARIA15 |
| `promocional` | Manual (campanha) | MAES2025 |
| `indicacao` | Automático (futuro) | REF-JOANA |

**Regra do cupom de peça autoral**:
- Desconto: 20%
- Aplica em: Experiências apenas
- Validade: **2 meses** a partir da compra
- Uso: 1 vez

**Impacto**:
- Removido campos `cupom_codigo` e `cupom_usado` de `pedidos_pecas`
- Adicionada tabela `cupons` (gestão)
- Adicionada tabela `cupons_uso` (histórico/rastreamento)

---

### DEC-023: Reestruturação do framework — Site completo e go-live obrigatório
**Data**: 2026-02-08  
**Fase**: Estrutura do curso / Framework ARCOS™  
**Decisão**: Incluir etapa obrigatória "Implementação de site completo e go-live"; critério de conclusão do curso = site 100% completo em produção, sem desenvolvimento adicional (apenas melhorias incrementais pós feedback).

**Contexto**:
- O curso foi concluído em documento (lições A–S), mas o site piloto (Verde Barro) permaneceu com placeholders, integrações pela metade e branding genérico.
- O framework não exigia, ao final, um site completo e em produção.

**Mudanças**:
- **Planejamento** (`planejamento_curso_completo_de_criacao_de_sites_de_negocios.md`): Nova seção "ETAPA OBRIGATÓRIA: IMPLEMENTAÇÃO DE SITE COMPLETO E GO-LIVE" com checklist verificável (páginas, canais de conversão, branding, conteúdo, UX, SEO, métricas, produção).
- **Checklist final do framework**: Incluído item "Site completo em produção"; "Conversão testada" e "Conteúdo publicado" refinados para refletir fluxos reais e conteúdo aplicado.
- **docs/01_ARCOS_Framework.md**: Checklist final alinhado ao planejamento.
- **docs/02_Course_Roadmap.md**: Seção da etapa go-live com checklist; status geral atualizado.
- **S3 e S4**: Adaptados para execução **após** go-live (métricas e rotina mensal fazem sentido com site no ar); adicionados "Quando executar" e "Passos práticos".

**Justificativa**: Garantir que o usuário do curso termine com um ativo real (site operando o negócio), não apenas com documentação e especificações.

**Impacto**: Todas as entregas futuras do curso devem considerar o checklist go-live; S3/S4 passam a ser "pós lançamento".

---

### DEC-024: Documento consolidado do site piloto + refino Verde Barro (PWAP, sitemap, form, header)
**Data**: 2026-02-08  
**Fase**: I — Implementação Site Go-Live / Otimização  
**Decisão**: (1) Criar documento único **08_Site_Verde_Barro_Consolidado.md** como fonte única da verdade do site Verde Barro; (2) Refinar o site com referência Pottery with a Purpose, novo sitemap, formulário único de cotação, header dinâmico, novas páginas e estrutura de Home.

**Contexto**:
- O curso precisa de uma documentação que consolide direcionamento, conteúdo, definições, estratégia, estrutura, implementações e pendências do site em desenvolvimento, para não perder trilha de auditoria e para uso como contexto em otimizações futuras.
- O site Verde Barro foi refinado com base em [Pottery with a Purpose](https://www.potterywithapurpose.com/), modelo de negócio próximo (workshops privados + corporativos).

**Decisões de implementação**:
- **Documento consolidado**: `docs/08_Site_Verde_Barro_Consolidado.md` — visão geral do negócio/site, referências de design, direção e identidade, sitemap, estrutura por página, formulário único, header/footer, histórico de implementações, pendências, e referência cruzada a demais docs.
- **Sitemap**: Rotas `/familia-e-amigos`, `/eventos-corporativos`, `/nossa-historia`, `/faq`; redirect `/experiencias` → `/familia-e-amigos`; navegação com dropdowns (Experiências Privadas, Aprenda).
- **Formulário único de cotação**: Campos obrigatórios (experiência, pessoas, nome, email, localização, como chegou); localização cidade/bairro (sem CEP); WhatsApp formatado; opcionais empresa e chamada de vídeo; API aceita payload novo.
- **Header**: Dinâmico no scroll; desktop com duas camadas (logo+redes que some + nav fixa com dropdowns); mobile com hamburger.
- **Home**: Carrossel de ofertas, Como funciona visual, oferta experiências, "Onde atendemos", newsletter virtual, CTA Nossa história, Quem já viveu, comunidade (newsletter com aceite por padrão e nome opcional), CTA final.
- **Contato**: Hero "Prefere WhatsApp?"; blocos Colabore conosco e Parcerias; formulário. **Footer**: Redesign com CTAs Instagram/TikTok. **WhatsApp flutuante** em todas as páginas.

**Justificativa**:
- Uma única fonte da verdade evita dispersão e perda de contexto ao longo do curso e em melhorias futuras.
- PWAP oferece padrões de UX/UI e estrutura de oferta alinhados ao negócio Verde Barro; refino aumenta clareza e conversão.

**Impacto**:
- Toda evolução do site deve ser refletida no documento consolidado e, quando aplicável, no Decisions Log e Backlog.
- README e fluxos "Para Desenvolver/Manter" passam a indicar o documento consolidado como primeira referência do site piloto.

**Riscos/Trade-offs**: Nenhum significativo.

---

### DEC-025: Refino UX/UI do header, footer, Família e Amigos e carrossel da Home (Verde Barro)
**Data**: 2026-02-08  
**Fase**: I — Implementação Site Go-Live / Otimização  
**Decisão**: Ajustes de alinhamento, branding, responsividade e interação no header (desktop e mobile), footer (newsletter), página Família e Amigos e carrossel de ofertas da Home, com documentação no Decisions Log e no documento consolidado do site.

**Contexto**:
- Feedback de uso: header com itens em duas linhas e página ativa com mudança de fonte estranha; footer newsletter truncando "Seu email" em larguras intermediárias; Família e Amigos com ofertas e "Como funciona" empilhados em vez de lado a lado; carrossel com arraste pouco responsivo, CTA às vezes bloqueado após arraste e auto-advance sem loop correto para a terceira oferta.

**Decisões de implementação**:
- **Header**: (1) Layer 1 desktop em grid de 3 colunas para centralização horizontal real do logo e blocos laterais. (2) Página ativa no nav em **negrito + sublinhado** (sem mudar família da fonte). (3) Itens do nav em **uma linha** (`whitespace-nowrap`). (4) Maior espaçamento horizontal entre itens (`gap-4 md:gap-6`). (5) Menu hamburger (mobile) com **font-serif** em todo o painel para alinhar ao branding.
- **Footer newsletter**: Layout email + botão em coluna abaixo do breakpoint `md`, para o placeholder "Seu email" não truncar; botão "Entrar na comunidade" abaixo do campo em telas estreitas.
- **Família e Amigos**: Grid fixo em **duas colunas** (`grid-cols-2`), ofertas à esquerda (max-width 280px) e "Como funciona" à direita no mesmo bloco vertical, em todas as larguras.
- **Carrossel Home**: (1) Arraste por mouse/touch: pointer capture só após movimento >10px, para **CTA permanecer clicável** em tap/clique. (2) Auto-advance em loop: uso de `indexRef` no setInterval para garantir avanço 0→1→2→0 (incl. "Peças autorais"). (3) Remoção do texto "Xs · Nome da oferta" ao lado do timer/dots (redundante). (4) Dots com `role="tablist"`/`role="tab"` e `aria-label` por oferta para acessibilidade.

**Justificativa**: Manter padrão de branding (serif, simetria), melhorar responsividade e usabilidade sem adicionar ruído visual; garantir que o CTA do carrossel seja o único elemento clicável para navegação e que o loop automático funcione em todas as ofertas.

**Impacto**: Header e carrossel mais consistentes e utilizáveis; documento consolidado e Decisions Log atualizados para rastreabilidade.

**Riscos/Trade-offs**: Nenhum significativo.

---

### DEC-026: Migração de assets da marca para verde-barro-site
**Data**: 2026-03-14  
**Fase**: Operação / Organização  
**Decisão**: Centralizar todos os recursos da marca Verde Barro (guia de marca, logos, imagens) em `verde-barro-site/assets/`, removendo a pasta `assets/` da raiz do repositório.

**Contexto**:
- O repositório passou a ser usado não só como base de deploy do site, mas como central de conhecimento da marca.
- Manter assets dentro do projeto do site evita duplicação e mantém uma única fonte da verdade; arquivos em `verde-barro-site/assets/` não são servidos em produção (ficam fora de `public/`), portanto não impactam a velocidade do site.

**Justificativa**: Um único lugar para documentação e assets da Verde Barro; referências em docs atualizadas para `verde-barro-site/assets/`.

**Impacto**: Estrutura do repositório (raiz sem `assets/`); documentação em `docs/` e CHANGELOG atualizados; `verde-barro-site/README.md` e `verde-barro-site/assets/README.md` documentam a pasta.

**Riscos/Trade-offs**: Nenhum significativo.

---

## 📊 Estatísticas

- **Total de decisões registradas**: 26
- **Decisões pendentes**: 0
- **Última atualização**: 2026-03-14
