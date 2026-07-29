# Project Workflow Guidelines

These rules apply to every Claude Code session in this project. Follow them
by default — do not ask whether to follow them, only ask about the specific
approvals called out below.

## 1. Plan before you build

If any requirement, design choice, or implementation detail is unclear or
ambiguous:
- Do NOT start writing code directly.
- Instead, propose 1-3 concrete suggestions/options with brief tradeoffs.
- Wait for my explicit approval or choice.
- Write a short plan (steps, files to touch, approach) based on my answer.
- Only after I approve the plan, generate the actual code from it.

Skip this step only when the task is fully unambiguous (e.g. "fix this typo",
"rename this variable").

## 2. Testing — use data-driven tests where possible

Before writing implementation code, check for and prefer skills/patterns for
data-driven / table-driven testing so generated code can be validated quickly
against multiple cases rather than one-off manual checks. Look for relevant
skills before defaulting to ad hoc test writing (see Section 4).

## 3. Final review by a fresh subagent

After a feature/task is implemented and appears to work:
- Spawn a NEW subagent (fresh context, not the one that wrote the code) whose
  only job is to review the finished work — correctness, edge cases, style,
  and whether it matches the approved plan.
- Report the review findings to me before considering the task fully done.
- The review subagent should be read-only (no Edit/Write) — see settings.json.

## 4. Actively look for relevant skills

Before implementing, search for and consider using skills/plugins for:
- Test-driven development workflow
- Data-driven / table-driven testing
- Coding language standards / style guides for the language in use
- General development workflow best practices
- Security review of generated code

If a relevant skill exists, prefer it over improvising the same thing from
scratch.

## 5. Permission philosophy

No agent in this project should ever run with full/unrestricted access.
Every agent operates under the permission rules in `.claude/settings.json`.
In particular, always ask for my explicit approval before:
- Accessing or reading any folder/file outside this project directory
- Editing or writing to any file
- Using any tool that fetches data from the internet (WebFetch, WebSearch, etc.)
- Running any command that could affect anything outside this project

This applies even if a task seems small or the answer seems obvious.

## Updating these guidelines

I will edit this file directly to add or remove guidelines at any point.
Always treat the current contents of this file as the source of truth for
project workflow — re-read it if unsure.
