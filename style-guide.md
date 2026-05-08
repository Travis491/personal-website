# Style Guide — Travis Kim Personal Site
*Extracted from ThetaWave AI inspiration*

---

## 1. Design Philosophy

Light, airy, and quietly confident. Space does the work — not decoration. The palette is almost white with soft lavender undertones, punctuated by a single bold purple-to-pink gradient that draws the eye. Everything feels modern, calm, and intelligent. Think: a product you trust before you've even clicked anything.

The site should feel like a breath of fresh air — a deliberate contrast to the loud, dark-mode portfolios everywhere. Warmth comes from subtle gradients and human copy, not color temperature.

---

## 2. Target User & Job-to-be-Done

**User:** A hiring manager, collaborator, or PM peer landing here for the first time.
**Job:** Quickly understand who Travis is, feel confidence in his work, and find a reason to reach out.
**Tone:** Smart but accessible. Personal without being casual. Ambitious without being self-promotional.

---

## 3. Layout, Grid & Spacing

- **Max content width:** 960px, centered
- **Page padding:** 2.5rem horizontal on desktop, 1.25rem on mobile
- **Section padding:** 6–8rem vertical
- **Grid:** 12-column conceptually; use auto-fit minmax for card grids
- **Card gap:** 1rem–1.25rem
- **Breathing room is the design:** when in doubt, add more whitespace

**Background texture:** Scattered floating dots (small, ~8–12px, opacity 0.25) in lavender/periwinkle, placed asymmetrically. They create depth without patterns.

---

## 4. Typography Standards

| Role | Family | Weight | Size |
|------|--------|--------|------|
| Display / Hero | Fraunces (serif) | 700 | clamp(4rem, 10vw, 8rem) |
| Section Title | Fraunces (serif) | 600 | clamp(2rem, 4vw, 3rem) |
| Body | Inter or DM Sans | 400 | 1rem–1.05rem |
| Caption / Label | Inter | 500 | 0.72–0.78rem |
| Nav | Inter | 500 | 0.82rem |
| CTA Button | Inter | 600 | 0.9rem |

- Line height: 1.6–1.75 for body; 1.0–1.1 for display
- Letter spacing: 0.02em body; 0.12–0.18em for all-caps labels
- Brand gradient text: apply pink→purple gradient as text fill on key headline words

---

## 5. Color Palette

```
--bg:             #F4F2F9       /* soft lavender white */
--bg-2:           #EDEAF5       /* slightly deeper lavender for alternate sections */
--surface:        #FFFFFF       /* pure white cards */
--surface-border: rgba(120,100,200,0.10)  /* subtle purple border */

--text:           #1A1730       /* near-black with purple tint */
--text-muted:     #7B7494       /* muted purple-gray */

--accent:         #6B48FF       /* primary purple */
--accent-2:       #C842A0       /* pink/magenta */
--accent-3:       #F5C842       /* golden yellow — for underlines, highlights */

--gradient-brand: linear-gradient(90deg, #C842A0, #6B48FF, #F5C842)
--gradient-glow:  radial-gradient(ellipse at 60% 40%, rgba(180,140,255,0.18) 0%, transparent 65%)

--dot:            rgba(107,72,255,0.18)   /* floating background dots */
```

**States:**
- Button hover: lighten `--accent` by 10%, slight scale(1.02)
- Card hover: translateY(-4px), box-shadow increases, border-color to `rgba(107,72,255,0.2)`
- Link hover: color shifts to `--accent`
- Active nav item: `--accent` with bottom border

---

## 6. Component Variants

### Navigation
- Fixed, white with `backdrop-filter: blur(16px) saturate(160%)`
- Border-bottom: 1px solid `rgba(107,72,255,0.08)`
- Logo: Fraunces italic, `--text`
- Links: small, 0.82rem, `--text-muted`, hover → `--text`
- CTA: pill-shaped button, `--accent` fill, white text, 0.75rem padding vertical

### Hero
- Center-aligned text
- Gradient background glow (radial, centered, lavender)
- Display headline in Fraunces 700; brand-name words get gradient text treatment
- Subheadline in body font, `--text-muted`, max-width 540px
- CTA button: large pill, `--accent`, 1rem font, 1rem vertical padding, 2.5rem horizontal

### Cards (Stat, Portfolio, Principle)
- Background: `--surface` (white)
- Border: 1px solid `--surface-border`
- Border-radius: 16–20px
- Padding: 1.75–2.25rem
- Subtle drop shadow: `0 2px 16px rgba(107,72,255,0.06)`
- Hover: lift + slightly stronger shadow + border brightens

### Section Labels
- All-caps, 0.72rem, `--accent`, letter-spacing 0.16em
- No decoration — just spacing and color

### Buttons
- Primary: `--accent` fill, white text, 8px–12px radius or full pill
- Secondary: transparent, `--accent` border + text
- Hover state: lighten, slight scale

---

## 7. Content Tone & Microcopy

- **Headlines:** Bold, human, slightly unexpected. "More than a job title." stays. Avoid corporate-speak.
- **Body:** First person, conversational, specific. Numbers > vague claims.
- **Labels/eyebrows:** Short phrases, not buzzwords. "Who I am" not "About Me."
- **CTAs:** Action-forward. "See the work" not "View portfolio."
- **Stat cards:** Let the number speak — minimal label, no explanation needed.

---

## 8. Accessibility Requirements

- Minimum contrast ratio 4.5:1 for body text against background
- `--text` (#1A1730) on `--bg` (#F4F2F9): passes AA
- `--text-muted` (#7B7494) on white: passes AA for large text, aim for AA on small text too
- All interactive elements keyboard-focusable with visible focus ring (`outline: 2px solid --accent, offset 2px`)
- Images: alt text required
- Floating decorative dots: `aria-hidden="true"`
- `prefers-reduced-motion`: disable all transitions/animations when set

---

## 9. Do / Don't

| Do | Don't |
|----|-------|
| Use white/lavender backgrounds — let content breathe | Use dark backgrounds (that's the old style) |
| Apply the brand gradient sparingly — headlines only | Gradient everything |
| Use Fraunces for display; Inter/DM Sans for body | Mix more than 2 typeface families |
| Floating dots as accent decoration | Dense background patterns or textures |
| Rounded cards with soft shadow | Sharp-cornered flat cards |
| Purple as the single bold accent | Multiple competing accent colors |
| Center-align hero content | Left-align the hero on desktop |
| Generous section whitespace | Tight, crowded sections |
| Specific numbers and human details in copy | Vague superlatives ("passionate", "driven") |
