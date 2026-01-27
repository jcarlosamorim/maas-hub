# Atoms - MaaS Hub Design System

**Project:** MaaS Knowledge Hub
**Style:** Dark theme, app-like interface with sidebar

---

## 1. Typography Atoms

### Display Text

```css
.text-display {
  font-family: var(--font-display);
  font-size: var(--text-display);
  font-weight: var(--weight-bold);
  line-height: var(--leading-tight);
  letter-spacing: -0.02em;
  color: var(--text-primary);
}

/* Italic accent word (like "Consciencia" in reference) */
.text-display-accent {
  font-family: var(--font-accent);
  font-style: italic;
  font-weight: var(--weight-regular);
  color: var(--text-secondary);
}
```

### Headings

```css
.text-h1 {
  font-size: var(--text-h1);
  font-weight: var(--weight-bold);
  line-height: var(--leading-tight);
  color: var(--text-primary);
}

.text-h2 {
  font-size: var(--text-h2);
  font-weight: var(--weight-semibold);
  line-height: var(--leading-snug);
  color: var(--text-primary);
}

.text-h3 {
  font-size: var(--text-h3);
  font-weight: var(--weight-semibold);
  line-height: var(--leading-snug);
  color: var(--text-primary);
}

.text-h4 {
  font-size: var(--text-h4);
  font-weight: var(--weight-medium);
  line-height: var(--leading-normal);
  color: var(--text-primary);
}
```

### Body Text

```css
.text-lg {
  font-size: var(--text-lg);
  line-height: var(--leading-relaxed);
  color: var(--text-secondary);
}

.text-base {
  font-size: var(--text-base);
  line-height: var(--leading-normal);
  color: var(--text-secondary);
}

.text-sm {
  font-size: var(--text-sm);
  line-height: var(--leading-normal);
  color: var(--text-secondary);
}

.text-xs {
  font-size: var(--text-xs);
  line-height: var(--leading-normal);
  color: var(--text-muted);
}
```

### Special Text

```css
/* Overline (category labels) */
.text-overline {
  font-size: var(--text-xs);
  font-weight: var(--weight-semibold);
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: var(--text-muted);
}

/* Metric numbers */
.text-metric {
  font-family: var(--font-display);
  font-size: var(--text-metric);
  font-weight: var(--weight-bold);
  line-height: 1;
  color: var(--text-primary);
}

.text-metric-accent {
  font-family: var(--font-accent);
  font-style: italic;
  color: var(--text-secondary);
}

/* Mono/code text */
.text-mono {
  font-family: var(--font-mono);
  font-size: var(--text-sm);
  color: var(--accent-gold);
}
```

---

## 2. Buttons

### Primary Button

```css
.btn-primary {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: var(--space-2);

  padding: var(--space-3) var(--space-6);
  min-height: 44px;

  font-family: var(--font-body);
  font-size: var(--text-sm);
  font-weight: var(--weight-medium);

  color: var(--bg-app);
  background: var(--accent-gold);

  border: none;
  border-radius: var(--radius-lg);
  cursor: pointer;

  transition: all var(--duration-fast) var(--ease-out);
}

.btn-primary:hover {
  background: var(--accent-gold-light);
  box-shadow: var(--glow-gold);
}
```

### Secondary Button

```css
.btn-secondary {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: var(--space-2);

  padding: var(--space-3) var(--space-6);
  min-height: 44px;

  font-size: var(--text-sm);
  font-weight: var(--weight-medium);

  color: var(--text-primary);
  background: var(--bg-card);

  border: var(--border-thin) solid var(--border-default);
  border-radius: var(--radius-lg);
  cursor: pointer;

  transition: all var(--duration-fast) var(--ease-out);
}

.btn-secondary:hover {
  background: var(--bg-card-hover);
  border-color: var(--border-hover);
}
```

### Ghost Button

