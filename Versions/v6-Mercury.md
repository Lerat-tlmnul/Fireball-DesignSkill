---
name: v6-mercury
description: UI build and code/reasoning tasks in one model pass with a mandatory rounded Liquid Glass nav, FireBall Logic Core and REI visible stages. Lightest v6 tier, for saving credits. Single verification, at most one repair pass.
---

# v6 Mercury · Light tier

Mercury is the economical v6. One model does the whole job, in one pass, with one optional repair. It keeps the three things that make v6 reliable: the FireBall Logic Core checks, the REI visible stages with a 10-point verification, and the Liquid Glass navigation.

**Credit profile:** lowest. One build, no team, no loop. Expect the first result to be good, not perfect. Mercury tells you honestly what is still open.

## 0. Modes

- **Website or app UI:** follow sections 1 to 6.
- **Code or reasoning task:** follow sections 2, 3, 4 and 5 with the code or reasoning criteria in section 5. Skip section 6 (nav).

## 1. Brief

If subject, audience or tone is missing, ask one question. Never build from nothing. State assumptions in one line.

## 2. REI visible pipeline (shown to the user)

Show each stage with its header:

**[1] Message**: restate the request in one or two sentences. Goal, constraints, assumptions, deliverable, acceptance conditions.

**[2] Analysis**: split into sub-problems. Mark known, unknown, failure points. Do not propose a solution yet.

**[3] Architecture**: choose an approach, justify it against one alternative. Map each sub-problem to a file or section.

**[4] Critique**: find the strongest objection to the architecture. Revise and list each flaw with its fix.

**[5] Verification**: build from the revised architecture, then score (section 5).

## 3. FireBall Logic Core (applies to all code and build work)

- **01 Structure parser.** Identify symbols, types, scopes, dependencies.
- **02 Dependency graph.** Relationships between functions, modules, variables and interfaces. Keep it short: a list is enough.
- **03 Constraint engine.** Check types, invariants, preconditions, postconditions, compatibility.
- **04 Solution selector.** Compare two valid strategies against the requirements; keep the one that fits best and say why.
- **05 Validation gate.** Run every available check: syntax parse, brace balance, undefined names or tokens, file wiring. Reject or revise anything that fails.

**Output contract:** validated output, detected risks, unresolved constraints.

## 4. Build rules (websites)

**Write order, each file once:** `tokens.css`, `base.css`, `nav.css`, `nav.js`, `hero.css`, `sections.css`, `motion.css`, `index.html`, `main.js`.

Every `var(--x)` and class used must be defined. Every file must be linked or loaded from `index.html`.

**Design rules**

- **Fit before style.** The style comes from the brief. No neon, glow, cyan or purple gradients, or dark glass by default.
- **No AI slop.** Two or more signals (glowing dark gradient with glass cards; centered hero plus three cards plus logo cloud plus testimonials; identical cards; emoji icons; hollow marketing words; invented stats) mean rework of layout, type, palette and material.
- **Identity.** One signature move, visible on the first screen, never captioned.
- **Clean output.** No section labels, version stamps, debug panels or design commentary in the shipped code.
- **Type.** Pair fonts for character. Fluid sizes with `clamp()`. 45 to 75 characters per line. Real fallback stacks.
- **Colour.** OKLCH tokens, neutrals tinted toward the brand hue. Dark mode engineered, not inverted. Colour never the only signal. No navy or violet background unless the brief asks.
- **Motion.** 150 to 250ms buttons, 300 to 500ms sections, 500 to 800ms entrances. Animate `transform` and `opacity` only. At least 3 `@keyframes`, at least 4 animated declarations, and a reduced-motion rule.
- **Accessibility (WCAG 2.2 AA).** Contrast 4.5:1 text, 3:1 large text and UI boundaries, on the worst-case backdrop. Real buttons, labelled inputs, ordered headings, `lang`, alt text, visible focus, 44px targets.
- **Writing.** Buttons say what happens. No lorem, no invented testimonials, logos or stats.

## 5. Verification (REI score out of 10)

**Websites and code**

| Criterion | Points | Full credit requires |
|---|---|---|
| Correctness | 3 | Runs or renders without errors. Every requirement met. Edge cases handled. |
| Code quality | 2 | Valid syntax, clear names, no dead code, no duplication, no security issue. |
| Visual quality | 3 | Clear hierarchy, consistent spacing and type, coherent palette, good contrast, not generic. |
| Responsiveness and a11y | 2 | Mobile and desktop widths. Semantic HTML, labelled controls, keyboard navigation. |

**Reasoning**

| Criterion | Points | Full credit requires |
|---|---|---|
| Correctness | 4 | Every fact and calculation checked. Uncertain points flagged and not load-bearing. |
| Completeness | 2 | Every sub-question answered. |
| Constraint compliance | 2 | Format, language, length, scope match the message stage. |
| Clarity | 2 | Easy to follow, no contradiction, no padding. |

**Scoring rules**

- Score each criterion separately, with one line of evidence (the check performed, or the recalculation).
- A check not performed cannot earn points.
- Never inflate. A real defect always costs points.

**Repair policy (Mercury)**

- Score 10: deliver, showing the score.
- Score 9 or lower: run **one** repair pass on the listed defects only, then re-score.
- After the repair, if the score is still below 10, deliver anyway and list the open defects and their points. Never hide them.

## 6. Liquid Glass navigation (mandatory in every website)

- The nav is a rounded pill: `border-radius: var(--radius-full)`.
- At the top of the page only brand, links and button show. The glass surface is hidden (`opacity: 0`) and fades in on scroll.
- Distortion is mandatory. The rim bends the backdrop through an SVG `feDisplacementMap`, built from the nav's own size and radius. Blur alone is not Liquid Glass.
- Chromium applies the full displacement. Other browsers keep blur glass. Text and icons are never filtered.
- Fallbacks: solid surface under `prefers-reduced-transparency` and `forced-colors`, and a visible surface with no JS.
- Presets: Subtle (scale 22, strength 0.6, bezel 14, blur 1), Standard (34, 1.0, 18, 2, default), Strong (42, 1.2, 24, 3, calm backdrops only). Never above scale 44.
- Use the `nav.css` and `liquidGlass()` code of the v5.6 Liquid Glass skill, section 5, verbatim. Do not rewrite the refraction.

Checks: `nav.js` contains `feDisplacementMap`; the nav is visible when scrolled and hidden at top; contrast passes on the worst-case backdrop.

## 7. Output contract

Return:

1. The validated output (files or text).
2. The REI score with each criterion and its evidence.
3. Detected risks.
4. Unresolved constraints and open defects, with points lost.

Keep the visible stages brief. The result is what matters.
