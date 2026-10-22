# FURNITURE DESIGN RULES

Version 1.2

## R1. Material

- Standard board: laminated chipboard (DSP), 18 mm thick (1.8 cm),
  sheet size 3660 x 2100 mm.
- All parts are designed with 18 mm boards unless I say otherwise.
- When calculating inner dimensions, subtract the real thickness
  (18 mm per board).
- "Grain" in these rules means the direction of the laminate
  decor/pattern on the board (chipboard itself has no grain).

## R2. Cutting precision

- This rule applies to BOARD SIZES: every board that is cut must
  be whole millimetres. No decimals.
- It does NOT apply to the spacing between shelves (see R15) or to
  the depth rounding in R16.
- Never round board sizes yourself. If a board size would be a
  fraction (e.g. 392.67 mm), stop and ask me. Show only TWO options:
  the nearest INCREASE and the nearest DECREASE of the total size
  that make every board a whole mm, with the resulting board sizes.
- Find both options with code (a loop over nearby sizes), not by
  reasoning in text.
- Recommend one of the two in one line, usually the one with the
  smaller change.
- Show only a short comparison, for example:
  "1251 mm -> modules 393 mm (+1) | 1248 mm -> modules 392 mm (-2).
  Recommended: 1251."
- After my answer, recalculate all parts from the new total size and
  confirm that every board is a whole mm.
- Always tell me the original size and the adjusted size.
- The board list shows only whole-mm values.

## R3. Drawings

- Draw 2D views (front, side, top) with dimensions.
- A 3D depiction is allowed as a technical plan drawing (line
  drawing, isometric or exploded view with part labels).
- Realistic 3D renderings are NOT allowed unless I explicitly
  request them.

## R4. Visible vs hidden edges

- An edge is VISIBLE if it can be seen from outside OR when doors
  and drawers are open. Overlay doors do NOT make an edge hidden.
- VISIBLE edges get edge banding. HIDDEN edges get none.
- Front edge: the front edge of every board that faces the opening
  is banded, even behind doors: side walls, floor board, top board,
  inner walls, shelves.
- Top edge of side walls: banded if nothing sits on top of them
  (e.g. the side walls of the top body, R9). Hidden if another body
  or board covers it (e.g. the main side walls under a separate
  top body).
- Hidden edges: edges that touch another board, the back board or
  the floor, and all edges of back boards.
- Doors and drawer fronts: all four edges banded.
- The board list shows, per part, which edges get banding.

## R5. Visible parts and grain direction

- Identify parts visible from outside: side walls, doors, drawer
  fronts, top panel, front plinth, etc.
- Visible parts have the best face outward.
- Parts that sit next to each other visibly (e.g. doors in a row,
  side walls) must have the same grain/cut direction.
- The board list shows the grain requirement for each part.

## R6. Final output: print-ready PDF

When planning is finished, produce a PDF ready to print (A4, black
and white, clear fonts) containing:

1. Plan pages: 2D views with dimensions, plus the 3D plan drawing.
2. Board list: one line per board type, in this format:
   X - Y - quantity
   Sizes in whole mm. Identical boards are merged into one line.

Edge banding marks (drawn above the size number):

- One line above a size = one edge of that dimension is banded.
- Two lines above a size = both edges of that dimension are banded.
- No line = no banding on that dimension.

Grain:

- X - Y: Y is the dimension that runs vertically when the board is
  installed.
- Boards that need vertical grain (grain along Y) get an upward
  arrow at the end of their line.
- No arrow = no grain requirement.

# Example (drawn in the PDF):

Example: "764 - 560 - 2 (up arrow)" with ONE line above 764 and TWO
lines above 560. Means: 2 boards, 764 x 560 mm. The 764 side has
one banded edge, the 560 side has both edges banded, vertical grain.
Means: 2 boards, 764 x 560 mm. The 764 side has one banded edge,
the 560 side has both edges banded, vertical grain.

- Boards of a different thickness (back board, thin drawer bottoms)
  are listed in their own group below, with the thickness in the
  group heading.

## R7. Doors and gaps

- Default: doors are OVERLAY. They cover all walls, top and bottom
  of the body. Inset doors are used only if I explicitly request them.
- Gap value is 3 mm or 4 mm. Ask me which one before designing doors.
- Use ONE gap value across the whole piece. Never mix 3 and 4 mm.
- Overlay doors: do NOT calculate a door-to-wall, door-to-top or
  door-to-bottom gap. Only the gap between neighbouring doors counts.
- Inset doors or drawers (sitting inside the walls): the gap applies
  on every side, and between neighbours.
