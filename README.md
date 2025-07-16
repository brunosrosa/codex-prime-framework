
# Codex Prime Framework: A Arquitetura para Conhecimento Vivo

**Versão:** 1.0.0
**Status:** Ativo
**Mantenedor:** @ArquitetoDoCodex

## 1. Propósito e Filosofia

O **Codex Prime Framework** é um sistema de governança e um conjunto de templates projetado para catalisar a criação, a gestão e a evolução de bases de conhecimento em um ecossistema de colaboração humano-IA. Ele não é apenas um repositório de documentos, mas uma **arquitetura para conhecimento vivo**.

Nossa filosofia se baseia em quatro pilares:

1.  **Docs-as-Code:** Tratamos a documentação com o mesmo rigor do código-fonte. Todo conhecimento é versionado, testável e parte de um fluxo de trabalho estruturado.
2.  **Fonte da Verdade Viva:** O conhecimento aqui não é estático. Ele evolui continuamente através de um processo de governança claro, garantindo que permaneça relevante e preciso.
3.  **Dualidade Humano-Máquina:** A estrutura é projetada para ser compreensível e utilizável tanto por humanos quanto por agentes de IA, permitindo uma colaboração simbiótica.
4.  **Governança Explícita:** As regras de engajamento, contribuição e evolução do conhecimento são definidas de forma clara e aplicadas de maneira consistente.

## 2. A Estrutura Dual: Motor e Instância

O framework opera com uma estrutura dual fundamental para sua escalabilidade e manutenibilidade:

### 2.1. `.codex-prime/` - O Motor do Framework

Este diretório é o coração do **Codex Prime Framework**. Ele contém os **fundamentos, templates e agentes constitucionais** que definem como o conhecimento é estruturado e governado. Pense nele como o "motor" ou o "sistema operacional" para bases de conhecimento.

- **`/foundations`**: Contém os princípios e guias universais, como o guia de estilo e nomenclatura.
- **`/templates`**: Abriga os modelos reutilizáveis para artefatos de conhecimento (ADRs, especificações, etc.).
- **`/constitutional_agents`**: Define os perfis e capacidades dos agentes de IA que governam o ecossistema.

### 2.2. `.codex/` - A Instância de Conhecimento do Projeto

Este diretório representa a **instância específica de conhecimento** para um determinado projeto. Enquanto `.codex-prime` fornece o *como*, `.codex` contém o *quê*. Ele é preenchido usando os templates e seguindo as regras definidas em `.codex-prime`.

Sua estrutura é organizada por domínios de negócio (Empresa, Produto, Tecnologia, etc.), garantindo que o conhecimento seja contextualizado e fácil de localizar.

## 3. Como Usar e Contribuir

O uso e a contribuição para o framework seguem um processo manual e deliberado nesta Fase 0, garantindo a integridade e a qualidade da base de conhecimento.

1.  **Consulta:** Para entender um tópico, navegue pela estrutura de diretórios do `.codex/`.
2.  **Criação de Novo Conhecimento:**
    - Identifique o template apropriado em `.codex-prime/templates`.
    - Copie o template para o local relevante dentro de `.codex/`.
    - Preencha o artefato seguindo as diretrizes de estilo e conteúdo.
3.  **Contribuição e Evolução:** O processo de contribuição é governado pelo arquivo `CONTRIBUTING.md` e pelo `CODE_OF_CONDUCT.md`, operando sob um fluxo de Pull Request direto entre o `@Maestro` e o `@ArquitetoDoCodex`.

## 4. Documentos de Governança

- **`CONSTITUICAO-PRINCIPIOS_FUNDAMENTAIS-v1.0.md`**: A lei máxima que rege o framework.
- **`CONTRIBUTING.md`**: Como contribuir com melhorias para o framework e para as instâncias de conhecimento.
- **`CODE_OF_CONDUCT.md`**: As regras de engajamento para todos os colaboradores.
- **`CHANGELOG.md`**: O registro de todas as mudanças significativas no framework.