---
name: ui-design-engineering
description: >
  Design, build, redesign, restyle, or review any user interface: landing
  pages, websites, dashboards, app screens, portfolios, design systems,
  components, forms, onboarding flows (web, mobile, desktop). Use this skill
  whenever the user asks for a UI, a site, a page, a component, "make it look
  better", "more beautiful", "more original", a visual identity, CSS/Tailwind/
  React front-end work, or a UX/accessibility review, even if they never say
  "design". Produces designs that ADAPT to the request (never a generic
  "AI-looking" site), with clean output (only what the visitor should see),
  a verified accessibility floor (WCAG 2.2 AA), OKLCH color, ready-made
  Liquid Glass navigation templates (top, bottom, side): rounded, with a
  refraction/distortion effect, whose surface appears on scroll,
  and a mandatory short review pass instead of long reasoning. Do not use for
  pure backend, data-pipeline, or non-visual engineering.
---

# UI Design Engineering v5 - Liquid Glass (LG)

> **LG edition.** Same skill as v5 (adapt to the brief, clean output, accessibility floor, short reasoning, mandatory review), with one difference: the navigation surface is a **Liquid Glass**: still rounded, but it refracts the content behind it with a distortion at the rim (s.0.4, s.9.1). Everything else about the page stays governed by s.0.

Four jobs, in this order: **(1) fit the request: the design comes from the
brief, not from a trend; (2) ship only what the visitor should see; (3) make
it work for everyone; (4) review what you wrote before delivering.** Jobs 2
and 3 are a hard floor (Tier A). Jobs 1 and 4 are what separate a made-for-this-
brief site from AI slop.

**Prime directives**
1. **Adapt, never impose.** The brief decides the style. Your taste, your habits, and trends do not.
2. **No AI slop.** If the page could have been generated for any other brief, it failed (s.0.1).
3. **Think short, build once, review hard.** Reason only about what matters (s.0.2); write code once, in the output; fix problems in the review (s.2, Phase 7).
4. **The shipped page contains content and interface, nothing else** (s.1, Clean Output).
5. Beautiful but unusable = failure. Usable but forgettable = also failure. Inaccessible = never.
6. A rule broken on purpose, with a one-line reason, is design. A rule broken by accident is a bug.
7. Never claim a check passed unless you actually ran it. Say "not executed" instead.

---

## 0. Adapt to the request (read before anything else)

### 0.1 Futuristic is not a default. It is usually awful.
A "futuristic" look (neon glow, cyan/purple/blue gradients, dark glassy
everything, floating orbs, glowing borders, sci-fi fonts, "cyber" grids) is
the signature of AI slop. It is almost always wrong. Rules:
- **Never pick a futuristic or "techy" style because the product is software, AI, crypto, or "modern".** Software companies are not all neon.
- **Use it only when the user explicitly asks for it** ("futuristic", "cyberpunk", "sci-fi"), and even then keep it restrained: one light effect, real contrast, real content.
- **Adapt to the subject.** A bakery, a law firm, a surf school, a clinic, a punk label, a municipal service, and a B2B dashboard must look *different from each other* in type, color, layout, imagery, tone, and density.
- **Read the signals in the request**: industry, audience, age, country, tone words, references, existing brand, content volume. Extract the style from them. If the user gives a reference or an existing site, stay inside its logic.
- **When the request has no style signal, choose the most appropriate and least trendy answer** for the category, then add one distinctive, ownable detail. Not the flashiest answer.

### 0.2 Slop test (run it on your own plan and on the result)
It is slop if you can answer yes to two or more:
- Dark background + glowing gradient + glass cards, without the brief asking for it
- Purple/blue/cyan gradient anywhere as an identity, gradient text on headings
- Centered hero + "three feature cards" + logo cloud + testimonial carousel + final CTA
- Identical rounded cards with the same shadow and radius, repeated everywhere
- Blur/glass on everything, glow on everything, orbs/blobs floating in the background
- Inter or system-ui as the whole identity; Lucide icons in tinted squares
- Marketing clichés as copy: "Revolutionize", "Elevate", "Seamless", "Unleash", "Next-generation", "AI-powered"
- Emoji as icons, pill badges, eyebrow labels on every section, invented stats
- You could swap the brand name and nothing would change
If it fails, change layout, type, palette, and material, not just the color.

### 0.3 Reasoning discipline (think short, only what matters)
Your reasoning is for **decisions and risks**, not for drafting.
- **Think about**: the scope; who uses it and for what; the 3 to 5 direction decisions (type, palette, layout, hero, nav, material); content structure and real content needs; the 1 to 3 real risks (contrast on the hero, a tricky interaction, overflow, a11y trap).
- **Budget**: about 10 to 15 short lines for a full surface, 3 to 5 for a component or a quick iteration. If you are past that, stop and start writing.
- **Never write in your reasoning**: HTML, CSS, JS, or any full or partial code; the full token list; the full copy; a restatement of this skill; a rule-by-rule walkthrough; the same decision twice.
- **Decided means done.** Do not re-open a decision unless the review finds a real problem.
- **Code goes once, directly in the output.** Defects are found and fixed in the review (Phase 7), not by pre-writing the code in your head.

### 0.4 Liquid Glass scope (LG edition)
Liquid Glass is a translucent surface that **refracts** what is behind it: blurred, lightly tinted, bent along its rim, with a thin specular edge. It is a material, not a theme.
- **Always rounded.** Pill or generous radius, never square. The refraction follows the rounded shape.
- **Where**: floating layers above content. The navigation is the default; at most one more (a floating action, a menu panel). **Maximum 2 Liquid Glass surfaces per page.** Never cards, sections, or backgrounds in the flow.
- **Fit first.** Use it only when translucency suits the brief. A flat, brutalist, paper, or very sober direction gets a solid rounded surface instead (log it in the Deviation ledger). The rest of the page does **not** become glassy or futuristic: s.0.1 and s.0.2 still apply in full.
- **Distortion hits the backdrop only**, never the text or icons. The centre of the surface stays calm; the bend is at the rim.
- **Browser support is honest**: the true refraction needs a Chromium engine (`backdrop-filter: url(#svg-filter)`). Safari and Firefox get the blur glass. Both versions must look intentional.
- **Readability beats effect.** Keep the tint high enough that text passes contrast on the worst-case backdrop *after* distortion (s.9.1). Raise the tint rather than ship unreadable text.
- **Solid fallback** under `prefers-reduced-transparency`, `forced-colors`, and no `backdrop-filter` support.

---

## 1. Two tiers

### Tier A: the floor (never negotiable, whatever the creative mode)

**Clean Output (what ships is what the visitor sees)**
- **No parasitic information.** Banned in the page, visible or not: section labels ("Hero", "Features", "Section 2"), version stamps, "Built with...", "Design by AI", direction names, signature-move captions, deviation notes, token or color swatches, contrast badges, state galleries, grid/debug overlays, placeholder tags ("Your text here"), instructional captions, TODO text, `console.log`.
- **Eyebrow rule.** Small label lines above headings ("01 - Features", "Why us", "Our process") are the #1 parasite. Allowed only when they carry real information the visitor needs (a real category, date, place, price, step number in a true sequence). Same for pill badges ("New", "Beta", " AI-powered"), decorative numbering, "Scroll" hints, and emoji used as icons.
- **Testing parts only on request.** Test pages, QA panels, state showcases, contrast tables, Storybook-style galleries, `?debug` modes: build them only if the user asks, in a **separate file**, never inside the shipped page.
- **Process stays in chat, short.** Direction Card and Review go in the chat reply, never in the page or its comments. Components and quick iterations get no card. No victory recap, no feature list restating the code.
- **Code comments**: only for a non-obvious *why*. No section banners, no design commentary.

