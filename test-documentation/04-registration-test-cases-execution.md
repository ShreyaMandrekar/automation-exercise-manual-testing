# Registration Test Cases & Execution – Automation Exercise

## 1. Module Information

| Field | Details |
|---|---|
| Application | Automation Exercise |
| Module | Registration / Signup |
| Testing Type | Manual Testing |
| Test Level | System Testing |
| Test Approach | Functional, Positive, Negative, Validation |
| Test Case Status | Not Executed |
| Tester | Shreya Mandrekar |

---

## 2. Objective

The objective of these test cases is to verify the registration functionality of the Automation Exercise application, including:

- Signup page accessibility
- Input field validation
- Mandatory and optional fields
- Email validation
- Password behavior
- Date of birth selection
- Personal information
- Address information
- Country, State and City fields
- Zipcode and Mobile Number validation
- Newsletter and Special Offers preferences
- Account creation
- Account creation confirmation
- Logged-in user state
- Logout
- Account deletion

All Actual Results and Status values will be updated after executing the test cases against the live application.

---

## 3. Preconditions

Unless otherwise specified:

1. Automation Exercise website is accessible.
2. Tester has access to a web browser.
3. A unique email address is available for registration test cases requiring a new account.
4. Test data is prepared before execution.

---

## 4. Test Case Execution

### TC-REG-001 – Verify Signup/Login page is accessible

**Scenario:** TS-REG-01

| Field | Details |
|---|---|
| Test Case ID | TC-REG-001 |
| Priority | High |
| Preconditions | Application is accessible |
| Test Data | N/A |

**Steps:**
1. Open Automation Exercise.
2. Navigate to the Signup/Login page.

**Expected Result:**  
Signup/Login page should be displayed with the Login and New User Signup sections.

**Actual Result:**  
Signup/Login page opened successfully. The Login to your account section displayed Email Address, Password, and Login button. The New User Signup section displayed Name, Email Address, and Signup button.

**Status:**
PASS

**Defect ID:** 
N/A

**Comments:**  
Signup/Login page was accessible and both Login and New User Signup sections were displayed as expected.

---

### TC-REG-002 – Verify registration with valid user details

**Scenario:** TS-REG-02

| Field | Details |
|---|---|
| Test Case ID | TC-REG-002 |
| Priority | High |
| Test Data | Valid registration data |

**Steps:**
1. Open Signup/Login.
2. Enter a valid Name.
3. Enter a unique valid Email Address.
4. Click Signup.
5. Fill all required account information with valid data.
6. Click Create Account.

**Expected Result:**  
The account should be created successfully.

**Actual Result:**  
Registration was completed successfully using valid user details. The Account Created confirmation page was displayed after clicking Create Account.

**Status:** PASS

**Defect ID:** N/A

**Comments:**  
A new account was successfully created with valid registration data. Account Created confirmation was displayed as expected.

---

### TC-REG-003 – Verify mandatory field validation on initial signup

**Scenario:** TS-REG-03

**Steps:**
1. Open Signup/Login.
2. Leave Name blank.
3. Enter a valid Email Address.
4. Click Signup.
5. Repeat with Email Address blank.
6. Repeat with both fields blank.

**Expected Result:**  
Appropriate validation should prevent submission when required fields are blank.

**Actual Result:**  
Name blank: A validation pop-up displayed "Please fill out this field." on the Name field.

Email blank: A validation pop-up displayed "Please fill out this field." on the Email Address field.

Both Name and Email blank: A validation pop-up displayed "Please fill out this field." on the Name field first.

**Status:** PASS

**Defect ID:** N/A

**Comments:**  
Mandatory field validation worked as expected. When both fields were blank, validation was triggered on the Name field first.

---

### TC-REG-004 – Verify invalid email format validation

**Scenario:** TS-REG-04

**Test Data:**

- `test`
- `test@`
- `test.com`
- `test@@example.com`

**Steps:**
1. Open Signup/Login.
2. Enter a valid Name.
3. Enter an invalid email format.
4. Click Signup.
5. Repeat for each invalid email value.

**Expected Result:**  
Invalid email formats should be rejected and appropriate validation should be displayed.

**Actual Result:**  
Test 1 - "test": A validation message displayed, "Please include an @ in the email address. 'test' is missing an @."

Test 2 - "test@": A validation message displayed, "Please enter a part following @. 'test@' is incomplete."

Test 3 - "test.com": A validation message displayed, "Please include an @ in the email address. 'test.com' is missing an @."

