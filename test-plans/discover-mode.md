# Discover Mode Test Plan

**Duration**: ~20-30 minutes
**Input Required**: URL + credentials only
**Purpose**: Autonomous exploration to understand and document the application
**Output**: Discovery report with application understanding + initial issue findings

---

## Overview

Discover mode is the default testing mode. Given only a URL and login credentials, Claude will:

1. Explore the application systematically
2. Infer the application's purpose and target users
3. Identify core features and user journeys
4. Document the information architecture
5. Note any issues discovered during exploration
6. Generate a discovery report for future testing/development

---

## Phase 0: Environment Setup (2-3 min)

### 0.1 Browser Preparation
- [ ] Open Chrome browser
- [ ] Ensure Claude Chrome Extension is active and connected

### 0.2 Mobile Emulation Setup (if mobile testing required)

**IMPORTANT**: The Chrome extension cannot programmatically enable DevTools mobile emulation. This requires manual setup.

**User Action Required**:
1. [ ] Press `F12` to open Chrome DevTools
2. [ ] Press `Ctrl+Shift+M` (or click the device toolbar icon in DevTools)
3. [ ] Select a mobile device from the dropdown:
   - **Recommended**: iPhone 12 Pro (390x844) or iPhone SE (375x667)
   - Alternative: Any device matching target audience
4. [ ] Ensure "Responsive" mode shows correct dimensions
5. [ ] Refresh the page to apply mobile viewport

**Verification**:
- [ ] Viewport shows mobile dimensions (e.g., 390x844)
- [ ] Touch emulation is enabled (cursor shows as circle)
- [ ] User agent is mobile (can verify in DevTools Network tab)

**Skip mobile setup if**:
- App is desktop-only
- Config specifies desktop testing
- Quick desktop validation is sufficient

### 0.3 Console & Network Monitoring
- [ ] In DevTools, ensure Console tab is visible
- [ ] Enable "Preserve log" in Console settings (optional but helpful)
- [ ] Switch to Network tab briefly to confirm it's recording

---

## Phase 1: Initial Reconnaissance (5 min)

### 1.1 First Impressions
- [ ] Navigate to URL
- [ ] **Observe**: What loads first? (Landing page, login, dashboard?)
- [ ] **Observe**: Visual design language and branding
- [ ] **Observe**: Any taglines, headlines, or value propositions
- [ ] **Screenshot**: Initial state
- [ ] **Note**: First impression of what this app might be

### 1.2 Pre-Login Exploration
- [ ] Check if there's public content before login
- [ ] Look for "About", "Features", "How it works" pages
- [ ] Note any visible feature descriptions
- [ ] **Document**: Clues about application purpose

### 1.3 Login
- [ ] Locate login mechanism
- [ ] Enter provided credentials
- [ ] **Observe**: Post-login landing page
- [ ] **Screenshot**: Dashboard/home state
- [ ] **Note**: What does the app prioritize showing first?

---

## Phase 2: Navigation Mapping (5-7 min)

### 2.1 Primary Navigation Discovery
- [ ] Identify all navigation elements (header, sidebar, footer)
- [ ] List every navigation item visible
- [ ] Click through each primary nav item
- [ ] **Document**: Navigation structure as a tree

```
Navigation Map:
├── [Nav Item 1]
│   ├── [Sub-item]
│   └── [Sub-item]
├── [Nav Item 2]
└── [Nav Item 3]
```

### 2.2 Feature Inventory
For each navigation destination:
- [ ] **Name**: What is this section called?
- [ ] **Purpose**: What can users do here?
- [ ] **State**: Empty, has data, requires setup?
- [ ] **Screenshot**: Each major section

### 2.3 Secondary Navigation
- [ ] User profile/settings menu
- [ ] Contextual menus within sections
- [ ] Breadcrumbs or back navigation
- [ ] Search functionality

---

## Phase 3: Purpose Inference (5-7 min)

### 3.1 Analyze Collected Evidence

Based on exploration, answer:

**What type of application is this?**
- [ ] Productivity / Task management
- [ ] E-commerce / Marketplace
- [ ] Social / Community
- [ ] Content / Media
- [ ] Analytics / Dashboard
- [ ] Communication / Messaging
- [ ] Education / Learning
- [ ] Finance / Accounting
- [ ] Healthcare / Wellness
- [ ] Other: [Specify]

