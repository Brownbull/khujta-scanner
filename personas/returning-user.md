# Returning User Persona

## Profile

**Device**: Variable (any)
**Viewport**: Variable
**Connection**: Variable
**Context**: User with existing data and history

---

## Characteristics

### Technical Proficiency
- Familiar with this specific application
- Knows where features are located
- Has established workflows
- May rely on muscle memory

### Behavioral Patterns
- **Expectation of continuity**: Data should persist
- **Efficiency-seeking**: Knows shortcuts and patterns
- **History-aware**: References past actions
- **Trust established**: Expects consistent behavior

### Expectations
- Previous data still available
- Account settings preserved
- Preferences remembered
- Quick access to frequent features
- History/activity visible

---

## Testing Focus Areas

### Must Work Perfectly
- [ ] Login with existing account
- [ ] Previous data loads correctly
- [ ] User preferences persist
- [ ] Session state maintained
- [ ] History/activity accessible

### Data Persistence Testing
- [ ] User profile data intact
- [ ] Previous work/content visible
- [ ] Settings preserved
- [ ] Preferences honored
- [ ] No unexpected data loss

### Continuity Testing
- [ ] Multi-session persistence
- [ ] Cross-device consistency (if applicable)
- [ ] State recovery after logout
- [ ] Progress saved on return

---

## Simulated Conditions

When testing as returning user:

1. Use test account with existing data
2. Verify data loaded before proceeding
3. Check that preferences are applied
4. Test logout and re-login
5. Verify state persists across sessions

---

## Test Scenarios

### Scenario 1: Return After Session Break
- Login with returning user credentials
- Check: All previous data visible
- Check: No "first-time" prompts shown
- Check: Recent activity accessible

### Scenario 2: Continue Previous Work
- Login and locate previous incomplete task
- Check: Can resume from where left off
- Check: No data loss in progress

### Scenario 3: Access History
- Navigate to history/activity section
- Check: Past actions recorded
- Check: Can reference or repeat past actions

---

## Red Flags

Issues critical for returning users:

- Data appears lost or reset
- "New user" experience on return
- Settings not preserved
- Previous work inaccessible
- Unexpected changes to account
- Session suddenly invalid
