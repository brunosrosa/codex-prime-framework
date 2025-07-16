# Como Contribuir para o Codex Prime Framework

**Versão:** 1.0.0
**Status:** Ativo
**Mantenedor:** @ArquitetoDoCodex

## 1. Filosofia de Contribuição

Nossa filosofia é baseada na colaboração estreita e na manutenção de um alto padrão de qualidade. Todas as contribuições são bem-vindas, desde que sigam o processo estabelecido para garantir a consistência e a integridade do **Codex Prime Framework**.

O processo é projetado para ser simples, direto e eficaz, centrado na parceria entre o `@Maestro` (definidor da estratégia) e o `@ArquitetoDoCodex` (guardião da arquitetura).

## 2. O Fluxo de Trabalho de Contribuição (Pull Request)

Todas as mudanças no framework, desde a correção de um typo até a adição de um novo template, devem ser realizadas através de um **Pull Request (PR)**. Não são permitidos commits diretos na branch principal (`main`).

O processo é o seguinte:

1.  **Criação de uma Branch:**
    - O trabalho começa com a criação de uma nova branch a partir da `main`.
    - A branch deve seguir uma convenção de nomenclatura clara, como `feat/novo-template-xyz` ou `fix/correcao-documento-abc`.

2.  **Implementação da Mudança:**
    - Realize as alterações ou adições necessárias na sua branch.
    - Garanta que seu trabalho esteja em conformidade com a `CONSTITUICAO-PRINCIPIOS_FUNDAMENTAIS-v1.0.md` e com todos os guias de estilo relevantes.

3.  **Abertura do Pull Request:**
    - Uma vez que o trabalho esteja concluído, abra um Pull Request para a branch `main`.
    - A descrição do PR deve ser clara e concisa, explicando **o quê** foi mudado e **por quê**.

4.  **Revisão e Aprovação:**
    - O `@ArquitetoDoCodex` será automaticamente designado como revisor.
    - A revisão focará na conformidade com a arquitetura, nos padrões de qualidade e na clareza do conteúdo.
    - O `@Maestro` pode ser consultado para validação estratégica.

5.  **Merge:**
    - Após a aprovação, o `@ArquitetoDoCodex` realizará o merge do Pull Request na branch `main`.

## 3. Padrões de Commit

Para manter um histórico de commits limpo e significativo, exigimos o uso do padrão **Conventional Commits**. Isso é essencial para a rastreabilidade e para a automação futura do `CHANGELOG.md`.

- **Exemplos de mensagens de commit:**
  - `feat: Adiciona template para Relatório de Análise de Risco`
  - `fix: Corrige link quebrado no README.md`
  - `docs: Melhora a clareza da seção de governança na Constituição`
  - `refactor: Simplifica a estrutura de metadados do template de ADR`

## 4. Código de Conduta

Todas as contribuições e interações devem seguir o nosso `CODE_OF_CONDUCT.md`. Esperamos um ambiente de colaboração respeitoso e construtivo.