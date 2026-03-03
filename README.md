# Kids Math G2

A standalone HTML math learning app for 2nd graders (ages 7-9).

**[Play now](https://alexey-bass.github.io/kids-math-g2/)**

## Features

- **Addition, Subtraction, Multiplication** — toggle operations on/off
- **3 Difficulty levels** — Easy (up to 20), Medium (up to 50), Hard (up to 100)
- **2 Languages** — English and Polish, selected at startup with flag icons
- **Score & streak tracking** with star rewards
- **Touch-friendly** — on-screen numpad for tablets and phones
- **Zero dependencies** — no build step, no npm install needed

## How to use

Visit the [live version](https://alexey-bass.github.io/kids-math-g2/).

## Local development

The app uses ES modules, so it needs to be served over HTTP (not opened as a `file://` URL). Use any local server:

```bash
npx serve
```

Then open `http://localhost:3000` in your browser.

## Running tests

Tests use the Node.js built-in test runner (Node 18+). No dependencies to install.

```bash
npm test
```
