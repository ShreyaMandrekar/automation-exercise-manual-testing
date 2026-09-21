# Create Account API – Test Case Execution

## 1. Module Information

| Field            | Details                           |
| ---------------- | --------------------------------- |
| Project          | Automation Exercise – API Testing |
| API              | Create/Register User Account      |
| Endpoint         | `/api/createAccount`              |
| HTTP Method      | POST                              |
| Tool             | Postman                           |
| Test Type        | API Testing                       |
| Test Case Status | Executed                          |
| Tester           | Shreya Mandrekar                  |

---

# 2. Objective

To verify the Create Account API functionality, account creation with valid data, required parameter validation, duplicate account handling, and unsupported request method behavior.

---

# 3. Test Cases

## TC-API-ACCOUNT-001 – Verify user account creation with valid details

**Scenario:** TS-API-014

| Field         | Details                                                     |
| ------------- | ----------------------------------------------------------- |
| Test Case ID  | TC-API-ACCOUNT-001                                          |
| Priority      | High                                                        |
| Preconditions | A unique email address is available for account creation.   |
| Test Data     | Valid values for all documented account creation parameters |

**Steps:**

1. Open Postman.
2. Select **POST** method.
3. Enter `https://automationexercise.com/api/createAccount`.
4. Select **Body → x-www-form-urlencoded**.
5. Add all documented account creation parameters with valid test data.
6. Ensure the email address has not already been registered.
7. Click **Send**.
8. Verify the HTTP response and response body.

**Expected Result:**

The API should successfully create the user account and return `responseCode: 201` with the response message **`User created!`**.

**Actual Result:**
The POST request returned HTTP status 200 OK. The response contained responseCode: 201 with the message "User created!". The observed response time was 1.15 seconds.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The Create Account API successfully created the user account and returned the expected response code and confirmation message.

---

## TC-API-ACCOUNT-002 – Verify Create Account API validation for missing required parameter

**Scenario:** TS-API-015

| Field         | Details                                                |
| ------------- | ------------------------------------------------------ |
| Test Case ID  | TC-API-ACCOUNT-002                                     |
| Priority      | High                                                   |
| Preconditions | Create Account API is available.                       |
| Test Data     | Valid account data with one required parameter omitted |

**Steps:**

1. Open Postman.
2. Select **POST** method.
3. Enter `https://automationexercise.com/api/createAccount`.
4. Select **Body → x-www-form-urlencoded**.
5. Add the documented account creation parameters with valid test data.
6. Omit one parameter from the request.
7. Click **Send**.
8. Verify the HTTP response and response body.

**Expected Result:**

The API should reject the incomplete request and return an appropriate error response indicating that the required account information is missing.

**Actual Result:**
The POST request returned HTTP status 200 OK with responseCode: 400. The response message stated Bad request, email parameter is missing in POST request. The observed response time was 1.37 seconds.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The API correctly rejected the account creation request when the required email parameter was omitted and returned the expected 400 response code with an appropriate error message.

---

## TC-API-ACCOUNT-003 – Verify Create Account API handling of duplicate email

**Scenario:** TS-API-015

| Field         | Details                                                         |
| ------------- | --------------------------------------------------------------- |
| Test Case ID  | TC-API-ACCOUNT-003                                              |
| Priority      | High                                                            |
| Preconditions | A user account already exists for the test email address.       |
| Test Data     | Valid account details using an already registered email address |

**Steps:**

1. Open Postman.
2. Select **POST** method.
3. Enter `https://automationexercise.com/api/createAccount`.
4. Select **Body → x-www-form-urlencoded**.
5. Enter valid account creation details.
6. Use an email address that is already registered.
7. Click **Send**.
8. Verify the HTTP response and response body.

**Expected Result:**

The API should reject the duplicate account request and return an appropriate response indicating that the email address is already registered or cannot be used to create another account.

**Actual Result:**
The POST request returned HTTP status 200 OK with responseCode: 400. The response message stated "Email already exists!". The observed response time was 1.85 seconds.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The API correctly rejected the account creation request using an already registered email address and returned the expected 400 response code with an appropriate duplicate-email message.

---

## TC-API-ACCOUNT-004 – Verify Create Account API rejects unsupported GET method

**Scenario:** TS-API-030

| Field         | Details                                        |
| ------------- | ---------------------------------------------- |
| Test Case ID  | TC-API-ACCOUNT-004                             |
| Priority      | Medium                                         |
| Preconditions | Create Account API endpoint is available.      |
| Test Data     | GET request to the Create Account API endpoint |

**Steps:**

1. Open Postman.
2. Select **GET** method.
3. Enter `https://automationexercise.com/api/createAccount`.
4. Do not add request parameters.
5. Click **Send**.
6. Verify the HTTP response and response body.

**Expected Result:**

The API should reject the unsupported GET method and return an appropriate method-not-supported response.

**Actual Result:**
The GET request returned HTTP status 405 Method Not Allowed. No responseCode field was present in the response. The response message stated detail: Method GET not allowed. The observed response time was 1.25 seconds.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The API correctly rejected the unsupported GET method and returned a 405 Method Not Allowed response.

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
| API Endpoint     | `https://automationexercise.com/api/createAccount` |
| Execution Period | Sep 2026                                           |

---

# 6. Execution Notes

* Test cases were executed against the live Automation Exercise API using Postman.
* Actual Results were recorded based on the responses received during execution.
* HTTP status codes, response codes, response messages, account creation behavior, and parameter validation were validated.
* A unique test email was used for the successful account creation test to avoid unintended duplicate-account results.
* No performance threshold was applied; response time was recorded as an observation where relevant.
* No genuine reproducible API defects were identified during execution.
* All four test cases were executed individually and passed.
* Retesting and regression testing will be performed separately if a defect is fixed and a testable fix becomes available.
