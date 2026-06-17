# Project Ground Truth

> **Shipped — 25-question planning flow complete, all 13 chunks executed, repo live at https://github.com/jackwayne234/ground-truth-md. This file is the live example for that repo and will continue to be updated as the project evolves.**

## Desired Outcome

Display how the ground-truth.md system works for any project, and post it on GitHub.

## Chunk Plan

Current default rule for this project folder: after the enough-information checkpoint is satisfied and before permission to start work is requested, Hermes should break the project into many small execution chunks.

Each chunk should include:

- Chunk number and goal
- Likely files, scripts, commands, CLIs, or tools involved
- Whether an existing script/tool should be used or a new script should be created
- Verification step
- Status: pending, in progress, complete, blocked, or deferred

Script-first rule: before doing manual work in any chunk, Hermes should look for existing scripts, commands, CLIs, Makefiles, tests, or automation that can do the work deterministically. Prefer script/tool execution over repetitive AI-only work.

Permission wording for new work: **“Do I have your permission to start working from this ground truth and chunk plan?”**

## Progress Log

### 2026-05-30
- Created this `ground-truth.md` file as the source of truth for the project.
- Next step: ask the user to define the desired outcome.
- Project rule: log meaningful progress throughout this project in this file.

### 2026-05-31
- Created `ground-truth.md` files for 63 immediate project folders in `/home/jackwaynelinuxdesktop/workspace` that did not already have one.
- Skipped folders that already had a ground truth file, including `Eisenhower priority matrix to do list`.
- Planning mode started: ask 10 questions, one at a time, about what should be written into the project ground-truth files.

## 10-Question Ground Truth Fill-In Plan

### Question 1 of 10 — Fill-in style

**Question:** How should we fill these ground-truth files?

**Options offered:**
1. Same simple template for every folder — **recommended**
2. Customize each folder one by one
3. Group similar folders together, then customize by group
4. Other

**Recommendation:** Start with the same simple template for every folder, then customize only the important projects later.

**User answer:** 1 — Same simple template for every folder.

**Locked decision:** Use the same simple ground-truth template for every folder first, then customize only important projects later.

### Question 2 of 10 — Core sections

**Question:** What sections should every ground-truth file include?

**Options offered:**
1. Desired Outcome, Current Status, Next Actions, Progress Log — **recommended**
2. Desired Outcome and Progress Log only
3. Full project plan: outcome, scope, tasks, risks, links, log
4. Other

**Recommendation:** Use option 1 because it is useful without making every folder feel heavy.

**User answer:** 4 — Other: “I want it to be what hermes reads and executes as soon as i start talking to hermes in that folder. I want the ground truth file to describe the purpose of the ground truth file. and to ask me the desired outcome of the project. then ask me 25 questions. record each question and answer. confirm that it was enough information. then ask for permission to start.”

**Locked decision:** Every project `ground-truth.md` should act as Hermes’ project-start instruction file for that folder. It should explain its own purpose, ask for the desired project outcome, ask 25 planning questions, record each question and answer, confirm whether the collected information is enough, and then ask the user for permission before starting work.

### Question 3 of 10 — When to run the 25-question flow

**Question:** When Hermes opens a folder with a `ground-truth.md`, should the 25-question flow happen automatically every time, or only when the file has no completed planning answers yet?

**Options offered:**
1. Only when the project is new or missing answers — **recommended**
2. Every time I start talking in that folder
3. Ask me first whether to continue planning or start work
4. Other

**Recommendation:** Use option 1 so Hermes does not keep restarting the same 25 questions after a project already has answers.

**User answer:** 1 — Only when the project is new or missing answers. Also explain the purpose of the ground-truth file to make sure Hermes and the user are on the same page.

**Locked decision:** The 25-question flow should run only when the project is new or missing planning answers. At the start of each project, Hermes should explain the purpose of the `ground-truth.md` file before asking for the desired outcome.

### Question 4 of 10 — Purpose wording

**Question:** How should the ground-truth file describe its purpose?

**Options offered:**
1. “This file is the project’s source of truth. Hermes should read it first, follow the recorded decisions, ask missing planning questions, log progress, and wait for permission before starting work.” — **recommended**
2. “This file stores the project goal and progress log.”
3. “This file is a planning contract between the user and Hermes.”
4. Other