**Accessibility floor**
- **Contrast** computed with the script in s.10 (text 4.5:1, large text 3:1, UI boundaries / focus rings / meaningful icons 3:1). Show numbers in chat only when asked or when a pair is borderline. Text over images, heroes, or glass is computed against the **worst-case backdrop** it can sit on.
- **Semantics + keyboard**: real `<button>`, `<a>`, `<label>`, headings in order, landmarks, `lang` on `<html>`, alt text. Everything operable by keyboard, visible `:focus-visible`.
- **WCAG 2.2 additions**: focus not hidden by sticky UI (2.4.11, use `scroll-padding`); targets >= 24x24px minimum (2.5.8) and >= 44x44px on touch; no drag-only interactions (2.5.7); no re-asking known info (3.3.7); no cognitive-test login, allow paste and password managers (3.3.8); reflow at 320px (1.4.10).
- **States**: hover (only under `@media (hover: hover)`), focus-visible, active, disabled, loading (if async). Error/empty/overflow per s.5.2.
- **Color is never the only signal** (icon + text + color).
- **Motion safety**: honor `prefers-reduced-motion`; never animate layout properties of in-flow elements (`width`, `height`, `top`, `left`, `margin`); no flashing > 3 times/second. The nav templates (s.9) animate only `opacity`, `transform`, and `box-shadow`, so they need no exception.
- **Transparency safety**: every glass/blur surface has a solid fallback for `@supports not (backdrop-filter)`, `prefers-reduced-transparency: reduce`, and `forced-colors: active`. The Liquid Glass refraction is skipped (blur glass or solid) whenever the browser can't render it or the user asked for less transparency.
- **Forced colors**: nothing essential disappears under `forced-colors: active` (use `outline`, not only `box-shadow`, for focus).
- **Text resizes**: type in `rem`, layout survives 200% zoom.
- **Honest content**: no Lorem Ipsum, no fake stats or testimonials, no fake logos. Real empty states are required UX, not filler.
- **i18n stated**: logical CSS properties by default; if RTL/translation is out of scope, say so in one line in chat.

### Tier B: adaptable defaults (bend them freely, log it in chat)
Grid exactness, 8pt rhythm, modular scale, 60/30/10 palette, 12-col grid, card
systems, radius uniformity, easing conventions, one-accent restraint, "clean"
whitespace, the default navigation (s.3.6). These exist to stop *accidental*
choices, not to cap ambition. Break any of them when the brief calls for it and
record it in the **Deviation ledger** (Phase 4): `Rule -> what I did instead -> why`.

---

## 2. Workflow

### Phase 0: Scope (decide first, say it in one line)
- **Full surface** (landing, website, dashboard first screen, app shell, brand-defining page): all phases.
- **Single component in an existing system**: inherit tokens, skip Phases 3 and 4, still do Phase 7.
- **Quick iteration** ("punchier", "darker", "try another"): touch only the tokens and levers concerned; don't re-derive everything.
If a request fits both full and narrow scope, the narrower one wins unless the brief establishes a new surface.

### Phase 1: Context (short, not a questionnaire)
Who uses it, on what device, doing which job; category norms; the one action that matters; the 3-second emotional target; **the style signals in the request (s.0.1)**. Read the brief and any references before asking anything. Ask **one** question only if the answer would change the direction materially; otherwise state your assumption and proceed.

### Phase 2: Intent + Ambition dial
Pick an intent that matches the brief: Professional - Premium - Warm - Experimental - Playful - Corporate - Artistic - Minimal - Dense - Editorial - Freeform. ("Tech-forward / futuristic" exists only when the user asks, s.0.1.)
Then set the **Ambition dial** (1 to 5) and state it:

| Dial | Meaning | Typical use |
|---|---|---|
| 1 | Invisible craft, inherit everything | Component in a mature system |
| 2 | Refined, conventional | Internal tools, admin, dense data |
| 3 | Distinctive within category norms | SaaS product UI, e-commerce |
| 4 | Art-directed, memorable | Landing pages, brand sites, marketing |
| 5 | Expressive, rule-breaking with purpose | Portfolios, campaigns, culture/music/fashion/games |

Defaults: marketing surface -> 4, product UI -> 3, dense tool -> 2. User words override: "surprise me", "be bold", "no constraints", "wow" -> 5, no clarifying question. The dial changes how many Tier B rules you bend, never Tier A.

### Phase 3: Divergence + Variety roll (full surfaces at dial >= 3)
**Fit first, variety second.** Only keep options that suit the brief.
1. **Roll** (s.3.5): pick a starting point for each lever from the pools instead of your habit, discarding picks that don't fit the subject. Sketch **three directions** in 2 to 3 sentences each, differing on **at least four of seven levers**: type, palette hue family, layout archetype, hero archetype, material, motion, navigation. At least one must be unexpected for the category yet still appropriate.
2. **Anti-repeat**: never reuse the previous direction, font pairing, hero, or layout archetype of this conversation. Two sites in the same conversation differ on >= 4 levers.
3. Pick one and say why in one line, or hand the choice to the user when stakes are high. Do this in your head and keep it short (s.0.3); skip for a component or quick iteration.

### Phase 4: Direction Card (in chat, <= 5 lines, before the code, full surfaces only)
```
Direction: <name> | Big idea: <one sentence>
Type: <display + text>  Palette: <hue family, accent logic>  Material: <...>
Layout: <archetype> | Hero: <archetype> | Nav: <template>  Motion: <personality>
Signature move: <the one memorable, ownable detail>
Deviation ledger: <Tier B rules bent -> why>
```
The **signature move** is the thing someone would describe to a friend: an oversized running headline, a cursor-reactive grid, a nav that behaves like a table of contents. One per surface. It passes Tier A and is **never captioned on the page**.

### Phase 5: Blueprint (structure before skin)
Information hierarchy, user flow (discover -> understand -> decide -> act -> feedback -> return), scanning pattern (F for reading, Z for landing), real content length and data shape, navigation model, grid and density. Analyse real text and data before laying anything out: the interface adapts to content, not the reverse. Every section earns its place; cut any section that exists only to fill a template.

### Phase 6: Build
Use the locked direction. Tokens first (s.9), then layout, then components with all states, then edge states. Navigation: pick a template from s.3.6 / s.9.1 that suits the layout. Prefer modern CSS (s.4.6) with graceful fallback. **Write the code once, in the output, not in your reasoning.** The output must *behave* correctly and pass Clean Output.

### Phase 7: Review (mandatory, replaces long reasoning)
After writing, **reread your own code as a hostile reviewer**: assume there is at least one bug, one a11y problem, and one generic element, and find them. Do not praise the work. Do not rewrite what works.
1. **Reread** the produced file top to bottom (use `view` if you have a sandbox; otherwise reread the output).
2. **Run** what can be run (contrast script, HTML validity, link/class/token references). What you can't run is marked "not executed".
3. **Find** concrete defects: a quote of the problem line + the fix, not general worries.
4. **Fix** them in the file, then deliver. Fix only what the review found; don't start a new design pass.
5. **Report in chat, <= 5 lines**: what you found and fixed, what is "not executed". Nothing found -> say so in one line. No recap of features.

**Checkable (script or by reading)**
- [ ] **Clean Output scan**: no banned label, badge, eyebrow without real info, debug/test block, swatch, or design commentary in markup, comments, or `console`
- [ ] Every foreground/background pair was computed with s.10 (images, hero, glass: worst-case backdrop; nav text at the top state too)
- [ ] Every `var(--x)` used is defined; every meaningful light token has a dark override
- [ ] No `<div>`/`<span>` acting as button, link, or input; every input has a label
- [ ] No in-flow layout-property animation; `prefers-reduced-motion`, `prefers-reduced-transparency`, `forced-colors` blocks present
- [ ] `lang`, viewport meta, `alt`, heading order, landmarks present
- [ ] No Lorem Ipsum, no fake data presented as real
- [ ] Nav: top state (surface invisible, parts readable), scrolled state (surface visible), no-JS state (surface visible), mobile behavior, Escape/focus return, 44px targets, solid fallbacks
- [ ] Markup nests validly, nothing references an undefined class, prop, or token

**Judgment (answer each, fix before shipping)**
- [ ] **Slop test** (s.0.2): two or more yes -> rework layout, type, palette, material
- [ ] **Fit test**: does the style come from this brief (industry, audience, tone)? Would the user recognise their request in it?
- [ ] **Swap test**: replace the brand name with a competitor's. Does anything break? If not, it is generic.
- [ ] **Twin test**: could this be mistaken for the last site you made? If yes, re-roll two levers.
- [ ] **Squint test**: blur the screen. Is the primary action still the strongest element?
- [ ] **Grayscale test**: does hierarchy survive without color?
- [ ] **Noise test**: cover each small text element: if the page loses nothing, delete it.
- [ ] Signature move present, visible, harmless to usability
- [ ] Edge states (s.5.2) implemented or explicitly marked out of scope
- [ ] Layout holds with +35% text length and a non-Latin script

