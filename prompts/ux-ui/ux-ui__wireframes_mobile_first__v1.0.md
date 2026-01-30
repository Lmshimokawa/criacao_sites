# UX-UI — Wireframes Mobile-First (v1.0)

## Objetivo

Criar wireframes mobile-first para sites de serviços/experiências premium, definindo estrutura, hierarquia visual e fluxos de conversão antes do design final.

## Quando Usar

- Após definir arquitetura de informação (sitemap)
- Antes de iniciar design visual
- Quando público-alvo é majoritariamente mobile
- Para validar estrutura antes de investir em visual

## Inputs Necessários

- **Sitemap completo** (páginas e hierarquia)
- **Público-alvo** (perfil comportamental)
- **Ofertas** (produtos/serviços com preços se disponíveis)
- **CTAs principais** (por página)
- **Canais de conversão** (WhatsApp, checkout, etc.)
- **Conteúdo mínimo** (o que cada página deve ter)

## Prompt

```
Você é um especialista em UX/UI para sites mobile-first, focado em conversão e experiência fluida.

CONTEXTO:
- Nome do negócio: [NOME]
- Público-alvo: [PERFIL - idade, comportamento, dispositivo]
- Sitemap: [LISTA DE PÁGINAS]
- Ofertas: [PRODUTOS/SERVIÇOS]
- CTAs principais: [LISTA]
- Canal de conversão principal: [WHATSAPP/CHECKOUT/ETC]

TAREFA:
Crie wireframes mobile-first para cada página seguindo estes princípios:

1. ESTRUTURA MOBILE-FIRST
   - Largura: 375px (referência iPhone)
   - Touch targets: mínimo 44x44px
   - CTAs na parte inferior (alcançável com polegar)
   - Scroll vertical apenas
   - Conteúdo essencial above the fold

2. HIERARQUIA VISUAL
   - Hero section impactante
   - Informação mais importante primeiro
   - Seções bem delimitadas
   - Espaçamento generoso entre elementos
   - Progressão lógica (narrativa → detalhes → CTA)

3. ELEMENTOS POR PÁGINA
   Para cada página, defina:
   - Header (fixo ou não)
   - Seções em ordem de prioridade
   - CTAs e posicionamento
   - Elementos interativos (carrosséis, accordions)
   - Footer

4. FLUXOS DE CONVERSÃO
   - Mapeie cada passo do checkout/agendamento
   - Minimize campos e cliques
   - Feedback visual claro
   - Estados de sucesso/erro

5. PADRÕES MOBILE
   - Menu hambúrguer para navegação
   - Botão flutuante (WhatsApp ou CTA principal)
   - Carrosséis para múltiplos itens
   - Accordions para FAQ
   - Indicadores de progresso para fluxos

6. FORMATO DE SAÍDA
   Use ASCII art para representar wireframes:
   
   ```
   ┌─────────────────────────────────────┐
   │           SEÇÃO                     │
   │                                     │
   │    [Elemento]                       │
   │    Texto descritivo                 │
   │                                     │
   │    [ Botão CTA ]                    │
   │                                     │
   └─────────────────────────────────────┘
   ```

RESTRIÇÕES:
- Mobile-first obrigatório
- Máximo 5-7 seções por página
- CTAs repetidos ao longo da página (não apenas no fim)
- Sem scroll horizontal
- Carregamento rápido (indicar imagens otimizadas)

OUTPUT ESPERADO:
- Wireframe ASCII para cada página
- Descrição de cada seção
- Fluxos de checkout/conversão detalhados
- Notas sobre interações e estados
```

## Output Esperado

### Critérios de Sucesso

1. **Estrutura clara**
   - Cada página com seções bem definidas
   - Hierarquia visual evidente
   - Progressão lógica

2. **Mobile-first**
   - Otimizado para toque
   - CTAs acessíveis
   - Scroll fluido

3. **Conversão facilitada**
   - CTAs visíveis e repetidos
   - Fluxos curtos
   - Feedback claro

4. **Documentação completa**
   - Wireframes para todas as páginas
   - Fluxos de conversão mapeados
   - Interações descritas

### Formato de Saída

```markdown
# Wireframes — [NOME DO NEGÓCIO]

## Página: [NOME]

### Estrutura
[Wireframe ASCII]

### Seções
1. [Seção 1]: [Descrição]
2. [Seção 2]: [Descrição]
...

### CTAs
- Principal: [CTA]
- Secundários: [Lista]

### Interações
- [Elemento]: [Comportamento]
...

---

## Fluxo: [NOME DO FLUXO]
[Wireframes do fluxo passo a passo]
```

## Versões

- **v1.0** (2025-01-28): Versão inicial criada durante Lição C1 do curso ARCOS™
  - Baseado em caso piloto: Verde Barro Cerâmica
  - Inclui wireframes para páginas e fluxos de checkout
  - Formato ASCII art para representação

---

## Notas de Uso

- Wireframes são para validação de estrutura, não design final
- Testar com usuários antes de avançar para design
- Iterar conforme feedback
- Considerar estados de loading, erro e sucesso

---

**Criado em**: 2025-01-28  
**Última atualização**: 2025-01-28  
**Próxima revisão**: Após uso em 3+ projetos
