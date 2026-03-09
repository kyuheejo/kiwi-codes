---
title: "Why I Chose Tauri Over Electron for Desktop Apps"
date: 2024-12-01
description: "Tauri gave me native performance and tiny binaries. Here's why I switched and what I learned building two apps with it."
tags: ["tauri", "desktop", "rust"]
---

# Why I Chose Tauri Over Electron

Electron apps are convenient to build but painful to ship. My Slide Studio app was 200MB as an Electron bundle. After switching to Tauri, it dropped to 8MB.

## The Case for Tauri

- **Tiny bundles**: Uses the system webview instead of bundling Chromium
- **Rust backend**: Fast, safe, and memory-efficient
- **Web frontend**: Still write your UI in React/Vue/vanilla JS
- **Cross-platform**: macOS, Windows, Linux from one codebase

## What I Built

Two desktop apps now run on Tauri:

1. **Slide Studio** — A Markdown-to-slides presenter with live preview
2. **TTT (Tauri Translate Tool)** — An offline translator using llama.cpp

## The Learning Curve

Rust was the biggest hurdle. Coming from Python and JavaScript, the borrow checker felt like a strict teacher. But after a week, it clicked. The compiler errors are actually helpful — they prevent the bugs you'd spend hours debugging in other languages.

## When to Use Tauri

- You want a lightweight desktop app
- Your UI is web-based
- You care about binary size and performance
- You're okay learning some Rust

## When NOT to Use Tauri

- Heavy native UI requirements (use Swift/Qt instead)
- You need Electron's massive ecosystem of plugins
- Your team can't invest time in learning Rust

*Tauri isn't just a lighter Electron — it's a different philosophy about what desktop apps should be.*
