# HCM Lite — Responsive Frontend (HTML, CSS & JavaScript)

This project is built with **plain HTML, CSS and vanilla JavaScript**. It does not use React, JSX, React DOM, or a frontend framework.

## Run locally

No npm install or external packages are required.

**Option 1 — easiest:** open `index.html` in your browser (or use the VS Code Live Server extension).

**Option 2 — local server:** with Node.js installed, run:

```bash
node server.js
```

Then open `http://localhost:5173`. `server.js` uses only built-in Node.js modules. It serves the frontend files; it is not the project backend/API.

## Included frontend modules

1. Company first-run setup and role selector (Admin / HR / Employee demo UI).
2. Organization settings: office hours, grace period, location/radius and leave quotas.
3. Employee directory: search, department filter, add/edit/remove employee and CSV export.
4. Attendance: check-in/check-out demo records, status board and CSV export.
5. Leave management: submit requests, status tabs, approve/reject actions and leave quota display.
6. Payroll Lite: basic salary, HRA 40%, medical 10%, estimated gross salary and CSV preview export.
7. Dashboard and attendance chart, KPI cards, quick actions and responsive tables.
8. AI assistant chat UI with local demo responses and policy quick reference.
9. Departments & roles, announcements, activity/audit preview, settings and dark mode.

## Important: frontend only

This is deliberately a **frontend-first prototype**. Forms and demo interactions are stored in browser `localStorage`; they are not shared between users/devices and can be cleared by resetting browser data. No backend, database, real authentication, AI provider, camera/face detection, GPS verification, secure authorization, tax calculation, payroll finalization, or real PDF payslip generation is implemented yet.

The project starts at first-run company setup and does not pre-seed employee or attendance data.

## Backend integration checklist

- Add REST API and server-side role/scope guards for every endpoint.
- Implement secure Admin first-run setup, password hashing, session lifecycle and forced temporary-password change.
- Persist company settings, departments, designations, holidays, employees, attendance, leave, payroll, payslips, announcements, audit and AI logs.
- Validate leave working days/overlaps/quotas, attendance stamps/statuses and payroll deductions/tax/proration on the server.
- Add CSV import dry-run validation, real PDF payslips, immutable payroll finalization and audit history.
- Route AI requests through backend tool calling; keep API keys server-side and enforce role scope.
- For camera attendance, validate face detection and GPS/geofence server-side; do not trust browser-only checks.
- Add tests, loading/error states for API calls and deployment environment variables.
