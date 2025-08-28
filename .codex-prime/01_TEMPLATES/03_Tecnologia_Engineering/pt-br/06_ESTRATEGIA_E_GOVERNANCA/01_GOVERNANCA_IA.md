---
title: "Template: 01_GOVERNANCA_IA"
doc_id: "CODEX-PRIME-TECNOLOGIA-01-GOVERNANCA-IA-V1.0"
version: "1.0"
migrated_at: "2025-08-19 22:10:06"
timezone: "America/Sao_Paulo"
status: "Template"
owner: "@ArquitetoDoCodex"
tags: [template, codex-prime, v1.0, tecnologia]
description: "Template migrado do .codex para .codex-prime na versao 1.0"
source_path: "\03_Tecnologia_Engineering\pt-br\07_ESTRATEGIA_E_GOVERNANCA\01_GOVERNANCA_IA.md"
---

# Processo de Validação RAG - Recoloca.ai

**Versão:** 1.0  
**Data:** 19 de junho de 2025  
**Responsável:** @AgenteM_DevFastAPI + Maestro  
**Status:** ✅ Validado e Operacional  

## 📋 Resumo Executivo

Este documento registra o processo completo de validação do sistema RAG (Retrieval-Augmented Generation) do projeto Recoloca.ai, incluindo a resolução de problemas de configuração MCP, correções de importação e estabelecimento de procedimentos para futuras verificações.

## 🎯 Objetivo

Estabelecer um processo padronizado e reproduzível para validar o funcionamento do sistema RAG, garantindo que:
- O servidor MCP RAG esteja inicializado corretamente
- As consultas semânticas retornem resultados relevantes
- A qualidade das respostas atenda aos padrões do projeto
- Problemas sejam identificados e resolvidos rapidamente

## 🔧 Configuração Técnica Validada

### Stack RAG Operacional
- **Backend:** PyTorch com CUDA (RTX 2060)
- **Embedding Model:** BAAI/bge-m3 via Sentence Transformers
- **Vector Store:** FAISS-GPU
- **Documentos Indexados:** 281 documentos
- **Servidor MCP:** `mcp.config.usrlocalmcp.recoloca-rag`

### Configuração de Caminhos
- **Formato Validado:** Barras normais (`/`) em todos os caminhos
- **Diretório Source:** `rag_infra/source_documents`
- **Índice FAISS:** `rag_infra/data/indexes/faiss_index`

## 📝 Processo de Validação (Checklist)

### 1. Verificação de Status Inicial
```bash
# Via MCP RAG
rag_get_status
```

**Critérios de Sucesso:**
- ✅ `"initialized": true`
- ✅ `"last_error": null`
- ✅ Diretórios existem nos caminhos especificados
- ✅ Número de documentos indexados > 0

### 2. Teste de Consulta Básica
```bash
# Via MCP RAG
rag_query: "arquitetura do sistema Recoloca.ai"
```

**Critérios de Sucesso:**
- ✅ Retorna resultados (score > 0.3)
- ✅ Conteúdo relevante sobre arquitetura
- ✅ Metadados corretos (source, chunk_index, etc.)

### 3. Teste de Consulta Específica
```bash
# Via MCP RAG
rag_query: "stack tecnológica FastAPI Python Supabase Flutter"
```

**Critérios de Sucesso:**
- ✅ Informações precisas sobre a stack
- ✅ Componentes arquiteturais corretos
- ✅ Tecnologias alinhadas com o projeto

### 4. Validação de Qualidade
- **Relevância:** Resultados relacionados à consulta
- **Precisão:** Informações técnicas corretas
- **Completude:** Cobertura adequada dos tópicos
- **Atualidade:** Dados alinhados com versões atuais dos documentos

## 🚨 Problemas Identificados e Soluções

### Problema 1: Erro de Importação `get_retriever`
**Sintoma:** `name 'get_retriever' is not defined`

**Causa:** Função `get_retriever` não importada em `mcp_server.py`

**Solução Aplicada:**
```python
# Em rag_infra/server/mcp_server.py
from rag_infra.src.core.core_logic.rag_retriever import (
    RAGRetriever, 
    initialize_retriever, 
    search_documents,
    get_retriever  # ← Adicionado
)
```

### Problema 2: Cache de Código no Trae IDE
**Sintoma:** Correções não refletidas após modificação

**Causa:** IDE mantém versão antiga do código em cache

**Solução:** Reiniciar o Trae IDE após correções críticas

### Problema 3: Configuração de Caminhos
**Sintoma:** Problemas de inicialização com barras invertidas

