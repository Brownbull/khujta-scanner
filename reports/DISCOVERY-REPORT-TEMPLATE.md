# Discovery Report: [Application Name]

**Discovery Date**: [YYYY-MM-DD]
**Discoverer**: Claude Code + Chrome Extension
**Mode**: Discover (Autonomous Exploration)
**Duration**: [Time taken]

---

## Executive Summary

### Application at a Glance

| Attribute | Value |
|-----------|-------|
| **Name** | [Application Name] |
| **URL** | [URL] |
| **Type** | [e.g., Task Management, E-commerce, Analytics] |
| **Target Users** | [e.g., Teams, Consumers, Enterprises] |
| **Maturity** | [Production-ready / Beta / Early development] |
| **Overall State** | [Functional / Partially functional / Significant issues] |

### Key Findings

- [Most important discovery about the app]
- [Second most important finding]
- [Third important observation]

### Issues Found During Discovery

| Severity | Count |
|----------|-------|
| Blockers | X |
| Major | X |
| Minor | X |

---

## Application Profile

### What Is This Application?

[2-3 paragraph explanation of what this application is, written as if explaining to someone who has never seen it]

### Inferred Purpose

**Problem Being Solved**:
[What problem or need does this application address?]

**Value Proposition**:
[What benefit does a user get from using this application?]

**Core Functionality**:
[The main thing(s) users can do with this application]

### Target Users

**Primary Audience**:
[Who is this application primarily built for?]

**User Characteristics**:
- Technical level: [Technical / Non-technical / Mixed]
- Usage context: [Work / Personal / Both]
- Frequency: [Daily / Weekly / Occasional]

### Application Type Classification

- [ ] Productivity / Task Management
- [ ] E-commerce / Marketplace
- [ ] Social / Community
- [ ] Content / Media
- [ ] Analytics / Dashboard
- [ ] Communication / Messaging
- [ ] Education / Learning
- [ ] Finance / Accounting
- [ ] SaaS Tool
- [ ] Other: [Specify]

---

## Information Architecture

### Navigation Structure

```
[Application Name]
├── [Primary Nav Item 1]
│   ├── [Sub-item 1.1]
│   └── [Sub-item 1.2]
├── [Primary Nav Item 2]
│   ├── [Sub-item 2.1]
│   ├── [Sub-item 2.2]
│   └── [Sub-item 2.3]
├── [Primary Nav Item 3]
└── [User Menu]
    ├── [Profile]
    ├── [Settings]
    └── [Logout]
```

### Feature Inventory

| Feature | Location | Purpose | Status |
|---------|----------|---------|--------|
| [Feature 1] | [Nav path] | [What it does] | Working / Partial / Broken |
| [Feature 2] | [Nav path] | [What it does] | Working / Partial / Broken |
| [Feature 3] | [Nav path] | [What it does] | Working / Partial / Broken |

### Data Model (Inferred)

**Core Entities**:
- **[Entity 1]**: [Description, e.g., "Projects - containers for organizing work"]
- **[Entity 2]**: [Description]
- **[Entity 3]**: [Description]

**Relationships**:
- [Entity 1] has many [Entity 2]
- [Entity 2] belongs to [Entity 1]
- [etc.]

---

## User Journeys

### Primary Journey: [Name]

**Goal**: [What the user is trying to accomplish]
**Starting Point**: [Where user begins]
**Success Criteria**: [How user knows they succeeded]

**Steps**:
1. [Step 1]
2. [Step 2]
3. [Step 3]
4. [Step 4]

**Observations**:
- [What works well]
- [What could be confusing]
- [Any issues encountered]

**Screenshot**: [Reference to screenshot]

---

### Secondary Journey: [Name]

**Goal**: [What the user is trying to accomplish]
**Starting Point**: [Where user begins]

**Steps**:
1. [Step 1]
2. [Step 2]
3. [Step 3]

**Observations**:
[Notes about this workflow]

---

### Additional Journeys Identified

| Journey | Description | Priority |
|---------|-------------|----------|
| [Journey 3] | [Brief description] | High / Medium / Low |
| [Journey 4] | [Brief description] | High / Medium / Low |
| [Journey 5] | [Brief description] | High / Medium / Low |

---

## Technical State

### Console Errors

| Type | Count | Summary |
|------|-------|---------|
| Errors | X | [Brief description of error patterns] |
| Warnings | X | [Brief description of warning patterns] |

