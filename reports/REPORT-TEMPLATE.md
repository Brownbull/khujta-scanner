# Test Report: [Application Name]

**Test Date**: [YYYY-MM-DD]
**Tester**: Claude Code + Chrome Extension
**Test Mode**: [Quick / Comprehensive]
**Duration**: [Time taken]

---

## Executive Summary

### Overall Status: [PASS / PASS WITH ISSUES / FAIL]

| Metric | Count |
|--------|-------|
| Workflows Tested | X |
| Issues Found | X |
| Blockers | X |
| Major Issues | X |
| Minor Issues | X |
| Cosmetic Issues | X |

### Key Findings
- [Most critical finding 1]
- [Most critical finding 2]
- [Most critical finding 3]

### Recommendation
[Overall recommendation: ready for release, needs fixes, requires major rework]

---

## Application Under Test

**Name**: [Application Name]
**URL**: [URL]
**Purpose**: [Brief description]
**Test Environment**: Chrome via Claude Chrome Extension

### Test Users
| Persona | Username | Status |
|---------|----------|--------|
| Mobile User | [email] | Tested / Not Tested |
| Common User | [email] | Tested / Not Tested |
| Admin User | [email] | Tested / Not Tested |
| Returning User | [email] | Tested / Not Tested |

---

## Workflows Tested

### Completed Workflows

| # | Workflow | Persona | Status | Notes |
|---|----------|---------|--------|-------|
| 1 | [Workflow name] | [Persona] | PASS/FAIL | [Brief note] |
| 2 | [Workflow name] | [Persona] | PASS/FAIL | [Brief note] |
| 3 | [Workflow name] | [Persona] | PASS/FAIL | [Brief note] |

### Workflow Details

#### Workflow 1: [Name]
**Persona**: [Persona used]
**Objective**: [What user was trying to accomplish]

**Steps Taken**:
1. [Step 1]
2. [Step 2]
3. [Step 3]

**Result**: [PASS/FAIL]
**Notes**: [Any observations]
**Screenshot**: [Link to screenshot if applicable]

---

## Issues Found

### Issues Summary Table

| ID | Severity | Category | Summary | Screenshot |
|----|----------|----------|---------|------------|
| ISS-001 | Blocker | [Category] | [Brief description] | [Link] |
| ISS-002 | Major | [Category] | [Brief description] | [Link] |
| ISS-003 | Minor | [Category] | [Brief description] | [Link] |

### Issue Details

---

#### ISS-001: [Issue Title]

**Severity**: Blocker / Major / Minor / Cosmetic
**Category**: [UI / Functionality / Navigation / Form / Accessibility / Performance]
**Persona**: [Which user encountered this]
**Page/Feature**: [Where it occurred]

**Description**:
[Detailed description of the issue]

**Steps to Reproduce**:
1. [Step 1]
2. [Step 2]
3. [Step 3]

**Expected Behavior**:
[What should happen]

**Actual Behavior**:
[What actually happened]

**Screenshot**:
![ISS-001](./screenshots/iss-001.png)

**Impact**:
[How this affects users]

---

#### ISS-002: [Issue Title]

**Severity**: Blocker / Major / Minor / Cosmetic
**Category**: [UI / Functionality / Navigation / Form / Accessibility / Performance]
**Persona**: [Which user encountered this]
**Page/Feature**: [Where it occurred]

**Description**:
[Detailed description]

**Steps to Reproduce**:
1. [Step 1]
2. [Step 2]

**Expected Behavior**:
[What should happen]

**Actual Behavior**:
[What actually happened]

**Screenshot**:
![ISS-002](./screenshots/iss-002.png)

**Impact**:
[How this affects users]

---

## Responsiveness Testing

| Viewport | Dimensions | Status | Notes |
|----------|------------|--------|-------|
| Mobile | 375x667 | PASS/FAIL | [Notes] |
| Tablet Portrait | 768x1024 | PASS/FAIL | [Notes] |
| Tablet Landscape | 1024x768 | PASS/FAIL | [Notes] |
| Desktop | 1280x800 | PASS/FAIL | [Notes] |
| Large Desktop | 1920x1080 | PASS/FAIL | [Notes] |

### Responsiveness Issues
[List any responsive design issues found]

---

## Console Errors Log

### Errors

| Timestamp | Type | Message | Page |
|-----------|------|---------|------|
| [Time] | Error | [Message] | [URL] |
| [Time] | Error | [Message] | [URL] |

### Warnings

| Timestamp | Type | Message | Page |
|-----------|------|---------|------|
| [Time] | Warning | [Message] | [URL] |

### Full Console Output
```
[Paste full console log here if relevant]
```

---

## Network Errors Log

### Failed Requests

| Timestamp | Method | URL | Status | Error |
|-----------|--------|-----|--------|-------|
| [Time] | GET/POST | [URL] | [4xx/5xx] | [Error message] |

### Slow Requests (>3s)

| URL | Method | Duration | Notes |
|-----|--------|----------|-------|
| [URL] | [Method] | [Time] | [Notes] |

---

## Accessibility Findings

### Keyboard Navigation
- [ ] All interactive elements reachable via Tab
- [ ] Focus indicators visible
- [ ] Logical tab order
- [ ] No keyboard traps

**Issues Found**:
[List any keyboard navigation issues]

### Screen Reader Support
- [ ] Images have alt text
- [ ] Form fields have labels
- [ ] ARIA landmarks present
- [ ] Dynamic content announced

**Issues Found**:
[List any screen reader issues]

---

## Screenshots Index

| Filename | Description | Issue Reference |
|----------|-------------|-----------------|
| initial-load.png | Application initial state | - |
| iss-001.png | [Issue description] | ISS-001 |
| iss-002.png | [Issue description] | ISS-002 |
| mobile-view.png | Mobile viewport | - |

---

## Test Environment

- **Browser**: Chrome (via Claude Chrome Extension)
- **Date/Time**: [YYYY-MM-DD HH:MM]
- **Test Plan Used**: [Quick / Comprehensive]
- **Personas Tested**: [List personas]

---

## Appendix

### Derived Edge Cases Tested
[List any edge cases that were derived from the application purpose]

### Out of Scope
[List anything explicitly not tested]

### Notes for Future Testing
[Any observations for subsequent test runs]