- Door sizes must be whole mm (see R2).
- Doors next to each other have the same height and the same grain
  direction (see R5).
- State the chosen gap in the plan drawings and the board list notes.

Stacked fronts, OVERLAY (doors or drawer fronts one above another,
covering the walls):

- The seam gap is taken from the UPPER front. The lower front keeps
  its full height. The upper front is shorter by the gap.
- Example: top section 550 mm, gap 3 mm -> top door 547 mm. The
  main doors are unchanged.

Stacked fronts, INSET (sitting inside the frame):

- All gaps are equal. The gap to the walls, top and bottom, and the
  seam gap between stacked fronts all use the same gap value.
- Fronts in one stack are equal height:
  (opening height - (N + 1) x gap) / N, where N = number of fronts.
  The upper-front rule does NOT apply to inset fronts.
- Example: opening 600 mm, 3 drawer fronts, gap 3 mm ->
  (600 - 4 x 3) / 3 = 196 mm each.
- Inset fronts side by side use the same logic horizontally:
  (opening width - (N + 1) x gap) / N.
- If an inset front size is a fraction, follow R2 (board sizes).
- Inset doors in separate sections with a board between them: each
  door keeps its own gap to that board, and the fronts are sized
  per opening.

## R8. Drawers (front position)

- If not specified, ask me: drawer fronts OUTSIDE the walls (overlay)
  or INSIDE the walls (inset)?
- Inset drawers use the gap rule from R7.

## R9. Wardrobes

- The top board sits INSIDE the side walls (between them).
- Side walls run the full height of the wardrobe.

## R10. Drawer cabinets

- If not specified, ask me: should the top board fully cover the
  walls, or sit inside them?

## R11. Plinth (furniture base)

- The plinth is a narrow board that sits BETWEEN the main side walls,
  under the floor board. It is not individual feet or blocks.
- Ask me: ONE plinth (front only, visible) or TWO plinths (front
  visible + back hidden)?
- Front plinth setback from the front edge of the floor board.
  Do not ask me, decide automatically:
  - Front edge of the floor board is VISIBLE (not covered by a door
    or drawer front): setback is 3 cm.
  - Front edge of the floor board is COVERED by a door or drawer
    front: setback is 2 cm.
  - Use the same setback for the whole piece. If the piece mixes both
    cases, ask me which one to follow.
- The back plinth (if used) sits at the back, not visible.
- Plinth height is between 7 and 8 cm. Do not ask me, decide
  automatically:
  - Choose the height (whole mm, between 70 and 80 mm) that makes
    every cut board come out as a whole mm (see R2), e.g. door
    heights and drawer heights. Shelf spacing (R15) does not count.
  - If several heights work, use the one closest to 75 mm.
  - If no height between 70 and 80 mm works, ask me whether to
    INCREASE or DECREASE the total height (R2).
  - Use the same height for every plinth on the piece.
  - State the chosen plinth height in the plan notes.
- Plinth length = inner width between the side walls (flush between
  the walls). Whole mm (see R2).
- Banding (see R4): plinths get NO banding. The top edge touches the
  floor board, the bottom edge touches the floor, and the short
  ends touch the side walls, so all edges are hidden.
- Grain (see R5): the front plinth follows the grain direction of
  the other visible parts.

## R12. Drawer boxes (gap and bottom)

- Drawer boxes need a gap from the frame walls (side walls, dividers
  and neighbouring drawers). For every piece with drawers, ask me
  what gap to use. Do not decide it automatically.
- Use ONE drawer-box gap value across the whole piece.
- This gap is separate from the door/front gap in R7. Inset drawer
  fronts still follow R7.
- Drawer box sizes must be whole mm (see R2).
- Drawer bottom: always ask me whether to use a THINNER board or the
  STANDARD 18 mm board. If thinner, ask me for the thickness.
- Show the drawer bottom as a separate line in the board list, with
  its own thickness noted.

## R13. Back side of furniture
- Every body gets a back cover board, listed as a separate board
  and marked "BACK SIDE" in the board list and plan drawings.
  Separate bodies each get their own back board. One body gets one
  back board over its full height (see R17).
- The back board is applied on the rear face of the body.
- Width: outer width of the body - 2 mm.
  Example: outer width 1251 mm -> back width 1249 mm.
- Height:
  - Body WITH a plinth: body height - plinth height. No extra
    -2 mm.
  - Body WITHOUT a plinth: body height - 2 mm.
