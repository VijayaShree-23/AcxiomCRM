# AcxiomCRM – Submission Checklist

| Assignment requirement | Status |
|---|---|
| Authentication / logout | Implemented |
| Password hashing | Implemented with Node crypto scrypt |
| Account lockout | Implemented: 5 failures / 15 minutes |
| Admin / Manager / SalesExecutive roles | Implemented |
| Customer CRUD | Implemented |
| Lead CRUD + statuses | Implemented |
| Opportunity CRUD + amount/probability/date validation | Implemented |
| Follow-up CRUD + date validation | Implemented |
| Activity management | Implemented |
| Dashboard KPI cards | Implemented |
| Chart.js Lead Status + Opportunity Pipeline charts | Implemented |
| Search/filter | Implemented on list pages |
| User management | Implemented for Admin |
| Audit log | Implemented |
| Pipeline report | Implemented with weighted pipeline |
| REST APIs | Implemented |
| Client validation | HTML required/type constraints |
| Server validation | Implemented for all critical CRM writes |
| Anti-forgery/session protection | SameSite/HttpOnly session cookie; state-changing API requires authenticated session |

## Demo
Use the three seeded accounts in README.md. Start with Admin, then test Manager and SalesExecutive to demonstrate scope differences.
