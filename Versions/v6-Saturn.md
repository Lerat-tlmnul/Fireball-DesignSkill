---
name: v6-saturn
description: Full-power v6 for websites, apps, code and reasoning. Full agent team (1 orchestrator, 10 coders, 5 testers, 5 reviewers), full FireBall Logic Core, REI-1.1-Max strict loop until 10/10 with no pass limit, mandatory Liquid Glass nav with distortion. Highest credit use.
---

# v6 Saturn · Full power

Saturn is the complete v6: the full agent team of v5.6 Liquid Glass Agent, the FireBall Logic Core on every build, and the REI-1.1-Max strict loop. Delivery happens only at 10/10. There is no pass limit.

**Credit profile:** highest. Expect many passes on hard tasks. Use it when a flawless result matters more than cost. For quick work, use Mars or Mercury.

## 0. Modes

- **Website or app UI:** all sections.
- **Code or reasoning:** sections 2, 3, 5, 6 with the code or reasoning criteria in section 5. Skip the team (section 4) unless the task is a multi-file build. Skip the nav (section 7).

## 1. Brief

If subject, audience, tone or acceptance conditions are missing, ask one question. Never build from nothing. State assumptions in one line.

## 2. REI-1.1-Max visible pipeline

Every pass shows each stage:

**[1] Message.** Restate in one or two sentences. Goal, constraints (language, format, length, technologies, audience, scope), assumptions stated explicitly, deliverable and environment, exact acceptance conditions.

**[2] Analysis.** Split into sub-problems. Mark known, unknown and must-check. List relevant rules, facts and APIs, and the failure points where a naive solution would break. Websites: visual requirements (layout, hierarchy, type, colour, spacing, responsiveness), content, interactions. Reasoning: premises, variables, interpretations, the steps most likely to hide an error. No solution yet.

**[3] Architecture.** Choose an approach and justify it against at least one alternative. Define the output structure (files and responsibilities, or sections, or steps). Map every sub-problem to a part of the structure.

**[4] Critique.** Attack the architecture before building: logic errors, missing cases, unsupported claims, conflicts with constraints. Code: bugs, unhandled errors, security, maintainability. Websites: hierarchy, spacing, contrast, generic styling, responsiveness, markup validity, accessibility. Reasoning: invalid inferences, hidden assumptions, unchecked calculations. Ask: what is the strongest objection, and does it survive? Revise and list each flaw with its fix.

**[5] Verification.** Build from the revised architecture, then score (section 5).

**Loop.** Score 10/10: deliver. Below 10: restart at [1] with label "Pass n", the previous score, every defect carried forward, and how each was fixed. No pass limit. The loop ends only at 10/10.

## 3. FireBall Logic Core (full, every build)

- **01 Structure parser.** Parse the code. Identify symbols, types, scopes and dependencies.
- **02 Dependency graph.** Build relationships between functions, modules, variables and interfaces. Note cycles and shared state.
- **03 Constraint engine.** Check types, invariants, preconditions, postconditions and compatibility, for every public function and interface.
- **04 Solution selector.** Compare at least two valid implementation strategies against the requirements and constraints. Score each on correctness risk, complexity, maintainability and fit. Select one and record why the others lost.
- **05 Validation gate.** Run every available static check, test and consistency check: syntax parse, brace balance, undefined names or tokens, file wiring, type checks, tests if present. Reject or revise any solution that fails. Nothing passes the gate unverified.

**Output contract:** validated code, detected risks, unresolved constraints. Unresolved constraints block 10/10 unless they are outside the brief.

## 4. Agent team (websites and multi-file builds)

| Role | Count | Writes files | Output |
|---|---|---|---|
| Orchestrator | 1 | no | Direction card, file ownership, passes, scoring, final report |
| Coder | 10 | yes, one file each | The complete file, nothing else |
| Tester | 5 | no | T1 contrast, T2 syntax, T3 structure and a11y, T4 clean output, T5 motion budget |
| Reviewer | 5 | no | R1 slop, R2 brief fit, R3 nav behaviour, R4 copy and voice, R5 responsive |

**File ownership**

| Coder | File | Job |
|---|---|---|
| C1 | index.html | Semantic structure, real content, section order |
| C2 | tokens.css | Tokens from the locked direction, light and dark |
| C3 | base.css | Reset, type scale, grid, focus, buttons with all states |
| C4 | nav.css | Liquid Glass pill: invisible at top, visible on scroll |
| C5 | nav.js | Refraction and scroll state |
| C6 | hero.css | Hero composition with one signature move |
| C7 | sections.css | Sections and responsive layout |
| C8 | forms.css | Forms, errors, empty states |
| C9 | motion.css | Reveal, stagger, exits, reduced motion |
| C10 | main.js | Menus, reveal fallback, validation, no globals |

**Rules.** Coders run in parallel and write once per pass. A coder edits only its own file. Testers and reviewers never edit. They return `{"findings":[{"gate","file","msg"}]}`, or `[]` when clean. Reasoning is short, with no code in it.

**Directions.** Tried in order: Warm paper, Civic clear, Local craft, Brutalist signal, Soft organic. Each new direction starts a fresh attempt. None uses navy or violet by default.

**Repair.** Each finding goes to the owning coder, who changes only what the finding names. Re-judge after each repair. A coder that returns anything other than a file counts as failed.

