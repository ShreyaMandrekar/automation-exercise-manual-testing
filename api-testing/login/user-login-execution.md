# User Login API – Test Case Execution

## 1. Module Information

| Field            | Details                           |
| ---------------- | --------------------------------- |
| Project          | Automation Exercise – API Testing |
| API              | User Login                        |
| Endpoint         | `/api/verifyLogin`                |
| HTTP Method      | POST                              |
| Tool             | Postman                           |
| Test Type        | API Testing                       |
| Test Case Status | Executed                          |
| Tester           | Shreya Mandrekar                  |

---

# 2. Objective

To verify the User Login API functionality, credential validation, required parameter handling, and unsupported request method behavior.

---

# 3. Test Cases

## TC-API-LOGIN-001 – Verify User Login API with valid credentials

**Scenario:** TS-API-010, TS-API-013

| Field         | Details                                       |
| ------------- | --------------------------------------------- |
| Test Case ID  | TC-API-LOGIN-001                              |
| Priority      | High                                          |
| Preconditions | A valid registered user account is available. |
| Test Data     | Valid registered email and password           |

**Steps:**

1. Open Postman.
2. Select **POST** method.
3. Enter `https://automationexercise.com/api/verifyLogin`.
4. Select **Body → x-www-form-urlencoded**.
5. Add parameter `email` with valid registered email.
6. Add parameter `password` with valid password.
7. Click **Send**.
8. Verify the HTTP response and response body.

**Expected Result:**

The API should return HTTP status **200 OK** with `responseCode: 200` and the response message should be **`User exists!`**.

**Actual Result:**
The POST request was successfully processed with HTTP status 200 OK. The response contained responseCode: 200 with the message "User exists!". The observed response time was 1.20 seconds.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The User Login API successfully verified the valid registered credentials and returned the expected response.

---

## TC-API-LOGIN-002 – Verify User Login API rejects invalid credentials

**Scenario:** TS-API-011

| Field         | Details                       |
| ------------- | ----------------------------- |
| Test Case ID  | TC-API-LOGIN-002              |
| Priority      | High                          |
| Preconditions | User Login API is available.  |
| Test Data     | Invalid email and/or password |

**Steps:**

1. Open Postman.
2. Select **POST** method.
3. Enter `https://automationexercise.com/api/verifyLogin`.
4. Select **Body → x-www-form-urlencoded**.
5. Add `email` with invalid login details.
6. Add `password` with invalid login details.
7. Click **Send**.
8. Verify the HTTP response and response body.

**Expected Result:**

The API should return HTTP status **200 OK** with `responseCode: 404` and the response message should be **`User not found!`**.

**Actual Result:**
The POST request returned HTTP status 404 Not Found. The response contained responseCode: 404 with the message "User not found!". The observed response time was 1.12 seconds.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The API correctly rejected the invalid login credentials and returned the expected User not found! response.

---

## TC-API-LOGIN-003 – Verify User Login API validation when email parameter is missing

**Scenario:** TS-API-012

| Field         | Details                                |
| ------------- | -------------------------------------- |
| Test Case ID  | TC-API-LOGIN-003                       |
| Priority      | High                                   |
| Preconditions | User Login API is available.           |
| Test Data     | Valid password without email parameter |

**Steps:**

1. Open Postman.
2. Select **POST** method.
3. Enter `https://automationexercise.com/api/verifyLogin`.
4. Select **Body → x-www-form-urlencoded**.
5. Add only the `password` parameter with a valid password.
6. Do not add the `email` parameter.
7. Click **Send**.
8. Verify the HTTP response and response body.

**Expected Result:**

The API should return HTTP status **200 OK** with `responseCode: 400` and the response message should be **`Bad request, email or password parameter is missing in POST request.`**

**Actual Result:**
The POST request returned HTTP status 200 OK with responseCode: 400. The response message stated "Bad Request, email or password parameter is missing in POST request". The observed response time was 1.33 seconds.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The API correctly handled the missing email parameter and returned the expected 400 response code with an appropriate error message.

---

## TC-API-LOGIN-004 – Verify User Login API rejects unsupported DELETE method

**Scenario:** TS-API-013

| Field         | Details                                       |
| ------------- | --------------------------------------------- |
| Test Case ID  | TC-API-LOGIN-004                              |
| Priority      | Medium                                        |
| Preconditions | User Login API endpoint is available.         |
| Test Data     | DELETE request to the User Login API endpoint |

**Steps:**

1. Open Postman.
2. Select **DELETE** method.
3. Enter `https://automationexercise.com/api/verifyLogin`.
4. Do not add request parameters.
5. Click **Send**.
6. Verify the HTTP response and response body.

**Expected Result:**

The API should return HTTP status **200 OK** with `responseCode: 405` and the response message should be **`This request method is not supported.`**

**Actual Result:**
The DELETE request returned HTTP status 200 OK with responseCode: 405. The response message stated This request method is not supported. The observed response time was 1.34 seconds.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The API correctly rejected the unsupported DELETE method and returned the expected 405 response code with the appropriate message.

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

| Field            | Details                                          |
| ---------------- | ------------------------------------------------ |
| Tool             | Postman                                          |
| Application      | Automation Exercise                              |
| API Endpoint     | `https://automationexercise.com/api/verifyLogin` |
| Execution Period | Aug–Sep 2026                                     |

---

# 6. Execution Notes

* Test cases were executed against the live Automation Exercise API using Postman.
* Actual Results were recorded from the responses received during execution.
* HTTP status codes, response codes, response messages, and login behavior were validated.
* No performance threshold was applied; response time was recorded as an observation.
* No genuine reproducible API defects were identified.
* All four test cases passed.
