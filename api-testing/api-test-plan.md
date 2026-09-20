# API Test Plan – Automation Exercise

## 1. Document Information

| Field             | Details                             |
| ----------------- | ----------------------------------- |
| Project           | Automation Exercise – API Testing   |
| Application       | Automation Exercise Web Application |
| Testing Type      | API Testing                         |
| Tester            | Shreya Mandrekar                    |
| Tool              | Postman                             |
| API Documentation | Automation Exercise API List        |
| Test Environment  | Live Application                    |

---

# 2. Objective

The objective of this API testing activity is to verify the functionality, reliability, and response behavior of the APIs provided by the Automation Exercise application.

The testing will focus on validating HTTP methods, status codes, response data, response structure, request parameters, error handling, and other observable API behavior.

---

# 3. Scope

The API testing scope includes:

* Products-related APIs
* User/account-related APIs
* Authentication-related APIs
* Request method validation
* HTTP status code validation
* Response body validation
* Response structure validation
* Response header validation where applicable
* Request parameter validation
* Positive testing
* Negative testing
* Error-response validation
* Basic response-time observation

---

# 4. Out of Scope

The following activities are outside the scope of this testing:

* Performance/load testing
* Stress testing
* Security penetration testing
* Source-code testing
* Server/infrastructure testing
* Automated API testing using programming languages
* Production monitoring

---

# 5. Testing Approach

The APIs will be tested manually using Postman.

The testing process will include:

1. Review the API documentation.
2. Create requests in Postman.
3. Execute valid requests.
4. Validate HTTP status codes.
5. Validate response body and response structure.
6. Validate request parameters where applicable.
7. Execute negative test cases.
8. Record actual results and test status.
9. Investigate unexpected behavior.
10. Create a defect only when a genuine and reproducible issue is identified.
11. Document execution results in GitHub.

---

# 6. Testing Types

The following testing types will be performed where applicable:

* Functional API Testing
* Positive Testing
* Negative Testing
* Validation Testing
* Response Validation
* Error Handling Testing
* Integration-oriented API Testing
* Regression Testing when applicable

---

# 7. API Validation Areas

Each API will be evaluated against applicable validation points:

### Request Validation

* HTTP method
* Endpoint URL
* Query parameters
* Request parameters
* Request headers
* Request body

### Response Validation

* HTTP status code
* Response body
* Response format
* Response fields
* Data types
* Required fields
* Response structure
* Response headers where applicable
* Response time observation

---

# 8. Test Data

Test data will be created based on the requirements and behavior of the API being tested.

Where applicable, the following data will be used:

* Valid product information
* Valid user information
* Invalid or incomplete input
* Valid and invalid parameters
* Valid and invalid credentials
* Unsupported or incorrect request methods

Actual test data and results will be recorded in the respective API execution documents.

---

# 9. Defect Handling

If the actual API behavior differs from the expected behavior:

1. Reproduce the behavior to confirm the issue.
2. Record the actual response accurately.
3. Determine whether the behavior represents a genuine defect or an expected API response.
4. Create a Jira defect if a genuine reproducible defect is identified.
5. Record the defect ID against the relevant test case.
6. Document the defect details in the API defect report.

---

# 10. Test Environment

| Environment      | Details                         |
| ---------------- | ------------------------------- |
| Application      | Automation Exercise             |
| API Tool         | Postman                         |
| Browser          | Google Chrome                   |
| Operating System | Windows 11 Home Single Language |
| OS Version       | 25H2                            |
| Testing Period   | August–September 2026           |

---

# 11. Entry Criteria

API testing can begin when:

* API documentation is available.
* The API endpoint is accessible.
* Postman is available.
* Required test data is available.
* The application/API environment is accessible.

---

# 12. Exit Criteria

API testing for a module can be considered complete when:

* Planned test cases have been executed.
* Actual results have been recorded.
* Test statuses have been recorded.
* Identified defects have been documented.
* Failed test cases have been investigated.
* Required retesting has been performed where applicable.
* Execution results have been committed to GitHub.

---

# 13. Deliverables

The API testing activity will produce:

* API Test Plan
* API Test Scenarios
* API Test Cases
* API Execution Results
* API Defect Reports
* Postman API Collection
* Retesting/Regression Results where applicable

---

# 14. Current API Under Test

The first API selected for execution is the Products List API.

**Method:** GET

**Endpoint:**

`https://www.automationexercise.com/api/productsList`

The initial execution returned HTTP 200 with a JSON response containing product information.

Detailed execution results will be documented separately in the Products API execution file.

---

# 15. Test Execution Notes

* APIs will be tested against the live Automation Exercise application.
* Test results will be based on actual API responses observed during execution.
* HTTP status codes alone will not be treated as sufficient validation.
* Response body and response structure will also be validated.
* Observed behavior will not automatically be classified as a defect without a defined expected behavior or clear API requirement.
* Defects will be reported only when unexpected behavior is reproducible.
* Response time will be recorded as an observation and will not be treated as a performance defect unless a defined performance requirement exists.