**Recommendation:** Use option 1 because it clearly tells Hermes what to do without sounding too formal.

**User answer:** User prefers this wording: “A `ground-truth.md` file is the project’s source of truth. It tells Hermes what the project is, what decisions have already been made, what still needs to be asked, what progress has happened, and whether Hermes has permission to start working. The point is to stop Hermes from guessing, restarting, forgetting context, or building before you’ve approved the direction.”

**Locked decision:** Use the user-preferred detailed purpose wording in the reusable `ground-truth.md` template.

### Question 5 of 10 — Desired outcome prompt

**Question:** How should the template ask you for the desired outcome?

**Options offered:**
1. “What do you want the desired outcome of this project to be?” — **recommended**
2. “What should be true when this project is finished?”
3. “Describe the final result you want in plain English.”
4. Other

**Recommendation:** Use option 1 because it matches your existing project-start wording.

**User answer:** 1 — “What do you want the desired outcome of this project to be?”

**Locked decision:** Use this desired-outcome prompt: “What do you want the desired outcome of this project to be?”

### Question 6 of 10 — Planning question style

**Question:** What style should the 25 planning questions use?

**Options offered:**
1. One question at a time with short multiple-choice options and a recommended answer — **recommended**
2. One question at a time, open-ended only
3. All 25 questions shown at once
4. Other

**Recommendation:** Use option 1 because it keeps planning easy and matches how you like Hermes to work.

**User answer:** 1 — One question at a time with short multiple-choice options and a recommended answer.

**Locked decision:** The 25 planning questions should be asked one at a time, with short multiple-choice options and a clearly marked recommended answer.

### Question 7 of 10 — Recording answers

**Question:** How detailed should the recorded question-and-answer section be?

**Options offered:**
1. Record the question, options, recommendation, user answer, and locked decision — **recommended**
2. Record only the user answer and locked decision
3. Record a short summary after all 25 questions
4. Other

**Recommendation:** Use option 1 so future Hermes sessions can see exactly what was asked and decided.

**User answer:** 1 — Record the question, options, recommendation, user answer, and locked decision.

**Locked decision:** Each planning Q&A entry should record the question, options offered, recommendation, user answer, and locked decision.

### Question 8 of 10 — Enough-information checkpoint

**Question:** After the 25 questions are answered, how should Hermes confirm there is enough information?

**Options offered:**
1. Give a short summary of what is known, list any remaining gaps, then ask if it is enough — **recommended**
2. Just say “planning complete” and ask permission to start
3. Create a full project brief before asking permission
4. Other

**Recommendation:** Use option 1 because it gives you a final checkpoint without making the process too heavy.

**User answer:** 1 — Give a short summary of what is known, list any remaining gaps, then ask if it is enough.

**Locked decision:** After 25 questions, Hermes should give a short summary of what is known, list remaining gaps, and ask whether the information is enough before requesting permission to start.

### Question 9 of 10 — Permission wording

**Question:** How should Hermes ask for permission to start work after planning is complete?

**Options offered:**
1. “Do I have your permission to start working from this ground truth?” — **recommended**
2. “Ready for me to build/start?”
3. “Should I continue?”
4. Other

**Recommendation:** Use option 1 because it is clear, explicit, and tied to the ground-truth file.

**User answer:** 1 — “Do I have your permission to start working from this ground truth?”

**Locked decision:** Use this permission prompt after planning: “Do I have your permission to start working from this ground truth?”

### Question 10 of 10 — Apply template to existing folders

**Question:** After we finish this 10-question setup, should I update all existing project `ground-truth.md` files with the final reusable template?

**Options offered:**
1. Yes, update all project folders that have the placeholder ground truth — **recommended**
2. No, only use the template for new folders going forward
3. Show me the final template first, then ask permission to apply it
4. Other

**Recommendation:** Use option 3 if you want to review the wording first; use option 1 if you want me to apply it immediately.

**User answer:** 1 — Yes, update all project folders that have the placeholder ground truth.

**Locked decision:** Update all existing project folders that still have the placeholder `ground-truth.md` with the final reusable Hermes project-start template.

**Applied update:** 63 placeholder `ground-truth.md` files were updated with the final reusable template. The existing non-placeholder `Eisenhower priority matrix to do list/ground-truth.md` was skipped.

## Final Reusable Ground-Truth Template Decisions

