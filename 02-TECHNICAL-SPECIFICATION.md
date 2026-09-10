# RAJA ELECTRONICS — Technical Specification

## 1. Technology Profile
The current application is implemented as a large HTML document containing:
- HTML markup
- CSS styles
- JavaScript application logic
- Responsive media queries
- Client-side storage
- PDF/invoice rendering logic
- QR and barcode generation

External browser libraries currently referenced include:
- jsPDF
- html2canvas
- QRCode.js
- Google Fonts

## 2. UI Architecture

### Major Areas
1. Navigation/header
2. Home/hero area
3. Storefront/catalogue
4. Search/filter controls
5. Product cards
6. Product details
7. Cart
8. Wishlist
9. Compare
10. Billing
11. EMI
12. Payment modal
13. Invoice
14. Order tracking
15. Notifications
16. Support/chatbot
17. Footer

## 3. Styling Architecture
The application uses CSS custom properties for:
- Brand colors
- Typography
- Spacing
- Border radius
- Shadows
- Transitions
- Layout sizing

Responsive breakpoints are used for desktop, tablet and mobile layouts.

The design also includes:
- Dark mode
- Print-specific styling
- Reduced-motion handling
- Mobile touch-target improvements

## 4. State Management
Application state is maintained primarily in JavaScript variables and browser storage.

The source contains a storage compatibility layer that tests whether native `localStorage`/`sessionStorage` are usable and falls back to memory-backed storage when required.

## 5. Invoice Rendering
Invoice generation is a core subsystem.

The invoice supports:
- A4-style presentation
- On-screen fitting
- Print layout
- PDF capture
- QR code
- Barcode
- EMI information
- Tax and total breakdown

Long-invoice canvas scaling is guarded to reduce failures on mobile Safari.

## 6. Payment Architecture
Current architecture:

Browser
→ Billing
→ Payment UI
→ Client-side validation
→ Demo/simulated gateway
→ Invoice generation

Required production architecture:

Browser
→ Backend order creation
→ Payment gateway
→ Gateway callback/webhook
→ Backend verification
→ Order/payment confirmation
→ Invoice generation
→ Notification

## 7. Recommended Production Module Split

```text
src/
├── app/
│   ├── app.js
│   ├── router.js
│   └── state.js
├── components/
│   ├── header.js
│   ├── product-card.js
│   ├── cart.js
│   ├── billing.js
│   ├── payment.js
│   └── invoice.js
├── services/
│   ├── api.js
│   ├── auth.js
│   ├── payment.js
│   ├── invoice.js
│   ├── notification.js
│   └── storage.js
├── utils/
│   ├── validation.js
│   ├── currency.js
│   └── formatting.js
├── styles/
│   ├── variables.css
│   ├── layout.css
│   ├── components.css
│   └── responsive.css
└── index.html
```

## 8. External Integration Points
Production integration candidates mentioned by the current source include payment gateways and WhatsApp Business/Twilio-style notification integration.

These integrations should be implemented behind backend APIs rather than exposing secrets in browser JavaScript.
