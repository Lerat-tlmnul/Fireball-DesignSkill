---
name: UI Design Engineering v2 ECO
description: >
  Economy version of UI Design Engineering. Treat UI as engineering, not taste.
  Every decision must be justified by cognitive psychology, HCI, and product goals.
  Adapt design language to brand, audience, and intent. Max quality, min tokens.
---

# UI Design Engineering v2 - ECO

## Core Law
Every value must have a reason. No decoration without function.
A beautiful but confusing UI = failure. A functional but bland UI = incomplete.

## 1. Anti-Default Rule (Blocking)
NEVER default to:
- Generic SaaS hero + 3 cards + gradient
- Glassmorphism / purple glow everywhere
- Same Inter font / same 16px rhythm
A fintech, a game, a luxury brand MUST NOT look alike.

## 2. Workflow (4 steps, mandatory)
1.  **Context:** Audience? Product goal? Main action? Emotion? (1 sentence each)
2.  **Intent:** Detect: Professional / Premium / Playful / Technical / Editorial / Experimental / Luxury / Energetic
3.  **Structure:** Hierarchy (Primary/Secondary/Tertiary) + Flow (Discover > Understand > Act > Feedback)
4.  **System:** Tokens > Components > States

## 3. Adaptation Engine
| Intent | Spacing | Typography | Color | Motion |
|---|---|---|---|---|
| **Professional** | 8pt tight | Clear hierarchy, 65ch max | 60/30/10, low chroma | 150-250ms ease-out |
| **Premium** | Large, 32/64/96 | Elegant, large titles, tight leading | Restrained, neutrals | Slow, smooth 400ms |
| **Technical** | Dense 8/16 | Mono accents, high density | High contrast, functional | Crisp, 0 bouncy |
| **Playful** | Medium, grouped | Expressive, dynamic rhythm | High chroma accent | Bouncy, 200ms |
| **Editorial** | Generous whitespace | 45-75ch, 1.6 line-height | Soft, content-first | Minimal |
| **Luxury** | Very large | Refined, light weight | Black/white/beige + 1 accent | Intentional, slow |

## 4. Token System (Use these, no random values)
Spacing: 4, 8, 16, 24, 32, 48, 64, 96, 128
Radius: sm=8, md=16, lg=24, full=999
Shadows: sm=0 1px 2px /0.05, md=0 4px 12px /0.1, lg=0 16px 32px /0.12
Transition: micro 150ms, base 250ms, page 400ms

## 5. Execution Laws
- **Content First:** No Lorem Ipsum. No fake stats. Every heading/button must support user goal or business goal.
- **Hierarchy:** Primary action = strongest contrast + position. No equal weight for everything.
- **A11y:** Semantic HTML (<button>, <nav>), 44px touch target, focus-visible ring, color+icon+text for status.
- **Responsive:** 320px > 2560px. Don't shrink desktop. Adapt density/nav/hierarchy.
- **Real Product:** Include hover, focus, active (scale 0.98), disabled (0.5 opacity), loading, empty, error states. No "coming soon".
- **Perf:** No layout shift, images with dimensions, animate only transform/opacity.

## 6. Final Checklist (Must pass all)
[ ] Adapted to prompt, not generic template?
[ ] Primary action obvious in <3s?
[ ] 8pt grid respected?
[ ] Typography 45-75ch and intentional?
[ ] Color 60/30/10 and functional?
[ ] All interactive states defined?
[ ] A11y contrast + keyboard OK?
[ ] Feels like a real shipped product?

If any NO -> fix before delivering.