Test 4 - "test@@example.com": A validation message displayed, "A part following @ should not contain the symbol @."

**Status:** PASS

**Defect ID:** N/A

**Comments:**  
All four invalid email formats were rejected by the application's email validation. No defect was observed.

---

### TC-REG-005 – Verify duplicate email registration

**Scenario:** TS-REG-05

**Test Data:**  
An email address belonging to an already registered account.

**Steps:**
1. Open Signup/Login.
2. Enter a valid Name.
3. Enter an already registered email address.
4. Click Signup.

**Expected Result:**  
The application should prevent registration using an already registered email address and display an appropriate message.

**Actual Result:**  
A red validation message was displayed below the Email Address field stating "Email Address already exist!"

**Status:** PASS

**Defect ID:** N/A

**Comments:**  
The application prevented registration using an already registered email address and displayed an appropriate validation message. No defect was observed.

---

### TC-REG-006 – Verify Name field validation

**Scenario:** TS-REG-03

**Steps:**
1. Open Signup/Login.
2. Leave the Name field blank.
3. Enter a valid email.
4. Click Signup.
5. Test the Name field with valid alphabetic input.
6. Test with numeric and special-character input where applicable.

**Expected Result:**  
Name should be accepted according to the application's validation rules. Blank input should not be accepted if the field is mandatory.

**Actual Result:**  
Blank Name: A validation pop-up displayed "Please fill out this field."

Valid Name: The application accepted the valid Name and proceeded to the account information page.

Numeric Name: The application accepted numeric input in the Name field and proceeded to the account information page.

Special Characters: The application accepted special-character input in the Name field and proceeded to the account information page.

**Status:** PASS

**Defect ID:** N/A

**Comments:**  
Mandatory Name validation worked as expected. Numeric and special-character inputs were accepted during testing. This behavior is recorded as an observation and is not classified as a defect because no explicit requirement restricting Name input to alphabetic characters was established.

---

### TC-REG-007 – Verify Email Address field validation

**Scenario:** TS-REG-04

**Steps:**
1. Open Signup/Login.
2. Enter a valid Name.
3. Test the Email Address field with:
   - valid email
   - blank value
   - invalid format
4. Click Signup for each applicable test.

**Expected Result:**  
The application should accept valid email formats and reject blank/invalid email values where validation is required.

**Actual Result:**  
Valid email: The application accepted the valid email address and proceeded to the account information page.

Blank email: A validation pop-up displayed "Please fill out this field."

Invalid email "QA@": A validation pop-up displayed "Please enter a part following @. 'QA@' is incomplete."

**Status:** PASS

**Defect ID:** N/A

**Comments:**  
The Email Address field accepted valid email input and correctly prevented blank and invalid email input. No defect was observed.

---

### TC-REG-008 – Verify Title field behavior

**Scenario:** TS-REG-10

**Steps:**
1. Complete the initial signup.
2. On the account information page, observe the Title options.
3. Select Mr.
4. Select Mrs.
5. Test account creation without selecting a Title, if permitted.

**Expected Result:**  
The Title options should be displayed correctly and the application should handle selection according to its validation rules.

**Actual Result:**  
NOT EXECUTED

**Status:** NOT EXECUTED

**Defect ID:** N/A

**Comments:**  
To be updated during execution.

---

### TC-REG-009 – Verify Password field behavior and validation

**Scenario:** TS-REG-06

**Steps:**
1. Navigate to the account creation form.
2. Leave Password blank and attempt submission.
3. Enter a valid password.
4. Enter a short password such as `123`.
5. Observe whether the password is masked.

**Expected Result:**  
Password should be treated as a password field. Blank password should be rejected if mandatory. Any password length/format restrictions enforced by the application should work correctly.

**Actual Result:**  
NOT EXECUTED

**Status:** NOT EXECUTED

**Defect ID:** N/A

**Comments:**  
Specific password rules will be documented based on actual application behavior.

---

### TC-REG-010 – Verify Date of Birth field behavior

**Scenario:** TS-REG-07

**Steps:**
1. Navigate to the account creation form.
2. Open the Day dropdown.
3. Open the Month dropdown.
4. Open the Year dropdown.
5. Select a valid date.
6. Test boundary/alternative values where applicable.
7. Test account creation without selecting DOB.

**Expected Result:**  
DOB controls should display valid selectable values and handle date selection according to the application's validation rules.

**Actual Result:**  
NOT EXECUTED

**Status:** NOT EXECUTED

**Defect ID:** N/A

