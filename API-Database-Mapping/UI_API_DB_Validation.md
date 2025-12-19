# UI to API to Database Validation
## User Management System – Web Application

This document describes how frontend actions were validated against backend APIs and database records during testing.

---

## Objective
The objective of this validation is to ensure that actions performed on the UI are correctly processed by APIs and reflected accurately in the database.

---

## Scenario 1: User Registration – End-to-End Validation

### UI Action
User registers using email and password on the registration page.

### API Validation
Expected API behavior:
- Registration API should be triggered on form submission
- API should return a success response for valid inputs

Validation Performed:
- API request and response verified using Postman
- Status code validated (201 – Created)

---

### Database Validation
Expected Database Behavior:
- New user record should be created in users table
- Email should be unique

SQL Query Used:
SELECT * FROM users WHERE email = 'testuser@example.com';

Result:
User record was found successfully in the database.

---

## Scenario 2: User Login – Status Validation

### UI Action
User attempts to login with valid credentials.

### API Validation
Expected API behavior:
- Login API should validate user credentials
- API should reject inactive users

Validation Performed:
- API response verified for both active and inactive users
- Correct error messages returned for invalid scenarios

---

### Database Validation
Expected Database Behavior:
- User status should be checked before allowing login

SQL Query Used:
SELECT status FROM users WHERE email = 'testuser@example.com';

Result:
Inactive users were correctly identified during backend validation.

---

## Scenario 3: Admin Deactivates User

### UI Action
Admin changes user status from Active to Inactive.

### API Validation
Expected API behavior:
- Update user status API should be triggered
- API should return success response

Validation Performed:
- API response verified using Postman
- Status code validated (200 – OK)

---

### Database Validation
Expected Database Behavior:
- User status should be updated in the database

SQL Query Used:
SELECT status FROM users WHERE email = 'testuser@example.com';

Result:
User status updated successfully in the database.

---

## Summary
UI, API, and database validations confirmed that backend processing and data consistency were maintained across core user management workflows.
