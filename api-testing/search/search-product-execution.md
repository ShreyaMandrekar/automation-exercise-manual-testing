# Search Product API – Test Case Execution

## 1. Module Information

| Field            | Details                           |
| ---------------- | --------------------------------- |
| Project          | Automation Exercise – API Testing |
| API              | Search Product                    |
| Endpoint         | `/api/searchProduct`              |
| HTTP Method      | POST                              |
| Tool             | Postman                           |
| Test Type        | API Testing                       |
| Test Case Status | Executed                          |
| Tester           | Shreya Mandrekar                  |

---

# 2. Objective

To verify the Search Product API functionality, search parameter handling, response structure, returned product data, handling of unsupported request methods, and behavior for invalid or missing search parameters.

---

# 3. Test Cases

## TC-API-SEARCH-001 – Verify Search Product API returns matching products for a valid search term

**Scenario:** TS-API-007

| Field         | Details                                   |
| ------------- | ----------------------------------------- |
| Test Case ID  | TC-API-SEARCH-001                         |
| Priority      | High                                      |
| Preconditions | Search Product API endpoint is accessible |
| Test Data     | Valid product search term                 |

**Steps:**

1. Open Postman.
2. Open the `Automation Exercise – API Testing` collection.
3. Create or open the Search Product API request.
4. Set the HTTP method to POST.
5. Enter the Search Product API endpoint.
6. Add the required `search_product` parameter with a valid product search term.
7. Send the request.
8. Observe the HTTP response.
9. Verify the response body.
10. Verify the `responseCode` field.
11. Verify the returned product collection.

**Expected Result:**

The API should successfully process the search request and return the expected response with an appropriate HTTP status, successful `responseCode`, and a product collection containing products relevant to the search term.

**Actual Result:**
The POST request was successfully processed with HTTP status 200 OK. The response contained responseCode: 200 and returned product records matching the search term top. The returned products included IDs 1, 5, 6, 7, 8, 11, 12, 13, 14, 15, 16, 18, 24, and 42, and the product names contained the search term top. The observed response time was 1.65 seconds.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The Search Product API returned products relevant to the supplied search term as expected.

---

## TC-API-SEARCH-002 – Verify Search Product API response and product data structure

**Scenario:** TS-API-009

| Field         | Details                                    |
| ------------- | ------------------------------------------ |
| Test Case ID  | TC-API-SEARCH-002                          |
| Priority      | High                                       |
| Preconditions | Search Product API returns product records |
| Test Data     | Valid product search term                  |

**Steps:**

1. Send a POST request to the Search Product API with a valid search term.
2. Open the returned product collection.
3. Inspect multiple returned product records where available.
4. Verify the applicable product fields.
5. Verify the values of the returned fields.
6. Verify the response structure.
7. Verify the `responseCode`.

**Expected Result:**

The response should have the expected structure and contain applicable product information such as product ID, name, price, brand, category, and other available product fields. The response should contain the expected `responseCode`.

**Actual Result:**
The response returned multiple product records in the products collection. The product records contained applicable fields including id, name, price, brand, and category, with category information including usertype and category name. The response contained responseCode: 200 with HTTP status 200 OK. The observed response time was 1.65 seconds.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The Search Product API returned multiple product records with the expected response structure and applicable product information.

---

## TC-API-SEARCH-003 – Verify Search Product API behavior for a search term with no matching products

**Scenario:** TS-API-008

| Field         | Details                                       |
| ------------- | --------------------------------------------- |
| Test Case ID  | TC-API-SEARCH-003                             |
| Priority      | Medium                                        |
| Preconditions | Search Product API endpoint is accessible     |
| Test Data     | Search term with no expected matching product |

**Steps:**

1. Open the Search Product API request in Postman.
2. Set the HTTP method to POST.
3. Enter a search term that does not match the available product data.
4. Send the request.
5. Observe the HTTP response.
6. Review the response body and `responseCode`.

**Expected Result:**

The API should handle a search term with no matching products according to its implemented/documented behavior and return an appropriate response.