**Comments:**  
Boundary behavior will be recorded during execution.

---

### TC-REG-011 – Verify Newsletter checkbox behavior

**Scenario:** TS-REG-08

**Steps:**
1. Navigate to the account creation form.
2. Observe the default state of Newsletter.
3. Register with Newsletter unchecked.
4. Repeat with Newsletter checked.

**Expected Result:**  
Newsletter should be optional and the application should allow account creation with either selected or unselected state.

**Actual Result:**  
NOT EXECUTED

**Status:** NOT EXECUTED

**Defect ID:** N/A

**Comments:**  
To be updated during execution.

---

### TC-REG-012 – Verify Special Offers checkbox behavior

**Scenario:** TS-REG-09

**Steps:**
1. Navigate to the account creation form.
2. Observe the default state of Special Offers.
3. Register with Special Offers unchecked.
4. Repeat with Special Offers checked.

**Expected Result:**  
Special Offers should be optional and the application should allow account creation with either selected or unselected state.

**Actual Result:**  
NOT EXECUTED

**Status:** NOT EXECUTED

**Defect ID:** N/A

**Comments:**  
To be updated during execution.

---

### TC-REG-013 – Verify First Name field validation

**Scenario:** TS-REG-10

**Steps:**
1. Navigate to the account creation form.
2. Enter a valid First Name.
3. Leave First Name blank and attempt submission.
4. Test with different valid input values.

**Expected Result:**  
First Name should accept valid input and should not allow blank submission if the field is mandatory.

**Actual Result:**  
NOT EXECUTED

**Status:** NOT EXECUTED

**Defect ID:** N/A

**Comments:**  
To be updated during execution.

---

### TC-REG-014 – Verify Last Name field validation

**Scenario:** TS-REG-10

**Steps:**
1. Navigate to the account creation form.
2. Enter a valid Last Name.
3. Leave Last Name blank and attempt submission.
4. Test with different valid input values.

**Expected Result:**  
Last Name should accept valid input and should not allow blank submission if the field is mandatory.

**Actual Result:**  
NOT EXECUTED

**Status:** NOT EXECUTED

**Defect ID:** N/A

**Comments:**  
To be updated during execution.

---

### TC-REG-015 – Verify Company field behavior

**Scenario:** TS-REG-10

**Steps:**
1. Navigate to the account creation form.
2. Enter valid Company information.
3. Leave Company blank.
4. Attempt account creation with and without Company information.

**Expected Result:**  
The application should handle the Company field according to its defined/observed optional behavior.

**Actual Result:**  
NOT EXECUTED

**Status:** NOT EXECUTED

**Defect ID:** N/A

**Comments:**  
To be updated during execution.

---

### TC-REG-016 – Verify Address field validation

**Scenario:** TS-REG-10

**Steps:**
1. Navigate to the account creation form.
2. Enter a valid Address.
3. Leave Address blank and attempt submission.
4. Test with different valid address formats.

**Expected Result:**  
Address should accept valid input and should not allow blank submission if the field is mandatory.

**Actual Result:**  
NOT EXECUTED

**Status:** NOT EXECUTED

**Defect ID:** N/A

**Comments:**  
To be updated during execution.

---

### TC-REG-017 – Verify Address 2 field behavior

**Scenario:** TS-REG-10

**Steps:**
1. Navigate to the account creation form.
2. Leave Address 2 blank.
3. Enter valid Address 2 information.
4. Attempt account creation in both cases.

**Expected Result:**  
The application should allow Address 2 to remain blank if it is optional and should accept valid input when provided.

**Actual Result:**  
NOT EXECUTED

**Status:** NOT EXECUTED

**Defect ID:** N/A

**Comments:**  
To be updated during execution.

---

### TC-REG-018 – Verify Country dropdown

**Scenario:** TS-REG-10

**Steps:**
1. Navigate to the account creation form.
2. Open the Country dropdown.
3. Verify the available options.
4. Select different available countries.
5. Continue registration.

**Expected Result:**  
Country dropdown should open correctly, display valid options, and allow selection.

**Actual Result:**  
NOT EXECUTED

**Status:** NOT EXECUTED

**Defect ID:** N/A

**Comments:**  
Actual available options will be recorded during execution.

---

### TC-REG-019 – Verify State field validation

**Scenario:** TS-REG-10

**Steps:**
1. Navigate to the account creation form.
2. Enter a valid State.
3. Leave State blank and attempt submission.
4. Test with different valid values.

**Expected Result:**  
State should accept valid input and should not allow blank submission if mandatory.

