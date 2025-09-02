---
title: "Template: Style Guide - Guias de Estilo e Padrões"
doc_id: "CODEX-PRIME-TECNOLOGIA-STYLE-GUIDE-V1.0"
version: "1.0"
migrated_at: "2025-08-19 22:10:06"
timezone: "America/Sao_Paulo"
status: "Template"
owner: "@ArquitetoDoCodex"
tags: [template, codex-prime, v1.0, tecnologia, style-guide]
description: "Template migrado do .codex para .codex-prime na versao 1.0"
source_path: "\03_Tecnologia_Engineering\pt-br\02_PADROES_E_BOAS_PRATICAS\01_STYLE_GUIDE_GUIAS_ESTILO_PADROES.md"
---

# Style Guide - [PROJECT_NAME]

**Versão:** [VERSION]
**Data de Criação:** [CREATION_DATE]
**Data de Última Atualização:** [LAST_UPDATE_DATE]
**Autor:** [AUTHOR]
**Baseado em:** [REFERENCE_DOCUMENTS]
**Responsável pela Evolução:** [RESPONSIBLE_TEAM]

## 🎯 Visão Geral

### Objetivo
[STYLE_GUIDE_OBJECTIVE_DESCRIPTION]

### Princípios de Design
- **[PRINCIPLE_1]:** [PRINCIPLE_1_DESCRIPTION]
- **[PRINCIPLE_2]:** [PRINCIPLE_2_DESCRIPTION]
- **[PRINCIPLE_3]:** [PRINCIPLE_3_DESCRIPTION]
- **[PRINCIPLE_4]:** [PRINCIPLE_4_DESCRIPTION]
- **[PRINCIPLE_5]:** [PRINCIPLE_5_DESCRIPTION]

---

## 🎨 Identidade Visual

### Paleta de Cores

#### Cores Primárias
```css
/* [PRIMARY_COLORS_DESCRIPTION] */
--primary-color-1: #[HEX_COLOR_1]; /* [COLOR_1_DESCRIPTION] */
--primary-color-2: #[HEX_COLOR_2]; /* [COLOR_2_DESCRIPTION] */
--primary-color-3: #[HEX_COLOR_3]; /* [COLOR_3_DESCRIPTION] */
```

#### Cores Secundárias
```css
/* [SECONDARY_COLORS_DESCRIPTION] */
--secondary-color-1: #[HEX_COLOR_1]; /* [COLOR_1_DESCRIPTION] */
--secondary-color-2: #[HEX_COLOR_2]; /* [COLOR_2_DESCRIPTION] */
--secondary-color-3: #[HEX_COLOR_3]; /* [COLOR_3_DESCRIPTION] */
```

#### Cores de Sistema
```css
/* [SYSTEM_COLORS_DESCRIPTION] */
--success: #[HEX_COLOR]; /* [SUCCESS_COLOR_DESCRIPTION] */
--warning: #[HEX_COLOR]; /* [WARNING_COLOR_DESCRIPTION] */
--error: #[HEX_COLOR]; /* [ERROR_COLOR_DESCRIPTION] */
--info: #[HEX_COLOR]; /* [INFO_COLOR_DESCRIPTION] */
```

#### Cores Neutras
```css
/* [NEUTRAL_COLORS_DESCRIPTION] */
--neutral-white: #[HEX_COLOR]; /* [WHITE_DESCRIPTION] */
--neutral-light: #[HEX_COLOR]; /* [LIGHT_DESCRIPTION] */
--neutral-medium: #[HEX_COLOR]; /* [MEDIUM_DESCRIPTION] */
--neutral-dark: #[HEX_COLOR]; /* [DARK_DESCRIPTION] */
--neutral-black: #[HEX_COLOR]; /* [BLACK_DESCRIPTION] */
```

### Tipografia

#### Fontes Principais
```css
/* [PRIMARY_FONT_DESCRIPTION] */
--font-primary: '[FONT_NAME]', [FALLBACK_FONTS];
--font-secondary: '[FONT_NAME]', [FALLBACK_FONTS];
--font-monospace: '[FONT_NAME]', [FALLBACK_FONTS];
```

