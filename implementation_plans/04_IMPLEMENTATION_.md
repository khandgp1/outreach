# Simplistic Checklist Redesign Plan

## Objective
Implement a leaner, minimalist design for the checklist on the "WRITTEN OUTREACH" tab. This involves flattening the UI, removing card-like structures, and using subtle visual cues for a cleaner look.

## Proposed Changes

### CSS Updates (`style.css`)
- **`.checklist-item`**:
  - Remove `background`, `border`, `border-radius`, and `box-shadow`.
  - Add `border-bottom: 1px solid var(--border)` for subtle separation.
  - Reduce padding (e.g., from `padding: 20px` to `padding: 16px 8px`).
- **`.checklist-item:last-child`**:
  - Remove `border-bottom`.
- **`.checklist-item:hover`**:
  - Remove `transform: translateY(-2px)` and `box-shadow`.
  - Add a subtle background highlight (e.g., `background: #FAFAFA; border-radius: 4px;` just for the hover area).
- **`.checklist-text h4`**:
  - Decrease font size slightly (e.g., `1rem`) and adjust font-weight for a less dominant heading.
- **`.checkmark`**:
  - Update `border-radius: 50%` to make checkboxes circular.
  - Alternatively, make them slightly smaller with sharp corners if circular doesn't fit the vibe perfectly.
  - Adjust the inner checkmark icon (`.checkbox-container .checkmark:after`) to fit the new shape correctly.
- **Checked State (`.checklist-item:has(input:checked)`)**:
  - Ensure the crossed-out text and faded opacity still look good on the new flat layout.

## Progress Checklist
- [x] Update `.checklist-item` base styles (remove box, add bottom border, adjust padding).
- [x] Add rule for `.checklist-item:last-child` to hide the final border.
- [x] Update `.checklist-item:hover` for minimal interactive state.
- [x] Adjust `.checklist-text h4` typography.
- [x] Update `.checkmark` to be circular (`border-radius: 50%`).
- [x] Test the checklist interactively (hover and checked states) to ensure the flat aesthetic is cohesive.
