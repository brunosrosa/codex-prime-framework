---
title: "Plano Detalhado: Criação de Templates em Inglês (en-us)"
doc_id: "CODEX-PRIME-PLANO-TEMPLATES-EN-US-V1.0"
version: "1.0"
created_at: "2025-08-20 18:49:09"
timezone: "America/Sao_Paulo"
status: "Plano"
owner: "@ArquitetoDoCodex"
tags: [plano, templates, en-us, internacionalização, codex-prime]
description: "Plano detalhado para criação de todos os templates em inglês espelhando a estrutura pt-br"
---

# Plano Detalhado: Criação de Templates em Inglês (en-us)

## Análise da Estrutura Atual

### Templates Identificados em pt-br

**Total de arquivos a serem criados: 81 templates**

#### 1. 00_Empresa_Company (10 arquivos)
- 00_README.md
- 01_ESTRATEGIA_CENTRAL/ (3 arquivos)
  - 01_DIRETRIZES_ESTRATEGICAS_MISSAO_VISAO_VALORES.md
  - 02_MODELO_NEGOCIO_CANVAS.md
  - 03_PLANO_VALIDACAO_PREMISSAS_NEGOCIO.md
- 02_ANALISE_DE_MERCADO/ (2 arquivos)
  - 01_ANALISE_CONCORRENTES_MERCADO.md
  - 02_VANTAGENS_COMPETITIVAS_SUSTENTAVEIS.md
- 03_EXECUCAO_E_METRICAS/ (4 arquivos)
  - 01_ESTRATEGIA_GO_TO_MARKET.md
  - 02_PITCH_DECK_TEMPLATE.md
  - 03_KPIS_INDICADORES_CHAVE_NEGOCIO.md
  - 04_METRICAS_SUCESSO_BASE_MERCADO.md

#### 2. 01_Produto_Product (16 arquivos)
- 00_README.md
- 01_ESTRATEGIA_E_VISAO/ (3 arquivos)
  - 01_PLANO_MESTRE_PRD_CODEX_PRIME.md + .yaml
  - 02_ROADMAP_ESTRATEGICO.md
  - 03_METRICAS_PRODUTO_ENGAJAMENTO.md
- 02_REQUISITOS_E_HISTORIAS/ (9 arquivos)
  - 01_ERS_REQUISITOS_PRODUTO.md
  - 02_DEFINICAO_PERSONAS.md
  - 03_JORNADA_USUARIO.md
  - 04_HISTORIAS_USUARIO_CRITERIOS_ACEITE/ (6 arquivos)
- 03_METODOLOGIAS_E_PROCESSOS/ (6 arquivos)

#### 3. 02_Gestao_de_Projetos_Project_Management (30 arquivos)
- 01_INICIACAO_E_PLANEJAMENTO/ (4 arquivos)
- 02_PLANOS_DE_GERENCIAMENTO/ (10 arquivos)
- 03_FERRAMENTAS_E_MODELOS/ (14 arquivos incluindo KANBAN/)
- 04_REGISTROS_E_BOAS_PRATICAS/ (2 arquivos)

#### 4. 03_Tecnologia_Engineering (24 arquivos)
- 01_ARQUITETURA_E_DESIGN/ (11 arquivos incluindo ADRs/ e LLDs/)
- 02_PADROES_E_BOAS_PRATICAS/ (2 arquivos)
- 03_ESPECIFICACOES_E_CONTRATOS/ (2 arquivos)
- 04_DEVOPS_E_INFRAESTRUTURA/ (3 arquivos)
- 05_QUALIDADE_E_TESTES/ (2 arquivos)
- 06_PROCESSOS_E_FLUXOS_DE_TRABALHO/ (3 arquivos)
- 07_ESTRATEGIA_E_GOVERNANCA/ (2 arquivos)

#### 5. 06_Marketing_e_Vendas_Marketing_Sales (1 arquivo)
- ESTRATEGIA_GO_TO_MARKET.md

## Padrões de Tradução e Nomenclatura

### Convenções de Nomenclatura em Inglês

#### Diretórios Principais
- `00_Empresa_Company` → Manter (já bilíngue)
- `01_Produto_Product` → Manter (já bilíngue)
- `02_Gestao_de_Projetos_Project_Management` → Manter (já bilíngue)
- `03_Tecnologia_Engineering` → Manter (já bilíngue)
- `06_Marketing_e_Vendas_Marketing_Sales` → Manter (já bilíngue)

