---
name: v6-Mercury
description: Economy tier. Liquid Glass UI + compressed REI (Message → Plan → Check) + FireBall Lite (2 gates). One build + at most one fix pass. Full mandatory rounded Liquid Glass nav with rim distortion. Use for landing pages, sites, dashboards, app screens when credits are tight.
---

# v6 Mercury · Liquid Glass Economy

Tier: economy. You build the whole interface yourself, fast. Reasoning is compressed to three visible stages and one repair pass. The Liquid Glass nav and its distortion are never cut.

**Tier contract**
- Keep: the mandatory nav (markup, `nav.css`, `nav.js`, tokens), design rules, motion budget, accessibility floor, build order.
- Compress: reasoning stages (3 instead of 5), no critique essay, no per-criterion evidence table.
- Passes: 1 build + 1 targeted fix. Ship after that.

## 1. Brief

If subject, audience or tone is missing, ask one question. Never build from nothing. State assumptions in one line.

## 2. Pipeline (visible, terse)

**[M] Message** — One sentence: goal + audience + deliverable. Then 2 bullets: constraints, assumptions.

**[P] Plan** — The 5-line decide block (this is your Architecture):
- Direction name + one sentence.
- Type pair (display + text), real fallback stacks.
- Palette hue from the brief. Not navy or violet by default.
- Layout + hero archetype.
- Nav preset (Subtle / Standard / Strong) + one-signature move.
- File map: `tokens.css`, `base.css`, `nav.css`, `nav.js`, `hero.css`, `sections.css`, `motion.css`, `index.html`, `main.js`.

**FireBall Lite** (two lines, inside [P]):
- `Map:` symbols, types, scopes, dependencies, hard constraints.
- `Gate:` chosen strategy, checks run, known risks.

**[C] Check** — Binary gate:
- Nav rounded in every state; surface hidden at top, visible when scrolled; `feDisplacementMap` present.
- No undefined `var(--x)` or class; every file linked.
- Contrast 4.5:1 text / 3:1 large + UI, worst-case backdrop.
- No lorem, TODO, console, debug, section labels.
- Motion: ≥3 `@keyframes`, ≥4 animated declarations, reduced-motion rule.
- Identity visible on first screen, signature move not captioned.

If any check fails → fix once → re-run the failing checks only → ship. If a defect survives the fix pass, ship and list it in the Report as a known gap. Do not loop further at this tier.

## 3. Build order

Write each file once, in this order: `tokens.css`, `base.css`, `nav.css`, `nav.js`, `hero.css`, `sections.css`, `motion.css`, `index.html`, `main.js`.

## 4. Design rules (compressed)

- **Fit before style.** Style comes from the brief. No futuristic look by default.
- **No AI slop.** Two or more of: dark bg + glow + glass cards; centered hero + 3 feature cards + logo cloud + testimonials; identical rounded cards everywhere; emoji icons; filler words ("Revolutionize", "Seamless", "Unleash", "AI-powered"); invented stats → rework layout, type, palette, material.
- **Identity.** One signature move on the first screen, never captioned. One strong accent or two hue families above the fold.
- **Clean output.** No section labels, version stamps, swatches, debug panels, placeholder tags, design commentary.
- **Type.** Contrasting pair. `clamp()` display sizes. Body 45–75 characters per line.
- **Colour.** OKLCH tokens. Tinted neutrals. Separate fills from text (`--success` / `--success-fg`). Dark mode engineered, not inverted. Colour never the only signal.
- **Motion.** Every animation explains a relationship, gives feedback, guides attention or sets mood. 150–250ms buttons, 300–500ms sections, 500–800ms entrances. Ease-out default, ease-in exits. Only `transform` and `opacity`. Reduced motion removes movement, keeps gentle fades.
- **Accessibility (WCAG 2.2 AA).** 4.5:1 text, 3:1 large + UI on worst-case backdrop. Real buttons/links, labels, heading order, `lang`, alt text, visible focus, 44px targets, focus never hidden by sticky UI.
- **Writing.** Buttons say what happens. No Lorem, no invented testimonials or logos.

## 5. Liquid Glass nav (mandatory)

Rounded pill, always (`border-radius: var(--radius-full)`). At the top only its parts show; the glass surface is hidden. On scroll the surface fades in with its refraction. Only `opacity` changes, nothing resizes. The rim bends the backdrop — blur alone is not Liquid Glass. Chromium gets the full displacement map; other browsers keep blur glass. Text and icons are never filtered.

```html
<div data-nav-sentinel aria-hidden="true" style="position:absolute;top:0;left:0;height:48px;width:1px"></div>
<header class="site-header" data-hero="light">
  <nav class="nav" aria-label="Main">
    <a class="nav-brand" href="#top">Brand</a>
    <a class="nav-link" href="#work">Work</a>
    <a class="nav-link" href="#contact">Contact</a>
    <a class="btn-primary" href="#contact">Get started</a>
  </nav>
</header>
```

`nav.css`:

