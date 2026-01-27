# Organisms - MaaS Hub Design System

---

## 1. Sidebar

```html
<aside class="sidebar">
  <div class="sidebar-header">
    <div class="sidebar-logo">
      <span class="logo-symbol">Kₑ</span>
      <span class="logo-text">MaaS Hub</span>
    </div>
  </div>

  <nav class="sidebar-nav">
    <div class="nav-section">
      <span class="nav-section-title">Navegação</span>
      <a href="#" class="nav-item nav-item--active">
        <span class="nav-icon">🏠</span>
        <span class="nav-label">Início</span>
      </a>
      <a href="#" class="nav-item">
        <span class="nav-icon">⭐</span>
        <span class="nav-label">Favoritos</span>
      </a>
      <a href="#" class="nav-item">
        <span class="nav-icon">🕐</span>
        <span class="nav-label">Recentes</span>
      </a>
    </div>

    <div class="nav-section">
      <span class="nav-section-title">Categorias</span>
      <a href="#" class="nav-item">
        <span class="nav-icon">🔍</span>
        <span class="nav-label">Pesquisa</span>
        <span class="badge badge--muted">4</span>
      </a>
      <a href="#" class="nav-item">
        <span class="nav-icon">📐</span>
        <span class="nav-label">Metodologia</span>
        <span class="badge badge--muted">2</span>
      </a>
      <a href="#" class="nav-item">
        <span class="nav-icon">🧩</span>
        <span class="nav-label">Framework</span>
        <span class="badge badge--muted">2</span>
      </a>
      <a href="#" class="nav-item">
        <span class="nav-icon">📝</span>
        <span class="nav-label">Scripts</span>
        <span class="badge badge--muted">2</span>
      </a>
    </div>

    <div class="nav-section">
      <span class="nav-section-title">Coleções</span>
      <a href="#" class="nav-item">
        <span class="nav-icon">📚</span>
        <span class="nav-label">Arquiteto de Conhecimento</span>
      </a>
      <a href="#" class="nav-item">
        <span class="nav-icon">🎯</span>
        <span class="nav-label">Content System</span>
      </a>
    </div>
  </nav>

  <div class="sidebar-footer">
    <div class="user-menu">
      <div class="avatar">JC</div>
      <span class="user-name">José Carlos</span>
    </div>
  </div>
</aside>
```

```css
.sidebar {
  position: fixed;
  top: 0;
  left: 0;
  width: var(--sidebar-width);
  height: 100vh;
  display: flex;
  flex-direction: column;
  background: var(--bg-sidebar);
  border-right: var(--border-thin) solid var(--border-subtle);
  z-index: var(--z-sidebar);
}

.sidebar-header {
  padding: var(--space-6) var(--sidebar-padding);
  border-bottom: var(--border-thin) solid var(--border-subtle);
}

.sidebar-logo {
  display: flex;
  align-items: center;
  gap: var(--space-3);
}

.logo-symbol {
  font-family: var(--font-mono);
  font-size: var(--text-lg);
  font-weight: var(--weight-bold);
  color: var(--accent-gold);
  padding: var(--space-2);
  background: var(--accent-gold-muted);
  border-radius: var(--radius-md);
}

.logo-text {
  font-weight: var(--weight-semibold);
  color: var(--text-primary);
}

.sidebar-nav {
  flex: 1;
  overflow-y: auto;
  padding: var(--space-4) var(--sidebar-padding);
}

.nav-section {
  margin-bottom: var(--sidebar-section-gap);
}

.nav-section-title {
  display: block;
  font-size: var(--text-xs);
  font-weight: var(--weight-semibold);
  color: var(--text-muted);
  text-transform: uppercase;
  letter-spacing: 0.1em;
  padding: var(--space-2) var(--space-3);
  margin-bottom: var(--space-2);
}

.sidebar-footer {
  padding: var(--space-4) var(--sidebar-padding);
  border-top: var(--border-thin) solid var(--border-subtle);
}

.user-menu {
  display: flex;
  align-items: center;
  gap: var(--space-3);
}

.user-name {
  font-size: var(--text-sm);
  color: var(--text-secondary);
}
```

---

## 2. Main Content Layout

```html
<main class="main-content">
  <header class="content-header">
    <div class="search-bar">
      <div class="search">
        <svg class="search-icon">...</svg>
        <input type="text" class="input" placeholder="Buscar documentos...">
      </div>
    </div>
    <div class="header-actions">
      <button class="btn-icon"><svg>bell</svg></button>
      <div class="avatar">JC</div>
    </div>
  </header>

  <div class="content-body">
    <!-- Page content here -->
  </div>
</main>
```

