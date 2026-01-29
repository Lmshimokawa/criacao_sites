# CHECKPOINT — Fase R: Ritual do Usuário

> **Data**: 2025-01-28  
> **Status**: ✅ Concluída  
> **Próxima fase**: C — Conversão sem Atrito

---

## 📋 Resumo das Decisões

### Lição R1 — Jornada do Usuário

**Decisões principais**:
- Jornada mapeada em 6 etapas (Descoberta → Exploração → Consideração → Decisão → Experiência → Pós-Experiência)
- Jornada não-linear com múltiplos pontos de entrada
- Foco em jornada emocional, não apenas funcional

**Entregáveis**:
- Mapa da jornada completa (6 etapas com emoções, ações, microdecisões)
- 5 pontos de fricção críticos identificados
- 5 oportunidades de conexão mapeadas
- Lista de microdecisões por etapa

---

### Lição R2 — Funil de Conversão

**Decisões principais**:
- Funil em 4 estágios (TOFU, MOFU, BOFU, Pós-conversão)
- Múltiplos canais de conversão (WhatsApp principal)
- Estratégia de conversão: Peça → Workshop via combo

**Entregáveis**:
- Funil completo desenhado
- CTA principal definido ("Agende sua experiência")
- CTAs contextuais por estágio
- Canais de entrada mapeados

---

### Lição R3 — Arquitetura de Informação (Versão Refinada)

**Decisões principais**:
- **DEC-011**: Público-alvo refinado (mulheres 25-35, SP, médio-alto poder aquisitivo, redes sociais)
- **DEC-012**: Arquitetura mobile-first simplificada (4 páginas no menu)
- **DEC-013**: Blog escondido (SEO only, fora do menu principal)
- **DEC-014**: Contato sem formulário (WhatsApp + chamada de vídeo)
- **DEC-015**: Newsletter para comunidade e lista de espera
- **DEC-016**: Ofertas refinadas (Modelagem + Pintura + Peças Autorais)
- **DEC-017**: Experiências para grupos de 2-8 pessoas (não 1:1)
- **DEC-018**: Checkout com link compartilhável (pagamento dividido, viralização)

**Entregáveis**:
- Sitemap completo e simplificado
- Hierarquia de páginas (4 principais + SEO/legal)
- Navegação mobile-first (header, footer, sticky)
- 6 fluxos de conversão mapeados
- Conteúdo mínimo por página definido
- Funcionalidade de checkout compartilhável documentada

---

## 📱 Sitemap Final

```
/
├── / (Home)
│   └── Narrativa, fundadora, história, proposta de valor, ofertas, CTAs, newsletter
│
├── /experiencias (Experiências)
│   └── Modelagem e Pintura, como funciona, preços, FAQ, agendamento
│   └── Para grupos de 2-8 pessoas
│
├── /pecas (Peças Autorais)
│   └── Catálogo, história, combo workshop, checkout
│   └── Entrega para todo Brasil
│
├── /contato (Contato)
│   └── WhatsApp, chamada de vídeo, redes sociais
│   └── Sem formulário
│
├── /blog (SEO only — fora do menu)
│   └── Artigos para Google e LLMs
│
└── /legal (Footer only)
    ├── /politica-privacidade
    └── /termos-uso
```

---

## 🎯 Ofertas Definidas

| Oferta | Descrição | Público | Alcance |
|--------|-----------|---------|---------|
| **Modelagem em Cerâmica** | Criar peças do zero com argila | Grupos 2-8 pessoas | Apenas SP |
| **Pintura em Cerâmica** | Personalizar peças já modeladas | Grupos 2-8 pessoas | Apenas SP |
| **Peças Autorais** | Arte única criada pela fundadora | Qualquer pessoa | Todo Brasil |

**Combo**: Peça autoral = cupom 20% desconto na experiência (válido 2 meses)

---

## 🚀 Funcionalidade Inovadora: Checkout Compartilhável

**Conceito**: Link de pagamento compartilhável para grupos

**Fluxo**:
1. Organizador escolhe experiência (modelagem ou pintura)
2. Seleciona número de pessoas (2-8)
3. Escolhe: "Vou pagar por todos" ou "Vamos dividir"
4. Se dividir: gera link compartilhável
5. Compartilha via WhatsApp/Instagram
6. Amigos acessam, pagam sua parte, confirmam
7. Quando completo: organiza agenda

**Benefícios**:
- Facilita divisão de custos
- Viralização orgânica (cada link = exposição da marca)
- Experiência social/interativa
- Boca a boca sem esforço

---

## 👥 Público-Alvo Definido

- **Demografia**: Mulheres, 25-35 anos, São Paulo
- **Poder aquisitivo**: Médio a alto
- **Comportamento**: 
  - Alta propensão a redes sociais (Instagram, TikTok)
  - Antenadas em trends e novas experiências
  - Consomem conteúdo em vídeos curtos, não blogs
  - Preferem WhatsApp a formulários
- **Dispositivo**: Mobile (90%+ do tráfego)
- **Entrada**: Instagram e TikTok

---

## ⚠️ Riscos e Trade-offs Identificados

### Riscos Principais

**1. SEO fraco sem blog visível**
- **Risco**: Menor visibilidade no Google
- **Mitigação**: Blog existe (apenas não no menu), páginas principais otimizadas
- **Status**: Aceito

**2. Perda de clientes que preferem experiência individual**
- **Risco**: Não atender quem quer experiência solo
- **Mitigação**: Aceito — foco em experiência compartilhada é diferencial
- **Status**: Aceito

