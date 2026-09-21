# Update Account API – Test Case Execution

## 1. Module Information

| Field            | Details                           |
| ---------------- | --------------------------------- |
| Project          | Automation Exercise – API Testing |
| API              | Update User Account               |
| Endpoint         | `/api/updateAccount`              |
| HTTP Method      | PUT                               |
| Tool             | Postman                           |
| Test Type        | API Testing                       |
| Test Case Status | Not Executed                      |
| Tester           | Shreya Mandrekar                  |

---

# 2. Objective

To verify the Update User Account API functionality, account data validation, credential handling, and unsupported request method behavior.

---

# 3. Test Cases

## TC-API-UPDATE-001 – Verify successful account update with valid data

**Scenario:** TS-API-017

| Field         | Details                                          |
| ------------- | ------------------------------------------------ |
| Test Case ID  | TC-API-UPDATE-001                                |
| Priority      | High                                             |
| Preconditions | A valid user account exists.                     |
| Test Data     | Valid email/password and updated account details |

**Steps:**

1. Open Postman.
2. Select **PUT** method.
3. Enter `https://automationexercise.com/api/updateAccount`.
4. Select **Body → x-www-form-urlencoded**.
5. Enter the valid account email and password.
6. Enter the required account details.
7. Modify one or more account fields from the existing values.
8. Click **Send**.
9. Verify the HTTP response and response body.

**Expected Result:**

The API should successfully update the user account and return `responseCode: 200` with the response message **`User updated!`**.

**Actual Result:**
The PUT request returned HTTP status 200 OK with responseCode: 200. The response message was User updated!. The account update was successfully processed using valid account credentials and updated account data. The observed response time was 2.06 seconds.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The API successfully updated the user account and returned the expected successful response.

---

## TC-API-UPDATE-002 – Verify Update Account API validation when a required parameter is missing

**Scenario:** TS-API-018

| Field         | Details                                                |
| ------------- | ------------------------------------------------------ |
| Test Case ID  | TC-API-UPDATE-002                                      |
| Priority      | High                                                   |
| Preconditions | A valid user account exists.                           |
| Test Data     | Valid account data with one required parameter omitted |

**Steps:**

1. Open Postman.
2. Select **PUT** method.
3. Enter `https://automationexercise.com/api/updateAccount`.
4. Select **Body → x-www-form-urlencoded**.
5. Enter valid account data.
6. Omit one required parameter.
7. Click **Send**.
8. Verify the HTTP response and response body.

**Expected Result:**

The API should reject the request because a required parameter is missing and return an appropriate error response.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-API-UPDATE-003 – Verify Update Account API rejects invalid account credentials

**Scenario:** TS-API-018

| Field         | Details                                                |
| ------------- | ------------------------------------------------------ |
| Test Case ID  | TC-API-UPDATE-003                                      |
| Priority      | High                                                   |
| Preconditions | A valid user account exists and must remain unchanged. |
| Test Data     | Invalid email and/or password                          |

**Steps:**

1. Open Postman.
2. Select **PUT** method.
3. Enter `https://automationexercise.com/api/updateAccount`.
4. Select **Body → x-www-form-urlencoded**.
5. Enter invalid account credentials.
6. Enter otherwise valid update data.
7. Click **Send**.
8. Verify the HTTP response and response body.
9. Verify that the valid account was not incorrectly modified.

**Expected Result:**

The API should reject the invalid credentials and should not update the existing account.

**Actual Result:**

**Status:**

**Defect ID:**

**Comments:**

---

## TC-API-UPDATE-004 – Verify Update Account API rejects unsupported GET method

**Scenario:** TS-API-030

| Field         | Details                                        |
| ------------- | ---------------------------------------------- |
| Test Case ID  | TC-API-UPDATE-004                              |
| Priority      | Medium                                         |
| Preconditions | Update Account API endpoint is available.      |
| Test Data     | GET request to the Update Account API endpoint |

**Steps:**

1. Open Postman.
2. Select **GET** method.
3. Enter `https://automationexercise.com/api/updateAccount`.
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
| API Endpoint     | `https://automationexercise.com/api/updateAccount` |
| Execution Period | Sep 2026                                           |

---

# 6. Execution Notes

* Test cases will be executed against the live Automation Exercise API using Postman.
* Actual Results will be recorded based on the responses received during execution.
* HTTP status codes, response codes, response messages, account credentials, required parameter validation, account update behavior, and unsupported method handling will be validated.
* The existing active test account will be used for the account update testing.
* Negative test cases will be executed without making unintended changes to the valid test account.
* Response time will be recorded as an observation; no performance threshold will be applied.
* Any defect will be documented only if an actual reproducible deviation from the expected behavior is observed.
* Retesting and regression testing will be performed separately if a defect is fixed and a testable fix becomes available.
