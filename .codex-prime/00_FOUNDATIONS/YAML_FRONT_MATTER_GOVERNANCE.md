---
title: "Governança e Implementação de YAML Front Matter"
doc_id: "YAML-FRONT-MATTER-GOVERNANCE"
version: "1.0"
last_updated: "2025-07-23 20:52:12"
timezone: "America/Sao_Paulo"
status: "Ativo"
owner: "@ArquitetoDoCodex"
tags: ["yaml", "front-matter", "governança", "templates", "validação", "mcp"]
description: "Especificação completa para implementação, validação e governança de YAML Front Matter no Codex Prime Framework."
language: "pt-BR"
---

# **Governança e Implementação de YAML Front Matter**

## **1. Onde e Como Documentar a Estrutura**

### **1.1 Localização da Documentação**

**Estrutura Hierárquica de Documentação:**

```
/.codex-prime/
├── 01_TEMPLATES/
│   ├── YAML_SCHEMAS/
│   │   ├── base_document.yaml          # Schema base obrigatório
│   │   ├── blueprint_document.yaml     # Schema para blueprints
│   │   ├── report_document.yaml        # Schema para relatórios
│   │   ├── agent_profile.yaml          # Schema para perfis de agentes
│   │   └── research_document.yaml      # Schema para pesquisas
│   ├── DOCUMENT_TEMPLATES/
│   │   ├── template_blueprint.md
│   │   ├── template_report.md
│   │   ├── template_agent_profile.md
│   │   └── template_research.md
│   └── VALIDATION_RULES/
│       ├── yaml_validator.py           # Script de validação
│       ├── pre_commit_hooks.py         # Hooks para Git
│       └── validation_config.json      # Configurações de validação
└── 00_FOUNDATIONS/
    ├── YAML_FRONT_MATTER_SPEC.md      # Especificação completa
    └── GOVERNANCE_RULES.md            # Regras de governança
```

### **1.2 Documentos Principais**

1. **`YAML_FRONT_MATTER_SPEC.md`**: Especificação técnica completa
2. **`GOVERNANCE_RULES.md`**: Regras de aplicação e exceções
3. **Schemas YAML**: Definições estruturais para validação
4. **Templates**: Modelos prontos para cada tipo de documento

## **2. Validação Automática da Estrutura YAML**

### **2.1 Estratégia de Validação Multi-Camada**

#### **Camada 1: Validação Sintática (YAML Parser)**
```python
# yaml_validator.py
import yaml
import jsonschema
from pathlib import Path
from typing import Dict, List, Optional

class YAMLFrontMatterValidator:
    def __init__(self, schema_dir: Path):
        self.schema_dir = schema_dir
        self.schemas = self._load_schemas()
    
    def validate_document(self, file_path: Path) -> Dict:
        """Valida YAML front matter de um documento"""
        content = file_path.read_text(encoding='utf-8')
        
        # Extrai YAML front matter
        yaml_content = self._extract_yaml_front_matter(content)
        
        # Determina tipo de documento
        doc_type = self._determine_document_type(file_path, yaml_content)
        
        # Valida contra schema apropriado
        return self._validate_against_schema(yaml_content, doc_type)
```

#### **Camada 2: Validação Semântica (Regras de Negócio)**
```python
class SemanticValidator:
    def validate_business_rules(self, yaml_data: Dict) -> List[str]:
        errors = []
        
        # Validação de timezone
        if yaml_data.get('timezone') != 'America/Sao_Paulo':
            errors.append("Timezone deve ser 'America/Sao_Paulo'")
        
        # Validação de versionamento semântico
        version = yaml_data.get('version', '')
        if not self._is_semantic_version(version):
            errors.append(f"Versão '{version}' não segue padrão semântico")
        
        # Validação de timestamp via time-mcp
        if not self._validate_timestamp_format(yaml_data.get('last_updated')):
            errors.append("Timestamp deve ser gerado via time-mcp")
        
        return errors
```

