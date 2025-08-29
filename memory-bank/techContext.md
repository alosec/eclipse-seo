# Technical Context: Eclipse SEO Implementation

## Core Technology Stack

### Framework
- **Astro v5.13.5**: Static site generator chosen for optimal SEO performance
- **TypeScript**: Built-in TypeScript support for type safety
- **Static Generation**: All pages pre-rendered for fast loading

### Development Setup
```bash
npm run dev      # Development server at localhost:4321
npm run build    # Production build to ./dist/
npm run preview  # Preview production build locally
```

### Project Structure
```
eclipse-seo/
├── src/
│   ├── layouts/Layout.astro    # Base layout template
│   └── pages/                  # Route-based pages
├── public/                     # Static assets
└── astro.config.mjs           # Astro configuration
```

## Styling Implementation
- **No CSS Framework**: Pure CSS with custom properties
- **Co-located Styles**: Component styles within `.astro` files
- **Design System**: CSS custom properties for tokens
- **Theme System**: Data attribute-based theme switching

## Build Configuration
- **Minimal Config**: Default Astro configuration in `astro.config.mjs`
- **TypeScript**: Configured via `tsconfig.json`
- **Static Output**: Generates static HTML/CSS/JS bundle

## Dependencies
- **Runtime**: Single dependency on Astro framework
- **No Client Libraries**: Vanilla JavaScript for interactions
- **No UI Framework**: Custom components built with Astro

## Performance Characteristics
- **Static Generation**: All content pre-rendered
- **Minimal JavaScript**: Only essential mobile menu functionality
- **CSS Optimization**: Scoped styles prevent bloat
- **Fast Loading**: Optimized for Core Web Vitals

## Development Constraints
- **SEO First**: All decisions prioritize search engine optimization
- **Static Only**: No server-side rendering or dynamic content
- **Minimal Dependencies**: Lean dependency tree for security and performance
- **Standards Compliant**: Semantic HTML and modern CSS practices