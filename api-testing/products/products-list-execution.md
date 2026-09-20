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
| Test Case Status | Executed                          |
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
The POST request returned HTTP status 200 OK with responseCode: 405. The response message displayed “This request method is not supported.” The observed response time was 1.62 seconds.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The API correctly rejected the unsupported POST method and returned the expected method-not-supported response.

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
The GET request to the invalid endpoint returned HTTP status 404 Not Found. No responseCode field was present in the response. The response body contained HTML error-page content. The observed response time was 1.41 seconds.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The API correctly handled the invalid endpoint by returning a 404 Not Found response.

---

# 4. Execution Summary

| Metric             | Result |
| ------------------ | ------ |
| Total Test Cases   | 4      |
| Passed             | 4      |
| Failed             | 0      |
| Blocked            | 0      |
| Not Executed       | 0      |
| Defects Identified | 0      |

**Overall Result:**: PASS

All 4 Products List API test cases were executed against the live Automation Exercise API. All test cases passed, and no genuine reproducible defects were identified.

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

* Test cases were executed against the live Automation Exercise API.
* Actual Results were recorded based on the API responses observed in Postman.
* HTTP status codes, response body, response structure, and applicable response data were validated.
* Response time was recorded as an observation during execution.
* No performance threshold was defined for this project.
* All 4 Products List API test cases were executed and completed.
* No genuine reproducible defects were identified during Products List API execution.
* Retesting and regression testing will be documented separately if defects are identified and subsequently fixed.
