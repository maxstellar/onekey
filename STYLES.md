# onekey — reusable styles reference

A quick index of the reusable classes and design tokens in [styles.css](styles.css). When adding new UI, reach for these before writing one-off rules.

## Design tokens (`:root` CSS variables)

| Token | Value | Purpose |
|---|---|---|
| `--color-text` | `black` | Primary text / borders / fill |
| `--color-text-soft` | `#282828` | Hover / muted text |
| `--color-bg` | `white` | Default surface |
| `--color-bg-soft` | `whitesmoke` | Alt section / footer background |
| `--radius-pill` | `9999px` | Buttons, inputs |
| `--radius-card` | `1rem` | Cards |
| `--border-width` | `0.25rem` | All outlined elements |
| `--transition-fast` | `0.1s linear` | Base button/link hover |
| `--transition-med` | `0.2s linear` | Nav fill transitions |

## Shape / size

- **`button` / `.button` / `.input`** — pill shape: `border-radius: 9999px`, padding `1.25rem`, font-size `1.25rem`, Phantom Sans. Use on any button, link-as-button, or pill input.

## Border / fill

- **`.dotted`** — always-dotted black border. Typically combined with `.input`.
- **`.bdotted`** — outlined element: solid black border + white background; turns **dotted** on hover. Used for nav buttons and cards.
- **`.filled`** — solid black background, white text, bold; hover dims to `--color-text-soft`. Drop on any button for a primary action.

## Containers

- **`.card`** — `border-radius: 1rem`, white background, `1rem` padding. Combine with `.bdotted` for a bordered card, and a width modifier (`.famex`, `.faqbox`, `.faqwidebox`) for layout-specific sizing.
- **`.boxes`** — flex row with `1rem` gap; wraps card groups.
- **`.youmortalscantcontainme`** — full-viewport-width centered flex row; top-level page section wrapper.
- **`.centertext`** — 40vw centered text column with `2rem` padding; inner content wrapper of a section.

## Typography

- **`.sectionhead`** — large (`4rem`) section title.
- **`.smallhead`** — `1.3rem` subhead with letter-spacing + `3rem` top margin.
- **`.smallheadnm`** — same as `.smallhead` but **n**o **m**argin.
- **`.tagline`** — `2rem` left-aligned hero tagline.
- **`.ysws`** — slightly bumped body text (`1.13rem`) for the "you ship / we ship" line.

## Layout utilities

- **`.mt`** — `margin-top: 15rem` for large vertical section separation.
- **`.cheesecenter`** — `text-align: center` wrapper.

## Nav-specific

- **`.nav`** — compact nav button: reduced padding/font-size, flex-centers icon + label with `0.5rem` gap, transitions `background-color`/`color`/`border-color`.
- **`.nav-active`** — current-section state: black fill, white text, black border, icon inverted via `filter`. Toggled by the IntersectionObserver in [index.html](index.html).

## Typical combinations

| Element | Classes |
|---|---|
| Nav button | `bdotted nav` |
| Primary button (RSVP) | `filled` |
| Pill input with dotted border | `input dotted` |
| Example card | `card famex bdotted` |
| FAQ card | `card faqbox bdotted` |
| Wide FAQ card | `card faqwidebox bdotted` |
| Top-level section | `youmortalscantcontainme` (+ `mt` for spacing) |
