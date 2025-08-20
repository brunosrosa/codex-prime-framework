---
title: "Plano de Migração: Templates .codex → .codex-prime v1.0"
doc_id: "MIGRATION-PLAN-CODEX-PRIME-v1.0"
version: "1.0"
created_at: "2025-08-19 22:07:12"
timezone: "America/Sao_Paulo"
status: "Em Execução"
owner: "@ArquitetoDoCodex"
tags: [migração, templates, codex-prime, v1.0]
description: "Plano detalhado para migração de todos os templates limpos do diretório .codex para .codex-prime, estabelecendo a versão 1.0 do Motor Universal do Codex Prime Framework."
---

# Plano de Migração: Templates .codex → .codex-prime v1.0

## Resumo Executivo

**Objetivo**: Migrar todos os templates limpos e validados do diretório `.codex` para `.codex-prime`, estabelecendo a **versão 1.0 do Motor Universal** do Codex Prime Framework.

**Escopo**: 75+ arquivos de template distribuídos em 6 domínios de conhecimento.

**Status**: Em execução - Fase de mapeamento concluída.

## Inventário Completo de Templates

### 📊 Estatísticas Gerais
- **Total de Domínios**: 6 ativos (2 vazios: Pessoas, Jurídico)
- **Total de Arquivos**: ~75 templates
- **Idiomas**: pt-br (principal), en-us (parcial)
- **Status de Limpeza**: ✅ Concluída (28 arquivos processados)

### 🏢 00_Empresa_Company (10 arquivos)
**Estrutura**:
```
pt-br/
├── 00_README.md
├── 01_ESTRATEGIA_CENTRAL/ (3 arquivos)
│   ├── 01_DIRETRIZES_ESTRATEGICAS_MISSAO_VISAO_VALORES.md
│   ├── 02_MODELO_NEGOCIO_CANVAS.md
│   └── 03_PLANO_VALIDACAO_PREMISSAS_NEGOCIO.md
├── 02_ANALISE_DE_MERCADO/ (2 arquivos)
│   ├── 01_ANALISE_CONCORRENTES_MERCADO.md
│   └── 02_VANTAGENS_COMPETITIVAS_SUSTENTAVEIS.md
└── 03_EXECUCAO_E_METRICAS/ (4 arquivos)
    ├── 01_ESTRATEGIA_GO_TO_MARKET.md
    ├── 02_PITCH_DECK_TEMPLATE.md
    ├── 03_KPIS_INDICADORES_CHAVE_NEGOCIO.md
    └── 04_METRICAS_SUCESSO_BASE_MERCADO.md
```

### 📱 01_Produto_Product (16 arquivos)
**Estrutura**:
```
pt-br/
├── 00_README.md
├── 01_ESTRATEGIA_E_VISAO/ (3 arquivos + 1 YAML)
│   ├── 01_PLANO_MESTRE_PRD_CODEX_PRIME.md
│   ├── 01_PLANO_MESTRE_PRD_CODEX_PRIME.yaml
│   ├── 02_ROADMAP_ESTRATEGICO.md
│   └── 03_METRICAS_PRODUTO_ENGAJAMENTO.md
├── 02_REQUISITOS_E_HISTORIAS/ (7 arquivos + 3 YAML)
│   ├── 01_ERS_REQUISITOS_PRODUTO.md
│   ├── 02_DEFINICAO_PERSONAS.md
│   ├── 03_JORNADA_USUARIO.md
│   └── 04_HISTORIAS_USUARIO_CRITERIOS_ACEITE/
│       ├── 01_HU_AC_TEMPLATE.md + .yaml
│       ├── 02_HU_EXEMPLO_RF_ABC.md + .yaml
│       └── 03_HU_MVP_JORNADA_USUARIO.md + .yaml
└── 03_METODOLOGIAS_E_PROCESSOS/ (6 arquivos)
    ├── 01_METODOLOGIA_PRIORIZACAO.md
    ├── 02_METODOLOGIA_MVP.md
    ├── 03_PLANO_VALIDACAO_HIPOTESES.md
    ├── 04_MAPEAMENTO_DEPENDENCIAS_RF.md
    ├── 05_PRIORIZACAO_RICE_RF.md
    └── 06_GLOSSARIO_CODEX_PRIME.md
```

### 📋 02_Gestao_de_Projetos_Project_Management (28 arquivos)
**Estrutura**:
```
pt-br/
├── 01_INICIACAO_E_PLANEJAMENTO/ (4 arquivos)
├── 02_PLANOS_DE_GERENCIAMENTO/ (10 arquivos)
├── 03_FERRAMENTAS_E_MODELOS/ (13 arquivos)
│   └── KANBAN/ (7 arquivos + 1 YAML)
├── 04_REGISTROS_E_BOAS_PRATICAS/ (2 arquivos)
en-us/
└── XX_BEST_PRACTICES.md (1 arquivo)
```

