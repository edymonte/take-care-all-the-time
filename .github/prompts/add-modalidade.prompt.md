---
mode: agent
description: Adiciona uma nova modalidade esportiva ao site da academia Take Care All The Time, seguindo os padrões de código e identidade visual do projeto.
---

# Prompt: Adicionar Nova Modalidade

Antes de começar, leia os arquivos:
- `index.html` — para entender a estrutura atual dos cards
- `css/style.css` — para checar variáveis e classes disponíveis
- `.github/knowledge/modalidades.md` — para ver o catálogo atual

---

## Informações que preciso do usuário

Se não foram fornecidas, pergunte:

1. **Nome** da nova modalidade
2. **Emoji** representativo (ex: 🏸, 🥊, 🤸…)
3. **Badge** — 2 a 4 palavras que descrevem o diferencial (ex: "Baixo impacto", "Para iniciantes")
4. **Descrição** — ou quer que eu crie seguindo o tom de voz da academia?
5. **Tipo de card**:
   - **Padrão** (sem imagem de fundo) — maioria dos casos
   - **Destaque com foto** (`.card-natacao`, full-width) — para modalidades âncora
6. Se card destaque: **URL da imagem Unsplash** ou quer sugestão?

---

## Implementação

### Passo 1 — Gerar o bloco HTML

**Card padrão:**
```html
<div class="card">
  <div class="card-icon">[EMOJI]</div>
  <h3 class="card-title">[NOME]</h3>
  <p class="card-desc">[DESCRIÇÃO]</p>
  <span class="card-badge">[BADGE]</span>
</div>
```

**Card destaque (com foto):**
```html
<div class="card card-natacao">
  <div class="natacao-img-wrap">
    <img
      src="[URL_UNSPLASH]?auto=format&fit=crop&w=1200&q=80"
      alt="[ALT DESCRITIVO]"
      class="natacao-img"
      loading="lazy"
    />
    <div class="natacao-overlay"></div>
  </div>
  <div class="natacao-content">
    <div class="card-icon">[EMOJI]</div>
    <h3 class="card-title">[NOME]</h3>
    <p class="card-desc">[DESCRIÇÃO]</p>
    <span class="card-badge card-badge-light">[BADGE]</span>
  </div>
</div>
```

### Passo 2 — Inserir no `index.html`
- Cards padrão: inserir **antes** do `.card-natacao` (ou do último card destaque)
- Card destaque: sempre por **último** na `.cards-grid`

### Passo 3 — Atualizar o catálogo
- Adicionar a nova modalidade em `.github/knowledge/modalidades.md`

### Passo 4 — Validar
- [ ] Confirmar que não há `innerHTML` com dados externos
- [ ] Checar `alt` descritivo em qualquer `<img>` adicionado
- [ ] Verificar visual nos breakpoints 375px, 640px e 960px (descrever como ficou)

---

## Resposta esperada
1. Bloco HTML completo da nova modalidade
2. Onde exatamente inserir (antes de qual elemento, com linhas de contexto)
3. Confirmação de que o catálogo `.github/knowledge/modalidades.md` foi atualizado
4. Resumo visual do resultado esperado
