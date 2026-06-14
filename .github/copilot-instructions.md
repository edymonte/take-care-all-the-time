# Take Care All The Time — Copilot Instructions
<!-- applyTo: "**" -->

## Identidade do Projeto
- **Produto**: Site institucional da academia "Take Care All The Time"
- **Stack**: HTML5, CSS3, JavaScript puro (zero dependências de runtime)
- **Hospedagem**: GitHub Pages (branch `main`, pasta raiz)
- **Parceiro oficial**: Farmácia Boa Farma — presente no footer com badge verde

## Arquitetura
- Single-page application com scroll suave entre seções âncora
- Estrutura obrigatória: `index.html`, `css/style.css`, `js/main.js`
- Imagens: Unsplash via URL externa — **nunca** baixar ou versionar imagens binárias
- Fontes: Google Fonts — Poppins (300, 400, 600, 700, 900)
- Seções âncora fixas: `#home` e `#modalidades`

## Padrões de Código

### HTML
- Tag `<html>` sempre com `lang="pt-BR"`
- Todo `<img>` deve ter `alt` descritivo e `loading="lazy"` (exceto hero)
- Usar tags semânticas: `<nav>`, `<section>`, `<footer>`, `<article>`
- Links externos: sempre `rel="noopener noreferrer"`
- **Nunca** usar `innerHTML` com conteúdo dinâmico externo (XSS)

### CSS
- Variáveis em `:root` para qualquer cor ou espaçamento reutilizado
- Paleta principal: `--orange: #ff6b00` | `--bg: #0d0d0f` | `--text: #f0f0f5`
- Breakpoints: `640px` (mobile→tablet) e `960px` (tablet→desktop)
- Mobile-first: estilos base para mobile, `@media (min-width)` para expandir
- Transições: usar `--trans: .3s ease` em todos os `transition`

### JavaScript
- Vanilla JS — sem jQuery, sem frameworks, sem lodash
- Padrão IIFE: `(function () { 'use strict'; })()`
- Scroll listener: sempre `{ passive: true }`
- Animações de entrada: `IntersectionObserver` com `threshold: 0.12`
- Manipulação DOM: usar `textContent` em vez de `innerHTML`

## Identidade Visual
- **Tema**: Escuro com acentos laranja energético
- **Tom de voz**: Motivacional, premium, inclusivo — PT-BR formal-amigável
- Card destaque (Natação): `grid-column: 1 / -1`, imagem Unsplash de piscina
- Farmácia Boa Farma: badge verde `#2ecc71` com ícone ✚ no footer

## Modalidades Atuais (5)
| Emoji | Modalidade  | Badge             |
|-------|-------------|-------------------|
| 🏋️    | Musculação  | Todos os níveis   |
| 🚴    | Spinning    | Alta intensidade  |
| 🔥    | Crossfit    | Desafio máximo    |
| 🧘    | Yoga        | Bem-estar total   |
| 🏊    | Natação     | Para todas as idades |

## Segurança (OWASP Top 10)
- Sanitizar qualquer input antes de inserir no DOM
- Sem uso de `eval()` ou `Function()` dinâmico
- Headers de segurança configurados via `_headers` (GitHub Pages / Netlify)
- Dependências externas (CDN/npm) apenas de fontes confiáveis e fixadas na versão

## Convenções Git
- **Branches**: `feat/`, `fix/`, `docs/`, `style/`, `chore/`, `refactor/`
- **Commits**: Conventional Commits em português
  - `feat: adiciona seção de horários`
  - `fix: corrige quebra de layout no card de natação em mobile`
  - `style: ajusta espaçamento dos cards no breakpoint 960px`
- **PRs**: título em Conventional Commits + `Closes #N` no corpo
- **Reviews**: toda PR requer ao menos 1 aprovação antes do merge

## Agentes Disponíveis
- `web-developer` → alterações estruturais (HTML/CSS/JS)
- `content-manager` → atualização de textos, imagens e modalidades
