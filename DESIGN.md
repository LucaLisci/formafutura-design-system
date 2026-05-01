# Forma Futura — Design System

> AI Transformation Studio. Italian design sensibility, dark-first editorial aesthetic, single electric accent.
> Source: [formafutura.ai](https://www.formafutura.ai)
> Repo: [github.com/LucaLisci/formafutura-design-system](https://github.com/LucaLisci/formafutura-design-system)

---

## 1. Brand & Voice

**What it is**: Forma Futura is an AI consulting studio for organizations. The methodology is called NODO™ — find the smallest unit of work where friction emerges, intervene there, integrate AI, stabilize, scale.

**Personality**: Confident but humble. Editorial, not corporate. Italian sensibility — restraint, craft, intentional whitespace. Anti-hype: refuses generic "AI consulting" tropes (no purple gradients, no swoopy abstract shapes, no robot iconography).

**Tone of voice**:
- Direct: "Si discute, non si decide."
- Concrete over visionary: "Il cambiamento si costruisce dal basso."
- Honest framing: "Forma Futura seleziona le organizzazioni con cui lavora."
- Italics for the human pivot word in headlines (e.g., "Allena la tua *organizzazione* a lavorare meglio.")

**Anti-patterns to avoid**:
- ❌ Purple/blue tech gradients
- ❌ Glassmorphism, neon glow chrome
- ❌ Stock 3D abstract renders
- ❌ Inter or Roboto for display typography
- ❌ Rounded "friendly SaaS" iconography

---

## 2. Logo & assets

The official Forma Futura logo is an **SVG** hosted in this repo:

| Asset | Path | Direct URL (use this in `<img>` / `fetch`) |
|---|---|---|
| Primary logo | `FormaFuturaLogo.svg` | `https://raw.githubusercontent.com/LucaLisci/formafutura-design-system/main/FormaFuturaLogo.svg` |

### Usage rules

**DO**
- ✅ Always use the **SVG file** directly via the raw URL above. Never recreate the logo as text or rebuild it from shapes.
- ✅ Default placement: `brand.ink` (#0A0A0A) background. The logo is designed for dark mode.
- ✅ Maintain clear-space equal to the cap-height of the wordmark on all four sides.
- ✅ Minimum size: **24px height** in UI (header / footer), **80px+** in hero or print contexts.
- ✅ When inverting on a `brand.bone` (#F4F1EC) background is required, request the dark variant instead of recoloring.

**DON'T**
- ❌ Do not stretch, skew, rotate, or distort.
- ❌ Do not recolor unless explicitly using the documented inverse variant.
- ❌ Do not apply effects (drop shadow, glow, outline, gradient overlay).
- ❌ Do not place over photography or busy backgrounds without a solid color underlay.
- ❌ Do not embed as raster (`.png`) — the SVG scales perfectly at any resolution.

### Embedding examples

**HTML / web:**
```html
<img
  src="https://raw.githubusercontent.com/LucaLisci/formafutura-design-system/main/FormaFuturaLogo.svg"
  alt="Forma Futura"
  height="32"
/>
```

**React / JSX:**
```jsx
<img
  src="https://raw.githubusercontent.com/LucaLisci/formafutura-design-system/main/FormaFuturaLogo.svg"
  alt="Forma Futura"
  className="h-8 w-auto"
/>
```

**Markdown:**
```markdown
![Forma Futura](https://raw.githubusercontent.com/LucaLisci/formafutura-design-system/main/FormaFuturaLogo.svg)
```

> 📌 **Instruction for AI design agents (Claude Design, Stitch, etc.)**: when generating any layout that contains a navigation header, footer, splash screen, or branded surface, **embed the SVG file from the URL above** as an `<img>` element. **Do not recreate the logo as text styled with a font, and do not approximate it with shapes.**

---

## 3. Color

**Philosophy**: Quasi-monochrome dark base + one electric accent + one warm bone for inverse sections. Color is **scarce on purpose** — when something is colored, it matters.

### Brand
| Token | Hex | Use |
|---|---|---|
| `brand.ink` | `#0A0A0A` | Primary background. Almost-black, never pure `#000`. |
| `brand.bone` | `#F4F1EC` | Primary text on dark. Inverse section backgrounds. Warm, never `#FFF`. |
| `brand.accent` | `#C8FF00` | Lime electric. CTA, NODO™ wordmark, focus, hover, active state. **Use sparingly** — max 1 element per viewport. |
| `brand.accent-soft` | `#E6FF80` | Hover state for primary buttons only. |

### Neutrals (dark-first 10-step ramp)
`neutral.900` `#0A0A0A` · `800` `#161616` · `700` `#262626` · `600` `#3D3D3D` · `500` `#6B6B6B` · `400` `#9C9C9C` · `300` `#C9C5BE` · `200` `#E4E0D9` · `100` `#F4F1EC` · `050` `#FAF8F4`

### Semantic
`success` `#4ADE80` · `warning` `#FBBF24` · `danger` `#F87171` · `info` `#60A5FA`

### Usage rules
- Default surface = `brand.ink`. Cards = `neutral.800`. Modals = `neutral.700`.
- Primary text = `brand.bone`. Secondary = `neutral.300`. Muted = `neutral.400`.
- Borders are subtle: `neutral.700` for dividers, `neutral.600` for inputs.
- **Never** use the accent for body text or large surfaces — it's a pointer, not paint.

---

## 4. Typography

**Pairing**: A characterful serif for display + a neutral premium sans for body + monospace for technical labels.

| Family | Use | Weights |
|---|---|---|
| **Fraunces** (Google Fonts) | All headlines, display, key inline emphasis (italic) | 400 regular, 400 italic |
| **Inter** (Google Fonts) | Body, UI, buttons | 400, 500, 600 |
| **JetBrains Mono** (Google Fonts) | Eyebrow labels, step numbers, technical metadata | 400, 500 |

> Production option: swap Fraunces → custom italic serif if budget allows. Swap Inter → Söhne (Klim) for more refinement.

### Type scale
| Style | Family / Weight | Size / Line / Tracking | Use |
|---|---|---|---|
| `display-xl` | Fraunces 400 | 96 / 100 / -4% | Hero headline only |
| `display-lg` | Fraunces 400 | 72 / 76 / -2% | Section opener |
| `h1` | Fraunces 400 | 56 / 67 / -2% | Major section title |
| `h2` | Fraunces 400 | 40 / 48 / -2% | Sub-section |
| `h3` | Inter 500 | 24 / 29 / -2% | Card title |
| `h4` | Inter 500 | 20 / 24 / 0 | Component title |
| `body-lg` | Inter 400 | 20 / 34 / 0 | Lead paragraph under hero |
| `body` | Inter 400 | 16 / 27 / 0 | Default paragraph |
| `body-sm` | Inter 400 | 14 / 21 / 0 | Captions, secondary |
| `label` | JetBrains Mono 500 | 12 / 18 / +12% UPPERCASE | Section eyebrow ("IL PROBLEMA"), step numbers |
| `caption` | Inter 400 | 12 / 18 / +4% | Footer, legal |

### Typographic rules
- Headlines: **always Fraunces**, weight 400 only. Never bold a serif headline.
- One italic word per major headline maximum — pick the word that carries the human shift ("organizzazione", "Futura", "NODO").
- Mono labels are **always uppercase**, always tracked +12%, always small (12px).
- Body line-height is generous (1.7) — this is editorial, not dashboard.

---

## 5. Spacing

8-point base scale (with 4 as half-step):
`4 · 8 · 12 · 16 · 24 · 32 · 48 · 64 · 96 · 128 · 160 · 200`

**Section rhythm**: vertical padding between major sections is **96px** (mobile) → **160px** (desktop). Sections breathe.

**Card internal padding**: 32px. Button padding: 14px vertical / 24px horizontal.

---

## 6. Layout

- **Container max-width**: `1280px`. Narrow text-focused content: `720px`.
- **Grid**: 12 columns, 24px gutters, 48px outer margin (desktop).
- **Breakpoints**: `sm 640` · `md 768` · `lg 1024` · `xl 1280`.
- **Composition principle**: asymmetric. Hero text occupies left 7 cols, image bleeds right. Section headers offset from body. **Never center-everything.**

---

## 7. Border radius

`none 0` · `sm 4px` · `md 8px` (inputs) · `lg 16px` (cards) · `xl 24px` (large surfaces) · `pill 999px` (buttons, tags)

> Buttons are **always pill**. Cards are **always 16px or 24px**, never sharp.

---

## 8. Elevation / Shadow

Dark mode means shadows are subtle and warm — they suggest depth, not float.

| Token | Value | Use |
|---|---|---|
| `shadow.sm` | `0 1px 2px rgba(0,0,0,0.20)` | Subtle separation |
| `shadow.md` | `0 4px 12px rgba(0,0,0,0.30)` | Cards, dropdowns |
| `shadow.lg` | `0 12px 32px rgba(0,0,0,0.40)` | Modals |
| `shadow.glow-accent` | `0 0 40px rgba(200,255,0,0.25)` | **Reserved**: only on the active step in the NODO process visualization, or on focused primary CTA |

---

## 9. Motion

**Philosophy**: motion is editorial — long fades and slow staggered reveals beat snappy bouncy spring animations. The site should feel like *reading*, not *swiping*.

| Token | Duration | Curve | Use |
|---|---|---|---|
| `motion.fast` | 150ms | standard | Hover color change |
| `motion.base` | 250ms | standard | Button transform, focus ring |
| `motion.slow` | 400ms | entrance | Card reveal, accordion |
| `motion.slower` | 700ms | entrance | Section enter on scroll |

Easings: `standard cubic-bezier(0.2, 0, 0, 1)` · `entrance cubic-bezier(0, 0, 0.2, 1)` · `exit cubic-bezier(0.4, 0, 1, 1)`.

**Hero entry**: stagger reveal — eyebrow (0ms) → headline (100ms) → subhead (250ms) → CTA (400ms). Each slides up 16px while fading in.

---

## 10. Components

### Button
- **Primary**: bg `accent`, text `ink`, pill, 14×24 padding, weight 500 size 15. Hover → `accent-soft` + `translateY(-1px)`.
- **Secondary**: transparent bg, text `bone`, border `neutral.400`. Hover → border `bone`.
- **Ghost**: transparent, text `bone`, no border, trailing `→` arrow that translates 4px right on hover. Used for inline links like "Conosci i nostri coach".

### Tag / Badge
Pill shape, 6×12 padding, JetBrains Mono 11px uppercase +8% tracking.
- **Accent**: bg `accent`, text `ink` — for "NODO™" only
- **Default**: bg `neutral.700`, text `bone`
- **Outline**: transparent, border `neutral.500`

### Card
Background `neutral.800` or `neutral.900`, border 1px `neutral.700`, radius 16px, padding 32px. Step cards have a small mono number on top in `accent` color (e.g., `02`), then h4 title, then 14px body-sm in `neutral.300`.

### Step indicator (used in NODO methodology section)
48px circle. Inactive: transparent bg, 1px `neutral.500` border, mono number 14px. Active: `accent` bg, `ink` text. Used as a horizontal sequence 1→6.

### Input
Background `neutral.900`, border 1px `neutral.600`, radius 8px, padding 14×16, Inter 15px. Focus → border `accent`, no glow box-shadow.

### Top navigation
Horizontal flex, gap 24px. **Logo on the far left** (height 32px, embedded from `FormaFuturaLogo.svg` — see section 2). Plain text links in `bone`, hover → `accent`. CTA on right is primary pill button. No underlines, no boxes around active item — current page is bold weight 600, that's it.

### Footer
Logo (height 24-28px) on the left or top. Right or below: minimal links (Contatto, Privacy) in `body-sm` `neutral.400`. Copyright line in `caption`. Background `brand.ink`, top border 1px `neutral.700`.

---

## 11. Iconography & Imagery

- **Icons**: stroke-based, 1.5px stroke, 24×24 viewbox. Use Lucide or Phosphor (regular weight). **No filled icons**, no gradient icons, no 3D.
- **Photography**: editorial — desaturated, warm grain, mid-shot of people in real workspaces. Avoid stock corporate handshakes. The `000.png` and `001.png` referenced on the site are abstract organic compositions in muted earth tones.
- **Logos in client showcase** are always rendered in `bone` monochrome on `ink` background — never in their original colors. Forces visual coherence.

---

## 12. Section patterns

The site is built from a small set of repeating section templates:

1. **Hero**: full-viewport, eyebrow label + giant Fraunces headline (with one italic word) + lead paragraph + ghost-link CTA. Logo top-left in nav.
2. **Eyebrow + headline + 4-card grid**: used for "Il problema" and similar diagnostic sections.
3. **Numbered step sequence**: 1→6 horizontal step indicators above explanatory cards. Used for NODO methodology and process.
4. **3-column offering grid**: equal cards, each with a heading, sub-label, paragraph, bulleted feature list.
5. **Logo showcase**: monochrome client logos on dark, single row or wrap, generous spacing.
6. **CTA close**: short headline + 1-line subtext + primary button + tiny qualifier ("posti limitati").

---

## 13. Voice in UI copy

- Buttons: imperative verbs in Italian. "Prenota una call", "Come funziona", "Conosci i nostri coach". **Never** generic "Learn more" / "Get started".
- Empty states: honest. "Nessun nodo ancora identificato." not "Nothing here yet 🌱".
- Errors: technical and calm. "Email non valida." not "Oops! Something went wrong."

---

## License & attribution

This `DESIGN.md` describes a design system inspired by publicly visible patterns on formafutura.ai. It is intended for use with AI design agents (Claude Design, Stitch, etc.) to generate UI consistent with the Forma Futura aesthetic.

Trademarks "Forma Futura", "NODO™" and the Forma Futura logo belong to Forma Futura. Fonts referenced are SIL OFL licensed (Fraunces, Inter, JetBrains Mono).
