# Homework 7 LaTeX Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Replace the Homework 7 placeholder LaTeX with a complete, student-facing assignment that matches the approved image-analysis spec and the tone/style of earlier homeworks.

**Architecture:** Modify the single Homework 7 LaTeX source in place, preserving the established document preamble and formatting conventions from Homework 1 and Homework 2. Then run a local LaTeX build to catch syntax or formatting errors before completion.

**Tech Stack:** LaTeX, `pdflatex`

---

### Task 1: Draft the assignment content

**Files:**
- Modify: `Homework_7/MOL518_HW2.tex`

- [ ] **Step 1: Review the approved design and current homework shell**

Read:
- `docs/superpowers/specs/2026-04-17-homework-7-image-analysis-design.md`
- `Homework_7/MOL518_HW2.tex`
- `Homework_1/MOL518_HW1.tex`
- `Homework_2/MOL518_HW2.tex`

Expected outcome:
- Confirm the final assignment has 3 problems, friendly wording, lettered subparts, and explicit package guidance.

- [ ] **Step 2: Replace the placeholder body with complete Homework 7 prompts**

Update `Homework_7/MOL518_HW2.tex` so it includes:
- a short intro paragraph consistent with earlier homeworks
- a package guidance note naming the allowed libraries
- `Problem 1` on `Lecture_33/media/microscopy_example.png`
- `Problem 2` on a student-taken photo with FFT-based filtering
- `Problem 3` on a student-built image-processing pipeline using the same photo

Content requirements:
- use friendly, student-facing language
- keep the mechanics central
- avoid copying the lecture exercise wording
- keep all notebook references as `HW7`

- [ ] **Step 3: Review the edited LaTeX for consistency**

Check for:
- matching braces and environments
- consistent homework numbering and filenames
- correct relative paths in prompts
- consistent use of `\texttt{}` for code/package names
- no leftover placeholder text

Expected outcome:
- Source reads cleanly and matches the approved spec.

### Task 2: Verify the document builds

**Files:**
- Verify: `Homework_7/MOL518_HW2.tex`

- [ ] **Step 1: Run LaTeX build**

Run:

```bash
pdflatex -interaction=nonstopmode -halt-on-error MOL518_HW2.tex
```

from:

```bash
Homework_7
```

Expected:
- build completes successfully
- `MOL518_HW2.pdf` is produced or updated

- [ ] **Step 2: Inspect the build log for errors or important warnings**

Check that there are:
- no fatal LaTeX errors
- no obvious formatting issues caused by special characters or malformed lists

- [ ] **Step 3: If build fails, fix the source and rebuild**

Apply the minimal source fix in `Homework_7/MOL518_HW2.tex`, then rerun:

```bash
pdflatex -interaction=nonstopmode -halt-on-error MOL518_HW2.tex
```

Expected:
- clean successful build

### Task 3: Final review

**Files:**
- Review: `Homework_7/MOL518_HW2.tex`

- [ ] **Step 1: Confirm spec coverage**

Verify the final LaTeX includes:
- shared microscopy image problem
- student photo Fourier filtering problem
- open-ended pipeline problem
- explicit allowed-function guidance

- [ ] **Step 2: Confirm tone and scope**

Verify:
- language is friendly and a little playful without becoming vague
- scope remains reasonable for one homework notebook
- interpretation prompts are short and secondary to mechanics

- [ ] **Step 3: Summarize the result for the user**

Report:
- what changed in `Homework_7/MOL518_HW2.tex`
- whether the LaTeX build succeeded
- any remaining cleanup items, if any
