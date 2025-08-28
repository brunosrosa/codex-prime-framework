---
title: "Template: 01_STYLE_GUIDE_STANDARDS"
doc_id: "CODEX-PRIME-ENGINEERING-01-STYLE-GUIDE-STANDARDS-V1.0"
version: "1.0"
migrated_at: "2025-08-19 22:10:06"
timezone: "America/Sao_Paulo"
status: "Template"
owner: "@ArquitetoDoCodex"
tags: [template, codex-prime, v1.0, engineering, style-guide]
description: "Template migrated from .codex to .codex-prime in version 1.0"
source_path: "\03_Tecnologia_Engineering\en-us\02_STANDARDS_AND_BEST_PRACTICES\01_STYLE_GUIDE_STANDARDS.md"
---

# STYLE GUIDE - [PROJECT_NAME]

**Version:** [VERSION_NUMBER]
**Creation Date:** [CREATION_DATE]
**Last Updated:** [LAST_UPDATE_DATE]
**Author:** [AUTHOR_NAME]
**Based on:** [REFERENCE_DOCUMENTS]
**Evolution Responsible:** [RESPONSIBLE_PERSON]

## 🎯 OVERVIEW

### Objective
[STYLE_GUIDE_OBJECTIVE_DESCRIPTION]

### Design Principles
- **[PRINCIPLE_1]:** [PRINCIPLE_DESCRIPTION]
- **[PRINCIPLE_2]:** [PRINCIPLE_DESCRIPTION]
- **[PRINCIPLE_3]:** [PRINCIPLE_DESCRIPTION]
- **[PRINCIPLE_4]:** [PRINCIPLE_DESCRIPTION]
- **[PRINCIPLE_5]:** [PRINCIPLE_DESCRIPTION]

---

## 🎨 VISUAL IDENTITY

### Color Palette

#### Primary Colors
```css
/* Primary color definitions */
--primary-color: #[HEX]; /* [COLOR_DESCRIPTION] */
--primary-dark: #[HEX]; /* [COLOR_DESCRIPTION] */
--primary-light: #[HEX]; /* [COLOR_DESCRIPTION] */
```

#### Secondary Colors
```css
/* Secondary color definitions */
--secondary-color: #[HEX]; /* [COLOR_DESCRIPTION] */
--secondary-dark: #[HEX]; /* [COLOR_DESCRIPTION] */
--secondary-light: #[HEX]; /* [COLOR_DESCRIPTION] */
```

#### System Colors
```css
/* System feedback colors */
--success: #[HEX]; /* Success states and positive feedback */
--warning: #[HEX]; /* Warning states and attention */
--error: #[HEX]; /* Error states and validation */
--info: #[HEX]; /* Informational messages */
```

#### Neutral Colors
```css
/* Neutral color palette */
--neutral-100: #[HEX]; /* Lightest neutral */
--neutral-200: #[HEX];
--neutral-300: #[HEX];
--neutral-400: #[HEX];
--neutral-500: #[HEX]; /* Base neutral */
--neutral-600: #[HEX];
--neutral-700: #[HEX];
--neutral-800: #[HEX];
--neutral-900: #[HEX]; /* Darkest neutral */
```

### Typography

#### Primary Font
```css
font-family: '[PRIMARY_FONT]', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
```

#### Secondary Font
```css
font-family: '[SECONDARY_FONT]', Georgia, 'Times New Roman', serif;
```

#### Typography Scale
- **H1:** [SIZE]/[LINE_HEIGHT] - [USAGE_DESCRIPTION]
- **H2:** [SIZE]/[LINE_HEIGHT] - [USAGE_DESCRIPTION]
- **H3:** [SIZE]/[LINE_HEIGHT] - [USAGE_DESCRIPTION]
- **H4:** [SIZE]/[LINE_HEIGHT] - [USAGE_DESCRIPTION]
- **Body Large:** [SIZE]/[LINE_HEIGHT] - [USAGE_DESCRIPTION]
- **Body:** [SIZE]/[LINE_HEIGHT] - [USAGE_DESCRIPTION]
- **Body Small:** [SIZE]/[LINE_HEIGHT] - [USAGE_DESCRIPTION]
- **Caption:** [SIZE]/[LINE_HEIGHT] - [USAGE_DESCRIPTION]

