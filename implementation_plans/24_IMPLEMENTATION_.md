# Implementation Plan: Expand Subject Line Card

## Objective
Update the `Subject Line` card to expand to the entire width of its container, ensuring it spans appropriately across the available layout area.

## Context
Currently, the `Subject Line` card might be constrained in width, potentially sharing row space or conforming to a smaller column. The goal is to make it visually prominent by allowing it to take up the full 100% width of its parent container.

## Proposed Changes
1. **Identify the Subject Line Element**: Locate the specific HTML element or data structure generating the `Subject Line` card. This is likely in `program.json` or generated within `script.js`.
2. **Apply Full-Width Styling**: Determine the necessary CSS class or inline style to force the card to `width: 100%` or use appropriate grid/flexbox properties (e.g., `grid-column: 1 / -1;` if inside a CSS Grid, or `flex-basis: 100%;` if in a Flexbox container).
3. **Responsive Testing**: Ensure that the full-width behavior works correctly on both desktop and mobile viewports.

## Checklist
- [ ] Inspect the DOM or `program.json`/`script.js` to find the `Subject Line` section.
- [ ] Determine the parent container's layout (Flexbox vs. Grid).
- [ ] Add a specific CSS class (e.g., `full-width-card`) to the `Subject Line` card element.
- [ ] Update `index.css` to define the `.full-width-card` styles, ensuring it spans the entire row.
- [ ] Verify the `Subject Line` card expands the entire width on desktop view.
- [ ] Verify the layout remains responsive and correct on smaller screens.
