# gc-be-attendance-sys

A comprehensive attendance management system designed to streamline employee attendance tracking and reporting.

## Features

- [ ] Authentication
- [ ] Attendance Tracking
- [ ] Reporting
- [ ] Notifications
- [ ] User Management

API Endpoints
[ ] Authentication: Endpoints for user login and admin login, returning a JSON Web Token (JWT) for secure communication.

[ ] User Management

    GET /api/users/{id}: Fetch a single user's details.

    POST /api/users/checkin: Check a user in (takes user ID or QR code data).

    POST /api/users/checkout: Check a user out.

[ ] Admin Endpoints

    GET /api/admin/users: Fetch all user data.

    GET /api/admin/sessions: Fetch all attendance sessions.

    GET /api/admin/reports: Generate attendance reports based on query parameters.

    POST /api/admin/users: Add a new user.

    PUT /api/admin/users/{id}: Update user information.

    DELETE /api/admin/users/{id}: Delete a user.

[ ] Attendance Records

[ ] Database Schema Design: A relational database is a good choice for this project (e.g., PostgreSQL or MySQL).

    Users Table:

        id (PRIMARY KEY, UUID or integer)

        name (VARCHAR)

        email (VARCHAR, UNIQUE)

        membership_status (VARCHAR, e.g., 'active', 'inactive')

        created_at (TIMESTAMP)

        updated_at (TIMESTAMP)

    Sessions Table:

        id (PRIMARY KEY, UUID or integer)

        user_id (FOREIGN KEY to users.id)

        check_in_time (TIMESTAMP)

        check_out_time (TIMESTAMP)

        duration_minutes (INTEGER, calculated)