#### **Camada 3: Integração com Git (Pre-commit Hooks)**
```python
# pre_commit_hooks.py
def validate_yaml_on_commit():
    """Hook executado antes de cada commit"""
    modified_files = get_modified_markdown_files()
    
    for file_path in modified_files:
        validation_result = validator.validate_document(file_path)
        
        if not validation_result['valid']:
            print(f"❌ YAML Front Matter inválido em {file_path}")
            for error in validation_result['errors']:
                print(f"   • {error}")
            return False
    
    print("✅ Todos os YAML Front Matter válidos")
    return True
```

### **2.2 Ferramentas de Validação**

1. **VS Code Extension**: Validação em tempo real durante edição
2. **GitHub Actions**: Validação automática em PRs
3. **Pre-commit Hooks**: Validação local antes de commits
4. **CLI Tool**: Validação manual via linha de comando

## **3. Templates para Diferentes Tipos de Documentos**

### **3.1 Taxonomia de Documentos**

#### **Categoria: Documentos Estratégicos**
- **Blueprint**: Documentos de arquitetura e design
- **Research**: Pesquisas e análises
- **Report**: Relatórios e sínteses
- **Vision**: Documentos de visão e estratégia

#### **Categoria: Documentos Operacionais**
- **Agent Profile**: Perfis de agentes de IA
- **Process**: Documentação de processos
- **Guide**: Guias e tutoriais
- **Reference**: Documentação de referência

#### **Categoria: Documentos Técnicos**
- **API**: Documentação de APIs
- **Architecture**: Documentos arquiteturais
- **Specification**: Especificações técnicas
- **Changelog**: Registros de mudanças

### **3.2 Templates Específicos**

#### **Template: Blueprint**
```yaml
---
title: "[Blueprint] Título do Blueprint"
doc_id: "BLUEPRINT-IDENTIFICADOR-UNICO"
version: "1.0"
last_updated: "{{ timestamp_via_time_mcp }}"
timezone: "America/Sao_Paulo"
status: "Draft" # Draft, Review, Active, Deprecated
owner: "@AgenteName"
reviewer: "@CriticoDoCodex"
tags: ["blueprint", "arquitetura", "design"]
description: "Descrição concisa do blueprint"
language: "pt-BR"
# Campos específicos para blueprints
blueprint_type: "architectural" # architectural, process, technical
complexity: "medium" # low, medium, high
dependencies: ["DOC-ID-1", "DOC-ID-2"]
impact_level: "high" # low, medium, high
implementation_priority: "P1" # P0, P1, P2, P3
---
```

#### **Template: Agent Profile**
```yaml
---
title: "Perfil do Agente [Nome do Agente]"
doc_id: "AGENT-PROFILE-NOME-AGENTE"
version: "1.0"
last_updated: "{{ timestamp_via_time_mcp }}"
timezone: "America/Sao_Paulo"
status: "Active"
owner: "@ArquitetoDoCodex"
tags: ["agente", "perfil", "ia", "olympus"]
description: "Perfil completo do agente [Nome]"
language: "pt-BR"
# Campos específicos para agentes
agent_type: "operational" # constitutional, operational, specialized
guild: "Nome da Guilda"
capabilities: ["capacidade1", "capacidade2"]
mcp_tools_required: ["time-mcp", "GitHub"]
mcp_tools_optional: ["desktop-commander"]
interaction_level: "autonomous" # supervised, autonomous, collaborative
---
```

#### **Template: Research Document**
```yaml
---
title: "[Pesquisa] Título da Pesquisa"
doc_id: "RESEARCH-IDENTIFICADOR"
version: "1.0"
last_updated: "{{ timestamp_via_time_mcp }}"
timezone: "America/Sao_Paulo"
status: "Active"
owner: "@PesquisadorDoCodex"
reviewer: "@CriticoDoCodex"
tags: ["pesquisa", "análise", "estudo"]
description: "Descrição da pesquisa realizada"
language: "pt-BR"
# Campos específicos para pesquisas
research_type: "market" # market, technical, competitive, academic
methodology: "qualitative" # qualitative, quantitative, mixed
sources_count: 0
confidence_level: "high" # low, medium, high
validity_period: "6 months"
related_projects: ["projeto1", "projeto2"]
---
```

## **4. MCP para Preenchimento Automático**

### **4.1 Proposta: MCP `yaml-front-matter-generator`**

#### **Funcionalidades Principais**

