# System Patterns: Eclipse SEO Architecture

## Component Architecture

### Layout System
- **Single Layout**: `src/layouts/Layout.astro` serves as base template
- **Slot Pattern**: Content pages use layout slot for main content insertion
- **Props Interface**: TypeScript props for title and optional description

### Navigation Pattern
- **Dual Navigation**: Desktop horizontal nav + mobile sidebar overlay
- **Responsive Toggle**: CSS media queries hide/show navigation types
- **JavaScript Enhancement**: Mobile menu toggle with click-outside closing

### Page Structure Pattern
```
src/pages/[name].astro
├── Frontmatter (imports Layout)
├── Content sections
└── Co-located styles
```

## Styling Architecture

### CSS Custom Properties System
- **Theme Variables**: Defined at `:root` level with `data-theme` attribute switching
- **Design Tokens**: Centralized spacing, typography, and color variables
- **Co-location**: Component styles within `<style>` tags in each `.astro` file

### Theme Implementation
```css
:root[data-theme="light"] { /* light tokens */ }
:root[data-theme="dark"] { /* dark tokens */ }
:root[data-theme="purple"] { /* purple eclipse tokens */ }
```

### Responsive Design Pattern
- **Mobile-First**: Base styles for mobile, `@media (min-width: 768px)` for desktop
- **Grid Layouts**: CSS Grid for hero sections and feature cards
- **Flexible Components**: `auto-fit` and `minmax()` for responsive grids

## Content Organization
- **Semantic HTML**: Proper heading hierarchy and landmark elements
- **SEO Structure**: Meta descriptions and titles passed through layout props
- **Visual Hierarchy**: Consistent typography scale and spacing system

## Animation Patterns
- **CSS Animations**: Keyframe animations for eclipse visual effect
- **Transitions**: Consistent timing with `--transition` custom property
- **Hover Effects**: Subtle transforms and shadow changes

## JavaScript Patterns
- **Progressive Enhancement**: Basic functionality without JS, enhanced with JS
- **Event Delegation**: Minimal DOM manipulation for mobile menu
- **Vanilla JS**: No framework dependencies for simple interactions