**Causa:** Incompatibilidade entre formato Windows e configuração MCP

**Solução:** Usar barras normais (`/`) em todas as configurações

## 🔄 Procedimento de Reindexação

### Quando Reindexar
- Após adicionar novos documentos
- Quando há inconsistências nos resultados
- Após correções na estrutura de documentos
- Em caso de corrupção do índice

### Comando de Reindexação
```bash
# Via MCP RAG
rag_reindex:
  force_cpu: false  # Usar GPU se disponível
  clear_cache: true # Limpar cache antes
```

## 📊 Métricas de Validação

### Métricas Técnicas
- **Tempo de Inicialização:** < 30 segundos
- **Tempo de Consulta:** < 2 segundos
- **Score Mínimo:** 0.3 para resultados relevantes
- **Documentos Indexados:** 281 (atual)

### Métricas de Qualidade
- **Precisão:** > 80% de resultados relevantes
- **Cobertura:** Todos os documentos principais indexados
- **Atualidade:** Sincronização com documentação viva

## 🔍 Troubleshooting Rápido

### Servidor Não Inicializado
1. Verificar logs em `rag_infra/logs/`
2. Validar caminhos de configuração
3. Executar `rag_reindex` com `clear_cache: true`
4. Reiniciar Trae IDE se necessário

### Resultados de Baixa Qualidade
1. Verificar score mínimo (ajustar se necessário)
2. Revisar query (ser mais específico)
3. Validar se documentos relevantes estão indexados
4. Considerar reindexação

### Erros de Importação
1. Verificar imports em `mcp_server.py`
2. Validar estrutura de diretórios
3. Confirmar dependências instaladas
4. Reiniciar servidor MCP

## 📚 Referências Técnicas

- **Configuração MCP:** `rag_infra/config/trae_mcp_config.json`
- **Servidor RAG:** `rag_infra/server/mcp_server.py`
- **Core Logic:** `rag_infra/src/core/core_logic/rag_retriever.py`
- **Documentação:** `rag_infra/docs/README_RAG_OPERACIONAL.md`

## 🎯 Próximos Passos

### Melhorias Planejadas
1. **Health Checks Automatizados:** Implementar verificações periódicas
2. **Logging Estruturado:** Melhorar rastreabilidade de problemas
3. **Métricas de Performance:** Dashboard de monitoramento
4. **Testes de Integração:** Automatizar validação completa

### Integração com Backend FastAPI
1. Implementar endpoints de consulta RAG
2. Adicionar cache de resultados
3. Configurar rate limiting
4. Implementar logging de uso

## ✅ Status de Validação

**Data da Última Validação:** 19 de junho de 2025  
**Status:** ✅ OPERACIONAL  
**Próxima Validação:** Semanal ou após mudanças significativas  

---

## 🔄 Esclarecimento: DeepView vs RAG Recoloca.ai

### Confusão Identificada

Durante a análise da documentação, foi identificada uma **confusão terminológica** sobre "DeepView" no contexto do projeto:

### O que é DeepView (Real)
**DeepView MCP** é um servidor Model Context Protocol externo que:
- Analisa codebases grandes usando o contexto extenso do Gemini
- É uma ferramenta de análise de código, não um sistema RAG
- Funciona como MCP server para IDEs como Cursor e Windsurf

### O que é o RAG do Recoloca.ai
**Nosso sistema RAG** (`mcp.config.usrlocalmcp.recoloca-rag`) é:
- Sistema de recuperação semântica específico do projeto
- Indexa documentação viva do Recoloca.ai
- Usa FAISS + embeddings BAAI/bge-m3
- Servidor MCP customizado para o projeto

### Origem da Confusão
A documentação do projeto faz referência a "deepview" como:
- Uma ferramenta MCP disponível para análise de código
- Sistema RAG para análise da documentação (incorreto)
- Análise semântica do codebase

### Correção Necessária
**Ação Requerida:** Atualizar documentação para distinguir claramente:
1. **RAG Recoloca.ai:** Sistema interno de documentação
2. **DeepView MCP:** Ferramenta externa de análise de código
3. **Context7 MCP:** Documentação oficial de bibliotecas

### Recomendação
Manter a referência ao DeepView como ferramenta MCP disponível, mas esclarecer que:
- É diferente do nosso sistema RAG interno
- Serve para análise de código, não documentação do projeto
- Complementa, mas não substitui, nosso RAG customizado

---

**FIM DO DOCUMENTO PROCESSO_VALIDACAO_RAG.md (v1.0)**
