# AcxiomCRM

A professional, lightweight Customer Relationship Management (CRM) application built with Node.js and a zero-dependency backend. The project demonstrates CRM workflows, authentication, role-based access control, validation, audit logging, analytics, reporting, and REST APIs.

> **Portfolio / interview project:** Demonstrates full-stack application development, backend API design, authentication, authorization, validation, and practical business workflows.

## ✨ Features

### Authentication & Security
- Secure password hashing using Node.js crypto.scrypt
- Login and logout
- Session-based authentication with HttpOnly and SameSite cookies
- Account lockout after 5 failed login attempts for 15 minutes
- Role-based access control
- Audit logging for authentication and CRM operations

### CRM Management
- Customer, lead, opportunity, follow-up, and activity management
- Search and filtering
- Role-specific record visibility

### Dashboard & Reporting
- CRM KPI dashboard
- Lead-status and opportunity-pipeline charts
- Weighted pipeline calculation
- Pipeline report by opportunity stage

### Validation
- Required-field, email, phone, date, and numeric validation
- Duplicate customer email/phone protection
- Opportunity amount and probability validation
- Expected-close-date and follow-up date validation
- Server-side validation for critical write operations

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Backend | Node.js |
| HTTP/API | Node.js native http module |
| Frontend | HTML5, CSS3, JavaScript |
| UI | Bootstrap 5 |
| Charts | Chart.js |
| Authentication | Session-based authentication |
| Password hashing | Node.js crypto.scrypt |
| Data storage | JSON file for local/demo use |
| Dependencies | Zero external npm runtime dependencies |

## 🏗️ Architecture

```text
Browser
   │
   │ HTTP / REST API
   ▼
Node.js HTTP Server
   │
   ├── Authentication & Sessions
   ├── Role-Based Authorization
   ├── Validation
   ├── CRM CRUD Operations
   ├── Audit Logging
   └── Dashboard / Reports
   │
   ▼
data/db.json
```

The frontend is served directly by the Node.js server. CRM operations are exposed through REST-style /api/... endpoints.

## 📁 Project Structure

```text
AcxiomCRM/
├── public/
│   └── index.html
├── data/
│   └── db.json           # Local runtime data (ignored by Git)
├── server.js             # HTTP server, APIs, auth, validation
├── seed.js               # Optional demo-data seeding
├── package.json
├── .gitignore
└── README.md
```

## 🚀 Getting Started

### Prerequisites
- Node.js 18 or later
- VS Code or another code editor
- Modern web browser

### Installation
```bash
git clone https://github.com/VijayaShree-23/AcxiomCRM.git
cd AcxiomCRM
```

No database server or external npm packages are required.

### Run
```bash
npm start
```

Open http://localhost:3000 in your browser.

### Demo Accounts
These accounts are intended **only for local demonstration**:

| Role | Email | Password |
|---|---|---|
| Admin | admin@acxiomcrm.local | Admin@123 |
| Manager | manager@acxiomcrm.local | Manager@123 |
| Sales Executive | sales@acxiomcrm.local | Sales@123 |

Start with Admin, then test Manager and Sales Executive to demonstrate authorization differences.

## 🔌 API Overview

| Endpoint | Purpose |
|---|---|
| POST /api/auth/login | Authenticate a user |
| POST /api/auth/logout | End the current session |
| GET /api/me | Get the current user |
| GET /api/dashboard | Dashboard KPIs and chart data |
| GET /api/customers | List customers |
| GET /api/leads | List leads |
| GET /api/opportunities | List opportunities |
| GET /api/followups | List follow-ups |
| GET /api/activities | List activities |
| GET /api/reports/pipeline | Pipeline report |
| GET /api/users | User management data |
| GET /api/audit | Audit log |

The CRM resources also support authenticated create, update, and delete operations where permitted by the user's role.

## 🔐 Security Notes
This project is designed for **local demonstration and portfolio use**, not production deployment.

Current security features include password hashing, HttpOnly/SameSite cookies, authentication checks, role-based authorization, server-side validation, login lockout, and audit logging.

For production use, replace the JSON data store with a proper database and introduce HTTPS, environment-based secrets, stronger session management, deployment-appropriate CSRF protection, rate limiting, centralized logging, automated tests, and a production-grade authentication/data-access layer.

## 💡 Future Improvements
- PostgreSQL or MySQL persistence
- Modular Express, Spring Boot, or ASP.NET Core backend architecture
- Dedicated frontend components
- Environment-based configuration
- Automated unit and integration tests
- Docker deployment and CI/CD
- Pagination and server-side filtering
- Advanced analytics and exportable reports
- Email and notification integration

## 🎯 Interview Talking Points
1. **REST APIs:** authenticated CRUD endpoints for major CRM entities.
2. **Authentication:** password hashing and session-based login.
3. **Authorization:** Admin, Manager, and Sales Executive roles with different access scopes.
4. **Backend validation:** business rules enforced on the server, not only in the UI.
5. **Security awareness:** password hashing, lockout, HttpOnly/SameSite cookies, and audit logging.
6. **Business logic:** opportunity probability, weighted pipeline, follow-up rules, duplicate prevention, and role-based visibility.
7. **Frontend integration:** dashboard connected to REST APIs with Chart.js analytics.

## 📌 Project Status
The current version is a **working local/demo CRM implementation** focused on demonstrating the requested business workflows with minimal setup.

---

**Author:** Avvaru Vijaya Shree  
**Repository:** https://github.com/VijayaShree-23/AcxiomCRM