# Products List API – Test Case Execution

## 1. Module Information

| Field            | Details                           |
| ---------------- | --------------------------------- |
| Project          | Automation Exercise – API Testing |
| API              | Products List                     |
| Endpoint         | `/api/productsList`               |
| HTTP Method      | GET                               |
| Tool             | Postman                           |
| Test Type        | API Testing                       |
| Test Case Status | Not Executed                      |
| Tester           | Shreya Mandrekar                  |

---

# 2. Objective

To verify the functionality, response status, response structure, product data, request method handling, and error behavior of the Products List API.

---

# 3. Test Cases

## TC-API-PRODUCTS-001 – Verify Products List API with valid GET request

**Scenario:** TS-API-001

| Field         | Details                                  |
| ------------- | ---------------------------------------- |
| Test Case ID  | TC-API-PRODUCTS-001                      |
| Priority      | High                                     |
| Preconditions | Products List API endpoint is accessible |
| Test Data     | GET request to `/api/productsList`       |

**Steps:**

1. Open Postman.
2. Open the `Automation Exercise – API Testing` collection.
3. Select the Products List API request.
4. Set the HTTP method to GET.
5. Send the request.
6. Observe the response.

**Expected Result:**

The API should accept the GET request and return the expected Products List response.

**Actual Result:**

The GET request was successfully processed. The API returned HTTP 200 OK with a JSON response containing the products collection. The response was received in 1.79 seconds.

**Status:**

PASS

**Defect ID:**

N/A

**Comments:**

Valid GET request successfully returned the Products List response. No defect observed.

---

## TC-API-PRODUCTS-002 – Verify Products List API HTTP status code

**Scenario:** TS-API-001

| Field         | Details                         |
| ------------- | ------------------------------- |
| Test Case ID  | TC-API-PRODUCTS-002             |
| Priority      | High                            |
| Preconditions | Products List API is accessible |
| Test Data     | Valid GET request               |

**Steps:**

1. Send a valid GET request to `/api/productsList`.
2. Observe the HTTP response status code.

**Expected Result:**

The API should return the expected successful HTTP status code for a valid request.

**Actual Result:**

...

**Status:**

...

**Defect ID:**

...

**Comments:**

...

---

## TC-API-PRODUCTS-003 – Verify Products List API response code

**Scenario:** TS-API-003

| Field         | Details                         |
| ------------- | ------------------------------- |
| Test Case ID  | TC-API-PRODUCTS-003             |
| Priority      | High                            |
| Preconditions | Products List API is accessible |
| Test Data     | Valid GET request               |

**Steps:**

1. Send a valid GET request to `/api/productsList`.
2. Open the response body.
3. Locate the `responseCode` field.
4. Verify its value.

**Expected Result:**

The response should contain the expected `responseCode` value for a successful request.

**Actual Result:**

...

**Status:**

...

**Defect ID:**

...

**Comments:**

...

---

## TC-API-PRODUCTS-004 – Verify Products List API response format

**Scenario:** TS-API-003

| Field         | Details                         |
| ------------- | ------------------------------- |
| Test Case ID  | TC-API-PRODUCTS-004             |
| Priority      | High                            |
| Preconditions | Products List API is accessible |
| Test Data     | Valid GET request               |

**Steps:**

1. Send a valid GET request to `/api/productsList`.
2. Observe the response body.
3. Verify that the response is returned in JSON format.

**Expected Result:**

The API should return the response in the expected JSON format.

**Actual Result:**

...

**Status:**

...

**Defect ID:**

...

**Comments:**

...

---

## TC-API-PRODUCTS-005 – Verify Products List API returns products collection

**Scenario:** TS-API-003

| Field         | Details                         |
| ------------- | ------------------------------- |
| Test Case ID  | TC-API-PRODUCTS-005             |
| Priority      | High                            |
| Preconditions | Products List API is accessible |
| Test Data     | Valid GET request               |

**Steps:**

1. Send a valid GET request to `/api/productsList`.
2. Open the response body.
3. Locate the `products` field.
4. Verify that product records are returned.

**Expected Result:**

The response should contain a `products` collection containing product records.

