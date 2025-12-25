# Mobile User Persona

## Profile

**Device**: Smartphone (iPhone SE / Android equivalent)
**Viewport**: 375 x 667
**Connection**: Variable (4G/WiFi)
**Context**: On-the-go, potentially distracted

---

## Characteristics

### Technical Proficiency
- Moderate smartphone user
- Familiar with common mobile patterns (swipe, tap, pull-to-refresh)
- Expects app-like experience on mobile web

### Behavioral Patterns
- **Short sessions**: Quick tasks, not extended browsing
- **Interruption-prone**: May leave and return mid-task
- **Impatient**: Expects fast load times
- **Touch-first**: Uses fingers, not cursor

### Expectations
- Large, tappable buttons (minimum 44x44px)
- Clear visual feedback on interactions
- Minimal typing required
- Easy navigation back to starting point
- Content readable without zooming

---

## Testing Focus Areas

### Must Work Perfectly
- [ ] Login on mobile viewport
- [ ] Primary user journey on touch
- [ ] Navigation menu (hamburger/drawer pattern)
- [ ] Forms with mobile keyboard
- [ ] Scroll behavior

### Common Pain Points to Check
- [ ] Keyboard overlaying input fields
- [ ] Tap targets too small or too close together
- [ ] Horizontal scroll appearing
- [ ] Fixed elements blocking content
- [ ] Slow loading on simulated 3G
- [ ] Autofill behavior

### Viewport Testing
- [ ] Portrait orientation (375x667)
- [ ] Landscape orientation (667x375)
- [ ] With keyboard visible
- [ ] With browser chrome visible/hidden

---

## Simulated Conditions

When testing as mobile user:

1. Set viewport to 375x667
2. Enable touch simulation in DevTools
3. Consider throttling network to "Fast 3G"
4. Test with and without DevTools mobile emulation

---

## Red Flags

Issues that severely impact mobile users:

- Content wider than viewport
- Unresponsive tap targets
- Forms that don't work with mobile keyboards
- Excessive data usage
- No loading indicators
- Broken sticky/fixed positioning