**Actual Result:**
The POST request returned HTTP status 200 OK with responseCode: 200. The products collection was present as an empty array, indicating that no products matched the search term zzzznonexistent999. No message field was present in the response. The observed response time was 1.45 seconds.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The API handled a search term with no matching products by returning an empty products collection with a successful response.

---

## TC-API-SEARCH-004 – Verify Search Product API rejects unsupported GET method

**Scenario:** TS-API-008

| Field         | Details                                   |
| ------------- | ----------------------------------------- |
| Test Case ID  | TC-API-SEARCH-004                         |
| Priority      | Medium                                    |
| Preconditions | Search Product API endpoint is accessible |
| Test Data     | GET request to `/api/searchProduct`       |

**Steps:**

1. Open the Search Product API request in Postman.
2. Change the HTTP method from POST to GET.
3. Send the request.
4. Observe the HTTP response.
5. Review the response body.

**Expected Result:**

The API should reject the unsupported GET method and return the documented or implemented response for an unsupported request method.

**Actual Result:**
The GET request returned HTTP status 200 OK. The JSON response contained responseCode: 405 with the message This request method is not supported. The observed response time was 332 ms.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The API correctly rejected the unsupported GET method and returned the expected method-not-supported response.

---

## TC-API-SEARCH-005 – Verify Search Product API behavior when the search parameter is missing

**Scenario:** TS-API-008

| Field         | Details                                         |
| ------------- | ----------------------------------------------- |
| Test Case ID  | TC-API-SEARCH-005                               |
| Priority      | Medium                                          |
| Preconditions | Search Product API endpoint is accessible       |
| Test Data     | POST request without `search_product` parameter |

**Steps:**

1. Open the Search Product API request in Postman.
2. Set the HTTP method to POST.
3. Remove the `search_product` parameter.
4. Send the request.
5. Observe the HTTP response.
6. Review the response body and `responseCode`.

**Expected Result:**

The API should handle the missing search parameter according to its implemented/documented behavior and return an appropriate response.

**Actual Result:**
The POST request returned HTTP status 200 OK with responseCode: 400. The response message stated Bad request. Search product parameter is missing in post request. No product search was performed because the required search_product parameter was not provided. The observed response time was 1.29 seconds.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The API correctly handled the missing search parameter by returning a 400 response code with an appropriate error message.

---

## TC-API-SEARCH-006 – Verify Search Product API behavior for an invalid search parameter

**Scenario:** TS-API-008

| Field         | Details                                   |
| ------------- | ----------------------------------------- |
| Test Case ID  | TC-API-SEARCH-006                         |
| Priority      | Medium                                    |
| Preconditions | Search Product API endpoint is accessible |
| Test Data     | Invalid or unsupported search parameter   |

**Steps:**

1. Open the Search Product API request in Postman.
2. Set the HTTP method to POST.
3. Provide an invalid or unsupported search parameter.
4. Send the request.
5. Observe the HTTP response.
6. Review the response body and `responseCode`.

**Expected Result:**

The API should handle the invalid or unsupported search parameter according to its implemented/documented behavior and return an appropriate response.

**Actual Result:**
The POST request returned HTTP status 200 OK with responseCode: 400. The response message stated Bad Request, search product parameter is missing in POST request. The request used an unsupported parameter named invalid_parameter instead of the required search_product parameter. The observed response time was 1.14 seconds.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The API rejected the request because the required search_product parameter was not provided. The API did not specifically identify the unsupported parameter name in the error message.

---

# 4. Execution Summary

| Metric             | Result |
| ------------------ | ------ |
| Total Test Cases   | 6      |
| Passed             | 6      |
| Failed             | 0      |
| Blocked            | 0      |
| Not Executed       | 0      |
| Defects Identified | 0      |

**Overall Result:** PASS

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
* HTTP status codes, response body, response structure, response data, and search behavior were validated.
* Response time was recorded as an observation during execution.
* No performance threshold is defined for this project.
* No genuine reproducible API defects were identified during Search Product API testing.
* All six test cases were executed individually and passed.
* Retesting and regression testing will be documented separately if defects are identified and subsequently fixed.
