# Contact Us Test Scenarios – Automation Exercise

## 1. Module Overview

**Application:** Automation Exercise
**Module:** Contact Us
**Testing Type:** Manual Functional Testing
**Testing Approach:** Exploratory-based test design

This document contains test scenarios identified from exploratory testing of the Contact Us module. The scenarios cover Contact Us page accessibility, form fields, mandatory email validation, email-format validation, input handling, optional file upload, submission confirmation, confirmation dialog behavior, data retention after cancellation, successful submission, and post-submission navigation.

---

## 2. Test Scenario Summary

| Scenario ID   | Test Scenario                                                   | Priority |
| ------------- | --------------------------------------------------------------- | -------- |
| TS-CONTACT-01 | Verify Contact Us page accessibility and UI elements            | High     |
| TS-CONTACT-02 | Verify Contact Us form field availability                       | High     |
| TS-CONTACT-03 | Verify mandatory validation of Email field                      | High     |
| TS-CONTACT-04 | Verify Email field format validation                            | High     |
| TS-CONTACT-05 | Verify Name field input handling                                | Medium   |
| TS-CONTACT-06 | Verify Subject and Message field input handling                 | Medium   |
| TS-CONTACT-07 | Verify Message field handling for long text                     | Medium   |
| TS-CONTACT-08 | Verify optional File Upload functionality                       | Medium   |
| TS-CONTACT-09 | Verify form submission with optional fields omitted             | High     |
| TS-CONTACT-10 | Verify submission confirmation dialog behavior                  | High     |
| TS-CONTACT-11 | Verify cancellation of submission and retention of entered data | High     |
| TS-CONTACT-12 | Verify successful Contact Us submission and Home navigation     | High     |

---

# 3. Detailed Test Scenarios

## TS-CONTACT-01 – Verify Contact Us Page Accessibility and UI Elements

**Objective:**
Verify that the Contact Us page is accessible and contains the expected Contact Us UI elements.

**Precondition:**
User is on the Automation Exercise application.

**Test Conditions:**

* Navigate to the Contact Us section.
* Verify that the Contact Us page is displayed.
* Verify the Get In Touch section.
* Verify the Feedback for Us section.
* Verify the displayed feedback email address.
* Verify the Test Case Templates link/button.

**Expected Result:**
The Contact Us page should be accessible and the available Contact Us-related UI elements and information should be displayed correctly.

---

## TS-CONTACT-02 – Verify Contact Us Form Field Availability

**Objective:**
Verify that the Contact Us form contains the required input controls and submission control.

**Test Conditions:**

* Observe the Contact Us form.
* Verify the Name field.
* Verify the Email field.
* Verify the Subject field.
* Verify the Your Message Here field.
* Verify the Choose File control.
* Verify the Submit button.

**Expected Result:**
The Contact Us form should display the available input fields, file upload control, and Submit button.

---

## TS-CONTACT-03 – Verify Mandatory Validation of Email Field

**Objective:**
Verify that the Email field is required for Contact Us form submission.

**Test Conditions:**

* Leave the Email field blank.
* Enter valid or other appropriate data in the remaining fields where required for the test.
* Click Submit.
* Observe the validation behavior.

**Expected Result:**
The application should prevent form submission when the Email field is blank and should display appropriate mandatory-field validation.

**Observed Validation:**
Browser validation displays `Please fill out this field.` and highlights the Email field.

---

## TS-CONTACT-04 – Verify Email Field Format Validation

**Objective:**
Verify that the Email field validates the entered email address format.

**Test Data Examples:**

* `test`
* `test@`
* `test@example.com`

**Test Conditions:**

* Enter an invalid email value.
* Enter the remaining required data.
* Click Submit.
* Observe the validation message.
* Repeat with a valid email address.

**Expected Result:**
The application should prevent submission when an invalid email format is entered and should allow the form to proceed when a valid email format is provided.

**Observed Validation:**

* `test` → `Please include an '@' symbol in the email address.`
* `test@` → `Please enter a part following '@'.`
* `test@example.com` → accepted.

---

## TS-CONTACT-05 – Verify Name Field Input Handling

**Objective:**
Verify how the Name field handles different types of input.

**Test Data Examples:**

* Alphabetic text
* Alphanumeric text
* Numeric and special-character combination

**Test Conditions:**

* Enter normal text in the Name field.
* Enter a combination of letters and numbers.
* Enter numbers and special characters.
* Complete the required Email field.
* Submit the form.
* Observe the form behavior.

**Expected Result:**
The application should process the entered Name value according to its implemented input behavior without preventing form submission when the required Email field is valid.

**Note:**
Acceptance of numeric or special characters will be recorded as application behavior and will not automatically be treated as a defect without a defined input-format requirement.

---

## TS-CONTACT-06 – Verify Subject and Message Field Input Handling

**Objective:**
Verify that the Subject and Message fields accept appropriate user-entered content.

**Test Conditions:**

* Enter normal text in the Subject field.
* Enter normal text in the Message field.
* Complete the required Email field.
* Submit the form.
* Repeat using numbers and special characters in the Subject field.
* Observe the submission behavior.

**Expected Result:**
The application should accept the entered Subject and Message values and should allow the form to proceed when the required Email field contains valid data.

**Note:**
Subject and Message were observed to be optional during exploratory testing.

---

## TS-CONTACT-07 – Verify Message Field Handling for Long Text

**Objective:**
Verify the behavior of the Message field when a long message is entered.

