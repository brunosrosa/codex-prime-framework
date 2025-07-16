---
# Metadados Core (Obrigatórios)
document_type: "governance"
document_id: "CODEX-PRIME-STYLE-001"
title: "Guia de Estilo para Metadados e Nomenclatura"
version: "1.0.0"
status: "approved"
created_date: "2025-01-03"
last_updated: "2025-01-03"
author: "@ArquitetoDoCodex"
project: "Codex Prime Framework"

# Metadados para GraphRAG
tags: ["style-guide", "metadata", "nomenclature", "standards", "synapse-engine"]
category: "governance"
complexity: "medium"
stakeholders: ["@ArquitetoDoCodex", "@Maestro", "Synapse Engine"]
dependencies: ["CONSTITUICAO-PRINCIPIOS_FUNDAMENTAIS-v1.0"]
related_documents: ["TEMPLATE_ADR", "TEMPLATE_ERS", "TEMPLATE_GOVERNANCA_IA"]

# Metadados Específicos
template_usage: "frequent"
target_audience: ["developers", "agents", "stakeholders"]
---

# 📋 Guia de Estilo para Metadados e Nomenclatura

> **Padrão oficial para metadados YAML frontmatter e convenções de nomenclatura no Codex Prime Framework, otimizado para o Synapse Engine GraphRAG.**

## 🎯 Objetivo

Este documento estabelece os padrões obrigatórios para:
- **Metadados YAML frontmatter** em todos os documentos
- **Convenções de nomenclatura** para arquivos e diretórios
- **Otimização para GraphRAG** do Synapse Engine
- **Consistência** em todo o ecossistema da Arandu PoC

## 📊 Estrutura de Metadados YAML

### Metadados Core (Obrigatórios)

```yaml
---
# === METADADOS CORE (OBRIGATÓRIOS) ===
document_type: "[adr|ers|template|governance|user_story|tap|hld|lld]"
document_id: "[PROJETO]-[TIPO]-[NUMERO]"
title: "[TITULO_DOCUMENTO]"
version: "[MAJOR.MINOR.PATCH]"
status: "[draft|review|approved|deprecated|superseded]"
created_date: "YYYY-MM-DD"
last_updated: "YYYY-MM-DD"
author: "[NOME_AUTOR_OU_AGENTE]"
project: "[NOME_PROJETO]"
---
```

### Metadados para GraphRAG (Recomendados)

```yaml
# === METADADOS PARA GRAPHRAG (RECOMENDADOS) ===
tags: ["tag1", "tag2", "tag3"]  # Máximo 5 tags
category: "[empresa|produto|tecnologia|marketing|dados|agentes|governance]"
complexity: "[low|medium|high]"
stakeholders: ["stakeholder1", "stakeholder2"]
dependencies: ["doc_id_1", "doc_id_2"]
related_documents: ["doc_id_3", "doc_id_4"]
```

### Metadados Específicos por Tipo

#### Para ADRs (Architecture Decision Records)
```yaml
# === METADADOS ESPECÍFICOS PARA ADR ===
decision_status: "[proposed|accepted|superseded]"
decision_date: "YYYY-MM-DD"
impact_level: "[low|medium|high]"
decision_makers: ["pessoa1", "pessoa2"]
technical_consultant: "[NOME_CONSULTOR]"
```

#### Para Templates
```yaml
# === METADADOS ESPECÍFICOS PARA TEMPLATES ===
template_usage: "[frequent|occasional|specialized]"
target_audience: ["developers", "managers", "stakeholders", "agents"]
template_category: "[core|specialized|experimental]"
```

#### Para ERS (Especificação de Requisitos)
```yaml
# === METADADOS ESPECÍFICOS PARA ERS ===
requirements_type: "[functional|non_functional|business]"
module: "[NOME_MODULO]"
priority: "[critical|high|medium|low]"
```

## 📁 Convenções de Nomenclatura

### Estrutura Geral
```
[PREFIXO]_[TIPO]_[NOME]_[ESPECIALIZAÇÃO]-v[VERSAO].md
```

### Prefixos por Categoria

| Prefixo | Uso | Exemplo |
|---------|-----|----------|
| `TEMPLATE_` | Modelos reutilizáveis | `TEMPLATE_ADR_ARQUITETURA.md` |
| `DOC_` | Documentação específica | `DOC_SETUP_AMBIENTE.md` |
| `GUIDE_` | Guias e manuais | `GUIDE_CONTRIBUICAO.md` |
| `SPEC_` | Especificações técnicas | `SPEC_API_BACKEND.md` |
| `PROC_` | Procedimentos e processos | `PROC_DEPLOY_PRODUCAO.md` |
| `RFC_` | Request for Comments | `RFC_NOVA_ARQUITETURA.md` |