```css
.btn-ghost {
  display: inline-flex;
  align-items: center;
  gap: var(--space-2);

  padding: var(--space-2) var(--space-3);

  font-size: var(--text-sm);
  font-weight: var(--weight-medium);

  color: var(--text-secondary);
  background: transparent;
  border: none;
  cursor: pointer;

  transition: color var(--duration-fast) var(--ease-out);
}

.btn-ghost:hover {
  color: var(--text-primary);
}
```

### Icon Button

```css
.btn-icon {
  display: flex;
  align-items: center;
  justify-content: center;

  width: 40px;
  height: 40px;

  color: var(--text-muted);
  background: transparent;
  border: none;
  border-radius: var(--radius-md);
  cursor: pointer;

  transition: all var(--duration-fast) var(--ease-out);
}

.btn-icon:hover {
  color: var(--text-primary);
  background: var(--bg-card);
}
```

---

## 3. Icons

### Icon Sizes

```css
.icon-xs { width: 14px; height: 14px; }
.icon-sm { width: 18px; height: 18px; }
.icon-md { width: 24px; height: 24px; }
.icon-lg { width: 32px; height: 32px; }
.icon-xl { width: 48px; height: 48px; }
```

### Icon Container (for sidebar/collection icons)

```css
.icon-container {
  display: flex;
  align-items: center;
  justify-content: center;

  width: 48px;
  height: 48px;

  background: var(--bg-elevated);
  border-radius: var(--radius-lg);

  color: var(--text-muted);
}

.icon-container--gold {
  background: var(--accent-gold-muted);
  color: var(--accent-gold);
}

.icon-container--purple {
  background: var(--accent-purple-muted);
  color: var(--accent-purple);
}
```

---

## 4. Tags / Chips

### Category Tag

```css
.tag {
  display: inline-flex;
  align-items: center;
  gap: var(--space-1);

  padding: var(--tag-padding);

  font-size: var(--tag-font-size);
  font-weight: var(--weight-medium);
  text-transform: uppercase;
  letter-spacing: 0.05em;

  background: var(--bg-elevated);
  border-radius: var(--tag-radius);

  color: var(--text-muted);
}

/* Active/Selected state */
.tag--active {
  background: var(--text-primary);
  color: var(--bg-app);
}

/* Category-specific colors */
.tag--research { color: var(--cat-research); background: rgba(201, 169, 98, 0.15); }
.tag--methodology { color: var(--cat-methodology); background: rgba(155, 123, 255, 0.15); }
.tag--framework { color: var(--cat-framework); background: rgba(74, 222, 128, 0.15); }
.tag--script { color: var(--cat-script); background: rgba(96, 165, 250, 0.15); }
.tag--analysis { color: var(--cat-analysis); background: rgba(244, 114, 182, 0.15); }
.tag--manifesto { color: var(--cat-manifesto); background: rgba(251, 146, 60, 0.15); }
```

### Badge (count/status)

```css
.badge {
  display: inline-flex;
  align-items: center;
  justify-content: center;

  min-width: 20px;
  height: 20px;
  padding: 0 var(--space-2);

  font-size: 11px;
  font-weight: var(--weight-semibold);

  background: var(--accent-gold);
  color: var(--bg-app);
  border-radius: var(--radius-full);
}

.badge--muted {
  background: var(--bg-elevated);
  color: var(--text-muted);
}
```

---

## 5. Form Elements

### Input Field

```css
.input {
  width: 100%;
  height: var(--search-height);
  padding: var(--search-padding);

  font-family: var(--font-body);
  font-size: var(--text-sm);
  color: var(--text-primary);

  background: var(--bg-input);
  border: var(--border-thin) solid var(--border-subtle);
  border-radius: var(--search-radius);

  transition: all var(--duration-fast) var(--ease-out);
}

.input::placeholder {
  color: var(--text-muted);
}

.input:focus {
  outline: none;
  border-color: var(--accent-gold);
  box-shadow: 0 0 0 3px var(--accent-gold-muted);
}
```

