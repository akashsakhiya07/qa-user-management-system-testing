# Functional Test Cases
## User Management System – Web Application

---

## Module: User Registration

### TC_REG_01 – Verify registration with valid data
Steps:
1. Open registration page
2. Enter valid email and password
3. Click on Register button

Expected Result:
User should be registered successfully and shown a success message.

---

### TC_REG_02 – Verify registration with already registered email
Steps:
1. Open registration page
2. Enter an email that is already registered
3. Click on Register button

Expected Result:
Appropriate error message should be displayed indicating email already exists.

---

### TC_REG_03 – Verify registration with invalid email format
Steps:
1. Open registration page
2. Enter invalid email format
3. Click on Register button

Expected Result:
Validation message should be displayed for invalid email format.

---

## Module: User Login

### TC_LOGIN_01 – Verify login with valid credentials
Steps:
1. Open login page
2. Enter valid email and password
3. Click on Login button

Expected Result:
User should be logged in successfully and redirected to dashboard.

---

### TC_LOGIN_02 – Verify login with invalid credentials
Steps:
1. Open login page
2. Enter invalid email or password
3. Click on Login button

Expected Result:
Error message should be displayed for invalid login attempt.

---

## Module: User Logout

### TC_LOGOUT_01 – Verify user logout
Steps:
1. Login with valid credentials
2. Click on Logout option

Expected Result:
User should be logged out successfully and redirected to login page.

---

## Module: Admin – User Management

### TC_ADMIN_01 – Verify admin can view registered users
Steps:
1. Login as admin
2. Navigate to Users section

Expected Result:
List of registered users should be displayed.

---

### TC_ADMIN_02 – Verify admin can deactivate a user
Steps:
1. Login as admin
2. Select a user
3. Change user status to Inactive

Expected Result:
User status should be updated successfully.

---

### TC_ADMIN_03 – Verify inactive user cannot login
Steps:
1. Deactivate a user from admin panel
2. Attempt login with same user credentials

Expected Result:
User should not be able to login and proper message should be displayed.