- A `ground-truth.md` file is the project’s source of truth. It tells Hermes what the project is, what decisions have already been made, what still needs to be asked, what progress has happened, and whether Hermes has permission to start working. The point is to stop Hermes from guessing, restarting, forgetting context, or building before you’ve approved the direction.
- Hermes should read the file first when working in that folder.
- If the desired outcome is missing, Hermes should ask: “What do you want the desired outcome of this project to be?”
- The 25-question planning flow should run only when the project is new or missing planning answers.
- Planning questions should be one at a time, with short multiple-choice options when useful and a clearly marked recommended option.
- Each Q&A entry should record the question, options offered, recommendation, user answer, and locked decision.
- After 25 questions, Hermes should summarize what is known, list remaining gaps, and ask whether the information is enough.
- If the information is enough, Hermes should break the project into many small execution chunks before asking permission to start.
- Each chunk should be small enough to run, verify, and log independently, and should identify likely scripts/tools/commands first.
- Before doing manual work in a chunk, Hermes should look for existing scripts, CLIs, Makefiles, tests, or automation and prefer deterministic script/tool execution over repetitive AI-only work.
- Before starting work, Hermes should ask: “Do I have your permission to start working from this ground truth and chunk plan?”
- Hermes should not start project work until permission is granted.
### 2026-06-07
- Updated the reusable ground-truth template decision: after the enough-information checkpoint, Hermes must break projects into many small execution chunks before asking permission to start.
- Added script-first execution as a default chunk-planning rule: look for existing scripts/tools/commands before doing repetitive work manually.

### 2026-06-17
- Desired outcome for this project locked: "Display how the ground-truth.md system works for any project, and post it on GitHub."
- 25-question planning flow started.
- All 25 planning questions answered and locked. Decision summary and chunk plan written.
- All 13 chunks executed. Repo `ground-truth-md` created and pushed to GitHub at https://github.com/jackwayne234/ground-truth-md.
- README (62 lines, plain, 3-step quickstart, 4-section walkthrough, ASCII flow diagram), LICENSE (MIT), .gitignore (GitHub standard), templates/ground-truth.md (44 lines, lean), and the live `ground-truth.md` (this file) all live in the repo.
- GitHub repo description, topics (`ai`, `project-planning`, `documentation`, `markdown`), and visibility (`public`) all set.
- Desired outcome achieved: the ground-truth.md system is now displayed as a working GitHub repo using the very file as the live example.

### 2026-06-17 (later)
- Replaced the lean `templates/ground-truth.md` (44 lines, simplified) with the fuller meta-template the user authored (205 lines, includes the 10-question design history + locked decisions + clean per-project structure). Visitors now copy the same file that originally seeded the system, so the rationale for each rule ships with the rule.
- Updated README quickstart to match the actual workflow: create folder → drop file → tell AI to read it → AI does the rest. The 10-question history and locked decisions are for the AI to read, not the visitor.

## 25-Question Planning Flow (Desired Outcome: Display how the ground-truth.md system works for any project, and post it on GitHub)

**Question 1 of 25 — Repo scope**

**Question:** What kind of GitHub repo should this be?
**Options offered:**
1. Static demo repo — README + 2–3 worked example projects (recommended). Shows the system by example, no code to run.
2. Tool repo — code that generates ground-truth.md files for other projects.
3. Hybrid — example projects plus a small generator.
4. Other.
**Recommendation:** Option 1. The desired outcome is to "display how this groundtruth works for any project." A static demo is the fastest, clearest way to do that, and it matches your plain-English usefulness-first style for the Ascended Barron GitHub page.
**User answer:** 1 — Static demo repo (recommended).
**Locked decision:** This is a static demo repo: a README plus 2–3 worked example projects, no code to run.

### Question 2 of 25 — Repo name

**Question:** What should the GitHub repo be named?
**Options offered:**
1. ground-truth-md (recommended) — short, matches the file name, no special characters.
2. ground-truth-demo — makes the demo purpose explicit in the name.
3. groundtruth-md — drops the hyphens, single word.
4. Other.
**Recommendation:** Option 1. It is the shortest version that still reads clearly and matches the file name.
**User answer:** 1 — ground-truth-md.
**Locked decision:** Repo name is ground-truth-md.

### Question 3 of 25 — Account

