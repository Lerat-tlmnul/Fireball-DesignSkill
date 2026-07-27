---
name: ui-design-engineering
description: Use this skill whenever the user asks to design, build, redesign, or critique any user interface — web pages, app screens, components, dashboards, forms, landing pages, design systems, or style guides. Trigger for production-ready HTML/CSS/Tailwind/React UI code, color palettes, typography systems, spacing, motion, accessibility audits, screenshot reviews, and interface improvements.
---

# UI Design Engineering

Treat interface design as applied science, not personal taste.

Every spacing value, color choice, typography decision, and animation timing should be based on:
- Cognitive psychology
- Optical principles
- Mathematical systems
- Accessibility standards

The goal is not simply to "make it beautiful", but to engineer interfaces that feel natural, clear, and trustworthy.

---

# Workflow

Follow these steps in order for every design request.

Skip steps only when they clearly do not apply.

## 1. Contextual Analysis

Before designing:

- Identify the target audience
- Identify the platform:
  - Web
  - iOS
  - Android
  - Desktop
- Identify the main cognitive friction point

Example:

> An enterprise pricing page and a mobile game store page do not have the same user goals.

---

## 2. Structural Blueprint

Define structure before visuals.

Decide:

- Layout grid
- Information hierarchy
- User flow
- Content priority

A simple but well-structured interface is better than a beautiful interface with poor user flow.

---

# Core Design Systems

## Spacing — 8pt Grid

Use multiples of 8:

```
4px
8px
16px
24px
32px
48px
64px
96px
128px
```

Use 4px only for:

- Borders
- Icon spacing
- Small typography adjustments

Avoid random values.

Bad:

```css
margin: 17px;
```

Good:

```css
margin: 16px;
```

---

# Typography System

Use a modular scale.

Default ratio:

```
1.250 Major Third
```

Example:

```
12px → Caption
16px → Body
20px → H4
25px → H3
31px → H2
39px → H1
```

## Text Rules

Readable line length:

```
45–75 characters per line
```

Recommended:

```css
max-width: 65ch;
```

Line-height:

Body:
```
1.5–1.6
```

Headings:

```
1.1–1.2
```

Dense data:

```
1.2
```

---

# Color Engineering

Colors must be functional.

Use:

- HSL
- OKLCH

Avoid using raw hex values as the main design system.

---

## 60/30/10 Rule

```
60% Neutral background
30% Secondary / Brand color
10% Accent
```

Accent colors should mainly represent:

- Buttons
- Actions
- Important states

Do not use accent colors everywhere.

---

# Dark Mode

Dark mode is not simply inverted light mode.

Rules:

- Increase shadow brightness
- Reduce saturated colors by 20–30%
- Avoid extreme contrast vibration

---

# Motion Design

Animation timings:

## Micro interactions

```
150–250ms
```

## Page transitions

```
300–500ms
```

Use:

Entering elements:

```
ease-out
```

Leaving elements:

```
ease-in
```

Avoid linear animations.

---

# Accessibility

## Interactive States

Every interactive element needs:

| State | Behavior |
|-|-|
| Default | Normal appearance |
| Hover | +5% brightness or subtle movement |
| Focus | Visible keyboard outline |
| Active | scale(0.98) |
| Disabled | 40–50% opacity |
| Loading | Skeleton placeholders |

---

# Accessibility Rules

## Semantic HTML

Prefer:

```html
<button>
<nav>
<main>
<section>
<article>
```

Avoid creating fake buttons using:

```html
<div>
```

---

## Touch Targets

Minimum:

```
44×44 CSS pixels
```

---

## Never rely only on colors

Bad:

```
Red = Error
Green = Success
```

Better:

```
Color + Icon + Text
```

---

# Code Standards

When generating:

- HTML
- CSS
- Tailwind
- React

Always create production-ready code.

Requirements:

- Semantic HTML
- CSS variables
- Responsive design
- Dark mode support
- Accessible interactions
- Proper image dimensions

---

# Tailwind Rules

Avoid arbitrary values:

Bad:

```html
mt-[17px]
```

Good:

```html
mt-4
```

Follow:

- 8pt spacing system
- Modular typography scale
- Consistent tokens

---

# Responsive Design

Support:

```
320px → 2560px
```

Handle:

- Mouse
- Touch
- Keyboard

---

# Design Critique Framework

Never critique with:

> "It looks clean"

Evaluate using principles.

---

## Cognitive Load

Use:

- Hick's Law
- Miller's Law

Check:

- Too many choices
- Poor grouping
- Information overload

---

## Visual Hierarchy

Use:

- Von Restorff Effect
- Serial Position Effect

Ask:

- Is the primary action obvious?
- Are important elements prioritized?

---

## Spatial Mathematics

Check:

- 8pt grid consistency
- Line length
- Typography scale

---

## Accessibility

Check:

- Contrast ratio
- Focus states
- Touch targets
- Color accessibility

---

# Design Philosophy

A good interface is not decoration.

It is a system where:

- Every spacing value has meaning
- Every color has a purpose
- Every animation communicates something
- Every component behaves predictably

Design should feel obvious before users understand why.