### Numeração para Documentos de Projeto
```
[NUMERO]_[TIPO]_[NOME].md
```

**Exemplos:**
- `01_ADR_Escolha_Stack_Tecnologica.md`
- `02_ERS_Modulo_Autenticacao.md`
- `03_HLD_Arquitetura_Geral.md`

### Documentos de Governança
```
[TIPO]-[NOME]-v[VERSAO].md
```

**Exemplos:**
- `CONSTITUICAO-PRINCIPIOS_FUNDAMENTAIS-v1.0.md`
- `GUIA_ESTILO_METADADOS_NOMENCLATURA-v1.0.md`

### Documentos Especiais
```
[NOME_ESPECIAL].md
```

**Exemplos:**
- `README.md`
- `CHANGELOG.md`
- `CONTRIBUTING.md`
- `LICENSE.md`

## 🏷️ Sistema de Tags

### Tags Core (Sempre usar quando aplicável)
- `core` - Funcionalidades essenciais
- `template` - Templates reutilizáveis
- `governance` - Documentos de governança
- `architecture` - Decisões arquiteturais
- `security` - Aspectos de segurança
- `performance` - Otimizações de performance
- `ai-agents` - Relacionado a agentes de IA
- `synapse-engine` - Integração com Synapse Engine

### Tags por Domínio
- **Empresa:** `mission`, `vision`, `values`, `culture`
- **Produto:** `features`, `requirements`, `roadmap`, `mvp`
- **Tecnologia:** `backend`, `frontend`, `database`, `api`, `infrastructure`
- **Marketing:** `go-to-market`, `pricing`, `positioning`
- **Dados:** `analytics`, `metrics`, `data-model`
- **Agentes:** `agent-profile`, `prompts`, `orchestration`

## 🔗 Referências entre Documentos

### Campo `dependencies`
Use para documentos que são pré-requisitos:
```yaml
dependencies: ["CODEX-PRIME-CONST-001", "RECOLOCA-ADR-001"]
```

### Campo `related_documents`
Use para documentos relacionados mas não dependentes:
```yaml
related_documents: ["TEMPLATE_ERS", "GUIDE_CONTRIBUICAO"]
```

## 📈 Status de Documentos

| Status | Descrição | Quando Usar |
|--------|-----------|-------------|
| `draft` | Rascunho inicial | Documento em criação |
| `review` | Em revisão | Aguardando feedback |
| `approved` | Aprovado | Documento oficial |
| `deprecated` | Descontinuado | Não usar mais |
| `superseded` | Substituído | Substituído por versão mais nova |

## 🎯 Otimizações para Synapse Engine

### Campos Críticos para GraphRAG
1. **`document_id`** - Identificador único para referências
2. **`tags`** - Facilita busca semântica
3. **`category`** - Organização hierárquica
4. **`dependencies`** - Mapeamento de relações
5. **`stakeholders`** - Contexto de responsabilidade

### Boas Práticas
- **Máximo 5 tags** por documento
- **IDs únicos** seguindo padrão `[PROJETO]-[TIPO]-[NUMERO]`
- **Datas no formato ISO** (YYYY-MM-DD)
- **Versionamento semântico** (MAJOR.MINOR.PATCH)
- **Stakeholders específicos** (evitar genéricos como "equipe")

## ✅ Checklist de Validação

### Metadados Obrigatórios
- [ ] `document_type` definido
- [ ] `document_id` único e seguindo padrão
- [ ] `title` descritivo
- [ ] `version` em formato semântico
- [ ] `status` apropriado
- [ ] `created_date` e `last_updated` em formato ISO
- [ ] `author` identificado
- [ ] `project` especificado

### Nomenclatura
- [ ] Nome do arquivo segue convenção
- [ ] Prefixo apropriado usado
- [ ] Sem espaços ou caracteres especiais
- [ ] Versão incluída quando necessário

### GraphRAG
- [ ] Tags relevantes (máximo 5)
- [ ] Categoria apropriada
- [ ] Dependências mapeadas
- [ ] Stakeholders específicos

## 🔄 Processo de Atualização

1. **Mudança de Metadados:** Atualizar `last_updated` e incrementar `version`
2. **Mudança de Status:** Documentar no `CHANGELOG.md`
3. **Novos Templates:** Seguir processo RFC
4. **Validação:** Usar checklist antes de commit

---

## 📚 Referências

- [Constituição da Arandu PoC](../../CONSTITUICAO-PRINCIPIOS_FUNDAMENTAIS-v1.0.md)
- [Synapse Engine Documentation](../../../Synapse%20Engine/README.md)
- [Conventional Commits](https://www.conventionalcommits.org/)
- [Semantic Versioning](https://semver.org/)

---

**Última Atualização:** 2025-01-03  
**Próxima Revisão:** 2025-04-03  
**Responsável:** @ArquitetoDoCodex