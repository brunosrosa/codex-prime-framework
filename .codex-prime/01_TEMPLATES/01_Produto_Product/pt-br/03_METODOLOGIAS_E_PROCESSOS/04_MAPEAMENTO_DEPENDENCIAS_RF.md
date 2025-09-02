---
tags:
  - requisitos
  - dependencias
  - priorizacao
  - mvp
sticker: lucide//git-branch
---
# Mapeamento de Dependências dos Requisitos Funcionais - [NOME_DO_PROJETO]

**Versão**: [VERSAO_DOCUMENTO]
**Data de Criação**: [DATA_CRIACAO]
**Data de Última Atualização**: [DATA_ULTIMA_ATUALIZACAO]
**Baseado em**: [DOCUMENTOS_BASE]
**Criado por**: [AUTOR_DOCUMENTO]

## 1. Objetivo e Metodologia

### 1.1. Objetivo
Este documento mapeia as **dependências técnicas e de negócio** entre os requisitos funcionais do [DOCUMENTO_ERS] para:
- [OBJETIVO_1]
- [OBJETIVO_2]
- [OBJETIVO_3]
- [OBJETIVO_4]

### 1.2. Critérios Aplicados para Identificação de Dependências

**Critérios Explícitos Utilizados:**

1. **[CRITERIO_1] (Peso: [PESO_1])**
   - [DESCRICAO_CRITERIO_1]
   - Exemplo: [EXEMPLO_CRITERIO_1]

2. **[CRITERIO_2] (Peso: [PESO_2])**
   - [DESCRICAO_CRITERIO_2]
   - Exemplo: [EXEMPLO_CRITERIO_2]

3. **[CRITERIO_3] (Peso: [PESO_3])**
   - [DESCRICAO_CRITERIO_3]
   - Exemplo: [EXEMPLO_CRITERIO_3]

4. **[CRITERIO_4] (Peso: [PESO_4])**
   - [DESCRICAO_CRITERIO_4]
   - Exemplo: [EXEMPLO_CRITERIO_4]

5. **[CRITERIO_5] (Peso: [PESO_5])**
   - [DESCRICAO_CRITERIO_5]
   - Exemplo: [EXEMPLO_CRITERIO_5]

**Por que estes critérios:**
- **[JUSTIFICATIVA_CRITERIOS_1]**: [EXPLICACAO_CRITERIOS_1]
- **[JUSTIFICATIVA_CRITERIOS_2]**: [EXPLICACAO_CRITERIOS_2]
- **[JUSTIFICATIVA_CRITERIOS_3]**: [EXPLICACAO_CRITERIOS_3]

## 2. Mapa de Dependências por Módulo
### 2.1. Módulo [MODULO_1] ([DESCRICAO_MODULO_1]) - [TIPO_COMPONENTE_1]

**Requisitos Fundamentais (Sem Dependências):**
- `[RF_MODULO_1_1]` ([DESCRICAO_RF_1_1])
- `[RF_MODULO_1_2]` ([DESCRICAO_RF_1_2])
- `[RF_MODULO_1_3]` ([DESCRICAO_RF_1_3])
- `[RF_MODULO_1_4]` ([DESCRICAO_RF_1_4])
- `[RF_MODULO_1_5]` ([DESCRICAO_RF_1_5])

**Dependências Internas do Módulo:**
```
[DEPENDENCIA_INTERNA_MODULO_1]
```

**Justificativa**: [JUSTIFICATIVA_MODULO_1]

### 2.2. Módulo [MODULO_2] ([DESCRICAO_MODULO_2]) - [TIPO_COMPONENTE_2]

**Requisitos Fundamentais (Sem Dependências):**
- `[RF_MODULO_2_1]` ([DESCRICAO_RF_2_1])
- `[RF_MODULO_2_2]` ([DESCRICAO_RF_2_2])
- `[RF_MODULO_2_3]` ([DESCRICAO_RF_2_3])
- `[RF_MODULO_2_4]` ([DESCRICAO_RF_2_4])

**Dependências Internas do Módulo:**
```
[DEPENDENCIA_INTERNA_MODULO_2]
```

