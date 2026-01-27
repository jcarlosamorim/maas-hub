# Molecules - MaaS Hub Design System

---

## 1. Sidebar Nav Item

```html
<a href="#" class="nav-item">
  <span class="nav-icon">📐</span>
  <span class="nav-label">Metodologia</span>
  <span class="badge">3</span>
</a>
```

```css
.nav-item {
  display: flex;
  align-items: center;
  gap: var(--space-3);
  padding: var(--sidebar-item-padding);
  border-radius: var(--sidebar-item-radius);
  color: var(--text-secondary);
  text-decoration: none;
  transition: all var(--duration-fast) var(--ease-out);
}

.nav-item:hover {
  background: var(--bg-card);
  color: var(--text-primary);
}

.nav-item--active {
  background: var(--bg-card);
  color: var(--text-primary);
}

.nav-item--active::before {
  content: '';
  position: absolute;
  left: 0;
  width: 3px;
  height: 24px;
  background: var(--accent-gold);
  border-radius: 0 2px 2px 0;
}

.nav-icon { font-size: 18px; }
.nav-label { flex: 1; font-size: var(--text-sm); font-weight: var(--weight-medium); }
```

---

## 2. Content Card

```html
<article class="content-card">
  <div class="card-cover" style="background: var(--gradient-card-gold)">
    <span class="card-icon">📐</span>
  </div>
  <div class="card-body">
    <span class="tag tag--methodology">Metodologia</span>
    <h3 class="card-title">Arquiteto de Conhecimento</h3>
    <p class="card-desc">Mastermind & Mentoria High Ticket para Experts</p>
  </div>
  <button class="favorite"><svg>...</svg></button>
</article>
```

```css
.content-card {
  position: relative;
  display: flex;
  flex-direction: column;
  background: var(--bg-card);
  border: var(--border-thin) solid var(--border-subtle);
  border-radius: var(--card-radius);
  overflow: hidden;
  transition: all var(--duration-normal) var(--ease-out);
}

.content-card:hover {
  border-color: var(--border-hover);
  box-shadow: var(--shadow-card-hover);
  transform: translateY(-2px);
}

.card-cover {
  height: var(--card-cover-height);
  display: flex;
  align-items: center;
  justify-content: center;
  background: var(--gradient-card-neutral);
}

.card-icon { font-size: 48px; }

.card-body {
  padding: var(--card-padding);
  display: flex;
  flex-direction: column;
  gap: var(--space-2);
}

.card-title {
  font-size: var(--text-h4);
  font-weight: var(--weight-semibold);
  color: var(--text-primary);
  margin: 0;
}

.card-desc {
  font-size: var(--text-sm);
  color: var(--text-muted);
  margin: 0;
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
  overflow: hidden;
}

.content-card .favorite {
  position: absolute;
  top: var(--space-3);
  right: var(--space-3);
}
```

---

## 3. Collection Card

```html
<div class="collection-card">
  <div class="collection-icon icon-container icon-container--gold">
    <svg>...</svg>
  </div>
  <div class="collection-info">
    <h4 class="collection-title">Pesquisa Profunda</h4>
    <span class="collection-count">4 documentos</span>
  </div>
</div>
```

```css
.collection-card {
  display: flex;
  align-items: center;
  gap: var(--space-4);
  padding: var(--space-4);
  background: var(--bg-card);
  border: var(--border-thin) solid var(--border-subtle);
  border-radius: var(--radius-xl);
  cursor: pointer;
  transition: all var(--duration-fast) var(--ease-out);
}

.collection-card:hover {
  background: var(--bg-card-hover);
  border-color: var(--border-hover);
}

.collection-info {
  display: flex;
  flex-direction: column;
  gap: var(--space-1);
}

.collection-title {
  font-size: var(--text-base);
  font-weight: var(--weight-medium);
  color: var(--text-primary);
  margin: 0;
}

.collection-count {
  font-size: var(--text-xs);
  color: var(--text-muted);
  text-transform: uppercase;
  letter-spacing: 0.05em;
}
```

---

## 4. Section Header

```html
<div class="section-header">
  <div class="section-label">
    <span class="text-overline">Curadoria</span>
    <h2 class="text-h2">Coleções</h2>
  </div>
  <a href="#" class="btn-ghost">Ver todas →</a>
</div>
```

```css
.section-header {
  display: flex;
  align-items: flex-end;
  justify-content: space-between;
  gap: var(--space-4);
  margin-bottom: var(--space-6);
}

.section-label {
  display: flex;
  flex-direction: column;
  gap: var(--space-1);
}

.section-header h2 { margin: 0; }
```

---

## 5. Hero Banner