- Examples:
  - Separate bodies: main 2000 mm with a 70 mm plinth -> 1249 x
    1930 mm. Top body 550 mm, no plinth -> 1249 x 548 mm.
  - One body of 2550 mm with a 70 mm plinth -> 1249 x 2480 mm.
- Sizes are whole mm (see R2).
- The back board is hidden: no banding (see R4).
- Ask me for the back board thickness if I have not specified it.

## R14. Inner walls (dividers between sections)

- Inner walls are vertical boards between the side walls that
  divide the furniture into sections. They are 18 mm thick (R1).
- Decide per piece, no questions needed:
  - If the front of the section is covered by overlay doors (R7):
    the inner wall runs the full depth of the side walls, flush
    with the front. The door hides its front edge.
  - If the front of the section is NOT covered by doors (open
    section, or inset doors/drawers): the inner wall is SHORTER in
    depth by 18 mm. It is set back 18 mm from the front edge.
- Inner wall height: from the floor board to the underside of the
  top board (or the full inner height between them).
- Banding (R4): the front edge of an inner wall in an open section
  is visible and gets banding. A hidden front edge (behind a
  door) gets none.
- Section widths: (inner width - number of inner walls x 18 mm) /
  number of sections. If the result is a fraction, follow R2 and
  ask me INCREASE or DECREASE.
- Grain (R5): inner walls in visible open sections follow the
  decor direction of the other visible parts.
- If a piece mixes covered and open sections, apply the rule
  to each inner wall by the section it faces. If one wall has a
  covered section on one side and an open section on the other,
  ask me which one to follow.
- State in the notes which inner walls were set back by 18 mm.

## R15. Shelves and spaces

- "N shelves" in a module means N SPACES (compartments), not N
  boards. A module with N spaces needs N-1 shelf boards.
- Example: "6 shelves" = 6 spaces = 5 shelf boards.
- All spaces in a module are equal in height:
  (module inner height - (N-1) x 18 mm) / N.
- Spacing decimals are allowed. A difference under 1 mm is not
  visible, so do not ask me about it. Show spacing in drawings with
  one decimal. The shelf boards themselves stay whole mm (R2).
- State in the notes, e.g. "6 spaces, 5 shelf boards".

## R16. Depth with overlay doors

- The depth in my brief is the TOTAL depth, including overlay doors.
- If the front is covered by overlay doors: side wall depth =
  total depth - 18 mm (door thickness), rounded to the nearest
  whole cm (10 mm). Do not ask me. This is an exception to R2.
- Example: total 600 mm -> 600 - 18 = 582 -> side walls 580 mm.
  Actual total depth = 580 + 18 = 598 mm.
- If the result is exactly halfway between two cm values, ask me.
- If there are no overlay doors (open front, or inset doors and
  drawers): side wall depth = total depth.
- Floor board, top board, shelves and inner walls take their depth
  from the side walls (and R14 set-back).
- State both the side wall depth and the actual total depth in the
  notes.

## R17. Stacked sections (one above another)

- If the design has sections stacked vertically (e.g. main and top),
  ask me: are they SEPARATE BODIES or ONE BODY? Do not guess. Skip
  the question if the brief already says.

SEPARATE BODIES (the upper section is its own box sitting on the
lower one):

- Each body has its own 2 side walls, floor board and top board.
- Between the sections there are 2 boards: the top board of the
  lower body and the floor board of the upper body.
- Each body's height is the section height from the brief.
- Each body gets its own back board (R13).
- The plinth is only under the lowest body.
- R9 and R14 apply to each body on its own.

ONE BODY (the sections share the same side walls):

- The side walls run the full height of all sections.
- Between the sections there is ONE divider board (18 mm), like a
  shelf. There is one floor board at the bottom and one top board.
- The divider board counts as part of the lower section's height.
  The upper section starts above it.
- The body gets ONE back board over the full height (R13).
- Inner walls (R14) of each section run between its own floor or
  divider board and its own top or divider board.
- Doors are per section (R7). Stacked overlay doors follow the
  seam gap rule in R7.

- State in the notes which option was used.

## GENERAL BEHAVIOUR

- If a rule is unclear or two rules conflict, ask me before continuing.
- Ask drawer questions (R8, R10, R12) only if the design contains
  drawers. Ask door questions (R7) only if it contains doors.
- Ask all required questions before starting the design, but only
  the ones that apply to this piece.
- Do all calculations with code, not in your head.
- Before the final PDF, recheck R1 to R17. Show one compact list:
  "OK" for rules that pass, and a short note only for rules that
  failed or were applied in a special way (e.g. R14 set-back, R16
  depth rounding).
- Keep answers short.
