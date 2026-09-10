# Contributing to RAJA ELECTRONICS

## Development Guidelines

### Code
- Keep JavaScript functions focused.
- Prefer reusable modules over large global scripts.
- Use consistent naming.
- Validate external/user input.
- Avoid unsafe dynamic HTML.
- Handle errors explicitly.

### UI
- Preserve responsive behavior.
- Maintain keyboard accessibility.
- Test touch targets on mobile.
- Respect reduced-motion preferences.
- Verify dark mode and print layouts.

### Payments
Never implement production payment verification entirely in browser JavaScript.

### Pull Requests
A pull request should include:
1. Summary of change
2. Reason for change
3. Screenshots for UI changes
4. Testing performed
5. Security impact
6. Any required configuration changes

## Commit Examples

```text
feat: add product comparison
fix: correct invoice PDF rendering
fix: prevent duplicate coupon redemption
feat: add EMI summary
docs: update deployment guide
security: harden payment verification
```