#### Escalas Tipográficas
```css
/* [TYPOGRAPHY_SCALE_DESCRIPTION] */
--text-xs: [SIZE]rem; /* [SIZE_DESCRIPTION] */
--text-sm: [SIZE]rem; /* [SIZE_DESCRIPTION] */
--text-base: [SIZE]rem; /* [SIZE_DESCRIPTION] */
--text-lg: [SIZE]rem; /* [SIZE_DESCRIPTION] */
--text-xl: [SIZE]rem; /* [SIZE_DESCRIPTION] */
--text-2xl: [SIZE]rem; /* [SIZE_DESCRIPTION] */
--text-3xl: [SIZE]rem; /* [SIZE_DESCRIPTION] */
--text-4xl: [SIZE]rem; /* [SIZE_DESCRIPTION] */
```

#### Pesos de Fonte
```css
/* [FONT_WEIGHTS_DESCRIPTION] */
--font-light: [WEIGHT];
--font-normal: [WEIGHT];
--font-medium: [WEIGHT];
--font-semibold: [WEIGHT];
--font-bold: [WEIGHT];
```

### Espaçamento

#### Sistema de Espaçamento
```css
/* [SPACING_SYSTEM_DESCRIPTION] */
--space-xs: [SIZE]rem; /* [SIZE_DESCRIPTION] */
--space-sm: [SIZE]rem; /* [SIZE_DESCRIPTION] */
--space-md: [SIZE]rem; /* [SIZE_DESCRIPTION] */
--space-lg: [SIZE]rem; /* [SIZE_DESCRIPTION] */
--space-xl: [SIZE]rem; /* [SIZE_DESCRIPTION] */
--space-2xl: [SIZE]rem; /* [SIZE_DESCRIPTION] */
--space-3xl: [SIZE]rem; /* [SIZE_DESCRIPTION] */
```

### Bordas e Raios

#### Raios de Borda
```css
/* [BORDER_RADIUS_DESCRIPTION] */
--radius-none: 0;
--radius-sm: [SIZE]px;
--radius-md: [SIZE]px;
--radius-lg: [SIZE]px;
--radius-xl: [SIZE]px;
--radius-full: 9999px;
```

#### Larguras de Borda
```css
/* [BORDER_WIDTH_DESCRIPTION] */
--border-thin: [SIZE]px;
--border-medium: [SIZE]px;
--border-thick: [SIZE]px;
```

### Sombras

#### Sistema de Sombras
```css
/* [SHADOW_SYSTEM_DESCRIPTION] */
--shadow-sm: [SHADOW_VALUES];
--shadow-md: [SHADOW_VALUES];
--shadow-lg: [SHADOW_VALUES];
--shadow-xl: [SHADOW_VALUES];
--shadow-2xl: [SHADOW_VALUES];
```

---

## 🧩 Componentes de Interface

### Botões

#### Botão Primário
```css
.btn-primary {
  background-color: var(--primary-color-1);
  color: var(--neutral-white);
  padding: var(--space-sm) var(--space-md);
  border-radius: var(--radius-md);
  font-weight: var(--font-medium);
  /* [ADDITIONAL_STYLES] */
}

.btn-primary:hover {
  /* [HOVER_STYLES] */
}

.btn-primary:focus {
  /* [FOCUS_STYLES] */
}

.btn-primary:disabled {
  /* [DISABLED_STYLES] */
}
```

#### Botão Secundário
```css
.btn-secondary {
  background-color: transparent;
  color: var(--primary-color-1);
  border: var(--border-thin) solid var(--primary-color-1);
  padding: var(--space-sm) var(--space-md);
  border-radius: var(--radius-md);
  font-weight: var(--font-medium);
  /* [ADDITIONAL_STYLES] */
}

.btn-secondary:hover {
  /* [HOVER_STYLES] */
}
```

#### Botão Terciário
```css
.btn-tertiary {
  background-color: transparent;
  color: var(--primary-color-1);
  padding: var(--space-sm) var(--space-md);
  border-radius: var(--radius-md);
  font-weight: var(--font-medium);
  /* [ADDITIONAL_STYLES] */
}

.btn-tertiary:hover {
  /* [HOVER_STYLES] */
}
```

