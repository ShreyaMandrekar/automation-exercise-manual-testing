# Defect Reports

## 1. Document Information

| Field | Details |
|---|---|
| Project | Automation Exercise - Manual QA |
| Module | Registration, Cart & Checkout |
| Application | Automation Exercise |
| Defect Tracking Tool | Jira |
| Defects Identified | 3 |

---

## 2. Defect Summary

| Defect ID | Test Case | Summary | Severity | Priority | Status |
|---|---|---|---|---|---|
| AEMQ-1 | TC-REG-021 | Zipcode field accepts invalid input formats without validation | Medium | Medium | Open |
| AEMQ-2 | TC-REG-022 | Mobile Number field accepts invalid formats without validation | Medium | Medium | Open |
| AEMQ-3 | TC-CART-028 | Payment fields accept invalid input formats | High | High | Open |


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

## 5. Defect AEMQ-3

### Summary
Payment fields accept invalid input formats.

### Related Test Case
TC-CART-028 – Verify Payment field input format handling

### Module
Cart & Checkout

### Severity
High

### Priority
High

### Status
Open

### Preconditions
- User is logged in.
- Products have been added to the Cart.
- User has proceeded to the Checkout and Payment page.
- Payment form is displayed.

### Steps to Reproduce

1. Add a product to the Cart.
2. Proceed to Checkout.
3. Navigate to the Payment page.
4. Enter invalid input in the payment fields:
   - Name on Card: `123`
   - Card Number: `ABC`
   - CVC: `ABC`
   - Expiration Month: `AB`
   - Expiration Year: `ABCD`
5. Click Pay and Confirm Order.

### Expected Result

The payment fields should validate the entered values according to the expected input format and prevent order submission when invalid payment data is entered.

### Actual Result

The application accepted numeric input for Name on Card and alphabetic input for Card Number, CVC, Expiration Month, and Expiration Year without displaying format-validation messages. The order was successfully submitted.

### Test Data

| Field | Invalid Input | Result |
|---|---|---|
| Name on Card | `123` | Accepted |
| Card Number | `ABC` | Accepted |
| CVC | `ABC` | Accepted |
| Expiration Month | `AB` | Accepted |
| Expiration Year | `ABCD` | Accepted |

### Evidence

The defect was reproduced during actual test execution.

### Jira
AEMQ-3

---

## 6. Defect Reporting Notes

- Defects were reported only after the relevant test cases were executed.
- The observed behavior was reproduced during testing.
- The defects are documented separately in Jira and linked to their corresponding test cases.
- Severity and priority may be reassessed after business impact and requirements are formally confirmed.
- AEMQ-1, AEMQ-2, and AEMQ-3 are currently awaiting resolution and retesting.
