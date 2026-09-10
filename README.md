⚡ RAJA ELECTRONICS — User Website & Android App

Smart Shopping • Easy Billing • Flexible EMI • Reliable Support

RAJA ELECTRONICS is a customer-focused electronics shopping platform that brings product discovery, shopping, billing, payments, GST invoicing, EMI management, warranty tracking, order tracking, customer accounts, and support into one responsive experience.

✨ Key Features

🛍️ Shopping

Product catalogue with categories and featured products

Search by product, brand, category, and budget

Advanced filters and sorting

Product quick view and detailed specifications

Price, discount, GST, stock, model, serial and warranty information

Wishlist and product comparison

Shopping cart with quantity management

Checkout and billing flow

💳 Billing & Payments

Customer, billing and shipping details

Discounts and coupon support

Delivery-distance and technician/installation charges

UPI, Credit/Debit Card, Net Banking, Cash and EMI options

EMI calculator with tenure and down-payment information

EMI instalment payment flow

Payment confirmation and receipts

The source contains a dedicated payment flow and notes that a real gateway plus server-side verification should replace the current front-end/demo payment behaviour before production deployment. fileciteturn7file0L54-L59

🧾 GST Invoice & PDF

Professional GST invoice generation

Invoice number, date, customer and product details

GST calculations and totals

QR code and barcode

Invoice preview

Print invoice

Download invoice as PDF

Email/share support

Print-friendly invoice layout

Black & white invoice support

QR and barcode generation are built directly into the invoice rendering flow. fileciteturn8file5L268-L305

📦 Orders, Stock & Warranty

Order history

Order tracking:
Order Confirmed → Packed → Shipped → Out for Delivery → Delivered

Order notifications

Persistent inventory/stock ledger

Stock reduction when an invoice is completed

Product serial tracking

Warranty information and countdown

Installation and service support

The stock ledger is designed to keep catalogue stock synchronized with actual sold quantities. fileciteturn8file7L439-L485

👤 Customer Account

Sign in

Create account

OTP login

Password login

Password strength validation

Password visibility toggle

Customer-specific orders, invoices, EMI plans and warranties

The authentication interface provides separate Sign in, OTP and Sign up modes. fileciteturn8file10L637-L667

🤖 Smart Customer Chatbot

The built-in assistant can help customers with:

Product search

Price and offers

EMI

Warranty

Delivery

Installation

Returns

Billing

Order tracking

Product specifications

Stock availability

Voice input is also supported in compatible browsers. fileciteturn8file13L833-L884

📞 Customer Support

Floating WhatsApp support

Direct phone calling

Shop directions

Email support

Installation/demo information

Delivery and return guidance

WhatsApp support opens a ready-to-use customer assistance message. fileciteturn8file6L385-L403

🌐 Accessibility & UX

Responsive mobile, tablet and desktop design

Dark / Light theme

Audio assistance / text-to-speech

Voice product search

Keyboard focus support

Reduced-motion support

Mobile-friendly touch targets

Responsive product, cart, payment and invoice layouts

Multilingual interface support

The source includes dedicated responsive and mobile usability rules, including larger touch targets and reduced-motion handling. fileciteturn6file0L593-L616

🧰 Technology Stack

HTML5

CSS3

Vanilla JavaScript

Responsive CSS / Media Queries

Web Storage

jsPDF — PDF generation

html2canvas — HTML/document rendering

QRCode.js — QR generation

Web Speech API — voice search and chatbot voice input

WhatsApp integration

Browser APIs for printing, sharing and navigation

The current HTML references jsPDF, html2canvas and QRCode.js. fileciteturn6file0L129-L135

📱 Responsive Design

Designed to work across:

📱 Mobile phones

📲 Small-screen devices

💻 Laptops

🖥️ Desktop screens

🖨️ Print/PDF layouts

Special mobile handling is included for product grids, cart actions, forms, modals, payment screens and invoices. fileciteturn6file0L607-L667

🚀 Getting Started

Run with VS Code

Clone the repository.

Open the project in Visual Studio Code.

Open index1_v68.html.

Run it using Live Server or another local HTTP server.

Open the displayed local URL in your browser.

Run with Python

If Python is installed:

python -m http.server 8000

Then open:

http://localhost:8000

Serving through HTTP/HTTPS is recommended instead of opening the HTML through an Android content:// URI. The project includes an in-memory storage fallback for environments where browser storage is unavailable. fileciteturn6file0L30-L40

🔄 Customer Journey

🏠 Home
   ↓
🔎 Search / Categories
   ↓
📦 View Product
   ↓
❤️ Wishlist / ⚖️ Compare / 🛒 Cart
   ↓
🧾 Checkout & Billing
   ↓
💳 Payment / EMI
   ↓
✅ Payment Confirmation
   ↓
🧾 GST Invoice
   ↓
📍 Order Tracking
   ↓
🛡️ Warranty & Service

⭐ Feature Overview

Feature

Status

Product Catalogue

✅

Search & Filters

✅

Wishlist

✅

Product Compare

✅

Shopping Cart

✅

Billing

✅

Coupons

✅

UPI / Card / Net Banking / Cash

✅

EMI Calculator

✅

EMI Instalments

✅

GST Invoice

✅

PDF Invoice

✅

QR Code

✅

Barcode

✅

Order Tracking

✅

Inventory / Stock Ledger

✅

Warranty Tracking

✅

Customer Login

✅

OTP Login

✅

Customer Signup

✅

Chatbot

✅

Voice Search

✅

WhatsApp Support

✅

Dark Mode

✅

Responsive UI

✅

Print Support

✅

🔐 Production Security Note

This project contains front-end/demo implementations for some business operations. Before production use:

Move authentication to a secure backend.

Integrate a real payment gateway.

Perform server-side payment/signature verification.

Store authoritative inventory on the server.

Protect customer and invoice data with proper authorization.

Move sensitive business logic away from browser-only JavaScript.

Add backend APIs, validation, logging and audit controls.

📂 Suggested Repository Structure

raja-electronics-user-app/
│
├── index1_v68.html
├── README.md
├── assets/
│   ├── images/
│   ├── icons/
│   └── ...
│
├── website/
│   └── ...
│
└── apk/
    └── Raja-Electronics.apk

Adjust this structure according to the files included in your GitHub repository.

🎯 Project Goal

RAJA ELECTRONICS aims to transform the traditional electronics-store experience into a modern digital platform where customers can discover products, compare options, manage their cart, choose flexible payment methods, receive GST invoices, track orders, manage warranties, and contact support from one place.

🛠️ Future Improvements

Secure backend authentication

Real payment gateway integration

Server-side payment verification

Database-backed products and inventory

Admin dashboard

Role-based access control

Secure order and invoice APIs

Cloud image storage/CDN

Automated email and WhatsApp notifications

Automated testing and CI/CD

Modularize the large single-page HTML into maintainable files

📄 License

Add your preferred license here.

Example:

Copyright © RAJA ELECTRONICS.
All rights reserved.

💙 RAJA ELECTRONICS

Quality • Service • Trust

Built to make electronics shopping simple, transparent and customer-friendly.
