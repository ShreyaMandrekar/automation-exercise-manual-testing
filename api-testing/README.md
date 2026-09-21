# API Testing – Automation Exercise

## 1. Project Overview

This section documents API testing performed on the Automation Exercise web application using Postman.

**Application:** Automation Exercise

**Testing Type:** API Testing

**Tool:** Postman

**Tester:** Shreya Mandrekar

The API testing focused on functional validation, request method validation, parameter validation, response validation, error handling, and response-time observation.

---

## 2. API Modules Tested

| Module         | Endpoint                    | Test Cases | Result |
| -------------- | --------------------------- | ---------: | ------ |
| Products List  | `/api/productsList`         |          4 | 4 PASS |
| Brands List    | `/api/brandsList`           |          4 | 4 PASS |
| Search Product | `/api/searchProduct`        |          6 | 6 PASS |
| User Login     | `/api/verifyLogin`          |          4 | 4 PASS |
| Create Account | `/api/createAccount`        |          4 | 4 PASS |
| Delete Account | `/api/deleteAccount`        |          4 | 4 PASS |
| Update Account | `/api/updateAccount`        |          4 | 4 PASS |
| User Details   | `/api/getUserDetailByEmail` |          4 | 4 PASS |

---

## 3. Testing Coverage

The executed API tests covered:

* Positive API testing
* Negative API testing
* HTTP method validation
* Request parameter validation
* Missing parameter validation
* Invalid credential validation
* Duplicate account validation
* Non-existing user validation
* API response code validation
* HTTP status code validation
* Response message validation
* Response structure validation
* Response data validation
* Unsupported method handling
* Invalid endpoint handling
* Response-time observation

---

## 4. Execution Summary

| Metric             | Result |
| ------------------ | -----: |
| API Modules        |      8 |
| Total Test Cases   |     34 |
| Passed             |     34 |
| Failed             |      0 |
| Blocked            |      0 |
| Not Executed       |      0 |
| Defects Identified |      0 |

**Overall API Testing Status:** PASS

---

## 5. Defect Handling

No genuine API defects were identified during the executed API test cases.

The API returned appropriate responses for the tested valid, invalid, missing-parameter, non-existing-data, and unsupported-method scenarios.

---

## 6. Response-Time Observation

Response times were recorded during execution for observation purposes.

No performance threshold was defined for this project, therefore response-time observations were not treated as performance pass/fail criteria.

---

## 7. Tools and Approach

**Tool:**

* Postman

**Approach:**

* Created API test scenarios based on the available API documentation.
* Created execution templates before execution.
* Executed requests against the live application APIs.
* Validated HTTP status codes and API-level response codes.
* Validated response messages, response structure, and relevant response data.
* Recorded actual results and execution status.
* Documented only observed behavior.
* No defects were reported without reproducible evidence.

---

## 8. Execution Evidence

Individual API execution results are documented in the corresponding module folders:

* `products/products-list-execution.md`
* `brands/brands-list-execution.md`
* `search/search-product-execution.md`
* `login/user-login-execution.md`
* `account/create-account-execution.md`
* `account/delete-account-execution.md`
* `account/update-account-execution.md`
* `account/user-details-execution.md`

---

## 9. Conclusion

The planned API test scenarios were executed using Postman against the Automation Exercise APIs.

The executed test cases successfully validated API functionality, request handling, parameter validation, response codes, response messages, response structure, and relevant response data across the selected API modules.

No genuine API defects were identified during execution.

---
