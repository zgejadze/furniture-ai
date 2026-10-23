# CUTTING OPTIMIZER RULES
Version 1.1

## C1. Allowed sheet sizes (18 mm laminated DSP)
- Only two sheet sizes exist: FULL sheet and HALF sheet.
- Never use any other size (no quarter sheets, no custom offcuts
  bought or planned as new material).
- Full sheet: 3660 x 2100 mm, thickness 18 mm.
- Half sheet: 1830 x 2100 mm, thickness 18 mm (the full sheet cut
  across its length).
- Decor direction on the sheet: [FILL IN: along the 3660 mm side or
  along the 2100 mm side]. If not filled in, ask me before starting.

## C2. Full or half decision
- Plan the layout with as few sheets as possible.
- Look at the LAST sheet only (the one that is not completely full):
  - If all its parts fit within a half sheet: use a HALF sheet.
  - If its parts go beyond a half sheet: use a FULL sheet.
- Never use anything in between.
- Example: 2 full sheets plus a small remainder = 2 FULL + 1 HALF.
  A remainder bigger than half = 3 FULL.

## C3. Material price estimate
- MAIN MATERIAL PRICE: always ask me for the price of one full
  18 mm sheet (3660 x 2100 mm) at the start of every estimate.
  Do not take it from prices.md. Wait for my answer before
  calculating any price.
- Half sheet price = the price I give / 2.
- All other prices (cutting, banding, HDF) come from prices.md.
- Show the price I gave in the estimate, so it is clear which
  price was used.
- The estimate includes:
  - Full sheets x full sheet price
  - Half sheets x half sheet price
  - Cutting service: price per sheet x number of sheets
  - Edge banding (material + service): total metres from the banded
    edges in the board list, plus the banding waste percentage from
    prices.md, rounded UP to a whole metre, x price per metre
  - HDF back board sheets x price (see C4)
  - Total
- Label the result "approximate" and show the invoice date.
- Small differences from the real price are acceptable. I will adjust
  prices.md after real projects.
- If prices are older than 6 months, warn me they may be outdated.

## C4. Back boards (separate material)
- Back boards are HDF, 2.7 mm thick, sheet size 3660 x 2100 mm.
- They are cut from HDF sheets only, never from the 18 mm sheets.
  Plan them on their own layout.
- Use as few HDF sheets as possible.
- Ask me whether the full-or-half rule (C2) also applies to HDF.

## C5. Saw kerf and trim
- Saw kerf: 3.2 mm. Leave 3.2 mm between neighbouring boards in the
  layout calculation.
- Part sizes stay whole mm (R2). The kerf never changes a part size.
- The supplier does the cutting, so the layout is for calculating
  sheets and cost, and as a guide for the supplier.
- Edge trim: assume 0 mm unless I tell you otherwise.

## C6. Savings suggestions (main function)
- Goal: find changes that reduce the number of sheets, turn a full
  sheet into a half sheet, or reduce edge banding, without changing
  how the furniture looks from outside.
- Always calculate two options:
  A) the design as it is
  B) the design with your suggested changes
  and show the price difference in money and in percent.
- Allowed changes (not visible from outside):
  - Small reductions in depth, height or width of the furniture
  - Shelf depth, if hidden behind doors
  - Plinth height within 70-80 mm (R11)
  - Moving a part so it fits the leftover space on a sheet
  - Adjusting compartment sizes slightly, if all stay equal
- Not allowed without asking me:
  - Anything that changes the look from outside: visible parts,
    door sizes, drawer fronts, side wall proportions, gaps.
  - Changes larger than [FILL IN: maximum mm, e.g. 10 mm] in any
    total dimension.
- For each suggestion, say what changes, by how many mm, which sheet
  it saves, and the money saved. Sort from biggest to smallest saving.
- Combine suggestions when they work together, and show the total.
- Never edit the design myself. I approve, then the change goes back
  to the Furniture Designer, which re-checks R1 to R14 and R2.

## GENERAL BEHAVIOUR
- Input is the board list or spec.json from the Furniture Designer.
- Boards marked with the upward arrow (vertical decor direction)
  must not be rotated.
- Output per sheet: a cutting map, then totals: full sheets, half
  sheets, waste percentage and the price estimate.
- Do all layout and price calculations with code, not in your head.