**Notable Errors**:
```
[Paste significant console errors here]
```

### Network Issues

| Issue Type | Count | Details |
|------------|-------|---------|
| Failed requests (4xx) | X | [Details] |
| Failed requests (5xx) | X | [Details] |
| Slow requests (>3s) | X | [Details] |

### Responsiveness

| Viewport | Status | Notes |
|----------|--------|-------|
| Mobile (375x667) | Good / Partial / Poor | [Notes] |
| Tablet (768x1024) | Good / Partial / Poor | [Notes] |
| Desktop (1280x800) | Good / Partial / Poor | [Notes] |

---

## Issues Found

### Issues Summary

| ID | Severity | Category | Summary |
|----|----------|----------|---------|
| DIS-001 | [Severity] | [Category] | [Brief description] |
| DIS-002 | [Severity] | [Category] | [Brief description] |

### Issue Details

#### DIS-001: [Issue Title]

**Severity**: Blocker / Major / Minor
**Category**: [Functionality / Navigation / UX / Technical]
**Location**: [Where in the app]

**Description**:
[What's wrong]

**Impact**:
[How this affects users]

**Screenshot**: [Reference]

---

## Reasoning & Analysis

### How I Determined the Application Purpose

[Explain the reasoning process - what clues led to the conclusions about what this app is for]

**Evidence observed**:
1. [Clue 1 - e.g., "Dashboard shows project timelines and task lists"]
2. [Clue 2 - e.g., "Navigation includes 'Team', 'Projects', 'Reports'"]
3. [Clue 3 - e.g., "Data structure suggests team collaboration focus"]

**Conclusion**:
[Summary of what the app is based on evidence]

### Confidence Assessment

| Aspect | Confidence | Reasoning |
|--------|------------|-----------|
| Application type | High / Medium / Low | [Why] |
| Target users | High / Medium / Low | [Why] |
| Primary journey | High / Medium / Low | [Why] |
| Feature completeness | High / Medium / Low | [Why] |

### Uncertainties & Open Questions

- [ ] [Question 1 - something unclear about the app]
- [ ] [Question 2 - behavior that might be bug or feature]
- [ ] [Question 3 - missing functionality or intentional omission?]

---

## Recommendations

### For Quick Test

Focus on these areas:
1. [Primary journey to test]
2. [Secondary journey to test]
3. [Critical feature to verify]

**Suggested personas**: [Which personas are relevant]
**Estimated time**: ~15-20 minutes

### For Comprehensive Test

Additional areas to cover:
1. [Edge cases specific to this app]
2. [Form validation scenarios]
3. [Error handling paths]
4. [Admin features if applicable]

**Suggested personas**: [All relevant personas]
**Estimated time**: ~1-2 hours

### Derived Edge Cases

Based on the application purpose, test these scenarios:

| Edge Case | Description | Why It Matters |
|-----------|-------------|----------------|
| [Edge case 1] | [Description] | [Impact if broken] |
| [Edge case 2] | [Description] | [Impact if broken] |
| [Edge case 3] | [Description] | [Impact if broken] |

### For Development Team

**Strengths observed**:
- [What's working well]
- [Good UX patterns]

**Areas needing attention**:
- [Issues to fix]
- [UX improvements]

**Questions to clarify**:
- [Unclear behaviors]
- [Missing features?]

---

## Screenshots Index

| Filename | Description |
|----------|-------------|
| discovery-initial.png | Initial application state |
| discovery-dashboard.png | Main dashboard view |
| discovery-feature-x.png | [Feature X] section |
| discovery-mobile.png | Mobile viewport |

---

## Appendix

### Full Navigation Map

[Detailed navigation structure if complex]

### All Console Output

```
[Full console log if relevant]
```

### Session Details

- **Browser**: Chrome via Claude Chrome Extension
- **Date/Time**: [YYYY-MM-DD HH:MM]
- **Credentials Used**: [User type, not actual credentials]
- **Starting URL**: [URL]

---

## Using This Report

This discovery report can be used as:

1. **Input for Quick/Comprehensive tests**: Load this report to skip discovery phase
2. **Development context**: Understanding of what the app does and should do
3. **Onboarding document**: For team members unfamiliar with the application
4. **Baseline**: Point-in-time understanding for tracking changes
