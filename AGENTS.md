# AGENTS.md

## Purpose
This repository contains Jupyter notebooks for the MOL518 intro programming course. Some future lectures will be adapted from older BPY518 image-analysis slide decks. When an agent is asked to draft one of those lecture notebooks, follow the workflow below.

## Lecture Drafting Workflow
When asked to draft a lecture notebook from an old slide deck:

1. Read `course_summary.md` first.
   - Use it to remind yourself what students have already seen in the course.
   - Keep the new lecture consistent with the level, notation, and assumptions established earlier in the course.

2. Prefer the `.pptx` source over the PDF whenever a PowerPoint file is available.
   - The `.pptx` is the primary source because it preserves the original slide text, embedded media, and object structure.
   - Use the PDF only as a fallback when no `.pptx` exists or when you need to cross-check something visually.
   - If both exist, do not build the notebook from PDF screenshots first and try to fix it later. Start from the `.pptx`.

3. Read the relevant source deck carefully.
   - Preserve the conceptual flow and major teaching points from the slides.
   - The goal is not a literal slide-by-slide dump. Convert the material into a notebook that teaches well in notebook form.

4. Find the correct destination lecture directory and create a new notebook there.
   - Match the naming and organization patterns already used in the repository.
   - Reuse the style established by the existing notebooks, especially the image-analysis notebooks in `Lecture_31` and any related converted lectures.

5. Build the notebook as a teaching document, not just a transcription.
   - Use markdown cells for narrative, explanations, section structure, and image placement.
   - Use code cells for runnable examples, demonstrations, and adapted code from the source material.
   - Keep the order and logic of the original lecture, but rewrite for clarity where needed.
   - Prefer a clean rebuild from the source deck over incremental patching of a flawed earlier draft.

6. Use slide text as notebook markdown.
   - Pull titles, bullets, equations, and short explanatory text from the slide source and rewrite them as markdown.
   - Do not keep slide text as part of an image unless the text is inseparable from the figure.
   - If a slide is mostly text, convert it to markdown rather than inserting the slide itself.

7. Reuse figures from the original slide media, not from whole-slide screenshots.
   - When working from `.pptx`, inspect `ppt/slides/*.xml` and `ppt/media/*` to identify the actual source images for each slide.
   - Prefer extracting and reusing the original embedded media assets directly.
   - If a final notebook figure needs several source assets, compose a new clean figure from those assets.
   - Do not insert full-slide screenshots when only part of the slide is the actual figure.
   - If you must crop from a rendered slide, verify that the crop contains the real figure content and not slide titles, bullets, or cut-off labels.

8. Recover and reuse code snippets carefully.
   - Prefer source text from the `.pptx` when available.
   - If code exists only as an image, use OCR to recover it.
   - Reuse that code either verbatim or in spirit, depending on what best fits the notebook.
   - Clean up OCR errors and make the final code idiomatic, correct, and runnable.
   - When the slide uses a library that is unnecessary or inconsistent with the course style, it is acceptable to implement the same idea with libraries already used in the course.

9. Match the style of Lectures 1-6 and the existing converted notebooks.
   - Prefer clear section headings, short explanatory paragraphs, and runnable code blocks.
   - Keep notebooks student-facing and instructional.
   - Favor consistency over inventing a new format for each lecture.
   - Use images sparingly and intentionally; each included figure should earn its place.

10. Verify the draft notebook.
   - Ensure image links resolve correctly.
   - Ensure code cells are internally consistent and use the correct local file paths.
   - Remove obvious OCR artifacts, broken formatting, and slide-only clutter.
   - Check every included image manually to confirm that it shows the intended figure cleanly.
   - If the extracted figures are messy, rebuild them from the source media rather than accepting a poor crop.

## Content Expectations
- Assume the notebook should be usable as course material, not just as archival notes.
- Keep the concepts and sequencing from the source deck unless there is a clear teaching reason to slightly reorganize them.
- Prefer concise explanations around code so students can understand why each block exists.
- If a slide contains visual material with little text, preserve the teaching point by pairing the image with short explanatory markdown.
- If a slide contains equations or definitions plus a figure, usually convert the equation/definition to markdown and keep only the figure as an image.

## Practical Defaults
- Store lecture-specific media inside that lecture's folder, following the existing repo pattern.
- Use relative paths inside notebooks.
- Keep the media folder minimal. Do not keep failed crops, temporary previews, contact sheets, or exploratory extraction artifacts.
- If a code snippet from the source deck is incomplete or OCR is ambiguous, reconstruct the most likely intended code and keep the behavior faithful to the original lecture.
- If `course_summary.md` does not yet exist, note that it is missing and continue with the best available context from prior lectures in the repo.
