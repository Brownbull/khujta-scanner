# Discover Mode Configuration

Minimal configuration for autonomous application discovery.

---

## Application

**URL**: [https://your-app.com]

---

## Device Target

Select the primary device context for testing:

- [ ] **Mobile** (recommended for mobile-first apps) - Requires manual DevTools setup
- [ ] **Desktop** (default if unchecked)

**Mobile Device** (if mobile selected): iPhone 12 Pro (390x844) | iPhone SE (375x667) | Custom: [dimensions]

---

## Test Credentials

Provide credentials for at least one user type. Claude will use whichever are available.

### Common User
- **Email/Username**:
- **Password**:

### Admin User (optional)
- **Email/Username**:
- **Password**:

### Additional User Types (optional)
- **Role**: [e.g., Provider, Manager, etc.]
- **Email/Username**:
- **Password**:

---

## Notes (optional)

Any additional context that might help during discovery:

- [e.g., "App is still in beta, some features may be incomplete"]
- [e.g., "Focus on the dashboard area"]
- [e.g., "Ignore the settings page for now"]

---

## Pre-Discovery Checklist

Before starting discovery, ensure:

- [ ] Chrome browser is open
- [ ] Claude Chrome Extension is connected
- [ ] **If mobile testing**: DevTools mobile emulation is enabled (F12 → Ctrl+Shift+M → Select device)
- [ ] Test credentials are valid and accounts are not locked

---

*That's it. Claude will figure out the rest.*
