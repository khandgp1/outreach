# Duplicate Outreach Checklist

Duplicate the "Email Checklist" in the "WRITTEN OUTREACH" tab to allow for two separate review cycles: `Review 1` and `Review 2`.

## User Review Required

> [!NOTE]
> The "WRITTEN OUTREACH" tab will now feature two identical checklists stacked vertically, each under its own heading. This structure allows you to track progress across multiple review iterations.

## Proposed Changes

### [Data]

#### [MODIFY] [program.json](file:///Users/khandpv1/Desktop/.AntiGrav/outreach/program.json)

- Restructure the `WRITTEN OUTREACH` day to use a `groups` array instead of a flat `exercises` array.
- Create two groups: `Review 1` and `Review 2`, each containing the original 10 checklist items.

---

### [Logic]

#### [MODIFY] [script.js](file:///Users/khandpv1/Desktop/.AntiGrav/outreach/script.js)

- Update `renderChecklist(day)` to handle both flat `exercises` and the new `groups` structure.
- Ensure checkbox IDs are unique across groups (e.g., `check-${groupIdx}-${itemIdx}`).

---

### [Styling]

#### [MODIFY] [style.css](file:///Users/khandpv1/Desktop/.AntiGrav/outreach/style.css)

- Add styles for `.checklist-group` (margin between groups).
- Add styles for `.checklist-group-title` (muted, uppercase, small-caps style consistent with the theme).

## Verification Plan

### Automated Tests
- Use the browser tool to verify that both "Review 1" and "Review 2" sections appear.
- Verify that checking an item in "Review 1" does not affect "Review 2".

### Manual Verification
- Navigate to the "WRITTEN OUTREACH" tab.
- Confirm the presence of two separate checklists labeled "Review 1" and "Review 2".
- Interact with the checkboxes to ensure they work independently.

## Progress Checklist

- [x] Update `program.json` with grouped checklist data
- [x] Modify `script.js` to render grouped checklists
- [x] Add styling for checklist groups in `style.css`
- [x] Verify independent functionality of both checklists
