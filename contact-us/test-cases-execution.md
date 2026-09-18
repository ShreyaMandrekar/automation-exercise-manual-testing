# Contact Us Test Cases & Execution – Automation Exercise

## 1. Module Information

| Field            | Details                                    |
| ---------------- | ------------------------------------------ |
| Application      | Automation Exercise                        |
| Module           | Contact Us                                 |
| Testing Type     | Manual Testing                             |
| Test Level       | System Testing                             |
| Test Approach    | Functional, Positive, Negative, Validation |
| Test Case Status | Not Executed                               |
| Tester           | Shreya Mandrekar                           |

---

## 2. Objective

The objective of these test cases is to verify the Contact Us functionality of the Automation Exercise application, including:

* Contact Us page accessibility
* Contact Us form fields and controls
* Feedback section
* Email mandatory validation
* Email format validation
* Name field input handling
* Subject field input handling
* Message field input handling
* Long message handling
* File upload functionality
* Form submission with optional fields omitted
* Submission confirmation dialog
* OK and Cancel behavior
* Form data retention after cancellation
* Successful Contact Us submission
* Success confirmation
* Home navigation after successful submission

All Actual Results, Status, Defect ID, and Comments will be updated after executing the test cases against the live application.

---

## 3. Preconditions

Unless otherwise specified:

1. Automation Exercise website is accessible.
2. Tester has access to a web browser.
3. Contact Us page is accessible.
4. Required test data is prepared.
5. Test files are available for file-upload testing.

---

# 4. Test Case Execution

## TC-CONTACT-001 – Verify Contact Us page is accessible

**Scenario:** TS-CONTACT-01

| Field         | Details                   |
| ------------- | ------------------------- |
| Test Case ID  | TC-CONTACT-001            |
| Priority      | High                      |
| Preconditions | Application is accessible |
| Test Data     | N/A                       |

**Steps:**

1. Open Automation Exercise.
2. Navigate to the Contact Us page.

**Expected Result:**

The Contact Us page should be displayed successfully.

**Actual Result:**

The Contact Us page opened successfully. All Contact Us form fields were displayed properly, and the "Feedback for Us" section was also visible.

**Status:**

PASS

**Defect ID:**

N/A

**Comments:**

Contact Us page and its main UI elements were displayed successfully.

---

## TC-CONTACT-002 – Verify Contact Us form contains required fields and controls

**Scenario:** TS-CONTACT-02

| Field         | Details                 |
| ------------- | ----------------------- |
| Test Case ID  | TC-CONTACT-002          |
| Priority      | High                    |
| Preconditions | Contact Us page is open |
| Test Data     | N/A                     |

**Steps:**

1. Open the Contact Us page.
2. Locate the Contact Us form.
3. Verify the available fields and controls.

**Expected Result:**

The Contact Us form should contain the expected fields and controls, including Name, Email, Subject, Message, Choose File, and Submit.

**Actual Result:**
The Contact Us form displayed the Name, Email, Subject, Your Message Here, Choose File, and Submit button correctly.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
All expected Contact Us form fields and controls were present and displayed properly.

---

## TC-CONTACT-003 – Verify Feedback section

**Scenario:** TS-CONTACT-01

| Field         | Details                 |
| ------------- | ----------------------- |
| Test Case ID  | TC-CONTACT-003          |
| Priority      | High                    |
| Preconditions | Contact Us page is open |
| Test Data     | N/A                     |

**Steps:**

1. Open the Contact Us page.
2. Locate the Feedback section.
3. Verify the displayed feedback contact information.

**Expected Result:**

The Feedback section and displayed contact information should be visible.

**Actual Result:**
The Feedback for Us section was displayed successfully, and the email address was also visible.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
Feedback section and email contact information were displayed properly.

---

## TC-CONTACT-004 – Verify mandatory validation of Email field

**Scenario:** TS-CONTACT-03

| Field         | Details                 |
| ------------- | ----------------------- |
| Test Case ID  | TC-CONTACT-004          |
| Priority      | High                    |
| Preconditions | Contact Us page is open |
| Test Data     | Email: Blank            |

**Steps:**

1. Open the Contact Us page.
2. Leave the Email field blank.
3. Enter the required information in other fields.
4. Click Submit.

**Expected Result:**

The submission should be prevented and mandatory validation should be displayed for the Email field.

**Actual Result:**
The Email field was left blank and the Submit button was clicked. A browser validation popup appeared stating, "Please fill out this field." The validation was displayed for the Email field.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
Mandatory validation was displayed correctly when the Email field was left blank.

---

## TC-CONTACT-005 – Verify Email validation without @ symbol

**Scenario:** TS-CONTACT-04