### Campos de Entrada

#### Input Text
```css
.input-text {
  border: var(--border-thin) solid var(--neutral-medium);
  border-radius: var(--radius-md);
  padding: var(--space-sm) var(--space-md);
  font-size: var(--text-base);
  background-color: var(--neutral-white);
  /* [ADDITIONAL_STYLES] */
}

.input-text:focus {
  /* [FOCUS_STYLES] */
}

.input-text:error {
  /* [ERROR_STYLES] */
}
```

#### Textarea
```css
.textarea {
  border: var(--border-thin) solid var(--neutral-medium);
  border-radius: var(--radius-md);
  padding: var(--space-sm) var(--space-md);
  font-size: var(--text-base);
  background-color: var(--neutral-white);
  resize: vertical;
  min-height: [MIN_HEIGHT]px;
  /* [ADDITIONAL_STYLES] */
}
```

#### Select
```css
.select {
  border: var(--border-thin) solid var(--neutral-medium);
  border-radius: var(--radius-md);
  padding: var(--space-sm) var(--space-md);
  font-size: var(--text-base);
  background-color: var(--neutral-white);
  /* [ADDITIONAL_STYLES] */
}
```

### Cards

#### Card Básico
```css
.card {
  background-color: var(--neutral-white);
  border-radius: var(--radius-lg);
  box-shadow: var(--shadow-md);
  padding: var(--space-lg);
  /* [ADDITIONAL_STYLES] */
}

.card-header {
  /* [HEADER_STYLES] */
}

.card-body {
  /* [BODY_STYLES] */
}

.card-footer {
  /* [FOOTER_STYLES] */
}
```

### Navegação

#### Menu Principal
```css
.nav-main {
  /* [MAIN_NAV_STYLES] */
}

.nav-item {
  /* [NAV_ITEM_STYLES] */
}

.nav-item.active {
  /* [ACTIVE_NAV_ITEM_STYLES] */
}

.nav-item:hover {
  /* [HOVER_NAV_ITEM_STYLES] */
}
```

#### Breadcrumb
```css
.breadcrumb {
  /* [BREADCRUMB_STYLES] */
}

.breadcrumb-item {
  /* [BREADCRUMB_ITEM_STYLES] */
}

.breadcrumb-separator {
  /* [SEPARATOR_STYLES] */
}
```

### Modais e Overlays

#### Modal
```css
.modal-overlay {
  /* [OVERLAY_STYLES] */
}

.modal-content {
  /* [MODAL_CONTENT_STYLES] */
}

.modal-header {
  /* [MODAL_HEADER_STYLES] */
}

.modal-body {
  /* [MODAL_BODY_STYLES] */
}

.modal-footer {
  /* [MODAL_FOOTER_STYLES] */
}
```

### Feedback e Estados

#### Alertas
```css
.alert {
  padding: var(--space-md);
  border-radius: var(--radius-md);
  /* [BASE_ALERT_STYLES] */
}

.alert-success {
  background-color: var(--success);
  /* [SUCCESS_ALERT_STYLES] */
}

.alert-warning {
  background-color: var(--warning);
  /* [WARNING_ALERT_STYLES] */
}

.alert-error {
  background-color: var(--error);
  /* [ERROR_ALERT_STYLES] */
}

.alert-info {
  background-color: var(--info);
  /* [INFO_ALERT_STYLES] */
}
```

#### Loading States
```css
.loading-spinner {
  /* [SPINNER_STYLES] */
}

.loading-skeleton {
  /* [SKELETON_STYLES] */
}
```

---

## 📱 Responsividade

### Breakpoints
```css
/* [BREAKPOINTS_DESCRIPTION] */
--breakpoint-xs: [SIZE]px; /* [XS_DESCRIPTION] */
--breakpoint-sm: [SIZE]px; /* [SM_DESCRIPTION] */
--breakpoint-md: [SIZE]px; /* [MD_DESCRIPTION] */
--breakpoint-lg: [SIZE]px; /* [LG_DESCRIPTION] */
--breakpoint-xl: [SIZE]px; /* [XL_DESCRIPTION] */
--breakpoint-2xl: [SIZE]px; /* [2XL_DESCRIPTION] */
```