```css
.main-content {
  margin-left: var(--sidebar-width);
  min-height: 100vh;
  background: var(--bg-main);
}

.content-header {
  position: sticky;
  top: 0;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: var(--space-4) var(--content-padding);
  background: var(--bg-main);
  border-bottom: var(--border-thin) solid var(--border-subtle);
  z-index: var(--z-sticky);
}

.header-actions {
  display: flex;
  align-items: center;
  gap: var(--space-4);
}

.content-body {
  padding: var(--content-padding);
  max-width: var(--content-max-width);
}
```

---

## 3. Hero Section

```html
<section class="hero-section">
  <div class="hero-banner">
    <div class="hero-content">
      <span class="hero-badge">
        <span class="badge">Curadoria Exclusiva</span>
        <span class="text-sm text-muted">10 documentos</span>
      </span>
      <h1 class="text-display">
        Methodology <span class="text-display-accent">As A System.</span>
      </h1>
      <p class="text-lg">A tese completa do MaaS. Pesquisa, metodologia, frameworks e implementação.</p>
    </div>
    <button class="btn-secondary">Minha Lista</button>
  </div>
</section>
```

---

## 4. Collections Grid

```html
<section class="collections-section">
  <div class="section-header">
    <div class="section-label">
      <span class="text-overline">Curadoria</span>
      <h2 class="text-h2">Coleções</h2>
    </div>
    <a href="#" class="btn-ghost">Ver todas →</a>
  </div>

  <div class="collections-grid">
    <div class="collection-card">
      <div class="icon-container icon-container--gold">📐</div>
      <div class="collection-info">
        <h4 class="collection-title">Arquiteto de Conhecimento</h4>
        <span class="collection-count">6 documentos</span>
      </div>
    </div>
    <!-- More collection cards -->
  </div>
</section>
```

```css
.collections-section {
  margin-bottom: var(--space-16);
}

.collections-grid {
  display: grid;
  grid-template-columns: var(--grid-cols-collections);
  gap: var(--grid-gap);
}
```

---

## 5. Category Filter Bar

```html
<section class="filter-section">
  <div class="filter-tags">
    <button class="tag tag--active">Todos</button>
    <button class="tag">Pesquisa</button>
    <button class="tag">Metodologia</button>
    <button class="tag">Framework</button>
    <button class="tag">Scripts</button>
    <button class="tag">Análise</button>
    <button class="tag">Manifesto</button>
  </div>
</section>
```

---

## 6. Content Cards Grid

```html
<section class="catalog-section">
  <div class="section-header">
    <div class="section-label">
      <span class="text-overline">Catálogo Completo</span>
      <h2>
        <span class="text-metric">10</span>
        <span class="text-metric-accent">documentos</span>
      </h2>
    </div>
    <p class="text-sm text-muted">Explore toda a base de conhecimento MaaS.</p>
  </div>

  <div class="content-grid">
    <article class="content-card">
      <div class="card-cover" style="background: var(--gradient-card-gold)">
        <span class="card-icon">📐</span>
      </div>
      <div class="card-body">
        <span class="tag tag--methodology">Metodologia</span>
        <h3 class="card-title">Arquiteto de Conhecimento</h3>
        <p class="card-desc">Mastermind & Mentoria High Ticket para Experts</p>
      </div>
      <button class="favorite">☆</button>
    </article>
    <!-- More content cards -->
  </div>
</section>
```

```css
.catalog-section {
  margin-bottom: var(--space-16);
}

.content-grid {
  display: grid;
  grid-template-columns: var(--grid-cols-cards);
  gap: var(--grid-gap);
}
```

---

## 7. Document Reader View

```html
<article class="document-view">
  <header class="doc-header">
    <nav class="breadcrumb">
      <a href="#">Hub</a>
      <span>/</span>
      <a href="#">Metodologia</a>
      <span>/</span>
      <span>Arquiteto de Conhecimento</span>
    </nav>

    <div class="doc-title-row">
      <div>
        <span class="tag tag--methodology">Metodologia</span>
        <h1 class="text-h1">Arquiteto de Conhecimento</h1>
        <p class="text-lg">Mastermind & Mentoria High Ticket para Experts</p>
      </div>
      <div class="doc-actions">
        <button class="btn-icon favorite">☆</button>
        <button class="btn-secondary">Copiar Link</button>
      </div>
    </div>

    <div class="doc-meta">
      <span>24 Jan 2026</span>
      <span>•</span>
      <span>15 min leitura</span>
      <span>•</span>
      <span>5.400 palavras</span>
    </div>
  </header>

  <div class="doc-content">
    <!-- Rendered markdown content -->
  </div>

  <aside class="doc-toc">
    <h4>Neste documento</h4>
    <nav class="toc-nav">
      <a href="#" class="toc-item toc-item--active">Introdução</a>
      <a href="#" class="toc-item">O Problema</a>
      <a href="#" class="toc-item">A Solução</a>
      <a href="#" class="toc-item">Metodologia</a>
      <a href="#" class="toc-item">Implementação</a>
    </nav>
  </aside>
</article>
```