**Justificativa**: [JUSTIFICATIVA_MODULO_2]

### 2.3. Módulo [MODULO_3] ([DESCRICAO_MODULO_3]) - [TIPO_COMPONENTE_3]

**Dependências Externas:**
- `[RF_MODULO_3_1]` ← `[RF_DEPENDENCIA_3_1]` ([DESCRICAO_DEPENDENCIA_3_1])
- `[RF_MODULO_3_1]` ← `[RF_DEPENDENCIA_3_2]` ([DESCRICAO_DEPENDENCIA_3_2])

**Dependências Internas:**
```
[DEPENDENCIA_INTERNA_MODULO_3]
```

**Justificativa**: [JUSTIFICATIVA_MODULO_3]

### 2.4. Módulo [MODULO_4] ([DESCRICAO_MODULO_4]) - [TIPO_COMPONENTE_4]

**Dependências Externas:**
- `[RF_MODULO_4_1]` ← `[RF_DEPENDENCIA_4_1]` ([DESCRICAO_DEPENDENCIA_4_1])
- `[RF_MODULO_4_1]` ← `[RF_DEPENDENCIA_4_2]` ([DESCRICAO_DEPENDENCIA_4_2])
- `[RF_MODULO_4_2]` ← `[RF_DEPENDENCIA_4_3]` ([DESCRICAO_DEPENDENCIA_4_3])

**Dependências Internas:**
```
[DEPENDENCIA_INTERNA_MODULO_4]
```

**Justificativa**: [JUSTIFICATIVA_MODULO_4]

### 2.5. Módulo [MODULO_5] ([DESCRICAO_MODULO_5]) - [TIPO_COMPONENTE_5]

**Dependências Externas:**
- `[RF_MODULO_5_1]` ← `[RF_DEPENDENCIA_5_1]` ([DESCRICAO_DEPENDENCIA_5_1])
- `[RF_MODULO_5_1]` ← `[RF_DEPENDENCIA_5_2]` ([DESCRICAO_DEPENDENCIA_5_2])
- `[RF_MODULO_5_3]` ← `[RF_DEPENDENCIA_5_3]` ([DESCRICAO_DEPENDENCIA_5_3])
- `[RF_MODULO_5_4]` ← `[RF_DEPENDENCIA_5_4]` ([DESCRICAO_DEPENDENCIA_5_4])

**Dependências Internas:**
```
[DEPENDENCIA_INTERNA_MODULO_5]
```

**Justificativa**: [JUSTIFICATIVA_MODULO_5]

### 2.6. Módulo [MODULO_6] ([DESCRICAO_MODULO_6]) - [TIPO_COMPONENTE_6]

**Dependências Externas:**
- `[RF_MODULO_6_1]` ← `[RF_DEPENDENCIA_6_1]` ([DESCRICAO_DEPENDENCIA_6_1])
- `[RF_MODULO_6_2]` ← `[RF_DEPENDENCIA_6_2]` ([DESCRICAO_DEPENDENCIA_6_2])
- `[RF_MODULO_6_3]` ← `[RF_DEPENDENCIA_6_3]` ([DESCRICAO_DEPENDENCIA_6_3])
- `[RF_MODULO_6_4]` ← `[RF_DEPENDENCIA_6_4]` ([DESCRICAO_DEPENDENCIA_6_4])

**Dependências Internas:**
```
[DEPENDENCIA_INTERNA_MODULO_6]
```

**Justificativa**: [JUSTIFICATIVA_MODULO_6]

## 3. Grafo de Dependências Críticas (Mermaid)

