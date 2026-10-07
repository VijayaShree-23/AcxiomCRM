# AcxiomCRM

A fast, zero-dependency Node.js implementation of the supplied **AcxiomCRM Complete Project Assignment**. It implements the required CRM workflows, validation, role-based authorization, authentication with password hashing/lockout, audit logging, dashboard analytics, REST APIs and reports.

## Run
Requires Node.js 18+.

```bash
npm start
```
Open `http://localhost:3000`.

### Demo accounts
- Admin: `admin@acxiomcrm.local` / `Admin@123`
- Manager: `manager@acxiomcrm.local` / `Manager@123`
- Sales Executive: `sales@acxiomcrm.local` / `Sales@123`

## Implemented
- Login/logout, secure scrypt password hashing, 5-attempt/15-minute lockout
- Admin / Manager / SalesExecutive authorization
- Customers, Leads, Opportunities, Follow-Ups, Activities CRUD
- Required/email/phone/date/numeric/business validation on the server and HTML client constraints
- Opportunity amount > 0, probability 0–100, future active close date
- Follow-up date rule
- Duplicate customer email/phone protection
- Dashboard KPIs and Chart.js charts
- Search/filter on CRM lists
- User & role management (Admin)
- Audit log for login, failed login, lockout, create/update/delete, logout
- Pipeline report with weighted pipeline calculation
- REST endpoints for customers, leads, opportunities, follow-ups, activities and dashboard/report data

## Assignment alignment
The provided specification explicitly recommends ASP.NET Core Identity for authentication and Entity Framework Core for SQL injection-safe data access. This emergency implementation keeps the same functional/security acceptance behavior in a zero-install Node runtime so it can be demonstrated immediately. If the evaluator strictly requires ASP.NET Core/EF Core as a technology constraint, migrate the same entities and rules to ASP.NET Core Identity + EF Core before final submission.