| Field         | Details                 |
| ------------- | ----------------------- |
| Test Case ID  | TC-CONTACT-005          |
| Priority      | High                    |
| Preconditions | Contact Us page is open |
| Test Data     | Email: `test`           |

**Steps:**

1. Enter `test` in the Email field.
2. Complete the other required fields.
3. Click Submit.

**Expected Result:**

The invalid email format should be rejected and appropriate email validation should be displayed.

**Actual Result:**
The Email field was entered with `test`. A browser validation popup appeared stating, "Please include an '@' in your email address. 'test' is missing an '@'."

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
Invalid email format without the `@` symbol was rejected by email validation.

---

## TC-CONTACT-006 – Verify Email validation for incomplete email

**Scenario:** TS-CONTACT-04

| Field         | Details                 |
| ------------- | ----------------------- |
| Test Case ID  | TC-CONTACT-006          |
| Priority      | High                    |
| Preconditions | Contact Us page is open |
| Test Data     | Email: `test@`          |

**Steps:**

1. Enter `test@` in the Email field.
2. Complete the other required fields.
3. Click Submit.

**Expected Result:**

The incomplete email format should be rejected and appropriate email validation should be displayed.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-CONTACT-007 – Verify valid Email input

**Scenario:** TS-CONTACT-04

| Field         | Details                   |
| ------------- | ------------------------- |
| Test Case ID  | TC-CONTACT-007            |
| Priority      | High                      |
| Preconditions | Contact Us page is open   |
| Test Data     | Email: `test@example.com` |

**Steps:**

1. Enter `test@example.com` in the Email field.
2. Complete the required fields.
3. Submit the form.

**Expected Result:**

The valid email address should be accepted without email-format validation errors.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-CONTACT-008 – Verify Name field accepts normal text

**Scenario:** TS-CONTACT-05

| Field         | Details                 |
| ------------- | ----------------------- |
| Test Case ID  | TC-CONTACT-008          |
| Priority      | Medium                  |
| Preconditions | Contact Us page is open |
| Test Data     | Name: `Shreya`          |

**Steps:**

1. Enter `Shreya` in the Name field.
2. Enter a valid email address.
3. Enter valid Subject and Message values.
4. Submit the form.

**Expected Result:**

The Name field should accept normal text input and the form should proceed without Name-related validation errors.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-CONTACT-009 – Verify Name field accepts alphanumeric input

**Scenario:** TS-CONTACT-05

| Field         | Details                 |
| ------------- | ----------------------- |
| Test Case ID  | TC-CONTACT-009          |
| Priority      | Medium                  |
| Preconditions | Contact Us page is open |
| Test Data     | Name: `Shreya123`       |

**Steps:**

1. Enter `Shreya123` in the Name field.
2. Enter a valid email address.
3. Enter valid Subject and Message values.
4. Submit the form.

**Expected Result:**

The Name field should accept the entered input without unexpected validation or application errors.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-CONTACT-010 – Verify Name field input containing numbers and special characters

**Scenario:** TS-CONTACT-05

| Field         | Details                 |
| ------------- | ----------------------- |
| Test Case ID  | TC-CONTACT-010          |
| Priority      | Medium                  |
| Preconditions | Contact Us page is open |
| Test Data     | Name: `Shreya@123!`     |

**Steps:**

1. Enter `Shreya@123!` in the Name field.
2. Enter a valid email address.
3. Enter valid Subject and Message values.
4. Submit the form.

**Expected Result:**

The application should handle the entered Name value consistently without unexpected application errors.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-CONTACT-011 – Verify Subject field accepts normal text

**Scenario:** TS-CONTACT-06

| Field         | Details                    |
| ------------- | -------------------------- |
| Test Case ID  | TC-CONTACT-011             |
| Priority      | Medium                     |
| Preconditions | Contact Us page is open    |
| Test Data     | Subject: `Product Inquiry` |

**Steps:**

1. Enter a valid Name.
2. Enter a valid Email.
3. Enter `Product Inquiry` in the Subject field.
4. Enter a valid Message.
5. Submit the form.

**Expected Result:**

The Subject field should accept normal text input without unexpected validation errors.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-CONTACT-012 – Verify Subject field accepts numbers and special characters

**Scenario:** TS-CONTACT-06

| Field         | Details                 |
| ------------- | ----------------------- |
| Test Case ID  | TC-CONTACT-012          |
| Priority      | Medium                  |
| Preconditions | Contact Us page is open |
| Test Data     | Subject: `Order#123!`   |

**Steps:**

1. Enter a valid Name.
2. Enter a valid Email.
3. Enter `Order#123!` in the Subject field.
4. Enter a valid Message.
5. Submit the form.

**Expected Result:**

The application should handle the entered Subject value consistently without unexpected application errors.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-CONTACT-013 – Verify Message field accepts normal text

