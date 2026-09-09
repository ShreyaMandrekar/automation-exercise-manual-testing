# Registration Test Scenarios – Automation Exercise

## 1. Module Overview

**Application:** Automation Exercise
**Module:** Registration / Signup
**Testing Type:** Manual Functional Testing
**Testing Approach:** Exploratory-based test design

This document contains test scenarios identified from exploratory testing of the Registration / Signup module. The scenarios cover registration, field validation, optional preferences, account creation, login state, logout, and account deletion.

---

## 2. Test Scenario Summary

| Scenario ID | Test Scenario                                                                | Priority |
| ----------- | ---------------------------------------------------------------------------- | -------- |
| TS-REG-01   | Verify that the Signup / Login page is accessible                            | High     |
| TS-REG-02   | Verify registration with valid user details                                  | High     |
| TS-REG-03   | Verify registration when mandatory fields are left blank                     | High     |
| TS-REG-04   | Verify validation for an invalid email address                               | High     |
| TS-REG-05   | Verify registration using an already registered email address                | High     |
| TS-REG-06   | Verify password field behavior during registration                           | Medium   |
| TS-REG-07   | Verify Date of Birth field behavior                                          | Medium   |
| TS-REG-08   | Verify Newsletter checkbox behavior                                          | Low      |
| TS-REG-09   | Verify Special Offers checkbox behavior                                      | Low      |
| TS-REG-10   | Verify registration with valid personal and address information              | High     |
| TS-REG-11   | Verify successful account creation message                                   | High     |
| TS-REG-12   | Verify Continue button after successful registration                         | Medium   |
| TS-REG-13   | Verify that the newly registered user's name is displayed after registration | High     |
| TS-REG-14   | Verify Logout functionality after successful registration                    | High     |
| TS-REG-15   | Verify Delete Account functionality                                          | High     |
| TS-REG-16   | Verify account deletion confirmation and Continue navigation                 | High     |

---

## 3. Detailed Test Scenarios

### TS-REG-01 – Verify Signup / Login Page Accessibility

**Objective:**
Verify that the user can access the Signup / Login page from the application.

**Expected Result:**
The Signup / Login page should be displayed with options for existing users to log in and new users to sign up.

---

### TS-REG-02 – Verify Registration with Valid User Details

**Objective:**
Verify that a new user can successfully register using valid registration information.

**Test Data:**
Valid name, unique email address, valid password, date of birth, personal information, and address details.

**Expected Result:**
The account should be created successfully and an account-created confirmation message should be displayed.

---

### TS-REG-03 – Verify Mandatory Field Validation

**Objective:**
Verify that registration cannot be completed when required fields are left blank.

**Expected Result:**
The application should prevent registration and display appropriate validation messages for required fields.

**Note:**
Actual mandatory-field behavior will be confirmed during test execution.

---

### TS-REG-04 – Verify Invalid Email Address Validation

**Objective:**
Verify that the registration form validates the email address format.

**Examples of test data:**

*  test
*  test@
*  test.com
*  test@@example.com

**Expected Result:**
The application should reject an invalid email format and display an appropriate validation message.

---

### TS-REG-05 – Verify Duplicate Email Registration

**Objective:**
Verify that a user cannot create another account using an email address that is already registered.

**Expected Result:**
The application should prevent duplicate registration and display an appropriate message.

---

### TS-REG-06 – Verify Password Field Behavior

**Objective:**
Verify that the password field behaves correctly during registration.

**Expected Result:**
The password should be accepted according to the application's validation rules and should be handled as a password field rather than plain text.

**Note:**
Specific password rules and boundary conditions will be determined during execution.

---

### TS-REG-07 – Verify Date of Birth Field Behavior

**Objective:**
Verify that the Date of Birth fields accept valid date information.

**Expected Result:**
Valid date, month, and year values should be accepted and registration should proceed.

**Additional Checks:**

* Valid date
* Boundary date values
* Missing date information
* Invalid date combinations

---

### TS-REG-08 – Verify Newsletter Checkbox Behavior

**Objective:**
Verify the behavior of the Newsletter subscription checkbox during registration.

**Expected Result:**

* Registration should be possible when the checkbox is unselected.
* Registration should be possible when the checkbox is selected.
* Selecting the checkbox should not prevent successful registration.

---

### TS-REG-09 – Verify Special Offers Checkbox Behavior

**Objective:**
Verify the behavior of the Special Offers checkbox during registration.

**Expected Result:**

* Registration should be possible when the checkbox is unselected.
* Registration should be possible when the checkbox is selected.
* Selecting the checkbox should not prevent successful registration.

---

### TS-REG-10 – Verify Registration with Valid Personal and Address Information

**Objective:**
Verify that valid personal and address information can be entered during registration.

**Fields Observed:**

* Title
* First Name
* Last Name
* Company
* Address
* Address 2
* Country
* State
* City
* Zipcode
* Mobile Number

**Expected Result:**
Valid information should be accepted and the user should be able to proceed with account creation.

---

### TS-REG-11 – Verify Successful Account Creation

**Objective:**
Verify that the application displays an appropriate confirmation after successful registration.

**Expected Result:**
An account-created confirmation page should be displayed indicating that the new account has been successfully created.

---

### TS-REG-12 – Verify Continue Button After Successful Registration

**Objective:**
Verify the behavior of the Continue button displayed after successful account creation.

**Expected Result:**
Clicking Continue should redirect the user to the application's home page.

---

### TS-REG-13 – Verify Newly Registered User Display

**Objective:**
Verify that the application identifies the newly registered user after successful registration.

**Expected Result:**
The user's name should be displayed on the home page after completing registration.

---

### TS-REG-14 – Verify Logout Functionality

**Objective:**
Verify that a registered user can log out successfully.

**Expected Result:**
The user should be logged out and redirected to the Signup / Login page.

---

### TS-REG-15 – Verify Delete Account Functionality

**Objective:**
Verify that a logged-in user can delete their account.

**Expected Result:**
The application should process the account deletion request and display an account-deletion confirmation page.

---

### TS-REG-16 – Verify Account Deletion Confirmation and Continue Navigation

**Objective:**
Verify the confirmation message and navigation after account deletion.

**Expected Result:**
The application should display a confirmation indicating that the account has been permanently deleted. Clicking Continue should redirect the user to the home page.

---

## 4. Test Data Used During Exploration

The following data was used during exploratory registration testing:

| Field          | Observed Test Data                  |
| -------------- | ----------------------------------- |
| Title          | Mr                                  |
| First Name     | QA                                  |
| Last Name      | Tester                              |
| Email          | [Test@123.com](mailto:Test@123.com) |
| Password       | 123                                 |
| Date of Birth  | 7 September 2009                    |
| Newsletter     | Selected                            |
| Special Offers | Selected                            |
| Company        | Software                            |
| Address        | Thane                               |
| Address 2      | Thane 2                             |
| Country        | India                               |
| State          | Maharashtra                         |
| City           | Kalyan                              |
| Zipcode        | 561302                              |
| Mobile Number  | 857-345-2345                        |

**Note:** These values were used for exploratory testing. Test execution will use appropriate test data for individual scenarios, including valid, invalid, boundary, and duplicate-data conditions where applicable.

---

## 5. Scope for Test Execution

The above scenarios will be converted into detailed test cases and executed against the Automation Exercise application.

For each test case, the following information will be recorded:

* Test Case ID
* Test Data
* Preconditions
* Test Steps
* Expected Result
* Actual Result
* Status (Pass / Fail / Blocked)
* Defect ID, if applicable
* Comments / Observations

No test result will be marked until the corresponding test case has been actually executed.

