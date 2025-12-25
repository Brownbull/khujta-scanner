# Khujta Scanner - Testing Guide

A QA testing framework using Claude Code with the Chrome Extension to test web applications from the user's perspective.

---

## Quick Start

### Option 1: Discover Mode (Default - Recommended)

Just provide the URL and credentials. Claude will figure out the rest.

```
Discover the app at https://myapp.com
Credentials: user@test.com / password123
```

Claude will:
1. Explore the application autonomously
2. Figure out what the app is about
3. Identify core features and user journeys
4. Generate a discovery report with findings

### Option 2: Quick/Comprehensive Test (When You Know the App)

If you have a discovery report or know the app well:

```
Run a quick test on [app-name] using the discovery report at reports/[app-name]-discovery.md
```

Or with full configuration:

```
Run a comprehensive test using config/[app-name]-config.md
```

---

## Mobile Testing Setup (Required for Mobile-First Apps)

**IMPORTANT**: The Chrome extension cannot programmatically enable mobile device emulation. For apps designed for mobile use, you must manually enable this before starting.

### Steps to Enable Mobile Emulation

1. **Open DevTools**: Press `F12` (or `Ctrl+Shift+I`)
2. **Enable Device Toolbar**: Press `Ctrl+Shift+M` (or click the device icon in DevTools toolbar)
3. **Select Device**: Choose from dropdown:
   - **iPhone 12 Pro** (390x844) - Recommended
   - **iPhone SE** (375x667) - Smaller screen testing
   - **Pixel 5** (393x851) - Android testing
4. **Refresh Page**: Press `F5` to apply viewport changes
5. **Verify**:
   - Viewport dimensions shown in DevTools
   - Cursor appears as circle (touch emulation)
   - Page renders in mobile layout

### When to Use Mobile Emulation

| App Type | Mobile Emulation |
|----------|-----------------|
| Mobile-first / Mobile-only | **Required** |
| Responsive web app | Recommended |
| Desktop-only app | Skip |
| Unknown | Start with mobile, Claude will note if desktop is better |

### Quick Verification

After enabling, Claude will verify the viewport with:
```
Viewport: 390x844 ✓ (Mobile emulation active)
```

If you see dimensions like `500x600`, mobile emulation is not properly enabled.

---

## Test Modes

| Mode | Input Required | Duration | Best For |
|------|---------------|----------|----------|
| **Discover** (default) | URL + credentials only | ~20-30 min | New apps, first-time testing, autonomous exploration |
| **Quick** | Discovery report or config | ~15-20 min | Smoke tests, post-deploy validation |
| **Comprehensive** | Discovery report or config | ~1-2 hours | Pre-release, thorough QA |

---

## Discover Mode (Default)

**Input**: Just URL + login credentials
**Output**: Discovery report with app understanding + initial issues

### What Claude Does

1. **Explores** the application systematically
2. **Infers** purpose, target users, value proposition
3. **Maps** navigation and features
4. **Identifies** core user journeys
5. **Documents** the information architecture
6. **Logs** any issues found
7. **Generates** a discovery report

### Discovery Report Contains

- **Application Profile**: What it is, who it's for, what problem it solves
- **Reasoning**: How conclusions were reached (evidence-based)
- **Navigation Map**: Full structure of the app
- **User Journeys**: Primary and secondary workflows
- **Feature Inventory**: What's available and its status
- **Technical State**: Console errors, network issues
- **Issues Found**: Problems encountered during exploration
- **Recommendations**: What to test next in Quick/Comprehensive modes

### Using Discovery Reports

Discovery reports are designed to be reusable:
- **For further testing**: Load as context for Quick/Comprehensive tests
- **For development**: Share with dev team as app documentation
- **For other Claude sessions**: Use as context for bug fixes, feature work

---

## Quick Mode

**Input**: Discovery report or full config
**Duration**: ~15-20 minutes

Best for:
- Smoke testing after deploys
- Quick sanity checks
- Time-constrained testing

Covers:
- Initial load and login
- Primary navigation
- One core user journey
- Basic responsiveness
- Console/network error check

---

## Comprehensive Mode

**Input**: Discovery report or full config
**Duration**: ~1-2 hours

Best for:
- Pre-release validation
- Major feature testing
- Thorough quality assurance

Covers:
- Everything in Quick mode, plus:
- All user personas
- Multiple user journeys
- Form validation
- Full responsiveness suite
- Edge cases
- Accessibility audit
- Error handling scenarios

---

## Directory Structure

