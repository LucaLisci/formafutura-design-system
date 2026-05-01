# Forma Futura — Design System

Design system per [formafutura.ai](https://www.formafutura.ai), strutturato per essere consumato da AI design agents come **Claude Design** (`claude.ai/design`), Google Stitch e simili.

## Cosa c'è dentro

```
.
├── DESIGN.md              ← Documento principale. È il file che gli AI design agents leggono.
├── tokens/
│   ├── tokens.json        ← Tokens Studio format (per Figma plugin)
│   └── tokens.w3c.json    ← W3C Design Tokens Format (standard universale)
├── preview/
│   └── index.html         ← Documentazione visiva. Aprila in browser per vedere tutto renderizzato.
└── README.md
```

## Come usarla con Claude Design

1. Apri [claude.ai/design](https://claude.ai/design)
2. Crea un nuovo progetto
3. Allega o linka questa repo, oppure copia-incolla il contenuto di [`DESIGN.md`](./DESIGN.md) nel prompt iniziale
4. Chiedi a Claude di scaffoldare un'interfaccia ("crea una landing page", "disegna una dashboard del coach", ecc.) — userà il design system come riferimento

> **Tip**: per risparmiare token, riferisciti al `DESIGN.md` per nome invece di reincollarlo a ogni iterazione. Claude Design tiene il documento in contesto persistente.

## Come usarla con Figma

Installa il plugin gratuito **[Tokens Studio for Figma](https://tokens.studio/)**, poi:

1. Plugin → Tokens Studio → Settings → **Load from file**
2. Seleziona [`tokens/tokens.json`](./tokens/tokens.json)
3. Tab Tokens → **Create styles** → genera automaticamente tutti i color/text/effect styles in Figma

## Come usarla in codice

I tokens W3C-compatibili in [`tokens/tokens.w3c.json`](./tokens/tokens.w3c.json) sono direttamente consumabili da:

- [Style Dictionary](https://amzn.github.io/style-dictionary/) → CSS, SCSS, JS, iOS, Android
- [Tokens Studio CLI](https://docs.tokens.studio/)
- [Terrazzo](https://terrazzo.app/)

## Identità in 5 secondi

| | |
|---|---|
| **Mood** | Editoriale, dark-first, italian-design, anti-hype |
| **Display** | Fraunces (serif, italic per parole-chiave) |
| **Body** | Inter |
| **Accent unico** | `#C8FF00` lime elettrico — CTA, NODO™, focus |
| **Background** | `#0A0A0A` (Ink) — quasi nero, mai puro |
| **Forme** | Bottoni pill, card 16-24px radius, geometria minima |

Apri [`preview/index.html`](./preview/index.html) per vedere tutto renderizzato.

## License

`DESIGN.md`, tokens e documentazione: liberi d'uso per il progetto Forma Futura.

I marchi *Forma Futura* e *NODO™* appartengono a Forma Futura. I font referenziati (Fraunces, Inter, JetBrains Mono) sono distribuiti con licenza [SIL OFL](https://scripts.sil.org/OFL).
