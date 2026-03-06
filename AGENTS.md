# AGENTS.md

## Purpose
This repository contains Jupyter notebooks for the MOL518 intro programming course. Some future lectures will be adapted from older BPY518 image-analysis slide decks in PDF format. When an agent is asked to draft one of those lecture notebooks, follow the workflow below.

## Lecture Drafting Workflow
When asked to draft a lecture notebook from an old PDF slide deck:

1. Read `course_summary.md` first.
   - Use it to remind yourself what students have already seen in the course.
   - Keep the new lecture consistent with the level, notation, and assumptions established earlier in the course.

2. Read the relevant source PDF carefully.
   - Preserve the conceptual flow and major teaching points from the slides.
   - The goal is not a literal slide-by-slide dump. Convert the material into a notebook that teaches well in notebook form.

3. Find the correct destination lecture directory and create a new notebook there.
   - Match the naming and organization patterns already used in the repository.
   - Reuse the style established by the existing notebooks, especially the image-analysis notebooks in `Lecture_31` and any related converted lectures.

4. Build the notebook as a teaching document, not just a transcription.
   - Use markdown cells for narrative, explanations, section structure, and image placement.
   - Use code cells for runnable examples, demonstrations, and adapted code from the source material.
   - Keep the order and logic of the original lecture, but rewrite for clarity where needed.

5. Reuse figures from the PDF.
   - Extract relevant graphics from the PDF and place them in an appropriate `media/` subdirectory for that lecture.
   - Insert the extracted images into the notebook with relative paths.
   - Include only figures that materially support the lecture flow.

6. Recover and reuse code snippets from the PDF.
   - Many code snippets in the PDFs are embedded as images rather than selectable text.
   - Use OCR to read all relevant code snippets.
   - Reuse that code either verbatim or in spirit, depending on what best fits the notebook.
   - Clean up OCR errors and make the final code idiomatic, correct, and runnable.

7. Match the style of Lectures 1-6 and the existing converted notebooks.
   - Prefer clear section headings, short explanatory paragraphs, and runnable code blocks.
   - Keep notebooks student-facing and instructional.
   - Favor consistency over inventing a new format for each lecture.

8. Verify the draft notebook.
   - Ensure image links resolve correctly.
   - Ensure code cells are internally consistent and use the correct local file paths.
   - Remove obvious OCR artifacts, broken formatting, and slide-only clutter.

## Content Expectations
- Assume the notebook should be usable as course material, not just as archival notes.
- Keep the concepts and sequencing from the PDF unless there is a clear teaching reason to slightly reorganize them.
- Prefer concise explanations around code so students can understand why each block exists.
- If a slide contains visual material with little text, preserve the teaching point by pairing the image with short explanatory markdown.

## Practical Defaults
- Store lecture-specific media inside that lecture's folder, following the existing repo pattern.
- Use relative paths inside notebooks.
- If a code snippet from the PDF is incomplete or OCR is ambiguous, reconstruct the most likely intended code and keep the behavior faithful to the original lecture.
- If `course_summary.md` does not yet exist, note that it is missing and continue with the best available context from prior lectures in the repo.
