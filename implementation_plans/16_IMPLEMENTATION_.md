# Implementation Plan - Split Follow-Up Sections (Updated)

Split "FOLLOW-UP 1" and "FOLLOW-UP 3" into separate sections while keeping them adjacent (side-by-side) in the UI.

## Proposed Changes

### Data Layer

#### [MODIFY] [program.json](file:///Users/khandpv1/Desktop/.AntiGrav/outreach/program.json)
- Re-structure the follow-up checklists into two separate SuperGroups: `"FOLLOW-UP 1"` and `"FOLLOW-UP 3"`.
- Each will have its own `"groups"` array containing a single group.

### UI / Layout

#### [MODIFY] [script.js](file:///Users/khandpv1/Desktop/.AntiGrav/outreach/script.js)
- Update `renderChecklist` to wrap supergroups in a flex container if they should be adjacent.
- Or, more simply, update CSS to handle this.

#### [MODIFY] [style.css](file:///Users/khandpv1/Desktop/.AntiGrav/outreach/style.css)
- Add styling to allow `.checklist-super-group` elements to sit side-by-side when desired.
- Specifically, we can wrap the follow-up sections in a container or use a grid for the main checklist content area.

> [!NOTE]
> To ensure they are "adjacent", we will use a flex container for the SuperGroups themselves, allowing them to flow horizontally on larger screens.

---

## Progress Checklist

- [x] Re-structure `program.json` with separate "FOLLOW-UP 1" and "FOLLOW-UP 3" SuperGroups
- [x] Modify `style.css` to allow horizontal layout for SuperGroups
- [x] Update `renderChecklist` in `script.js` to support the new layout (e.g., wrap supergroups in a container)
- [x] Verify both sections are distinct but side-by-side on desktop
- [x] Verify they stack correctly on mobile

## Verification Plan

### Manual Verification
- Open the **WRITTEN OUTREACH** tab.
- Verify **Outreach 1** is full-width (if desired) or follows the new layout.
- Verify **FOLLOW-UP 1** and **FOLLOW-UP 3** appear as two distinct boxes next to each other.
- Verify that each has its own header.
