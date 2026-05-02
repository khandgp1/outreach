# Implementation Plan - Add Follow-Up 1 Section

Add a new section called "FOLLOW-UP 1" below the "OUTREACH 1" section in the Written Outreach tab. This section will contain a single checklist with specific items.

## User Review Required

> [!IMPORTANT]
> The data structure in `program.json` will be updated from a single level of `groups` to a nested `superGroups` structure to allow for multiple sections (Outreach 1, Follow-Up 1, etc.).

## Proposed Changes

### Data & Logic

#### [MODIFY] [program.json](file:///Users/khandpv1/Desktop/.AntiGrav/outreach/program.json)
- Restructure `days[0]` (WRITTEN OUTREACH) to use a `superGroups` array.
- Move the existing "Review 1", "Review 2", and "10 Sec Test" groups into a "superGroup" named "Outreach 1".
- Add a new "superGroup" named "Follow-Up 1" containing the "Follow-Up Checklist" with the requested items:
    - Shorter
    - Same Issue
    - No Call
    - No Internal Data
    - Not Annoyed Tone
    - Same Micro Yes
    - Forward Internally

#### [MODIFY] [script.js](file:///Users/khandpv1/Desktop/.AntiGrav/outreach/script.js)
- Update `renderChecklist` to iterate over `day.superGroups`.
- Each `superGroup` will render its own `.checklist-super-group` container, maintaining the current aesthetic.
- Update checkbox IDs to include the super-group index to avoid collisions (`check-${sgIdx}-${gIdx}-${idx}`).

### Styling

#### [MODIFY] [style.css](file:///Users/khandpv1/Desktop/.AntiGrav/outreach/style.css)
- Add `margin-bottom: 40px` to `.checklist-super-group` to provide consistent spacing between sections.
- Ensure the layout handles a single checklist within a super-group gracefully (the grid should just show one column).

---

## Progress Checklist

- [x] Update `program.json` structure and add "Follow-Up 1" data
- [x] Update `script.js` to render nested `superGroups`
- [x] Adjust `style.css` for section spacing
- [x] Verify UI layout and functionality

## Verification Plan

### Manual Verification
- Navigate to the **WRITTEN OUTREACH** tab.
- Verify "OUTREACH 1" still contains its three checklists in a row.
- Verify "FOLLOW-UP 1" appears below it with its checklist.
- Verify checkboxes in both sections work correctly and persist state.
- Check mobile responsiveness.
