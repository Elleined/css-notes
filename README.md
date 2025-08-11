# css-notes
Notes for CSS

# CSS Selectors

## 1. Basic Selectors
| Selector | Description | Example | Matches |
|----------|-------------|---------|---------|
| `element` | Selects all elements of that type | `p { color: red; }` | All `<p>` |
| `.class` | Selects elements with a class | `.btn { background: blue; }` | `<button class="btn">` |
| `#id` | Selects a single element by ID | `#header { font-size: 20px; }` | `<div id="header">` |
| `*` | Universal selector (all elements) | `* { margin: 0; }` | All elements |

---

## 2. Grouping and Combining
| Selector | Example | Meaning |
|----------|---------|---------|
| `A, B` | `h1, h2 { color: blue; }` | Style multiple selectors |
| `A B` | `div p { color: gray; }` | Descendant selector (p inside div) |
| `A > B` | `div > p { font-weight: bold; }` | Direct child |
| `A + B` | `h1 + p { margin-top: 0; }` | Adjacent sibling |
| `A ~ B` | `h1 ~ p { color: red; }` | General sibling |

---

## 3. Pseudo-classes (State-based)
| Example | Description |
|---------|-------------|
| `a:hover` | When hovered |
| `a:active` | When clicked |
| `input:focus` | When focused |
| `li:first-child` | First child |
| `li:last-child` | Last child |
| `li:nth-child(2)` | Second child |
| `:not(selector)` | Negation |

---

## 4. Pseudo-elements (Part of an element)
| Example | Description |
|---------|-------------|
| `p::first-line` | First line of text |
| `p::first-letter` | First letter |
| `::before` | Content before element |
| `::after` | Content after element |
