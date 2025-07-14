
# 🏛️ Codex Prime Framework

> **A Constituição para Ecossistemas de Desenvolvimento Aumentado por IA**
> 
> _Um framework para criar, gerir e escalar conhecimento vivo e legível por máquina._

[![Status do Projeto](https://img.shields.io/badge/status-ativo-green)](https://github.com/) [![Versão](https://img.shields.io/badge/versão-1.0.0-blue)](./docs/CHANGELOG.md) [![Docs-as-Code](https://img.shields.io/badge/princípio-Docs--as--Code-blueviolet)](https://www.writethedocs.org/guide/docs-as-code/) [![Markdown](https://img.shields.io/badge/markdown-%E2%9C%93-brightgreen?logo=markdown)](https://www.markdownguide.org/) [![YAML](https://img.shields.io/badge/YAML-%E2%9C%93-important?logo=yaml)](https://yaml.org/) [![Mermaid](https://img.shields.io/badge/Mermaid-%E2%9C%93-ff2e93?logo=mermaid)](https://mermaid.js.org/) [![Licença](https://img.shields.io/badge/licença-pendente-lightgrey)](./LICENSE)

## 🏛️ O Que é o Codex Prime?

O **Codex Prime Framework** não é uma simples pasta de documentos. É um **ativo estratégico** e uma **metodologia** para a criação e gestão de conhecimento num ecossistema onde humanos e agentes de IA colaboram. Ele representa a fonte canónica da verdade, a "constituição" que define os padrões, os processos e a cultura de engenharia de todos os projetos nascidos sob a batuta do `Maestro.AI`.

A sua filosofia central é **"Docs-as-Code" (Documentação como Código)**. Tratamos o conhecimento com o mesmo rigor que o código-fonte: ele é versionado, testado, revisado e integrado em fluxos de trabalho automatizados.

## ✨ Princípios Fundamentais

O Codex rege-se por três princípios não-negociáveis:

1. **Fonte da Verdade Viva:** O conhecimento aqui não é um arquivo morto. É uma representação dinâmica e sempre atualizada do estado dos nossos projetos, decisões e processos.
    
2. **Dualidade Humano-Máquina:** Cada documento é projetado para ser perfeitamente legível por um **humano** e rigorosamente processável por uma **máquina**. A clareza narrativa anda de mãos dadas com a estrutura de metadados.
    
3. **Governança Explícita:** O caos é o inimigo da autonomia. O funcionamento do ecossistema é regido por regras claras, definidas no documento central [`CONSTITUICAO-PRINCIPIOS_FUNDAMENTAIS-v1.0.md`](./.codex/CONSTITUICAO-PRINCIPIOS_FUNDAMENTAIS-v1.0.md), que estabelece desde a nomenclatura de arquivos até o processo de tomada de decisões.
    

## 💡 Como Funciona: Um Ecossistema Evolutivo

O Codex Prime não é para ser usado diretamente, mas sim **instanciado**. Cada novo projeto (como o `Recoloca.AI`) recebe uma "cópia" do Codex, que serve como seu esqueleto de conhecimento.

O mais importante é que o Codex aprende. Este é o ciclo de vida do conhecimento:

```
graph TD
    A[Codex Prime Framework<br>(O Molde)] --> |1. Instanciação| B[Instância do Projeto<br>(e.g., Recoloca.AI Docs)];
    B --> |2. Desenvolvimento e Aprendizado| C{Agente de<br>Aprendizagem};
    C --> |3. Propõe Melhoria<br>Validada por Humano| D[Refinamento e Evolução];
    D --> A;

```

1. **Instanciação:** Um novo projeto é criado a partir da estrutura e dos templates do Codex.
    
2. **Aprendizado Local:** Durante o desenvolvimento do projeto, novas soluções, padrões e melhorias são criados.
    
3. **Promoção e Refinamento:** O `Agente de Aprendizagem` (orquestrado pelo `Maestro.AI`) identifica esses padrões de sucesso. Após validação humana, eles são abstraídos e incorporados de volta ao `Codex Prime Framework` original, tornando-o mais inteligente e robusto para o próximo projeto.
    

## 📦 Conteúdo do Framework

O Codex está organizado numa estrutura de pilares que representam os domínios de conhecimento de uma organização de tecnologia. A sua espinha dorsal é o diretório `.codex-prime/templates`.

### Estrutura de Pilares

- **`00_EMPRESA_COMPANY`**: Missão, visão, estrutura organizacional.
    
- **`01_PRODUTO_PRODUCT`**: Roadmaps, especificações de requisitos (ERS), histórias de utilizador.
    
- **`02_DESIGN_UX_UI`**: Guias de estilo, componentes de UI, pesquisas com utilizadores.
    
- **`03_TECNOLOGIA_ENGINEERING`**: Arquitetura (HLD, ADRs), guias de codificação, estratégias de teste.
    
- **`04_MARKETING_GROWTH`**: Estratégias de mercado, planos de lançamento.
    
- **`05_DADOS_DATA`**: Modelos de dados, dicionários, estratégias de MLOps.
    
- **`06_AGENTES_IA_AGENTS`**: Perfis, prompts e fluxos de orquestração dos nossos agentes de IA.
    

### Templates Essenciais

O diretório [`.codex-prime/templates`](./.codex-prime/templates/) é o coração do bootstrapping. Ele contém os modelos de documentos que os agentes usarão para criar conhecimento de forma padronizada, incluindo:

- `TEMPLATE_ADR.md`: Para registar Decisões Arquiteturais.
    
- `TEMPLATE_ERS.md`: Para especificações de requisitos funcionais.
    
- `TEMPLATE_HU_AC.md`: Para histórias de usuário e critérios de aceite.
    
- `TEMPLATE_GOVERNANCA_IA.md`: Para governança de sistemas de IA.
    

## 🚀 Como Usar este Framework

Para iniciar um novo projeto utilizando o Codex Prime:

1. **Clone este repositório:**
    
    ```
    # Não clone para usar diretamente, mas como fonte para o script
    git clone [URL_DO_CODEX_PRIME]
    ```
    
2. Execute o Script de Inicialização (Exemplo):
    
    Um script de inicialização será criado para automatizar este processo.
    
    ```
    python initialize_project.py --name "MeuNovoProjeto" --codex-path ./CodexPrimeFramework
    ```
    
3. **Comece a Documentar:** O script irá gerar a estrutura de pastas do seu novo projeto, preenchida com os templates do Codex. Comece por preencher os documentos mais importantes, como a especificação de requisitos e as primeiras decisões arquiteturais.
    

## 🤝 Como Contribuir para o Framework

A contribuição para o `Codex Prime` é de alto impacto, pois melhora a fundação de todos os projetos futuros. As contribuições devem focar em:

- **Melhorar Templates Existentes:** Refinar os modelos para serem mais claros ou mais úteis para os agentes.
    
- **Propor Novos Templates:** Criar novos padrões de documentos que se mostrem necessários.
    
- **Evoluir a `CONSTITUICAO-PRINCIPIOS_FUNDAMENTAIS-v1.0.md`:** Sugerir melhorias no processo de governança.
    

Toda contribuição deve ser proposta através de um **RFC (Request for Comments)**, seguindo o processo definido no nosso guia de contribuição.

## 📄 Licença

Distribuído sob a licença [Nome da Licença]. Veja `LICENSE.txt` para mais informações.

## 📞 Contato

Maestro (Desenvolvedor Principal): Bruno S. Rosa

LinkedIn: [/In/BrunoSRosa](https://linkedin.com/in/brunosrosa)