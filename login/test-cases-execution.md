# Login / Logout Test Cases & Execution – Automation Exercise

## 1. Module Information

| Field            | Details                                    |
| ---------------- | ------------------------------------------ |
| Application      | Automation Exercise                        |
| Module           | Login / Logout                             |
| Testing Type     | Manual Testing                             |
| Test Level       | System Testing                             |
| Test Approach    | Functional, Positive, Negative, Validation |
| Test Case Status | Not Executed                               |
| Tester           | Shreya Mandrekar                           |

---

## 2. Objective

The objective of these test cases is to verify the Login and Logout functionality of the Automation Exercise application, including:

* Login page accessibility
* Valid login
* Invalid credentials
* Unregistered email handling
* Mandatory field validation
* Email format validation
* Password masking
* Successful login navigation
* Logged-in user identification
* Logout
* Re-login after logout
* Session behavior after logout
* Browser Back navigation after logout
* Email case handling
* Leading and trailing whitespace handling

All Actual Results, Status, Defect ID, and Comments will be updated after executing the test cases against the live application.

---

## 3. Preconditions

Unless otherwise specified:

1. Automation Exercise website is accessible.
2. Tester has access to a web browser.
3. A registered test account is available for valid-login scenarios.
4. Test data is prepared before execution.
5. User is logged out before starting independent login test cases unless otherwise specified.

---

# 4. Test Case Execution

## TC-LOGIN-001 – Verify Signup/Login page is accessible

**Scenario:** TS-LOGIN-01

| Field         | Details                   |
| ------------- | ------------------------- |
| Test Case ID  | TC-LOGIN-001              |
| Priority      | High                      |
| Preconditions | Application is accessible |
| Test Data     | N/A                       |

**Steps:**

1. Open Automation Exercise.
2. Navigate to the Signup/Login page.

**Expected Result:**
The Signup/Login page should be displayed successfully with the Login section available.

**Actual Result:**
Signup / Login page opened successfully and the Login section loaded correctly. The Login form was visible.

**Status:** PASS

**Defect ID:** N/A

**Comments:** Login page is accessible and loads correctly.

---

## TC-LOGIN-002 – Verify Login form contains required fields

**Scenario:** TS-LOGIN-01

| Field         | Details                         |
| ------------- | ------------------------------- |
| Test Case ID  | TC-LOGIN-002                    |
| Priority      | High                            |
| Preconditions | Signup/Login page is accessible |
| Test Data     | N/A                             |

**Steps:**

1. Open the Signup/Login page.
2. Locate the Login section.
3. Verify the Email Address field.
4. Verify the Password field.
5. Verify the Login button.

**Expected Result:**
The Login section should contain Email Address, Password, and Login button, and the controls should be available for interaction.

**Actual Result:** 
Email Address, Password, and Login button were visible. The Email Address and Password fields were clickable and allowed text input.

**Status:** PASS 

**Defect ID:** N/A

**Comments:** All required Login form elements are present and usable.

---

## TC-LOGIN-003 – Verify login with valid registered credentials

**Scenario:** TS-LOGIN-02

| Field         | Details                                     |
| ------------- | ------------------------------------------- |
| Test Case ID  | TC-LOGIN-003                                |
| Priority      | High                                        |
| Preconditions | A valid registered account exists           |
| Test Data     | Registered email and corresponding password |

**Steps:**

1. Open the Signup/Login page.
2. Enter the registered email address.
3. Enter the corresponding password.
4. Click Login.

**Expected Result:**
The user should be successfully authenticated and the login attempt should complete without an authentication error.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-LOGIN-004 – Verify login with incorrect email and correct password

**Scenario:** TS-LOGIN-03

| Field         | Details                            |
| ------------- | ---------------------------------- |
| Test Case ID  | TC-LOGIN-004                       |
| Priority      | High                               |
| Preconditions | A registered account exists        |
| Test Data     | Incorrect email + correct password |

**Steps:**

1. Open the Signup/Login page.
2. Enter an incorrect email address.
3. Enter the correct password of the registered account.
4. Click Login.

**Expected Result:**
The login attempt should be rejected and an appropriate authentication error message should be displayed.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-LOGIN-005 – Verify login with correct email and incorrect password

**Scenario:** TS-LOGIN-03

