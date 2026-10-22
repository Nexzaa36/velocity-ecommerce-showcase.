<div align="center">

# VELOCITY

### A Modern E-Commerce Platform

A full-stack online shopping experience powered by a Node.js backend, MongoDB, and event-driven messaging.

[**View Live Store**](https://velocity-ecom.vercel.app) · [**Backend Health**](https://velocity-y30h.onrender.com/api/health)

<br />

![Status](https://img.shields.io/badge/status-deployed-success)
![Frontend](https://img.shields.io/badge/frontend-HTML%20%7C%20CSS%20%7C%20JavaScript-orange)
![Backend](https://img.shields.io/badge/backend-Node.js%20%7C%20Express-green)
![Database](https://img.shields.io/badge/database-MongoDB-brightgreen)
![Messaging](https://img.shields.io/badge/messaging-RabbitMQ-orange)

</div>

---

## Project Preview

> Replace the placeholders below with screenshots from the live website. Add the images to a `screenshots/` folder in this repository and keep the filenames consistent.

<table>
  <tr>
    <td align="center" width="50%">
      <strong>Storefront</strong><br />
      <img src="screenshots/homepage.png" alt="VELOCITY storefront screenshot" width="100%" />
    </td>
    <td align="center" width="50%">
      <strong>Product Catalogue</strong><br />
      <img src="screenshots/catalogue.png" alt="VELOCITY product catalogue screenshot" width="100%" />
    </td>
  </tr>
  <tr>
    <td align="center" width="50%">
      <strong>Shopping Cart</strong><br />
      <img src="screenshots/cart.png" alt="VELOCITY shopping cart screenshot" width="100%" />
    </td>
    <td align="center" width="50%">
      <strong>Order Tracking</strong><br />
      <img src="screenshots/order-tracking.png" alt="VELOCITY order tracking screenshot" width="100%" />
    </td>
  </tr>
</table>

<details>
  <summary><strong>More screenshots to add</strong></summary>

  - `screenshots/product-details.png` — Product details
  - `screenshots/checkout.png` — Checkout (test mode)
  - `screenshots/admin-dashboard.png` — Admin dashboard

</details>

---

## Overview

**VELOCITY** is a deployed e-commerce application built to demonstrate a complete shopping workflow alongside backend services and asynchronous event processing. The static frontend is hosted on Vercel, while the Node.js/Express API runs on Render. MongoDB stores application data, and CloudAMQP provides hosted RabbitMQ messaging for background workflows.

This public repository is a **project showcase only**. The source code is maintained separately in a private repository.

## Key Capabilities

- **User authentication** — JWT-based authentication with password hashing
- **Product browsing** — Product catalogue and product details
- **Shopping cart** — Cart API integration
- **Orders and tracking** — Order workflow and status timeline
- **Payment integration** — Razorpay integration configured for test mode
- **Event-driven processing** — RabbitMQ messaging and SAGA-style workflows
- **Resilience patterns** — Retry and dead-letter queue handling
- **API security** — Protected routes, rate limiting, and security headers
- **Containerization** — Docker image for the backend
- **Continuous integration** — GitHub Actions workflow for dependency installation and Docker build

## Technology Stack

| Component | Technology |
|---|---|
| Frontend | HTML, CSS, JavaScript |
| Backend API | Node.js, Express |
| Database | MongoDB |
| Message broker | RabbitMQ via CloudAMQP |
| Authentication | JSON Web Tokens (JWT), bcrypt |
| Payments | Razorpay — test mode |
| Frontend hosting | Vercel |
| Backend hosting | Render |
| Containerization | Docker |
| CI workflow | GitHub Actions |

## System Architecture

```text
┌──────────────────────────┐
│      Customer Browser    │
└────────────┬─────────────┘
             │ HTTPS
             ▼
┌──────────────────────────┐
│   Vercel — Static UI     │
│     HTML / CSS / JS      │
└────────────┬─────────────┘
             │ REST API
             ▼
┌──────────────────────────┐
│ Render — Express API     │
│ Authentication & Orders │
└───────┬───────────┬──────┘
        │           │
        ▼           ▼
┌─────────────┐  ┌────────────────────┐
│  MongoDB    │  │ CloudAMQP RabbitMQ │
│ Application │  │ Async event flows  │
│    data     │  │ Retry / DLQ / SAGA │
└─────────────┘  └────────────────────┘
```

## Live Deployment

| Resource | Link |
|---|---|
| Live storefront | [velocity-ecom.vercel.app](https://velocity-ecom.vercel.app) |
| Backend health endpoint | [velocity-y30h.onrender.com/api/health](https://velocity-y30h.onrender.com/api/health) |

The health endpoint is intended as a basic availability check, not as API documentation.

## Engineering and Testing

Development and deployment work included:

- API endpoint checks with Postman
- Local health endpoint verification
- A local load-test baseline against the health endpoint
- RabbitMQ failure and recovery checks
- Docker image build and container execution
- GitHub Actions CI verification
- Production frontend-to-backend connectivity checks

**Testing note:** The load-test result was a local baseline against the health endpoint. It should not be interpreted as a production capacity or performance guarantee.

## Commercial Inquiries

VELOCITY may be available for purchase or commercial licensing.

**Contact:** _Add your preferred business email or contact link here._

Before any sale, document what is included: source-code access, setup assistance, deployment migration, domain arrangements, maintenance, and third-party service costs. Transfers of hosting or provider accounts are subject to each provider's terms.

## Security Notes

- This public repository should contain documentation and approved screenshots only.
- Never commit `.env` files, credentials, tokens, database URLs, RabbitMQ/CloudAMQP connection strings, or private source code.
- Do not use screenshots containing personal information, customer records, payment details, or admin credentials.
- Payment integration is currently configured for **Razorpay test mode**; live payments are not implied.
- Review public demo behavior and exposed endpoints before sharing widely.

## Future Improvements

Potential directions for a future release include:

- Faster catalogue and cart responses
- Database query and index optimization
- Enhanced search, filtering, and sorting
- Expanded administration tools
- More monitoring, structured logging, and automated test coverage
- Further accessibility, mobile usability, and loading-state improvements

---

<div align="center">

**VELOCITY** · Project Showcase

<sub>Built as a full-stack e-commerce and event-driven backend project.</sub>

</div>
