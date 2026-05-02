# Implementation Plan - Add Follow-Up 3 Section

Add a new checklist section called "FOLLOW-UP 3" to the right of "FOLLOW-UP 1" in the Written Outreach tab. This will follow the design pattern of the "OUTREACH 1" section by grouping both follow-up checklists under a single "FOLLOW-UP" header.

## Proposed Changes

### Data Layer

#### [MODIFY] [program.json](file:///Users/khandpv1/Desktop/.AntiGrav/outreach/program.json)
- Rename the superGroup `"Follow-Up 1"` to `"FOLLOW-UP"`.
- Rename the group within it from `"Follow-Up Checklist"` to `"FOLLOW-UP 1"`.
- Add a second group named `"FOLLOW-UP 3"` to the `"groups"` array of the same superGroup.
- Populate `"FOLLOW-UP 3"` with the following items:
    - Short
    - One Lane
    - Clear Boundary
    - Minutes
    - Micro Yes

---

## Progress Checklist

- [x] Rename existing "Follow-Up 1" superGroup to "FOLLOW-UP" in `program.json`
- [x] Rename "Follow-Up Checklist" group to "FOLLOW-UP 1"
- [x] Add "FOLLOW-UP 3" group with requested checklist items
- [x] Verify both checklists appear side-by-side in the UI
- [x] Verify checkbox persistence for the new section

## Verification Plan

### Manual Verification
- Open the **WRITTEN OUTREACH** tab.
- Verify the header now says **FOLLOW-UP**.
- Verify there are two columns side-by-side: **FOLLOW-UP 1** and **FOLLOW-UP 3**.
- Verify the items in **FOLLOW-UP 3** match the request.
- Click a checkbox in **FOLLOW-UP 3** and refresh the page to ensure state is maintained (if state persistence is implemented, otherwise just check functionality).
- Check responsiveness on smaller screens (should stack vertically).
