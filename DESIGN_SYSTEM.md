# KodNest Premium Build System

A premium SaaS design system for B2C product experiences. Calm, intentional, coherent, confident.

---

## Design philosophy

- **Calm** — No gradients, glassmorphism, neon, or animation noise.
- **Intentional** — Every color, space, and transition has a reason.
- **Coherent** — One visual language across all surfaces.
- **Confident** — Serif headlines, clear hierarchy, generous whitespace.

---

## Color system (max 4 in use)

| Token | Value | Use |
|-------|--------|-----|
| `--color-bg` | `#F7F6F3` | Background (off-white) |
| `--color-text` | `#111111` | Primary text |
| `--color-accent` | `#8B0000` | Primary actions, links, focus |
| `--color-success` | `#4a5d4a` | Success states, shipped |
| `--color-warning` | `#7a6b4a` | In progress, warnings |

Use only these. No extra palette colors.

---

## Typography

- **Headings:** Serif (`Georgia`), large, confident, generous spacing. Use `h1` / `.h1`, `h2` / `.h2`.
- **Body:** Sans-serif (`Inter`), 16–18px, line-height 1.6–1.8. Use `.text-block` for max-width 720px.
- **Caption:** 14px, line-height 1.5. Use `.subtext`, `.panel__title`.
- No decorative fonts. No random sizes.

---

## Spacing scale

Use **only** these values: `8px`, `16px`, `24px`, `40px`, `64px`.

| Token | Value |
|-------|--------|
| `--space-1` | 8px |
| `--space-2` | 16px |
| `--space-3` | 24px |
| `--space-4` | 40px |
| `--space-5` | 64px |

Never use 13px, 27px, or other ad-hoc spacing. Whitespace is part of the design.

---

## Global layout structure

Every page follows this order:

1. **Top Bar** — Left: project name. Center: progress (Step X / Y). Right: status badge (Not Started / In Progress / Shipped).
2. **Context Header** — One large serif headline, one-line subtext. Clear purpose. No hype.
3. **Primary Workspace (70%)** — Main product interaction. Clean cards, predictable components.
4. **Secondary Panel (30%)** — Step explanation, copyable prompt box, actions: Copy, Build in Lovable, It Worked, Error, Add Screenshot.
5. **Proof Footer** — Persistent checklist: □ UI Built □ Logic Working □ Test Passed □ Deployed. Each requires user proof.

Classes: `.layout`, `.layout__topbar`, `.layout__context-header`, `.layout__main`, `.layout__workspace`, `.layout__panel`, `.layout__proof-footer`.

---

## Components

### Buttons

- **Primary:** `.btn .btn--primary` — Solid deep red. Use for one main action per context.
- **Secondary:** `.btn .btn--secondary` — Outlined. Same border radius and hover behavior.

Same hover (180ms ease-in-out) and radius everywhere.

### Inputs

- `.input` — Clean border, no heavy shadow. Clear focus state (accent outline).

### Cards

- `.card` — Subtle border, no drop shadow. Padding from spacing scale (e.g. `--space-3`). Use `.card--elevated` for more padding.

### Badges

- `.badge` — Base.
- `.badge--not-started` | `.badge--in-progress` | `.badge--shipped` — Status variants.

### Prompt box (secondary panel)

- `.prompt-box` — Container.
- `.prompt-box__actions` — Wrapper for Copy, Build in Lovable, etc.

### Error & empty states

- `.state-message` — Container.
- `.state-message--error` — Explain what went wrong and how to fix. Never blame the user.
- `.state-message--empty` — Next action only. Never feel dead.
- Use `.state-message__title`, `.state-message__body`, `.state-message__action`.

---

## Interaction

- **Transitions:** 150–200ms, ease-in-out. No bounce, no parallax.
- Token: `--transition-duration: 180ms`, `--transition-ease: ease-in-out`.

---

## File structure

```
kodnest-design-system/
├── index.css      ← Entry: import this
├── tokens.css     ← Colors, type, spacing, radii, transitions
├── base.css       ← Reset, typography, focus
├── components.css ← Buttons, inputs, cards, badges, prompt box, proof item, states
├── layout.css     ← Top bar, context header, workspace, panel, proof footer
└── DESIGN_SYSTEM.md
```

---

## Usage

```html
<link rel="stylesheet" href="index.css" />
```

Then use the layout and component classes as documented. Do not add product features in the design system layer; keep it visual and structural only.

---

*KodNest Premium Build System — one mind, no drift.*
