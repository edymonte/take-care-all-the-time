# Knowledge Base — Brand Guide
# Take Care All The Time

## Identidade da Marca

### Nome oficial
**Take Care All The Time**
- Abreviação aceita internamente: **TCATT**
- Nunca abreviar em comunicações externas/site

### Slogan
> "Cuide do seu corpo. Cuide da sua mente. Cuide da sua vida."

### Tom de voz
| Atributo     | Descrição                                          |
|--------------|----------------------------------------------------|
| Motivacional | Incentiva, desafia, celebra conquistas             |
| Premium      | Linguagem sofisticada, sem gírias excessivas        |
| Inclusivo    | Todas as idades, todos os níveis, todos os corpos  |
| Próximo      | Formal-amigável, "você" (não "tu" nem "vós")       |

### O que nunca dizer
- "Produto" (use "modalidade", "serviço", "experiência")
- "Clique aqui" (use ações específicas: "Conheça", "Comece agora")
- "Usuário" (use "aluno", "membro", "você")

---

## Paleta de Cores

| Token CSS       | Hex        | Uso                              |
|-----------------|------------|----------------------------------|
| `--orange`      | `#ff6b00`  | Acento principal, CTAs, ícones   |
| `--orange-d`    | `#e05c00`  | Hover states de botões           |
| `--orange-l`    | `#ff8c33`  | Textos sobre fundos escuros      |
| `--bg`          | `#0d0d0f`  | Fundo principal da página        |
| `--bg2`         | `#111116`  | Seções alternadas                |
| `--bg3`         | `#17171f`  | Cards especiais                  |
| `--card-bg`     | `#1a1a26`  | Background dos cards             |
| `--text`        | `#f0f0f5`  | Texto principal                  |
| `--text-muted`  | `#8888aa`  | Texto secundário / placeholders  |
| Verde parceiro  | `#2ecc71`  | Badge Farmácia Boa Farma         |

---

## Tipografia

**Família**: Poppins (Google Fonts)

| Peso | Uso                           |
|------|-------------------------------|
| 300  | Subtítulos leves              |
| 400  | Corpo de texto padrão         |
| 600  | Labels, badges, nav links     |
| 700  | Títulos de seção e cards      |
| 900  | Hero title, logo principal    |

---

## Parceiro Oficial — Farmácia Boa Farma

### Regras de uso
- Sempre exibido no footer como "Parceiro oficial"
- Badge verde com ícone ✚ (cruz farmacêutica)
- Cor: `#2ecc71` — nunca alterar sem aprovação do cliente
- Nome completo: **Farmácia Boa Farma** (sem "A" ou "Da")
- Link para o site da farmácia deve usar `rel="noopener noreferrer"`

### Posicionamento no footer
- Coluna central entre brand da academia (esquerda) e redes sociais (direita)
- Label: "Parceiro oficial" (texto em `--text-muted`, uppercase, letter-spacing)

---

## Imagens e Mídia

### Fonte aprovada
- **Unsplash** — único serviço aprovado para imagens externas
- Formato de URL: `?auto=format&fit=crop&w=1200&q=80`
- Nunca baixar ou versionar imagens binárias no repositório

### Critérios de seleção de imagens
- Diversidade de pessoas (idade, corpo, etnia)
- Expressões positivas e energia
- Sem logos de concorrentes visíveis
- Qualidade profissional (iluminação, composição)

### Imagens em uso (URLs ativas)
| Local            | Descrição                        |
|------------------|----------------------------------|
| Hero background  | Academia com pessoas treinando   |
| Card Natação     | Piscina com pessoas nadando felizes |

---

## Diretrizes de Acessibilidade
- Contraste mínimo: WCAG AA (4.5:1 para texto normal)
- Todo `<img>` precisa de `alt` descritivo em PT-BR
- Botões e links precisam de `aria-label` quando o texto não é suficiente
- Navegação por teclado: foco visível em todos os elementos interativos