```json
{
  "server_name": "yaml-front-matter-generator",
  "description": "Gerador automático de YAML Front Matter padronizado",
  "tools": [
    {
      "name": "generate_yaml_front_matter",
      "description": "Gera YAML front matter baseado no tipo de documento",
      "inputSchema": {
        "type": "object",
        "properties": {
          "document_type": {
            "type": "string",
            "enum": ["blueprint", "research", "report", "agent_profile", "guide", "reference"]
          },
          "title": {"type": "string"},
          "owner": {"type": "string"},
          "description": {"type": "string"},
          "tags": {"type": "array", "items": {"type": "string"}},
          "custom_fields": {"type": "object"}
        },
        "required": ["document_type", "title", "owner"]
      }
    },
    {
      "name": "update_yaml_timestamp",
      "description": "Atualiza timestamp de last_updated via time-mcp",
      "inputSchema": {
        "type": "object",
        "properties": {
          "file_path": {"type": "string"}
        },
        "required": ["file_path"]
      }
    },
    {
      "name": "validate_yaml_structure",
      "description": "Valida estrutura YAML contra schemas",
      "inputSchema": {
        "type": "object",
        "properties": {
          "file_path": {"type": "string"},
          "document_type": {"type": "string"}
        },
        "required": ["file_path"]
      }
    }
  ]
}
```

#### **Integração com time-mcp**

```python
class YAMLFrontMatterGenerator:
    def __init__(self, time_mcp_client, github_mcp_client):
        self.time_mcp = time_mcp_client
        self.github_mcp = github_mcp_client
    
    async def generate_yaml_front_matter(self, document_type: str, **kwargs):
        # Obtém timestamp atual via time-mcp
        current_time = await self.time_mcp.current_time(
            format="YYYY-MM-DD HH:mm:ss",
            timezone="America/Sao_Paulo"
        )
        
        # Gera doc_id único
        doc_id = self._generate_doc_id(document_type, kwargs.get('title'))
        
        # Carrega template apropriado
        template = self._load_template(document_type)
        
        # Preenche template com dados
        yaml_data = {
            'title': kwargs['title'],
            'doc_id': doc_id,
            'version': '1.0',
            'last_updated': current_time,
            'timezone': 'America/Sao_Paulo',
            'status': 'Draft',
            'owner': kwargs['owner'],
            'tags': kwargs.get('tags', []),
            'description': kwargs.get('description', ''),
            'language': 'pt-BR',
            **kwargs.get('custom_fields', {})
        }
        
        return self._format_yaml_output(yaml_data)
```

### **4.2 Workflow de Uso**

1. **Criação de Documento**:
   ```bash
   # Via MCP
   yaml-generator generate --type blueprint --title "Nova Arquitetura" --owner "@ArquitetoDoCodex"
   ```

2. **Atualização Automática**:
   ```bash
   # Atualiza timestamp ao salvar
   yaml-generator update-timestamp --file documento.md
   ```

3. **Validação Contínua**:
   ```bash
   # Valida estrutura
   yaml-generator validate --file documento.md
   ```

## **5. Implementação e Roadmap**

### **5.1 Fase 1: Fundação (Semana 1-2)**
- [ ] Criar estrutura de diretórios
- [ ] Definir schemas YAML base
- [ ] Implementar validador básico
- [ ] Criar templates principais

### **5.2 Fase 2: Automação (Semana 3-4)**
- [ ] Desenvolver MCP yaml-front-matter-generator
- [ ] Integrar com time-mcp
- [ ] Implementar pre-commit hooks
- [ ] Criar VS Code extension

### **5.3 Fase 3: Governança (Semana 5-6)**
- [ ] Implementar GitHub Actions
- [ ] Criar dashboard de métricas
- [ ] Documentar processos
- [ ] Treinar agentes

### **5.4 Métricas de Sucesso**
- **Cobertura**: 100% dos documentos com YAML válido
- **Consistência**: 0 erros de validação em PRs
- **Automação**: 90% dos YAML gerados automaticamente
- **Adoção**: Todos os agentes utilizando templates

---

**Próximos Passos Imediatos:**
1. Aprovar estrutura proposta
2. Criar diretórios e schemas base
3. Implementar validador MVP
4. Testar com documentos existentes