---
mode: ask
description: Realiza um code review completo dos arquivos do site da academia, verificando qualidade, acessibilidade, segurança e aderência aos padrões do projeto.
---

# Prompt: Code Review — Take Care All The Time

Faça um code review completo dos arquivos do projeto. Leia:
- `index.html`
- `css/style.css`
- `js/main.js`

Organize o resultado nos seguintes blocos:

---

## 🔒 Segurança (OWASP Top 10)
Verifique e reporte:
- [ ] Uso de `innerHTML` com dados externos → deve usar `textContent`
- [ ] `eval()` ou `Function()` dinâmico → proibido
- [ ] Links externos sem `rel="noopener noreferrer"`
- [ ] Inputs sem sanitização antes de inserir no DOM
- [ ] Scripts de terceiros sem versão fixada

---

## ♿ Acessibilidade
Verifique e reporte:
- [ ] Todo `<img>` tem atributo `alt` descritivo?
- [ ] Botões com `aria-label` onde necessário?
- [ ] Contraste de texto (mínimo WCAG AA: 4.5:1 para texto normal)?
- [ ] Navegação por teclado funcional (foco visível)?
- [ ] `lang="pt-BR"` na tag `<html>`?

---

## 📐 Padrões de Código
Verifique e reporte:

**HTML:**
- [ ] Tags semânticas usadas corretamente (`<nav>`, `<section>`, `<footer>`)?
- [ ] IDs de âncora corretos: `#home`, `#modalidades`?
- [ ] `loading="lazy"` em todos os `<img>` (exceto hero)?

**CSS:**
- [ ] Variáveis CSS em `:root` para cores e espaçamentos?
- [ ] Mobile-first com `@media (min-width)`?
- [ ] `--trans: .3s ease` em todos os `transition`?
- [ ] Nenhuma cor hardcoded que deveria ser variável?

**JavaScript:**
- [ ] Padrão IIFE com `'use strict'`?
- [ ] Scroll listeners com `{ passive: true }`?
- [ ] `IntersectionObserver` com `threshold: 0.12`?
- [ ] Zero dependências de runtime?

---

## 🎨 Identidade Visual
- [ ] Paleta respeitada: `--orange: #ff6b00`, `--bg: #0d0d0f`?
- [ ] Tipografia: apenas Poppins (300/400/600/700/900)?
- [ ] Badge da Farmácia Boa Farma com cor `#2ecc71`?
- [ ] Card Natação como destaque full-width com `grid-column: 1 / -1`?

---

## 📱 Responsividade
- [ ] Grid de cards: 3 colunas (>960px) → 2 colunas (640–960px) → 1 coluna (<640px)?
- [ ] Menu hamburguer aparece em mobile (<640px)?
- [ ] Nenhum overflow horizontal em nenhum viewport?

---

## 🚀 Performance
- [ ] Imagens Unsplash com parâmetros `?auto=format&fit=crop&w=1200&q=80`?
- [ ] JS no final do `<body>`?
- [ ] Google Fonts com `rel="preconnect"` antes do link?

---

## Resultado Final

Para cada problema encontrado, informe:
- **Arquivo e linha** aproximada
- **Problema** (descrição clara)
- **Sugestão de correção** (código corrigido)
- **Severidade**: 🔴 Crítico | 🟡 Médio | 🟢 Sugestão