**Actual Result:**  
NOT EXECUTED

**Status:** NOT EXECUTED

**Defect ID:** N/A

**Comments:**  
To be updated during execution.

---

### TC-REG-020 – Verify City field validation

**Scenario:** TS-REG-10

**Steps:**
1. Navigate to the account creation form.
2. Enter a valid City.
3. Leave City blank and attempt submission.
4. Test with different valid values.

**Expected Result:**  
City should accept valid input and should not allow blank submission if mandatory.

**Actual Result:**  
NOT EXECUTED

**Status:** NOT EXECUTED

**Defect ID:** N/A

**Comments:**  
To be updated during execution.

---

### TC-REG-021 – Verify Zipcode field validation

**Scenario:** TS-REG-10

**Steps:**
1. Navigate to the account creation form.
2. Enter a valid Zipcode.
3. Leave Zipcode blank and attempt submission.
4. Test different numeric and character inputs.
5. Submit the form.

**Expected Result:**  
Zipcode should accept valid input according to the application's validation rules and should not allow blank submission if mandatory.

**Actual Result:**  
NOT EXECUTED

**Status:** NOT EXECUTED

**Defect ID:** N/A

**Comments:**  
Character acceptance observed during exploration will be formally verified during execution.

---

### TC-REG-022 – Verify Mobile Number field validation

**Scenario:** TS-REG-10

**Steps:**
1. Navigate to the account creation form.
2. Enter a valid mobile number.
3. Leave Mobile Number blank and attempt submission.
4. Test numeric and character inputs.
5. Submit the form.

**Expected Result:**  
Mobile Number should accept valid input according to the application's validation rules and should not allow blank submission if mandatory.

**Actual Result:**  
NOT EXECUTED

**Status:** NOT EXECUTED

**Defect ID:** N/A

**Comments:**  
Character acceptance observed during exploration will be formally verified during execution.

---

### TC-REG-023 – Verify registration with incomplete mandatory information

**Scenario:** TS-REG-03

**Steps:**
1. Open the account creation form.
2. Leave one or more mandatory fields blank.
3. Enter valid information in the remaining fields.
4. Click Create Account.

**Expected Result:**  
Account creation should be prevented and appropriate validation should be displayed for the missing mandatory fields.

**Actual Result:**  
NOT EXECUTED

**Status:** NOT EXECUTED

**Defect ID:** N/A

**Comments:**  
To be updated during execution.

---

### TC-REG-024 – Verify successful account creation

**Scenario:** TS-REG-11

**Steps:**
1. Enter valid values in all required registration fields.
2. Click Create Account.

**Expected Result:**  
The account should be created successfully and the Account Created confirmation page should be displayed.

**Actual Result:**  
NOT EXECUTED

**Status:** NOT EXECUTED

**Defect ID:** N/A

**Comments:**  
To be updated during execution.

---

### TC-REG-025 – Verify Account Created confirmation message

**Scenario:** TS-REG-11

**Steps:**
1. Complete registration with valid information.
2. Observe the confirmation page.

**Expected Result:**  
A successful account creation message should be displayed.

**Actual Result:**  
NOT EXECUTED

**Status:** NOT EXECUTED

**Defect ID:** N/A

**Comments:**  
To be updated during execution.

---

### TC-REG-026 – Verify Continue button after account creation

**Scenario:** TS-REG-12

**Steps:**
1. Successfully create an account.
2. Click Continue.

**Expected Result:**  
The user should be redirected to the Home page.

**Actual Result:**  
NOT EXECUTED

**Status:** NOT EXECUTED

**Defect ID:** N/A

**Comments:**  
To be updated during execution.

---

### TC-REG-027 – Verify newly registered user is displayed

**Scenario:** TS-REG-13

**Steps:**
1. Successfully create an account.
2. Click Continue.
3. Observe the Home page.

**Expected Result:**  
The newly registered user's name should be displayed as a logged-in user.

**Actual Result:**  
NOT EXECUTED

**Status:** NOT EXECUTED

**Defect ID:** N/A

**Comments:**  
To be updated during execution.

---

### TC-REG-028 – Verify Logout functionality

**Scenario:** TS-REG-14

**Steps:**
1. Log in or remain logged in after successful registration.
2. Click Logout.

**Expected Result:**  
The user should be logged out and redirected to the Signup/Login page.

**Actual Result:**  
NOT EXECUTED

**Status:** NOT EXECUTED

**Defect ID:** N/A

