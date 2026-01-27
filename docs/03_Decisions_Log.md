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

## 📊 Estatísticas

- **Total de decisões registradas**: 10
- **Decisões pendentes**: 1
- **Última atualização**: 2025-01-25

---

**Próxima decisão esperada**: Stack tecnológica (Lição O2)
