# Automation Exercise – Exploration Notes

## 1. Purpose

This document records observations made during exploratory testing of the Automation Exercise web application. The purpose of this exploration was to understand the application's functionality, user flows, input fields, validations, and observed behavior before designing formal test scenarios and test cases.

## 2. Application Under Test

**Application:** Automation Exercise
**Testing Type:** Manual Exploratory Testing
**Module Explored:** Registration / Signup
**Testing Approach:** Exploratory testing based on direct interaction with the application.

---

## 3. Registration / Signup Module

### 3.1 Initial Signup Page

The Signup/Login page contains two sections:

* **Login to your account**
* **New User Signup**

The New User Signup section contains:

* Name
* Email Address
* Signup button

### 3.2 Initial Signup Field Observations

| Field         | Observation                                                                                                                                                                                 |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Name          | Required. Leaving the field blank displays a validation message asking the user to fill the field. Numeric characters were accepted during exploration.                                     |
| Email Address | Required. Leaving the field blank displays a validation message. Invalid email formats were rejected in some cases, including an email without `@` and an incomplete email ending with `@`. |
| Signup button | Clicking Signup with valid initial details opens the account creation form.                                                                                                                 |

---

## 4. Account Creation Form

After submitting the initial Signup form with valid details, the application displays the account creation form.

### 4.1 Account Creation Fields

| No. | Field          | Type / Control  | Observation                                                                                       |
| --: | -------------- | --------------- | ------------------------------------------------------------------------------------------------- |
|   1 | Title          | Radio button    | Mr. and Mrs. options are available. Blank selection was accepted during exploration.              |
|   2 | Name           | Text field      | Value is carried from the initial Signup step.                                                    |
|   3 | Email          | Email field     | Value is carried from the initial Signup step.                                                    |
|   4 | Password       | Password field  | Required. Blank value was not accepted. Short password values were accepted during exploration.   |
|   5 | Date of Birth  | Dropdown fields | Day, month and year controls are available.                                                       |
|   6 | Newsletter     | Checkbox        | Unselected by default. Registration worked with both selected and unselected states.              |
|   7 | Special Offers | Checkbox        | Unselected by default. Registration worked with both selected and unselected states.              |
|   8 | First Name     | Text field      | Required during account creation.                                                                 |
|   9 | Last Name      | Text field      | Required during account creation.                                                                 |
|  10 | Company        | Text field      | Input was accepted during exploration.                                                            |
|  11 | Address        | Text field      | Required. Blank value was not accepted. Numeric and text values were accepted during exploration. |
|  12 | Address 2      | Text field      | Blank value was accepted.                                                                         |
|  13 | Country        | Dropdown        | India was selected by default. Multiple country options were available.                           |
|  14 | State          | Text field      | Required. Blank value was not accepted.                                                           |
|  15 | City           | Text field      | Required. Blank value was not accepted.                                                           |
|  16 | Zipcode        | Text field      | Required. Blank value was not accepted. Character input was accepted during exploration.          |
|  17 | Mobile Number  | Text field      | Required. Blank value was not accepted. Character input was accepted during exploration.          |

---

## 5. Newsletter and Special Offers

### Newsletter

* Control type: Checkbox
* Default state: Unselected
* Selecting the checkbox: Registration remained successful.
* Leaving the checkbox unselected: Registration remained successful.
* Observed as an optional field during exploration.

### Special Offers

* Control type: Checkbox
* Default state: Unselected
* Selecting the checkbox: Registration remained successful.
* Leaving the checkbox unselected: Registration remained successful.
* Observed as an optional field during exploration.

---

## 6. Country Dropdown

The Country field is presented as a dropdown.

The following options were observed:

1. India
2. United States
3. Canada
4. Australia
5. Israel
6. New Zealand
7. Singapore

**Default selection observed:** India

---

## 7. Successful Registration Flow

A complete registration was performed using test data.

### Test Data Used

| Field          | Test Data                           |
| -------------- | ----------------------------------- |
| Title          | Mr.                                 |
| Name           | QA Tester                           |
| Email          | [Test@123.com](mailto:Test@123.com) |
| Password       | 123                                 |
| Date of Birth  | 7 September 2009                    |
| Newsletter     | Selected                            |
| Special Offers | Selected                            |
| First Name     | QA                                  |
| Last Name      | Tester                              |
| Company        | Software                            |
| Address        | Thane                               |
| Address 2      | Thane 2                             |
| Country        | India                               |
| State          | Maharashtra                         |
| City           | Kalyan                              |
| Zipcode        | 561302                              |
| Mobile Number  | 857-345-2345                        |

### Observed Result

1. The Create Account button was clicked after entering the registration details.
2. An Account Created confirmation page appeared.
3. The page displayed a successful account creation message.
4. A Continue button was displayed.
5. Clicking Continue redirected to the Home page.
6. The logged-in user's name, **QA Tester**, was displayed.
7. Logout and Delete Account options were available.

---

## 8. Logout Flow

### Action

The Logout option was selected from the logged-in user's navigation.

### Observed Result

* The user was successfully logged out.
* The application redirected to the Signup/Login page.

---

## 9. Account Deletion Flow

### Action

The Delete Account option was selected while logged in.

### Observed Result

* An account deletion confirmation page appeared.
* The page indicated that the account had been permanently deleted.
* A Continue button was displayed.
* Clicking Continue redirected to the Home page.

---

## 10. Observations Requiring Further Formal Testing

The following behaviors were observed during exploration and should be investigated more systematically when formal test cases are created:

* Name field accepted numeric characters.
* Email validation behavior should be tested with different valid and invalid formats.
* A short password value was accepted during exploration.
* Date of Birth field behavior should be tested with valid, invalid and boundary values.
* Address field accepted numeric and text input.
* Zipcode field accepted character input during exploration.
* Mobile Number field accepted character input during exploration.

These observations are **not automatically classified as defects**. They require comparison against the expected requirements and formal test execution before a defect is reported.

---

## 11. Exploration Summary

The Registration module was explored from the initial Signup page through:

**Signup → Account Creation → Successful Registration → Logged-in State → Logout → Account Deletion**

The exploration identified the available registration fields, input controls, mandatory/optional behavior observed during exploration, validation behavior, dropdown values, and the complete account lifecycle.

Formal test scenarios and detailed test cases will be created after completing the exploratory phase.