**Test Conditions:**

* Enter a long text value in the Message field.
* Complete the required Email field.
* Submit the form.
* Observe whether the message is accepted or restricted.

**Expected Result:**
The Message field should handle the entered text according to the application's supported behavior without unexpected truncation or submission failure.

**Note:**
No visible character limit or restriction was observed during exploratory testing.

---

## TS-CONTACT-08 – Verify Optional File Upload Functionality

**Objective:**
Verify that the file upload control accepts supported files and that file selection is optional.

**Test Conditions:**

* Open the Contact Us form.
* Submit the form without selecting a file.
* Select a text file using Choose File.
* Submit the form.
* Repeat using an image file.
* Observe the submission behavior.

**Expected Result:**
The application should allow Contact Us submission without requiring a file and should process selected supported files without preventing form submission.

**Observed Behavior:**
Both a text file and an image file were accepted during exploratory testing.

---

## TS-CONTACT-09 – Verify Form Submission with Optional Fields Omitted

**Objective:**
Verify that the Contact Us form can be submitted when optional fields are left blank.

**Precondition:**
A valid Email address is available.

**Test Conditions:**

* Enter a valid Email address.
* Leave Subject blank.
* Leave Message blank.
* Leave the File Upload control without selecting a file.
* Submit the form.
* Observe the submission behavior.

**Expected Result:**
The form should allow submission when the optional Subject, Message, and File Upload fields are left blank, provided the required Email field contains valid data.

**Observed Behavior:**
The form was successfully submitted with these fields blank.

---

## TS-CONTACT-10 – Verify Submission Confirmation Dialog Behavior

**Objective:**
Verify that the confirmation dialog is displayed when a valid Contact Us form is submitted.

**Precondition:**
Valid Contact Us form data has been entered.

**Test Conditions:**

* Click Submit.
* Observe the confirmation dialog.
* Verify the displayed message.
* Verify the OK and Cancel options.
* Click OK.
* Observe the resulting page.

**Expected Result:**
The confirmation dialog should be displayed before the form is submitted. Selecting OK should continue the submission process and display the appropriate success result.

**Observed Dialog Message:**
`Press OK to proceed!`

---

## TS-CONTACT-11 – Verify Cancellation of Submission and Retention of Entered Data

**Objective:**
Verify the behavior when the user cancels the Contact Us submission from the confirmation dialog.

**Precondition:**
Valid Contact Us form data has been entered and the confirmation dialog is displayed.

**Test Conditions:**

* Click Submit.
* When the confirmation dialog appears, select Cancel.
* Observe the Contact Us page.
* Verify whether the entered form data remains available.
* Submit the form again.
* Select OK.

**Expected Result:**
Selecting Cancel should stop the current submission and return the user to the Contact Us form without unexpectedly clearing the entered information. The user should be able to submit the form again.

**Observed Behavior:**
After selecting Cancel, the Contact Us page remained displayed and the previously entered data remained in the form. The form could be submitted again successfully by selecting Submit and then OK.

---

## TS-CONTACT-12 – Verify Successful Contact Us Submission and Home Navigation

**Objective:**
Verify that a valid Contact Us form can be successfully submitted and that the Home option works after submission.

**Precondition:**
Valid Contact Us data has been entered.

**Test Conditions:**

* Enter a valid Email address.
* Enter other form data as required for the test.
* Optionally select a file.
* Click Submit.
* Select OK on the confirmation dialog.
* Observe the success message.
* Verify the Home button.
* Click Home.

**Expected Result:**
The Contact Us form should be submitted successfully and an appropriate success message should be displayed. The Home option should be available and should redirect the user to the application's Home page.

**Observed Success Message:**
`Success, your detail has been submitted successfully.`

---

# 4. Test Data

The following test data categories will be used during Contact Us testing:

| Data Type                       | Example / Description                              |
| ------------------------------- | -------------------------------------------------- |
| Valid Name                      | Generic test name                                  |
| Alphanumeric Name               | Combination of letters and numbers                 |
| Special-character Name          | Numeric and special-character combination          |
| Valid Email                     | `test@example.com`                                 |
| Invalid Email                   | `test`                                             |
| Incomplete Email                | `test@`                                            |
| Valid Subject                   | Generic subject text                               |
| Subject with special characters | Generic text containing numbers/special characters |
| Valid Message                   | Generic message content                            |
| Long Message                    | Long text exceeding normal short-message length    |
| Text File                       | `.txt` test file                                   |
| Image File                      | `.jpg`/image test file                             |
| Blank Subject                   | Empty field                                        |
| Blank Message                   | Empty field                                        |
| No File                         | File upload left unselected                        |

**Note:**
Test data will be selected appropriately during execution. Real personal information will not be used in the public test documentation.

---

# 5. Scope for Test Execution

The following areas will be covered during formal Contact Us testing:

* Contact Us page accessibility
* Contact Us UI elements
* Form field availability
* Email mandatory validation
* Email format validation
* Name input handling
* Subject input handling
* Message input handling
* Long message handling
* Optional file upload
* Form submission with optional fields omitted
* Submission confirmation dialog
* Confirmation OK behavior
* Confirmation Cancel behavior
* Data retention after cancellation
* Successful form submission
* Success message
* Home navigation after submission

Formal test cases will be created from these scenarios and executed against the live Automation Exercise application.

Any reproducible deviation from the expected behavior will be documented separately as a defect.