#### Font Weights
- **Light:** 300
- **Regular:** 400
- **Medium:** 500
- **Semibold:** 600
- **Bold:** 700

### Iconography
- **Library:** [ICON_LIBRARY_NAME]
- **Style:** [OUTLINE/FILLED/MIXED]
- **Sizes:** [SIZE_LIST]
- **Usage Guidelines:** [USAGE_GUIDELINES]

### Logo and Branding
- **Versions:** [LOGO_VERSIONS]
- **Protection Area:** [PROTECTION_AREA_RULES]
- **Incorrect Usage:** [INCORRECT_USAGE_EXAMPLES]

---

## 🧩 INTERFACE COMPONENTS

### Buttons

#### Primary Buttons
- **Usage:** [PRIMARY_BUTTON_USAGE]
- **Style:** [STYLE_SPECIFICATIONS]
- **States:** Default, Hover, Active, Disabled, Loading

```css
.btn-primary {
  /* Primary button styles */
  background-color: var(--primary-color);
  color: var(--neutral-100);
  border: none;
  border-radius: [BORDER_RADIUS];
  padding: [PADDING_VALUES];
  font-size: [FONT_SIZE];
  font-weight: [FONT_WEIGHT];
  transition: all 0.2s ease;
}

.btn-primary:hover {
  background-color: var(--primary-dark);
  transform: translateY(-1px);
}

.btn-primary:disabled {
  background-color: var(--neutral-300);
  cursor: not-allowed;
}
```

#### Secondary Buttons
- **Usage:** [SECONDARY_BUTTON_USAGE]
- **Style:** [STYLE_SPECIFICATIONS]
- **States:** Default, Hover, Active, Disabled

```css
.btn-secondary {
  /* Secondary button styles */
  background-color: transparent;
  color: var(--primary-color);
  border: 1px solid var(--primary-color);
  border-radius: [BORDER_RADIUS];
  padding: [PADDING_VALUES];
  font-size: [FONT_SIZE];
  font-weight: [FONT_WEIGHT];
  transition: all 0.2s ease;
}
```

#### Tertiary Buttons
- **Usage:** [TERTIARY_BUTTON_USAGE]
- **Style:** [STYLE_SPECIFICATIONS]

### Form Elements

#### Input Fields
```css
.input-field {
  /* Input field styles */
  border: 1px solid var(--neutral-300);
  border-radius: [BORDER_RADIUS];
  padding: [PADDING_VALUES];
  font-size: [FONT_SIZE];
  transition: border-color 0.2s ease;
}

.input-field:focus {
  border-color: var(--primary-color);
  outline: none;
  box-shadow: 0 0 0 3px rgba([PRIMARY_COLOR_RGB], 0.1);
}

.input-field.error {
  border-color: var(--error);
}
```

#### Select Dropdowns
[SELECT_DROPDOWN_SPECIFICATIONS]

#### Checkboxes and Radio Buttons
[CHECKBOX_RADIO_SPECIFICATIONS]

### Navigation

#### Primary Navigation
[PRIMARY_NAVIGATION_SPECIFICATIONS]

#### Secondary Navigation
[SECONDARY_NAVIGATION_SPECIFICATIONS]

#### Breadcrumbs
[BREADCRUMB_SPECIFICATIONS]

### Cards and Containers

#### Card Component
```css
.card {
  /* Card component styles */
  background-color: var(--neutral-100);
  border: 1px solid var(--neutral-200);
  border-radius: [BORDER_RADIUS];
  padding: [PADDING_VALUES];
  box-shadow: [BOX_SHADOW_VALUES];
  transition: box-shadow 0.2s ease;
}

.card:hover {
  box-shadow: [HOVER_BOX_SHADOW_VALUES];
}
```

### Feedback Components

#### Alerts and Notifications
[ALERT_SPECIFICATIONS]

#### Loading States
[LOADING_STATE_SPECIFICATIONS]

#### Empty States
[EMPTY_STATE_SPECIFICATIONS]

---

## 📱 RESPONSIVE DESIGN

### Breakpoints
```css
/* Responsive breakpoints */
--breakpoint-xs: 320px;
--breakpoint-sm: 576px;
--breakpoint-md: 768px;
--breakpoint-lg: 992px;
--breakpoint-xl: 1200px;
--breakpoint-xxl: 1400px;
```

### Grid System
[GRID_SYSTEM_SPECIFICATIONS]

