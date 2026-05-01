<p align="center">
  <img src="https://raw.githubusercontent.com/LucaLisci/formafutura-design-system/main/FormaFuturaLogo.svg" alt="Forma Futura" height="64" />
</p>

<h1 align="center">Forma Futura — Design System</h1>

<p align="center">
  Design system per <a href="https://www.formafutura.ai">formafutura.ai</a>, strutturato per essere consumato da AI design agents come <strong>Claude Design</strong> (<code>claude.ai/design</code>), Google Stitch e simili.
</p>

---

## Cosa c'è dentro

```
.
├── DESIGN.md              ← Documento principale. È il file che gli AI design agents leggono.
├── FormaFuturaLogo.svg    ← Logo ufficiale (SVG, scalabile).
├── tokens/
│   ├── tokens.json        ← Tokens Studio format (per plugin Figma)
│   └── tokens.w3c.json    ← W3C Design Tokens Format (standard universale)
├── preview/
│   └── index.html         ← Documentazione visiva. Aprila in browser.
└── README.md
```

## Logo

Asset ufficiale: [`FormaFuturaLogo.svg`](./FormaFuturaLogo.svg)

**URL diretto da usare in `<img>`, fetch, o nei prompt verso AI agents:**
```
https://raw.githubusercontent.com/LucaLisci/formafutura-design-system/main/FormaFuturaLogo.svg
```

Per le regole d'uso (clear-space, dimensioni minime, varianti, do/don't) vedi [`DESIGN.md` § 2 — Logo & assets](./DESIGN.md#2-logo--assets).

## Come usarla con Claude Design

1. Apri [claude.ai/design](https://claude.ai/design)
2. Crea un nuovo progetto
3. Nel prompt iniziale incolla:

   > "Usa il design system descritto in https://github.com/LucaLisci/formafutura-design-system/blob/main/DESIGN.md come riferimento per tutto ciò che generi. Per ogni layout con header, footer o pagina branded, embedda il logo SVG da https://raw.githubusercontent.com/LucaLisci/formafutura-design-system/main/FormaFuturaLogo.svg come elemento `<img>` — non ricrearlo come testo o forme."

4. Da qui in poi chiedi schermate ("crea una landing page del Coach", "disegna la pagina ESG Decision Lab", ecc.) — userà colori, font, componenti e logo del sistema

> **Tip**: per risparmiare token, riferisciti al `DESIGN.md` per nome invece di reincollarlo a ogni iterazione.

## Come usarla con Figma

Installa il plugin gratuito **[Tokens Studio for Figma](https://tokens.studio/)**, poi:

1. Plugin → Tokens Studio → Settings → **Load from file**
2. Seleziona [`tokens/tokens.json`](./tokens/tokens.json)
3. Tab Tokens → **Create styles** → genera automaticamente tutti i color/text/effect styles in Figma
4. Trascina il file `FormaFuturaLogo.svg` direttamente nel tuo file Figma per usarlo come componente master

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

I marchi *Forma Futura*, *NODO™* e il logo Forma Futura appartengono a Forma Futura. I font referenziati (Fraunces, Inter, JetBrains Mono) sono distribuiti con licenza [SIL OFL](https://scripts.sil.org/OFL).
