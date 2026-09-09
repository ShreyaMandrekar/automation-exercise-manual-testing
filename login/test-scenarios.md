# Login / Logout – Test Scenarios

## 1. Module Overview

The Login module allows registered users to authenticate using their email address and password.

The module includes:

* Login using valid credentials
* Validation of invalid credentials
* Email format validation
* Mandatory field validation
* Password masking
* Successful login navigation
* Logged-in user identification
* Logout functionality
* Re-login after logout
* Session behavior after logout
* Handling of different email input formats

Testing will be performed on the **Automation Exercise** web application.

---

## 2. Test Scenario Summary

| Scenario ID | Test Scenario                                                      | Priority |
| ----------- | ------------------------------------------------------------------ | -------- |
| TS-LOGIN-01 | Verify Login page accessibility and UI elements                    | High     |
| TS-LOGIN-02 | Verify login using valid registered credentials                    | High     |
| TS-LOGIN-03 | Verify login with invalid credentials                              | High     |
| TS-LOGIN-04 | Verify login with an unregistered email address                    | High     |
| TS-LOGIN-05 | Verify mandatory field validation                                  | High     |
| TS-LOGIN-06 | Verify invalid email format validation                             | High     |
| TS-LOGIN-07 | Verify password field masking                                      | Medium   |
| TS-LOGIN-08 | Verify successful login navigation and logged-in user display      | High     |
| TS-LOGIN-09 | Verify Logout functionality                                        | High     |
| TS-LOGIN-10 | Verify login after logout                                          | High     |
| TS-LOGIN-11 | Verify session behavior after logout using browser Back navigation | Medium   |
| TS-LOGIN-12 | Verify email case handling during login                            | Medium   |
| TS-LOGIN-13 | Verify handling of leading and trailing spaces in email            | Medium   |

---

# 3. Detailed Test Scenarios

## TS-LOGIN-01 – Verify Login Page Accessibility and UI Elements

**Objective:**
Verify that the Login section is accessible and contains the required login elements.

**Precondition:**
User is not logged in.

**Test Conditions:**

* Navigate to the Signup/Login page.
* Verify the Login section is displayed.
* Verify Email Address field is available.
* Verify Password field is available.
* Verify Login button is available.

**Expected Result:**
The Login section should be accessible and all required login elements should be displayed and usable.

---

## TS-LOGIN-02 – Verify Login Using Valid Registered Credentials

**Objective:**
Verify that a registered user can log in using valid credentials.

**Precondition:**
A valid registered user account is available.

**Test Conditions:**

* Enter the registered email address.
* Enter the corresponding correct password.
* Click Login.

**Expected Result:**
The user should be successfully authenticated without displaying an authentication error.

---

## TS-LOGIN-03 – Verify Login With Invalid Credentials

**Objective:**
Verify that login is rejected when incorrect credentials are provided.

**Test Conditions:**

* Enter an incorrect email address with an incorrect password.
* Enter a correct registered email address with an incorrect password.
* Attempt to log in.

**Expected Result:**
The application should reject invalid credentials and display an appropriate authentication error message.

---

## TS-LOGIN-04 – Verify Login With an Unregistered Email Address

**Objective:**
Verify that a user cannot log in using an email address that is not registered.

**Test Conditions:**

* Enter an unregistered email address in valid email format.
* Enter a password.
* Click Login.

**Expected Result:**
The application should reject the login attempt and display an appropriate authentication error message.

---

## TS-LOGIN-05 – Verify Mandatory Field Validation

**Objective:**
Verify that Email Address and Password are mandatory fields.

**Test Conditions:**

### Condition 1 – Both fields blank

* Leave Email Address blank.
* Leave Password blank.
* Click Login.

### Condition 2 – Password blank

* Enter a valid registered email address.
* Leave Password blank.
* Click Login.

### Condition 3 – Email blank

* Leave Email Address blank.
* Enter a password.
* Click Login.

**Expected Result:**
The application should prevent submission when a required field is blank and display appropriate mandatory-field validation.

---

## TS-LOGIN-06 – Verify Invalid Email Format Validation

**Objective:**
Verify that invalid email formats are handled correctly by the Login form.

**Test Conditions:**
Test the Login form with invalid email formats such as:

* `test`
* `test@`
* Email containing a space in the middle
* Spaces-only input

