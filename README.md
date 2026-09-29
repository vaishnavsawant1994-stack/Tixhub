# Tixhub

## Project overview

Tixhub is a full-stack booking application with account authentication, QR-code ticket workflows, analytics, and real-time client/server communication.

## What it contains

- React 19 and Vite frontend
- Express 5 backend
- MySQL database connectivity
- JWT authentication and bcrypt password hashing
- QR-code generation and scanning
- Socket.IO real-time updates
- Axios API client, charts, and routed application screens
- Project-management material

## Current status

The frontend and backend foundations are present, but the exact event/venue/booking lifecycle, user roles, database migrations, API contract, and test coverage are not documented at the repository root.

## Security and repository hygiene

The public repository tree currently includes `backend/.env`, dependency directories, cache/build material, and log files. Do not place real credentials in tracked environment files. Any credential that has ever been committed publicly should be treated as exposed and rotated before further deployment.

A safe configuration pattern is:

```env
DATABASE_URL=<your-database-url>
JWT_SECRET=<generate-a-long-random-secret>
```

## Recommended next work

1. Rotate any exposed credentials and remove tracked environment/generated files, including their sensitive Git history where required.
2. Document booking, payment, QR validation, cancellation/refund, and real-time update flows.
3. Add database setup/migrations, environment templates, authorization tests, and end-to-end booking verification.