### Media Queries
```css
/* [MEDIA_QUERIES_DESCRIPTION] */
@media (min-width: var(--breakpoint-sm)) {
  /* [SM_STYLES] */
}

@media (min-width: var(--breakpoint-md)) {
  /* [MD_STYLES] */
}

@media (min-width: var(--breakpoint-lg)) {
  /* [LG_STYLES] */
}

@media (min-width: var(--breakpoint-xl)) {
  /* [XL_STYLES] */
}
```

### Grid System
```css
.container {
  /* [CONTAINER_STYLES] */
}

.row {
  /* [ROW_STYLES] */
}

.col {
  /* [COLUMN_STYLES] */
}

.col-1 { /* [COL_1_STYLES] */ }
.col-2 { /* [COL_2_STYLES] */ }
.col-3 { /* [COL_3_STYLES] */ }
.col-4 { /* [COL_4_STYLES] */ }
.col-6 { /* [COL_6_STYLES] */ }
.col-8 { /* [COL_8_STYLES] */ }
.col-12 { /* [COL_12_STYLES] */ }
```

---

## ♿ Acessibilidade

### Diretrizes WCAG 2.1

#### Contraste de Cores
- **Nível AA:** Contraste mínimo de 4.5:1 para texto normal
- **Nível AA:** Contraste mínimo de 3:1 para texto grande
- **Nível AAA:** Contraste mínimo de 7:1 para texto normal

#### Navegação por Teclado
```css
/* [KEYBOARD_NAVIGATION_DESCRIPTION] */
:focus {
  outline: [OUTLINE_STYLES];
  outline-offset: [OFFSET]px;
}

.skip-link {
  /* [SKIP_LINK_STYLES] */
}
```

#### Estados de Foco
```css
.focus-visible {
  /* [FOCUS_VISIBLE_STYLES] */
}

.focus-within {
  /* [FOCUS_WITHIN_STYLES] */
}
```

#### Texto Alternativo
- Todas as imagens devem ter atributo `alt` descritivo
- Ícones decorativos devem ter `alt=""` ou `aria-hidden="true"`
- Ícones funcionais devem ter descrição adequada

#### ARIA Labels
```html
<!-- [ARIA_EXAMPLES] -->
<button aria-label="[BUTTON_DESCRIPTION]">[BUTTON_TEXT]</button>
<input aria-describedby="[DESCRIPTION_ID]" />
<div role="[ROLE]" aria-label="[LABEL]">[CONTENT]</div>
```

---

## 🎭 Animações e Transições

### Durações
```css
/* [ANIMATION_DURATIONS_DESCRIPTION] */
--duration-fast: [DURATION]ms;
--duration-normal: [DURATION]ms;
--duration-slow: [DURATION]ms;
```

### Easing Functions
```css
/* [EASING_FUNCTIONS_DESCRIPTION] */
--ease-in: [EASING_FUNCTION];
--ease-out: [EASING_FUNCTION];
--ease-in-out: [EASING_FUNCTION];
--ease-bounce: [EASING_FUNCTION];
```

### Transições Comuns
```css
.transition-default {
  transition: all var(--duration-normal) var(--ease-in-out);
}

.transition-colors {
  transition: color var(--duration-fast) var(--ease-in-out),
              background-color var(--duration-fast) var(--ease-in-out);
}

.transition-transform {
  transition: transform var(--duration-normal) var(--ease-in-out);
}
```

### Animações de Entrada
```css
@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}

@keyframes slideInUp {
  from {
    opacity: 0;
    transform: translateY([DISTANCE]px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes scaleIn {
  from {
    opacity: 0;
    transform: scale([SCALE]);
  }
  to {
    opacity: 1;
    transform: scale(1);
  }
}
```

---

## 📐 Layout e Estrutura

