# Admin User Persona

## Profile

**Device**: Desktop (large monitor)
**Viewport**: 1920 x 1080
**Connection**: Stable broadband
**Context**: Management and oversight tasks

---

## Characteristics

### Technical Proficiency
- Above-average technical skills
- Power user of the application
- Comfortable with complex interfaces
- May use keyboard shortcuts

### Behavioral Patterns
- **Management-focused**: Oversees other users/content
- **Data-oriented**: Needs access to reports/analytics
- **Bulk operations**: May perform actions on multiple items
- **Security-conscious**: Expects appropriate access controls

### Expectations
- Access to admin-specific features
- Clear separation of admin vs user views
- Audit trails and logging
- Bulk action capabilities
- Dashboard/overview screens

---

## Testing Focus Areas

### Must Work Perfectly
- [ ] Admin features visible and accessible
- [ ] User management (if applicable)
- [ ] Content management (if applicable)
- [ ] Settings/configuration
- [ ] Data export/reporting

### Permission Testing
- [ ] Admin-only features hidden from regular users
- [ ] Admin can access all areas
- [ ] Elevated actions require confirmation
- [ ] No permission errors for valid actions

### Admin-Specific Workflows
- [ ] User management operations
- [ ] Content moderation
- [ ] System configuration
- [ ] Report generation
- [ ] Bulk actions

---

## Simulated Conditions

When testing as admin user:

1. Set viewport to 1920x1080
2. Login with admin credentials
3. Verify admin UI elements appear
4. Test admin-specific navigation
5. Check for admin-only features

---

## Red Flags

Issues critical for admin users:

- Admin features not accessible
- Permission errors on valid actions
- No audit trail for sensitive actions
- Bulk operations fail silently
- Admin UI hidden or confusing
- No confirmation for destructive actions
