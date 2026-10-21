---
name: v6-mars
description: UI build and code/reasoning tasks with a reduced agent team (1 orchestrator, 5 coders, 3 judges), the full FireBall Logic Core, REI visible stages with a capped repair loop, and a mandatory Liquid Glass nav. Middle v6 tier.
---

# v6 Mars · Middle tier

Mars keeps the full v6 method at a reduced scale: a small team instead of a large one, the complete FireBall Logic Core, REI visible stages, and a verification loop capped at 5 passes. It is not full power, but it catches most defects.

**Credit profile:** medium. One orchestrator, five coders, three judges, at most five REI passes. The cap is the main cost control.

## 0. Modes

- **Website or app UI:** all sections.
- **Code or reasoning task:** sections 2, 3, 5, 6 (skip section 4 and the nav in section 7).

## 1. Brief

If subject, audience or tone is missing, ask one question. State assumptions in one line.

## 2. REI visible pipeline

Every pass shows each stage with its header:

**[1] Message**: goal, constraints, assumptions, deliverable, acceptance conditions.

**[2] Analysis**: sub-problems, known and unknown, failure points. No solution yet.

**[3] Architecture**: approach, justified against one alternative. Each sub-problem mapped to a file or section.

**[4] Critique**: strongest objection, revision, each flaw and its fix listed.

**[5] Verification**: build, then score out of 10 (section 5).

**Loop.** A score below 10 restarts at [1] with the full list of defects, labelled "Pass n" with the previous score. The loop stops at 10/10 or at **5 passes**. After pass 5, deliver the best result with its score and the open defects.

## 3. FireBall Logic Core (full, all build work)

- **01 Structure parser.** Symbols, types, scopes, dependencies.
- **02 Dependency graph.** Functions, modules, variables, interfaces and how they connect.
- **03 Constraint engine.** Types, invariants, preconditions, postconditions, compatibility.
- **04 Solution selector.** Compare at least two valid strategies against requirements and constraints. Keep the best and state why the other lost.
- **05 Validation gate.** Run every available check (syntax parse, brace balance, undefined names or tokens, file wiring, tests if present). Reject or revise anything that fails.

**Output contract:** validated code, detected risks, unresolved constraints.

## 4. Team (websites)

| Role | Count | Writes files | Job |
|---|---|---|---|
| Orchestrator | 1 | no | Direction card, file assignment, pass loop, best-result selection, final report |
| Coder | 5 | yes | Each owns a group of files, written once per pass |
| Judge | 3 | no | J1 technical gates (T2 syntax, T3 structure and wiring, T4 clean output, T5 motion); J2 design judgment (R1 slop, R2 brief fit, R5 responsive); J3 nav and copy (R3 nav behaviour, R4 copy and voice) |

**Coder groups (no write conflicts)**

| Coder | Files |
|---|---|
| K1 | `index.html`, `main.js` |
| K2 | `tokens.css`, `base.css` |
| K3 | `nav.css`, `nav.js` |
| K4 | `hero.css`, `sections.css` |
| K5 | `motion.css`, `forms.css` |

**Rules.** A coder edits only its own files. Judges never edit. Reasoning is short: decisions and risks, no code in reasoning. Class and token names come from the direction card, not from another coder.

**Directions.** Tried in order: Warm paper, Civic clear, Local craft. Each pass uses the next one. None uses navy or violet by default.

**Scoring.** Gate failures weigh 2 points, judgment findings 1. Lower is better. Stop early on zero findings.

## 5. Verification (REI score out of 10)

**Websites and code**

| Criterion | Points | Full credit requires |
|---|---|---|
| Correctness | 3 | Runs or renders without errors. Every requirement met. Edge cases handled. |
| Code quality | 2 | Valid syntax, clear names, no dead code or duplication, no security issue. |
| Visual quality | 3 | Clear hierarchy, consistent spacing and type, coherent palette, good contrast, not generic. |
| Responsiveness and a11y | 2 | Mobile and desktop widths. Semantic HTML, labelled controls, keyboard navigation. |

**Reasoning**

| Criterion | Points | Full credit requires |
|---|---|---|
| Correctness | 4 | Every fact and calculation checked. Uncertain points flagged and not load-bearing. |
| Completeness | 2 | Every sub-question answered. |
| Constraint compliance | 2 | Format, language, length, scope match the message stage. |
| Clarity | 2 | Easy to follow, no contradiction, no padding. |

**Rules.** Each criterion scored separately, with one line of evidence. A check not performed cannot earn points. Never inflate a score.

## 6. Design rules (websites)

- **Fit before style.** No neon, glow, cyan or purple gradients, or dark glass by default.
- **No AI slop.** Two or more signals (glowing dark gradient with glass cards; centered hero plus three cards plus logo cloud plus testimonials; identical cards; emoji icons; hollow marketing words; invented stats) mean rework of layout, type, palette and material.
- **Identity.** One signature move, visible on the first screen, never captioned.
- **Clean output.** No section labels, version stamps, debug panels or commentary in shipped code.
- **Type.** Fluid `clamp()` sizes. 45 to 75 characters per line. Real fallback stacks.
- **Colour.** OKLCH tokens, neutrals tinted toward the brand hue. Engineered dark mode. Colour never the only signal.
- **Motion.** 150 to 250ms, 300 to 500ms, 500 to 800ms by role. `transform` and `opacity` only. At least 3 `@keyframes`, at least 4 animated declarations, reduced-motion rule.
- **Accessibility (WCAG 2.2 AA).** Contrast 4.5:1 text, 3:1 UI, on the worst-case backdrop. 44px targets, visible focus, `lang`, alt text.
- **Writing.** Buttons say what happens. No lorem, invented testimonials, logos or stats.

## 7. Liquid Glass navigation (mandatory in every website)

- Rounded pill: `border-radius: var(--radius-full)`.
- Top of page: brand, links and button only. Glass surface hidden, fading in on scroll with `opacity`.
- Distortion is mandatory: an SVG `feDisplacementMap` bends the backdrop at the rim. Blur alone fails.
- Chromium gets full distortion; other browsers keep blur glass. Text and icons never filtered.
- Fallbacks: solid surface under `prefers-reduced-transparency` and `forced-colors`; visible surface with no JS.
- Presets: Subtle, Standard (default), Strong (calm backdrops only). Never above scale 44.
- Reuse the `nav.css` and `liquidGlass()` code from the v5.6 Liquid Glass skill, section 5, verbatim.

Judges check: `nav.js` contains `feDisplacementMap`, the nav appears on scroll, contrast passes on the worst-case backdrop.

## 8. Output contract

1. Validated output (files or text).
2. The REI score per criterion, with evidence, and the number of passes used.
3. Detected risks.
4. Unresolved constraints and open defects, with points lost.
