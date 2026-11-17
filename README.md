# CSS-cms v2

**Who needs HTML, JavaScript, or AI-scrapable DOM nodes when your entire multi-page website lives inside CSS?**

> **Live Demo:** https://shangle.me/CSS-cms/  
> **Experience V1 (April 11, 2013) in pristine glory:** [./v1/index.html](./v1/index.html) (Live: https://shangle.me/CSS-cms/v1/)

---

## Overview

In **2013**, **CSS-cms v1** poked fun at the "pure CSS replaces JavaScript" hype by stuffing an entire website into a 53-byte `index.html` compiled with LESS and Crunch.

In **2026**, **CSS-cms v2** returns for the **Agentic Web**. Every `<article>`, `<h1>`, and `<p>` published in normal HTML is immediately harvested by RAG pipelines, summarized by search wrappers, and cloned in one prompt by autonomous coding agents. CSS-cms v2 makes your website **functionally invisible to HTML-only AI scrapers** while looking like a full-featured, multi-page web application to human visitors.

Check [`index.html`](./index.html) yourself—the entire HTML document is **134 bytes**, with zero `<div>`s, zero `<p>`s, zero `<input>`s, zero `<script>`s, and zero body copy:

```html
<!doctype html><meta charset=utf-8><link rel=stylesheet href=app.css><link rel=prev href=v1/><title>CSS cms v2</title><a href=v1/></a>
```

---

## What's Inside V2

- **Hijacked `<head>` Sticky Glassmorphic Navbar:** Overrides the UA stylesheet (`head { display: flex }`, `title { display: block }`, `link { display: block }`) so `<title>` renders directly on screen as the brand button and `<link>` elements act as interactive navigation tabs.
- **Zero-`<a>`, Zero-`<input>` Multi-Page Routing:** Uses `@property --page` (`<integer>`), `:has(:active)`, an asymmetric `transition-delay: 999999s` latch (with a `--page: 0` sentinel state), and Baseline `@container style(--page: N)` queries to switch between **4 full views** (*Overview*, *AI Immunity*, *V1 Time Capsule*, *Under the Hood*).
- **Zero-JS Live Telemetry & Stopwatch:** Scroll-driven animations (`animation-timeline: scroll(root)`) power both a sticky progress bar and a live `0%–100%` scroll readout via `counter(pct)%`, while stepped `@keyframes` drive a ticking `00:00` session timer in the footer.
- **Animated Inline Vector Graphics (`css/svg.css`):** Terminal mockups, a threat radar, KPI cards, benchmark tables, a 2013 museum frame, and a DOM schematic—all built as SMIL-animated SVG data URIs inside CSS custom properties, sized responsively with container query units (`cqw`).
- **No Build Step:** Replaces V1's Crunch + LESS pipeline with native `@layer` ordering + `@import`, `light-dark()`, `oklch()`, `color-mix()`, and `@supports`-gated Chromium enhancements (`@function`, `if()`, `@container scroll-state(stuck: top)`, `corner-shape: squircle`).

---

## The V1 Time Capsule (2013)

The original 2013 release is preserved completely untouched inside [`v1/`](./v1/):

- [`v1/index.html`](./v1/index.html) — The original 53-byte HTML file (no doctype, Quirks Mode, unclosed `<title>`).
- [`v1/app.css`](./v1/app.css) — Compiled via Crunch (`http://crunchapp.net/`) with `68.06888381267834px` LESS unit-math floats.
- [`v1/assets/`](./v1/assets/) — Original `.less` modules (`app.less`, `colors.less`, `sizes.less`, `content.less`, `style.less`), including all preserved 2013 quirks (`line-spacing` typo, `font-weight: 0`, unused `@content-text`, and the 47% single-page web prediction).

Open [`v1/index.html`](./v1/index.html) (or click the **Experience V1 (2013) in Pristine Glory** CTA on V2) to view it identically to April 11, 2013.

---

## Disclaimer

Do **not** use this in production unless you actively despise SEO, screen readers, copy-paste, and your coworkers. (Also, vision-capable browser agents that take screenshots can still read pixels—that feature is scheduled for v3.)
