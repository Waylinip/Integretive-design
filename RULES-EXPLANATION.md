# Autism-Friendly Web Design: Rules Followed vs. Rules Broken

## ✅ AUTISM-FRIENDLY WEBSITE — Rules Followed

| # | Rule | How it was applied |
|---|------|--------------------|
| 1 | **Skip-to-content link** | A visually hidden `<a href="#main">Skip to main content</a>` appears on focus — lets keyboard/screen-reader users bypass the nav instantly |
| 2 | **Persistent, predictable navigation** | The header and nav are sticky; they stay in the same place on every scroll. Links use `aria-current="page"` to show where you are |
| 3 | **Descriptive link text** | Every link says exactly what it does: "Send an email to Calm Corner", not "click here" |
| 4 | **Calm colour palette** | Muted cream `#F7F4EF`, warm tan, and a single soft teal accent `#4A7C6F`. No pure red/green/blue, no neon, no jarring hue shifts |
| 5 | **Plain language** | Short sentences (≤ 3–4 per paragraph), active voice, no idioms or figures of speech, no sarcasm |
| 6 | **No auto-playing media** | No audio, video, or GIFs start automatically. `prefers-reduced-motion` is respected — animations are off by default |
| 7 | **Large, readable typography** | `Lexend` and `Atkinson Hyperlegible` — both designed specifically for low-literacy and dyslexic readers. Base size 1.125 rem, line-height 1.8 |
| 8 | **Generous white space** | Cards are well-padded; paragraphs are capped at 65 characters wide (`max-width: 65ch`); sections breathe with 2.5 rem gaps |
| 9 | **Explicit focus styles** | `focus-visible` gives a 3px blue ring with 4px offset on every interactive element — never hidden |
| 10 | **One focus per section** | Each section has a single heading, a single purpose, and a single action. No competing CTAs |
| 11 | **Consistent layout** | Header → Nav → Hero → Cards → Reading → Tips → CTA → Footer. Same every time. No surprise changes |
| 12 | **Numbered lists for sequences** | Tips use visible numbered badges so the order is unambiguous, even without CSS |
| 13 | **WCAG 2.1 AA contrast** | All text/background pairs exceed 4.5:1 contrast ratio |
| 14 | **No pop-ups or modals** | Nothing appears unexpectedly. The page is the page |
| 15 | **Semantic HTML** | `<header>`, `<nav>`, `<main>`, `<article>`, `<section>`, `<footer>` — full landmark structure for screen readers |

---

## ❌ CHAOS WEBSITE — Rules Broken

| # | Rule Broken | How it was broken |
|---|-------------|-------------------|
| 1 | **Flashing background** | `animation: seizure 0.5s infinite` cycles through 10 saturated hues — violates WCAG 2.3.1 (Three Flashes). This can trigger photosensitive seizures |
| 2 | **Constant movement** | Every element has a `bounce`, `spin`, `shake`, or `zoom` animation. Nothing is ever still. Extremely distressing for autistic users |
| 3 | **No skip link** | Keyboard users must tab through every nav link every time. No escape route |
| 4 | **Immediate pop-up** | A full-screen modal fires on page load, covering content. The close button is 0.5 rem, nearly invisible, and has `aria-label="."` |
| 5 | **Deceptive buttons** | The "No" button is labelled `DEFINITELY NO PRIZE (yes)` — exploits trust and is confusing for literal thinkers |
| 6 | **Auto-playing audio** | Simulated with an always-on banner; in a real deployment the `<audio autoplay>` attribute would blast music immediately |
| 7 | **Scrolling marquee** | Continuous horizontal ticker text — the `<marquee>` element was deprecated in HTML5 specifically because of accessibility harm |
| 8 | **Illegible header** | The `<h1>` uses deliberate leet-speak (`WELC0ME`), four conflicting animations, and a colour that clashes with the flashing background |
| 9 | **Vague link text** | All nav links say "click here". Screen reader users hear "link: click here" five times with no context |
| 10 | **No visual hierarchy** | Everything is the same weight — four competing CTAs, all identical, all animating, all screaming |
| 11 | **Wall of text** | Legal-ish copy in 0.65 rem font, `line-height: 1.1`, four columns, `#cccccc` on `#1a1a1a` — borderline illegible |
| 12 | **Images with no alt text** | Three `role="img"` elements with no `aria-label` or one labelled simply `"image"` — completely useless to screen readers |
| 13 | **Full-screen hover tooltip** | Hovering a button triggers an `::after` pseudo-element that covers the entire viewport with red text — impossible to dismiss without moving the mouse |
| 14 | **Invisible form** | Labels are single characters (`e`, `p`). Text colour and background colour are nearly identical. The submit button is invisible |
| 15 | **Undismissable cookie banner** | A full-width fixed banner at the bottom with a flashing background and no close button, reading "No close button. Deal with it." |
| 16 | **Right-click disabled** | `contextmenu` event is blocked — users lose access to browser accessibility features, zoom, and save-page |
| 17 | **Multiple competing CTAs** | Three "Buy" buttons of equal size in one block, two of which say contradictory things — creates decision paralysis |
| 18 | **Non-semantic document** | `<header role="none">`, `<nav aria-label="i dunno lol">` — landmarks are actively broken or mislabelled |
| 19 | **Custom skull cursor** | An SVG 💀 cursor replaces the pointer — disorienting, and some users with motor impairments rely on the system cursor |
| 20 | **Idioms and sarcasm** | "Your computer has 47 viruses!!" and "Accessibility? Never heard of her." — literal thinkers take these at face value |

---


