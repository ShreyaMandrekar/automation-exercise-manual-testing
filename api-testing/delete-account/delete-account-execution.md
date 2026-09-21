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
| Test Case Status | Executed                          |
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
The DELETE request returned HTTP status 200 OK with responseCode: 400. The response message stated Bad request, email parameter is missing in delete request. The request contained the valid password but did not include the required email parameter. The observed response time was 902 ms.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The API correctly rejected the request because the required email parameter was missing, and the test account remained available for subsequent test cases.

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
The DELETE request returned HTTP status 200 OK with responseCode: 404. The response message displayed Account not found. The request used invalid credentials, and the observed response time was 1.16 seconds.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The API correctly rejected the invalid credentials and returned an account-not-found response. The valid test account remained available for subsequent test cases.

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
The GET request returned HTTP status 405 Method Not Allowed. No responseCode field was present in the response. The response detail stated Method GET not allowed. The observed response time was 545 ms.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The API correctly rejected the unsupported GET method and returned a 405 Method Not Allowed response.

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
The DELETE request returned HTTP status 200 OK with responseCode: 200. The response message was Account deleted!. The observed response time was 952 ms.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The user account was successfully deleted using valid credentials, and the API returned the expected successful deletion response.

---

# 4. Execution Summary

| Metric           | Count        |
| ---------------- | ------------ |
| Total Test Cases | 4            |
| Passed           | 4            |
| Failed           | 0            |
| Blocked          | 0            |
| Not Executed     | 0            |
| Defects          | 0            |
| Overall Status   | PASS         |

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

- Test cases were executed against the live Automation Exercise API using Postman.
- Actual Results were recorded based on the responses received during execution.
- HTTP status codes, response codes, response messages, credential validation, required parameter handling, unsupported method behavior, and account deletion behavior were validated.
- The dedicated test account created during the Create Account API testing was retained until the final successful deletion test.
- Negative test cases were executed before the successful deletion test so that the test account remained available.
- TC-API-DELETE-004 was executed last because successful execution permanently deleted the test account.
- Response time was recorded as an observation; no performance threshold was applied.
- No genuine reproducible API defects were identified during execution.
- All four test cases were executed individually and passed.
- Retesting and regression testing will be performed separately if a defect is fixed and a testable fix becomes available.