**Scenario:** TS-CONTACT-06

| Field         | Details                               |
| ------------- | ------------------------------------- |
| Test Case ID  | TC-CONTACT-013                        |
| Priority      | Medium                                |
| Preconditions | Contact Us page is open               |
| Test Data     | Message: `I need help with my order.` |

**Steps:**

1. Enter a valid Name.
2. Enter a valid Email.
3. Enter a valid Subject.
4. Enter `I need help with my order.` in the Message field.
5. Submit the form.

**Expected Result:**

The Message field should accept normal text input and the form should proceed without unexpected validation errors.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-CONTACT-014 – Verify Message field handles long text

**Scenario:** TS-CONTACT-07

| Field         | Details                 |
| ------------- | ----------------------- |
| Test Case ID  | TC-CONTACT-014          |
| Priority      | Medium                  |
| Preconditions | Contact Us page is open |
| Test Data     | Long text message       |

**Steps:**

1. Enter a valid Name.
2. Enter a valid Email.
3. Enter a valid Subject.
4. Enter a long text message in the Message field.
5. Submit the form.

**Expected Result:**

The application should accept the Message input according to its defined field constraints and should not produce an unexpected application error.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-CONTACT-015 – Verify Contact Us submission without file upload

**Scenario:** TS-CONTACT-08

| Field         | Details                 |
| ------------- | ----------------------- |
| Test Case ID  | TC-CONTACT-015          |
| Priority      | Medium                  |
| Preconditions | Contact Us page is open |
| Test Data     | File: None              |

**Steps:**

1. Enter a valid Name.
2. Enter a valid Email.
3. Enter a valid Subject.
4. Enter a valid Message.
5. Do not select any file.
6. Click Submit.

**Expected Result:**

The form should allow submission without a file if file upload is optional.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-CONTACT-016 – Verify text file upload functionality

**Scenario:** TS-CONTACT-08

| Field         | Details                 |
| ------------- | ----------------------- |
| Test Case ID  | TC-CONTACT-016          |
| Priority      | Medium                  |
| Preconditions | Contact Us page is open |
| Test Data     | Text file               |

**Steps:**

1. Enter a valid Name.
2. Enter a valid Email.
3. Enter a valid Subject.
4. Enter a valid Message.
5. Click Choose File.
6. Select a valid text file.
7. Submit the form.

**Expected Result:**

The selected text file should be accepted and the form should proceed according to the application's behavior.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-CONTACT-017 – Verify image file upload functionality

**Scenario:** TS-CONTACT-08

| Field         | Details                 |
| ------------- | ----------------------- |
| Test Case ID  | TC-CONTACT-017          |
| Priority      | Medium                  |
| Preconditions | Contact Us page is open |
| Test Data     | Image file              |

**Steps:**

1. Enter a valid Name.
2. Enter a valid Email.
3. Enter a valid Subject.
4. Enter a valid Message.
5. Click Choose File.
6. Select a valid image file.
7. Submit the form.

**Expected Result:**

The selected image file should be accepted and the form should proceed according to the application's behavior.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-CONTACT-018 – Verify submission with optional fields omitted

**Scenario:** TS-CONTACT-09

| Field         | Details                                                                            |
| ------------- | ---------------------------------------------------------------------------------- |
| Test Case ID  | TC-CONTACT-018                                                                     |
| Priority      | High                                                                               |
| Preconditions | Contact Us page is open                                                            |
| Test Data     | Name: Blank; Email: `test@example.com`; Subject: Blank; Message: Blank; File: None |

**Steps:**

1. Open the Contact Us page.
2. Leave the Name field blank.
3. Enter `test@example.com` in the Email field.
4. Leave the Subject field blank.
5. Leave the Message field blank.
6. Do not select a file.
7. Click Submit.

**Expected Result:**

The form should apply mandatory validation only to fields that are required and should not prevent submission solely because optional fields are blank.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-CONTACT-019 – Verify submission confirmation dialog is displayed

**Scenario:** TS-CONTACT-10

| Field         | Details                   |
| ------------- | ------------------------- |
| Test Case ID  | TC-CONTACT-019            |
| Priority      | High                      |
| Preconditions | Contact Us page is open   |
| Test Data     | Valid contact information |

**Steps:**

1. Enter valid contact information.
2. Click Submit.
3. Observe the displayed confirmation dialog.

**Expected Result:**

A confirmation dialog should be displayed before the Contact Us submission is completed.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-CONTACT-020 – Verify OK action on submission confirmation dialog

**Scenario:** TS-CONTACT-10

| Field         | Details                          |
| ------------- | -------------------------------- |
| Test Case ID  | TC-CONTACT-020                   |
| Priority      | High                             |
| Preconditions | Confirmation dialog is displayed |
| Test Data     | Valid contact information        |