### Estrutura de Página
```html
<!DOCTYPE html>
<html lang="[LANGUAGE]">
<head>
  <!-- [HEAD_CONTENT] -->
</head>
<body>
  <header class="site-header">
    <!-- [HEADER_CONTENT] -->
  </header>
  
  <nav class="site-navigation">
    <!-- [NAVIGATION_CONTENT] -->
  </nav>
  
  <main class="site-main">
    <!-- [MAIN_CONTENT] -->
  </main>
  
  <aside class="site-sidebar">
    <!-- [SIDEBAR_CONTENT] -->
  </aside>
  
  <footer class="site-footer">
    <!-- [FOOTER_CONTENT] -->
  </footer>
</body>
</html>
```

### Layouts Comuns

#### Layout de Dashboard
```css
.dashboard-layout {
  /* [DASHBOARD_LAYOUT_STYLES] */
}

.dashboard-sidebar {
  /* [SIDEBAR_STYLES] */
}

.dashboard-content {
  /* [CONTENT_STYLES] */
}
```

#### Layout de Formulário
```css
.form-layout {
  /* [FORM_LAYOUT_STYLES] */
}

.form-section {
  /* [FORM_SECTION_STYLES] */
}

.form-group {
  /* [FORM_GROUP_STYLES] */
}
```

---

## 🎨 Iconografia

### Sistema de Ícones
- **Biblioteca:** [ICON_LIBRARY_NAME]
- **Tamanhos:** [ICON_SIZES]
- **Estilo:** [ICON_STYLE_DESCRIPTION]

### Ícones Comuns
```css
.icon {
  /* [BASE_ICON_STYLES] */
}

.icon-sm { /* [SMALL_ICON_STYLES] */ }
.icon-md { /* [MEDIUM_ICON_STYLES] */ }
.icon-lg { /* [LARGE_ICON_STYLES] */ }
.icon-xl { /* [EXTRA_LARGE_ICON_STYLES] */ }
```

### Ícones de Estado
```css
.icon-success { color: var(--success); }
.icon-warning { color: var(--warning); }
.icon-error { color: var(--error); }
.icon-info { color: var(--info); }
```

---

## 📝 Diretrizes de Conteúdo

### Tom de Voz
- **[TONE_ASPECT_1]:** [TONE_DESCRIPTION_1]
- **[TONE_ASPECT_2]:** [TONE_DESCRIPTION_2]
- **[TONE_ASPECT_3]:** [TONE_DESCRIPTION_3]

### Linguagem
- **[LANGUAGE_GUIDELINE_1]:** [GUIDELINE_DESCRIPTION_1]
- **[LANGUAGE_GUIDELINE_2]:** [GUIDELINE_DESCRIPTION_2]
- **[LANGUAGE_GUIDELINE_3]:** [GUIDELINE_DESCRIPTION_3]

### Mensagens de Sistema

#### Mensagens de Sucesso
- [SUCCESS_MESSAGE_EXAMPLE_1]
- [SUCCESS_MESSAGE_EXAMPLE_2]
- [SUCCESS_MESSAGE_EXAMPLE_3]

#### Mensagens de Erro
- [ERROR_MESSAGE_EXAMPLE_1]
- [ERROR_MESSAGE_EXAMPLE_2]
- [ERROR_MESSAGE_EXAMPLE_3]

#### Mensagens de Confirmação
- [CONFIRMATION_MESSAGE_EXAMPLE_1]
- [CONFIRMATION_MESSAGE_EXAMPLE_2]
- [CONFIRMATION_MESSAGE_EXAMPLE_3]

---

## 🔧 Implementação Técnica

### Estrutura CSS
```
styles/
├── base/
│   ├── reset.css
│   ├── typography.css
│   └── variables.css
├── components/
│   ├── buttons.css
│   ├── forms.css
│   ├── cards.css
│   └── navigation.css
├── layouts/
│   ├── grid.css
│   ├── dashboard.css
│   └── forms.css
├── utilities/
│   ├── spacing.css
│   ├── colors.css
│   └── typography.css
└── themes/
    ├── light.css
    └── dark.css
```

