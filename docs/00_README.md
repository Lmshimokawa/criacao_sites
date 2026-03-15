# Repositório: Curso Completo de Criação de Sites de Negócios — Framework ARCOS™

> **Status do Projeto**: Em desenvolvimento ativo  
> **Caso Piloto**: Verde Barro Cerâmica  
> **Versão do Framework**: 1.0.0

---

## 📋 Visão Geral

Este repositório contém:
- **Curso completo** baseado no framework ARCOS™ para criação de sites de negócios premium
- **Biblioteca de prompts reutilizáveis** versionados
- **Código-fonte** do site piloto (Verde Barro Cerâmica)
- **Documentação estratégica, técnica e operacional**

---

## 🗂️ Estrutura do Repositório

```
/
├── docs/                    # Documentação núcleo
│   ├── 00_README.md         # Este arquivo
│   ├── 01_ARCOS_Framework.md
│   ├── 02_Course_Roadmap.md
│   ├── 03_Decisions_Log.md
│   ├── 04_Audit_Log.md
│   ├── 05_State.md
│   ├── 06_Backlog.md
│   ├── 07_Definitions_Glossary.md
│   └── 08_Site_Verde_Barro_Consolidado.md  # Fonte única da verdade do site piloto
│
├── prompts/                 # Biblioteca de prompts reutilizáveis
│   ├── README.md
│   ├── strategy/
│   ├── ux-ui/
│   ├── copy/
│   ├── seo/
│   ├── analytics/
│   └── infra-deploy/
│
├── course/                  # Conteúdo do curso por fase ARCOS
│   ├── A_Arquitetura_de_Valor/
│   ├── R_Ritual_do_Usuario/
│   ├── C_Conversao_sem_Atrito/
│   ├── O_Operacao_Infra/
│   └── S_Scale_SEO_Otimizacao/
│
├── src/                     # Código-fonte do site (stack a definir)
├── verde-barro-site/        # Site piloto + central de conhecimento da marca
│   ├── assets/              # Recursos da marca Verde Barro (guia, logos, imagens)
│   │   ├── brand/
│   │   └── images/
│   └── ...
│
└── CHANGELOG.md             # Histórico de mudanças
```

---

## 🎯 Objetivos do Projeto

1. **Implementar site completo** para Verde Barro Cerâmica
2. **Documentar todo o processo** seguindo ARCOS™
3. **Criar biblioteca de prompts** reutilizáveis e versionados
4. **Refinar framework ARCOS™** para uso como template
5. **Estabelecer rotina de otimização contínua**

---

## 🚀 Como Usar Este Repositório

### Para Estudar o Curso
1. Leia `docs/01_ARCOS_Framework.md` para entender o framework
2. Siga `docs/02_Course_Roadmap.md` para ver o roteiro completo
3. Acompanhe as lições em `course/<FASE>/`

### Para Aplicar em Outro Negócio
1. Use os prompts em `prompts/` como base
2. Adapte as decisões registradas em `docs/03_Decisions_Log.md`
3. Siga a estrutura ARCOS™ documentada

### Para Desenvolver/Manter
1. Consulte **`docs/08_Site_Verde_Barro_Consolidado.md`** como fonte única da verdade do site piloto (direção, estrutura, implementações, pendências)
2. Consulte `docs/05_State.md` para estado atual do curso
3. Verifique `docs/06_Backlog.md` para pendências
4. Revise `docs/04_Audit_Log.md` para inconsistências

---

## 📊 Status Atual

**Última atualização**: Ver `docs/05_State.md`

**Fase atual**: A — Arquitetura de Valor (Lição A1 em andamento)

---

## 🔄 Ciclo de Operação

1. **Lição** → Explicação de conceitos (3 camadas)
2. **Entregáveis** → Docs, prompts, código
3. **Registro** → Decisions Log, State, Changelog
4. **Auditoria** → Verificação de consistência

---

## 📝 Convenções

- **Prompts**: `prompts/<categoria>/<categoria>__<tema>__vX.Y.md`
- **Checkpoints**: `course/<FASE>/CHECKPOINT.md`
- **Versões**: Semânticas (MAJOR.MINOR.PATCH)

---

## 🤝 Contribuindo

Este é um projeto educacional e de referência.  
Todas as decisões e mudanças devem ser documentadas nos logs apropriados.

---

**Próximo passo**: Ver `docs/02_Course_Roadmap.md` para iniciar o curso.
