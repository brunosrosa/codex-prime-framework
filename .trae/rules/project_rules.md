```
---
# METADADOS DO PROJETO (Para uso do Maestro.AI)
project_name: 'Codex Prime Framework'
codex_framework_version: 'self-referential' # Este projeto define o framework
tech_lead: 'Bruno S. Rosa'
status: 'ativo'
document_version: '2.0'
---
```

# Regras do Projeto: Codex Prime Framework

## 1. Diretrizes Gerais e Metodologia

- **Objetivo Principal:** Desenvolver, manter e versionar um framework de documentação e governança de primeira linha, que sirva como o **"DNA Organizacional"** e a fonte da verdade para a criação e gestão de todos os futuros projetos do ecossistema.
    
- **Metodologia:** Gestão de Ativos Estratégicos com Revisão Contínua. As mudanças são propostas via RFCs (Request for Comments) e aprovadas pelo Maestro, garantindo uma evolução controlada e bem documentada.
    
- **Repositório Principal:** github.com/brunosrosa/codex-prime-framework
    
- **Caminho da Documentação:** Este repositório **É** a própria documentação. O código-fonte _é_ o produto.
    

## 2. Stack de Tecnologia e Ferramentas ("Tech Stack da Documentação")

- **Linguagem Principal (Marcação):** Markdown (GFM - GitHub Flavored Markdown)
    
- **Linguagem de Metadados:** YAML (para o Front Matter)
    
- **Linguagem de Diagramas:** Mermaid.js
    
- **Ferramentas de Qualidade (Linting):**
    
    - `markdownlint` (Para consistência do Markdown)
        
    - `yamllint` (Para validação da sintaxe YAML)
        
    - `lychee` (Para verificação de links quebrados)
        
- **Plataforma de Deploy Alvo:** N/A (O produto é o próprio repositório Git).
    

## 3. Padrões de Conteúdo e Versionamento

- **Convenção de Nomenclatura:** Utilizar estritamente o padrão **`MAIUSCULA_COM_UNDERLINE`** para todos os arquivos e pastas de documentação, para garantir consistência e legibilidade.
    
- **Estilo de Commits:** Utilizar estritamente o padrão de **Conventional Commits** (ex: `feat:`, `fix:`, `docs:`, `refactor:`, `style:`) para manter um histórico de mudanças claro e automatizável.
    
- **Guia de Estilo de Escrita:** Aderir às melhores práticas de "Technical Writing". O conteúdo deve ser claro, conciso, inequívoco e útil.
    

## 4. Hierarquia e Delegação de Agentes

- **Agente Estratégico (Chefe de Gabinete):** `@Janus` (Responsável por debater e aprovar a evolução estratégica do Framework).
    
- **Agente Tático (Gerente de Projetos):** `@Orquestrador` (Responsável por gerenciar as tarefas de criação e refatoração dos templates).
    
- **Agentes Especialistas Principais:**
    
    - `@Arquiteto_de_Documentacao` (Especialista em criar e organizar estruturas de informação).
        
    - `@Revisor_Tecnico` (Especialista em garantir a precisão, clareza e utilidade do conteúdo dos templates).
        

## 5. Protocolo de Resolução de Conflitos

Em caso de conflito ou ambiguidade entre diferentes fontes de regras, a seguinte hierarquia de prioridade **DEVE** ser seguida:

1. **Decisão explícita e atual do Maestro:** Uma instrução direta de Bruno S. Rosa sempre tem a maior prioridade.
    
2. **`project_rules.md` (Este Documento):** As regras específicas para a governança do `Codex Prime Framework`.
    
3. **`user_rules.md`:** As regras e preferências globais do Maestro.
    
4. **`Regras_do_Jogo.md`:** A constituição geral do ecossistema.
    
5. **Padrões da Indústria para Documentação Técnica.**
    

O agente que identificar um conflito tem a responsabilidade de sinalizá-lo e solicitar orientação para garantir o alinhamento.