**Question:** Where should the repo live on GitHub?
**Options offered:**
1. Your personal GitHub account (recommended for now) — fastest to publish, keeps the demo under your name.
2. Ascended Barron org (if one exists) — puts it under the brand.
3. A new org just for this project.
4. Other.
**Recommendation:** Option 1. You can move it later if you want it under a brand org.
**User answer:** 1 — Your personal GitHub account.
**Locked decision:** Repo lives on your personal GitHub account. Easy to move later.

### Question 4 of 25 — Example projects

**Question:** What mix of example projects should the demo include?
**Options offered:**
1. Mixed domains (recommended) — software project + writing project + personal-life project. Best proves "works for any project."
2. All software dev, different sizes — small script, medium app, large system. Shows the system scales within one domain.
3. All from the same domain — keep it tight and focused.
4. Other.
**Recommendation:** Option 1 was the standard pick, but the user's own answer wins.
**User answer:** "no examples — this itself is the example." Use this real `ground-truth.md` file (in progress, with the 25-question flow) as the single example in the repo.
**Locked decision:** The repo itself is the example. No synthetic examples. The single example is the real, in-progress `ground-truth.md` (this file) plus its associated `progress log`, `25-question planning flow`, and `chunk plan`. Anyone reading the repo can watch the system being applied to itself.

### Question 5 of 25 — Repo contents

**Question:** What files should the repo contain?
**Options offered:**
1. README + templates/ folder with a clean reusable template (recommended) — visitors get both the live example (this file) and a clean starter they can copy.
2. README only — just this file as the example. Simpler, but visitors have to extract the template themselves.
3. README + examples/ folder containing this real example in a subfolder.
4. Other.
**Recommendation:** Option 1. The clean template in `templates/` is what most visitors will copy. The real `ground-truth.md` (this file) stays at repo root as the live example.
**User answer:** 1 — README + templates/ folder with clean reusable template.
**Locked decision:** Repo contents = `README.md` at root, `templates/` folder with a clean reusable template, and the real `ground-truth.md` at repo root as the live example.

### Question 6 of 25 — README style

**Question:** How long and detailed should the README be?
**Options offered:**
1. Short and plain (recommended) — under 200 lines, scannable, links to template and live example.
2. Medium — full walkthrough of every section and how to use it, no edge cases.
3. Long — comprehensive guide covering edge cases, customization, and FAQs.
4. Other.
**Recommendation:** Option 1. Matches your plain-English usefulness-first style. Visitors can dive into the live example or copy the clean template.
**User answer:** 1 — Short and plain (recommended).
**Locked decision:** README is short and plain, under 200 lines, scannable, links to the template and the live example.

### Question 7 of 25 — Template folder

**Question:** What should the templates/ folder contain?
**Options offered:**
1. Single clean template file (recommended) — `templates/ground-truth.md`. One starter visitors can copy and customize.
2. Multiple variants — `templates/solo.md`, `templates/team.md`, `templates/oss.md`. More useful, but more to maintain.
3. Template + variants for different project sizes (small, medium, large).
4. Other.
**Recommendation:** Option 1. Start with one, add variants later if visitors ask for them.
**User answer:** 1 — Single clean template file (recommended).
**Locked decision:** templates/ contains a single clean template file: `templates/ground-truth.md`. Variants can be added later if needed.

### Question 8 of 25 — License

**Question:** What license should the repo use?
**Options offered:**
1. MIT (recommended) — permissive, well-understood, works for both code and text.
2. CC0 — public domain dedication, fits the "template anyone can copy" feel.
3. CC-BY-4.0 — attribution required, also fits templates.
4. Other.
**Recommendation:** Option 1. MIT is the simplest, most familiar choice for a small docs/template repo.
**User answer:** 1 — MIT (recommended).
**Locked decision:** License is MIT. Add a LICENSE file at repo root.

### Question 9 of 25 — Repo description

**Question:** What should the GitHub "About" sidebar description say?
**Options offered:**
1. Long version (recommended) — "A `ground-truth.md` file is the source of truth for any project — it stops AI assistants from guessing, restarting, forgetting context, or building before you've approved the direction." Uses the locked purpose wording.
2. "Plan any project with an AI assistant and stop losing context."
3. "The simplest way to keep AI coding assistants on track."
4. Other.
**Recommendation:** Option 1. It is the locked purpose wording, so the README and the GitHub sidebar reinforce each other.
**User answer:** 1 — Long version (recommended).
**Locked decision:** GitHub "About" description = the locked purpose wording, full sentence, set in repo settings.

