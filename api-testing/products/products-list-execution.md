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

To verify the Products List API functionality, response structure, product data, and handling of unsupported request methods.

---

# 3. Test Cases

## TC-API-PRODUCTS-001 – Verify Products List API returns successful response with valid product data

**Scenario:** TS-API-001

| Field         | Details                                  |
| ------------- | ---------------------------------------- |
| Test Case ID  | TC-API-PRODUCTS-001                      |
| Priority      | High                                     |
| Preconditions | Products List API endpoint is accessible |
| Test Data     | Valid GET request to `/api/productsList` |

**Steps:**

1. Open Postman.
2. Open the `Automation Exercise – API Testing` collection.
3. Send a GET request to `/api/productsList`.
4. Observe the HTTP response.
5. Verify the response body.
6. Verify the `responseCode` field.
7. Verify that the `products` collection is present.
8. Verify that product records contain applicable product information.

**Expected Result:**

The API should successfully process the GET request and return the expected Products List response with HTTP 200, a successful `responseCode`, a `products` collection, and applicable product information.

**Actual Result:**
The GET request was successfully processed with HTTP status 200 OK. The response contained responseCode: 200, the products collection was present, and product records contained the expected product information. The observed response time was 1.23 seconds.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The Products List API returned the expected successful response and product data.

---

## TC-API-PRODUCTS-002 – Verify Products List API product data structure

**Scenario:** TS-API-003

| Field         | Details                                   |
| ------------- | ----------------------------------------- |
| Test Case ID  | TC-API-PRODUCTS-002                       |
| Priority      | High                                      |
| Preconditions | Products List API returns product records |
| Test Data     | Valid GET request to `/api/productsList`  |

**Steps:**

1. Send a GET request to `/api/productsList`.
2. Open the `products` collection in the response.
3. Inspect multiple product records.
4. Verify the applicable product fields and their values.
5. Check whether product IDs are unique.

**Expected Result:**

Returned product records should have the expected data structure, including applicable fields such as ID, name, price, brand, and category. Product IDs should be unique.

**Actual Result:**
Multiple product records were present in the products collection. The product records contained applicable fields including id, name, price, brand, user_type, and category. A total of 43 product records were observed, and the product IDs were unique.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The product data structure and applicable product fields were present as expected.

---

## TC-API-PRODUCTS-003 – Verify Products List API rejects unsupported POST method

**Scenario:** TS-API-002

| Field         | Details                                  |
| ------------- | ---------------------------------------- |
| Test Case ID  | TC-API-PRODUCTS-003                      |
| Priority      | Medium                                   |
| Preconditions | Products List API endpoint is accessible |
| Test Data     | POST request to `/api/productsList`      |

**Steps:**

1. Open the Products List API request in Postman.
2. Change the HTTP method from GET to POST.
3. Send the request.
4. Observe the HTTP response and response body.

**Expected Result:**

The API should reject the unsupported POST method and return the documented response for the unsupported request method.

**Actual Result:**

...

**Status:**

...

**Defect ID:**

...

**Comments:**

...

---

## TC-API-PRODUCTS-004 – Verify Products List API response behavior for invalid request

**Scenario:** TS-API-030

| Field         | Details                                         |
| ------------- | ----------------------------------------------- |
| Test Case ID  | TC-API-PRODUCTS-004                             |
| Priority      | Medium                                          |
| Preconditions | Products List API endpoint is accessible        |
| Test Data     | Invalid request condition applicable to the API |

**Steps:**

1. Prepare an invalid request condition applicable to the Products List API.
2. Send the request.
3. Observe the HTTP response.
4. Review the response body.

**Expected Result:**

The API should handle the invalid request appropriately and return a meaningful error response according to its documented behavior.

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
| Total Test Cases   | 4      |
| Passed             | 0      |
| Failed             | 0      |
| Blocked            | 0      |
| Not Executed       | 4      |
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
* Actual Results will be recorded based on the API response observed in Postman.
* HTTP status codes, response body, response structure, and applicable response data will be validated.
* Response time may be recorded as an observation during execution.
* No performance threshold is defined for this project.
* Defect IDs will be added only when genuine reproducible defects are identified.
* Test cases will be executed individually and updated after execution.
* Retesting and regression testing will be documented separately if defects are identified and subsequently fixed.
