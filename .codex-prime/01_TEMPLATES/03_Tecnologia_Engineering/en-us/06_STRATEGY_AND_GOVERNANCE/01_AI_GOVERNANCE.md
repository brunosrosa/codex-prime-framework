---
title: "AI Governance Template"
doc_id: "AI-GOVERNANCE-TEMPLATE-v1.0"
version: "1.0"
migration_date: "2025-01-23"
status: "Template"
owner: "@ArquitetoDoCodex"
tags: [ai-governance, rag, validation, mcp, template]
description: "Comprehensive template for AI governance including RAG system validation, MCP server management, and AI integration best practices."
source_path: "/.codex-prime/01_TEMPLATES/03_Tecnologia_Engineering/en-us/07_STRATEGY_AND_GOVERNANCE/01_AI_GOVERNANCE.md"
---

# RAG System Validation Process - [PROJECT_NAME]

**Version:** 1.0  
**Date:** [DATE]  
**Responsible:** @BackendDeveloperAgent_M + Maestro  
**Status:** ✅ Validated and Operational  

## 📋 Executive Summary

This document records the complete validation process for the RAG (Retrieval-Augmented Generation) system of [PROJECT_NAME], including MCP configuration issue resolution, import corrections, and establishment of procedures for future verifications.

## 🎯 Objective

Establish a standardized and reproducible process to validate RAG system functionality, ensuring that:
- The MCP RAG server is correctly initialized
- Semantic queries return relevant results
- Response quality meets project standards
- Issues are identified and resolved quickly

## 🔧 Validated Technical Configuration

### Operational RAG Stack
- **Backend:** PyTorch with CUDA ([GPU_MODEL])
- **Embedding Model:** BAAI/bge-m3 via Sentence Transformers
- **Vector Store:** FAISS-GPU
- **Indexed Documents:** [NUMBER] documents
- **MCP Server:** `mcp.config.usrlocalmcp.[project-name]-rag`

### Path Configuration
- **Validated Format:** Normal slashes (`/`) in all paths
- **Source Directory:** `rag_infra/source_documents`
- **FAISS Index:** `rag_infra/data/indexes/faiss_index`

## 📝 Validation Process (Checklist)

### 1. Initial Status Verification
```bash
# Via MCP RAG
rag_get_status
```

**Success Criteria:**
- ✅ `"initialized": true`
- ✅ `"last_error": null`
- ✅ Directories exist in specified paths
- ✅ Number of indexed documents > 0

### 2. Basic Query Test
```bash
# Via MCP RAG
rag_query: "[project name] system architecture"
```

**Success Criteria:**
- ✅ Returns results (score > 0.3)
- ✅ Relevant content about architecture
- ✅ Correct metadata (source, chunk_index, etc.)

### 3. Specific Query Test
```bash
# Via MCP RAG
rag_query: "technology stack [BACKEND_TECH] [DATABASE] [FRONTEND_TECH]"
```

**Success Criteria:**
- ✅ Accurate information about the stack
- ✅ Correct architectural components
- ✅ Technologies aligned with the project

### 4. Quality Validation
- **Relevance:** Results related to the query
- **Accuracy:** Correct technical information
- **Completeness:** Adequate topic coverage
- **Currency:** Data aligned with current document versions

## 🚨 Identified Problems and Solutions

### Problem 1: `get_retriever` Import Error
**Symptom:** `name 'get_retriever' is not defined`

**Cause:** `get_retriever` function not imported in `mcp_server.py`

**Applied Solution:**
```python
# In rag_infra/server/mcp_server.py
from rag_infra.src.core.core_logic.rag_retriever import (
    RAGRetriever, 
    initialize_retriever, 
    search_documents,
    get_retriever  # ← Added
)
```

### Problem 2: Code Cache in Trae IDE
**Symptom:** Corrections not reflected after modification

**Cause:** IDE maintains old version of code in cache

**Solution:** Restart Trae IDE after critical corrections

### Problem 3: Path Configuration
**Symptom:** Initialization problems with backslashes

**Cause:** Incompatibility between Windows format and MCP configuration

**Solution:** Use normal slashes (`/`) in all configurations

## 🔄 Reindexing Procedure

### When to Reindex
- After adding new documents
- When there are inconsistencies in results
- After corrections in document structure
- In case of index corruption

### Reindexing Command
```bash
# Via MCP RAG
rag_reindex:
  force_cpu: false  # Use GPU if available
  clear_cache: true # Clear cache before
```

## 📊 Validation Metrics