```css
.site-header { position: fixed; inset-inline: 0; inset-block-start: 16px; z-index: 50; display: flex; justify-content: center; padding-inline: 16px; pointer-events: none; }
.nav { pointer-events: auto; position: relative; isolation: isolate; display: flex; align-items: center; gap: 24px;
  width: min(100%, 960px); padding: 8px 8px 8px 24px; border-radius: var(--radius-full); color: var(--text-primary); }
.nav::before { content: ""; position: absolute; inset: 0; z-index: -1; border-radius: inherit;
  background: color-mix(in oklch, var(--bg-surface) 62%, transparent);
  border: 1px solid oklch(1 0 0 / 0.5);
  box-shadow: inset 0 1px 0 oklch(1 0 0 / 0.65), inset 0 0 18px oklch(1 0 0 / 0.18), 0 10px 30px oklch(0 0 0 / 0.14);
  -webkit-backdrop-filter: blur(14px) saturate(1.6); backdrop-filter: var(--lg-backdrop, blur(14px) saturate(1.6));
  transition: opacity 250ms var(--ease-out); }
.site-header[data-scrolled="false"] .nav::before { opacity: 0; }
.nav-brand { font-family: var(--font-display); font-size: 1.25rem; color: inherit; text-decoration: none; margin-inline-end: auto; }
.nav-link { color: inherit; text-decoration: none; padding: 8px 12px; border-radius: var(--radius-full); }
.nav-link:hover { background: color-mix(in oklch, currentColor 12%, transparent); }
@media (prefers-reduced-transparency: reduce) { .nav::before { background: var(--bg-surface); -webkit-backdrop-filter: none; backdrop-filter: none; } }
@media (forced-colors: active) { .nav::before { background: Canvas; border-color: CanvasText; } }
```

`nav.js`:

```js
// Liquid Glass nav: scroll state + real refraction (displacement map on the backdrop only).
const header = document.querySelector('.site-header');
const nav = header.querySelector('.nav');
header.dataset.scrolled = 'false';
new IntersectionObserver(([e]) => { header.dataset.scrolled = String(!e.isIntersecting); })
  .observe(document.querySelector('[data-nav-sentinel]'));

function liquidGlass(el, { bezel = 18, strength = 1, scale = 34, blur = 2 } = {}) {
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
        const depth = -sd;
        let dx = 0, dy = 0;
        if (depth < b) {
          let nx, ny;
          if (qx > 0 || qy > 0) {
            nx = Math.sign(px) * Math.max(qx, 0); ny = Math.sign(py) * Math.max(qy, 0);
            const l = Math.hypot(nx, ny) || 1; nx /= l; ny /= l;
          } else if (qx > qy) { nx = Math.sign(px); ny = 0; } else { nx = 0; ny = Math.sign(py); }
          const t = 1 - Math.max(depth, 0) / b;
          const m = t * t * strength;
          dx = -nx * m; dy = -ny * m;
        }
        const i = (y * w + x) * 4;
        d[i] = 128 + dx * 127; d[i + 1] = 128 + dy * 127; d[i + 2] = 128; d[i + 3] = 255;
      }
    }
    ctx.putImageData(img, 0, 0);
    image.setAttribute('href', canvas.toDataURL());
    el.style.setProperty('--lg-backdrop', `url(#${id}) blur(${blur}px) saturate(1.6) brightness(1.04)`);
  };
  let queued = false;
  const ro = new ResizeObserver(() => {
    if (queued) return;
    queued = true;
    requestAnimationFrame(() => { queued = false; draw(); });
  });
  ro.observe(el);
  new IntersectionObserver(([e]) => { if (e.isIntersecting) draw(); }).observe(el);
}

const lgSupported = !!navigator.userAgentData?.brands?.some((b) => b.brand === 'Chromium')
  && !matchMedia('(prefers-reduced-transparency: reduce)').matches
  && !matchMedia('(forced-colors: active)').matches;
if (lgSupported) liquidGlass(nav);
```

`tokens.css`:

```css
:root {
  color-scheme: light dark;
  --bg-base: oklch(0.97 0.012 80);
  --bg-surface: oklch(0.995 0.005 80);
  --text-primary: oklch(0.22 0.02 60);
  --text-secondary: oklch(0.42 0.02 60);
  --accent: oklch(0.62 0.16 40);
  --on-accent: oklch(0.99 0.005 80);
  --accent-text: oklch(0.5 0.16 40);
  --border-default: oklch(0.88 0.015 80);
  --radius-full: 9999px;
  --lg-backdrop: blur(14px) saturate(1.6);
  --radius-lg: 24px;
  --font-display: 'Fraunces', Georgia, serif;
  --font-sans: 'Work Sans', system-ui, sans-serif;
  --ease-out: cubic-bezier(0.16, 1, 0.3, 1);
}
@media (prefers-color-scheme: dark) {
  :root { --bg-base: oklch(0.2 0.015 60); --bg-surface: oklch(0.25 0.015 60);
    --text-primary: oklch(0.95 0.01 80); --text-secondary: oklch(0.8 0.015 80);
    --accent: oklch(0.72 0.15 40); --on-accent: oklch(0.2 0.02 60); --accent-text: oklch(0.8 0.14 40); }
}
```

Replace the placeholder hue (`80`/`60`/`40`) with the brief's hue. Keep the structure.

## 6. Presets

| Preset | `scale` | `strength` | `bezel` | `blur` | tint | Use when |
|---|---|---|---|---|---|---|
| Subtle | 22 | 0.6 | 14 | 1 | 70% | text-heavy, busy photos, dense UI |
| Standard | 34 | 1.0 | 18 | 2 | 62% | default landing / brand |
| Strong | 42 | 1.2 | 24 | 3 | 56% | playful surfaces over calm backdrops |

Change one value at a time. Never above `scale` 44 or below tint 52%.

## 7. Templates

- **Top pill** (default): markup above.
- **Bottom dock** (mobile-first apps): fixed bottom pill, 3–5 items, icon + visible label.
- **Side rail** (docs, editorial): vertical pill on inline-start, collapses to a bottom bar below 64em.

All templates: rounded, surface hidden at top, distortion when visible, 44px targets, Escape closes menus, focus returns to the trigger.

## 8. Report (3 lines)

What you built + preset + direction; checks run; known gaps (and whether the fix pass was used).