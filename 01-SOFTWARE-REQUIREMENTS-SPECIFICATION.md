# RAJA ELECTRONICS — Software Requirements Specification (SRS)

## 1. Document Purpose
This document describes the functional and non-functional requirements represented by the current RAJA ELECTRONICS customer-facing HTML application.

## 2. Product Overview
RAJA ELECTRONICS is a responsive customer-facing web application covering shopping, billing, payments, invoices, order tracking, warranty/service information, notifications, customer support, and accessibility features.

The current implementation is a front-end application/demo. Payment processing is explicitly designed to be replaced by a real payment gateway with server-side verification.

## 3. Functional Requirements

### 3.1 Storefront
- Product catalogue and product categories
- Product search
- Product filtering and sorting
- Product details
- Product stock information
- Wishlist
- Product comparison
- Shopping cart
- Quantity and pricing controls

### 3.2 Customer Account
- Customer sign-in/session handling
- Customer-specific order/invoice ownership
- Customer preferences
- Customer history

### 3.3 Billing
- Customer billing information
- Product line items
- Quantity, price and GST calculations
- Discounts and coupon handling
- Delivery charges
- Installation/technician travel fee
- Grand-total calculation

### 3.4 EMI
- Bank selection
- CIBIL score input
- Tenure selection
- Automatic interest-rate calculation
- Down-payment calculation
- EMI summary
- EMI payment flow and invoice EMI details

### 3.5 Payments
Supported UI flows include:
- UPI
- Credit Card
- Debit Card
- Net Banking
- EMI

The current payment screen validates input and simulates a gateway. Production deployment requires a backend gateway integration and server-side payment/signature verification.

### 3.6 Invoice
- Tax invoice generation
- Customer details
- GSTIN
- Invoice number/date/time
- Itemized invoice
- GST
- Discount/coupon
- Delivery and installation charges
- Grand total
- QR code
- Barcode
- EMI details
- Digital-signature presentation
- Print
- PDF download
- Invoice sharing/email flow

### 3.7 Orders and Services
- Order tracking
- Delivery status
- Warranty information
- Service/order history
- Customer notifications
- Stock updates

### 3.8 Communication
- WhatsApp contact flow
- Customer support chatbot
- Voice input/audio-related accessibility
- Email/invoice communication flow

## 4. Non-Functional Requirements

### Performance
- Responsive UI
- Optimized invoice rendering
- Canvas-size protection for long invoices
- Responsive product grids

### Usability
- Mobile-first controls
- Touch-friendly controls
- Clear validation messages
- Empty states
- Search/filter interactions

### Accessibility
- Visible keyboard focus
- Reduced-motion support
- Larger mobile touch targets
- Audio/voice assistance features

### Compatibility
The application is designed for modern desktop and mobile browsers. Production browser/device testing is required before release.

## 5. Data Requirements
The application maintains client-side state for shopping, invoices, preferences and related flows. Web Storage availability is handled with a fallback in-memory storage mechanism for restricted/opaque origins.

## 6. Security Requirements
- Never treat browser-side payment simulation as secure payment processing.
- Integrate a server-side payment gateway.
- Verify payment signatures on the server.
- Never store CVV, OTP or sensitive payment credentials.
- Protect backend APIs with authentication and authorization.
- Validate and sanitize all server-side input.
- Use HTTPS in production.

## 7. Future Backend Requirements
Recommended production services:
- Authentication service
- Product/catalogue service
- Inventory service
- Order service
- Payment service
- Invoice service
- Notification service
- Customer/service service
- Audit logging

## 8. Acceptance Criteria
A release is acceptable when:
1. Customers can browse and search products.
2. Customers can add/remove products from the cart.
3. Billing totals are calculated correctly.
4. EMI calculations are validated against approved business rules.
5. Successful production payments are verified server-side.
6. Invoices render correctly on desktop and mobile.
7. PDF/print output matches the invoice preview.
8. Orders and invoice records are associated with the correct customer.
9. Error states are handled without breaking the application.
10. Security and browser/device testing is completed.
