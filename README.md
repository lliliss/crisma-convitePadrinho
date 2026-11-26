# 🕊️ Convite de Crisma

Convite digital e animado para convidar um padrinho de Crisma. É uma página única em HTML, CSS e JavaScript puro, sem frameworks e sem build, pronta para hospedar no Vercel.

## ✨ Como funciona

1. **Envelope lacrado**: a página abre com um envelope selado com cera, flutuando sobre um fundo terracota com partículas de luz dourada subindo.
2. **Abertura**: ao tocar no envelope, o selo se rompe, a aba se abre e a carta sobe.
3. **Cartão**: a pomba do Espírito Santo se desenha na tela e o texto do convite aparece linha por linha.
4. **Resposta**:
   - **"Sim, aceito!"**: solta uma explosão de partículas douradas e mostra um agradecimento.
   - **"Preciso pensar…"**: o botão foge do cursor 😄 e, na quarta tentativa, vira "Tá bom, aceito!".
5. **WhatsApp**: depois de aceitar, um botão abre uma conversa com a afilhada, com a resposta já escrita.

## 🛠️ Tecnologias

- HTML5 e CSS3, com animações, transformações 3D e `clip-path`
- JavaScript puro, com as partículas desenhadas em `<canvas>`
- SVG para a pomba (animada com `stroke-dashoffset`), o selo e o envelope
- Fontes do Google Fonts: Cormorant Garamond, Great Vibes e Lato

## 🎨 Personalização

No início do `<script>`, edite o objeto `CONFIG`:

```js
const CONFIG = {
  padrinho: 'Nome do padrinho',  // aparece no texto do convite
  afilhada: 'Seu nome',          // assinatura e mensagem do WhatsApp
  whatsapp: '5582999999999'      // 55 + DDD + número, só dígitos
}
```

A mensagem que ele envia pelo WhatsApp fica na função `aceitar`:

```js
const msg = `Aceito ser seu padrinho de Crisma, ${CONFIG.afilhada}! 🙏🏻🧡`
```

As cores principais ficam nas variáveis do `:root`, no começo do `<style>`:

| Variável | Uso |
|---|---|
| `--bg` / `--bg2` | Degradê do fundo (tema claro e escuro) |
| `--red` | Cor de destaque: título, nome e botões |
| `--gold` | Moldura, pomba e detalhes dourados |
| `--paper` | Cor do papel do cartão |

## 🚀 Deploy no Vercel

**Pela CLI:**

```bash
npx vercel          # preview
npx vercel --prod   # produção
```

**Pelo GitHub:** importe o repositório no painel do Vercel, escolha **Other** em *Framework Preset* e faça o deploy. Não é preciso comando de build nem pasta de saída.

## 📁 Estrutura

```
.
├── index.html   # convite completo (HTML, CSS e JS)
└── README.md
```

## ♿ Acessibilidade

- Funciona por teclado: o envelope e os botões recebem foco visível
- Respeita `prefers-reduced-motion`: com animações desativadas no aparelho, o cartão aparece direto, sem movimento
- Layout responsivo, pensado primeiro para celular

## 🙏 Versículo

> "E, havendo dito isso, assoprou sobre eles e disse-lhes: Recebei o Espírito Santo."
> — João 20:22

---

Feito com carinho por **llilis** 
