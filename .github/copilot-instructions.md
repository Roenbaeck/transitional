# Copilot instructions

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
