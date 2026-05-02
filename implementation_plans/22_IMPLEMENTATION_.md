# Implementation Plan: Remove Green Line from Checklist Cards

## Objective
Remove the green line (`border-top: 4px solid var(--accent);`) at the top of all three checklist card sections ("Outreach 1", "FOLLOW-UP 2", "FOLLOW-UP 3").

## Files to Modify
- `style.css`

## Step-by-Step Instructions

1. **Update `style.css`:**
   - Locate the `.checklist-super-group` class.
   - Remove the `border-top: 4px solid var(--accent);` property.
   - This will remove the green line from the top of "Outreach 1", "FOLLOW-UP 2", and "FOLLOW-UP 3" cards.

## Progress Checklist
- [x] Remove `border-top` from `.checklist-super-group` in `style.css`
- [x] Verify the green line is removed from "Outreach 1" card
- [x] Verify the green line is removed from "FOLLOW-UP 2" card
- [x] Verify the green line is removed from "FOLLOW-UP 3" card
