# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static single-page landing site for **CodeUp** — a Brazilian test automation course platform (Portuguese content). No build tools, no framework, no package manager.

## Development

Open `index.html` directly in a browser or use any local static server:

```
python -m http.server 8080
```

There are no build, lint, or test commands.

## Architecture

Everything lives in one file: `index.html` contains all HTML, CSS (in `<style>`), and JavaScript (in `<script>`). Course thumbnail images are in `imagens/`.

**Key sections (navigated by anchor links):**
- `#cursos` — 2-column course grid, each card links to a Udemy course
- `#consultorias` — contact form submitted via Formspree (`https://formspree.io/f/mrbnebrn`)
- `#sobre` — about section

**JavaScript behaviors (inline at bottom of `<body>`):**
- Testimonials carousel: auto-advances every 4.5 s, dot navigation, CSS `translateX` slide transition
- Particle animation: 200 absolutely-positioned `<div class="particle">` elements injected at runtime with random size/position/speed

**CSS design tokens (CSS custom properties in `:root`):**
- `--bg`, `--panel`, `--ink`, `--muted`, `--brand`, `--accent`, `--line`
- Dark navy theme; brand purple `#6c63ff`