### Search Input

```css
.search {
  position: relative;
}

.search-icon {
  position: absolute;
  left: var(--space-4);
  top: 50%;
  transform: translateY(-50%);
  color: var(--text-muted);
}

.search .input {
  padding-left: calc(var(--space-4) + 24px + var(--space-2));
}
```

---

## 6. Avatar

```css
.avatar {
  display: flex;
  align-items: center;
  justify-content: center;

  width: 40px;
  height: 40px;

  font-size: var(--text-sm);
  font-weight: var(--weight-semibold);

  background: var(--bg-elevated);
  border: var(--border-thin) solid var(--border-default);
  border-radius: var(--radius-full);

  color: var(--text-primary);
  overflow: hidden;
}

.avatar img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.avatar--sm { width: 32px; height: 32px; font-size: var(--text-xs); }
.avatar--lg { width: 48px; height: 48px; font-size: var(--text-base); }
```

---

## 7. Dividers

```css
.divider {
  width: 100%;
  height: 1px;
  background: var(--border-subtle);
}

.divider--vertical {
  width: 1px;
  height: 100%;
}

.divider--with-label {
  display: flex;
  align-items: center;
  gap: var(--space-4);
}

.divider--with-label::before,
.divider--with-label::after {
  content: '';
  flex: 1;
  height: 1px;
  background: var(--border-subtle);
}
```

---

## 8. Skeleton / Loading

```css
.skeleton {
  background: linear-gradient(
    90deg,
    var(--bg-card) 0%,
    var(--bg-elevated) 50%,
    var(--bg-card) 100%
  );
  background-size: 200% 100%;
  animation: skeleton-pulse 1.5s ease-in-out infinite;
  border-radius: var(--radius-md);
}

@keyframes skeleton-pulse {
  0% { background-position: 200% 0; }
  100% { background-position: -200% 0; }
}

.skeleton-text {
  height: 1em;
  width: 100%;
}

.skeleton-title {
  height: 1.5em;
  width: 60%;
}

.skeleton-avatar {
  width: 40px;
  height: 40px;
  border-radius: var(--radius-full);
}
```

---

## 9. Favorite/Bookmark Icon

```css
.favorite {
  display: flex;
  align-items: center;
  justify-content: center;

  width: 32px;
  height: 32px;

  color: var(--text-muted);
  background: transparent;
  border: none;
  cursor: pointer;

  transition: all var(--duration-fast) var(--ease-out);
}

.favorite:hover {
  color: var(--accent-gold);
}

.favorite--active {
  color: var(--accent-gold);
}

.favorite--active svg {
  fill: var(--accent-gold);
}
```

---

## 10. Progress Indicator

```css
.progress {
  width: 100%;
  height: 4px;
  background: var(--bg-elevated);
  border-radius: var(--radius-full);
  overflow: hidden;
}

.progress-bar {
  height: 100%;
  background: var(--accent-gold);
  border-radius: var(--radius-full);
  transition: width var(--duration-normal) var(--ease-out);
}
```

---

## 11. Tooltip

```css
.tooltip {
  position: relative;
}

.tooltip-content {
  position: absolute;
  bottom: calc(100% + 8px);
  left: 50%;
  transform: translateX(-50%);

  padding: var(--space-2) var(--space-3);

  font-size: var(--text-xs);
  white-space: nowrap;

  background: var(--bg-elevated);
  border: var(--border-thin) solid var(--border-default);
  border-radius: var(--radius-md);
  box-shadow: var(--shadow-lg);

  opacity: 0;
  visibility: hidden;
  transition: all var(--duration-fast) var(--ease-out);
}

.tooltip:hover .tooltip-content {
  opacity: 1;
  visibility: visible;
}
```

---

*Atoms v1.0 - MaaS Hub*
*Building blocks for the knowledge hub*
