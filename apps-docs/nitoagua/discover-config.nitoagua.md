# Discover Mode Configuration - Nitoagua

Minimal configuration for autonomous application discovery.

---

## Application

**URL**: https://nitoagua.vercel.app

---

## Device Target

Select the primary device context for testing:

- [x] **Mobile** (recommended for mobile-first apps) - Requires manual DevTools setup
- [ ] **Desktop** (default if unchecked)

**Mobile Device**: iPhone 12 Pro (390x844)

---

## Test Credentials

Provide credentials for at least one user type. Claude will use whichever are available.

### Consumer
- **Username/Email**: consumer@nitoagua.cl
- **Password**: consumer.123
- **Role**: Standard consumer user accessing via mobile device
- **Notes**: Primary user type - orders water

### Provider
- **Username/Email**: provider@nitoagua.cl
- **Password**: provider.123
- **Role**: Standard provider user accessing via mobile device
- **Notes**: Supplier side - fulfills water orders

### Admin
- **Username/Email**: admin@nitoagua.cl
- **Password**: admin.123
- **Role**: Administrative user
- **Notes**: Platform management

---

## Notes

- App is still in beta, some features may be incomplete
- App is intended to be used on mobile devices only
- Three distinct user types: Consumer, Provider, Admin

---

## Pre-Discovery Checklist

Before starting discovery, ensure:

- [ ] Chrome browser is open
- [ ] Claude Chrome Extension is connected
- [x] **Mobile testing required**: Enable DevTools mobile emulation (F12 → Ctrl+Shift+M → iPhone 12 Pro)
- [ ] Test credentials are valid and accounts are not locked

---

*That's it. Claude will figure out the rest.*