```mermaid
graph TD
    %% [MODULO_1] ([DESCRICAO_MODULO_1])
    [RF_MODULO_1_1]["[RF_MODULO_1_1]<br/>[DESCRICAO_RF_1_1]"] --> [RF_MODULO_1_2]["[RF_MODULO_1_2]<br/>[DESCRICAO_RF_1_2]"]
    [RF_MODULO_1_1] --> [RF_MODULO_1_3]["[RF_MODULO_1_3]<br/>[DESCRICAO_RF_1_3]"]
    [RF_MODULO_1_2] --> [RF_MODULO_1_4]["[RF_MODULO_1_4]<br/>[DESCRICAO_RF_1_4]"]
    [RF_MODULO_1_3] --> [RF_MODULO_1_4]
    [RF_MODULO_1_5]["[RF_MODULO_1_5]<br/>[DESCRICAO_RF_1_5]"] --> [RF_MODULO_1_1]
    
    %% [MODULO_2] ([DESCRICAO_MODULO_2])
    [RF_MODULO_1_4] --> [RF_MODULO_2_1]["[RF_MODULO_2_1]<br/>[DESCRICAO_RF_2_1]"]
    [RF_MODULO_2_1] --> [RF_MODULO_2_2]["[RF_MODULO_2_2]<br/>[DESCRICAO_RF_2_2]"]
    [RF_MODULO_2_2] --> [RF_MODULO_2_3]["[RF_MODULO_2_3]<br/>[DESCRICAO_RF_2_3]"]
    [RF_MODULO_2_3] --> [RF_MODULO_2_4]["[RF_MODULO_2_4]<br/>[DESCRICAO_RF_2_4]"]
    
    %% [MODULO_3] ([DESCRICAO_MODULO_3])
    [RF_MODULO_2_3] --> [RF_MODULO_3_1]["[RF_MODULO_3_1]<br/>[DESCRICAO_RF_3_1]"]
    [RF_MODULO_2_4] --> [RF_MODULO_3_1]
    [RF_MODULO_3_1] --> [RF_MODULO_3_2]["[RF_MODULO_3_2]<br/>[DESCRICAO_RF_3_2]"]
    
    %% [MODULO_4] ([DESCRICAO_MODULO_4])
    [RF_MODULO_2_3] --> [RF_MODULO_4_1]["[RF_MODULO_4_1]<br/>[DESCRICAO_RF_4_1]"]
    [RF_MODULO_4_1] --> [RF_MODULO_4_2]["[RF_MODULO_4_2]<br/>[DESCRICAO_RF_4_2]"]
    [RF_MODULO_4_2] --> [RF_MODULO_3_1]
    
    %% [MODULO_5] ([DESCRICAO_MODULO_5])
    [RF_MODULO_2_3] --> [RF_MODULO_5_1]["[RF_MODULO_5_1]<br/>[DESCRICAO_RF_5_1]"]
    [RF_MODULO_2_4] --> [RF_MODULO_5_1]
    [RF_MODULO_5_1] --> [RF_MODULO_5_2]["[RF_MODULO_5_2]<br/>[DESCRICAO_RF_5_2]"]
    [RF_MODULO_5_2] --> [RF_MODULO_5_3]["[RF_MODULO_5_3]<br/>[DESCRICAO_RF_5_3]"]
    [RF_MODULO_3_1] --> [RF_MODULO_5_3]
    [RF_MODULO_4_1] --> [RF_MODULO_5_3]
    [RF_MODULO_5_3] --> [RF_MODULO_5_4]["[RF_MODULO_5_4]<br/>[DESCRICAO_RF_5_4]"]
    
    %% [MODULO_6] ([DESCRICAO_MODULO_6])
    [RF_MODULO_2_3] --> [RF_MODULO_6_1]["[RF_MODULO_6_1]<br/>[DESCRICAO_RF_6_1]"]
    [RF_MODULO_3_1] --> [RF_MODULO_6_2]["[RF_MODULO_6_2]<br/>[DESCRICAO_RF_6_2]"]
    
    %% Styling
    classDef [CLASSE_ESTILO_1] fill:[COR_1],stroke:[COR_BORDA_1],stroke-width:[LARGURA_1],color:[COR_TEXTO_1]
    classDef [CLASSE_ESTILO_2] fill:[COR_2],stroke:[COR_BORDA_2],stroke-width:[LARGURA_2],color:[COR_TEXTO_2]
    classDef [CLASSE_ESTILO_3] fill:[COR_3],stroke:[COR_BORDA_3],stroke-width:[LARGURA_3],color:[COR_TEXTO_3]
    classDef [CLASSE_ESTILO_4] fill:[COR_4],stroke:[COR_BORDA_4],stroke-width:[LARGURA_4],color:[COR_TEXTO_4]
    classDef [CLASSE_ESTILO_5] fill:[COR_5],stroke:[COR_BORDA_5],stroke-width:[LARGURA_5],color:[COR_TEXTO_5]
    
    class [ELEMENTOS_CLASSE_1] [CLASSE_ESTILO_1]
    class [ELEMENTOS_CLASSE_2] [CLASSE_ESTILO_2]
    class [ELEMENTOS_CLASSE_3] [CLASSE_ESTILO_3]
    class [ELEMENTOS_CLASSE_4] [CLASSE_ESTILO_4]
    class [ELEMENTOS_CLASSE_5] [CLASSE_ESTILO_5]
```

