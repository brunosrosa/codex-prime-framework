---
doc_id: "KNOWLEDGE-ARTIFACT-SPEC-v1.0"
spec_name: "Especificação de Artefato de Conhecimento v1.0"
version: "1.0"
status: "Active"
owner: "@ArquitetoDoCodex"
tags: [especificação, governança, metadados, template]
description: "Define o schema mandatório para o frontmatter YAML de todos os artefatos de conhecimento no Codex Prime, garantindo consistência, capacidade de descoberta e governança automatizada."
---

# Especificação do Artefato de Conhecimento

## 1. Propósito e Escopo

Esta especificação estabelece a estrutura **obrigatória** para o bloco de metadados (frontmatter YAML) de todos os documentos de conhecimento (`.md`) dentro do ecossistema governado pelo Codex Prime. A adesão a este schema é fundamental para:

-   **Descoberta e Indexação:** Permitir que o `Synapse Engine` (baseado em GraphRAG) construa um grafo de conhecimento preciso e navegável.
-   **Governança Automatizada:** Habilitar o `Agente Guardião` a validar a conformidade de novos artefatos de conhecimento durante os Pull Requests.
-   **Interoperabilidade:** Garantir que todos os agentes tenham uma compreensão consistente da natureza e do propósito de cada artefato.

## 2. Schema do Frontmatter (YAML)

Todo artefato de conhecimento DEVE começar com um bloco YAML (`---...---`) contendo os seguintes campos:

```yaml
# --- METADADOS OBRIGATÓRIOS ---

# (String) O identificador único e imutável do documento. 
# Padrão: [TIPO]-[ASSUNTO]-[VERSÃO_SEMÂNTICA]
# Ex: "ADR-AUTENTICACAO_OAUTH2-v1.0"
doc_id: "string"

# (String) A versão semântica do artefato (Major.Minor.Patch).
# Ex: "1.0.0", "2.1.3"
version: "string"

# (String) O status atual do ciclo de vida do artefato.
# Valores permitidos: "Draft", "InReview", "Active", "Deprecated", "Archived"
status: "string"

# (String) O agente ou time responsável pela manutenção e veracidade deste artefato.
# Deve ser um ID de agente ou time válido. Ex: "@ArquitetoDoCodex", "@TimeDeSeguranca"
owner: "string"

# (Array de Strings) Uma lista de tags para facilitar a busca e a categorização.
# Deve incluir o tipo do artefato (adr, how-to, tutorial, etc.) e o domínio principal.
# Ex: [adr, segurança, autenticação, oauth2]
tags: ["string"]

# (String) Uma descrição concisa (1-2 frases) do propósito e conteúdo do artefato.
# Otimizada para ser exibida em resultados de busca.
description: "string"

# --- METADADOS OPCIONAIS (RECOMENDADOS) ---

# (String) A data em que o artefato foi criado.
# Formato: YYYY-MM-DD
created_at: "string"

# (String) A data da última modificação significativa.
# Formato: YYYY-MM-DD
updated_at: "string"

# (Array de Strings) Lista de IDs de documentos que este artefato substitui ou torna obsoletos.
# Ex: ["ADR-AUTENTICACAO_JWT-v1.2"]
supersedes: ["string"]

# (Array de Strings) Lista de IDs de documentos que estão relacionados a este.
# Ajuda a construir as arestas do grafo de conhecimento.
# Ex: ["TUTORIAL-CONFIGURAR_OAUTH2_CLIENT-v1.0"]
related_to: ["string"]

# (String) O quadrante do Framework Diátaxis ao qual este artefato pertence.
# Valores permitidos: "Tutorial", "HowToGuide", "Reference", "Explanation"
diataxis_quadrant: "string"
```

## 3. Validação e Aplicação (Enforcement)

-   **CI/CD Pipeline:** Um passo no pipeline de integração contínua (ex: GitHub Actions) será responsável por validar o frontmatter de todos os arquivos `.md` modificados em um Pull Request contra este schema.
-   **Agente Guardião:** O `@GuardiãoDoCodex` (Agente Constitucionalista) usará esta especificação como uma de suas regras primárias para aprovar ou rejeitar contribuições.
-   **Falha na Validação:** Pull Requests que contenham artefatos não conformes serão bloqueados até que os metadados sejam corrigidos.

## 4. Exemplo Completo

```markdown
---
doc_id: "HOW-TO-CONFIGURAR_VARIAVEIS_AMBIENTE-v1.1"
version: "1.1.0"
status: "Active"
owner: "@EngenheiroDePlataforma"
tags: [how-to, devops, configuração, segurança]
description: "Um guia passo a passo para configurar variáveis de ambiente de forma segura em ambientes de desenvolvimento, teste e produção."
created_at: "2023-10-26"
updated_at: "2024-01-15"
supersedes: ["HOW-TO-CONFIGURAR_VARIAVEIS_AMBIENTE-v1.0"]
related_to: ["EXPLANATION-PADRAO_12_FACTOR_APP-v1.0"]
diataxis_quadrant: "HowToGuide"
---

# Guia: Como Configurar Variáveis de Ambiente

Este guia fornece instruções detalhadas para...

(Resto do conteúdo do documento)
```

---
**Histórico de Versões:**
-   **v1.0 (DD/MM/AAAA):** Criação inicial da especificação.