---

## 3. Creative toolkit

### 3.1 The seven levers (each one is a decision to make from the brief, not a default to take)
- **Type.** Pair for contrast of *character*, not just weight. Scale jumps >= 1.5x between display and body when the direction wants drama. Exploit variable axes (`opsz`, `wdth`, `wght`, `SOFT`) as expression. Tabular numerals for data. Never ship the system fallback as an identity.
- **Color.** Tint your neutrals toward the brand hue (chroma 0.005 to 0.03) instead of dead gray. Shift hue slightly in shadows and highlights. Allow one deliberately "wrong" color. `color-mix(in oklch, ...)` for ramps. Gradients need a reason (light source, depth, data), not decoration.
- **Composition.** Asymmetry, overlap, a single element that breaks the grid, extreme scale contrast, deliberate density changes between sections. Whitespace is a material; spend it unevenly.
- **Hero.** The first screen is its own decision (pool in s.3.5), not "centered title + button".
- **Material.** Flat ink, paper and grain (inline SVG `feTurbulence` as a data URI), hard offset shadows, hairline rules, halftone, frosted or Liquid Glass **only** where layering has meaning (the nav is the default place; scope in s.0.4). Pick one main material and commit.
- **Motion.** A personality, not an effect: snappy (steps, <= 150ms), editorial (slow fades and clip-path reveals), luxe (500 to 700ms ease-out), playful (springs, +/-2 deg tilts), instrument (<= 120ms, no flourish). One orchestrated entrance beats ten scattered hovers.
- **Voice.** Microcopy, empty states, and errors share the direction's tone. Tone is part of the design. Write like a person from that industry, not like a marketing generator.

### 3.2 Direction seeds (starting points to combine, mutate, or ignore; choose by fit, never by "coolest")
Fonts named are Google Fonts families; always give a real fallback stack, `font-display: swap`, and load responsibly. If a family can't be loaded, say what fallback you used.

1. **Editorial Warm**: Fraunces or Newsreader + a clean grotesk; paper neutrals tinted hue 70 to 90, terracotta or ink-blue accent; asymmetric columns, pull-quotes at 5 to 8x body size, hairline rules; slow `clip-path` text reveals.
2. **Brutalist Signal**: Archivo wide/black or a heavy mono; zero radius, 2px borders, hard offset shadows, visible grid; off-white or black with one screaming signal color; instant or stepped motion.
3. **Luxe Nocturne**: light-weight serif display with wide-tracked caps labels; dark surfaces tinted hue 280 to 300 at chroma <= 0.02, a muted metallic accent; huge spacing; 500 to 700ms ease-out. Only for genuinely premium/nocturnal subjects.
4. **Technical Instrument**: mono for data + a neutral grotesk for UI; 1px borders, radius 2 to 4px, tabular numerals, keyboard-first, command palette; one accent plus status colors; <= 120ms motion. For real tools, not for decoration.
5. **Playful Pop**: rounded or quirky grotesk (Bricolage Grotesque, Unbounded); 3 saturated hues at matched lightness, radius 20 to 28px, sticker borders, slightly tilted elements, spring easing.
6. **Calm Workspace**: humanist sans + a quiet serif accent; low-chroma tinted neutrals, generous line-height, almost no shadow; motion barely there.
7. **Data Poster**: oversized numerals and labels as the hero, charts as graphic design, 2-color system, tight leading, annotations like a newspaper graphic.
8. **Neo-Swiss Grid**: one grotesk in two weights, strict visible columns, flush-left ragged-right, red or cobalt as the only color, huge numerals as navigation; motion limited to alignment snaps.
9. **Risograph Zine**: two spot colors with `mix-blend-mode: multiply`, halftone dots, slight misregistration offsets, condensed display + typewriter text, rotated stickers, torn-edge SVG masks.
10. **Soft Organic**: warm off-whites, moss/clay/sand palette, blob and pebble shapes via `border-radius` and SVG paths, rounded serif display, slow floating motion at tiny amplitude, photography with soft masks.
11. **Cinematic Dark**: full-bleed media, subtitle-style captions, letterbox bars, one amber or teal accent, slow dolly-style scale on scroll (`transform` only), huge condensed display. Only when the content is real footage or imagery.
12. **Blueprint**: deep blue or cream "drafting paper" ground, hairline construction lines, dimension marks and callout leaders as layout, mono labels that are *real data*.
13. **Terminal Retro**: mono everywhere, phosphor green/amber on near-black or inverted paper, box-drawing borders, command-palette as primary navigation. Only when the subject is genuinely terminal/hacker culture.
14. **Maximal Collage**: overlapping cut-out images, mixed type families used deliberately, clashing-but-balanced palette at matched lightness, sticker UI. Needs dial 5 and a stricter Tier A pass.
15. **Quiet Japanese Minimal**: extreme whitespace (ma), one vertical text element, ink black + vermilion seal accent, thin serif, very slow fades.
16. **Local Craft**: for shops, food, trades, associations: real photography, hand-set serif or sturdy slab, warm paper or painted-wall colors, plain wayfinding, big phone/address/opening-hours block that is real information.
17. **Civic Clear**: for public services, health, education: high contrast, large type, plain words, strong focus states, calm color, no decoration that competes with the task.

Mixing is encouraged: take the type of one, the material of another.

### 3.3 Anti-defaults (avoid by habit, allowed only by reason)
Everything in the Slop test (s.0.2), plus: purple-to-blue diagonal gradients - blur-on-everything glass - neon glow and sci-fi fonts for non-sci-fi subjects - Lucide outlines with no optical adjustment - gradient text on every heading - stats band with invented numbers - the same layout across fintech, gaming, luxury, edu, music. If the brief truly wants one of these, say why in chat and proceed.

### 3.4 Reading references
Extract the *logic*, never the pixels. Apple -> intentional spacing and product storytelling, not white rounded cards. Stripe -> technical confidence, controlled gradients. Linear -> density and keyboard-first precision. Notion -> calm, content priority. Gaming -> contrast and fast feedback. Luxury -> restraint and slow motion. Brutalist -> visible structure, rules broken with purpose.

### 3.5 Variety engine (pools to roll from, after the fit filter)
**How to roll.** Models drift to the same few choices. For each lever, take `index = (character count of the brief) mod (pool size) + offset` (offset 0 for type, 1 for palette, 2 for layout, 3 for hero...), then step forward until the pick **fits the brief** (s.0.1). A surprising-but-defensible pick beats a safe one; an inappropriate pick beats nothing. Never take the first item by habit.

**Layout archetypes**: asymmetric split with oversized type - bento grid with varied cell sizes - magazine columns - sticky-stack storytelling - index list as the hero (big rows, hover preview) - full-bleed media with overlaid type - 50/50 split with one sticky half - poster / typographic wall - vertical timeline spine - dashboard-first - overlapping collage - horizontal scroll chapter (with keyboard and vertical fallback) - centered monolith (one column) - diagonal or stepped sections.

**Hero archetypes**: oversized type alone - product shown in context - interactive toy (cursor-reactive grid, drag-free) - marquee statement - split typography/image - command-palette hero - live real-data hero - single-sentence manifesto - image mosaic - scroll-driven reveal of the headline - video or looping CSS animation behind restrained type.

**Section archetypes (real content only)**: sticky scroll steps - big numerals with real figures - comparison table - accordion FAQ - pricing with a real toggle - masonry gallery - quote wall of real quotes - timeline - CTA band with one action - tabbed showcase - before/after slider (keyboard operable) - map or schedule.

**Palette recipes (verify contrast)**: bone + cobalt - moss + cream + clay - ink + tangerine - plum dusk + pale pink - sand + terracotta + deep green - graphite + amber - deep teal + coral - off-white + signal lime on black - rosewood + butter yellow - navy + warm paper - chalk + brick red - pine + oat.

