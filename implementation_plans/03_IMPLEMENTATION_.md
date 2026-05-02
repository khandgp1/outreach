# Implementation Plan - Written Outreach UI Refinement

This plan covers removing the top banner, updating the header for the "WRITTEN OUTREACH" tab, and replacing its content with a modern, interactive checklist.

## Proposed Changes

### UI & Layout

#### [MODIFY] [index.html](file:///Users/khandpv1/Desktop/.AntiGrav/outreach/index.html)
- Remove the `#top-banner` div (lines 10-12).

#### [MODIFY] [style.css](file:///Users/khandpv1/Desktop/.AntiGrav/outreach/style.css)
- Remove CSS rules for `#top-banner` (lines 18-28).
- Add new styles for the checklist component:
    - `.checklist-container`: Grid/flex layout for items.
    - `.checklist-item`: Card-style item with hover effects.
    - `.checkbox-wrapper`: Custom styled checkbox using the `--accent` color.
    - Typography for checklist headers and descriptions.

### Content & Logic

#### [MODIFY] [program.json](file:///Users/khandpv1/Desktop/.AntiGrav/outreach/program.json)
- Update the first day object:
    - Change `focus` from `"Vibe Coding Workflow"` to `"Email Checklist"`.
    - Change `description` to a placeholder suitable for outreach.
    - Replace `exercises` with placeholder checklist items (e.g., "Research Prospect", "Personalize Hook", "Clear CTA", "Grammar Check").

#### [MODIFY] [script.js](file:///Users/khandpv1/Desktop/.AntiGrav/outreach/script.js)
- Update `renderContent` to call a new `renderChecklist` function when the "WRITTEN OUTREACH" tab is active.
- Implement `renderChecklist(day)` function to generate the HTML for the checklist items.

## Progress Checklist

- [x] Remove top banner from `index.html` and `style.css`
- [x] Update `program.json` with new "Email Checklist" focus and placeholder items
- [x] Implement `renderChecklist` function in `script.js`
- [x] Add modern checklist styling to `style.css`
- [x] Verify checklist interactivity and responsive design
