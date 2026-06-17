# Project Ground Truth

## Desired Outcome

_To be defined by the user._

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