**Font pairings (Google Fonts)**: Instrument Serif + Geist - Bricolage Grotesque + Literata - Syne + DM Sans - Familjen Grotesk + Spectral - Unbounded + Manrope - Archivo + JetBrains Mono - Young Serif + Outfit - DM Serif Display + DM Sans - Space Mono + Rethink Sans - Gloock + Schibsted Grotesk - Anybody + IBM Plex Sans - Big Shoulders Display + Barlow - Fraunces + Work Sans - Newsreader + Geist.

**Backgrounds and surfaces**: grain - dot grid - blueprint grid - topographic lines (inline SVG) - halftone - soft radial light source - solid color blocks - paper texture - subtle noise-masked gradient (one light source). Pick one.

### 3.6 Navigation (templates to choose from; pick by layout and device)
Three ready-made templates live in s.9.1: **Top**, **Bottom (dock)**, **Side (rail)**. Pick the one that suits the layout: Top for most sites; Bottom for mobile-first, app-like, or portfolio surfaces; Side for editorial, documentation, or desktop-heavy surfaces. Any other variant is allowed if the direction asks (centered logo with split links - command-bar nav (`/` or CmdK) - table-of-contents nav that highlights the current section - hide on scroll down, reveal on scroll up with focus kept reachable).

**Shared behavior (Tier B, log it if you change it):**
- **At the very top of the page the rounded bar is invisible except its parts**: brand, links, and buttons stay visible; the pill's background, border, blur, and shadow are fully transparent.
- **As soon as the user scrolls, the bar becomes visible**: the rounded surface fades in as **Liquid Glass** (translucent, lightly tinted, refracting the content behind it with a distortion at the rim, thin specular edge, soft shadow). Back at the top, it fades out again. The shape stays rounded; the distortion only bends what is behind the surface.
- Only `opacity`, `transform`, and `box-shadow` animate; nothing changes size, so there is no reflow.
- **Text must be readable in both states.** At the top, nav text sits directly on the hero: compute contrast against the worst-case hero backdrop and set `data-hero="dark"` (light text) or keep the default (dark text) accordingly. Scrolled state: compute against the glass surface at its worst-case backdrop.
- **No-JS safe**: without JavaScript the surface stays visible (JS adds `data-scrolled="false"` only after it runs).
- Targets >= 44px; mobile collapses links into a disclosure or reshapes the nav (see templates); Escape closes menus and returns focus.
- State is driven by an `IntersectionObserver` sentinel (no scroll listeners).

### 3.7 Interaction delights (at most three per surface; all behind Tier A)
Cursor spotlight on cards (`@media (hover: hover) and (pointer: fine)`) - magnetic buttons (<= 8px shift) - scroll-linked progress line - line-by-line text reveal - number counters (final real value is in the markup) - View Transitions between pages - pausable marquee - sticky stacking cards - subtle parallax via `animation-timeline` in `@supports` - branded `::selection` and `scrollbar-color` - image preview following hover on list rows - tilt cards (<= 6 deg). Each disappears cleanly under `prefers-reduced-motion` and on touch. None may be captioned or explained on the page. Skip them all when the subject is a calm, serious, or information-first one.

---

## 4. System specs (defaults you may bend)

### 4.1 Spacing *(Tier B)*
Default scale: 4 - 8 - 12 - 16 - 24 - 32 - 48 - 64 - 96 - 128 - 160px. The scale exists so numbers are never accidental; `17px` is fine when you can say why. Small gaps connect related items, medium separate groups, large separate sections. Use `rem` for anything tied to text size.

### 4.2 Typography *(Tier B for ratios, Tier A for resizability)*
Default modular scale 1.25 from 1rem: 0.75 - 0.875 - 1 - 1.25 - 1.5625 - 1.9375 - 2.4375 - 3.0625 - 3.8125 - 4.75rem. Switch ratio per intent (1.2 calm, 1.333 confident, 1.5+ dramatic). Body 45 to 75ch (`max-width: 65ch`), line-height body 1.5 to 1.65, headings 1.05 to 1.2, dense UI 1.2. Large headings tracking -0.02em. `text-wrap: balance` on headings, `pretty` on paragraphs. Fluid display type with `clamp()`.

### 4.3 Color *(OKLCH; contrast is Tier A)*
- Define tokens in OKLCH. Hex is only a tooling fallback.
- **Separate fills from text colors for semantics.** A green that works as an icon fill rarely passes as text; ship `--success` (fill) and `--success-fg` (text).
- Separate `--accent` (fills, with `--on-accent` text) from `--accent-text` (accent used *as* text on light surfaces).
- UI boundaries (inputs, checkboxes) need `--border-control` at >= 3:1, distinct from the decorative `--border-default`.
- Dark mode is engineered, not inverted: no pure `#000`, lower chroma ~20 to 30%, depth from surface layers, stronger shadows, re-check every pair. Dark is a mode the user can have, not a style you impose.
- 60/30/10 is a default; a maximalist or monochrome direction can abandon it.
- OKLCH lightness is perceptual, not WCAG luminance. Never assume a lightness value passes; compute it.

### 4.4 Motion *(personality is Tier B; safety is Tier A)*
Every animation explains a relationship, gives feedback, guides attention, or sets mood. Micro 120 to 250ms, transitions 300 to 500ms, ceremonial up to ~800ms. Animate `transform`, `opacity`, and with care `clip-path` and `filter`. Never layout properties on in-flow elements. Entrance = ease-out, exit = ease-in, unless the direction wants spring, linear, or stepped.

### 4.5 Layout and cognition
Gestalt (proximity, similarity, continuity, closure, figure-ground). Hick: fewer choices. Miller: chunk lists into groups of roughly 5 to 9; beyond ~7 add sub-groups or progressive disclosure. Reveal complexity on demand. Hierarchy check: primary action obvious, scannable in under 3 seconds, eye path intended.

### 4.6 Modern CSS toolkit (progressive enhancement, always with a working fallback)
`color-mix()` - `light-dark()` - container queries - `:has()` - `@property` for animated gradients - View Transitions - scroll-driven animations (`animation-timeline`, wrapped in `@supports`) - `clamp()` fluid type - `dvh` units - `font-optical-sizing` - `accent-color` - `color-scheme`. A feature that fails in an older browser must degrade to a usable, static layout.

### 4.7 Data visualization
Chart type follows the question: comparison -> bar, trend -> line, distribution -> histogram, relationship -> scatter. Direct-label instead of legends when possible. Honest axes and units. Never rely on hue alone to separate series. A chart can be art-directed; it cannot mislead.

---

## 5. Components and states

### 5.1 Component brief
For each component specify: purpose, sizes, variants, states, spacing, radius, type, interaction, accessibility behavior. Button hierarchy: primary (core goal), secondary, tertiary (low emphasis). Sizes sm 32 / md 40 to 44 / lg 48 to 56px height.

| State | Behavior |
|---|---|
| Default | token defaults |
| Hover | subtle shift, only under `@media (hover: hover)` |
| Focus-visible | 2px `outline`, 2px offset, >= 3:1 against neighbors |
| Active | `scale(0.98)` + deeper color |
| Disabled | `opacity: .5`, `aria-disabled`, explain *why* nearby when not obvious |
| Loading | `aria-busy="true"`, visible label change ("Saving..."), spinner decorative |

### 5.2 Edge and error states (Tier A when data, input, or async is involved)
- **Empty**: first-use (explain + next action), zero-results (why + clear filters). Banned: a bare "Coming soon" with no path.
- **Errors**: recoverable ones are inline, specific, and say what to do ("Enter an email like name@site.com"), not "Error". Unrecoverable (offline, 500) look different and offer retry. More than 3 errors -> summary at the top plus inline messages. Validate on blur first, live afterwards. Never discard input on failed submit.
- **Dependencies**: say why a field is disabled; re-validate dependents when upstream changes.
- **Long forms**: persist draft state; warn before leaving with unsaved changes.
- **Loading**: skeletons for known shapes, spinners for short unknown waits; anything over 2 to 3s needs progress or a skeleton.
- **Offline / stale**: tell the user the data may be old.
- **Destructive**: confirm, state the consequence, offer undo or cancel.
- **Overflow**: pick a strategy (ellipsis + title, show more, pagination) so content never clips silently.

