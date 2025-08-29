# Eclipse Website Design System

## Design Tokens

### Colors

#### Light Theme
```css
--color-primary: #2B1B17;
--color-secondary: #8B4513;
--color-accent: #F4A460;
--color-background: #FFFEF7;
--color-surface: #FFFFFF;
--color-text: #2B1B17;
--color-text-secondary: #6B5B73;
--color-border: #E5E7EB;
```

#### Dark Theme
```css
--color-primary: #F4A460;
--color-secondary: #CD853F;
--color-accent: #FFD700;
--color-background: #0A0A0A;
--color-surface: #1A1A1A;
--color-text: #F4A460;
--color-text-secondary: #CD853F;
--color-border: #2A2A2A;
```

#### Purple Eclipse Theme
```css
--color-primary: #6A0DAD;
--color-secondary: #8A2BE2;
--color-accent: #DA70D6;
--color-background: #0D0015;
--color-surface: #1A0B2E;
--color-text: #E6E6FA;
--color-text-secondary: #D8BFD8;
--color-border: #483D8B;
```

### Typography

```css
--font-primary: 'Inter', system-ui, -apple-system, sans-serif;
--font-mono: 'JetBrains Mono', 'Fira Code', monospace;

--text-xs: 0.75rem;
--text-sm: 0.875rem;
--text-base: 1rem;
--text-lg: 1.125rem;
--text-xl: 1.25rem;
--text-2xl: 1.5rem;
--text-3xl: 1.875rem;
--text-4xl: 2.25rem;
```

### Spacing

```css
--space-1: 0.25rem;
--space-2: 0.5rem;
--space-3: 0.75rem;
--space-4: 1rem;
--space-6: 1.5rem;
--space-8: 2rem;
--space-12: 3rem;
--space-16: 4rem;
--space-24: 6rem;
```

### Layout

```css
--max-width: 80rem;
--header-height: 4rem;
--sidebar-width: 20rem;
--border-radius: 0.5rem;
--transition: all 0.2s ease;
```

## Component Architecture

### Header
- Desktop: Logo left, navigation items in flex grid on right
- Mobile: Logo left, hamburger button right
- Max width: 80rem
- Height: 4rem

### Mobile Sidebar
- Hamburger menu trigger
- Half-screen overlay (top to middle)
- Simple navigation list
- Smooth slide animation

### Main Content
- Max width: 80rem
- Responsive padding
- Centered layout

## Page Structure

### Landing Page
- Hero section with eclipse imagery
- What are eclipses section
- Upcoming eclipses
- Eclipse safety information

### Additional Pages
- `/types` - Types of eclipses (solar, lunar, etc.)
- `/safety` - Eclipse viewing safety
- `/upcoming` - Upcoming eclipse events
- `/gallery` - Eclipse photography gallery
- `/science` - The science behind eclipses

## Co-located Styles

All styles will be co-located within Astro components using `<style>` tags with CSS custom properties for theming. Each component will include:

```astro
<style>
  .component {
    /* Base styles using design tokens */
    color: var(--color-text);
    background: var(--color-surface);
  }
</style>
```

## Theme Implementation

Themes will be implemented using CSS custom properties that can be toggled via JavaScript:

```css
:root[data-theme="light"] { /* light theme tokens */ }
:root[data-theme="dark"] { /* dark theme tokens */ }
:root[data-theme="purple"] { /* purple theme tokens */ }
```