**3. Complexidade do checkout compartilhável**
- **Risco**: Implementação técnica complexa
- **Mitigação**: MVP simples primeiro, iterar
- **Status**: A monitorar

**4. Links de grupo não completados**
- **Risco**: Grupos que não fecham, links abandonados
- **Mitigação**: Timeout para links, lembretes automáticos
- **Status**: A implementar

### Trade-offs Aceitos

**1. Estrutura ultra-simples vs Completa**
- **Escolha**: 4 páginas no menu principal
- **Trade-off**: Menos conteúdo detalhado
- **Justificativa**: Público tem atenção fragmentada, prefere simplicidade

**2. Blog escondido vs Blog visível**
- **Escolha**: Blog apenas para SEO, fora do menu
- **Trade-off**: Menos autoridade via conteúdo
- **Justificativa**: Autoridade via redes sociais e prova social

**3. Grupos obrigatórios vs Individual**
- **Escolha**: Apenas grupos de 2-8 pessoas
- **Trade-off**: Exclui clientes individuais
- **Justificativa**: Reforça proposta de valor (memória compartilhada)

**4. WhatsApp vs Formulário**
- **Escolha**: WhatsApp como canal principal
- **Trade-off**: Menos dados estruturados de leads
- **Justificativa**: Público prefere WhatsApp, menos fricção

---

## 📝 Itens a Revisar

### Antes de Implementar

1. **Precificação por pessoa**
   - Valor por pessoa para modelagem
   - Valor por pessoa para pintura
   - Desconto progressivo para grupos maiores?

2. **Checkout compartilhável**
   - Timeout para links (quanto tempo válido?)
   - Lembretes automáticos (frequência?)
   - Mínimo para confirmar (precisa de todos?)

3. **Newsletter**
   - Ferramenta de email marketing
   - Conteúdo inicial para comunidade
   - Frequência de envio

4. **Integração WhatsApp**
   - WhatsApp Business API ou link direto?
   - Mensagem inicial automática?

### Durante Implementação

1. **Teste mobile**
   - Site funciona perfeitamente no celular?
   - Touch targets adequados?

2. **Teste de fluxo compartilhável**
   - Link funciona corretamente?
   - Experiência é intuitiva?

3. **Teste de conversão**
   - Taxa de conversão por fluxo
   - Onde pessoas desistem?

---

## 📚 Lista Final de Prompts Aprovados

### UX-UI

1. **`ux-ui__jornada_usuario__v1.0.md`**
   - **Criado em**: 2025-01-26
   - **Status**: ✅ Aprovado
   - **Uso**: Mapear jornada emocional e funcional do usuário

2. **`ux-ui__funil_conversao__v1.0.md`**
   - **Criado em**: 2025-01-26
   - **Status**: ✅ Aprovado
   - **Uso**: Definir funil de conversão e CTAs

3. **`ux-ui__sitemap_mobile_first__v1.0.md`**
   - **Criado em**: 2025-01-28
   - **Status**: ✅ Aprovado
   - **Uso**: Definir arquitetura de informação mobile-first

---

## ✅ Validações Realizadas

### Auditorias

- **AUD-003**: Consistência entre R1, R2, R3 e Fase A (✅ Resolvido)
- **AUD-004**: Alinhamento com 18 decisões estratégicas (✅ Resolvido)

### Consistências Verificadas

- ✅ Proposta de valor (experiência compartilhada) alinha com grupos 2-8
- ✅ Público-alvo alinha com decisões de arquitetura (mobile-first, redes sociais)
- ✅ Ofertas (modelagem + pintura) são evoluções naturais do conceito
- ✅ Checkout compartilhável reforça proposta de valor e viralização
- ✅ Blog escondido mantém SEO sem comprometer UX

### Nota sobre Evolução

R3 contém refinamentos que superam R1 e R2 em detalhes específicos:
- R1/R2 mencionam "experiência individual" — superado por grupos 2-8 (DEC-017)
- R1/R2 mencionam "workshop" genérico — refinado para modelagem + pintura (DEC-016)
- R3 é a **fonte de verdade** para decisões de arquitetura

Isso é evolução natural em projetos iterativos, não inconsistência.

---

## 🎯 Próximos Passos

1. **Fase C — Conversão sem Atrito**
   - Lição C1: Wireframes / Layout
   - Lição C2: Copy das Páginas
   - Lição C3: CTAs e Microcopy

2. **Decisões pendentes para Fase C**:
   - Wireframes mobile-first
   - Copy emocional por página
   - Microcopy para checkout compartilhável
   - CTAs específicos por contexto

---

## 📊 Métricas da Fase R

- **Lições concluídas**: 3/3 (100%)
- **Prompts criados**: 3 (total: 6)
- **Decisões registradas**: 8 (DEC-011 a DEC-018) — total: 18
- **Auditorias realizadas**: 2 (AUD-003, AUD-004) — total: 4
- **Fluxos de conversão**: 6

---

## 🔄 Notas Finais

A Fase R estabeleceu a experiência do usuário e arquitetura do site:

**Jornada mapeada**: 6 etapas com emoções, fricções e oportunidades
**Funil definido**: TOFU → MOFU → BOFU → Pós-conversão
**Arquitetura simplificada**: 4 páginas no menu, mobile-first
**Público-alvo claro**: Mulheres 25-35, SP, redes sociais
**Ofertas refinadas**: Modelagem + Pintura + Peças
**Inovação**: Checkout compartilhável para viralização

A Fase C irá converter essa arquitetura em wireframes, copy e CTAs prontos para implementação.

---

**Última atualização**: 2025-01-28  
**Próxima revisão**: Após conclusão da Fase C