---

## 6. Responsive and platform
Support 320 -> 2560px+. Default breakpoints (bend if the content grid says so): 375 - 640 - 768 - 1024 - 1280 - 1536. Adapt hierarchy, nav, density, and interaction per breakpoint (touch targets, safe areas, hover vs tap, keyboard shortcuts on desktop, container queries for components).

### 6.1 i18n and RTL
Logical properties (`margin-inline-start`, `padding-block-end`, `inset-inline-end`) over physical. Mirror directional icons in RTL, never mirror neutral ones. Budget ~30 to 35% extra length for German/Finnish, plus taller line-height for Thai, Devanagari, CJK. If out of scope, state it.

## 7. Performance as UX
LCP (optimize critical image/font), CLS (reserve space, set image dimensions), INP (light handlers). SVG for icons, WebP/AVIF for photos, lazy-load below the fold. Max 3 to 4 font files, variable fonts, `font-display: swap`, size-adjusted fallbacks. Heavy effects (grain, blur, big shadows) are performance decisions; budget them.

## 8. UX writing
Text is interface: clear, short, action-oriented, in the direction's voice. Buttons say what happens ("Save changes"), not "Submit". Empty states and errors are the best place for personality. Banned: generic marketing filler (s.0.2).

---

## 9. Skeleton tokens (a runnable starting point, not an identity)

> Contrast pairs below are **computed**, not asserted (hue 250; table after the code). Change `--hue` first, then rerun s.10; chroma at some hues clips out of gamut and shifts luminance. Shipping this unmodified on a full surface means you skipped Phases 3 and 4 (fails the Swap test).

```css
:root {
  color-scheme: light dark;
  --hue: 250; /* identity knob: change it, then re-verify contrast */

  /* Spacing */
  --space-1: 4px;  --space-2: 8px;  --space-3: 12px; --space-4: 16px;
  --space-5: 20px; --space-6: 24px; --space-8: 32px; --space-10: 48px;
  --space-12: 64px; --space-14: 96px; --space-15: 128px; --space-16: 160px;

  /* Radius */
  --radius-xs: 4px; --radius-sm: 8px; --radius-md: 12px; --radius-lg: 16px;
  --radius-xl: 20px; --radius-2xl: 24px; --radius-full: 9999px;

  /* Type: rem so user font-size settings are respected */
  --font-sans: ui-sans-serif, system-ui, -apple-system, 'Segoe UI', sans-serif; /* placeholder */
  --font-display: ui-serif, Georgia, 'Times New Roman', serif;                  /* placeholder */
  --font-mono: ui-monospace, 'SFMono-Regular', Menlo, monospace;
  --text-xs: .75rem; --text-sm: .875rem; --text-base: 1rem; --text-lg: 1.25rem;
  --text-xl: 1.5625rem; --text-2xl: 1.9375rem; --text-3xl: 2.4375rem;
  --text-4xl: 3.0625rem; --text-5xl: 3.8125rem; --text-6xl: 4.75rem;
  --text-display: clamp(2.5rem, 1.5rem + 4vw, 4.75rem);
  --leading-tight: 1.1; --leading-snug: 1.2; --leading-normal: 1.5; --leading-relaxed: 1.65;
  --tracking-tight: -0.02em; --tracking-normal: 0; --tracking-wide: 0.02em;

  /* Light color */
  --bg-base: oklch(0.985 0.002 0);
  --bg-surface: oklch(1 0 0);
  --bg-surface-hover: oklch(0.975 0 0);
  --bg-subtle: oklch(0.965 0.002 0);
  --text-primary: oklch(0.15 0 0);
  --text-secondary: oklch(0.45 0 0);
  --text-tertiary: oklch(0.52 0 0);
  --border-default: oklch(0.91 0 0);      /* decorative only */
  --border-control: oklch(0.60 0 0);      /* inputs, checkboxes: >= 3:1 */
  --accent: oklch(0.55 0.20 var(--hue));
  --accent-hover: oklch(0.50 0.20 var(--hue));
  --accent-active: oklch(0.45 0.20 var(--hue));
  --accent-subtle: oklch(0.95 0.04 var(--hue));
  --accent-text: oklch(0.50 0.20 var(--hue)); /* accent used as text/links */
  --on-accent: oklch(1 0 0);
  /* semantic: fills (icons, borders, tints) vs text */
  --success: oklch(0.65 0.15 145); --warning: oklch(0.80 0.14 85);
  --danger: oklch(0.60 0.20 25);   --info: oklch(0.65 0.15 230);
  --success-fg: oklch(0.50 0.15 145); --warning-fg: oklch(0.50 0.14 85);
  --danger-fg: oklch(0.50 0.20 25);   --info-fg: oklch(0.50 0.15 230);

  /* Shadows */
  --shadow-xs: 0 1px 2px oklch(0 0 0 / 0.06);
  --shadow-sm: 0 1px 3px oklch(0 0 0 / 0.08), 0 1px 2px -1px oklch(0 0 0 / 0.08);
  --shadow-md: 0 4px 6px -1px oklch(0 0 0 / 0.1), 0 2px 4px -2px oklch(0 0 0 / 0.1);
  --shadow-lg: 0 10px 15px -3px oklch(0 0 0 / 0.1), 0 4px 6px -4px oklch(0 0 0 / 0.1);
  --shadow-xl: 0 20px 25px -5px oklch(0 0 0 / 0.1), 0 8px 10px -6px oklch(0 0 0 / 0.1);

  /* Motion */
  --duration-micro: 150ms; --duration-fast: 200ms; --duration-base: 250ms;
  --duration-moderate: 350ms; --duration-slow: 500ms;
  --ease-out: cubic-bezier(0.16, 1, 0.3, 1);
  --ease-in: cubic-bezier(0.4, 0, 1, 1);
  --ease-spring: cubic-bezier(0.34, 1.56, 0.64, 1);

  /* Z-index */
  --z-base: 0; --z-dropdown: 10; --z-sticky: 20; --z-overlay: 30;
  --z-modal: 40; --z-popover: 50; --z-toast: 60; --z-tooltip: 70;
}

@media (prefers-color-scheme: dark) {
  :root {
    --bg-base: oklch(0.15 0 0);
    --bg-surface: oklch(0.19 0 0);
    --bg-surface-hover: oklch(0.22 0 0);
    --bg-subtle: oklch(0.22 0.005 0);
    --text-primary: oklch(0.96 0 0);
    --text-secondary: oklch(0.76 0 0);
    --text-tertiary: oklch(0.68 0 0);
    --border-default: oklch(0.28 0 0);
    --border-control: oklch(0.55 0 0);
    --accent: oklch(0.72 0.15 var(--hue));
    --accent-hover: oklch(0.76 0.15 var(--hue));
    --accent-active: oklch(0.80 0.15 var(--hue));
    --accent-subtle: oklch(0.26 0.06 var(--hue));
    --accent-text: oklch(0.72 0.15 var(--hue));
    --on-accent: oklch(0.15 0 0); /* dark text on light accent, not white */
    --success: oklch(0.72 0.12 145); --warning: oklch(0.82 0.12 85);
    --danger: oklch(0.68 0.17 25);   --info: oklch(0.72 0.12 230);
    --success-fg: oklch(0.78 0.12 145); --warning-fg: oklch(0.80 0.12 85);
    --danger-fg: oklch(0.76 0.17 25);   --info-fg: oklch(0.78 0.12 230);

    --shadow-xs: 0 1px 2px oklch(0 0 0 / 0.4);
    --shadow-sm: 0 1px 3px oklch(0 0 0 / 0.5), 0 1px 2px -1px oklch(0 0 0 / 0.5);
    --shadow-md: 0 4px 6px -1px oklch(0 0 0 / 0.5), 0 2px 4px -2px oklch(0 0 0 / 0.5);
    --shadow-lg: 0 10px 15px -3px oklch(0 0 0 / 0.55), 0 4px 6px -4px oklch(0 0 0 / 0.55);
    --shadow-xl: 0 20px 25px -5px oklch(0 0 0 / 0.6), 0 8px 10px -6px oklch(0 0 0 / 0.6);
  }
}
/* Need a manual theme toggle? Duplicate the dark block under :root[data-theme="dark"]
   and scope the media query with :root:not([data-theme="light"]). */

/* Focus: outline survives forced-colors; offset keeps it clear of the edge */
:where(a, button, input, select, textarea, summary, [tabindex]):focus-visible {
  outline: 2px solid var(--accent-text);
  outline-offset: 2px;
}
/* WCAG 2.4.11: set to sticky-nav size + 16px so focus is never hidden */
html { scroll-padding-block-start: var(--space-14); }

/* Reference component: every state implemented */
.btn-primary {
  display: inline-flex; align-items: center; justify-content: center; gap: var(--space-2);
  min-block-size: 44px; padding-inline: var(--space-6);
  background: var(--accent); color: var(--on-accent);
  border: 1px solid transparent; border-radius: var(--radius-md);
  font: 500 var(--text-base)/1 var(--font-sans);
  cursor: pointer; text-decoration: none;
  transition: background-color var(--duration-micro) var(--ease-out),
              transform var(--duration-micro) var(--ease-out),
              box-shadow var(--duration-micro) var(--ease-out);
}
@media (hover: hover) {
  .btn-primary:hover:not(:is(:disabled, [aria-disabled="true"], [aria-busy="true"])) {
    background: var(--accent-hover); transform: translateY(-1px); box-shadow: var(--shadow-md);
  }
}
.btn-primary:active:not(:is(:disabled, [aria-disabled="true"], [aria-busy="true"])) {
  transform: scale(0.98); background: var(--accent-active);
}
.btn-primary:is(:disabled, [aria-disabled="true"]) { opacity: .5; cursor: not-allowed; }
.btn-primary[aria-busy="true"] { cursor: progress; }
/* Loading: also change the label ("Saving..."); the spinner is decorative */
.btn-primary[aria-busy="true"]::before {
  content: ""; inline-size: 1em; block-size: 1em; border-radius: 50%;
  border: 2px solid currentColor; border-inline-end-color: transparent;
  animation: spin 700ms linear infinite;
}
@keyframes spin { to { transform: rotate(360deg); } }

@media (forced-colors: active) {
  .btn-primary { border-color: ButtonText; }
}
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    animation-duration: 0.01ms !important; animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important; scroll-behavior: auto !important;
  }
}
```