## 4. Componentes de Núcleo Identificados

### 4.1. [NUCLEO_1] ([PRIORIDADE_NUCLEO_1])
**Módulo [MODULO_1] - [DESCRICAO_NUCLEO_1]:**
- `[RF_NUCLEO_1_1]` ([DESCRICAO_RF_NUCLEO_1_1])
- `[RF_NUCLEO_1_2]` ([DESCRICAO_RF_NUCLEO_1_2])
- `[RF_NUCLEO_1_3]` ([DESCRICAO_RF_NUCLEO_1_3])
- `[RF_NUCLEO_1_4]` ([DESCRICAO_RF_NUCLEO_1_4])
- `[RF_NUCLEO_1_5]` ([DESCRICAO_RF_NUCLEO_1_5])

**Critério**: [CRITERIO_NUCLEO_1]

### 4.2. [NUCLEO_2] ([PRIORIDADE_NUCLEO_2])
**Módulo [MODULO_2] - [DESCRICAO_NUCLEO_2]:**
- `[RF_NUCLEO_2_1]` ([DESCRICAO_RF_NUCLEO_2_1])
- `[RF_NUCLEO_2_2]` ([DESCRICAO_RF_NUCLEO_2_2])
- `[RF_NUCLEO_2_3]` ([DESCRICAO_RF_NUCLEO_2_3])
- `[RF_NUCLEO_2_4]` ([DESCRICAO_RF_NUCLEO_2_4])

**Critério**: [CRITERIO_NUCLEO_2]

### 4.3. [NUCLEO_3] ([PRIORIDADE_NUCLEO_3])
**Módulo [MODULO_3] + [MODULO_4] - [DESCRICAO_NUCLEO_3]:**
- `[RF_NUCLEO_3_1]` ([DESCRICAO_RF_NUCLEO_3_1])
- `[RF_NUCLEO_3_2]` ([DESCRICAO_RF_NUCLEO_3_2])
- `[RF_NUCLEO_3_3]` ([DESCRICAO_RF_NUCLEO_3_3])

**Critério**: [CRITERIO_NUCLEO_3]

### 4.4. [NUCLEO_4] ([PRIORIDADE_NUCLEO_4])
**Módulo [MODULO_5] - [DESCRICAO_NUCLEO_4]:**
- `[RF_NUCLEO_4_1]` ([DESCRICAO_RF_NUCLEO_4_1])
- `[RF_NUCLEO_4_2]` ([DESCRICAO_RF_NUCLEO_4_2])
- `[RF_NUCLEO_4_3]` ([DESCRICAO_RF_NUCLEO_4_3])
- `[RF_NUCLEO_4_4]` ([DESCRICAO_RF_NUCLEO_4_4])

**Critério**: [CRITERIO_NUCLEO_4]

## 5. Sequência Otimizada para Desenvolvimento

### 5.1. Fase 0 - [NOME_FASE_0] ([PERIODO_FASE_0])
1. `[RF_FASE_0_1]` - [DESCRICAO_FASE_0_1]
2. `[RF_FASE_0_2]` - [DESCRICAO_FASE_0_2]
3. `[RF_FASE_0_3]` - [DESCRICAO_FASE_0_3]

