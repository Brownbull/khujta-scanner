# Common User Persona

## Profile

**Device**: Desktop/Laptop
**Viewport**: 1280 x 800 (standard laptop)
**Connection**: Stable broadband
**Context**: Focused task completion

---

## Characteristics

### Technical Proficiency
- Average computer user
- Comfortable with standard web conventions
- Uses mouse and keyboard
- May use keyboard shortcuts for common actions

### Behavioral Patterns
- **Goal-oriented**: Comes with a specific task in mind
- **Efficiency-focused**: Wants to complete tasks quickly
- **Standard expectations**: Follows learned web patterns
- **Moderate patience**: Will try a few times before giving up

### Expectations
- Familiar UI patterns (buttons look like buttons)
- Clear confirmation of actions
- Predictable navigation
- Visible feedback on interactions
- Reasonable load times (<3 seconds)

---

## Testing Focus Areas

### Must Work Perfectly
- [ ] Primary user journey end-to-end
- [ ] All core features functional
- [ ] Data saves and persists
- [ ] Navigation clear and complete
- [ ] Error messages helpful

### Common Pain Points to Check
- [ ] Confusing terminology or labels
- [ ] Hidden features or unclear CTAs
- [ ] Lack of feedback after actions
- [ ] Unexpected navigation behavior
- [ ] Lost data after errors
- [ ] Inconsistent UI patterns

### Workflow Testing
- [ ] Complete primary task
- [ ] Complete secondary tasks
- [ ] Switch between features
- [ ] Return to previous state

---

## Simulated Conditions

When testing as common user:

1. Set viewport to 1280x800
2. Use standard mouse/keyboard interaction
3. Don't use DevTools or special debugging
4. Approach tasks as if unfamiliar with internal logic

---

## Red Flags

Issues that frustrate common users:

- Can't figure out how to do main task
- Actions don't provide feedback
- Data disappears unexpectedly
- Navigation is confusing
- Error messages are unhelpful
- Features that "should just work" don't
