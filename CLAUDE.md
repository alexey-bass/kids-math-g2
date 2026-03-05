# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Kids math practice app for 2nd graders. Single-page HTML app with zero dependencies and no build step. Deployed to GitHub Pages via CI on push to `main`.

Live: https://alexey-bass.github.io/kids-math-g2/

## Commands

- **Run tests:** `npm test` (uses Node.js built-in test runner, requires Node 18+)
- **Local dev server:** `npx serve` then open http://localhost:3000 (ES modules require HTTP, not file://)

## Architecture

- **`index.html`** — entire app: HTML, CSS, and game logic in a `<script type="module">`. Contains i18n strings (English/Polish), UI state management, DOM event handlers, and numpad input.
- **`math.js`** — pure functions extracted for testability: `rand`, `pick`, `getRange`, `generateProblem`, `checkAnswer`. Imported by both `index.html` and tests.
- **`math.test.js`** — tests for `math.js` using `node:test` and `node:assert/strict`.

## Key Details

- Operations use Unicode symbols: `+`, `−` (U+2212 minus), `×` (U+00D7 multiply) — not ASCII `-` or `x`
- Subtraction always produces non-negative results (b <= a)
- Multiplication on medium/hard difficulty excludes ×1 (mulMin = 2)
- The answer input is `readonly` — all input comes through the on-screen numpad (prevents mobile keyboard)