### 5.2. Fase 1 - [NOME_FASE_1] ([PERIODO_FASE_1])
4. `[RF_FASE_1_1]` - [DESCRICAO_FASE_1_1]
5. `[RF_FASE_1_2]` - [DESCRICAO_FASE_1_2]
6. `[RF_FASE_1_3]` - [DESCRICAO_FASE_1_3]

### 5.3. Fase 2 - [NOME_FASE_2] ([PERIODO_FASE_2])
7. `[RF_FASE_2_1]` - [DESCRICAO_FASE_2_1]
8. `[RF_FASE_2_2]` - [DESCRICAO_FASE_2_2]
9. `[RF_FASE_2_3]` - [DESCRICAO_FASE_2_3]

### 5.4. Fase 3 - [NOME_FASE_3] ([PERIODO_FASE_3])
10. `[RF_FASE_3_1]` - [DESCRICAO_FASE_3_1]
11. `[RF_FASE_3_2]` - [DESCRICAO_FASE_3_2]
12. `[RF_FASE_3_3]` - [DESCRICAO_FASE_3_3]

### 5.5. Fase 4 - [NOME_FASE_4] ([PERIODO_FASE_4])
13. `[RF_FASE_4_1]` - [DESCRICAO_FASE_4_1]
14. `[RF_FASE_4_2]` - [DESCRICAO_FASE_4_2]
15. `[RF_FASE_4_3]` - [DESCRICAO_FASE_4_3]

## 6. Impacto para Aplicação do RICE

### 6.1. Ajustes no "Effort" (Esforço)
- **[CATEGORIA_ESFORCO_1]**: [FORMULA_ESFORCO_1]
- **[CATEGORIA_ESFORCO_2]**: [FORMULA_ESFORCO_2]

### 6.2. Bônus de "Unlocking Value" (Valor de Desbloqueio)
- **[COMPONENTE_VALOR_1]**: +[PONTOS_VALOR_1] pontos ([JUSTIFICATIVA_VALOR_1])
- **[COMPONENTE_VALOR_2]**: +[PONTOS_VALOR_2] pontos ([JUSTIFICATIVA_VALOR_2])
- **[COMPONENTE_VALOR_3]**: +[PONTOS_VALOR_3] pontos ([JUSTIFICATIVA_VALOR_3])
- **[COMPONENTE_VALOR_4]**: +[PONTOS_VALOR_4] pontos ([JUSTIFICATIVA_VALOR_4])

### 6.3. Ajustes na "Probability" (Probabilidade)
- **[CATEGORIA_PROB_1]**: [AJUSTE_PROB_1]
- **[CATEGORIA_PROB_2]**: [AJUSTE_PROB_2]
- **[CATEGORIA_PROB_3]**: [AJUSTE_PROB_3]

## 7. Riscos e Mitigações Identificados

### 7.1. Riscos de Dependência
1. **[RISCO_1]**: [DESCRICAO_RISCO_1]
   - **Mitigação**: [MITIGACAO_RISCO_1]

2. **[RISCO_2]**: [DESCRICAO_RISCO_2]
   - **Mitigação**: [MITIGACAO_RISCO_2]

3. **[RISCO_3]**: [DESCRICAO_RISCO_3]
   - **Mitigação**: [MITIGACAO_RISCO_3]

### 7.2. Oportunidades Identificadas
1. **[OPORTUNIDADE_1]**: [DESCRICAO_OPORTUNIDADE_1]
2. **[OPORTUNIDADE_2]**: [DESCRICAO_OPORTUNIDADE_2]
3. **[OPORTUNIDADE_3]**: [DESCRICAO_OPORTUNIDADE_3]

## 7. Considerações de Orquestração Inteligente

### 7.1 Impacto na Specialized Intelligence

**Métricas de Eficiência de Orquestração**:
- **Tempo de Resolução de Dependências**: Medição do tempo para resolver bloqueios entre módulos
- **Taxa de Paralelização**: Percentual de desenvolvimento que pode ocorrer em paralelo
- **Índice de Retrabalho**: Frequência de mudanças devido a dependências mal mapeadas

**Integração com Sistema RAG**:
- Documentação automática de decisões de dependência
- Histórico de mudanças e justificativas
- Base de conhecimento para futuras decisões similares