**Steps:**

1. Enter valid contact information.
2. Click Submit.
3. When the confirmation dialog appears, click OK.

**Expected Result:**

The confirmation dialog should close and the Contact Us submission should proceed successfully.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-CONTACT-021 – Verify Cancel action on submission confirmation dialog

**Scenario:** TS-CONTACT-11

| Field         | Details                          |
| ------------- | -------------------------------- |
| Test Case ID  | TC-CONTACT-021                   |
| Priority      | High                             |
| Preconditions | Confirmation dialog is displayed |
| Test Data     | Valid contact information        |

**Steps:**

1. Enter valid contact information.
2. Click Submit.
3. When the confirmation dialog appears, click Cancel.

**Expected Result:**

The confirmation dialog should close and the submission should not be completed.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-CONTACT-022 – Verify form data remains after Cancel action

**Scenario:** TS-CONTACT-11

| Field         | Details                          |
| ------------- | -------------------------------- |
| Test Case ID  | TC-CONTACT-022                   |
| Priority      | High                             |
| Preconditions | Confirmation dialog is displayed |
| Test Data     | Valid contact information        |

**Steps:**

1. Enter valid contact information in the Contact Us form.
2. Click Submit.
3. When the confirmation dialog appears, click Cancel.
4. Observe the Contact Us form.

**Expected Result:**

The entered form data should remain available after cancelling the submission unless the application is designed to clear the form.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-CONTACT-023 – Verify form can be resubmitted after Cancel

**Scenario:** TS-CONTACT-11

| Field         | Details                             |
| ------------- | ----------------------------------- |
| Test Case ID  | TC-CONTACT-023                      |
| Priority      | High                                |
| Preconditions | Contact Us form contains valid data |
| Test Data     | Valid contact information           |

**Steps:**

1. Enter valid contact information.
2. Click Submit.
3. When the confirmation dialog appears, click Cancel.
4. Click Submit again.
5. Click OK on the confirmation dialog.

**Expected Result:**

The form should allow the user to resubmit the contact information after cancelling the previous submission.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-CONTACT-024 – Verify successful Contact Us submission

**Scenario:** TS-CONTACT-12

| Field         | Details                   |
| ------------- | ------------------------- |
| Test Case ID  | TC-CONTACT-024            |
| Priority      | High                      |
| Preconditions | Contact Us page is open   |
| Test Data     | Valid contact information |

**Steps:**

1. Open the Contact Us page.
2. Enter valid contact information.
3. Click Submit.
4. Click OK on the confirmation dialog.
5. Observe the result after submission.

**Expected Result:**

The Contact Us form should be submitted successfully and a successful submission confirmation should be displayed.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-CONTACT-025 – Verify Home button after successful Contact Us submission

**Scenario:** TS-CONTACT-12

| Field         | Details                                |
| ------------- | -------------------------------------- |
| Test Case ID  | TC-CONTACT-025                         |
| Priority      | Medium                                 |
| Preconditions | Contact Us form submitted successfully |
| Test Data     | N/A                                    |

**Steps:**

1. Complete a successful Contact Us submission.
2. Observe the success confirmation page.
3. Click the Home button.

**Expected Result:**

The Home button should redirect the user to the Automation Exercise homepage.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

# 5. Test Execution Summary

| Metric             | Result |
| ------------------ | ------ |
| Total Test Cases   | 25     |
| Passed             |        |
| Failed             |        |
| Blocked            |        |
| Not Executed       | 25     |
| Defects Identified |        |

---

# 6. Test Environment

| Environment      | Details                         |
| ---------------- | ------------------------------- |
| Application      | Automation Exercise             |
| Browser          | Google Chrome                   |
| Browser Version  | Chrome 152.0.7977.82            |
| Operating System | Windows 11 Home Single Language |
| OS Version       | 25H2                            |
| OS Build         | 26200.9278                      |
| Testing Period   | August–September 2026           |

---

# 7. Defect Handling

If the Actual Result differs from the Expected Result during execution:

1. Reproduce the issue to confirm the behavior.
2. Record the actual behavior accurately.
3. Assess whether the difference represents a defect or an expected/observed behavior.
4. Create a Jira defect if a genuine defect is identified.
5. Add the Jira Defect ID to the relevant test case.
6. Record relevant details in the defect report.

---

# 8. Execution Notes

* Test cases will be executed against the live Automation Exercise application.
* Actual Results will contain the behavior observed during execution.
* Status will be updated as PASS, FAIL, BLOCKED, or NOT EXECUTED.
* Defect IDs will be added only when genuine reproducible defects are identified.
* Observations will not automatically be treated as defects without a defined requirement or clear expected behavior.
* Retesting and regression testing will be documented separately after defects are fixed.