### Question 10 of 25 — Repo topics

**Question:** What GitHub topics/tags should the repo have?
**Options offered:**
1. ai, project-planning, documentation, markdown (recommended) — broad, helps anyone working with AI assistants and project docs find it.
2. ai-assistant, claude-code, cursor, copilot — tool-specific, helps people using those tools find it.
3. No topics — keep it minimal.
4. Other.
**Recommendation:** Option 1. Broad topics give the most reach. Tool-specific topics can be added later if useful.
**User answer:** 1 — ai, project-planning, documentation, markdown.
**Locked decision:** GitHub topics = `ai`, `project-planning`, `documentation`, `markdown`.

### Question 11 of 25 — Quickstart structure

**Question:** How should the README's quickstart section be structured?
**Options offered:**
1. 3-step quickstart (recommended) — (1) copy template into your project, (2) run the 25-question flow, (3) ask for permission to start. Easy to scan.
2. 5-step quickstart — adds (4) chunk plan and (5) progress log as named steps.
3. No numbered steps — flow explained in paragraphs.
4. Other.
**Recommendation:** Option 1. The chunk plan and progress log are already part of the template; they don't need to be top-level quickstart steps.
**User answer:** 1 — 3-step quickstart.
**Locked decision:** README quickstart is exactly 3 steps: copy template, run 25-question flow, ask permission.

### Question 12 of 25 — Visual style

**Question:** Should the README include diagrams or images?
**Options offered:**
1. Plain text + 1 ASCII flow diagram (recommended) — shows the "ask 25 questions → chunk plan → permission → progress log" loop visually. No images, no external assets.
2. Plain text only — no diagrams, no images. Most minimal.
3. Plain + screenshots or GIFs showing the flow in a real tool. More work, looks more polished.
4. Other.
**Recommendation:** Option 1. One small ASCII flow diagram adds a lot of clarity for almost no cost.
**User answer:** 1 — Plain text + 1 ASCII flow diagram.
**Locked decision:** README includes exactly one ASCII flow diagram showing the loop. No images, no external assets.

### Question 13 of 25 — Branching

**Question:** What Git branching strategy should the repo use?
**Options offered:**
1. Main only (recommended) — single `main` branch, direct commits, simple for a docs/template repo.
2. Main + docs branch — keep doc polish on a separate branch.
3. Main + feature branches + PRs — full open-source contribution workflow.
4. Other.
**Recommendation:** Option 1. A docs/template repo doesn't need branches or PRs.
**User answer:** 1 — Main only.
**Locked decision:** Repo uses a single `main` branch. Direct commits, no PRs required.

### Question 14 of 25 — How it works structure

**Question:** How should the README's "How it works" section be structured?
**Options offered:**
1. 4-section walkthrough (recommended) — purpose / 25-question flow / chunk plan / progress log. One short section per piece, matches the template structure.
2. Single paragraph summarizing the loop.
3. Detailed walkthrough — 6+ sections covering every detail.
4. Other.
**Recommendation:** Option 1. Each section mirrors a section in the template, so the README and the template reinforce each other.
**User answer:** 1 — 4-section walkthrough.
**Locked decision:** README "How it works" has exactly 4 sections: purpose, 25-question flow, chunk plan, progress log.

### Question 15 of 25 — AI assistant wording

**Question:** How should the README refer to the AI assistant?
**Options offered:**
1. Use "your AI assistant" (recommended) — works for any tool (Cursor, Copilot, Claude Code, Hermes, etc.). More useful as a generic template.
2. Keep "Hermes" — matches the actual live example file, but narrows the audience.
3. Use "the AI" — neutral and short.
4. Other.
**Recommendation:** Option 1. The live example in this repo is the only place "Hermes" is named. The README should be tool-agnostic.
**User answer:** 1 — Use "your AI assistant."
**Locked decision:** README uses "your AI assistant" throughout. The live example (this file) is the only place "Hermes" is named.

### Question 16 of 25 — Repo hygiene

