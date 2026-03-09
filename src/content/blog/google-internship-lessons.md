---
title: "What Google Taught Me About Shipping Code at Scale"
date: 2024-04-10
description: "Lessons from my SWE internship at Google — code reviews, design docs, and why boring infrastructure matters."
tags: ["google", "internship", "engineering"]
---

# What Google Taught Me About Shipping Code at Scale

In the summer of 2022, I interned at Google in Sunnyvale. I shipped a feature that touched an API pipeline processing millions of requests. Here's what I learned.

## Design Docs Before Code

At Google, you don't just start coding. Every meaningful change starts with a design doc. It forces you to think about edge cases, scalability, and alternatives before writing a single line.

## Code Reviews Are a Gift

My first CL (changelist) got 47 comments. I was mortified. But each comment taught me something — naming conventions, error handling patterns, performance considerations I'd never thought about.

## Boring Infrastructure > Flashy Features

The most impactful work at Google isn't the shiny consumer features. It's the internal tools, the monitoring dashboards, the migration scripts. Unglamorous but essential.

## The Culture

- **Psychological safety**: No one mocked a bad idea in a meeting
- **Documentation as culture**: Everything is written down
- **Testing is non-negotiable**: If it's not tested, it doesn't exist

## What I Took With Me

I still write design docs for my personal projects. I still write tests first. And I still hear my tech lead's voice saying, "What happens when this fails?"

*The best engineers aren't the ones who write the most clever code — they're the ones who prevent problems before they happen.*
