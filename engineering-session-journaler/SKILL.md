---
name: engineering-session-journaler
description: Use when documenting an engineering work session that should become durable project memory, including planning, investigation, implementation, debugging, validation, operations, or hardware work, especially when questions were asked, options were considered, actions were taken, outcomes were observed, failures occurred, decisions were made, or project history may need updating.
---

# Engineering Session Journaler

Preserve durable engineering memory. Do not reduce the session to only the final outcome when the path, questions, failures, or decisions matter to future work.

## When To Use

Use this skill when the session includes any of:

- planning a feature, fix, or migration
- clarifying questions that affect scope or design
- comparing approaches or making tradeoffs
- implementation work with verification
- debugging or investigation
- validation, ops, or hardware work
- unresolved questions that should be preserved for next time

Do not use this for generic meeting notes, casual chat, or trivial work with no continuity value.

## Core Rule

If the session should count as durable project memory, preserve enough evidence that a future engineer can understand what happened, why it happened, and what remains.

If a fact matters but is unknown, mark it unknown. Do not guess.

## Required Core Evidence

Unless truly not applicable, preserve:

1. environment, target system, or relevant context
2. goals of the session
3. important questions asked or constraints clarified
4. options considered when they affected the decision
5. actions taken or commands run
6. observed outcomes
7. failures, false starts, or challenges that mattered
8. decisions made and why
9. next steps or open questions

## Session Mode Selection

| Mode | Use When | Expected Output |
| --- | --- | --- |
| Full | planning plus work, meaningful investigation, or durable continuity needed | detailed session record in the repo's natural docs/history location |
| Short | focused work still worth preserving | shorter note or history entry |
| Micro | too small for a standalone record | small continuation note only if needed |

Default to **Full** when the work would be hard to reconstruct later from the final diff, issue state, or final outcome alone.

## Workflow

### 1. Gather the session facts

Collect or confirm:

- date
- title or scope
- environment/context
- goals
- questions asked
- options considered
- actions taken
- outcomes observed
- failures or challenges
- decisions
- next steps or open questions

Ask for missing high-value facts instead of smoothing over them.

### 2. Choose the right documentation destination

Adapt to the repository instead of forcing one format.

Use the repo's existing conventions when available:

- session logs or worklogs
- project journal or history file
- design docs or ADRs for planning-heavy decisions
- changelog or release history
- handoff or continuation docs when the main need is seamless resumption
- issue tracker references or handoff docs

If the repo has no clear session-log convention, preserve the session in the most appropriate existing project-history location. Do not create a new documentation structure unless the user wants one.

### 3. Preserve the planning path when it matters

If the session included clarifying questions, competing approaches, or a recommendation, preserve the useful parts of that path.

Do not keep raw conversation transcripts. Preserve the engineering substance:

- key questions
- important constraints
- options considered
- why one direction was chosen
- what remains unresolved

### 4. Preserve execution and validation evidence

Keep the actions that matter:

- exact commands when available
- files or systems affected
- verification run
- observed behavior
- important failed attempts and the correction path

Do not keep noisy scratch work unless it teaches something reusable.

### 5. Evaluate project-history impact

If the session produced durable project changes, update the repo's history surface when appropriate.

Examples:

- `CHANGELOG.md`
- release notes
- architecture notes
- work journal
- project history document

Ask: "Would a future contributor expect this change or decision to appear in project history?"

### 6. Run a lightweight documentation audit

Before considering the session documented, do a narrow check for likely omissions.

Examples:

- a decision was made but captured nowhere durable
- a session note exists but the compact project-history entry was skipped
- a changelog-worthy change was not reflected in history
- open questions were discussed but not preserved
- a related existing session record should be extended instead of creating a duplicate

Keep this audit lightweight. Do not turn it into a full archaeology pass.

## Suggested Output Heuristics

### For planning-heavy sessions, preserve:

- problem being solved
- constraints and assumptions
- questions asked
- options considered
- chosen direction and rationale
- unresolved questions

### For implementation or debugging sessions, preserve:

- actions taken
- verification run
- outcomes observed
- failures encountered
- corrections made
- remaining risks or follow-ups

### For validation, ops, or hardware sessions, preserve:

- environment
- commands or procedures run
- observed behavior
- deviations from expectation
- proof of outcome
- next steps

## Quick Reference

| If the session includes... | Preserve at minimum |
| --- | --- |
| planning and clarifying questions | goals, constraints, questions, options, decision |
| implementation work | actions, affected area, verification, next steps |
| failed attempts | the important failure and what corrected it |
| unresolved items | explicit open questions or follow-ups |
| durable project change | project-history update if the repo uses one |

## Common Mistakes

### Mistake: keeping only the final answer

Fix: preserve the planning path when the decision would otherwise be hard to reconstruct.

### Mistake: preserving every raw detail

Fix: keep useful engineering continuity, not noisy transcript-level chronology.

### Mistake: dropping failed attempts entirely

Fix: keep the failures that changed understanding, exposed a pitfall, or affected the final decision.

### Mistake: forcing one file pattern on every repo

Fix: adapt to the repository's actual documentation conventions.

### Mistake: forgetting open questions

Fix: unresolved items are often the most important bridge to the next session.
