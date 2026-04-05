# Repo Documentation Implementation Plan

> **For Claude:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task.

**Goal:** Add a minimal root README and lightweight documentation records for the `jacyskills` public repo.

**Architecture:** Keep documentation centralized at the repo root. Add one README for GitHub discoverability and install guidance, plus a small design/plan record under `docs/plans` for continuity.

**Tech Stack:** Markdown, GitHub, Skills CLI

---

### Task 1: Add Root README

**Files:**
- Create: `README.md`

**Step 1: Write the README content**

Include:
- repo purpose
- included skills
- install commands
- repo layout
- AMBER-specific exclusion note

**Step 2: Verify paths and commands are accurate**

Run: `Get-ChildItem -Recurse -Name`
Expected: shows `README.md` plus the two skill directories and `SKILL.md` files.

**Step 3: Commit**

```bash
git add README.md
git commit -m "add repo readme"
```

### Task 2: Preserve Design And Plan Context

**Files:**
- Create: `docs/plans/2026-04-05-repo-documentation-design.md`
- Create: `docs/plans/2026-04-05-repo-documentation-plan.md`

**Step 1: Write the design note**

Capture the approved decision to use a root-only README.

**Step 2: Write the implementation plan**

Capture the minimal documentation scope and verification steps.

**Step 3: Verify repo tree**

Run: `Get-ChildItem -Recurse -Name`
Expected: shows `README.md` and both files under `docs/plans`.

**Step 4: Commit**

```bash
git add docs/plans/2026-04-05-repo-documentation-design.md docs/plans/2026-04-05-repo-documentation-plan.md
git commit -m "add documentation planning notes"
```
