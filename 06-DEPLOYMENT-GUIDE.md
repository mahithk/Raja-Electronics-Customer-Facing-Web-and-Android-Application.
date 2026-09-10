# RAJA ELECTRONICS — Deployment Guide

## 1. Local Development

The current application can be opened using a local HTTP server.

Example with Python:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000/
```

Using an HTTP server is preferable to opening the HTML directly because browser storage and external integration behavior can differ on `file://` or opaque origins.

## 2. Recommended Production Hosting
Suitable static hosting options include:
- Nginx
- Apache
- Cloudflare Pages
- GitHub Pages for a front-end/demo build
- Other approved static hosting/CDN platforms

## 3. Production Requirements
Before production:
- Use HTTPS.
- Move payment processing to the backend.
- Remove demo credentials/data.
- Configure approved backend API URLs.
- Configure production payment gateway.
- Configure email/WhatsApp notification service.
- Add monitoring and error logging.
- Configure backups for backend data.

## 4. GitHub Repository Structure

```text
raja-electronics-user-app/
├── index.html
├── README.md
├── docs/
│   ├── 01-SOFTWARE-REQUIREMENTS-SPECIFICATION.md
│   ├── 02-TECHNICAL-SPECIFICATION.md
│   ├── 03-SYSTEM-ARCHITECTURE.md
│   ├── 04-API-BACKEND-INTEGRATION-SPEC.md
│   ├── 05-TEST-PLAN.md
│   ├── 06-DEPLOYMENT-GUIDE.md
│   ├── 07-SECURITY-AND-COMPLIANCE.md
│   └── 08-USER-GUIDE.md
├── assets/
└── .gitignore
```

## 5. GitHub Pages
GitHub Pages is appropriate for demonstrating the static front-end.

For production payments and customer data, use a proper backend and secure deployment architecture.

## 6. Release Checklist
- [ ] Update version
- [ ] Run functional tests
- [ ] Run security review
- [ ] Test mobile
- [ ] Test PDF generation
- [ ] Test payment integration
- [ ] Verify no secrets are committed
- [ ] Update changelog
- [ ] Create Git tag/release