```html
<div class="hero-banner">
  <div class="hero-content">
    <span class="hero-badge">
      <span class="badge">Curadoria Exclusiva</span>
      <span class="text-sm text-muted">10 documentos</span>
    </span>
    <h1 class="text-display">
      Methodology <span class="text-display-accent">As A System.</span>
    </h1>
    <p class="text-lg">Toda a tese do MaaS centralizada e organizada.</p>
  </div>
  <button class="btn-secondary">Minha Lista</button>
</div>
```

```css
.hero-banner {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: var(--space-10) var(--space-8);
  background: var(--gradient-hero);
  border: var(--border-thin) solid var(--border-subtle);
  border-radius: var(--radius-2xl);
}

.hero-content {
  display: flex;
  flex-direction: column;
  gap: var(--space-4);
  max-width: 600px;
}

.hero-badge {
  display: flex;
  align-items: center;
  gap: var(--space-3);
}

.hero-content p { margin: 0; }
```

---

## 6. Filter Tags Row

```html
<div class="filter-tags">
  <button class="tag tag--active">Todos</button>
  <button class="tag">Pesquisa</button>
  <button class="tag">Metodologia</button>
  <button class="tag">Framework</button>
  <button class="tag">Scripts</button>
</div>
```

```css
.filter-tags {
  display: flex;
  flex-wrap: wrap;
  gap: var(--space-2);
  padding: var(--space-4) 0;
}

.filter-tags .tag {
  cursor: pointer;
  border: none;
  transition: all var(--duration-fast) var(--ease-out);
}

.filter-tags .tag:hover:not(.tag--active) {
  background: var(--bg-card-hover);
  color: var(--text-primary);
}
```

---

## 7. Search Bar with Filters

```html
<div class="search-bar">
  <div class="search">
    <svg class="search-icon">...</svg>
    <input type="text" class="input" placeholder="Buscar documentos...">
  </div>
  <div class="search-actions">
    <button class="btn-icon"><svg>filter</svg></button>
    <button class="btn-icon"><svg>grid</svg></button>
  </div>
</div>
```

```css
.search-bar {
  display: flex;
  align-items: center;
  gap: var(--space-4);
}

.search-bar .search { flex: 1; max-width: 400px; }

.search-actions {
  display: flex;
  gap: var(--space-1);
}
```

---

## 8. Document Meta

```html
<div class="doc-meta">
  <span class="doc-date">24 Jan 2026</span>
  <span class="doc-divider">•</span>
  <span class="doc-reading">15 min leitura</span>
  <span class="doc-divider">•</span>
  <span class="doc-words">5.400 palavras</span>
</div>
```

```css
.doc-meta {
  display: flex;
  align-items: center;
  gap: var(--space-2);
  font-size: var(--text-xs);
  color: var(--text-muted);
}

.doc-divider { opacity: 0.5; }
```

---

## 9. Breadcrumb

```html
<nav class="breadcrumb">
  <a href="#">Hub</a>
  <span class="breadcrumb-sep">/</span>
  <a href="#">Metodologia</a>
  <span class="breadcrumb-sep">/</span>
  <span class="breadcrumb-current">Arquiteto de Conhecimento</span>
</nav>
```

```css
.breadcrumb {
  display: flex;
  align-items: center;
  gap: var(--space-2);
  font-size: var(--text-sm);
}

.breadcrumb a {
  color: var(--text-muted);
  text-decoration: none;
  transition: color var(--duration-fast);
}

.breadcrumb a:hover { color: var(--text-primary); }

.breadcrumb-sep { color: var(--text-disabled); }

.breadcrumb-current { color: var(--text-primary); }
```

---

## 10. Stats Row

```html
<div class="stats-row">
  <div class="stat">
    <span class="stat-value">10</span>
    <span class="stat-label">Documentos</span>
  </div>
  <div class="stat">
    <span class="stat-value">5.5k</span>
    <span class="stat-label">Linhas</span>
  </div>
  <div class="stat">
    <span class="stat-value">6</span>
    <span class="stat-label">Categorias</span>
  </div>
</div>
```

```css
.stats-row {
  display: flex;
  gap: var(--space-8);
}

.stat {
  display: flex;
  flex-direction: column;
  gap: var(--space-1);
}

.stat-value {
  font-family: var(--font-display);
  font-size: var(--text-h2);
  font-weight: var(--weight-bold);
  color: var(--accent-gold);
}

.stat-label {
  font-size: var(--text-xs);
  color: var(--text-muted);
  text-transform: uppercase;
  letter-spacing: 0.05em;
}
```

---

*Molecules v1.0 - MaaS Hub*
