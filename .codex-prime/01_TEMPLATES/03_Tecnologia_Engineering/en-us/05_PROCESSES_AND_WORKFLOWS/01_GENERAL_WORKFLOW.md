---
title: "General Workflow Template"
doc_id: "GENERAL-WORKFLOW-TEMPLATE-v1.0"
version: "1.0"
migration_date: "2025-01-23"
status: "Template"
owner: "@ArquitetoDoCodex"
tags: [workflow, process, agile, ai-agents, orchestration, sdlc]
description: "Comprehensive template for general workflow processes in AI-augmented development projects, based on Intelligent Orchestration methodology with specialized domain expertise."
source_path: "/.codex-prime/01_TEMPLATES/03_Tecnologia_Engineering/en-us/05_PROCESSES_AND_WORKFLOWS/01_GENERAL_WORKFLOW.md"
---

# General Workflow Template

## 1. Overview and Philosophy

### 1.1. Methodology Foundation
**Base Methodology**: "AI-Augmented Solo Agile Development"
**Core Focus**: Intelligent orchestration with domain specialization
**Central Agent**: `@OrchestratorAgent_M` (PM Mentor and Prompt Engineer)
**Specialized Mentors**: Domain-specific agents for each SDLC phase

### 1.2. Workflow Principles
- **Strategic Validation**: Every task undergoes strategic alignment verification
- **Constructive Questioning**: Challenge assumptions before implementation
- **RAG-Driven Analysis**: Leverage knowledge base for informed decisions
- **Core Component Identification**: Distinguish critical vs. standard components
- **Prompt Co-creation**: Collaborative prompt engineering for optimal results
- **Rich Contextualization**: Comprehensive context provision to agents
- **Best Practices Application**: Consistent application of proven methodologies
- **Adaptive Templates**: Dynamic template usage based on task requirements

## 2. Main Development Flow

```mermaid
flowchart TD
    A["New Task"] --> B["@OrchestratorAgent_M\nStrategic Analysis"]
    B --> C{"Task Complexity\nAssessment"}
    
    C -->|Simple| D["Direct Execution\nSpecialized Agent"]
    C -->|Complex| E["Multi-Phase\nOrchestration"]
    C -->|Core Component| F["Enhanced Security\n& Quality Process"]
    
    D --> G["Quality Review"]
    E --> H["Phase Coordination"]
    F --> I["Security Review"]
    
    H --> G
    I --> G
    G --> J["Delivery"]
    J --> K["Metrics Collection"]
    K --> L["Next Iteration"]
    
    classDef orchestrator fill:#ff9999,stroke:#333,stroke-width:3px
    classDef agent fill:#99ccff,stroke:#333,stroke-width:2px
    classDef process fill:#99ff99,stroke:#333,stroke-width:2px
    
    class B orchestrator
    class D,E,F,H,I agent
    class A,C,G,J,K,L process
```

## 3. Orchestrator Agent (`@OrchestratorAgent_M`)

### 3.1. Core Responsibilities
**Primary Role**: PM Mentor and Prompt Engineer

**Key Functions**:
- **Strategic Validation**: Ensure alignment with project objectives
- **Constructive Questioning**: Challenge assumptions and validate approaches
- **RAG Analysis**: Leverage knowledge base for informed decision-making
- **Core Component Identification**: Distinguish critical system components
- **Prompt Co-creation**: Collaborate on optimal prompt engineering
- **Rich Contextualization**: Provide comprehensive context to specialized agents
- **Best Practices Application**: Ensure consistent methodology application
- **Adaptive Templates**: Select and customize templates based on task requirements

### 3.2. Orchestration Process

```mermaid
sequenceDiagram
    participant M as Maestro
    participant O as @OrchestratorAgent_M
    participant RAG as Knowledge Base
    participant SA as Specialized Agent
    
    M->>O: Task Request
    O->>RAG: Context Analysis
    RAG-->>O: Relevant Knowledge
    O->>O: Strategic Assessment
    
    alt Clarification Needed
        O->>M: Strategic Questions
        M->>O: Clarifications
    end
    
    O->>O: Agent Selection & Prompt Engineering
    O->>SA: Contextualized Task
    SA->>SA: Task Execution
    SA->>O: Deliverable
    O->>O: Quality Review
    O->>M: Final Delivery
```

### 3.3. Activation Criteria
- **New Task Reception**: All tasks pass through orchestrator first
- **Complexity Assessment**: Evaluate task complexity and requirements
- **Agent Selection**: Choose appropriate specialized agent(s)
- **Context Preparation**: Gather and structure relevant context
- **Quality Assurance**: Review deliverables before final submission

## 4. Agent Evolution Strategy

### 4.1. Maturity Levels

#### Basic Level (Tier 1)
**Characteristics**:
- Follows explicit instructions
- Requires detailed prompts
- Limited autonomous decision-making
- Basic template usage

**Objective Criteria**:
- Task completion rate: >70%
- Instruction adherence: >85%
- Template compliance: >90%
- Revision requests: <30%