```
khujta-scanner/
├── config/
│   ├── test-config.template.md      # Full config template
│   └── discover-config.template.md  # Minimal config for discover mode
├── test-plans/
│   ├── discover-mode.md             # Autonomous exploration plan
│   ├── quick-test.md                # Major flows checklist
│   └── comprehensive-test.md        # Full test plan
├── personas/
│   ├── mobile-user.md               # Mobile-first testing
│   ├── common-user.md               # Standard user testing
│   ├── admin-user.md                # Admin feature testing
│   └── returning-user.md            # Data persistence testing
├── reports/
│   ├── REPORT-TEMPLATE.md           # Test report structure
│   ├── DISCOVERY-REPORT-TEMPLATE.md # Discovery report structure
│   └── screenshots/                 # Screenshot storage
├── CLAUDE.md                        # Claude Code instructions
└── TESTING-GUIDE.md                 # This file
```

---

## User Personas

| Persona | Viewport | Focus |
|---------|----------|-------|
| **Mobile User** | 375x667 | Touch, small screen, mobile UX |
| **Common User** | 1280x800 | Standard workflows, core features |
| **Admin User** | 1920x1080 | Admin features, permissions |
| **Returning User** | Variable | Data persistence, session state |

---

## Example Commands

### Discover Mode (Default)
```
Discover the app at https://myapp.com
Login: user@test.com / password123
```

### Discover with Multiple Users
```
Discover the app at https://myapp.com
Users:
- Common: user@test.com / pass123
- Admin: admin@test.com / admin123
```

### Quick Test (After Discovery)
```
Run a quick test on myapp using the discovery report at reports/myapp-discovery.md
```

### Comprehensive Test
```
Run a comprehensive test on myapp.
Use the discovery report for context.
Focus on the checkout workflow.
```

### Re-test Specific Issue
```
Re-test issue DIS-003 from the discovery report.
The navigation should now work correctly.
```

---

## Workflow: New Application

1. **Start with Discover**
   ```
   Discover https://new-app.com
   Credentials: test@example.com / test123
   ```

2. **Review Discovery Report**
   - Understand what Claude found
   - Check identified issues
   - Note recommended test areas

3. **Run Quick Test** (if needed)
   ```
   Run a quick test using reports/new-app-discovery.md
   ```

4. **Run Comprehensive Test** (pre-release)
   ```
   Run a comprehensive test using reports/new-app-discovery.md
   Focus on: [specific areas of concern]
   ```

---

## Reading Reports

### Discovery Report Structure

1. **Application Profile** - What the app is, who it's for
2. **Reasoning** - Evidence for conclusions
3. **Information Architecture** - Navigation and features
4. **User Journeys** - Identified workflows
5. **Technical State** - Errors, performance
6. **Issues Found** - Problems discovered
7. **Recommendations** - Next steps

### Test Report Structure

1. **Executive Summary** - Pass/fail, issue counts
2. **Workflows Tested** - What was covered
3. **Issues Table** - All issues with severity
4. **Issue Details** - Steps to reproduce
5. **Console/Network Logs** - Technical errors
6. **Screenshots** - Visual evidence

### Issue Severities

| Severity | Meaning | Action |
|----------|---------|--------|
| **Blocker** | Core functionality broken | Must fix before release |
| **Major** | Significant user impact | Should fix soon |
| **Minor** | Inconvenient, workaround exists | Fix when possible |
| **Cosmetic** | Polish issues | Nice to fix |

---

## Report File Naming

```
Discovery:    reports/[app-name]-[YYYY-MM-DD]-discovery.md
Quick Test:   reports/[app-name]-[YYYY-MM-DD]-quick.md
Comprehensive: reports/[app-name]-[YYYY-MM-DD]-comprehensive.md
Screenshots:  reports/screenshots/[app-name]-[description].png
```

---

## Tips for Best Results

### For Discover Mode
- Provide working credentials
- Ensure the app is accessible
- Let Claude explore without interruption
- Review the discovery report before further testing

### For Quick/Comprehensive Modes
- Use the discovery report as context
- Mention specific areas of concern
- Specify which personas to prioritize

---

## Integrating Reports

Reports are Markdown files designed to be consumed by:
- **Other Claude Code agents** - For bug fixes, feature development
- **Issue tracking systems** - Import issues with severity
- **Development team** - Review findings, prioritize fixes
- **Release documentation** - QA sign-off records

---

## Limitations

- **No registration testing** - Tests logged-in users only
- **No Google OAuth** - Uses test credentials only
- **No password entry** - You must provide credentials
- **No payment testing** - Cannot enter financial data
- **Browser automation only** - Chrome via Claude extension

---

## Troubleshooting

### Chrome Extension Not Responding
- Check that Claude Chrome Extension is installed and enabled
- Refresh the browser tab
- Restart Chrome if necessary

### Login Failing
- Verify credentials are correct
- Check if account is locked or expired
- Ensure test environment is accessible

### Screenshots Not Saving
- Verify `/reports/screenshots/` directory exists
- Check disk space
- Report may note if screenshot failed

### Discovery Taking Too Long
- Complex apps may need more time
- Check if app is responding slowly
- Consider network conditions