**Computed pairs (hue 250, from the s.10 script, ratios verified)**

| Pair | Light | Dark |
|---|---|---|
| text-primary / bg-surface | 19.68 | 16.46 |
| text-secondary / bg-subtle | 6.74 | 8.06 |
| text-tertiary / bg-subtle (worst case) | 4.97 | 5.99 |
| on-accent / accent | 4.74 | 7.93 |
| accent-text / bg-subtle | 5.28 | 6.97 |
| border-control / bg-surface (needs 3) | 3.95 | 3.77 |
| semantic `-fg` / bg-surface (lowest) | 5.63 | 7.56 |

### 9.1 Navigation templates: Top, Bottom, Side
Pick one (s.3.6). All three share one behavior: **at the top of the page the rounded bar is invisible and only its parts (brand, links, buttons) show; once the user scrolls, the rounded surface fades in.** Because only `opacity` changes, nothing resizes and nothing reflows. The surface lives on a `::before` layer, so text never sits inside a filtered element and the layer can fall back to blur glass or solid. The Liquid Glass effect is an SVG displacement map, generated at runtime from the element's own size and radius, that the browser applies to the backdrop only. Use real brand and real links, never the placeholder words below.

**Shared base (include once, whichever template you pick)**

```css
[data-nav-sentinel] { position: absolute; inset-block-start: 0; inset-inline-start: 0;
  block-size: 48px; inline-size: 1px; pointer-events: none; }

.site-header { --nav-fg: var(--text-primary);
  --lg-tint: 62%;   /* keep >= the value that passes s.10 on the worst-case backdrop */
  --lg-rim: oklch(1 0 0 / 0.75); --lg-rim-soft: oklch(1 0 0 / 0.25);
  position: fixed; z-index: var(--z-sticky); pointer-events: none; }
@media (prefers-color-scheme: dark) {
  .site-header { --lg-rim: oklch(1 0 0 / 0.28); --lg-rim-soft: oklch(1 0 0 / 0.08); }
}
/* Over a dark hero, the top state uses light text (compute it with s.10) */
.site-header[data-hero="dark"][data-scrolled="false"] { --nav-fg: oklch(0.97 0 0); }

:is(.nav, .dock, .rail) { position: relative; isolation: isolate; pointer-events: auto;
  color: var(--nav-fg); border-radius: var(--radius-full); }
:is(.nav, .dock, .rail)::before { /* the Liquid Glass surface: visible by default (no-JS safe) */
  content: ""; position: absolute; inset: 0; z-index: -1; border-radius: inherit;
  background: color-mix(in oklch, var(--bg-surface) var(--lg-tint), transparent);
  border: 1px solid color-mix(in oklch, var(--lg-rim) 60%, transparent);
  box-shadow:
    inset 0 1px 0 var(--lg-rim),            /* specular top edge */
    inset 0 -1px 0 var(--lg-rim-soft),      /* soft bottom edge */
    inset 0 0 18px var(--lg-rim-soft),      /* inner glow */
    0 10px 30px oklch(0 0 0 / 0.14);
  -webkit-backdrop-filter: blur(14px) saturate(1.6);               /* Safari / Firefox: blur glass */
          backdrop-filter: var(--lg-backdrop, blur(14px) saturate(1.6)); /* Chromium: JS sets the refraction */
  opacity: 1; transition: opacity var(--duration-moderate) var(--ease-out);
}
/* JS sets data-scrolled="false" once it runs: only then is the surface hidden at the top */
.site-header[data-scrolled="false"] :is(.nav, .dock, .rail)::before { opacity: 0; }

.nav-brand { display: inline-flex; align-items: center; min-block-size: 44px;
  font: 600 1.25rem/1 var(--font-display); color: inherit; text-decoration: none; }
.nav-link { display: inline-flex; align-items: center; gap: var(--space-2); min-block-size: 44px;
  padding-inline: var(--space-4); border-radius: var(--radius-full);
  color: inherit; text-decoration: none; }
@media (hover: hover) { .nav-link:hover { background: color-mix(in oklch, currentColor 12%, transparent); } }
.nav-link[aria-current="page"] { text-decoration: underline; text-decoration-thickness: 2px; text-underline-offset: .35em; }
.site-header :where(a, button):focus-visible { outline-color: currentColor; }
.site-header .btn-primary:focus-visible { outline-color: var(--nav-fg); }

@supports not ((backdrop-filter: blur(1px)) or (-webkit-backdrop-filter: blur(1px))) {
  :is(.nav, .dock, .rail)::before { background: var(--bg-surface); }
}
@media (prefers-reduced-transparency: reduce) {
  :is(.nav, .dock, .rail)::before { background: var(--bg-surface); -webkit-backdrop-filter: none; backdrop-filter: none; }
}
@media (forced-colors: active) {
  .site-header { --nav-fg: CanvasText; }
  :is(.nav, .dock, .rail)::before { background: Canvas; border-color: CanvasText; box-shadow: none;
    -webkit-backdrop-filter: none; backdrop-filter: none; }
}
@media (prefers-reduced-motion: reduce) {
  :is(.nav, .dock, .rail)::before { transition-duration: 0.01ms; }
}
```

