# Retesting and Regression

## 1. Document Information

| Field | Details |
|---|---|
| Project | Automation Exercise - Manual QA |
| Module | Registration, Cart & Checkout |
| Application | Automation Exercise |
| Defect Tracking Tool | Jira |
| Defects Pending Retest | 3 |

---

## 2. Retesting Summary

| Defect ID | Related Test Case | Defect | Current Status | Retest Status |
|---|---|---|---|---|
| AEMQ-1 | TC-REG-021 | Zipcode field accepts invalid input formats without validation | Open | Pending |
| AEMQ-2 | TC-REG-022 | Mobile Number field accepts invalid formats without validation | Open | Pending |
| AEMQ-3 | TC-CART-028 | Payment fields accept invalid input formats | Open | Pending |

The identified defects have been documented in Jira but have not yet been fixed. Therefore, retesting has not been performed.

---

## 3. Retesting Approach

After a defect is marked as fixed:

1. Review the developer's fix or Jira update.
2. Execute the original failed test case again.
3. Verify that the expected behavior is now achieved.
4. Record the actual result.
5. Mark the test case as PASS if the defect is resolved.
6. Mark the test case as FAIL if the issue still occurs.
7. Update the corresponding Jira defect status based on the retest result.

---

## 4. AEMQ-1 Retesting

### Defect
Zipcode field accepts invalid input formats without validation.

### Related Test Case
TC-REG-021

### Jira Defect
AEMQ-1

### Current Status
Open

### Retest Status
Pending

### Retest Result
Not yet executed because the defect has not been confirmed as fixed.

### Regression Scope

After AEMQ-1 is fixed, related registration functionality should be checked, including:

- Zipcode mandatory-field validation
- Valid zipcode acceptance
- Address information submission
- Successful account creation
- Other registration form validations

---

## 5. AEMQ-2 Retesting

### Defect
Mobile Number field accepts invalid formats without validation.

### Related Test Case
TC-REG-022

### Jira Defect
AEMQ-2

### Current Status
Open

### Retest Status
Pending

### Retest Result
Not yet executed because the defect has not been confirmed as fixed.

### Regression Scope

After AEMQ-2 is fixed, related registration functionality should be checked, including:

- Mobile Number mandatory-field validation
- Valid mobile number acceptance
- Invalid mobile number format validation
- Successful account creation
- Other registration form validations

---

## 6. AEMQ-3 Retesting

### Defect
Payment fields accept invalid input formats.

### Related Test Case
TC-CART-028

### Jira Defect
AEMQ-3

### Current Status
Open

### Retest Status
Pending

### Retest Result
Not yet executed because the defect has not been confirmed as fixed.

### Regression Scope

After AEMQ-3 is fixed, related Cart & Checkout functionality should be checked, including:

- Payment field mandatory validation
- Valid payment data acceptance
- Invalid payment format validation
- Successful order placement
- Order confirmation
- Invoice download
- Cart state after successful order placement

---

## 7. Regression Testing Status

Regression testing for the Registration and Cart & Checkout modules has not yet been performed specifically after defect fixes because AEMQ-1, AEMQ-2, and AEMQ-3 remain open.

Regression testing will be performed after the relevant fixes are available.

---

## 8. Notes

- Retesting will use the original failed test cases whenever possible.
- A defect will not be marked as resolved without successful retesting.
- Regression testing will focus on functionality potentially affected by the defect fixes.
- No retest or regression result has been fabricated or assumed.
