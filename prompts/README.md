# Biblioteca de Prompts Reutilizáveis

> **Objetivo**: Centralizar prompts versionados e reutilizáveis para criação de sites de negócios premium.

---

## 📁 Estrutura

```
prompts/
├── README.md (este arquivo)
├── strategy/        # Prompts de estratégia (ARCOS Fase A)
├── ux-ui/          # Prompts de UX/UI (ARCOS Fases R e C)
├── copy/           # Prompts de copywriting (ARCOS Fase C)
├── seo/            # Prompts de SEO (ARCOS Fase S)
├── analytics/       # Prompts de métricas e otimização (ARCOS Fase S)
└── infra-deploy/   # Prompts de infraestrutura e deploy (ARCOS Fase O)
```

---

## 📋 Formato Padrão

Cada prompt deve seguir este formato:

```markdown
# <Categoria> — <Tema> (vX.Y)

## Objetivo
[O que este prompt faz]

## Quando Usar
[Em que contexto aplicar este prompt]

## Inputs Necessários
- [Input 1]
- [Input 2]

## Prompt
[Texto completo do prompt]

## Output Esperado
[Criterios de sucesso]

## Versões
- vX.Y (data): [Descrição da mudança]
```

---

## 🔢 Convenção de Nomenclatura

**Formato**: `<categoria>__<tema>__vX.Y.md`

**Exemplos**:
- `strategy__proposta_valor__v1.0.md`
- `ux-ui__jornada_usuario__v1.0.md`
- `copy__conversao_premium__v1.0.md`

---

## 📊 Status da Biblioteca

- **Total de prompts**: 11
- **Por categoria**:
  - strategy: 3 (`strategy__proposta_valor__v1.0.md`, `strategy__posicionamento__v1.0.md`, `strategy__definicao_oferta__v1.0.md`)
  - ux-ui: 5 (`ux-ui__jornada_usuario__v1.0.md`, `ux-ui__funil_conversao__v1.0.md`, `ux-ui__sitemap_mobile_first__v1.0.md`, `ux-ui__wireframes_mobile_first__v1.0.md`, `ux-ui__canais_conversao__v1.0.md`)
  - copy: 2 (`copy__paginas_experiencias__v1.0.md`, `copy__conteudo_autoridade__v1.0.md`)
  - seo: 1 (`seo__estrategia__v1.0.md`)
  - analytics: 1 (`analytics__setup__v1.0.md`)
  - infra-deploy: 0

---

## 🔄 Versionamento

- **vX.0**: Versão inicial ou mudança major
- **vX.Y**: Versão minor (melhorias, ajustes)
- Changelog dentro de cada arquivo

---

## ✅ Checklist para Criar um Prompt

- [ ] Nome segue convenção `<categoria>__<tema>__vX.Y.md`
- [ ] Contém todos os campos obrigatórios
- [ ] Prompt testado e validado
- [ ] Output esperado claro e mensurável
- [ ] Versão inicial registrada

---

**Última atualização**: 2026-02-01
