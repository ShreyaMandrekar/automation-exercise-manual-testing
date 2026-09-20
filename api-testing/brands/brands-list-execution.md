# Brands List API – Test Case Execution

## 1. Module Information

| Field            | Details                           |
| ---------------- | --------------------------------- |
| Project          | Automation Exercise – API Testing |
| API              | Brands List                       |
| Endpoint         | `/api/brandsList`                 |
| HTTP Method      | GET                               |
| Tool             | Postman                           |
| Test Type        | API Testing                       |
| Test Case Status | Not Executed                      |
| Tester           | Shreya Mandrekar                  |

---

# 2. Objective

To verify the Brands List API functionality, response structure, brand data, handling of unsupported request methods, and behavior for an invalid endpoint.

---

# 3. Test Cases

## TC-API-BRANDS-001 – Verify Brands List API returns successful response with valid brand data

**Scenario:** TS-API-004

| Field         | Details                                |
| ------------- | -------------------------------------- |
| Test Case ID  | TC-API-BRANDS-001                      |
| Priority      | High                                   |
| Preconditions | Brands List API endpoint is accessible |
| Test Data     | Valid GET request to `/api/brandsList` |

**Steps:**

1. Open Postman.
2. Open the `Automation Exercise – API Testing` collection.
3. Send a GET request to `/api/brandsList`.
4. Observe the HTTP response.
5. Verify the response body.
6. Verify the `responseCode` field.
7. Verify that the `brands` collection is present.
8. Verify that brand records contain applicable brand information.

**Expected Result:**

The API should successfully process the GET request and return the expected Brands List response with HTTP 200, a successful `responseCode`, a `brands` collection, and applicable brand information.

**Actual Result:**
he GET request was successfully processed with HTTP status 200 OK. The response contained responseCode: 200, the brands collection was present, and brand records displayed applicable information including id and brand. The observed response time was 1.62 seconds.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The Brands List API returned the expected successful response and brand data.

---

## TC-API-BRANDS-002 – Verify Brands List API brand data structure

**Scenario:** TS-API-006

| Field         | Details                                |
| ------------- | -------------------------------------- |
| Test Case ID  | TC-API-BRANDS-002                      |
| Priority      | High                                   |
| Preconditions | Brands List API returns brand records  |
| Test Data     | Valid GET request to `/api/brandsList` |

**Steps:**

1. Send a GET request to `/api/brandsList`.
2. Open the `brands` collection in the response.
3. Inspect multiple brand records.
4. Verify the applicable brand fields and their values.
5. Check whether brand IDs are unique.

**Expected Result:**

Returned brand records should have the expected data structure, including applicable fields such as ID and brand name. Brand IDs should be unique.

**Actual Result:**
Multiple brand records were present in the brands collection, with brand IDs ranging from 1 to 43. The brand records contained id and brand fields, and the brand IDs were unique. The response contained responseCode: 200 with HTTP status 200 OK. The observed response time was 1.96 seconds.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The brand data structure and applicable brand fields were present as expected, and the brand IDs were unique.

---

## TC-API-BRANDS-003 – Verify Brands List API rejects unsupported POST method

**Scenario:** TS-API-005

| Field         | Details                                |
| ------------- | -------------------------------------- |
| Test Case ID  | TC-API-BRANDS-003                      |
| Priority      | Medium                                 |
| Preconditions | Brands List API endpoint is accessible |
| Test Data     | POST request to `/api/brandsList`      |

**Steps:**

1. Open the Brands List API request in Postman.
2. Change the HTTP method from GET to POST.
3. Send the request.
4. Observe the HTTP response and response body.

**Expected Result:**

The API should reject the unsupported POST method and return the documented response for the unsupported request method.

**Actual Result:**
The POST request returned HTTP status 200 OK with responseCode: 405. The response message displayed “This request method is not supported.” The observed response time was 1.80 seconds.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The API correctly rejected the unsupported POST method and returned the expected method-not-supported response.

---

## TC-API-BRANDS-004 – Verify Brands List API response behavior for invalid endpoint

**Scenario:** TS-API-030

| Field         | Details                                                   |
| ------------- | --------------------------------------------------------- |
| Test Case ID  | TC-API-BRANDS-004                                         |
| Priority      | Medium                                                    |
| Preconditions | Brands List API endpoint is accessible                    |
| Test Data     | GET request to invalid endpoint `/api/brandsList/invalid` |

**Steps:**

1. Prepare a GET request to the invalid endpoint `/api/brandsList/invalid`.
2. Send the request.
3. Observe the HTTP response.
4. Review the response body.

**Expected Result:**

The API should handle the invalid endpoint appropriately and return a meaningful error response according to its documented behavior.

**Actual Result:**
The GET request to the invalid endpoint returned HTTP status 404 Not Found. No responseCode field was present in the response. The response body contained HTML error-page content. The observed response time was 1.95 seconds.

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
* Actual Results will be recorded based on the API responses observed in Postman.
* HTTP status codes, response body, response structure, and applicable response data will be validated.
* Response time may be recorded as an observation during execution.
* No performance threshold is defined for this project.
* Defect IDs will be added only when genuine reproducible defects are identified.
* Test cases will be executed individually and updated after execution.
* Retesting and regression testing will be documented separately if defects are identified and subsequently fixed.