| Field         | Details                                       |
| ------------- | --------------------------------------------- |
| Test Case ID  | TC-LOGIN-005                                  |
| Priority      | High                                          |
| Preconditions | A registered account exists                   |
| Test Data     | Correct registered email + incorrect password |

**Steps:**

1. Open the Signup/Login page.
2. Enter the registered email address.
3. Enter an incorrect password.
4. Click Login.

**Expected Result:**
The login attempt should be rejected and an appropriate authentication error message should be displayed.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-LOGIN-006 – Verify login with both incorrect email and incorrect password

**Scenario:** TS-LOGIN-03

| Field         | Details                              |
| ------------- | ------------------------------------ |
| Test Case ID  | TC-LOGIN-006                         |
| Priority      | High                                 |
| Preconditions | Signup/Login page is accessible      |
| Test Data     | Incorrect email + incorrect password |

**Steps:**

1. Open the Signup/Login page.
2. Enter an incorrect email address.
3. Enter an incorrect password.
4. Click Login.

**Expected Result:**
The login attempt should be rejected and an appropriate authentication error message should be displayed.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-LOGIN-007 – Verify login with an unregistered email address

**Scenario:** TS-LOGIN-04

| Field         | Details                                    |
| ------------- | ------------------------------------------ |
| Test Case ID  | TC-LOGIN-007                               |
| Priority      | High                                       |
| Preconditions | Signup/Login page is accessible            |
| Test Data     | Valid-format unregistered email + password |

**Steps:**

1. Open the Signup/Login page.
2. Enter an email address that is not registered.
3. Enter a password.
4. Click Login.

**Expected Result:**
The application should reject the login attempt and display an appropriate authentication error message.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-LOGIN-008 – Verify mandatory validation when both Login fields are blank

**Scenario:** TS-LOGIN-05

| Field         | Details                         |
| ------------- | ------------------------------- |
| Test Case ID  | TC-LOGIN-008                    |
| Priority      | High                            |
| Preconditions | Signup/Login page is accessible |
| Test Data     | Email: Blank; Password: Blank   |

**Steps:**

1. Open the Signup/Login page.
2. Leave Email Address blank.
3. Leave Password blank.
4. Click Login.

**Expected Result:**
The application should prevent login and display mandatory-field validation for the required input.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-LOGIN-009 – Verify mandatory validation when Password is blank

**Scenario:** TS-LOGIN-05

| Field         | Details                                 |
| ------------- | --------------------------------------- |
| Test Case ID  | TC-LOGIN-009                            |
| Priority      | High                                    |
| Preconditions | Signup/Login page is accessible         |
| Test Data     | Valid registered email + blank password |

**Steps:**

1. Open the Signup/Login page.
2. Enter a valid registered email address.
3. Leave Password blank.
4. Click Login.

**Expected Result:**
The application should prevent login and display mandatory-field validation for the Password field.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-LOGIN-010 – Verify mandatory validation when Email Address is blank

**Scenario:** TS-LOGIN-05

| Field         | Details                         |
| ------------- | ------------------------------- |
| Test Case ID  | TC-LOGIN-010                    |
| Priority      | High                            |
| Preconditions | Signup/Login page is accessible |
| Test Data     | Blank email + password          |

**Steps:**

1. Open the Signup/Login page.
2. Leave Email Address blank.
3. Enter a password.
4. Click Login.

**Expected Result:**
The application should prevent login and display mandatory-field validation for the Email Address field.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-LOGIN-011 – Verify invalid email format without @ symbol

**Scenario:** TS-LOGIN-06

| Field         | Details                         |
| ------------- | ------------------------------- |
| Test Case ID  | TC-LOGIN-011                    |
| Priority      | High                            |
| Preconditions | Signup/Login page is accessible |
| Test Data     | `test`                          |

**Steps:**

1. Open the Signup/Login page.
2. Enter `test` in the Email Address field.
3. Enter a password.
4. Click Login.

**Expected Result:**
The application should reject the invalid email format and display appropriate email validation.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-LOGIN-012 – Verify incomplete email format ending with @

**Scenario:** TS-LOGIN-06

| Field         | Details                         |
| ------------- | ------------------------------- |
| Test Case ID  | TC-LOGIN-012                    |
| Priority      | High                            |
| Preconditions | Signup/Login page is accessible |
| Test Data     | `test@`                         |

**Steps:**

