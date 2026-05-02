# Implementation Plan - Dev Config & Password Toggle

This plan outlines the creation of a centralized configuration file to manage development features, with the first feature being a toggle for the password protection popup.

## User Review Required

> [!NOTE]
> I am proposing a `config.js` file instead of `config.json` to allow for synchronous loading and avoid any content flash while waiting for a fetch request.

## Proposed Changes

### Core Configuration

#### [NEW] [config.js](file:///Users/khandpv1/Desktop/.AntiGrav/outreach/config.js)
- Define a global `APP_CONFIG` object.
- Add `features` object with `passwordProtection: true`.

### Integration

#### [MODIFY] [index.html](file:///Users/khandpv1/Desktop/.AntiGrav/outreach/index.html)
- Include `<script src="config.js"></script>` before `script.js`.

#### [MODIFY] [script.js](file:///Users/khandpv1/Desktop/.AntiGrav/outreach/script.js)
- Reference `APP_CONFIG.features.passwordProtection` in the initialization logic.
- If `passwordProtection` is `false`, hide the `password-overlay` immediately.

## Verification Plan

### Automated Tests
- I will use the browser tool to verify:
    1. With `passwordProtection: true`, the password popup is visible on load.
    2. With `passwordProtection: false`, the password popup is hidden on load.

### Manual Verification
- Manually edit `config.js` and refresh the page to ensure the toggle works as expected.

---

## Progress Checklist
- [x] Create `config.js`
- [x] Update `index.html` to include `config.js`
- [x] Update `script.js` to use the toggle
- [x] Verify functionality with browser tests