### Variáveis CSS Customizadas
```css
:root {
  /* [ROOT_VARIABLES] */
}

[data-theme="dark"] {
  /* [DARK_THEME_VARIABLES] */
}

[data-theme="light"] {
  /* [LIGHT_THEME_VARIABLES] */
}
```

### Metodologia CSS
- **Metodologia:** [CSS_METHODOLOGY] (BEM, SMACSS, etc.)
- **Convenções de Nomenclatura:** [NAMING_CONVENTIONS]
- **Organização:** [ORGANIZATION_APPROACH]

---

## 📋 Checklist de Implementação

### Design
- [ ] [DESIGN_CHECKLIST_ITEM_1]
- [ ] [DESIGN_CHECKLIST_ITEM_2]
- [ ] [DESIGN_CHECKLIST_ITEM_3]
- [ ] [DESIGN_CHECKLIST_ITEM_4]
- [ ] [DESIGN_CHECKLIST_ITEM_5]

### Desenvolvimento
- [ ] [DEVELOPMENT_CHECKLIST_ITEM_1]
- [ ] [DEVELOPMENT_CHECKLIST_ITEM_2]
- [ ] [DEVELOPMENT_CHECKLIST_ITEM_3]
- [ ] [DEVELOPMENT_CHECKLIST_ITEM_4]
- [ ] [DEVELOPMENT_CHECKLIST_ITEM_5]

### Acessibilidade
- [ ] [ACCESSIBILITY_CHECKLIST_ITEM_1]
- [ ] [ACCESSIBILITY_CHECKLIST_ITEM_2]
- [ ] [ACCESSIBILITY_CHECKLIST_ITEM_3]
- [ ] [ACCESSIBILITY_CHECKLIST_ITEM_4]
- [ ] [ACCESSIBILITY_CHECKLIST_ITEM_5]

### Performance
- [ ] [PERFORMANCE_CHECKLIST_ITEM_1]
- [ ] [PERFORMANCE_CHECKLIST_ITEM_2]
- [ ] [PERFORMANCE_CHECKLIST_ITEM_3]
- [ ] [PERFORMANCE_CHECKLIST_ITEM_4]
- [ ] [PERFORMANCE_CHECKLIST_ITEM_5]

---

## 📚 Recursos e Referências

### Ferramentas de Design
- [DESIGN_TOOL_1]: [TOOL_DESCRIPTION_1]
- [DESIGN_TOOL_2]: [TOOL_DESCRIPTION_2]
- [DESIGN_TOOL_3]: [TOOL_DESCRIPTION_3]

### Bibliotecas e Frameworks
- [LIBRARY_1]: [LIBRARY_DESCRIPTION_1]
- [LIBRARY_2]: [LIBRARY_DESCRIPTION_2]
- [LIBRARY_3]: [LIBRARY_DESCRIPTION_3]

### Documentação Externa
- [EXTERNAL_DOC_1]: [DOC_DESCRIPTION_1]
- [EXTERNAL_DOC_2]: [DOC_DESCRIPTION_2]
- [EXTERNAL_DOC_3]: [DOC_DESCRIPTION_3]

---

## 🔄 Versionamento e Evolução

### Controle de Versões
- **Versão Atual:** [CURRENT_VERSION]
- **Próxima Versão:** [NEXT_VERSION]
- **Responsável:** [RESPONSIBLE_PERSON]

### Histórico de Mudanças

#### [VERSION] - [DATE]
- [CHANGE_DESCRIPTION_1]
- [CHANGE_DESCRIPTION_2]
- [CHANGE_DESCRIPTION_3]

#### [PREVIOUS_VERSION] - [PREVIOUS_DATE]
- [PREVIOUS_CHANGE_1]
- [PREVIOUS_CHANGE_2]
- [PREVIOUS_CHANGE_3]

### Processo de Atualização
1. [UPDATE_STEP_1]
2. [UPDATE_STEP_2]
3. [UPDATE_STEP_3]
4. [UPDATE_STEP_4]
5. [UPDATE_STEP_5]

---

**Documento gerado pelo Codex Prime Framework v1.0**  
**Última atualização:** [LAST_UPDATE_TIMESTAMP]