# Quick Test Plan

**Duration**: ~15-20 minutes
**Focus**: Major flows, critical functionality, obvious issues
**Depth**: Surface-level validation

---

## Pre-Test Setup

- [ ] Load test configuration from `/config/`
- [ ] Set viewport to mobile (375x667) for mobile user testing
- [ ] Open browser DevTools console (to monitor errors)
- [ ] Start network request monitoring
- [ ] Create report file in `/reports/`

---

## Phase 1: Initial Load & Login (3-5 min)

### 1.1 Application Load
- [ ] Navigate to application URL
- [ ] **Check**: Page loads without errors
- [ ] **Check**: No console errors on initial load
- [ ] **Check**: Network requests complete successfully
- [ ] **Check**: Visual elements render correctly
- [ ] **Screenshot**: Initial state

### 1.2 Authentication
- [ ] Locate login form/button
- [ ] Enter test credentials
- [ ] Submit login
- [ ] **Check**: Login succeeds
- [ ] **Check**: Redirect to appropriate landing page
- [ ] **Check**: User session established
- [ ] **Screenshot**: Post-login state

---

## Phase 2: Navigation & Structure (3-5 min)

### 2.1 Primary Navigation
- [ ] Identify main navigation elements
- [ ] Click through each primary nav item
- [ ] **Check**: All nav links functional
- [ ] **Check**: Current page indicator works
- [ ] **Check**: No dead links

### 2.2 Information Architecture
- [ ] **Check**: Content organization is logical
- [ ] **Check**: User can find main features
- [ ] **Check**: Breadcrumbs/back navigation works (if present)

---

## Phase 3: Core Journey (5-7 min)

### 3.1 Primary User Flow
Based on application purpose, execute the main user journey:

- [ ] Identify the primary action user wants to take
- [ ] Execute the flow step-by-step
- [ ] **Check**: Each step completes successfully
- [ ] **Check**: Feedback is provided at each step
- [ ] **Check**: Final outcome is achieved
- [ ] **Screenshot**: Key states in the flow

### 3.2 Secondary Actions
- [ ] Test 1-2 secondary features
- [ ] **Check**: Features work as expected
- [ ] **Check**: Data persists correctly

---

## Phase 4: Responsiveness (2-3 min)

### 4.1 Mobile Viewport (375x667)
- [ ] **Check**: Layout adapts correctly
- [ ] **Check**: No horizontal scroll
- [ ] **Check**: Touch targets are adequate size
- [ ] **Check**: Text is readable
- [ ] **Screenshot**: Mobile view

### 4.2 Tablet Viewport (768x1024)
- [ ] **Check**: Layout transition is smooth
- [ ] **Check**: No broken layouts

---

## Phase 5: Quick Health Checks (2-3 min)

### 5.1 Console Errors
- [ ] Review browser console
- [ ] **Log**: Any errors or warnings
- [ ] **Severity**: Critical / Warning / Info

### 5.2 Network Issues
- [ ] Review failed requests
- [ ] **Log**: Any 4xx or 5xx responses
- [ ] **Check**: No unnecessary requests

### 5.3 Basic Accessibility
- [ ] Tab through interactive elements
- [ ] **Check**: Focus indicators visible
- [ ] **Check**: Logical tab order

---

## Post-Test

- [ ] Compile findings into report
- [ ] Attach screenshots
- [ ] Log console/network errors
- [ ] Assign severity to issues
- [ ] Generate executive summary

---

## Issue Severity Guide

| Severity | Definition |
|----------|------------|
| **Blocker** | Prevents core functionality, no workaround |
| **Major** | Significant impact on user experience |
| **Minor** | Inconvenient but workaround exists |
| **Cosmetic** | Visual/polish issues, no functional impact |