**Comments:**  
To be updated during execution.

---

### TC-REG-029 – Verify Delete Account functionality

**Scenario:** TS-REG-15

**Steps:**
1. Log in using a valid account.
2. Click Delete Account.
3. Observe the resulting page.

**Expected Result:**  
The account should be deleted and an appropriate account deletion confirmation should be displayed.

**Actual Result:**  
NOT EXECUTED

**Status:** NOT EXECUTED

**Defect ID:** N/A

**Comments:**  
To be updated during execution.

---

### TC-REG-030 – Verify account deletion confirmation and Continue

**Scenario:** TS-REG-16

**Steps:**
1. Delete the account.
2. Verify the account deletion confirmation message.
3. Click Continue.

**Expected Result:**  
The account deletion confirmation should be displayed and Continue should redirect the user to the Home page.

**Actual Result:**  
NOT EXECUTED

**Status:** NOT EXECUTED

**Defect ID:** N/A

**Comments:**  
To be updated during execution.

---

## 5. Test Execution Summary

| Metric | Result |
|---|---:|
| Total Test Cases | 30 |
| Passed | 0 |
| Failed | 0 |
| Blocked | 0 |
| Not Executed | 30 |
| Defects Raised | 0 |

> This summary will be updated after test execution.

---

## 6. Execution Status Definitions

| Status | Meaning |
|---|---|
| PASS | Actual result matches expected result |
| FAIL | Actual result does not match expected result |
| BLOCKED | Test cannot be executed because of a blocker |
| NOT EXECUTED | Test has not yet been executed |

---

## 7. Defect Handling

A defect will be reported only when:

1. The test case is actually executed.
2. The observed behavior differs from the expected behavior.
3. The issue can be reproduced or sufficiently evidenced.
4. The issue is documented with appropriate details.

Defect IDs will be added to the relevant test cases after defects are genuinely identified.

Detailed defect reports will be maintained in:

`05-defect-reports.md`

---

## 8. Retesting and Regression

After a genuine defect is fixed:

- The failed test case will be executed again for retesting.
- The result will be updated in this document.
- Related functionality will be tested for regression.
- Retesting and regression details will be maintained in:

`06-retesting-regression.md`

---

## 9. Test Data

The following data was used during exploratory testing and may be reused where appropriate. New unique email addresses should be generated when a fresh registration is required.

| Field | Exploration Data |
|---|---|
| Title | Mr. |
| Name | QA Tester |
| Email | Test@123.com |
| Password | 123 |
| Day | 7 |
| Month | September |
| Year | 2009 |
| Newsletter | Selected |
| Special Offers | Selected |
| First Name | QA |
| Last Name | Tester |
| Company | Software |
| Address | Thane |
| Address 2 | Thane 2 |
| Country | India |
| State | Maharashtra |
| City | Kalyan |
| Zipcode | 561302 |
| Mobile Number | 857-345-2345 |

---

## 10. Execution Environment

The following information will be recorded during actual execution:

| Field | Details |
|---|---|
| Application URL | https://www.automationexercise.com/ |
| Browser | To be recorded |
| Browser Version | To be recorded |
| Operating System | To be recorded |
| Execution Date | To be recorded |

---

## 11. Traceability

| Test Scenario | Related Test Cases |
|---|---|
| TS-REG-01 | TC-REG-001 |
| TS-REG-02 | TC-REG-002 |
| TS-REG-03 | TC-REG-003, TC-REG-006, TC-REG-023 |
| TS-REG-04 | TC-REG-004, TC-REG-007 |
| TS-REG-05 | TC-REG-005 |
| TS-REG-06 | TC-REG-009 |
| TS-REG-07 | TC-REG-010 |
| TS-REG-08 | TC-REG-011 |
| TS-REG-09 | TC-REG-012 |
| TS-REG-10 | TC-REG-008, TC-REG-013 to TC-REG-022 |
| TS-REG-11 | TC-REG-024, TC-REG-025 |
| TS-REG-12 | TC-REG-026 |
| TS-REG-13 | TC-REG-027 |
| TS-REG-14 | TC-REG-028 |
| TS-REG-15 | TC-REG-029 |
| TS-REG-16 | TC-REG-030 |

---

## 12. Notes

- Test cases are derived from application functionality, exploratory observations, documented application behavior, and standard QA practices.
- Official Automation Exercise test cases are not copied as project test cases.
- Expected results will be validated during execution.
- Exploratory observations are not automatically treated as defects.
- No defect will be added unless it is actually reproduced during testing.