### 7.2 Agentes de IA Envolvidos

**Tier 1 (MVP)**:
- `@AgenteM_Backend`: Implementação das dependências técnicas críticas
- `@AgenteM_Frontend`: Coordenação de fluxos UX dependentes
- `@AgenteM_Testes`: Validação de integração entre módulos dependentes

**Tier 2 (Pós-MVP)**:
- `@AgenteM_DevOps`: Automação de deploy considerando dependências
- `@AgenteM_Performance`: Otimização baseada no grafo de dependências

## 8. Próximos Passos Recomendados

1. **[PASSO_1]**: [DESCRICAO_PASSO_1]
2. **[PASSO_2]**: [DESCRICAO_PASSO_2]
3. **[PASSO_3]**: [DESCRICAO_PASSO_3]
4. **[PASSO_4]**: [DESCRICAO_PASSO_4]
5. **[PASSO_5]**: [DESCRICAO_PASSO_5]
6. **[PASSO_6]**: [DESCRICAO_PASSO_6]

## 9. Histórico de Versões

### v1.1 (Junho 2025) - Orquestração Inteligente e Specialized Intelligence
- **Adição**: Considerações de orquestração inteligente e métricas de specialized intelligence
- **Melhoria**: Integração com sistema RAG para documentação automática de decisões
- **Expansão**: Mapeamento de agentes de IA por tier para implementação das dependências
- **Alinhamento**: Sincronização com documentos centrais atualizados (GUIA_AVANCADO v1.1, HLD v1.1, ERS v1.1)
- **Framework**: Inclusão de métricas de eficiência de orquestração e índices de qualidade
- **Correção**: Atualização de versões e datas para refletir o estado atual (Junho 2025)

### v1.0 (Maio 2025) - Versão Inicial
- **Criação**: Mapeamento inicial de dependências baseado no ERS v0.9
- **Estrutura**: Definição de critérios, grafo de dependências e componentes de núcleo
- **Metodologia**: Aplicação de framework RICE ajustado
- **Sequenciamento**: Proposta de fases de desenvolvimento otimizadas

## 10. Documentos Relacionados

### Documentos de Gestão
- [[docs/00_Gerenciamento_Projeto/01_TAP.md]] - Termo de Abertura do Projeto
- [[docs/01_Guias_Centrais/01_PLANO_MESTRE_[NOME_DO_PROJETO].md]] - Plano Mestre e Roadmap
- [[docs/01_Guias_Centrais/02_GUIA_AVANCADO.md]] - Metodologia de Orquestração Inteligente
- [[docs/00_Gerenciamento_Projeto/KANBAN/]] - Prioridades e Status

### Documentos Técnicos
- [[docs/02_Requisitos/01_ERS.md]] - Especificação de Requisitos de Software
- [[docs/03_Arquitetura_e_Design/01_HLD.md]] - Arquitetura de Alto Nível
- [[docs/04_Agentes_IA/02_AGENTES_IA_MENTORES_OVERVIEW.md]] - Visão Geral dos Agentes
- [[docs/01_Guias_Centrais/07_GLOSSARIO_[NOME_DO_PROJETO].md]] - Glossário do Projeto

### Perfis de Agentes
- [[docs/04_Agentes_IA/01_Perfis/]] - Perfis detalhados dos Agentes de IA Mentores

---

**Critérios de Validação deste Documento:**
- ✅ Dependências mapeadas com critérios explícitos
- ✅ Componentes de núcleo identificados
- ✅ Sequência otimizada proposta
- ✅ Impactos para RICE documentados
- ✅ Riscos e oportunidades analisados

**Nota**: Este documento é parte da "Documentação Viva" do projeto [NOME_DO_PROJETO], integrado à metodologia de "Orquestração Inteligente" e "Specialized Intelligence". É atualizado automaticamente conforme o desenvolvimento progride e novas dependências são identificadas, com todas as decisões documentadas no sistema RAG para aprendizado contínuo.

--- FIM DO DOCUMENTO MAPEAMENTO_DEPENDENCIAS_RF.md (v1.1) ---