```css
.document-view {
  display: grid;
  grid-template-columns: 1fr 240px;
  gap: var(--space-12);
  max-width: 1200px;
}

.doc-header {
  grid-column: 1 / -1;
  display: flex;
  flex-direction: column;
  gap: var(--space-4);
  padding-bottom: var(--space-8);
  border-bottom: var(--border-thin) solid var(--border-subtle);
  margin-bottom: var(--space-8);
}

.doc-title-row {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  gap: var(--space-8);
}

.doc-title-row h1 { margin: var(--space-2) 0; }
.doc-title-row p { margin: 0; }

.doc-actions {
  display: flex;
  gap: var(--space-2);
}

.doc-content {
  font-size: var(--text-base);
  line-height: var(--leading-relaxed);
  color: var(--text-secondary);
}

.doc-content h2 {
  font-size: var(--text-h3);
  color: var(--text-primary);
  margin: var(--space-10) 0 var(--space-4);
  padding-top: var(--space-4);
  border-top: var(--border-thin) solid var(--border-subtle);
}

.doc-content h3 {
  font-size: var(--text-h4);
  color: var(--text-primary);
  margin: var(--space-8) 0 var(--space-3);
}

.doc-content p {
  margin-bottom: var(--space-4);
}

.doc-content ul, .doc-content ol {
  margin-bottom: var(--space-4);
  padding-left: var(--space-6);
}

.doc-content li {
  margin-bottom: var(--space-2);
}

.doc-content code {
  font-family: var(--font-mono);
  font-size: 0.9em;
  padding: 0.2em 0.4em;
  background: var(--bg-elevated);
  border-radius: var(--radius-sm);
  color: var(--accent-gold);
}

.doc-content pre {
  background: var(--bg-card);
  border: var(--border-thin) solid var(--border-subtle);
  border-radius: var(--radius-lg);
  padding: var(--space-4);
  overflow-x: auto;
  margin-bottom: var(--space-4);
}

.doc-content blockquote {
  border-left: 3px solid var(--accent-gold);
  padding-left: var(--space-4);
  margin: var(--space-6) 0;
  color: var(--text-primary);
  font-style: italic;
}

.doc-toc {
  position: sticky;
  top: calc(var(--space-4) + 60px);
  height: fit-content;
}

.doc-toc h4 {
  font-size: var(--text-sm);
  font-weight: var(--weight-semibold);
  color: var(--text-muted);
  text-transform: uppercase;
  letter-spacing: 0.05em;
  margin-bottom: var(--space-4);
}

.toc-nav {
  display: flex;
  flex-direction: column;
  gap: var(--space-1);
}

.toc-item {
  font-size: var(--text-sm);
  color: var(--text-muted);
  text-decoration: none;
  padding: var(--space-2) var(--space-3);
  border-left: 2px solid transparent;
  transition: all var(--duration-fast);
}

.toc-item:hover {
  color: var(--text-primary);
}

.toc-item--active {
  color: var(--text-primary);
  border-left-color: var(--accent-gold);
  background: var(--bg-card);
}
```

---

## 8. Empty State

```html
<div class="empty-state">
  <div class="empty-icon">📭</div>
  <h3>Nenhum documento encontrado</h3>
  <p>Tente buscar com outros termos ou limpe os filtros.</p>
  <button class="btn-secondary">Limpar Filtros</button>
</div>
```

```css
.empty-state {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: var(--space-4);
  padding: var(--space-16);
  text-align: center;
}

.empty-icon {
  font-size: 48px;
  opacity: 0.5;
}

.empty-state h3 {
  font-size: var(--text-h4);
  color: var(--text-primary);
  margin: 0;
}

.empty-state p {
  color: var(--text-muted);
  margin: 0;
  max-width: 300px;
}
```

---

*Organisms v1.0 - MaaS Hub*
