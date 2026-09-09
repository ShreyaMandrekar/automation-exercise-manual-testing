# Defect Reports

## 1. Document Information

| Field | Details |
|---|---|
| Project | Automation Exercise - Manual QA |
| Module | Registration |
| Application | Automation Exercise |
| Defect Tracking Tool | Jira |
| Defects Identified | 2 |

---

## 2. Defect Summary

| Defect ID | Test Case | Summary | Severity | Priority | Status |
|---|---|---|---|---|---|
| AEMQ-1 | TC-REG-021 | Zipcode field accepts invalid input formats without validation | Medium | Medium | Open |
| AEMQ-2 | TC-REG-022 | Mobile Number field accepts invalid formats without validation | Medium | Medium | Open |

---

## 3. Defect AEMQ-1

### Summary
Zipcode field accepts invalid input formats without validation.

### Related Test Case
TC-REG-021 – Zipcode field validation

### Module
Registration

### Severity
Medium

### Priority
Medium

### Status
Open

### Preconditions
- User is on the account creation form.
- Required registration information is available.

### Steps to Reproduce

1. Navigate to the account creation form.
2. Enter valid values in the required fields.
3. Enter an invalid value in the Zipcode field.
4. Use inputs such as:
   - `ABCDE`
   - `56130A`
   - `@12345`
5. Click Create Account.

### Expected Result

The Zipcode field should validate the entered value according to the application's expected postal-code format and display an appropriate validation message for invalid input.

### Actual Result

The application accepted alphabetic-only, alphanumeric, and special-character input in the Zipcode field without displaying a validation message.

### Test Data

| Input Type | Value | Result |
|---|---|---|
| Valid numeric | 561302 | Accepted |
| Numeric | 12345 | Accepted |
| Alphabetic | ABCDE | Accepted |
| Alphanumeric | 56130A | Accepted |
| Special characters | @12345 | Accepted |

### Evidence

The defect was reproduced during actual test execution.

### Jira
AEMQ-1

---

## 4. Defect AEMQ-2

### Summary
Mobile Number field accepts invalid formats without validation.

### Related Test Case
TC-REG-022 – Mobile Number field validation

### Module
Registration

### Severity
Medium

### Priority
Medium

### Status
Open

### Preconditions
- User is on the account creation form.
- Required registration information is available.

### Steps to Reproduce

1. Navigate to the account creation form.
2. Enter valid values in the required fields.
3. Enter invalid input in the Mobile Number field.
4. Test alphabetic, alphanumeric, special-character, and different-length inputs.
5. Click Create Account.

### Expected Result

The Mobile Number field should validate the entered value according to the application's expected mobile-number format and display an appropriate validation message for invalid input.

### Actual Result

The application accepted alphabetic, alphanumeric, special-character, and different-length inputs in the Mobile Number field without displaying an appropriate validation message.

### Test Data

| Input Type | Example | Result |
|---|---|---|
| Valid mobile number | 857-345-2345 | Accepted |
| Numeric | 12345 | Accepted |
| Alphabetic | ABCDE | Accepted |
| Alphanumeric | 123ABC | Accepted |
| Special characters | @12345 | Accepted |
| Different length | Various lengths | Accepted |

### Evidence

The defect was reproduced during actual test execution.

### Jira
AEMQ-2

---

## 5. Defect Reporting Notes

- Defects were reported only after the relevant test cases were executed.
- The observed behavior was reproduced during testing.
- The defects are documented separately in Jira and linked to their corresponding test cases.
- Severity and priority may be reassessed after business impact and requirements are formally confirmed.
- Both defects are currently awaiting resolution and retesting.
