# Design Tokens - MaaS Hub (Methodology As A System)

**Project:** MaaS Knowledge Hub
**Methodology:** Brad Frost Atomic Design
**Reference:** app.lendario.ai/livros (dark theme, cards, sidebar)

---

## 1. Color Palette

### Core Colors (Dark Theme)

```css
:root {
  /* Background Hierarchy */
  --bg-app: #0D0D0D;              /* App background - deepest */
  --bg-sidebar: #0F0F0F;          /* Sidebar background */
  --bg-main: #111111;             /* Main content area */
  --bg-card: #1A1A1A;             /* Card background */
  --bg-card-hover: #222222;       /* Card hover state */
  --bg-elevated: #252525;         /* Elevated surfaces */
  --bg-input: #1A1A1A;            /* Input fields */

  /* Border Colors */
  --border-subtle: #2A2A2A;       /* Subtle borders */
  --border-default: #333333;      /* Default borders */
  --border-hover: #444444;        /* Hover state borders */

  /* Text Hierarchy */
  --text-primary: #FFFFFF;        /* Primary text */
  --text-secondary: #B3B3B3;      /* Secondary text */
  --text-muted: #808080;          /* Muted text */
  --text-disabled: #4D4D4D;       /* Disabled text */

  /* Accent Colors */
  --accent-gold: #C9A962;         /* Primary accent - gold */
  --accent-gold-light: #E5D4A1;   /* Gold light */
  --accent-gold-muted: rgba(201, 169, 98, 0.2);

  --accent-purple: #9B7BFF;       /* Secondary accent - purple */
  --accent-purple-light: #B99FFF;
  --accent-purple-muted: rgba(155, 123, 255, 0.2);

  --accent-green: #4ADE80;        /* Success */
  --accent-red: #F87171;          /* Error */
  --accent-blue: #60A5FA;         /* Info */

  /* Category Colors (for tags) */
  --cat-research: #C9A962;        /* Pesquisa */
  --cat-methodology: #9B7BFF;     /* Metodologia */
  --cat-framework: #4ADE80;       /* Framework */
  --cat-script: #60A5FA;          /* Scripts */
  --cat-analysis: #F472B6;        /* Análise */
  --cat-manifesto: #FB923C;       /* Manifesto */
}
```

### Gradients

```css
:root {
  /* Card gradients */
  --gradient-card-gold: linear-gradient(135deg, #2A2318 0%, #1A1A1A 100%);
  --gradient-card-purple: linear-gradient(135deg, #1F1A2E 0%, #1A1A1A 100%);
  --gradient-card-neutral: linear-gradient(135deg, #1F1F1F 0%, #1A1A1A 100%);

  /* Hero/Featured gradient */
  --gradient-hero: linear-gradient(135deg, #1A1815 0%, #0D0D0D 100%);

  /* Overlay */
  --overlay-dark: rgba(0, 0, 0, 0.6);
  --overlay-light: rgba(0, 0, 0, 0.3);
}
```

---

## 2. Typography

### Font Stack

```css
:root {
  /* Primary - Clean sans-serif */
  --font-display: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  --font-body: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  --font-mono: 'JetBrains Mono', 'Fira Code', 'Consolas', monospace;

  /* Accent - For italic emphasis */
  --font-accent: 'Playfair Display', Georgia, serif;
}
```

### Type Scale

```css
:root {
  /* Display */
  --text-display: clamp(2.5rem, 5vw, 4rem);     /* Hero headlines */

  /* Headings */
  --text-h1: clamp(2rem, 4vw, 3rem);            /* Page titles */
  --text-h2: clamp(1.5rem, 3vw, 2rem);          /* Section titles */
  --text-h3: clamp(1.25rem, 2vw, 1.5rem);       /* Card titles */
  --text-h4: 1.125rem;                           /* Subsection titles */

  /* Body */
  --text-lg: 1.125rem;                           /* Lead text */
  --text-base: 1rem;                             /* Body */
  --text-sm: 0.875rem;                           /* Small body */
  --text-xs: 0.75rem;                            /* Captions */

  /* Special */
  --text-metric: clamp(3rem, 6vw, 5rem);        /* Big numbers */
}
```

### Font Weights

```css
:root {
  --weight-regular: 400;
  --weight-medium: 500;
  --weight-semibold: 600;
  --weight-bold: 700;
}
```

### Line Heights

```css
:root {
  --leading-tight: 1.15;
  --leading-snug: 1.3;
  --leading-normal: 1.5;
  --leading-relaxed: 1.7;
}
```

---

## 3. Spacing System (4px base)

```css
:root {
  --space-0: 0;
  --space-1: 0.25rem;    /* 4px */
  --space-2: 0.5rem;     /* 8px */
  --space-3: 0.75rem;    /* 12px */
  --space-4: 1rem;       /* 16px */
  --space-5: 1.25rem;    /* 20px */
  --space-6: 1.5rem;     /* 24px */
  --space-8: 2rem;       /* 32px */
  --space-10: 2.5rem;    /* 40px */
  --space-12: 3rem;      /* 48px */
  --space-16: 4rem;      /* 64px */
  --space-20: 5rem;      /* 80px */
  --space-24: 6rem;      /* 96px */
}
```

