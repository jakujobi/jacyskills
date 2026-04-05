---
name: engineering-clarifier
description: Use when engineering work needs clarification before or during planning, design, implementation, or decision-making, especially when requirements are ambiguous, tradeoffs must be explained, preferences are unknown, or meaningful decisions remain blocked by missing context.
---

# Engineering Clarifier

Research first, then clarify. Do not jump straight into vague questions or a giant interview dump.

The goal is not only to collect answers. The goal is to help the user understand the important decisions, tradeoffs, and consequences well enough to choose confidently.

## When To Use

Use this skill when:

- the task is ambiguous
- multiple directions are possible
- the user has not fully specified constraints or preferences
- planning or design needs clarification before implementation
- a mid-project decision needs user input
- the user explicitly asks to be interviewed or clarified

Do not use this when the requirement is already clear enough to proceed without meaningful uncertainty.

## Core Rule

Research before questioning. Ask only the questions that still matter after checking context.

Default to grouped question rounds, not a full interview plan.

For each question, provide a recommendation and a reason for that recommendation.

## Research Order

Before asking questions, check in this order:

1. the current user request and conversation context
2. repo files and docs, if relevant
3. web research only if the clarification depends on external facts, standards, APIs, technical comparisons, or market context

Do not do web research when the repo and conversation already answer the important questions.

## Build A Clarification Map

Before asking anything, identify:

- what is already known
- what is uncertain
- what decisions actually matter
- what is blocked by ambiguity
- what questions are unnecessary

Common buckets:

- goals and success criteria
- scope and priorities
- constraints
- user preferences
- technical tradeoffs
- rollout or testing decisions

## Default Interaction Mode

Default to one grouped round of related questions at a time.

After the user answers:

1. update your understanding
2. remove questions that are no longer needed
3. ask the next grouped round only if real ambiguity remains

Do not ask all possible questions up front unless the user explicitly asks for a full interview plan.

## Optional Modes

### Grouped Rounds (default)

Use for most work.

Best when early answers may eliminate later questions.

### Full Interview Plan

Use only when the user explicitly asks to see the full interview plan up front.

### Fast Clarify

Use when only one narrow decision or a few missing facts block progress.

## Grouped Round Rules

Each grouped round should:

1. focus on one decision area or one tightly related set of areas
2. usually contain 2 to 5 questions
3. start with a short note on why this round matters
4. avoid mixing unrelated domains in the same batch

Good examples of round themes:

- goals and success criteria
- scope and constraints
- UX/product direction
- technical tradeoffs
- rollout and testing

## Per-Question Format

For each question, include all of the following.

### 1. Question

State the decision or clarification clearly.

### 2. Plain-Language Explanation

Explain what the question means in a way that is easy for a lay person to understand.

### 3. Options

Provide multiple concrete options when structured choices exist.

Usually give 2 to 5 options.

### 4. Pros And Cons

For each option, explain what it helps with and what it gives up.

### 5. Consequences

For each option, explain the likely downstream impact on the project.

### 6. Recommendation

Recommend one option when enough context exists.

### 7. Reason For Recommendation

State why that option is recommended in the current context.

Do not make the reason implicit. Say it explicitly.

## Decision Heuristics

Use a decision-heavy style by default.

That means:

1. recommend when enough context exists
2. explain why the recommendation fits the user's goals
3. be explicit when uncertainty is still high
4. do not pretend all options are equally good when they are not

Default heuristic order:

1. fit to the user's goal
2. simplicity and maintainability
3. risk reduction
4. alignment with existing project conventions
5. long-term flexibility only when it materially matters

## Stopping Rules

Stop asking questions when:

1. enough clarity exists to proceed
2. only trivial preferences remain
3. the next step is better served by a concrete proposal or plan

When you stop, summarize:

- what is now clear
- what was decided
- what is still open
- what should happen next

## Quick Reference

| If the situation is... | Then do this |
| --- | --- |
| ambiguous planning request | research first, then ask one grouped round |
| mid-project tradeoff | use a focused grouped round or fast clarify |
| user wants full discovery upfront | switch to full interview plan mode |
| context already answers the question | do not ask it |
| one option is clearly better | recommend it and explain why |

## Common Mistakes

### Mistake: asking vague questions

Fix: ask a concrete decision question with explained options.

### Mistake: asking too many questions in one pass

Fix: use grouped rounds by default and defer later questions until after answers.

### Mistake: skipping the explanation

Fix: explain why the question matters in plain language before expecting the user to choose.

### Mistake: listing options without consequences

Fix: describe what each option changes downstream.

### Mistake: giving a recommendation without a reason

Fix: explicitly say why the recommendation fits the current project context.

### Mistake: doing web research too early

Fix: check current context and repo docs first.
