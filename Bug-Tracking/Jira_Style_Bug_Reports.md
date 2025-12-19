# Jira Style Bug Reports
## User Management System – Web Application

This document contains sample bug reports identified during manual testing and tracked in a Jira-like workflow.

---

## BUG-001: User can register with invalid email format

Module: User Registration  
Environment: Web Application (Chrome)  

Severity: Medium  
Priority: High  
Status: New  

Steps to Reproduce:
1. Open the registration page
2. Enter an invalid email format (e.g. user@com)
3. Enter a valid password
4. Click on Register button

Expected Result:
System should display a validation message for invalid email format.

Actual Result:
User is able to register successfully with invalid email format.

Comments:
Validation check is missing on the email field.

---

## BUG-002: Inactive user is able to login

Module: User Login  
Environment: Web Application  

Severity: High  
Priority: High  
Status: New  

Steps to Reproduce:
1. Login as admin
2. Navigate to Users section
3. Change user status to Inactive
4. Logout
5. Try to login using the same user credentials

Expected Result:
Inactive user should not be allowed to login.

Actual Result:
Inactive user is able to login successfully.

Comments:
User status validation is not enforced during login.

---

## BUG-003: Error message not cleared after successful login

Module: User Login  
Environment: Web Application  

Severity: Low  
Priority: Low  
Status: New  

Steps to Reproduce:
1. Enter invalid credentials and click Login
2. Observe error message
3. Enter valid credentials and login successfully

Expected Result:
Error message should disappear after successful login.

Actual Result:
Previous error message is still visible after successful login.

Comments:
UI refresh issue observed.

---

## Bug Lifecycle Example (BUG-002)

Status Flow:
New → In Progress → Fixed → Retest → Closed

QA Action:
- Bug logged with severity and priority
- Developer fixed the issue
- QA retested the scenario
- Bug verified and closed successfully
