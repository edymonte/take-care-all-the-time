---
description: >
  Domínio completo do site Take Care All The Time — estrutura de arquivos,
  padrões de componentes, variáveis CSS, grid de cards e guidelines de
  conteúdo. Use esta skill em qualquer tarefa que envolva alterar ou criar
  HTML/CSS/JS do site.
---

# Skill: Academia Website — Take Care All The Time

## Quando usar esta skill
- Adicionar, editar ou remover uma modalidade
- Criar nova seção (horários, planos, depoimentos, equipe…)
- Ajustar identidade visual (cores, tipografia, espaçamentos)
- Corrigir problemas de responsividade nos breakpoints
- Integrar parceiros ou patrocinadores no footer

## Estrutura do Projeto
```
teste_context7/
├── index.html          ← página única com âncoras #home e #modalidades
├── css/
│   └── style.css       ← variáveis CSS, componentes, responsivo
└── js/
    └── main.js         ← navbar scroll, hamburger, IntersectionObserver
```

## Componentes — HTML

### Card de Modalidade (padrão — copie este bloco)
```html
<div class="card">
  <div class="card-icon">🏋️</div>
  <h3 class="card-title">Nome da Modalidade</h3>
  <p class="card-desc">Descrição motivacional em 2-3 frases.</p>
  <span class="card-badge">Tag descritiva</span>
</div>
```

### Card Destaque com Imagem (estilo Natação — full-width)
```html
<div class="card card-natacao">
  <div class="natacao-img-wrap">
    <img
      src="https://images.unsplash.com/photo-PHOTO_ID?auto=format&fit=crop&w=1200&q=80"
      alt="Descrição acessível da imagem"
      class="natacao-img"
      loading="lazy"
    />
    <div class="natacao-overlay"></div>
  </div>
  <div class="natacao-content">
    <div class="card-icon">🏊</div>
    <h3 class="card-title">Nome da Modalidade</h3>
    <p class="card-desc">Descrição motivacional em 2-3 frases.</p>
    <span class="card-badge card-badge-light">Tag descritiva</span>
  </div>
</div>
```

## Variáveis CSS disponíveis
| Variável          | Valor          | Uso                         |
|-------------------|----------------|-----------------------------|
| `--orange`        | `#ff6b00`      | Cor de acento principal      |
| `--orange-d`      | `#e05c00`      | Hover de botões laranja      |
| `--orange-l`      | `#ff8c33`      | Textos sobre fundo escuro    |
| `--bg`            | `#0d0d0f`      | Fundo da página              |
| `--bg2`           | `#111116`      | Seções alternadas            |
| `--bg3`           | `#17171f`      | Cards especiais              |
| `--card-bg`       | `#1a1a26`      | Background dos cards         |
| `--text`          | `#f0f0f5`      | Texto principal              |
| `--text-muted`    | `#8888aa`      | Texto secundário             |
| `--border`        | `rgba(255,107,0,.18)` | Borda dos cards       |
| `--radius`        | `16px`         | Border-radius padrão         |
| `--shadow`        | `0 8px 40px rgba(0,0,0,.55)` | Sombra hover  |
| `--trans`         | `.3s ease`     | Transição padrão             |

## Grid de Cards — Regras
- Desktop (>960px): `repeat(3, 1fr)` — 3 colunas
- Tablet (640–960px): `repeat(2, 1fr)` — 2 colunas
- Mobile (<640px): `1fr` — 1 coluna
- **Card destaque** (`.card-natacao`): sempre `grid-column: 1 / -1` (full width)
- O card destaque vai **sempre por último** antes do fechamento da `.cards-grid`

## Adicionar Nova Modalidade — Checklist
1. Copie o bloco "Card padrão" acima no `index.html`
2. Insira **antes** do `.card-natacao`
3. Escolha emoji representativo
4. Escreva descrição em PT-BR, tom motivacional, máx. 3 frases
5. Defina badge (ex: "Para iniciantes", "Baixo impacto")
6. Abra DevTools → redimensione para 640px e 375px e valide o layout

## Parceiro — Farmácia Boa Farma
- Localização: coluna central do footer
- Visual: badge verde `#2ecc71` com ícone ✚
- Quando o logo real estiver disponível, substituir `.parceiro-badge` por:
  ```html
  <a href="URL_FARMACIA" rel="noopener noreferrer">
    <img src="assets/boa-farma-logo.svg" alt="Farmácia Boa Farma" width="140" loading="lazy" />
  </a>
  ```

## Boas Práticas de Performance
- Imagens Unsplash: sempre usar `?auto=format&fit=crop&w=1200&q=80`
- `loading="lazy"` em todos os `<img>` exceto o hero
- CSS crítico inline não é necessário (site pequeno, 1 CSS)
- JS no final do `<body>`, antes de `</body>`