**Expected Result:**
The application should prevent invalid email input from being submitted as a valid email address and should display appropriate validation feedback.

---

## TS-LOGIN-07 – Verify Password Field Masking

**Objective:**
Verify that the password entered by the user is not displayed as plain text.

**Test Conditions:**

* Enter a password in the Password field.
* Observe the characters displayed in the field.
* Check whether a password visibility/show-password control is available.

**Expected Result:**
The entered password should be masked and should not be directly visible as plain text.

---

## TS-LOGIN-08 – Verify Successful Login Navigation and Logged-In User Display

**Objective:**
Verify the application behavior after successful authentication.

**Precondition:**
A valid registered account is available.

**Test Conditions:**

* Log in using valid credentials.
* Observe the page after successful authentication.
* Verify the displayed user information.

**Expected Result:**
After successful login:

* The user should be redirected to the appropriate authenticated page.
* The logged-in user's name should be displayed.
* The application should indicate that the user is logged in.

---

## TS-LOGIN-09 – Verify Logout Functionality

**Objective:**
Verify that a logged-in user can successfully log out.

**Precondition:**
User is logged in.

**Test Conditions:**

* Click the Logout option.

**Expected Result:**
The user should be logged out successfully and should be redirected to the Signup/Login page or appropriate logged-out state.

---

## TS-LOGIN-10 – Verify Login After Logout

**Objective:**
Verify that a user can log in again after successfully logging out.

**Precondition:**
User has previously logged in and then logged out.

**Test Conditions:**

* Navigate to the Login section.
* Enter valid registered credentials.
* Click Login.

**Expected Result:**
The user should be successfully authenticated again and redirected to the appropriate logged-in page.

---

## TS-LOGIN-11 – Verify Session Behavior After Logout Using Browser Back Navigation

**Objective:**
Verify that logging out does not restore the authenticated session through browser navigation.

**Precondition:**
User is logged in.

**Test Conditions:**

* Log out from the application.
* After being redirected to the logged-out state, use the browser Back button.
* Observe the application state.

**Expected Result:**
The application should not restore the authenticated session merely through browser Back navigation after logout.

---

## TS-LOGIN-12 – Verify Email Case Handling During Login

**Objective:**
Verify how the application handles email addresses with different letter casing.

**Precondition:**
A registered user account is available.

**Test Conditions:**

* Use the registered email address with different letter casing.
* Enter the correct password.
* Attempt to log in.

**Expected Result:**
Email case handling should be consistent with the application's defined authentication rules.

**Note:**
The behavior observed during exploratory testing will be recorded during formal execution. It should not automatically be classified as a defect unless it conflicts with a documented requirement.

---

## TS-LOGIN-13 – Verify Handling of Leading and Trailing Spaces in Email

**Objective:**
Verify how the application handles leading and trailing whitespace in the email address.

**Precondition:**
A registered user account is available.

**Test Conditions:**

* Enter the registered email address with leading spaces.
* Enter the registered email address with trailing spaces.
* Enter the correct password.
* Attempt to log in.

**Expected Result:**
Whitespace handling should be consistent with the application's defined input-validation and authentication rules.

**Note:**
Observed behavior will be documented during formal execution. Acceptance or rejection of whitespace should not be considered a defect without a defined requirement.

---

# 4. Test Data

The following test data categories will be used during Login testing:

| Data Type                 | Example / Description                             |
| ------------------------- | ------------------------------------------------- |
| Valid credentials         | Registered test account                           |
| Invalid email             | Incorrect email with valid format                 |
| Invalid password          | Incorrect password for registered account         |
| Unregistered email        | Valid-format email not associated with an account |
| Invalid email format      | `test`, `test@`                                   |
| Email with internal space | Email containing a space within the address       |
| Spaces-only input         | Email field containing only spaces                |
| Uppercase email           | Registered email converted to uppercase           |
| Leading/trailing spaces   | Registered email with whitespace added            |

---

# 5. Scope for Test Execution

The following areas will be covered during formal Login testing:

* Login page UI
* Valid login
* Invalid credentials
* Unregistered users
* Mandatory field validation
* Email format validation
* Password masking
* Successful login navigation
* Logged-in user identification
* Logout
* Re-login
* Session behavior after logout
* Email case handling
* Email whitespace handling

Formal test cases will be created from these scenarios and executed against the live application.

Any reproducible deviation from expected behavior will be documented separately as a defect.

