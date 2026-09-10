# RAJA ELECTRONICS — API & Backend Integration Specification

This document defines a recommended backend contract for converting the current front-end/demo application into a production system.

## 1. Authentication

### POST /api/auth/login
Request:
```json
{
  "email": "customer@example.com",
  "password": "********"
}
```

Response:
```json
{
  "accessToken": "<token>",
  "customer": {
    "id": "CUS-001",
    "name": "Customer",
    "email": "customer@example.com"
  }
}
```

## 2. Catalogue

### GET /api/products
Supports:
- category
- search
- price range
- brand
- availability
- sorting

### GET /api/products/{productId}
Returns product specifications, pricing, stock and warranty information.

## 3. Cart

### POST /api/cart
Create/update cart.

### GET /api/cart
Retrieve the authenticated customer's cart.

## 4. Order Calculation

### POST /api/orders/quote
Server calculates:
- item subtotal
- GST
- discount
- coupon
- delivery charge
- installation charge
- final total

The client-provided total must not be trusted.

## 5. Payment

### POST /api/payments/create-order
Creates a gateway order from a server-calculated amount.

### POST /api/payments/verify
Verifies the gateway response/signature.

### POST /api/payments/webhook
Receives gateway status notifications.

## 6. Invoice

### GET /api/invoices/{invoiceId}
Returns invoice data after authorization.

### GET /api/invoices/{invoiceId}/pdf
Returns the generated invoice PDF.

### POST /api/invoices/{invoiceId}/send
Triggers approved email/notification delivery.

## 7. Orders

### GET /api/orders
Returns only the authenticated customer's orders.

### GET /api/orders/{orderId}
Returns order status and tracking information.

## 8. Warranty/Service

### GET /api/services
Returns customer service/warranty history.

### POST /api/services/request
Creates a service request.

## 9. Notifications

### GET /api/notifications
Returns customer notifications.

### POST /api/notifications/read
Marks a notification as read.

## 10. Security Rules
- All protected APIs require authentication.
- Authorization must be checked for every customer-owned resource.
- Financial amounts are recalculated server-side.
- Payment success is based on verified gateway information.
- Webhook requests must be authenticated/verified.
- Rate limiting should be applied to authentication and payment APIs.
