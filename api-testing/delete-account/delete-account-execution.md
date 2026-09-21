# Delete Account API – Test Case Execution

## 1. Module Information

| Field            | Details                           |
| ---------------- | --------------------------------- |
| Project          | Automation Exercise – API Testing |
| API              | Delete User Account               |
| Endpoint         | `/api/deleteAccount`              |
| HTTP Method      | DELETE                            |
| Tool             | Postman                           |
| Test Type        | API Testing                       |
| Test Case Status | Not Executed                      |
| Tester           | Shreya Mandrekar                  |

---

# 2. Objective

To verify the Delete User Account API functionality, credential validation, required parameter handling, unsupported request method behavior, and successful deletion of a user account.

---

# 3. Test Cases

## TC-API-DELETE-001 – Verify Delete Account API validation when email parameter is missing

**Scenario:** TS-API-021, TS-API-024

| Field         | Details                                |
| ------------- | -------------------------------------- |
| Test Case ID  | TC-API-DELETE-001                      |
| Priority      | High                                   |
| Preconditions | A valid user account exists.           |
| Test Data     | Valid password without email parameter |

**Steps:**

1. Open Postman.
2. Select **DELETE** method.
3. Enter `https://automationexercise.com/api/deleteAccount`.
4. Select **Body → x-www-form-urlencoded** if required by the API.
5. Add the `password` parameter with the valid account password.
6. Do not add the `email` parameter.
7. Click **Send**.
8. Verify the HTTP response and response body.

**Expected Result:**

The API should reject the request because the required email parameter is missing and return an appropriate error response.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-API-DELETE-002 – Verify Delete Account API rejects invalid credentials

**Scenario:** TS-API-021

| Field         | Details                                                                |
| ------------- | ---------------------------------------------------------------------- |
| Test Case ID  | TC-API-DELETE-002                                                      |
| Priority      | High                                                                   |
| Preconditions | A valid user account exists and must remain available after this test. |
| Test Data     | Invalid email and/or password                                          |

**Steps:**

1. Open Postman.
2. Select **DELETE** method.
3. Enter `https://automationexercise.com/api/deleteAccount`.
4. Select **Body → x-www-form-urlencoded** if required by the API.
5. Add an invalid email address.
6. Add an invalid password.
7. Click **Send**.
8. Verify the HTTP response and response body.
9. Verify that the existing test account has not been deleted.

**Expected Result:**

The API should reject the invalid credentials and should not delete the existing user account.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-API-DELETE-003 – Verify Delete Account API rejects unsupported GET method

**Scenario:** TS-API-030

| Field         | Details                                        |
| ------------- | ---------------------------------------------- |
| Test Case ID  | TC-API-DELETE-003                              |
| Priority      | Medium                                         |
| Preconditions | Delete Account API endpoint is available.      |
| Test Data     | GET request to the Delete Account API endpoint |

**Steps:**

1. Open Postman.
2. Select **GET** method.
3. Enter `https://automationexercise.com/api/deleteAccount`.
4. Do not add request parameters.
5. Click **Send**.
6. Verify the HTTP response and response body.

**Expected Result:**

The API should reject the unsupported GET method and return an appropriate method-not-supported response.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-API-DELETE-004 – Verify successful user account deletion with valid credentials

**Scenario:** TS-API-020

| Field         | Details                                                                    |
| ------------- | -------------------------------------------------------------------------- |
| Test Case ID  | TC-API-DELETE-004                                                          |
| Priority      | High                                                                       |
| Preconditions | A dedicated test account exists and is no longer required after this test. |
| Test Data     | Valid registered email and password                                        |

**Steps:**

1. Open Postman.
2. Select **DELETE** method.
3. Enter `https://automationexercise.com/api/deleteAccount`.
4. Select **Body → x-www-form-urlencoded** if required by the API.
5. Add the registered `email`.
6. Add the corresponding `password`.
7. Click **Send**.
8. Verify the HTTP response and response body.
9. Verify that the account can no longer be used as an active account after deletion.

**Expected Result:**

The API should successfully delete the user account and return `responseCode: 200` with the response message **`Account deleted!`**.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

# 4. Execution Summary

| Metric           | Count        |
| ---------------- | ------------ |
| Total Test Cases | 4            |
| Passed           | 0            |
| Failed           | 0            |
| Blocked          | 0            |
| Not Executed     | 4            |
| Defects          | 0            |
| Overall Status   | NOT EXECUTED |

---

# 5. Test Environment

| Field            | Details                                            |
| ---------------- | -------------------------------------------------- |
| Tool             | Postman                                            |
| Application      | Automation Exercise                                |
| API Endpoint     | `https://automationexercise.com/api/deleteAccount` |
| Execution Period | Sep 2026                                           |

---

# 6. Execution Notes

* Test cases will be executed against the live Automation Exercise API using Postman.
* Actual Results will be recorded based on the responses received during execution.
* HTTP status codes, response codes, response messages, credential validation, parameter validation, and account deletion behavior will be validated.
* The dedicated test account created during the Create Account API testing will be retained until the final successful deletion test.
* Negative test cases will be executed before the successful deletion test so that the test account remains available.
* TC-API-DELETE-004 will be executed last because successful execution permanently deletes the test account.
* No performance threshold will be applied; response time will only be recorded as an observation where relevant.
* Any defect will be documented only if an actual reproducible deviation from the expected behavior is observed.
* Retesting and regression testing will be performed separately if a defect is fixed and a testable fix becomes available.