#### Intermediate Level (Tier 2)
**Characteristics**:
- Contextual understanding
- Proactive suggestions
- Pattern recognition
- Adaptive template usage

**Objective Criteria**:
- Task completion rate: >85%
- Proactive improvements: >20% of tasks
- Context utilization: >80%
- Revision requests: <15%

#### Advanced Level (Tier 3)
**Characteristics**:
- Strategic thinking
- Cross-domain knowledge
- Innovation capability
- Template creation/modification

**Objective Criteria**:
- Task completion rate: >95%
- Strategic contributions: >40% of tasks
- Innovation instances: >10% of tasks
- Revision requests: <5%

### 4.2. HITL Evolution Process

```mermaid
flowchart LR
    A["Performance\nAssessment"] --> B["Criteria\nEvaluation"]
    B --> C{"Promotion\nEligible?"}
    C -->|Yes| D["Human\nValidation"]
    C -->|No| E["Improvement\nPlan"]
    D --> F["Tier\nPromotion"]
    E --> G["Targeted\nTraining"]
    F --> H["New\nCapabilities"]
    G --> A
    H --> A
    
    classDef assessment fill:#e3f2fd,stroke:#1565c0,stroke-width:2px
    classDef decision fill:#fff3e0,stroke:#ef6c00,stroke-width:2px
    classDef action fill:#e8f5e8,stroke:#2e7d32,stroke-width:2px
    
    class A,B assessment
    class C,D decision
    class E,F,G,H action
```

## 5. Living Documentation and RAG Integration

### 5.1. RAG Strategy for Workflow

**Knowledge Sources**:
- Project documentation (`/.codex/`)
- Best practices repository
- Historical task patterns
- Agent performance data
- Domain-specific knowledge bases

**RAG Technologies**:
- **Vector Database**: FAISS-GPU for high-performance similarity search
- **Embedding Model**: BAAI/bge-m3 for multilingual support
- **Framework**: LangChain for orchestration
- **Runtime**: Python 3.10 for optimal performance

### 5.2. Documentation Update Cycle

```mermaid
gantt
    title Documentation Maintenance Cycle
    dateFormat  YYYY-MM-DD
    section Daily
    Task Logs           :active, daily1, 2025-01-01, 1d
    Metrics Collection  :active, daily2, 2025-01-01, 1d
    section Weekly
    Pattern Analysis    :weekly1, 2025-01-01, 7d
    Process Refinement  :weekly2, after weekly1, 7d
    section Monthly
    Knowledge Base Update :monthly1, 2025-01-01, 30d
    Agent Performance Review :monthly2, after monthly1, 30d
```

## 6. Neurodivergent Considerations

### 6.1. Inclusive Design Principles
- **Clear Structure**: Consistent formatting and organization
- **Immediate Feedback**: Real-time status updates and confirmations
- **Cognitive Flexibility**: Multiple approaches to task completion
- **Overload Reduction**: Chunked information and progressive disclosure
- **Predictable Patterns**: Standardized workflows and templates

### 6.2. Adaptive Features
- **Customizable Interfaces**: Adjustable complexity levels
- **Multiple Input Methods**: Text, voice, and visual options
- **Progress Tracking**: Visual indicators and milestone markers
- **Break Reminders**: Automated wellness check-ins
- **Sensory Considerations**: Reduced visual noise and distractions

## 7. Metrics and Monitoring

### 7.1. Workflow KPIs

| **Metric** | **Target** | **Frequency** |
|------------|------------|---------------|
| **Task Completion Rate** | > 90% | Daily |
| **Average Cycle Time** | < 2 hours (simple tasks) | Weekly |
| **First-Time Right Rate** | > 85% | Weekly |
| **Rework Rate** | < 15% | Weekly |
| **Maestro Satisfaction** | > 8/10 | After each delivery |
| **Agent Accuracy** | > 80% (Basic Level) | Monthly |
| **RAG Coverage** | > 90% successful queries | Monthly |

### 7.2. Continuous Improvement Process

```mermaid
graph LR
    A["Metrics\nCollection"] --> B["Pattern\nAnalysis"]
    B --> C["Bottleneck\nIdentification"]
    C --> D["Process\nRefinement"]
    D --> E["Documentation\nUpdate"]
    E --> A
    
    classDef process fill:#e3f2fd,stroke:#1565c0,stroke-width:2px
    class A,B,C,D,E process
```

## 8. Task-Specific Flows

### 8.1. Complete Feature Development

