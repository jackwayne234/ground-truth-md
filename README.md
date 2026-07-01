# ground-truth.md

This `ground-truth.md` file provides scaffolding and structure for any project using AI

## Quickstart

1. Create a folder for your project.
2. Drop [`templates/ground-truth.md`](./templates/ground-truth.md) into the folder.
3. Open a terminal in that folder, log into your AI assistant, and tell it to read `ground-truth.md`.
4. Your AI assistant does the rest: asks for your desired outcome, runs the 25 planning questions one at a time, summarizes what is known, builds a chunk plan, and asks for permission before starting work.

## How it works

### 1. Purpose

A `ground-truth.md` file is the project's source of truth. It tells your AI assistant what the project is, what decisions have already been made, what still needs to be asked, what progress has happened, and whether your AI assistant has permission to start working.

### 2. 25-question flow

When the project is new (or the answers are missing), your AI assistant runs a 25-question planning flow. Questions are asked one at a time, with short multiple-choice options and a clearly marked recommended answer. Each answer is recorded with the question, options, recommendation, and the locked decision.

### 3. Chunk plan

After the 25 questions, your AI assistant breaks the project into many small execution chunks. Each chunk has a goal, likely tools, a verification step, and a status. Before manual work, your AI assistant looks for existing scripts, CLIs, Makefiles, or tests — and prefers deterministic tool execution over repetitive AI-only work.

### 4. Progress log

As work happens, meaningful progress is logged back into the same file. The file stays the source of truth from start to finish.

```
   ground-truth.md
        │
        ▼
   AI assistant reads
        │
        ▼
   25 planning questions
   (one at a time, with
   recommended answer)
        │
        ▼
   Summary + remaining gaps
   "Is this enough?"
        │
        ▼
   Chunk plan
        │
        ▼
   "Do I have your
   permission to start?"
        │
        ▼
   Work in chunks,
   log progress
```

## See it in action

The repository's own [`ground-truth.md`](./ground-truth.md) is a real, in-progress example — the same file used to plan and build this very repo. Watch the system being applied to itself.

## License

MIT — see [`LICENSE`](./LICENSE).

## The experiment behind this

This method is part of a live, public experiment: **can AI agents earn back their own
$200/month cost?** Everything on this GitHub — including [a cozy puzzle game](https://jackwayne234.itch.io/stormlight-village-chapter-1)
and [a shelf of small business tools](https://rinerchris.gumroad.com) — was built with
this file and an AI agent, and I post the real numbers (including the zeros) on
[TikTok](https://www.tiktok.com/@buckrvepjvy) as the journey unfolds.

If the method helps you ship something, a star helps other people find it.