### Mobile-First Approach
[MOBILE_FIRST_GUIDELINES]

---

## ♿ ACCESSIBILITY

### WCAG Compliance
- **Level:** [WCAG_LEVEL]
- **Guidelines:** [ACCESSIBILITY_GUIDELINES]

### Color Contrast
- **Minimum Ratio:** [CONTRAST_RATIO]
- **Testing Tools:** [TESTING_TOOLS]

### Keyboard Navigation
[KEYBOARD_NAVIGATION_GUIDELINES]

### Screen Reader Support
[SCREEN_READER_GUIDELINES]

---

## 🎭 ANIMATION AND MOTION

### Animation Principles
- **[PRINCIPLE_1]:** [PRINCIPLE_DESCRIPTION]
- **[PRINCIPLE_2]:** [PRINCIPLE_DESCRIPTION]
- **[PRINCIPLE_3]:** [PRINCIPLE_DESCRIPTION]

### Timing Functions
```css
/* Animation timing functions */
--ease-in-out: cubic-bezier(0.4, 0, 0.2, 1);
--ease-out: cubic-bezier(0, 0, 0.2, 1);
--ease-in: cubic-bezier(0.4, 0, 1, 1);
```

### Duration Guidelines
- **Micro-interactions:** [DURATION]
- **Page transitions:** [DURATION]
- **Loading animations:** [DURATION]

---

## 📝 CONTENT GUIDELINES

### Voice and Tone
- **Voice:** [VOICE_DESCRIPTION]
- **Tone:** [TONE_DESCRIPTION]

### Writing Style
- **[STYLE_RULE_1]:** [RULE_DESCRIPTION]
- **[STYLE_RULE_2]:** [RULE_DESCRIPTION]
- **[STYLE_RULE_3]:** [RULE_DESCRIPTION]

### Microcopy Guidelines
[MICROCOPY_GUIDELINES]

---

## 🔧 IMPLEMENTATION

### CSS Architecture
[CSS_ARCHITECTURE_APPROACH]

### Component Library
[COMPONENT_LIBRARY_INFORMATION]

### Design Tokens
```css
/* Design tokens structure */
:root {
  /* Spacing tokens */
  --space-xs: [VALUE];
  --space-sm: [VALUE];
  --space-md: [VALUE];
  --space-lg: [VALUE];
  --space-xl: [VALUE];
  
  /* Border radius tokens */
  --radius-sm: [VALUE];
  --radius-md: [VALUE];
  --radius-lg: [VALUE];
  
  /* Shadow tokens */
  --shadow-sm: [VALUE];
  --shadow-md: [VALUE];
  --shadow-lg: [VALUE];
}
```

---

## 📋 QUALITY ASSURANCE

### Design Review Checklist
- [ ] [CHECKLIST_ITEM_1]
- [ ] [CHECKLIST_ITEM_2]
- [ ] [CHECKLIST_ITEM_3]
- [ ] [CHECKLIST_ITEM_4]
- [ ] [CHECKLIST_ITEM_5]

### Testing Guidelines
[TESTING_GUIDELINES]

### Browser Support
[BROWSER_SUPPORT_MATRIX]

---

## 📚 RESOURCES

### Design Assets
- [ASSET_1]: [LINK_OR_LOCATION]
- [ASSET_2]: [LINK_OR_LOCATION]
- [ASSET_3]: [LINK_OR_LOCATION]

### Tools and Plugins
- [TOOL_1]: [DESCRIPTION_AND_LINK]
- [TOOL_2]: [DESCRIPTION_AND_LINK]
- [TOOL_3]: [DESCRIPTION_AND_LINK]

### References
- [REFERENCE_1]
- [REFERENCE_2]
- [REFERENCE_3]

---

## 🔄 MAINTENANCE

### Update Schedule
[UPDATE_SCHEDULE_INFORMATION]

### Version Control
[VERSION_CONTROL_PROCESS]

### Feedback Process
[FEEDBACK_COLLECTION_PROCESS]

---

## 📖 CHANGELOG

### Version [VERSION_NUMBER] - [DATE]
- [CHANGE_1]
- [CHANGE_2]
- [CHANGE_3]

### Version [VERSION_NUMBER] - [DATE]
- [CHANGE_1]
- [CHANGE_2]
- [CHANGE_3]