**Question:** Should the repo include any standard config files?
**Options offered:**
1. Just .gitignore (recommended) — standard GitHub template, covers Mac/Windows/Linux/editor junk. No extra noise.
2. No extra config files — pure markdown only.
3. .gitignore + .editorconfig + CODEOWNERS — full open-source hygiene.
4. Other.
**Recommendation:** Option 1. The standard GitHub .gitignore template is enough.
**User answer:** 1 — Just .gitignore.
**Locked decision:** Repo includes a single .gitignore (GitHub's standard template). No .editorconfig, no CODEOWNERS, no other config.

### Question 17 of 25 — Community files

**Question:** Should the repo include CONTRIBUTING.md or issue templates?
**Options offered:**
1. None (recommended) — small docs repo, no need for formal community files.
2. Small CONTRIBUTING.md only — short, points visitors at the ground-truth template as the way to contribute.
3. Full set — CONTRIBUTING + bug/feature issue templates + PR template.
4. Other.
**Recommendation:** Option 1. The 25-question flow inside the template is the contribution model — no separate CONTRIBUTING.md needed.
**User answer:** 1 — None.
**Locked decision:** No CONTRIBUTING.md, no issue templates, no PR template. The 25-question flow inside the template is the contribution model.

### Question 18 of 25 — Template completeness

**Question:** How filled-in should `templates/ground-truth.md` be?
**Options offered:**
1. Lean with light instructions (recommended) — purpose, prompts, section rules, 1-2 lines of guidance each.
2. Fully annotated — every line has comments for first-time users.
3. Bare-bones — just section headings, no instructions.
4. Other.
**Recommendation:** Option 1. Light instructions help first-time users without making the template heavy.
**User answer:** 1 — Lean with light instructions.
**Locked decision:** templates/ground-truth.md is a lean starter with 1–2 lines of guidance in each section. Not annotated, not bare.

### Question 19 of 25 — Live example link

**Question:** How should the README link to the live example (this file)?
**Options offered:**
1. Inline link + 1-2 sentence description (recommended) — "See [ground-truth.md](./ground-truth.md) for a real, in-progress example."
2. Quoted excerpt — show 5–10 lines of the live example right in the README.
3. Side-by-side — template on the left, live example excerpt on the right.
4. Other.
**Recommendation:** Option 1. A simple inline link is enough; the example speaks for itself.
**User answer:** 1 — Inline link + 1-2 sentence description.
**Locked decision:** README links to `./ground-truth.md` with a 1-2 sentence description. No quoted excerpt, no side-by-side.

### Question 20 of 25 — Initial state

**Question:** How should the first commit / initial repo state be structured?
**Options offered:**
1. One initial commit (recommended) — README + LICENSE + .gitignore + templates/ + this live `ground-truth.md`. Clean, single commit, easy to clone.
2. README first, then follow-up commits for the rest — shows build-up but adds noise.
3. Use GitHub "Initialize with README" + push the rest — fine, but mixed workflow.
4. Other.
**Recommendation:** Option 1. One clean initial commit is the most useful starting point.
**User answer:** 1 — One initial commit.
**Locked decision:** First commit contains all repo files: README.md, LICENSE, .gitignore, templates/ground-truth.md, and the live `ground-truth.md`.

### Question 21 of 25 — Versioning

**Question:** Should the template/README carry a version number?
**Options offered:**
1. No version number (recommended) — keep it simple. The file is the source of truth; visitors copy the latest.
2. Semver in a VERSION file — formal version tracking.
3. Git tags only — version via releases, no VERSION file.
4. Other.
**Recommendation:** Option 1. A docs/template repo does not need formal versioning.
**User answer:** 1 — No version number.
**Locked decision:** No version number, no VERSION file, no release tags. Visitors always copy the latest.

### Question 22 of 25 — Closing CTA

**Question:** What should the README end with?
**Options offered:**
1. Single line (recommended) — "Copy the template, drop it in your project, and start your own ground-truth.md."
2. Short paragraph — copy the template + run the 25-question flow + ask permission.
3. "Questions? Open an issue." — invite engagement.
4. Other.
**Recommendation:** Option 1. The closing line is the most important part of the README. Keep it short and actionable.
**User answer:** 1 — Single line.
**Locked decision:** README ends with one line: "Copy the template, drop it in your project, and start your own ground-truth.md."

### Question 23 of 25 — Audience

**Question:** Who is the README written for?
**Options offered:**
1. Anyone using an AI assistant (recommended) — broadest, matches the "any project" outcome. Plain enough for non-developers, technical enough for developers.
2. Developers only — assumes tech literacy, can use jargon.
3. Non-developers only — assumes little tech literacy, no jargon.
4. Other.
**Recommendation:** Option 1. The system is project-agnostic and tool-agnostic; the README should be too.
**User answer:** 1 — Anyone using an AI assistant.
**Locked decision:** README is written for anyone using an AI assistant. Plain English, no jargon, no assumed tech background.

### Question 24 of 25 — Live example state

**Question:** How should the repo show that the live example is in progress?
**Options offered:**
1. Header note (recommended) — add a small "In progress — 25-question flow at Q23 of 25" note at the top of the live example. Transparent, honest, shows the system mid-use.
2. Commit a "completed" snapshot as the example file, keep the real one in a separate folder.
3. Trim the live example to just the first 5 questions for readability.
4. Other.
**Recommendation:** Option 1. Honesty about the in-progress state is a feature, not a bug — it shows the system working in real time.
**User answer:** 1 — Header note.
**Locked decision:** Add a small "In progress — 25-question flow at Q24 of 25" header note at the top of the live `ground-truth.md` once committed to the repo.

### Question 25 of 25 — Enough-information checkpoint

**Question:** Is the info we have enough, or do you want to revise?
**Options offered:**
1. Yes, info is enough (recommended) — proceed to summary, remaining gaps, and chunk plan.
2. Add more questions — extend the planning flow before locking.
3. Revise some decisions — go back and change a few answers first.
4. Other.
**Recommendation:** Option 1. 25 questions covers the major decisions for a small static demo repo.
**User answer:** 1 — Yes, info is enough.
**Locked decision:** Planning is complete. Proceed to enough-information summary and chunk plan.

## Enough-Information Summary

**What we know (locked):**
- Repo type: static demo. README + templates/ + this live `ground-truth.md` as the example.
- Repo name: `ground-truth-md`. Lives on your personal GitHub account.
- The repo itself is the example. No synthetic examples.
- Repo contents: `README.md`, `LICENSE` (MIT), `.gitignore` (GitHub standard), `templates/ground-truth.md` (lean with light instructions), and the live `ground-truth.md` at repo root with an "in progress" header note.
- README: short and plain, under 200 lines. 3-step quickstart. 4-section "How it works". One ASCII flow diagram. References "your AI assistant" (tool-agnostic). Ends with one CTA line.
- License: MIT. Topics: `ai`, `project-planning`, `documentation`, `markdown`. Description: the locked purpose wording.
- Branching: `main` only, direct commits. No community files, no version number, no editorconfig.
- First commit contains all files. No releases, no tags.

**Remaining gaps / decisions deferred:**
- Exact wording of the ASCII flow diagram (will draft as part of the README chunk).
- Exact wording of the README opening line (the locked purpose wording is the candidate; will confirm in the README chunk).
- GitHub username (need to confirm before `gh repo create`).
- Whether to add a `CHANGELOG.md` once the project is published (deferred — not needed at launch).
- Repo homepage URL (set automatically from GitHub).
- README badges (none planned unless you ask).

**Is the information enough?** Yes, per your Q25 answer. Proceeding to chunk plan.

## Chunk Plan

Script-first rule: `gh` CLI is available for GitHub operations. Use it for `gh repo create`, `gh repo edit`, `gh auth status`. The standard GitHub .gitignore template is available as a known string. LICENSE text for MIT is a known string.

### Chunk 1 — Confirm GitHub username
- **Goal:** Confirm the GitHub username where the `ground-truth-md` repo will be created.
- **Likely tools:** manual question to the user.
- **Verification:** user states their GitHub username.
- **Status:** complete (jackwayne234)

### Chunk 2 — Verify `gh` CLI auth
- **Goal:** Confirm the `gh` CLI is installed and authenticated.
- **Likely tools:** `gh --version`, `gh auth status`.
- **Verification:** `gh auth status` reports logged-in user matches the username from Chunk 1.
- **Status:** complete (gh 2.46.0, authenticated as jackwayne234)

### Chunk 3 — Write LICENSE file
- **Goal:** Add an MIT LICENSE file at repo root.
- **Likely tools:** `write_file` with the standard MIT LICENSE text and current year + username.
- **Verification:** File exists, contains standard MIT text with correct year and copyright holder.
- **Status:** complete (MIT, 2026 Christopher Riner)

### Chunk 4 — Write .gitignore
- **Goal:** Add GitHub's standard .gitignore template at repo root.
- **Likely tools:** `write_file` with the standard GitHub .gitignore content (covers Mac, Windows, Linux, common editors).
- **Verification:** File exists and matches the standard GitHub template.
- **Status:** complete

### Chunk 5 — Write templates/ground-truth.md
- **Goal:** Create the clean, lean template at `templates/ground-truth.md` with 1-2 lines of guidance in each section.
- **Likely tools:** `write_file`.
- **Verification:** File exists, sections present (purpose, desired outcome, 25-question flow, chunk plan, progress log), lean instructions only, no in-progress content.
- **Status:** complete (44 lines, lean)

### Chunk 6 — Write README.md
- **Goal:** Create the short, plain README at repo root with: 3-step quickstart, 4-section "How it works", one ASCII flow diagram, one-line CTA, link to live example.
- **Likely tools:** `write_file`.
- **Verification:** File exists, under 200 lines, contains all 4 "How it works" sections, ASCII diagram renders, link to `./ground-truth.md` works, ends with the locked CTA line, uses "your AI assistant" (not "Hermes").
- **Status:** complete (62 lines, all sections present, ASCII diagram renders)

### Chunk 7 — Add in-progress header to live ground-truth.md
- **Goal:** Add a small "In progress — 25-question flow at Q25 of 25" header note to this file.
- **Likely tools:** `patch` (insert note near the top, after the `# Project Ground Truth` heading).
- **Verification:** File contains the header note and still reads correctly.
- **Status:** complete

### Chunk 8 — Initialize git repo
- **Goal:** Initialize a new git repo in `/home/jackwaynelinuxdesktop/Desktop/Ground-truth.md` (or a copy of it in a clean working dir if you prefer), set `main` as the default branch.
- **Likely tools:** `git init -b main`, `git config user.name`, `git config user.email` (only if not already set globally).
- **Verification:** `git status` shows the files we wrote; `git branch --show-current` shows `main`.
- **Status:** complete (main branch, identity set: Christopher Riner / 107547623+jackwayne234@users.noreply.github.com)

### Chunk 9 — First commit
- **Goal:** Stage all files and make the first commit.
- **Likely tools:** `git add .`, `git commit -m "..."`.
- **Verification:** `git log` shows one commit; `git status` is clean.
- **Status:** complete (commit 47e5459, 5 files, 800 insertions)

### Chunk 10 — Create GitHub repo
- **Goal:** Create the `ground-truth-md` repo on your personal account via `gh repo create`. Public, no README (we have one locally).
- **Likely tools:** `gh repo create ground-truth-md --public --source=. --remote=origin --description="..."`.
- **Verification:** `gh repo view ground-truth-md` shows the repo exists and the description is set.
- **Status:** complete (https://github.com/jackwayne234/ground-truth-md, public, description set)

### Chunk 11 — Push to GitHub
- **Goal:** Push the local `main` branch to the `origin` remote.
- **Likely tools:** `git push -u origin main`.
- **Verification:** `git log origin/main` matches local `main`; GitHub web shows the files.
- **Status:** complete

### Chunk 12 — Set GitHub topics
- **Goal:** Add the locked topics (`ai`, `project-planning`, `documentation`, `markdown`) to the repo.
- **Likely tools:** `gh repo edit --add-topic ai --add-topic project-planning --add-topic documentation --add-topic markdown`.
- **Verification:** `gh repo view --json topics` shows the four topics.
- **Status:** complete (all 4 topics set: ai, project-planning, documentation, markdown)

### Chunk 13 — Verify on github.com
- **Goal:** Open the GitHub repo URL in the browser and confirm the README, license, template, and live example all render correctly.
- **Likely tools:** `gh repo view --web` (opens the browser) or just print the URL.
- **Verification:** Browser view shows all files; README renders; ASCII diagram displays; topics visible in the sidebar.
- **Status:** complete (README renders, ASCII diagram displays, all 5 files visible at root + templates/)

**All chunks complete. Repo live at https://github.com/jackwayne234/ground-truth-md.**

**Permission wording:** Do I have your permission to start working from this ground truth and chunk plan?
