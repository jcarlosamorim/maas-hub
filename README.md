# MaaS Hub

**Methodology As A System** - Biblioteca de conhecimento curado.

## Sobre

MaaS Hub e uma aplicacao web para navegacao e leitura de documentos da metodologia MaaS (Methodology As A System). O sistema apresenta pesquisas, frameworks, scripts e manifestos em um formato otimizado para leitura.

## Funcionalidades

- Catalogo de 15 documentos organizados por categoria
- Sistema de busca em tempo real
- Filtros por tipo: Pesquisa, Metodologia, Framework, Script, Analise, Manifesto
- Leitor de documentos com:
  - 3 temas: Dark, Light, Sepia
  - 3 tamanhos de fonte
  - Suporte a Markdown e diagramas Mermaid
  - Tipografia editorial otimizada para leitura

## Stack Tecnico

- **Frontend:** HTML5, CSS3 (Design Tokens), Vanilla JavaScript
- **Markdown:** marked.js
- **Diagramas:** mermaid.js
- **Hospedagem:** Vercel (edge network)

## Estrutura

```
maas-hub/
├── index.html        # Pagina principal (catalogo)
├── reader.html       # Leitor de documentos
├── content.js        # Conteudo dos documentos (embedded)
├── design-system/    # Documentacao do design system
└── vercel.json       # Configuracao de deploy
```

## Categorias de Conteudo

| Categoria | Documentos | Descricao |
|-----------|------------|-----------|
| Pesquisa | 6 | Deep research e analises |
| Metodologia | 3 | Frameworks metodologicos |
| Framework | 2 | Sistemas de conteudo |
| Script | 1 | Scripts de vendas |
| Manifesto | 2 | Visao e filosofia |
| Analise | 1 | Analise competitiva |

## Desenvolvimento Local

Abra `index.html` diretamente no navegador ou use um servidor local:

```bash
# Python
python -m http.server 8080

# Node.js
npx serve .
```

## Deploy

O deploy e automatico via Vercel ao fazer push para a branch `main`.

**URL de producao:** (sera configurada apos primeiro deploy)

## Design System

O sistema de design utiliza CSS Custom Properties (tokens) para consistencia visual. Documentacao completa em `design-system/`.

### Cores Principais

- Background: `#0D0D0D` (dark mode)
- Accent Gold: `#C9A962`
- Accent Purple: `#9B7BFF`

### Tipografia

- UI: Inter
- Display: Playfair Display
- Body: Source Serif 4
- Mono: JetBrains Mono

## Licenca

Proprietario - Uso interno.

---

*Parte do ecossistema AIOS-FullStack*