1. Open the Signup/Login page.
2. Enter `test@` in the Email Address field.
3. Enter a password.
4. Click Login.

**Expected Result:**
The application should reject the incomplete email format and display appropriate email validation.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-LOGIN-013 – Verify email containing a space in the middle

**Scenario:** TS-LOGIN-06

| Field         | Details                                    |
| ------------- | ------------------------------------------ |
| Test Case ID  | TC-LOGIN-013                               |
| Priority      | High                                       |
| Preconditions | Signup/Login page is accessible            |
| Test Data     | Email address containing an internal space |

**Steps:**

1. Open the Signup/Login page.
2. Enter an email address containing a space in the middle.
3. Enter a password.
4. Click Login.

**Expected Result:**
The application should reject an email address containing an invalid internal space and provide appropriate validation.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-LOGIN-014 – Verify password is masked

**Scenario:** TS-LOGIN-07

| Field         | Details                         |
| ------------- | ------------------------------- |
| Test Case ID  | TC-LOGIN-014                    |
| Priority      | Medium                          |
| Preconditions | Signup/Login page is accessible |
| Test Data     | Any test password               |

**Steps:**

1. Open the Signup/Login page.
2. Click the Password field.
3. Enter a password.
4. Observe the characters displayed in the field.

**Expected Result:**
The entered password should be displayed in masked form rather than plain text.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-LOGIN-015 – Verify successful login navigation

**Scenario:** TS-LOGIN-08

| Field         | Details                           |
| ------------- | --------------------------------- |
| Test Case ID  | TC-LOGIN-015                      |
| Priority      | High                              |
| Preconditions | A valid registered account exists |
| Test Data     | Valid registered credentials      |

**Steps:**

1. Open the Signup/Login page.
2. Enter valid registered credentials.
3. Click Login.
4. Observe the page displayed after successful login.

**Expected Result:**
After successful authentication, the application should redirect the user to the appropriate logged-in page.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-LOGIN-016 – Verify logged-in user's name is displayed

**Scenario:** TS-LOGIN-08

| Field         | Details                         |
| ------------- | ------------------------------- |
| Test Case ID  | TC-LOGIN-016                    |
| Priority      | High                            |
| Preconditions | User has successfully logged in |
| Test Data     | Valid registered account        |

**Steps:**

1. Log in using valid credentials.
2. Observe the top section of the Home page.
3. Verify the logged-in user's displayed name.

**Expected Result:**
The logged-in user's name should be displayed correctly after successful authentication.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-LOGIN-017 – Verify Logout functionality

**Scenario:** TS-LOGIN-09

| Field         | Details                 |
| ------------- | ----------------------- |
| Test Case ID  | TC-LOGIN-017            |
| Priority      | High                    |
| Preconditions | User is logged in       |
| Test Data     | Valid logged-in account |

**Steps:**

1. Log in successfully.
2. Click Logout.
3. Observe the resulting page.

**Expected Result:**
The user should be logged out successfully and redirected to the Signup/Login page or appropriate logged-out state.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-LOGIN-018 – Verify login after logout

**Scenario:** TS-LOGIN-10

| Field         | Details                          |
| ------------- | -------------------------------- |
| Test Case ID  | TC-LOGIN-018                     |
| Priority      | High                             |
| Preconditions | User has successfully logged out |
| Test Data     | Valid registered credentials     |

**Steps:**

1. Log in successfully.
2. Click Logout.
3. Navigate to the Login section.
4. Enter the same valid registered credentials.
5. Click Login.

**Expected Result:**
The user should be able to log in successfully again after logout.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-LOGIN-019 – Verify session behavior after logout using browser Back

**Scenario:** TS-LOGIN-11

| Field         | Details                 |
| ------------- | ----------------------- |
| Test Case ID  | TC-LOGIN-019            |
| Priority      | Medium                  |
| Preconditions | User is logged in       |
| Test Data     | Valid logged-in account |

**Steps:**

1. Log in successfully.
2. Click Logout.
3. Confirm that the user is in the logged-out state.
4. Click the browser Back button.
5. Observe the application state.

**Expected Result:**
Browser Back navigation after logout should not restore the authenticated session.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-LOGIN-020 – Verify login behavior with uppercase version of registered email

**Scenario:** TS-LOGIN-12