**Who are the target users?**
- [ ] Individual consumers
- [ ] Business professionals
- [ ] Teams / Organizations
- [ ] Specific industry: [Which?]
- [ ] Technical users / Developers
- [ ] Non-technical users

**What problem does it solve?**
[Infer the core problem this application addresses]

**What is the primary value proposition?**
[What benefit does a user get from using this?]

### 3.2 Core Workflow Hypothesis

Based on the UI, what are users likely trying to accomplish?

1. **Primary Journey**: [Most important thing users do]
   - Starting point:
   - Goal:
   - Likely steps:

2. **Secondary Journey**: [Second most important workflow]
   - Starting point:
   - Goal:
   - Likely steps:

3. **Tertiary Journey**: [Additional workflows]
   - [List other identified workflows]

---

## Phase 4: Feature Deep Dive (5-7 min)

### 4.1 Core Feature Testing

For the primary identified workflow:
- [ ] Attempt to complete the workflow
- [ ] **Document**: Actual steps required
- [ ] **Document**: UI elements involved
- [ ] **Check**: Does it work as expected?
- [ ] **Screenshot**: Key states

### 4.2 Data Model Discovery
- [ ] What entities/objects exist? (Users, Projects, Items, etc.)
- [ ] What are the relationships between them?
- [ ] What data can users create/manage?

### 4.3 Feature Completeness Assessment
For each major feature:
| Feature | Status | Notes |
|---------|--------|-------|
| [Feature 1] | Working / Partial / Broken | [Notes] |
| [Feature 2] | Working / Partial / Broken | [Notes] |

---

## Phase 5: Technical & UX Observations (3-5 min)

### 5.1 Console Check
- [ ] Open DevTools console
- [ ] **Log**: Any errors present
- [ ] **Log**: Any warnings

### 5.2 Network Check
- [ ] Review network tab
- [ ] **Log**: Any failed requests
- [ ] **Note**: API patterns observed

### 5.3 Responsiveness Quick Check
- [ ] Switch to mobile viewport (375x667)
- [ ] **Check**: Does layout adapt?
- [ ] **Screenshot**: Mobile view
- [ ] **Note**: Mobile-readiness assessment

### 5.4 UX Observations
- [ ] Intuitive or confusing navigation?
- [ ] Clear or unclear affordances?
- [ ] Consistent or inconsistent design?
- [ ] Any obvious UX issues?

---

## Phase 6: Issue Logging

During exploration, log any issues encountered:

### Issue Categories for Discovery
- **Blockers**: Cannot complete core actions
- **Confusion**: Unclear purpose or navigation
- **Broken**: Features that don't work
- **Missing**: Expected features not present
- **UX Problems**: Frustrating or confusing interactions

---

## Phase 7: Synthesis & Documentation

### 7.1 Application Summary
Write a concise summary:
- What the application is
- Who it's for
- What problems it solves
- How users accomplish their goals

### 7.2 Recommended Test Scope
Based on discovery, recommend:
- [ ] Which personas are relevant?
- [ ] Which journeys to test in Quick mode?
- [ ] Which areas need Comprehensive testing?
- [ ] Any areas to skip or deprioritize?

### 7.3 Edge Cases to Explore
Based on the application purpose, derive:
- [ ] Edge case 1: [Description]
- [ ] Edge case 2: [Description]
- [ ] Edge case 3: [Description]

### 7.4 Questions for Developers
- [ ] [Any unclear aspects that need clarification]
- [ ] [Features that seem incomplete]
- [ ] [Behaviors that might be bugs or intentional]

---

## Output: Discovery Report

Generate a discovery report including:

1. **Application Profile**
   - Name, URL, type
   - Inferred purpose
   - Target users
   - Value proposition

2. **Information Architecture**
   - Navigation map
   - Feature inventory
   - Data model

3. **User Journeys**
   - Primary workflow (detailed)
   - Secondary workflows
   - User flow diagrams

4. **Technical State**
   - Console errors
   - Network issues
   - Responsiveness

5. **Issues Found**
   - Blockers
   - Bugs
   - UX problems

6. **Recommendations**
   - For Quick test scope
   - For Comprehensive test scope
   - Edge cases to test
   - Open questions

---

## Using Discovery Output

The discovery report can be used as:
- **Input for Quick/Comprehensive tests**: Already knows the app
- **Context for development**: What the app does and should do
- **Baseline documentation**: App understanding at a point in time
- **Onboarding material**: For new team members or testers
