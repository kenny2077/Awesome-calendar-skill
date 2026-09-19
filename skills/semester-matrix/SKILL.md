---
name: semester-matrix-interactive-html-block
description: Use when generating or revising an interactive HTML in GPT / Claude / Other agent for student schedule that summarizes a semester as a course-by-week matrix and a weekly course view.
---

### Data Source

Build an interactive calendar from normalized user uploaded data such as syllabus pages, grade pages, course schedules and more.

### Visual layers

- Produce two layers **semester view** and **weekly view**. The semester view opens first.
- Simplicity design principle. Example: no text inside matrix cell, only symbols are allowed. Do not add unnecessary elements elsewhere such as unnecessary Description sections.

### Visual Front End

Use a purple light canvas and one white working background.

### Semester matrix

Render one `course × week` matrix:

- rows → courses title. Example: CS 2011, MATH 4242... no course description needed;
- columns → real calendar-week matrix;
- cells → use purple color intensity represents course load. Example: darker purple represents more load/due date this week
- month labels → above the corresponding week columns;
- quiz/exam marks → event-type symbol overlays on the cell. Example: spades, clubs, hearts, and diamonds symbol and more. spades means Quiz, clubs means Exam, spades clubs means both are present, more special types such as Seminar/Presentation/code review may use other symbols. avoid using very small symbol such as ` or * that hurt distinguishability.

### Semester view

- Mouse hover on a cell → show its content near the cell.
- Mouse click on a cell → open weekly view with that course detail.

### Weekly view

Render one calendar view

- X → date/time;
- Y → course lane;
- point → due item with short description and due time, we don't need the item position to represent due time, just brief item text block without position meaning.
- "Previous Week <-  Next Week ->" Button on top right of weekly calendar same level as " <- Semester view"
- Mouse hover on item → show more details near the item

## Inspect Agent

Inspect built project, Score **1–10** on:

- simplicity front end design;
- semester and week readability; Example: Verify that the matrix visualization preserves a clean, uniform and precisely aligned grid structure. All rows and columns must align consistently, with no distortion, skewing, warping, or malformed cells or irregular spacing. Ensure that the data within every cell is clearly legible, properly contained within its boundaries, and given adequate spacing, with no crowding, overlap or collisions between data elements. Conduct a thorough visual QA inspection before finalizing.

**Only 8 or higher score passes.** If the first score is lower than 8, make one batched fix pass, re-render all inspected states, and inspect once more. looping until scored 8 or higher.

## Output

- Live HTML code preview preferred, not images.
- If live view failed, you should tell users to download HTML and open HTML on Chrome or other browsers for interactive view.
