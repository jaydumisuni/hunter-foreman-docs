# Lablab / Hackathon Submission Draft

## Project Name

Hunter Foreman

## Tagline

AI operations foreman for small businesses.

## Problem

Small businesses receive requests through websites, WhatsApp, email, phone calls, and social media. The problem is not only receiving the request. The real problem is turning that request into owned work.

Without a clear operating layer, requests get lost, staff miss handoffs, clients wait too long, and owners have to personally chase everything.

## Solution

Hunter Foreman turns incoming requests into structured work.

- ROSE receives the customer request.
- Foreman analyzes the request.
- A workflow is selected.
- A task is created.
- The dashboard updates.
- A connected app receives the task through a versioned bridge contract.
- Human review is requested when confidence is low or the request is sensitive.

## What We Built

Phase 1 includes three public-safe repositories:

1. `hunter-foreman` — main demo app, Foreman routing, ROSE intake, app bridge, Docker, CI.
2. `hunter-foreman-demo` — external receiver app that accepts Foreman task events and displays the timeline.
3. `hunter-foreman-docs` — submission, pitch, demo script, architecture, and judge answers.

## Technical Highlights

- Node.js public demo app.
- Docker-based local startup.
- GitHub Actions smoke and Docker checks.
- Versioned app bridge contract: `foreman.app.task.v1`.
- Receiver app supports task timeline display.
- Public/private boundaries documented.

## Why It Matters

This is more than a chatbot. Hunter Foreman demonstrates an operating layer where AI does not replace the human owner, but helps organize work, surface priorities, and keep humans in control.

## AMD Alignment

The roadmap includes deployment on a compact AMD Ryzen mini PC as a local always-on AI operations assistant for businesses that want ownership, privacy, and reliability while still being able to connect to cloud services when needed.