```mermaid
sequenceDiagram
    participant M as Maestro
    participant O as @OrchestratorAgent_M
    participant A as @ArchitectAgent_M
    participant U as @UXUIAgent_M
    participant D as @DevFastAPIAgent_M
    participant F as @DevFlutterAgent_M
    participant Q as @QAAgent_M
    
    M->>O: New feature request
    O->>O: Strategic analysis (RAG)
    O->>M: Clarifying questions
    M->>O: Validation and approval
    O->>A: Architecture prompt
    O->>U: UX/UI prompt
    
    par Parallel Development
        A->>A: Create HLD/LLD
        U->>U: Design UX/UI
    end
    
    A->>D: Backend specifications
    U->>F: Frontend specifications
    
    par Implementation
        D->>D: Develop API
        F->>F: Develop UI
    end
    
    D->>Q: Backend code ready
    F->>Q: Frontend code ready
    Q->>Q: Integrated testing
    Q->>M: Delivery for review
```

### 8.2. Bug Fix

```mermaid
sequenceDiagram
    participant M as Maestro
    participant O as @OrchestratorAgent_M
    participant D as Specialized Dev
    participant Q as @QAAgent_M
    
    M->>O: Bug report
    O->>O: Impact analysis
    
    alt Simple Bug
        O->>D: Direct fix
        D->>Q: Fix implemented
    else Complex Bug
        O->>M: Deep analysis needed
        M->>O: Investigation approval
        O->>D: Investigation and fix
        D->>Q: Fix implemented
    end
    
    Q->>M: Final validation
```

### 8.3. Core Component

```mermaid
sequenceDiagram
    participant M as Maestro
    participant O as @OrchestratorAgent_M
    participant A as @ArchitectAgent_M
    participant S as @SecurityAgent_M
    participant D as @DevFastAPIAgent_M
    participant Q as @QAAgent_M
    participant DevOps as @DevOpsAgent_M
    
    M->>O: Critical component
    O->>O: Rigorous strategic validation
    O->>A: Architectural analysis
    A->>S: Security review
    S->>O: Security approval
    O->>D: Secure implementation
    D->>Q: Extensive testing
    Q->>DevOps: Gradual deployment
    DevOps->>M: Active monitoring
```

## 9. Implementation and Evolution

### 9.1. Immediate Implementation
1. **Maestro Validation**: Aligned workflow approval
2. **Agent Training**: Apply maturity criteria
3. **RAG Integration**: Complete knowledge base setup
4. **Baseline Metrics**: Establish initial indicators

### 9.2. Planned Evolution (6-12 months)
1. **Progressive Automation**: Gradual reduction of manual supervision
2. **Advanced Specialization**: Development of agent-specific expertise
3. **Tool Integration**: Additional MCPs as needed
4. **Performance Optimization**: Data-driven continuous improvement

### 9.3. Strategic Considerations

#### 9.3.1. Reflection Questions
1. **Balance**: How to balance agent autonomy with strategic control?
2. **Scalability**: How does the workflow adapt to project growth?
3. **Quality**: How to maintain consistency with increasing autonomy?
4. **Innovation**: How to incorporate learnings and continuous improvements?

#### 9.3.2. Risks and Mitigations
- **Risk**: Loss of control with excessive automation
  - **Mitigation**: Objective maturity criteria and escalation
- **Risk**: Inconsistency between agents
  - **Mitigation**: Centralized RAG and living documentation
- **Risk**: Orchestrator overload
  - **Mitigation**: Gradual evolution and intelligent delegation

## 10. Related Documents

- **Advanced Methodology Guide** - Base methodology (v1.1)
- **MVP Methodology** - Methodology MVP
- **Requirements Specification** (v1.1) - System requirements
- **High-Level Design** (v1.1) - Architecture overview
- **Core Tools ADR** (v1.1) - Technology decisions
- **AI Agents Overview** - Agent specifications
- **Internal Kanban** - Task management
- **Prompt Templates** - Base prompt library
- **PM Knowledge Base** - Project management resources

## 11. Intelligent Orchestration Considerations

### 11.1. Integration with Methodology v1.1
- **Production-Ready Agents**: Workflow supports Tier 2 and Tier 3 agents
- **Continuous Metrics**: Automated productivity data collection
- **Operational RAG**: Continuous contextualization via knowledge base
- **Specialized Intelligence**: Efficient delegation to specialized agents

### 11.2. Validation Criteria
- ✅ **Efficiency**: Reduced development time
- ✅ **Quality**: Improved deliverable quality
- ✅ **Consistency**: Process standardization
- ✅ **Scalability**: Support for agent team growth

## 12. Version History

### v1.1 (June 2025) - Intelligent Orchestration and Specialized Intelligence
- Updated references to v1.1 documents
- Alignment with Intelligent Orchestration methodology
- Added considerations for Production-Ready agents
- Integration with productivity metrics

### v1.0 (May 2025) - Initial Version
- Base workflow definition
- Establishment of adapted agile processes
- Initial AI agent integration

**Note:** This document (v1.1) is fully aligned with the "Intelligent Orchestration" and "Specialized Intelligence" methodology defined in the Advanced Guide (v1.1), incorporating optimized flows for Production-Ready agents and continuous productivity measurement.

---

**END OF GENERAL_WORKFLOW.md TEMPLATE (v1.0)**

*"True efficiency is not about doing things faster, but about doing the right things with the right strategy."*