#### Subdiretórios (Tradução para Inglês)
- `ESTRATEGIA_CENTRAL` → `CORE_STRATEGY`
- `ANALISE_DE_MERCADO` → `MARKET_ANALYSIS`
- `EXECUCAO_E_METRICAS` → `EXECUTION_AND_METRICS`
- `ESTRATEGIA_E_VISAO` → `STRATEGY_AND_VISION`
- `REQUISITOS_E_HISTORIAS` → `REQUIREMENTS_AND_STORIES`
- `METODOLOGIAS_E_PROCESSOS` → `METHODOLOGIES_AND_PROCESSES`
- `INICIACAO_E_PLANEJAMENTO` → `INITIATION_AND_PLANNING`
- `PLANOS_DE_GERENCIAMENTO` → `MANAGEMENT_PLANS`
- `FERRAMENTAS_E_MODELOS` → `TOOLS_AND_MODELS`
- `REGISTROS_E_BOAS_PRATICAS` → `RECORDS_AND_BEST_PRACTICES`
- `ARQUITETURA_E_DESIGN` → `ARCHITECTURE_AND_DESIGN`
- `PADROES_E_BOAS_PRATICAS` → `STANDARDS_AND_BEST_PRACTICES`
- `ESPECIFICACOES_E_CONTRATOS` → `SPECIFICATIONS_AND_CONTRACTS`
- `DEVOPS_E_INFRAESTRUTURA` → `DEVOPS_AND_INFRASTRUCTURE`
- `QUALIDADE_E_TESTES` → `QUALITY_AND_TESTING`
- `PROCESSOS_E_FLUXOS_DE_TRABALHO` → `PROCESSES_AND_WORKFLOWS`
- `ESTRATEGIA_E_GOVERNANCA` → `STRATEGY_AND_GOVERNANCE`

### Padrões de Metadados

#### Estrutura de Metadados para Templates em Inglês
```yaml
---
title: "Template: [NOME_TEMPLATE_EN]"
doc_id: "CODEX-PRIME-[DOMINIO]-[NUMERO]-[NOME]-EN-V1.0"
version: "1.0"
created_at: "2025-08-20 18:49:09"
timezone: "America/Sao_Paulo"
status: "Template"
owner: "@ArquitetoDoCodex"
tags: [template, codex-prime, v1.0, en-us, [dominio]]
description: "English version of [TEMPLATE_NAME] template for Codex Prime Framework"
source_template: "[CAMINHO_TEMPLATE_PT_BR]"
language: "en-us"
---
```

## Estratégia de Implementação

### Fase 1: Criação da Estrutura de Diretórios
1. Criar todos os subdiretórios necessários em cada pasta `en-us`
2. Manter a mesma hierarquia da versão `pt-br`

### Fase 2: Tradução dos Templates por Domínio
1. **Prioridade Alta**: 00_Empresa_Company (base estratégica)
2. **Prioridade Alta**: 01_Produto_Product (core do framework)
3. **Prioridade Média**: 02_Gestao_de_Projetos_Project_Management
4. **Prioridade Média**: 03_Tecnologia_Engineering
5. **Prioridade Baixa**: 06_Marketing_e_Vendas_Marketing_Sales

### Fase 3: Validação e Qualidade
1. Verificar consistência de metadados
2. Validar estrutura de diretórios
3. Revisar qualidade das traduções
4. Testar integridade dos links internos

## Princípios de Tradução

### Conteúdo
1. **Manter Estrutura**: Preservar exatamente a mesma estrutura de seções e campos
2. **Traduzir Contexto**: Adaptar exemplos e contextos para audiência internacional
3. **Preservar Placeholders**: Manter placeholders em formato `[CAMPO_EM_INGLES]`
4. **Consistência Terminológica**: Usar glossário consistente de termos técnicos

### Metadados
1. **doc_id**: Adicionar sufixo `-EN` antes da versão
2. **tags**: Incluir `en-us` e manter tags originais traduzidas
3. **description**: Traduzir para inglês
4. **source_template**: Referenciar template original em pt-br
5. **language**: Definir como `en-us`

## Cronograma de Execução

### Semana 1: Estrutura e Empresa
- [ ] Criar estrutura completa de diretórios en-us
- [ ] Traduzir todos os templates de 00_Empresa_Company

### Semana 2: Produto
- [ ] Traduzir todos os templates de 01_Produto_Product
- [ ] Validar consistência com templates de Empresa

### Semana 3: Gestão de Projetos
- [ ] Traduzir templates de 02_Gestao_de_Projetos_Project_Management
- [ ] Foco especial nos templates KANBAN

### Semana 4: Tecnologia e Finalização
- [ ] Traduzir templates de 03_Tecnologia_Engineering
- [ ] Traduzir template de 06_Marketing_e_Vendas_Marketing_Sales
- [ ] Validação final e testes de qualidade

## Critérios de Qualidade

### Checklist por Template
- [ ] Metadados completos e corretos
- [ ] Estrutura idêntica ao template pt-br
- [ ] Tradução precisa e contextualizada
- [ ] Placeholders em inglês
- [ ] Links internos funcionais
- [ ] Formatação Markdown correta

### Validação Final
- [ ] Todos os 81 templates criados
- [ ] Estrutura de diretórios espelhada
- [ ] Metadados consistentes
- [ ] Qualidade de tradução validada
- [ ] Documentação de processo atualizada

## Próximos Passos

1. **Aprovação do Plano**: Validar estratégia com Maestro
2. **Início da Implementação**: Começar pela criação da estrutura
3. **Execução Faseada**: Seguir cronograma por domínio
4. **Validação Contínua**: Revisar qualidade a cada fase
5. **Documentação**: Atualizar status e progresso

---

**Status**: Plano aprovado e pronto para execução
**Próxima Ação**: Aguardar validação do Maestro para iniciar implementação
**Estimativa Total**: 4 semanas de trabalho focado
**Impacto**: Internacionalização completa do Codex Prime Framework