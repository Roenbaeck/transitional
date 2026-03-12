# Copilot instructions

## Target files
- We are currently working on a new version of the paper, contained in representation.tex. There is an old sketch of a paper in transitional.tex, a bunch of blog posts in MOTIVATION.md, journal guidelines in GUIDELINES.md, and information about the Traqula query language in TRAQULA.md, traqula.pest, and traqula.rs.

There is also a living document of feedback from reviewers in FEEDBACK.md, in which the whole content is replaced when new feedback is added, so it is not a good candidate for copilot instructions. 

## Context
- This repository is a LaTeX project (Tufte classes).
- LaTeX is **not installed locally** in this workspace environment.
- PDF builds are done via an **online LaTeX service** (not via local `latexmk`, `pdflatex`, etc.).

## What to do
- When editing `.tex`/`.bib` files, focus on correctness by inspection (syntax, matching braces/environments, consistent macros, etc.).
- Prefer minimal, surgical edits; preserve existing style and macros.

## What not to do
- Do not assume local compilation is possible.
- Do not add build scripts/tasks that require a local TeX distribution unless explicitly requested.