| Field         | Details                                                  |
| ------------- | -------------------------------------------------------- |
| Test Case ID  | TC-LOGIN-020                                             |
| Priority      | Medium                                                   |
| Preconditions | A registered account exists                              |
| Test Data     | Uppercase version of registered email + correct password |

**Steps:**

1. Open the Signup/Login page.
2. Enter the registered email address using uppercase letters.
3. Enter the correct password.
4. Click Login.
5. Observe the result.

**Expected Result:**
Email case handling should be consistent with the application's defined authentication rules.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-LOGIN-021 – Verify login behavior with leading and trailing spaces in email

**Scenario:** TS-LOGIN-13

| Field         | Details                                                          |
| ------------- | ---------------------------------------------------------------- |
| Test Case ID  | TC-LOGIN-021                                                     |
| Priority      | Medium                                                           |
| Preconditions | A registered account exists                                      |
| Test Data     | Registered email with leading/trailing spaces + correct password |

**Steps:**

1. Open the Signup/Login page.
2. Enter the registered email address with leading spaces.
3. Enter the correct password.
4. Click Login.
5. Repeat using the registered email address with trailing spaces.
6. Observe the result.

**Expected Result:**
The application should handle leading and trailing whitespace according to its defined input-validation and authentication rules.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

# 5. Test Execution Summary

| Metric           | Result |
| ---------------- | -----: |
| Total Test Cases |     21 |
| Passed           |      0 |
| Failed           |      0 |
| Blocked          |      0 |
| Not Executed     |     21 |
| Defects Raised   |      0 |

> The execution summary will be updated after all Login test cases have been executed.

---

# 6. Execution Status Definitions

| Status       | Meaning                                      |
| ------------ | -------------------------------------------- |
| PASS         | Actual result matches expected result        |
| FAIL         | Actual result does not match expected result |
| BLOCKED      | Test cannot be executed because of a blocker |
| NOT EXECUTED | Test has not yet been executed               |

---

# 7. Test Data

The following data categories will be used during Login testing:

| Data Type                 | Description                                       |
| ------------------------- | ------------------------------------------------- |
| Valid credentials         | Registered test account                           |
| Incorrect email           | Email address not matching the registered account |
| Incorrect password        | Incorrect password for the registered account     |
| Unregistered email        | Valid-format email not associated with an account |
| Invalid email             | `test`                                            |
| Incomplete email          | `test@`                                           |
| Email with internal space | Email containing a space within the address       |
| Uppercase email           | Registered email converted to uppercase           |
| Leading/trailing spaces   | Registered email with whitespace added            |
| Blank email               | Empty Email Address field                         |
| Blank password            | Empty Password field                              |

---

# 8. Traceability

| Test Scenario | Related Test Cases                       |
| ------------- | ---------------------------------------- |
| TS-LOGIN-01   | TC-LOGIN-001, TC-LOGIN-002               |
| TS-LOGIN-02   | TC-LOGIN-003                             |
| TS-LOGIN-03   | TC-LOGIN-004, TC-LOGIN-005, TC-LOGIN-006 |
| TS-LOGIN-04   | TC-LOGIN-007                             |
| TS-LOGIN-05   | TC-LOGIN-008, TC-LOGIN-009, TC-LOGIN-010 |
| TS-LOGIN-06   | TC-LOGIN-011, TC-LOGIN-012, TC-LOGIN-013 |
| TS-LOGIN-07   | TC-LOGIN-014                             |
| TS-LOGIN-08   | TC-LOGIN-015, TC-LOGIN-016               |
| TS-LOGIN-09   | TC-LOGIN-017                             |
| TS-LOGIN-10   | TC-LOGIN-018                             |
| TS-LOGIN-11   | TC-LOGIN-019                             |
| TS-LOGIN-12   | TC-LOGIN-020                             |
| TS-LOGIN-13   | TC-LOGIN-021                             |

---

# 9. Notes

These test cases were derived from:

* Login exploratory testing observations
* Application functionality
* Standard functional testing practices
* Positive and negative test conditions
* Input validation scenarios

Actual behavior will be recorded only after executing each test case.

Exploratory observations such as email case handling and whitespace handling will not automatically be classified as defects. A defect will be raised only when the observed behavior is confirmed to violate an applicable requirement or clearly defined expected behavior.

Any genuine reproducible defect identified during execution will be documented separately in the defect reports.