---

## 4. Layout

### Sidebar

```css
:root {
  --sidebar-width: 260px;
  --sidebar-width-collapsed: 72px;
  --sidebar-padding: var(--space-4);
}
```

### Content Area

```css
:root {
  --content-padding: var(--space-8);
  --content-max-width: 1400px;
  --content-width-narrow: 800px;
}
```

### Grid

```css
:root {
  --grid-gap: var(--space-6);
  --grid-gap-sm: var(--space-4);

  /* Card grid columns */
  --grid-cols-cards: repeat(auto-fill, minmax(280px, 1fr));
  --grid-cols-collections: repeat(auto-fill, minmax(320px, 1fr));
}
```

---

## 5. Borders & Radius

```css
:root {
  /* Radius */
  --radius-xs: 4px;
  --radius-sm: 6px;
  --radius-md: 8px;
  --radius-lg: 12px;
  --radius-xl: 16px;
  --radius-2xl: 24px;
  --radius-full: 9999px;

  /* Border widths */
  --border-thin: 1px;
  --border-medium: 2px;
}
```

---

## 6. Shadows

```css
:root {
  /* Elevation */
  --shadow-sm: 0 1px 2px rgba(0, 0, 0, 0.3);
  --shadow-md: 0 4px 8px rgba(0, 0, 0, 0.3);
  --shadow-lg: 0 8px 24px rgba(0, 0, 0, 0.4);
  --shadow-xl: 0 16px 48px rgba(0, 0, 0, 0.5);

  /* Glow effects */
  --glow-gold: 0 0 20px rgba(201, 169, 98, 0.2);
  --glow-purple: 0 0 20px rgba(155, 123, 255, 0.2);

  /* Card shadows */
  --shadow-card: 0 2px 8px rgba(0, 0, 0, 0.2);
  --shadow-card-hover: 0 8px 24px rgba(0, 0, 0, 0.3);
}
```

---

## 7. Motion & Animation

```css
:root {
  /* Duration */
  --duration-instant: 0ms;
  --duration-fast: 150ms;
  --duration-normal: 250ms;
  --duration-slow: 400ms;

  /* Easing */
  --ease-default: cubic-bezier(0.4, 0, 0.2, 1);
  --ease-in: cubic-bezier(0.4, 0, 1, 1);
  --ease-out: cubic-bezier(0, 0, 0.2, 1);
  --ease-bounce: cubic-bezier(0.34, 1.56, 0.64, 1);
}
```

### Keyframes

```css
@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}

@keyframes slideInLeft {
  from {
    opacity: 0;
    transform: translateX(-20px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes slideInUp {
  from {
    opacity: 0;
    transform: translateY(10px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes pulse {
  0%, 100% { opacity: 1; }
  50% { opacity: 0.5; }
}
```

---

## 8. Z-Index Scale

```css
:root {
  --z-base: 0;
  --z-sidebar: 100;
  --z-sticky: 200;
  --z-dropdown: 300;
  --z-modal-backdrop: 400;
  --z-modal: 500;
  --z-popover: 600;
  --z-toast: 700;
  --z-tooltip: 800;
}
```

---

## 9. Breakpoints

```css
/* Mobile-first approach */
--bp-sm: 640px;    /* Large phones */
--bp-md: 768px;    /* Tablets */
--bp-lg: 1024px;   /* Laptops */
--bp-xl: 1280px;   /* Desktops */
--bp-2xl: 1536px;  /* Large screens */
```

---

## 10. Component-Specific Tokens

### Sidebar

```css
:root {
  --sidebar-item-height: 40px;
  --sidebar-item-padding: var(--space-3) var(--space-4);
  --sidebar-item-radius: var(--radius-md);
  --sidebar-item-gap: var(--space-1);
  --sidebar-section-gap: var(--space-6);
}
```

### Cards

```css
:root {
  --card-padding: var(--space-6);
  --card-radius: var(--radius-xl);
  --card-border: var(--border-thin) solid var(--border-subtle);
  --card-cover-height: 180px;
  --card-cover-radius: var(--radius-lg);
}
```

### Tags/Chips

```css
:root {
  --tag-padding: var(--space-2) var(--space-4);
  --tag-radius: var(--radius-full);
  --tag-font-size: var(--text-xs);
}
```

### Search

```css
:root {
  --search-height: 44px;
  --search-radius: var(--radius-lg);
  --search-padding: var(--space-3) var(--space-4);
}
```

---

## 11. Content Categories

| Category | Color Token | Icon |
|----------|-------------|------|
| Pesquisa | `--cat-research` | 🔍 |
| Metodologia | `--cat-methodology` | 📐 |
| Framework | `--cat-framework` | 🧩 |
| Script | `--cat-script` | 📝 |
| Análise | `--cat-analysis` | 📊 |
| Manifesto | `--cat-manifesto` | 📜 |

---

*Design Tokens v1.0 - MaaS Hub*
*Brad Frost Atomic Design*
