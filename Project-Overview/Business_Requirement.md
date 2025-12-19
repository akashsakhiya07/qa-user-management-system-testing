# Business Requirement Document (BRD)
## User Management System – Web Application

---

## Project Overview
The User Management System is a web-based application designed to allow users to register, log in, and manage their profile.
The system also provides an admin interface to view and manage registered users.

---

## Business Objective
The main objective of this application is to securely manage user information and provide a simple and reliable user onboarding process.

---

## User Roles

### 1. End User
- Can register using email and password
- Can log in with valid credentials
- Can log out of the application

### 2. Admin User
- Can view the list of registered users
- Can view user details
- Can activate or deactivate users

---

## Functional Requirements

### User Registration
- User should be able to register using a valid email and password
- Email should be unique
- Password should follow basic validation rules
- User should see a success message after registration

### User Login
- Registered users should be able to log in using valid credentials
- Error message should be displayed for invalid login attempts

### User Logout
- Logged-in users should be able to log out successfully

### Admin Panel
- Admin should be able to view all registered users
- Admin should be able to change user status (Active / Inactive)

---

## Non-Functional Requirements
- Application should be responsive
- Application should handle invalid inputs gracefully
- Error messages should be user-friendly

---

## Assumptions
- This application is a web-based system
- User authentication is email and password based

---

## Out of Scope
- Payment functionality
- Email verification
- Password recovery
