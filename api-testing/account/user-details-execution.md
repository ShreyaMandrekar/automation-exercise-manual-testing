# User Details API – Test Case Execution

## 1. Module Information

| Field            | Details                           |
| ---------------- | --------------------------------- |
| Project          | Automation Exercise – API Testing |
| API Module       | User Details                      |
| Endpoint         | `/api/getUserDetailByEmail`       |
| HTTP Method      | GET                               |
| Tool             | Postman                           |
| Tester           | Shreya Mandrekar                  |
| Execution Status | Not Executed                      |

---

# 2. Test Cases

## TC-API-DETAILS-001 – Retrieve user details with valid email

**Scenario:** TS-API-023

| Field         | Details                                        |
| ------------- | ---------------------------------------------- |
| Test Case ID  | TC-API-DETAILS-001                             |
| Priority      | High                                           |
| Preconditions | A valid user account exists                    |
| Test Data     | Valid email address of the active test account |

**Request:**

```text
GET https://www.automationexercise.com/api/getUserDetailByEmail
```

**Parameter:**

```text
email = <valid registered email>
```

**Expected Result:**

The API should successfully retrieve the user details for the provided email. The response should contain `responseCode: 200` and the user details in the response body.

**Actual Result:**
The GET request was successfully processed with HTTP status 200 OK. The response contained responseCode: 200 and a user object with the expected user details, including ID, name, email, title, date of birth, address, country, state, city, and zipcode. The observed response time was 1.67 seconds.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The User Details API successfully retrieved the user details for the valid registered email address.

---

## TC-API-DETAILS-002 – Validate missing email parameter

**Scenario:** TS-API-024

| Field         | Details                 |
| ------------- | ----------------------- |
| Test Case ID  | TC-API-DETAILS-002      |
| Priority      | High                    |
| Preconditions | None                    |
| Test Data     | Email parameter omitted |

**Request:**

```text
GET https://www.automationexercise.com/api/getUserDetailByEmail
```

**Expected Result:**

The API should return an appropriate error response indicating that the required email parameter is missing.

**Actual Result:**
The GET request was processed with HTTP status 200 OK. The response contained responseCode: 400 with the message “Bad Request, email parameter is missing in GET request.” The observed response time was 6.66 seconds.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The API correctly returned a validation response when the required email parameter was omitted.

---

## TC-API-DETAILS-003 – Validate non-existing email

**Scenario:** TS-API-024

| Field         | Details                    |
| ------------- | -------------------------- |
| Test Case ID  | TC-API-DETAILS-003         |
| Priority      | Medium                     |
| Preconditions | None                       |
| Test Data     | Non-existing email address |

**Request:**

```text
GET https://www.automationexercise.com/api/getUserDetailByEmail
```

**Parameter:**

```text
email = nonexistent_test_user_999@example.com
```

**Expected Result:**

The API should return an appropriate response indicating that no user account exists for the provided email.

**Actual Result:**
The GET request was processed with HTTP status 200 OK. The response contained responseCode: 404 with the message “Account not found with this email, try another email.” The observed response time was 15.92 seconds.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The API correctly returned a not-found response when a non-existing email address was provided.

---

## TC-API-DETAILS-004 – Reject unsupported POST method

**Scenario:** TS-API-030

| Field         | Details                                   |
| ------------- | ----------------------------------------- |
| Test Case ID  | TC-API-DETAILS-004                        |
| Priority      | Medium                                    |
| Preconditions | None                                      |
| Test Data     | POST request to the User Details endpoint |

**Request:**

```text
POST https://www.automationexercise.com/api/getUserDetailByEmail
```

**Expected Result:**

The API should reject the unsupported HTTP method and return an appropriate method-not-allowed response.

**Actual Result:**
The POST request was processed with HTTP status 200 OK. The response contained responseCode: 405 with the message “This request method is not supported.” The observed response time was 11.23 seconds.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The API correctly rejected the unsupported POST method and returned the expected method-not-supported response.

---

# 3. Execution Summary

| Metric           | Count |
| ---------------- | ----- |
| Total Test Cases | 4     |
| Passed           | 0     |
| Failed           | 0     |
| Blocked          | 0     |
| Not Executed     | 4     |
| Defects          | 0     |

**Overall Status:** Not Executed

---

# 4. Execution Notes

* Test execution will be performed using Postman.
* Actual results will be recorded based on the live API response.
* HTTP status code, `responseCode`, response message, response structure, and relevant user data will be validated.
* Any defect will be recorded only if the observed behavior does not meet the expected result.
* Response time will be observed and recorded where relevant; no performance threshold is defined for this project.
* After execution, the summary and execution status will be updated.

---
