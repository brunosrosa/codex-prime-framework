---
doc_id: 'CPF-DEF-002'
version: '1.0'
status: 'template'
owner: '@ArquitetoDoCodex'
tags:
  - definicao
  - componente
  - capacidade
  - funcionalidade
  - template
description: 'Define a estrutura para descrever uma Capacidade de um Agente, detalhando sua interface (schema de entrada/saída), implementação, dependências, gatilhos e governança.'
---

# Capacidade: {{capability_name}}

## 1. Definição e Propósito

-   **ID da Capacidade:** `{{doc_id}}`
-   **Nome:** `{{capability_name}}`
-   **Versão:** `{{version}}`
-   **Status:** `{{status}}`
-   **Proprietário:** `{{owner}}`

### 1.1. Descrição Funcional

> (Descreva em 1-2 parágrafos o que esta capacidade faz, qual problema ela resolve e qual o resultado esperado de sua execução. Ex: "Esta capacidade analisa um arquivo de código-fonte Python e gera um relatório de qualidade, identificando violações de estilo (PEP8), complexidade ciclomática e potenciais bugs usando as ferramentas Black e Flake8.")

## 2. Interface Executável (Schema)

(Esta seção define a "assinatura" da capacidade, como se fosse uma função em um programa. Ela deve ser consumível por um agente para entender como invocar a capacidade.)

### 2.1. Parâmetros de Entrada (Input)

```yaml
# Exemplo de schema de entrada para uma capacidade de análise de código
- name: "file_path"
  type: "string"
  description: "O caminho absoluto para o arquivo de código a ser analisado."
  required: true

- name: "fail_on_error"
  type: "boolean"
  description: "Se verdadeiro, a execução falhará se qualquer erro for encontrado."
  required: false
  default: true
```

### 2.2. Saída (Output)

```yaml
# Exemplo de schema de saída
- name: "report"
  type: "object"
  description: "Um objeto contendo o relatório da análise."
  properties:
    - name: "score"
      type: "float"
      description: "A pontuação de qualidade final de 0.0 a 10.0."
    - name: "issues"
      type: "array"
      description: "Uma lista de problemas encontrados."
      items:
        - type: "object"
          properties:
            - name: "line"
              type: "integer"
            - name: "code"
              type: "string"
            - name: "message"
              type: "string"
- name: "status"
  type: "string"
  description: "O status final da execução (Success, Failure)."
```

## 3. Implementação e Lógica

### 3.1. Script ou Comando

(Referencie o script, comando ou endpoint de API que implementa a lógica desta capacidade. Esta é a parte "executável" do conhecimento.)

-   **Tipo:** `script` # Pode ser: script, command, api_endpoint
-   **Referência:** `scripts/run_code_analysis.py`

### 3.2. Dependências

(Liste quaisquer outras capacidades, ferramentas ou pacotes de software necessários para que esta capacidade funcione.)

-   **Capacidades:** N/A
-   **Ferramentas:** `run_command`
-   **Pacotes:** `flake8`, `radon`

## 4. Gatilhos e Eventos (Triggers)

(Descreva os eventos que podem invocar esta capacidade automaticamente.)

-   **Gatilho Principal:** Em um Pull Request, para cada arquivo `.py` modificado.
-   **Gatilho Secundário:** Invocação manual por um agente com a permissão necessária.

## 5. Governança e Testes

### 5.1. Testes de Validação

(Referencie os casos de teste que validam o funcionamento desta capacidade.)

-   **Referência:** `tests/test_code_analysis.py`

### 5.2. Guardrails de Execução

(Defina quaisquer limites ou restrições para a execução desta capacidade para garantir a segurança e a estabilidade do sistema.)

-   **Timeout:** 120 segundos.
-   **Restrição de Alvo:** Só pode ser executada em arquivos dentro do diretório `/src`.

---
**Histórico de Versões:**
-   **v1.0 (DD/MM/AAAA):** Criação inicial do template.