### ⚙️ 03_Tecnologia_Engineering (20 arquivos)
**Estrutura**:
```
pt-br/
├── 01_ARQUITETURA_E_DESIGN/ (10 arquivos)
│   ├── 01_HLD_VISAO_GERAL_ARQUITETURA.md
│   ├── ADRs/ (vazio)
│   └── LLDs/ (9 arquivos)
├── 02_PADROES_E_BOAS_PRATICAS/ (2 arquivos)
├── 03_ESPECIFICACOES_E_CONTRATOS/ (2 arquivos)
│   └── API_Specs/ (1 MD + 1 YAML)
├── 04_DEVOPS_E_INFRAESTRUTURA/ (3 arquivos)
├── 05_QUALIDADE_E_TESTES/ (2 arquivos)
├── 06_PROCESSOS_E_FLUXOS_DE_TRABALHO/ (3 arquivos)
└── 07_ESTRATEGIA_E_GOVERNANCA/ (2 arquivos)
```

### 📢 06_Marketing_e_Vendas_Marketing_Sales (1 arquivo)
**Estrutura**:
```
└── ESTRATEGIA_GO_TO_MARKET.md
```

### 🚫 Domínios Vazios
- **04_Pessoas_People**: Diretório vazio
- **05_Juridico_Legal**: Diretório vazio

## Estratégia de Migração

### Fase 1: Preparação da Estrutura
1. **Criar diretório `.codex-prime`**
2. **Estabelecer estrutura de domínios**
3. **Configurar metadados base**

### Fase 2: Migração por Domínio
**Ordem de Prioridade**:
1. 🏢 **Empresa** (10 arquivos) - Base estratégica
2. 📱 **Produto** (16 arquivos) - Core do framework
3. 📋 **Gestão de Projetos** (28 arquivos) - Maior volume
4. ⚙️ **Tecnologia** (20 arquivos) - Complexidade técnica
5. 📢 **Marketing** (1 arquivo) - Complementar

### Fase 3: Versionamento e Validação
1. **Aplicar versão 1.0** em todos os templates
2. **Atualizar metadados YAML**
3. **Validar integridade estrutural**
4. **Gerar relatório final**

## Padrões de Versionamento

### Metadados Obrigatórios
```yaml
---
title: "[TÍTULO_DO_TEMPLATE]"
doc_id: "[ID_ÚNICO]"
version: "1.0"
migrated_at: "2025-08-19 22:07:12"
timezone: "America/Sao_Paulo"
status: "Template"
owner: "@ArquitetoDoCodex"
tags: [template, codex-prime, v1.0, [domínio]]
description: "[DESCRIÇÃO_DO_TEMPLATE]"
source_path: "[CAMINHO_ORIGINAL_NO_.CODEX]"
---
```

### Convenções de Nomenclatura
- **Manter estrutura original** dos diretórios
- **Preservar nomes de arquivo** existentes
- **Adicionar sufixo de versão** apenas nos metadados
- **Documentar origem** no campo `source_path`

## Cronograma de Execução

| Fase | Atividade | Estimativa | Status |
|------|-----------|------------|--------|
| 1 | Mapeamento completo | 1h | ✅ Concluído |
| 2 | Criação da estrutura base | 30min | 🔄 Em andamento |
| 3 | Migração Empresa (10 arquivos) | 1h | ⏳ Pendente |
| 4 | Migração Produto (16 arquivos) | 1.5h | ⏳ Pendente |
| 5 | Migração Gestão (28 arquivos) | 2h | ⏳ Pendente |
| 6 | Migração Tecnologia (20 arquivos) | 1.5h | ⏳ Pendente |
| 7 | Migração Marketing (1 arquivo) | 15min | ⏳ Pendente |
| 8 | Versionamento global | 1h | ⏳ Pendente |
| 9 | Relatório final | 30min | ⏳ Pendente |
| **Total** | **Estimativa Total** | **~8 horas** | **12% Concluído** |

## Critérios de Sucesso

### ✅ Critérios Técnicos
- [ ] Todos os 75+ arquivos migrados com sucesso
- [ ] Estrutura de diretórios preservada
- [ ] Metadados YAML padronizados
- [ ] Versão 1.0 aplicada consistentemente
- [ ] Integridade de conteúdo mantida

### ✅ Critérios de Qualidade
- [ ] Templates limpos (sem referências específicas)
- [ ] Documentação de origem rastreável
- [ ] Padrões de nomenclatura seguidos
- [ ] Timezone consistente (America/Sao_Paulo)
- [ ] Relatório de migração completo

## Próximos Passos

1. **Imediato**: Criar estrutura base do `.codex-prime`
2. **Sequencial**: Executar migração por domínio conforme prioridade
3. **Final**: Validar e documentar o Motor Universal v1.0

---

**Documento gerado em**: 2025-08-19 22:07:12 (America/Sao_Paulo)  
**Responsável**: @ArquitetoDoCodex  
**Status**: Plano aprovado - Iniciando execução