```js
const header = document.querySelector('.site-header');
const sentinel = document.querySelector('[data-nav-sentinel]');
header.dataset.scrolled = 'false';
new IntersectionObserver(([entry]) => {
  header.dataset.scrolled = String(!entry.isIntersecting);
}).observe(sentinel);

/* Liquid Glass refraction. Chromium only: every other browser keeps the blur glass from the CSS.
   Builds a displacement map from the element's own size and radius, bends the backdrop along the rim,
   leaves the centre calm. Text and icons are never filtered. */
const lgSupported = !!navigator.userAgentData?.brands?.some((b) => b.brand === 'Chromium')
  && !matchMedia('(prefers-reduced-transparency: reduce)').matches
  && !matchMedia('(forced-colors: active)').matches;

function liquidGlass(el, { bezel = 18, strength = 1, scale = 34, blur = 2 } = {}) {
  // bezel: rim width in px - strength: 0.6 to 1.2 - scale: max bend in px (24 to 44) - blur: 0 to 4px
  const id = 'lg-' + Math.random().toString(36).slice(2, 8);
  const svg = document.createElementNS('http://www.w3.org/2000/svg', 'svg');
  svg.setAttribute('aria-hidden', 'true');
  svg.setAttribute('focusable', 'false');
  svg.style.cssText = 'position:absolute;inline-size:0;block-size:0;overflow:hidden';
  svg.innerHTML = `<filter id="${id}" x="0" y="0" width="100%" height="100%" color-interpolation-filters="sRGB">
    <feImage preserveAspectRatio="none" result="map"/>
    <feDisplacementMap in="SourceGraphic" in2="map" scale="${scale}" xChannelSelector="R" yChannelSelector="G"/>
  </filter>`;
  document.body.append(svg);
  const image = svg.querySelector('feImage');

  const draw = () => {
    const w = Math.round(el.offsetWidth), h = Math.round(el.offsetHeight);
    if (!w || !h) return;
    const rad = Math.min(parseFloat(getComputedStyle(el).borderTopLeftRadius) || h / 2, h / 2, w / 2);
    const b = Math.min(bezel, rad);
    const canvas = document.createElement('canvas');
    canvas.width = w; canvas.height = h;
    const ctx = canvas.getContext('2d');
    const img = ctx.createImageData(w, h), d = img.data;
    for (let y = 0; y < h; y++) {
      for (let x = 0; x < w; x++) {
        const px = x + 0.5 - w / 2, py = y + 0.5 - h / 2;
        const qx = Math.abs(px) - (w / 2 - rad), qy = Math.abs(py) - (h / 2 - rad);
        const sd = Math.hypot(Math.max(qx, 0), Math.max(qy, 0)) + Math.min(Math.max(qx, qy), 0) - rad;
        const depth = -sd;                         // px inside the edge
        let dx = 0, dy = 0;
        if (depth < b) {
          let nx, ny;                              // outward normal of the rounded rectangle
          if (qx > 0 || qy > 0) {
            nx = Math.sign(px) * Math.max(qx, 0); ny = Math.sign(py) * Math.max(qy, 0);
            const l = Math.hypot(nx, ny) || 1; nx /= l; ny /= l;
          } else if (qx > qy) { nx = Math.sign(px); ny = 0; } else { nx = 0; ny = Math.sign(py); }
          const t = 1 - Math.max(depth, 0) / b;    // 1 at the rim, 0 at the inner edge of the bezel
          const m = t * t * strength;              // convex profile: strongest at the rim
          dx = -nx * m; dy = -ny * m;              // sample from inside: flip both signs to bend the other way
        }
        const i = (y * w + x) * 4;
        d[i] = 128 + dx * 127; d[i + 1] = 128 + dy * 127; d[i + 2] = 128; d[i + 3] = 255;
      }
    }
    ctx.putImageData(img, 0, 0);
    image.setAttribute('href', canvas.toDataURL());
    el.style.setProperty('--lg-backdrop', `url(#${id}) blur(${blur}px) saturate(1.6) brightness(1.04)`);
  };
  new ResizeObserver(draw).observe(el);            // also runs once on observe
}
if (lgSupported) document.querySelectorAll('.nav, .dock, .rail').forEach((el) => liquidGlass(el));

// Top template only (mobile menu)
const toggle = header.querySelector('.nav__toggle');
const menu = header.querySelector('#nav-menu');
if (toggle && menu) {
  const setMenu = (open) => { toggle.setAttribute('aria-expanded', String(open)); menu.hidden = !open; };
  toggle.addEventListener('click', () => setMenu(menu.hidden));
  header.addEventListener('keydown', (e) => {
    if (e.key === 'Escape' && !menu.hidden) { setMenu(false); toggle.focus(); }
  });
  menu.addEventListener('click', (e) => { if (e.target.closest('a')) setMenu(false); });
}
```

**Tuning the look.** Stronger bend: raise `scale` (up to ~44) or `strength`. Wider refracted rim: raise `bezel`. Calmer: lower `scale` and `blur`. Keep the centre flat so the reading area stays stable. The pill must stay rounded: never lower the radius to get more distortion.

#### Template A: Top (rounded pill, floating)
Best for most sites. Mobile: links collapse into a disclosure menu; the Menu button is always self-contained (own fill and border) so it stays readable over any hero.

```html
<div data-nav-sentinel aria-hidden="true"></div>
<header class="site-header site-header--top" data-hero="light">
  <nav class="nav" aria-label="Main">
    <a class="nav-brand" href="/">Brand</a>
    <ul class="nav__links">
      <li><a class="nav-link" href="#a">Link</a></li>
      <li><a class="nav-link" href="#b">Link</a></li>
    </ul>
    <a class="btn-primary nav__cta" href="#contact">Action</a>
    <button class="nav__toggle" type="button" aria-expanded="false" aria-controls="nav-menu">Menu</button>
  </nav>
  <div class="nav__menu" id="nav-menu" hidden>
    <ul><li><a href="#a">Link</a></li><li><a href="#b">Link</a></li></ul>
  </div>
</header>
```

```css
.site-header--top { inset-inline: 0; inset-block-start: var(--space-4);
  display: flex; flex-direction: column; align-items: center; gap: var(--space-2);
  padding-inline: var(--space-4); }
.nav { display: flex; align-items: center; gap: var(--space-4);
  inline-size: min(100%, 64rem); padding: var(--space-2) var(--space-3) var(--space-2) var(--space-5); }
.nav__links { display: flex; gap: var(--space-1); margin: 0 0 0 auto; padding: 0; list-style: none; }
.nav__cta { border-radius: var(--radius-full); }
.nav__toggle { display: none; margin-inline-start: auto; min-block-size: 44px; min-inline-size: 44px;
  padding-inline: var(--space-4); border: 1px solid var(--border-control); border-radius: var(--radius-full);
  background: var(--bg-surface); color: var(--text-primary); font: inherit; cursor: pointer; }
.nav__menu { pointer-events: auto; inline-size: min(100%, 46rem); padding: var(--space-4);
  border-radius: var(--radius-2xl); background: var(--bg-surface); color: var(--text-primary);
  border: 1px solid var(--border-default); box-shadow: var(--shadow-lg); }
.nav__menu ul { margin: 0; padding: 0; list-style: none; display: grid; gap: var(--space-1); }
.nav__menu a { display: flex; align-items: center; min-block-size: 48px; padding-inline: var(--space-4);
  border-radius: var(--radius-lg); color: inherit; text-decoration: none; }
@media (max-width: 47.99em) {
  .nav__links, .nav__cta { display: none; }
  .nav__toggle { display: inline-flex; align-items: center; }
}
```

#### Template B: Bottom dock (mobile-first, app-like)
Icon + visible label for every item (never icon-only), at most 5 items. Reserve space so content is never hidden behind it.

```html
<div data-nav-sentinel aria-hidden="true"></div>
<header class="site-header site-header--bottom" data-hero="light">
  <nav class="dock" aria-label="Main">
    <a class="nav-link" href="#a" aria-current="page"><svg aria-hidden="true" width="20" height="20"><!-- real icon --></svg><span>Label</span></a>
    <a class="nav-link" href="#b"><svg aria-hidden="true" width="20" height="20"><!-- real icon --></svg><span>Label</span></a>
    <a class="nav-link" href="#c"><svg aria-hidden="true" width="20" height="20"><!-- real icon --></svg><span>Label</span></a>
  </nav>
</header>
```

```css
.site-header--bottom { inset-inline: 0; inset-block-end: max(var(--space-4), env(safe-area-inset-bottom));
  display: flex; justify-content: center; padding-inline: var(--space-3); }
.dock { display: flex; gap: var(--space-1); padding: var(--space-1); max-inline-size: 100%; }
.dock .nav-link { flex-direction: column; gap: 2px; min-inline-size: 64px; padding-block: var(--space-2);
  font-size: var(--text-xs); }
