# furniture-ai

Rules and instructions for planning furniture with Claude.

- designer/ - design rules (R1-R14) and project instructions for
  the Furniture Designer. Output: print-ready PDF plans with the
  board list, and spec.json.
- optimizer/ - cutting rules (C1-C6), prices and instructions for
  the Cutting Optimizer. Output: sheet count, savings suggestions
  and an approximate material price.
- designs/ - finished designs, one folder per piece.
- CHANGELOG.md - history of rule changes.
- mistakes_log.md - corrections to add to the rules later.

Material: laminated chipboard (DSP) 18 mm, sheet 3660 x 2100 mm.

## Updating the Claude projects
1. Edit the file here and commit it.
2. Delete the old file in the Claude project, then add the new text.
3. In a new chat, ask "What version is rules.md?" to check.

GitHub is the master. The Claude projects only hold copies.