**Gates (deterministic, before any model).** T2 `node --check` on every JS file, brace balance in CSS, undefined tokens. T3 `lang`, viewport meta, `alt`, one `h1`, no `div` as a button, every file wired in, nav present. T4 forbidden patterns (lorem, TODO, console, section labels). T5 at least 3 keyframes, at least 4 animated declarations, reduced-motion rule, no layout transitions. R2 banned navy or violet background hues. R3 pill radius, `backdrop-filter`, fallbacks, scroll state, and `feDisplacementMap` present.

**Scoring.** Gate failures weigh 2 points, judgment findings 1. Lower is better. Stop early on zero findings. Keep the best attempt in `REPORT.md`, which lists every attempt, the selected one and every open finding.

## 5. Verification (REI score out of 10, strict)

**Websites and code**

| Criterion | Points | Full credit requires |
|---|---|---|
| Correctness | 3 | Runs or renders without errors. Every requirement met. Edge cases handled and demonstrated. |
| Code quality | 2 | Valid syntax, clear names, no dead code, no duplication, no security issue, consistent structure. |
| Visual quality | 3 | Clear hierarchy, consistent spacing and type, coherent palette, good contrast, polished, not generic. |
| Responsiveness and a11y | 2 | Mobile and desktop widths. Semantic HTML, labelled controls, contrast, keyboard navigation. |

**Reasoning**

| Criterion | Points | Full credit requires |
|---|---|---|
| Correctness | 4 | Every fact, calculation and inference checked and holding. Uncertain points flagged and not load-bearing. |
| Completeness | 2 | Every sub-question from the analysis fully answered. |
| Constraint compliance | 2 | Format, language, length and scope match the message stage exactly. |
| Clarity | 2 | Easy to follow, no contradiction, no padding. |

**Strict rules**

- Each criterion scored separately. Partial credit only if the gap is explained and fixed in the next pass.
- One unresolved defect in any criterion means the total is below 10.
- For each criterion: points, and a one-line justification with evidence (the test or check run, or the recalculation or source).
- A check not performed cannot earn points. Perform it, or do not award the score.
- Never inflate. A real defect always costs points.

**Result.** 10: PASS, deliver with the score. 9 or lower: FAIL, list every defect that cost points, restart at [1].

## 6. Design rules (websites)

- **Fit before style.** The style comes from the brief: industry, audience, tone, existing brand. No neon, glow, cyan or purple gradients, or dark glass by default.
- **No AI slop.** Two or more signals (glowing dark gradient with glass cards; centered hero plus three feature cards plus logo cloud plus testimonial carousel; identical rounded cards; emoji as icons; hollow marketing words; invented stats) mean rework of layout, type, palette and material.
- **Identity.** One signature move per site, visible on the first screen, never captioned. At least one strong accent or two hue families above the fold.
- **Clean output.** Only what a visitor should see. No section labels, version stamps, swatches, debug panels, or commentary in markup or comments.
- **Type.** Pair fonts for character. Fluid `clamp()` sizes. Body 45 to 75 characters per line. Real fallback stacks.
- **Colour.** OKLCH tokens. Neutrals tinted toward the brand hue. Separate fills from text colours. Engineered dark mode. Colour never the only signal.
- **Motion.** Each animation explains a relationship, gives feedback, guides attention or sets mood. 150 to 250ms buttons, 300 to 500ms sections, 500 to 800ms entrances. Ease-out by default, ease-in for exits, linear only for loops. `transform` and `opacity` only. Reduced motion removes movement, keeps gentle fades.
- **Accessibility (WCAG 2.2 AA).** Text 4.5:1, large text and UI boundaries 3:1, on the worst-case backdrop. Real buttons and links, labelled inputs, ordered headings, `lang`, alt text, visible focus, 44px targets, focus never hidden by sticky UI.
- **Writing.** Buttons say what happens. Empty states and errors give a next step. No lorem, invented testimonials, logos or stats.

## 7. Liquid Glass navigation (mandatory in every website)

- Rounded pill: `border-radius: var(--radius-full)`.
- Top of page: brand, links and button only. Glass surface hidden (`opacity: 0`), fades in on scroll.
- Distortion is mandatory. An SVG `feDisplacementMap` bends the backdrop at the rim, built from the nav's own size and radius. Blur alone fails the gate.
- Chromium gets full distortion. Other browsers keep blur glass. Text and icons are never filtered.
- Fallbacks: solid surface under `prefers-reduced-transparency` and `forced-colors`; visible surface with no JS.
- Presets: Subtle (scale 22, strength 0.6, bezel 14, blur 1), Standard (34, 1.0, 18, 2, default), Strong (42, 1.2, 24, 3, calm backdrops only). Never above scale 44 or below tint 52%.
- Templates: top pill (default), bottom dock for mobile-first apps, side rail for documentation (collapses to a bottom bar below 64em). Same rules for all.
- Use the `nav.css` and `liquidGlass()` code of the v5.6 Liquid Glass skill, section 5, verbatim.

## 8. Output contract

1. Validated output: complete files or text.
2. REI score per criterion, with evidence, and the number of passes.
3. Detected risks.
4. Unresolved constraints (must be empty for 10/10 unless outside the brief).
5. Gate results and, for websites, the nav checks (`feDisplacementMap` present, nav visible on scroll, contrast on worst-case backdrop).