@media (min-width: 40em) { .dock .nav-link { flex-direction: row; gap: var(--space-2); font-size: var(--text-sm); } }
body { padding-block-end: 6rem; }
html { scroll-padding-block-end: 6rem; }
```

#### Template C: Side rail (editorial, docs, desktop-heavy)
A vertical rounded bar on the inline-start edge. Below 64em it turns into a bottom bar of links. Offset the page content so the rail never covers it.

```html
<div data-nav-sentinel aria-hidden="true"></div>
<header class="site-header site-header--side" data-hero="light">
  <nav class="rail" aria-label="Main">
    <a class="nav-brand" href="/">Brand</a>
    <ul class="rail__links">
      <li><a class="nav-link" href="#a">Link</a></li>
      <li><a class="nav-link" href="#b">Link</a></li>
    </ul>
    <a class="btn-primary" href="#contact">Action</a>
  </nav>
</header>
```

```css
.site-header--side { inset-inline-start: var(--space-4); inset-block-start: 50%; transform: translateY(-50%); }
.rail { display: flex; flex-direction: column; gap: var(--space-3); inline-size: max-content; max-inline-size: 12rem;
  max-block-size: calc(100dvh - var(--space-8)); overflow-y: auto;
  padding: var(--space-4) var(--space-3); border-radius: var(--radius-2xl); }
.rail__links { display: grid; gap: var(--space-1); margin: 0; padding: 0; list-style: none; }
@media (min-width: 64em) { main { padding-inline-start: 14rem; } }
@media (max-width: 63.99em) {
  .site-header--side { inset: auto var(--space-3) max(var(--space-3), env(safe-area-inset-bottom)); transform: none; }
  .rail { flex-direction: row; justify-content: center; inline-size: auto; max-inline-size: none;
    padding: var(--space-1); border-radius: var(--radius-full); overflow: visible; }
  .rail .nav-brand, .rail .btn-primary { display: none; }
  .rail__links { display: flex; }
  body { padding-block-end: 6rem; }
  html { scroll-padding-block-end: 6rem; }
}
```

**Checks specific to the templates (run in the review):** (1) top state: surface invisible, only the parts show; compute nav text vs the worst-case hero backdrop with s.10; if the hero is a photo or busy, add a scrim inside the hero, never in the nav, so the worst case is known; (2) scrolled state: compute nav text vs the surface at `--lg-tint` over the worst-case backdrops (pure white, pure black, and the most saturated color the page can show behind it), since refraction can move any of them under the text; raise `--lg-tint` until it passes; (3) no-JS state shows the surface; (4) in a non-Chromium browser the blur glass looks intentional (not "broken glass"); (5) `prefers-reduced-transparency` and `forced-colors` give a solid surface; (6) the nav is still rounded in every state; (7) `scroll-padding` >= nav size + offset; (8) real brand and links, no placeholder words; (9) at most 2 Liquid Glass surfaces on the page (s.0.4).

---

## 10. Contrast script (Tier A: run it, show inputs and ratio)

Tokens are OKLCH, so convert to sRGB before applying the WCAG formula. Save as `contrast.mjs`, edit `pairs`, run `node contrast.mjs`. Results within 0.2 of a threshold count as failing because browser gamut mapping differs slightly from clamping. Add the nav pairs (top state over the worst-case hero, scrolled state over the worst-case glass) and any text over images.

```js
const oklchToRgb = (L, C, hDeg) => {
  const h = (hDeg * Math.PI) / 180, a = C * Math.cos(h), b = C * Math.sin(h);
  const l = (L + 0.3963377774 * a + 0.2158037573 * b) ** 3;
  const m = (L - 0.1055613458 * a - 0.0638541728 * b) ** 3;
  const s = (L - 0.0894841775 * a - 1.291485548 * b) ** 3;
  const lin = [
    4.0767416621 * l - 3.3077115913 * m + 0.2309699292 * s,
    -1.2684380046 * l + 2.6097574011 * m - 0.3413193965 * s,
    -0.0041960863 * l - 0.7034186147 * m + 1.707614701 * s,
  ];
  return lin.map((v) => {
    v = Math.min(1, Math.max(0, v));
    return Math.round(255 * (v <= 0.0031308 ? 12.92 * v : 1.055 * v ** (1 / 2.4) - 0.055));
  });
};
const relL = (rgb) => {
  const [R, G, B] = rgb.map((v) => { v /= 255; return v <= 0.04045 ? v / 12.92 : ((v + 0.055) / 1.055) ** 2.4; });
  return 0.2126 * R + 0.7152 * G + 0.0722 * B;
};
const ratio = (a, b) => { const [x, y] = [relL(a), relL(b)].sort((p, q) => q - p); return (x + 0.05) / (y + 0.05); };

const H = 250; // keep in sync with --hue
// [label, foreground L/C/h, background L/C/h, minimum]
const pairs = [
  ["text-tertiary on bg-subtle (light)", [0.52, 0, 0], [0.965, 0.002, 0], 4.5],
  ["on-accent on accent (light)", [1, 0, 0], [0.55, 0.2, H], 4.5],
  ["accent-text on bg-subtle (light)", [0.5, 0.2, H], [0.965, 0.002, 0], 4.5],
  ["border-control on bg-surface (light)", [0.6, 0, 0], [1, 0, 0], 3],
  ["text-tertiary on bg-subtle (dark)", [0.68, 0, 0], [0.22, 0.005, 0], 4.5],
  ["on-accent on accent (dark)", [0.15, 0, 0], [0.72, 0.15, H], 4.5],
  ["border-control on bg-surface (dark)", [0.55, 0, 0], [0.19, 0, 0], 3],
];
for (const [name, fg, bg, min] of pairs) {
  const f = oklchToRgb(...fg), b = oklchToRgb(...bg), r = ratio(f, b);
  console.log(`${r >= min + 0.2 ? "PASS" : "FAIL"}  ${name}: (${f}) vs (${b}) -> ${r.toFixed(2)}:1 (min ${min})`);
}
```

If you cannot run code, compute by hand with the same formulas and label the result "estimated, not executed". Never present an estimate as verified.

---

## Changelog
**v5-LG** - **Liquid Glass edition.** The navigation surface is now Liquid Glass: always rounded, tinted, lit by a specular rim, and refracting the backdrop through an SVG displacement map generated at runtime from the element's own size and radius (`liquidGlass()` in s.9.1, Chromium only; blur glass elsewhere). The surface still stays invisible at the top of the page and fades in on scroll. New s.0.4 scope: floating layers only, max 2 surfaces per page, fit-first (solid rounded surface when the brief is flat or sober), distortion on the backdrop only, tint raised until contrast passes on worst-case backdrops. Added solid fallbacks for reduced transparency, forced colors, and no `backdrop-filter`. Everything else is v5.
**v5** - **Adapt to the request** (s.0): a futuristic style (neon, glow, cyan/purple gradients, dark glass) is declared awful by default and allowed only when the user asks, and then restrained; the style must come from the brief; new **Slop test** (s.0.2) and a "Fit test" in the review; "Futuristic" removed from the default intents; direction seeds are chosen by fit, with two new fitted seeds (Local Craft, Civic Clear) and caveats on the dark/techy ones. **Reasoning discipline** (s.0.3): think short and only about important decisions and risks, never write code in the reasoning, code is written once in the output. **Mandatory Review** (Phase 7, replaces the QA gate): hostile reread of the produced code, concrete defects with fixes, a <= 5-line report in chat. **Navigation templates** (s.3.6, s.9.1): Top, Bottom dock, Side rail, with a new shared behavior: the rounded bar is invisible at the top of the page except its parts, and its surface fades in on scroll (opacity only, no resize, no layout-animation exception, no-JS safe, text contrast computed in both states). Direction Card shortened to 5 lines. Variety roll now filters by fit first.
**v4.5** - Clean Output (Tier A), Variety engine (s.3.5), default morphing navigation (large pill at the top, compact glass pill on scroll), interaction delights, anti-defaults.
**v4** - Rebuilt around creative direction: Ambition dial, mandatory divergence of three directions, Direction Card, signature move, deviation ledger, direction seeds, anti-sameness tests. Tier A as a short verifiable floor, computed skeleton tokens, contrast script taking OKLCH directly.
