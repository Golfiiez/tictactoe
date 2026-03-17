# TicTacToe Vue

A small turn-based Tic-Tac-Toe game built as a personal JavaScript learning project.

This project was originally created around 7 years ago while I was studying for my bachelor's degree and trying to learn JavaScript. It started as a simple exercise to understand user interaction, state changes, and basic game logic in the browser.

The current maintenance work is a goodbye performance before this repository is archived.

## Project Status

This repository is now in maintenance-only mode and is being prepared for archive.

## What The App Does

This is a classic 3x3 turn-based Tic-Tac-Toe game:

- `O` always starts first
- players alternate between `O` and `X`
- occupied cells cannot be played again
- the game checks rows, columns, and diagonals after every move
- the winning line is highlighted
- if all 9 moves are used without a winner, the game ends in a tie
- after a win or tie, clicking the board resets the game

## Tech Snapshot

The project currently runs on:

- Vue 3
- Vite
- Node.js 20+
- ESLint

This means the repository now carries a modern tooling refresh on top of an older student project.

## Local Development

Install dependencies:

```bash
npm install
```

Start the development server:

```bash
npm run dev
```

Build for production:

```bash
npm run build
```

Preview the production build locally:

```bash
npm run preview
```

Run lint checks:

```bash
npm run lint
```

## Why Keep It Around

Even though the project is small, it represents an early step in learning how to turn JavaScript ideas into an interactive app with visible game state, win detection, and reset behavior.

## Acknowledgment

This README refresh and final maintenance pass were prepared with assistance from OpenCode (`gpt-5.4`).