**Actual Result:**

...

**Status:**

...

**Defect ID:**

...

**Comments:**

...

---

## TC-API-PRODUCTS-006 – Verify product records contain expected fields

**Scenario:** TS-API-003

| Field         | Details                                   |
| ------------- | ----------------------------------------- |
| Test Case ID  | TC-API-PRODUCTS-006                       |
| Priority      | High                                      |
| Preconditions | Products List API returns product records |
| Test Data     | Valid GET request                         |

**Steps:**

1. Send a valid GET request to `/api/productsList`.
2. Open the `products` collection.
3. Inspect multiple product records.
4. Verify the applicable product fields.

**Expected Result:**

Product records should contain the expected product information such as ID, name, price, brand, and category.

**Actual Result:**

...

**Status:**

...

**Defect ID:**

...

**Comments:**

...

---

## TC-API-PRODUCTS-007 – Verify product IDs are unique

**Scenario:** TS-API-003

| Field         | Details                                            |
| ------------- | -------------------------------------------------- |
| Test Case ID  | TC-API-PRODUCTS-007                                |
| Priority      | Medium                                             |
| Preconditions | Products List API returns multiple product records |
| Test Data     | Valid GET request                                  |

**Steps:**

1. Send a valid GET request to `/api/productsList`.
2. Review the `id` value of each returned product.
3. Compare the IDs for duplicate values.

**Expected Result:**

Each returned product should have a unique product ID.

**Actual Result:**

...

**Status:**

...

**Defect ID:**

...

**Comments:**

...

---

## TC-API-PRODUCTS-008 – Verify Products List API response time

**Scenario:** TS-API-032

| Field         | Details                         |
| ------------- | ------------------------------- |
| Test Case ID  | TC-API-PRODUCTS-008             |
| Priority      | Low                             |
| Preconditions | Products List API is accessible |
| Test Data     | Valid GET request               |

**Steps:**

1. Send a valid GET request to `/api/productsList`.
2. Observe the response time displayed by Postman.

**Expected Result:**

The API should return a response successfully and the observed response time should be recorded.

**Actual Result:**

...

**Status:**

...

**Defect ID:**

...

**Comments:**

No performance threshold is defined for this project. Response time is recorded as an observation only.

---

## TC-API-PRODUCTS-009 – Verify Products List API behavior for unsupported POST method

**Scenario:** TS-API-002

| Field         | Details                                  |
| ------------- | ---------------------------------------- |
| Test Case ID  | TC-API-PRODUCTS-009                      |
| Priority      | Medium                                   |
| Preconditions | Products List API endpoint is accessible |
| Test Data     | POST request to `/api/productsList`      |

**Steps:**

1. Open the Products List API request in Postman.
2. Change the HTTP method from GET to POST.
3. Send the request.
4. Observe the response.

**Expected Result:**

The API should reject the unsupported POST method and return the documented response for an unsupported method.

**Actual Result:**

...

**Status:**

...

**Defect ID:**

...

**Comments:**

...

---

# 4. Execution Summary

| Metric             | Result |
| ------------------ | ------ |
| Total Test Cases   | 9      |
| Passed             | 0      |
| Failed             | 0      |
| Blocked            | 0      |
| Not Executed       | 9      |
| Defects Identified | 0      |

**Overall Result:** NOT EXECUTED

---

# 5. Test Environment

| Environment      | Details                         |
| ---------------- | ------------------------------- |
| Application      | Automation Exercise             |
| API Tool         | Postman                         |
| Browser          | Google Chrome                   |
| Operating System | Windows 11 Home Single Language |
| OS Version       | 25H2                            |
| Testing Period   | August–September 2026           |

---

# 6. Execution Notes

* Test cases will be executed against the live Automation Exercise API.
* Actual Results will be recorded based on the response observed in Postman.
* HTTP status codes, response body, response structure, and applicable response data will be validated.
* Response time will be recorded as an observation where applicable.
* Defect IDs will be added only when genuine reproducible defects are identified.
* Test cases will be executed individually and updated after execution.
* Retesting and regression testing will be documented separately if defects are identified and subsequently fixed.
