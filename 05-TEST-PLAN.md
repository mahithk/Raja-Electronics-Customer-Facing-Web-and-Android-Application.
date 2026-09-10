# RAJA ELECTRONICS — Test Plan

## 1. Functional Testing

### Store
- [ ] Open catalogue
- [ ] Search product
- [ ] Filter products
- [ ] Sort products
- [ ] Open product details
- [ ] Add product to cart
- [ ] Change quantity
- [ ] Remove product
- [ ] Add/remove wishlist item
- [ ] Compare products
- [ ] Verify stock status

### Billing
- [ ] Enter customer details
- [ ] Add multiple line items
- [ ] Verify subtotal
- [ ] Verify GST
- [ ] Apply valid coupon
- [ ] Reject invalid/expired coupon
- [ ] Verify delivery charge
- [ ] Verify installation charge
- [ ] Verify grand total

### EMI
- [ ] Select EMI
- [ ] Select bank
- [ ] Enter valid CIBIL score
- [ ] Select tenure
- [ ] Verify interest rate
- [ ] Verify down payment
- [ ] Verify EMI summary
- [ ] Verify EMI information on invoice

### Payment
- [ ] UPI flow
- [ ] Credit card validation
- [ ] Debit card validation
- [ ] Net banking selection
- [ ] EMI down payment flow
- [ ] Cancel payment
- [ ] Payment failure
- [ ] Successful payment
- [ ] Duplicate callback protection in production

### Invoice
- [ ] Generate invoice
- [ ] Verify customer details
- [ ] Verify GST
- [ ] Verify totals
- [ ] Verify QR code
- [ ] Verify barcode
- [ ] Print invoice
- [ ] Download PDF
- [ ] Test long invoice
- [ ] Test dark mode invoice
- [ ] Test mobile invoice

## 2. Responsive Testing
Test at minimum:
- 320px
- 375px
- 390px
- 414px
- 768px
- 1024px
- 1366px
- 1920px

## 3. Browser Testing
Recommended:
- Chrome
- Edge
- Firefox
- Safari
- Android Chrome
- iOS Safari

## 4. Accessibility Testing
- [ ] Keyboard navigation
- [ ] Visible focus
- [ ] Screen reader labels
- [ ] Color contrast
- [ ] Reduced motion
- [ ] Touch target size
- [ ] Form error announcements

## 5. Security Testing
- [ ] XSS review
- [ ] Authentication testing
- [ ] Authorization testing
- [ ] API input validation
- [ ] Payment tampering attempts
- [ ] Coupon manipulation
- [ ] Price manipulation
- [ ] Invoice ID enumeration
- [ ] Sensitive data storage review

## 6. Performance Testing
- [ ] Initial load
- [ ] Catalogue rendering
- [ ] Large product lists
- [ ] Large invoice PDF
- [ ] Mobile memory usage
- [ ] Network throttling
- [ ] Slow/failed external libraries

## 7. Release Gate
A production release should not be approved until critical functional, security and payment tests pass.
