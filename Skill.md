---
name: ui-design-engineering
description: Use this skill whenever the user asks to design, build, redesign, or critique any user interface — web pages, app screens, components, dashboards, forms, landing pages, design systems, or style guides — including requests for production-ready HTML/CSS/Tailwind/React UI code, color palettes, typography scales, spacing/layout systems, motion and micro-interaction specs, or accessibility audits. Also trigger on requests to review a screenshot or existing design, explain why an interface feels cluttered, clunky, unbalanced, or unprofessional, or improve visual hierarchy, readability, or usability — even when the user never says the word "design" (e.g. "make this page look better," "build me a pricing page," "why does this form feel off," "review my app screenshot," "clean up this dashboard," "give this landing page more polish").
---

# UI Design Engineering

Treat interface design as applied science, not taste. Every spacing value, color, and animation timing should trace back to a principle below — cognitive psychology, optical physics, or a mathematical ratio — rather than being eyeballed. That's what separates "make it look nice" from engineering an interface, and it's what this skill is for.

## Workflow

Work through these in order for any design, build, or critique request. Skip steps that plainly don't apply (e.g. a critique request has no code-generation step), but don't skip straight to visuals — hierarchy and flow decisions made first prevent rework later.

1. **Contextual analysis** — Name the assumed audience, platform (web / iOS / Android / desktop), and the main cognitive friction point in the request. A pricing page for enterprise buyers and one for a mobile game have different friction points; say which one you're solving before designing anything.
2. **Structural blueprint** — Decide the layout grid, information hierarchy, and user flow *before* discussing colors or fonts. A well-sequenced flow with plain styling beats a beautifully styled flow that asks for the wrong things in the wrong order.
3. **Visual engineering** — Apply the numeric systems below deliberately: 8pt spacing, a modular type scale, HSL/OKLCH color tokens. Arbitrary values (a random `17px` margin, a hand-picked hex) are the most common source of interfaces that feel subtly "off" without anyone being able to say why.
4. **Code generation** (if code is requested) — see [Code standards](#code-standards).
5. **Critique** (if reviewing an existing design) — see [Critique framework](#critique-framework).

## Core numeric systems

Use these as defaults rather than inventing numbers per-project. Consistency across a system is what makes components snap into alignment without per-instance tweaking — that's the actual payoff, not aesthetics for their own sake.

### Spacing — 8pt grid
Every margin, padding, gap, width, and height should be a multiple of 8 (4, 8, 16, 24, 32, 48, 64, 96, 128px). Drop to a 4pt increment only for hairline borders, icon-internal padding, and line-height fine-tuning — those genuinely need finer control; everything else doesn't.

### Typography — modular scale
Pick one ratio and derive every size from it instead of choosing sizes ad hoc. 1.250 ("Major Third") is a safe default:
`12px caption → 16px body → 20px H4 → 25px H3 → 31px H2 → 39px H1`

- **Measure**: 45–75 characters per line (`max-width: min(100%, 65ch)`). Beyond that, eyes lose their place on the wrap.
- **Leading**: 1.5–1.6 for body/long-form, 1.1–1.2 for headings, 1.2 for dense data tables (scannability over comfort there).
- **Tracking**: tighten −0.02 to −0.05em on large headings; loosen +0.05em on all-caps labels (all-caps loses word-shape cues, so it needs the extra room to stay legible).
- **Contrast**: 4.5:1 minimum (WCAG AA), 7:1 for AAA. Avoid pure `#000000` on pure `#FFFFFF` — the stark edge causes halation/eye strain; prefer off-black `#1A1A1A` on off-white `#FAFAFA`.

### Color — functional, not decorative
- Define colors in **HSL or OKLCH**, never raw hex as the source of truth. This is what lets a hover state be "base color +5% lightness" instead of a hand-picked new hex that may drift from the palette. OKLCH is worth the extra step when perceptual uniformity matters (e.g. a lightness ramp that shouldn't shift hue as it goes).
- **60/30/10**: 60% neutral background, 30% secondary/brand color, 10% accent. Reserve the accent exclusively for interactive/actionable elements — an accent color on decorative elements teaches users to ignore it where it matters (this is the Von Restorff effect working against you).
- **Dark mode is not inverted light mode.** Shadows need to get *lighter*, not stay dark, because dark surfaces don't read depth the same way light ones do. Desaturate saturated brand colors by 20–30% or they visually vibrate against a dark background.

### Motion
- Micro-interactions: 150–250ms. View/page transitions: 300–500ms. Past ~500ms, motion reads as sluggish rather than smooth.
- `ease-out` for elements entering the screen, `ease-in` for elements leaving — nothing in the physical world moves at constant (linear) speed, and linear motion is what reads as "robotic" to users even when they can't articulate why.
- Wrap non-essential motion in `@media (prefers-reduced-motion: reduce)` — this isn't optional polish, it's what keeps the interface usable for people with vestibular disorders.

### Interactive states
Define all six for every interactive element — missing one is a common source of interfaces that feel unfinished or untrustworthy:

| State | Treatment |
|---|---|
| Default | Resting visual |
| Hover | Subtle feedback: +5% brightness or −2px translate |
| Focus | **Mandatory** for keyboard users — 2–3px visible outline, `outline-offset: 2px`. Never remove an outline without replacing it with something equally visible. |
| Active/Pressed | `transform: scale(0.98)` |
| Disabled | 40–50% opacity, `pointer-events: none` — should look "dead" but the shape must still be identifiable |
| Loading | Prefer skeleton screens (shimmering placeholders matching the incoming layout) over spinners — they hold the layout shape and prevent Cumulative Layout Shift |

### Accessibility non-negotiables
- **Semantic HTML first**: `button`, `nav`, `main`, `article`, `dialog` — screen readers navigate the DOM structure, not the visual layout, so a `div` styled to look like a button is invisible to them as a button. Use ARIA only to fill gaps semantic HTML genuinely can't cover; unnecessary ARIA is worse than none.
- **Touch targets**: minimum 44×44 CSS px — this is sized for a thumb, not a cursor.
- **Never encode meaning in color alone.** A red/green colorblind user needs a success/error state to still be legible — pair color with an icon or text label.

For the fuller WCAG-level checklist, see `references/accessibility.md`.

## Code standards

When generating HTML/CSS/Tailwind/React:
- Production-ready, not a sketch: semantic HTML, CSS custom properties for every token (spacing, color, radius, shadow) rather than hard-coded values scattered through the markup.
- Every interactive element implements all six states above, including `:focus-visible`.
- Responsive from 320px to 2560px; handle mouse, touch, and keyboard input simultaneously — don't assume one input method.
- Zero Cumulative Layout Shift: reserve space for images/async content, use skeletons rather than pop-in.
- For platform-native conventions (Apple HIG, Material Design 3, Fluent, generic responsive web), see `references/platforms.md` before assuming generic web patterns are the right fit — a request for an iOS screen shouldn't get Material Design elevation shadows.

## Critique framework

Don't evaluate on taste ("this looks clean" / "this feels busy"). Evaluate through four lenses and name the specific principle behind each observation — this is what makes a critique actionable instead of a matter of opinion the user has to just trust:

1. **Cognitive load** — Hick's Law (too many simultaneous choices), Miller's Law (ungrouped fields exceeding ~7 items)
2. **Visual hierarchy** — Von Restorff effect (is anything actually isolated as the primary action, or is everything emphasized equally?), Serial Position effect (are the most important items at the start/end of a sequence?)
3. **Spatial mathematics** — 8pt grid violations, measure (line-length) violations, inconsistent modular-scale steps
4. **Accessibility** — contrast ratios, touch target size, color-only state encoding, missing focus states

Match this standard rather than a vague compliment: *"The 16px gap between the header and body groups them as one region by proximity, but the 95-character line length exceeds the 75-character readability ceiling and should be constrained with `max-width: 65ch`."*

## Going deeper

This file covers what's needed for most design, build, and critique requests. Read a reference file when the request specifically calls for that depth — most tasks only need what's above:

- `references/cognitive-and-gestalt.md` — the psychology behind layout decisions (Fitts's, Hick's, Miller's, and Jakob's laws; Von Restorff and Serial Position effects; the five Gestalt laws of visual perception). Read this when the user asks *why* a layout choice works, is choosing between competing layouts, or wants the reasoning spelled out rather than just the recommendation.
- `references/typography-and-color.md` — optical vs. mathematical alignment (why a centered triangle needs nudging), icon stroke-weight parity, the full OKLCH/dark-mode color engineering detail.
- `references/motion-interaction.md` — the twelve animation principles (anticipation, follow-through, staging, squash & stretch, etc.) for richer or more expressive motion design than the quick-reference timings above.
- `references/platforms.md` — Apple HIG, Material Design 3, and Fluent Design conventions in depth, for when a request is platform-specific rather than generic web.
- `references/accessibility.md` — the fuller accessibility checklist beyond the non-negotiables above, for accessibility-audit requests specifically.
