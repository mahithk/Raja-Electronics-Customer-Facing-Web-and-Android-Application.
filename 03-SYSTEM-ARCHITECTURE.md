# RAJA ELECTRONICS — System Architecture

## 1. Current Front-End Architecture

```text
                ┌──────────────────────────┐
                │       Customer Browser   │
                └────────────┬─────────────┘
                             │
             ┌───────────────┼────────────────┐
             │               │                │
             ▼               ▼                ▼
        Storefront        Billing          Account
             │               │                │
             ▼               ▼                ▼
          Cart            EMI/Pay         History
             │               │                │
             └───────────────┼────────────────┘
                             ▼
                         Invoice
                      ┌──────┴──────┐
                      ▼             ▼
                    Print          PDF
```

## 2. Recommended Production Architecture

```text
                         Customer
                            │
                            ▼
                    Web / Android App
                            │
                            ▼
                       API Gateway
                            │
       ┌────────────────────┼─────────────────────┐
       ▼                    ▼                     ▼
 Authentication        Catalogue/Stock        Orders
       │                    │                     │
       └────────────────────┼─────────────────────┘
                            ▼
                       Billing Service
                            │
                            ▼
                       Payment Service
                            │
                     Payment Gateway
                            │
                            ▼
                    Verified Payment
                            │
            ┌───────────────┼───────────────┐
            ▼               ▼               ▼
         Invoice        Notification      Audit
            │               │
            ▼               ▼
         PDF/Email      WhatsApp/SMS
```

## 3. Security Boundary
The browser should be treated as an untrusted client.

Business-critical values must be validated on the server:
- Product price
- Stock availability
- Discount
- Coupon validity
- GST
- Delivery fee
- Installation fee
- EMI terms
- Final payable amount
- Payment status
- Invoice ownership

## 4. Data Ownership
Orders, invoices and customer records should be persisted in a backend database.

The client may cache presentation state, but cached state must never become the authoritative source for financial or authorization decisions.

## 5. Availability and Failure Handling
The production system should handle:
- Payment timeout
- Payment cancellation
- Duplicate payment callbacks
- Network failure
- Invoice-generation failure
- Out-of-stock conditions
- Session expiry
- Invalid coupon
- Backend timeout