### Technical Metrics
- **Initialization Time:** < 30 seconds
- **Query Time:** < 2 seconds
- **Minimum Score:** 0.3 for relevant results
- **Indexed Documents:** [NUMBER] (current)

### Quality Metrics
- **Precision:** > 80% relevant results
- **Coverage:** All main documents indexed
- **Currency:** Synchronization with living documentation

## 🔍 Quick Troubleshooting

### Server Not Initialized
1. Check logs in `rag_infra/logs/`
2. Validate configuration paths
3. Execute `rag_reindex` with `clear_cache: true`
4. Restart Trae IDE if necessary

### Low Quality Results
1. Check minimum score (adjust if necessary)
2. Review query (be more specific)
3. Validate if relevant documents are indexed
4. Consider reindexing

### Import Errors
1. Verify imports in `mcp_server.py`
2. Validate directory structure
3. Confirm installed dependencies
4. Restart MCP server

## 📚 Technical References

- **MCP Configuration:** `rag_infra/config/trae_mcp_config.json`
- **RAG Server:** `rag_infra/server/mcp_server.py`
- **Core Logic:** `rag_infra/src/core/core_logic/rag_retriever.py`
- **Documentation:** `rag_infra/docs/README_RAG_OPERATIONAL.md`

## 🎯 Next Steps

### Planned Improvements
1. **Automated Health Checks:** Implement periodic verifications
2. **Structured Logging:** Improve problem traceability
3. **Performance Metrics:** Monitoring dashboard
4. **Integration Tests:** Automate complete validation

### Backend Integration
1. Implement RAG query endpoints
2. Add result caching
3. Configure rate limiting
4. Implement usage logging

## ✅ Validation Status

**Last Validation Date:** [DATE]  
**Status:** ✅ OPERATIONAL  
**Next Validation:** Weekly or after significant changes  

---

## 🔄 Clarification: External Tools vs Internal RAG

### Identified Confusion

During documentation analysis, a **terminological confusion** was identified about external analysis tools in the project context:

### What is DeepView (Real)
**DeepView MCP** is an external Model Context Protocol server that:
- Analyzes large codebases using Gemini's extended context
- Is a code analysis tool, not a RAG system
- Functions as MCP server for IDEs like Cursor and Windsurf

### What is [PROJECT_NAME] RAG
**Our RAG system** (`mcp.config.usrlocalmcp.[project-name]-rag`) is:
- Project-specific semantic retrieval system
- Indexes [PROJECT_NAME] living documentation
- Uses FAISS + BAAI/bge-m3 embeddings
- Custom MCP server for the project

### Source of Confusion
Project documentation references external tools as:
- MCP tools available for code analysis
- RAG system for documentation analysis (incorrect)
- Semantic codebase analysis

### Required Correction
**Required Action:** Update documentation to clearly distinguish:
1. **[PROJECT_NAME] RAG:** Internal documentation system
2. **External MCP Tools:** External code analysis tools
3. **Context7 MCP:** Official library documentation

### Recommendation
Maintain reference to external tools as available MCP tools, but clarify that:
- They are different from our internal RAG system
- They serve for code analysis, not project documentation
- They complement, but do not replace, our custom RAG

---

## 🤖 AI Integration Best Practices

### MCP Server Management
- **Naming Convention:** `mcp.config.usrlocalmcp.[project-name]-[service]`
- **Configuration Path:** `[project_root]/config/mcp/`
- **Health Monitoring:** Implement status endpoints
- **Error Handling:** Graceful degradation on failures

### RAG System Guidelines
- **Document Chunking:** Optimal size 512-1024 tokens
- **Embedding Model:** Use domain-specific models when available
- **Vector Store:** FAISS for performance, Chroma for development
- **Query Processing:** Implement query expansion and filtering

### AI Agent Coordination
- **Agent Hierarchy:** Define clear roles and responsibilities
- **Communication Protocol:** Standardized message formats
- **Conflict Resolution:** Escalation procedures
- **Performance Monitoring:** Track agent effectiveness

### Security and Privacy
- **Data Sanitization:** Remove sensitive information before indexing
- **Access Control:** Implement role-based permissions
- **Audit Logging:** Track all AI system interactions
- **Model Governance:** Version control for AI models

### Quality Assurance
- **Response Validation:** Implement quality scoring
- **Human-in-the-Loop:** Critical decision checkpoints
- **Continuous Learning:** Feedback incorporation mechanisms
- **Performance Benchmarks:** Regular evaluation against baselines

---

**END OF AI_GOVERNANCE.md TEMPLATE (v1.0)**

*"Effective AI governance ensures that artificial intelligence serves as a reliable partner in achieving project objectives."*