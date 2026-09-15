# Cart & Checkout Test Cases & Execution – Automation Exercise

## 1. Module Information

| Field            | Details                                    |
| ---------------- | ------------------------------------------ |
| Application      | Automation Exercise                        |
| Module           | Cart & Checkout                            |
| Testing Type     | Manual Testing                             |
| Test Level       | System Testing                             |
| Test Approach    | Functional, Positive, Negative, Validation |
| Test Case Status | Executed                                   |
| Tester           | Shreya Mandrekar                           |

---

## 2. Objective

The objective of these test cases is to verify the Cart and Checkout functionality of the Automation Exercise application, including:

* Empty Cart behavior
* Product display in Cart
* Multiple products
* Product information
* Product quantity
* Product price and total calculation
* Product removal
* Continue On Cart
* Proceed To Checkout
* Checkout access for logged-out users
* Cart persistence after login
* Checkout page and order summary
* Delivery Address and Billing Address
* Order comments
* Payment page fields
* Payment mandatory-field validation
* Payment field input-format handling
* Successful order placement
* Order confirmation
* Invoice download
* Continue after order completion
* Post-order order history or tracking availability

All Actual Results, Status, Defect ID, and Comments will be updated after executing the test cases against the live application.

---

## 3. Preconditions

Unless otherwise specified:

1. Automation Exercise website is accessible.
2. Tester has access to a web browser.
3. A registered test account is available for scenarios requiring login.
4. Test products are available.
5. Test data is prepared before execution.
6. User is logged out before independent logged-out scenarios unless otherwise specified.

---

# 4. Test Case Execution

## TC-CART-001 – Verify Cart page is accessible

**Scenario:** TS-CART-01

| Field         | Details                   |
| ------------- | ------------------------- |
| Test Case ID  | TC-CART-001               |
| Priority      | High                      |
| Preconditions | Application is accessible |
| Test Data     | N/A                       |

**Steps:**

1. Open Automation Exercise.
2. Navigate to the Cart page.
3. Observe the Cart page.

**Expected Result:**
The Cart page should open successfully and display the appropriate cart state.

**Actual Result:**
The Cart page opened successfully from the navbar. The breadcrumb displayed Home > Shopping Cart. Since no products were present, the page displayed “Cart is empty!” in bold text along with “Click here to buy products”, where “here” is a hyperlink.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
Cart page is accessible and displays the expected empty-cart state.

---

## TC-CART-002 – Verify empty Cart message

**Scenario:** TS-CART-01

| Field         | Details                            |
| ------------- | ---------------------------------- |
| Test Case ID  | TC-CART-002                        |
| Priority      | High                               |
| Preconditions | Cart does not contain any products |
| Test Data     | Empty Cart                         |

**Steps:**

1. Open the Cart page.
2. Ensure no product is present.
3. Observe the Cart content.

**Expected Result:**
The application should display an appropriate message indicating that the Cart is empty.

**Actual Result:**
The Cart page displayed “Cart is empty!” in bold text when no products were present in the Cart. The message also included “Click here to buy products”, with “here” displayed as a hyperlink.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The expected empty Cart message was displayed correctly when the Cart contained no products.

---

## TC-CART-003 – Verify Products link from empty Cart

**Scenario:** TS-CART-01

| Field         | Details       |
| ------------- | ------------- |
| Test Case ID  | TC-CART-003   |
| Priority      | Medium        |
| Preconditions | Cart is empty |
| Test Data     | N/A           |

**Steps:**

1. Open the Cart page with no products.
2. Locate the available Products link in the empty-cart message.
3. Click the link.
4. Observe the resulting page.

**Expected Result:**
The link should redirect the user to the Products page.

**Actual Result:**
Clicking the “here” hyperlink in the empty Cart message redirected the user to the Products page successfully.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The “here” hyperlink correctly redirects the user from the empty Cart to the Products page.

---

## TC-CART-004 – Verify single product is displayed in Cart

**Scenario:** TS-CART-02

| Field         | Details                |
| ------------- | ---------------------- |
| Test Case ID  | TC-CART-004            |
| Priority      | High                   |
| Preconditions | A product is available |
| Test Data     | Madame Top For Women   |

**Steps:**

1. Add a product to the Cart.
2. Open the Cart page.
3. Observe the Cart.

**Expected Result:**
The added product should be displayed correctly in the Cart.

**Actual Result:**
The Madame Top For Women was successfully added to the Cart and was displayed in the Cart. After adding the product, the application displayed an “Added!” confirmation popup with the message “Your product has been added to cart.” The popup also provided “View Cart” and “Continue Shopping” options.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The single product was successfully added and displayed in the Cart. The application also displayed the expected add-to-cart confirmation popup.

---

## TC-CART-005 – Verify multiple different products are displayed in Cart

**Scenario:** TS-CART-03

| Field         | Details                                |
| ------------- | -------------------------------------- |
| Test Case ID  | TC-CART-005                            |
| Priority      | High                                   |
| Preconditions | Products are available                 |
| Test Data     | Madame Top For Women; Summer White Top |

**Steps:**

1. Add the first product to the Cart.
2. Add a different product to the Cart.
3. Open the Cart page.
4. Observe the products.

**Expected Result:**
All successfully added products should be displayed separately in the Cart.

**Actual Result:**
Madame Top For Women and Summer White Top were successfully added to the Cart. Both products were displayed separately in the Cart.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
Both different products were successfully added and displayed as separate Cart items.

---

## TC-CART-006 – Verify product information displayed in Cart

**Scenario:** TS-CART-04

| Field         | Details                          |
| ------------- | -------------------------------- |
| Test Case ID  | TC-CART-006                      |
| Priority      | High                             |
| Preconditions | A product is present in the Cart |
| Test Data     | Madame Top For Women             |

**Steps:**

1. Add the product to the Cart.
2. Open the Cart.
3. Observe the product information.

**Expected Result:**
The Cart should display the relevant product information, including product details, unit price, quantity, and total price.

**Actual Result:**
For Madame Top For Women, the Cart displayed the product image, product name, unit price, quantity, and total price properly.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The relevant product information was displayed correctly for the product in the Cart.

---

## TC-CART-007 – Verify selected product quantity is reflected in Cart

**Scenario:** TS-CART-05

| Field         | Details                            |
| ------------- | ---------------------------------- |
| Test Case ID  | TC-CART-007                        |
| Priority      | High                               |
| Preconditions | Product details page is accessible |
| Test Data     | Madame Top For Women; Quantity 3   |

**Steps:**

1. Open the product details page.
2. Increase the product quantity to 3.
3. Add the product to the Cart.
4. Open the Cart.
5. Observe the displayed quantity.

**Expected Result:**
If the product already exists in the Cart, adding the product with a selected quantity should increment the existing Cart quantity by the selected quantity.

**Actual Result:**
The Madame Top For Women was already present in the Cart with quantity 1. After selecting quantity 3 on the product details page and clicking Add to Cart, the application updated the existing product quantity to 4 (1 existing + 3 newly added). No duplicate product entry was created.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
Existing product quantity was correctly incremented by the newly selected quantity. The same product was updated instead of creating a duplicate Cart entry.

---

## TC-CART-008 – Verify product total calculation

**Scenario:** TS-CART-06

| Field         | Details                                 |
| ------------- | --------------------------------------- |
| Test Case ID  | TC-CART-008                             |
| Priority      | High                                    |
| Preconditions | Product is present in Cart              |
| Test Data     | Madame Top For Women – ₹400; Quantity 3 |

**Steps:**

1. Add the product to the Cart.
2. Set the quantity to 3 before adding it, where supported.
3. Open the Cart.
4. Observe the unit price, quantity, and product total.

**Expected Result:**
The product total should equal the unit price multiplied by the selected quantity.

**Actual Result:**
To be updated during formal execution.

**Status:**
NOT EXECUTED

**Defect ID:**
N/A

**Comments:**
To be updated after execution.

---

## TC-CART-009 – Verify overall Cart total with multiple products

**Scenario:** TS-CART-06

| Field         | Details                                                        |
| ------------- | -------------------------------------------------------------- |
| Test Case ID  | TC-CART-009                                                    |
| Priority      | High                                                           |
| Preconditions | Multiple products are available                                |
| Test Data     | Madame Top For Women – ₹400 × 3; Summer White Top – ₹1,000 × 1 |

**Steps:**

1. Add Madame Top For Women with quantity 3.
2. Add Summer White Top with quantity 1.
3. Open the Cart.
4. Observe the individual product totals.
5. Observe the overall Cart total.

**Expected Result:**
The overall Cart total should correctly reflect the combined totals of all products and quantities.

**Actual Result:**
To be updated during formal execution.

**Status:**
NOT EXECUTED

**Defect ID:**
N/A

**Comments:**
To be updated after execution.

---

## TC-CART-010 – Verify removal of one product from Cart

**Scenario:** TS-CART-07

| Field         | Details                                   |
| ------------- | ----------------------------------------- |
| Test Case ID  | TC-CART-010                               |
| Priority      | High                                      |
| Preconditions | At least two products are present in Cart |
| Test Data     | Madame Top For Women; Summer White Top    |

**Steps:**

1. Open the Cart.
2. Remove one product.
3. Observe the Cart.

**Expected Result:**
The selected product should be removed while the remaining product(s) should remain in the Cart.

**Actual Result:**
To be updated during formal execution.

**Status:**
NOT EXECUTED

**Defect ID:**
N/A

**Comments:**
To be updated after execution.

---

## TC-CART-011 – Verify empty Cart after removing the last product

**Scenario:** TS-CART-07

| Field         | Details                     |
| ------------- | --------------------------- |
| Test Case ID  | TC-CART-011                 |
| Priority      | High                        |
| Preconditions | One product remains in Cart |
| Test Data     | Remaining Cart product      |

**Steps:**

1. Open the Cart.
2. Remove the remaining product.
3. Observe the Cart.

**Expected Result:**
The product should be removed and the appropriate empty-cart state should be displayed.

**Actual Result:**
To be updated during formal execution.

**Status:**
NOT EXECUTED

**Defect ID:**
N/A

**Comments:**
To be updated after execution.

---

## TC-CART-012 – Verify Continue On Cart functionality

**Scenario:** TS-CART-08

| Field         | Details                                 |
| ------------- | --------------------------------------- |
| Test Case ID  | TC-CART-012                             |
| Priority      | Medium                                  |
| Preconditions | At least one product is present in Cart |
| Test Data     | Any Cart product                        |

**Steps:**

1. Open the Cart.
2. Click Continue On Cart.
3. Observe the resulting page and Cart contents.

**Expected Result:**
The user should remain on the Cart page and existing Cart contents should remain available.

**Actual Result:**
To be updated during formal execution.

**Status:**
NOT EXECUTED

**Defect ID:**
N/A

**Comments:**
To be updated after execution.

---

## TC-CART-013 – Verify Proceed To Checkout from Cart

**Scenario:** TS-CART-09

| Field         | Details                                 |
| ------------- | --------------------------------------- |
| Test Case ID  | TC-CART-013                             |
| Priority      | High                                    |
| Preconditions | At least one product is present in Cart |
| Test Data     | Any Cart product                        |

**Steps:**

1. Open the Cart.
2. Click Proceed To Checkout.
3. Observe the resulting flow.

**Expected Result:**
The application should proceed to the Checkout flow or display the appropriate authentication requirement based on the user's login state.

**Actual Result:**
To be updated during formal execution.

**Status:**
NOT EXECUTED

**Defect ID:**
N/A

**Comments:**
To be updated after execution.

---

## TC-CART-014 – Verify checkout access for logged-out user

**Scenario:** TS-CART-10

| Field         | Details                                             |
| ------------- | --------------------------------------------------- |
| Test Case ID  | TC-CART-014                                         |
| Priority      | High                                                |
| Preconditions | User is logged out and a product is present in Cart |
| Test Data     | Any Cart product                                    |

**Steps:**

1. Open the Cart.
2. Click Proceed To Checkout.
3. Observe the displayed message.
4. Locate the Register/Login option.

**Expected Result:**
The application should inform the logged-out user that login or registration is required to proceed with checkout.

**Actual Result:**
To be updated during formal execution.

**Status:**
NOT EXECUTED

**Defect ID:**
N/A

**Comments:**
To be updated after execution.

---

## TC-CART-015 – Verify Register/Login link redirects to Signup/Login

**Scenario:** TS-CART-10

| Field         | Details                                              |
| ------------- | ---------------------------------------------------- |
| Test Case ID  | TC-CART-015                                          |
| Priority      | High                                                 |
| Preconditions | Logged-out user has attempted to proceed to Checkout |
| Test Data     | N/A                                                  |

**Steps:**

1. Click the Register/Login link.
2. Observe the resulting page.

**Expected Result:**
The Register/Login link should redirect the user to the Signup/Login page.

**Actual Result:**
To be updated during formal execution.

**Status:**
NOT EXECUTED

**Defect ID:**
N/A

**Comments:**
To be updated after execution.

---

## TC-CART-016 – Verify Cart persistence after login

**Scenario:** TS-CART-11

| Field         | Details                                             |
| ------------- | --------------------------------------------------- |
| Test Case ID  | TC-CART-016                                         |
| Priority      | High                                                |
| Preconditions | Product is present in Cart while user is logged out |
| Test Data     | Registered test account                             |

**Steps:**

1. Add a product to the Cart while logged out.
2. Click Proceed To Checkout.
3. Log in using valid credentials.
4. Return to the Checkout flow.
5. Observe the Cart contents.

**Expected Result:**
The product previously added to the Cart should remain available after successful login.

**Actual Result:**
To be updated during formal execution.

**Status:**
NOT EXECUTED

**Defect ID:**
N/A

**Comments:**
To be updated after execution.

---

## TC-CART-017 – Verify Checkout page displays Review Your Order section

**Scenario:** TS-CART-12

| Field         | Details                                            |
| ------------- | -------------------------------------------------- |
| Test Case ID  | TC-CART-017                                        |
| Priority      | High                                               |
| Preconditions | User is logged in and products are present in Cart |
| Test Data     | Cart products                                      |

**Steps:**

1. Proceed to Checkout.
2. Locate the Review Your Order section.
3. Observe the displayed products.

**Expected Result:**
The Checkout page should display the Review Your Order section with the products included in the order.

**Actual Result:**
To be updated during formal execution.

**Status:**
NOT EXECUTED

**Defect ID:**
N/A

**Comments:**
To be updated after execution.

---

## TC-CART-018 – Verify Checkout order summary details

**Scenario:** TS-CART-12

| Field         | Details                  |
| ------------- | ------------------------ |
| Test Case ID  | TC-CART-018              |
| Priority      | High                     |
| Preconditions | User is on Checkout page |
| Test Data     | Multiple Cart products   |

**Steps:**

1. Observe the Review Your Order table.
2. Verify product description.
3. Verify price.
4. Verify quantity.
5. Verify product total.
6. Verify overall order total.

**Expected Result:**
The Checkout order summary should correctly display the products, quantities, prices, individual totals, and overall order total.

**Actual Result:**
To be updated during formal execution.

**Status:**
NOT EXECUTED

**Defect ID:**
N/A

**Comments:**
To be updated after execution.

---

## TC-CART-019 – Verify Delivery Address display

**Scenario:** TS-CART-13

| Field         | Details                                |
| ------------- | -------------------------------------- |
| Test Case ID  | TC-CART-019                            |
| Priority      | High                                   |
| Preconditions | User is logged in and on Checkout page |
| Test Data     | Registered test account                |

**Steps:**

1. Locate the Delivery Address section.
2. Observe the displayed address information.

**Expected Result:**
The Delivery Address section should display the available address information associated with the user.

**Actual Result:**
To be updated during formal execution.

**Status:**
NOT EXECUTED

**Defect ID:**
N/A

**Comments:**
To be updated after execution.

---

## TC-CART-020 – Verify Billing Address display

**Scenario:** TS-CART-13

| Field         | Details                                |
| ------------- | -------------------------------------- |
| Test Case ID  | TC-CART-020                            |
| Priority      | High                                   |
| Preconditions | User is logged in and on Checkout page |
| Test Data     | Registered test account                |

**Steps:**

1. Locate the Billing Address section.
2. Observe the displayed address information.

**Expected Result:**
The Billing Address section should display the available address information associated with the order.

**Actual Result:**
To be updated during formal execution.

**Status:**
NOT EXECUTED

**Defect ID:**
N/A

**Comments:**
To be updated after execution.

---

## TC-CART-021 – Verify Order Comment field accepts blank input

**Scenario:** TS-CART-14

| Field         | Details                  |
| ------------- | ------------------------ |
| Test Case ID  | TC-CART-021              |
| Priority      | Medium                   |
| Preconditions | User is on Checkout page |
| Test Data     | Blank Order Comment      |

**Steps:**

1. Locate the Order Comment field.
2. Leave the field blank.
3. Continue with the order flow.

**Expected Result:**
The user should be able to proceed without entering an Order Comment.

**Actual Result:**
To be updated during formal execution.

**Status:**
NOT EXECUTED

**Defect ID:**
N/A

**Comments:**
To be updated after execution.

---

## TC-CART-022 – Verify Order Comment accepts text

**Scenario:** TS-CART-14

| Field         | Details                                           |
| ------------- | ------------------------------------------------- |
| Test Case ID  | TC-CART-022                                       |
| Priority      | Medium                                            |
| Preconditions | User is on Checkout page                          |
| Test Data     | `Please handle the product carefully do not fold` |

**Steps:**

1. Locate the Order Comment field.
2. Enter a valid text comment.
3. Continue with the order flow.
4. Observe the subsequent page.

**Expected Result:**
The Order Comment should be accepted without preventing the order process.

**Actual Result:**
To be updated during formal execution.

**Status:**
NOT EXECUTED

**Defect ID:**
N/A

**Comments:**
Whether the comment is displayed or carried forward to a later page will be recorded as an observation during execution.

---

## TC-CART-023 – Verify Payment page fields

**Scenario:** TS-CART-15

| Field         | Details                                         |
| ------------- | ----------------------------------------------- |
| Test Case ID  | TC-CART-023                                     |
| Priority      | High                                            |
| Preconditions | User has completed Checkout and reached Payment |
| Test Data     | N/A                                             |

**Steps:**

1. Open the Payment page.
2. Verify Name on Card.
3. Verify Card Number.
4. Verify CVC.
5. Verify Expiration Month.
6. Verify Expiration Year.
7. Verify Pay and Confirm Order button.

**Expected Result:**
The Payment page should display all required payment fields and the Pay and Confirm Order control.

**Actual Result:**
To be updated during formal execution.

**Status:**
NOT EXECUTED

**Defect ID:**
N/A

**Comments:**
To be updated after execution.

---

## TC-CART-024 – Verify mandatory validation for blank Name on Card

**Scenario:** TS-CART-16

| Field         | Details                    |
| ------------- | -------------------------- |
| Test Case ID  | TC-CART-024                |
| Priority      | High                       |
| Preconditions | Payment page is accessible |
| Test Data     | Name on Card: Blank        |

**Steps:**

1. Leave Name on Card blank.
2. Leave the remaining payment fields blank.
3. Click Pay and Confirm Order.
4. Observe the validation.

**Expected Result:**
The application should prevent submission and display mandatory-field validation for Name on Card.

**Actual Result:**
To be updated during formal execution.

**Status:**
NOT EXECUTED

**Defect ID:**
N/A

**Comments:**
To be updated after execution.

---

## TC-CART-025 – Verify mandatory validation for blank Card Number

**Scenario:** TS-CART-16

| Field         | Details                    |
| ------------- | -------------------------- |
| Test Case ID  | TC-CART-025                |
| Priority      | High                       |
| Preconditions | Payment page is accessible |
| Test Data     | Card Number: Blank         |

**Steps:**

1. Enter a value in Name on Card.
2. Leave Card Number blank.
3. Leave remaining required fields blank.
4. Click Pay and Confirm Order.
5. Observe the validation.

**Expected Result:**
The application should prevent submission and display mandatory-field validation for Card Number.

**Actual Result:**
To be updated during formal execution.

**Status:**
NOT EXECUTED

**Defect ID:**
N/A

**Comments:**
To be updated after execution.

---

## TC-CART-026 – Verify mandatory validation for blank CVC

**Scenario:** TS-CART-16

| Field         | Details                    |
| ------------- | -------------------------- |
| Test Case ID  | TC-CART-026                |
| Priority      | High                       |
| Preconditions | Payment page is accessible |
| Test Data     | CVC: Blank                 |

**Steps:**

1. Enter values in the preceding payment fields.
2. Leave CVC blank.
3. Leave the remaining required fields blank.
4. Click Pay and Confirm Order.
5. Observe the validation.

**Expected Result:**
The application should prevent submission and display mandatory-field validation for CVC.

**Actual Result:**
To be updated during formal execution.

**Status:**
NOT EXECUTED

**Defect ID:**
N/A

**Comments:**
To be updated after execution.

---

## TC-CART-027 – Verify mandatory validation for blank Expiration Month

**Scenario:** TS-CART-16

| Field         | Details                    |
| ------------- | -------------------------- |
| Test Case ID  | TC-CART-027                |
| Priority      | High                       |
| Preconditions | Payment page is accessible |
| Test Data     | Expiration Month: Blank    |

**Steps:**

1. Complete the preceding payment fields.
2. Leave Expiration Month blank.
3. Leave remaining required fields blank.
4. Click Pay and Confirm Order.
5. Observe the validation.

**Expected Result:**
The application should prevent submission and display mandatory-field validation for Expiration Month.

**Actual Result:**
To be updated during formal execution.

**Status:**
NOT EXECUTED

**Defect ID:**
N/A

**Comments:**
To be updated after execution.

---

## TC-CART-028 – Verify mandatory validation for blank Expiration Year

**Scenario:** TS-CART-16

| Field         | Details                    |
| ------------- | -------------------------- |
| Test Case ID  | TC-CART-028                |
| Priority      | High                       |
| Preconditions | Payment page is accessible |
| Test Data     | Expiration Year: Blank     |

**Steps:**

1. Complete the preceding payment fields.
2. Leave Expiration Year blank.
3. Click Pay and Confirm Order.
4. Observe the validation.

**Expected Result:**
The application should prevent submission and display mandatory-field validation for Expiration Year.

**Actual Result:**
To be updated during formal execution.

**Status:**
NOT EXECUTED

**Defect ID:**
N/A

**Comments:**
To be updated after execution.

---

## TC-CART-029 – Verify Payment field input format handling

**Scenario:** TS-CART-17

| Field         | Details                     |
| ------------- | --------------------------- |
| Test Case ID  | TC-CART-029                 |
| Priority      | High                        |
| Preconditions | Payment page is accessible  |
| Test Data     | Inappropriate input formats |

**Steps:**

1. Enter numeric characters in Name on Card.
2. Enter alphabetic characters in Card Number.
3. Enter alphabetic characters in CVC.
4. Enter alphabetic characters in Expiration Month.
5. Enter alphabetic characters in Expiration Year.
6. Attempt to submit the payment form.
7. Record the behavior of each field.

**Expected Result:**
The application should apply appropriate input validation to payment fields according to the supported field format and validation rules.

**Actual Result:**
To be updated during formal execution.

**Status:**
NOT EXECUTED

**Defect ID:**
N/A

**Comments:**
Any acceptance of inappropriate input will be evaluated as a potential defect only if the expected validation behavior can be reasonably established and the issue is reproducible.

---

## TC-CART-030 – Verify successful order placement with supported payment data

**Scenario:** TS-CART-18

| Field         | Details                                        |
| ------------- | ---------------------------------------------- |
| Test Case ID  | TC-CART-030                                    |
| Priority      | High                                           |
| Preconditions | User is logged in and has completed Checkout   |
| Test Data     | Payment test data supported by the application |

**Steps:**

1. Enter payment information supported by the application.
2. Click Pay and Confirm Order.
3. Observe the result.

**Expected Result:**
The application should process the order successfully and display an order confirmation.

**Actual Result:**
To be updated during formal execution.

**Status:**
NOT EXECUTED

**Defect ID:**
N/A

**Comments:**
To be updated after execution.

---

## TC-CART-031 – Verify Order Confirmation message

**Scenario:** TS-CART-18

| Field         | Details                               |
| ------------- | ------------------------------------- |
| Test Case ID  | TC-CART-031                           |
| Priority      | High                                  |
| Preconditions | Order has been successfully submitted |
| Test Data     | Successful order                      |

**Steps:**

1. Complete the payment process.
2. Observe the confirmation message displayed after submission.

**Expected Result:**
The application should indicate that the order has been successfully confirmed.

**Actual Result:**
To be updated during formal execution.

**Status:**
NOT EXECUTED

**Defect ID:**
N/A

**Comments:**
To be updated after execution.

---

## TC-CART-032 – Verify Order Confirmation page information

**Scenario:** TS-CART-19

| Field         | Details                            |
| ------------- | ---------------------------------- |
| Test Case ID  | TC-CART-032                        |
| Priority      | High                               |
| Preconditions | Order has been successfully placed |
| Test Data     | Successful order                   |

**Steps:**

1. Observe the Order Confirmation page.
2. Verify the order status.
3. Verify the confirmation message.
4. Verify Continue.
5. Verify Download Invoice.

**Expected Result:**
The Order Confirmation page should indicate successful order placement and provide the available post-order options.

**Actual Result:**
To be updated during formal execution.

**Status:**
NOT EXECUTED

**Defect ID:**
N/A

**Comments:**
To be updated after execution.

---

## TC-CART-033 – Verify Download Invoice functionality

**Scenario:** TS-CART-20

| Field         | Details                            |
| ------------- | ---------------------------------- |
| Test Case ID  | TC-CART-033                        |
| Priority      | Medium                             |
| Preconditions | Order has been successfully placed |
| Test Data     | Successful order                   |

**Steps:**

1. Click Download Invoice.
2. Observe the download.
3. Open the downloaded invoice.
4. Verify the available customer/order information.

**Expected Result:**
The invoice should download successfully and contain the available order/customer information.

**Actual Result:**
To be updated during formal execution.

**Status:**
NOT EXECUTED

**Defect ID:**
N/A

**Comments:**
To be updated after execution.

---

## TC-CART-034 – Verify Continue after Order Confirmation

**Scenario:** TS-CART-21

| Field         | Details                            |
| ------------- | ---------------------------------- |
| Test Case ID  | TC-CART-034                        |
| Priority      | Medium                             |
| Preconditions | Order has been successfully placed |
| Test Data     | Successful order                   |

**Steps:**

1. On the Order Confirmation page, click Continue.
2. Observe the resulting page.

**Expected Result:**
The user should be redirected to the application's Home page.

**Actual Result:**
To be updated during formal execution.

**Status:**
NOT EXECUTED

**Defect ID:**
N/A

**Comments:**
To be updated after execution.

---

## TC-CART-035 – Verify post-order order history or tracking availability

**Scenario:** TS-CART-22

| Field         | Details                                                |
| ------------- | ------------------------------------------------------ |
| Test Case ID  | TC-CART-035                                            |
| Priority      | Low                                                    |
| Preconditions | User is logged in and has successfully placed an order |
| Test Data     | Successfully placed order                              |

**Steps:**

1. Return to the application after order completion.
2. Observe the navigation options available to the logged-in user.
3. Check for an Order History, My Orders, or Order Tracking section.
4. Observe whether the previously placed order can be accessed.

**Expected Result:**
If the application provides an order history or tracking feature, previously placed orders should be accessible through the available navigation.

**Actual Result:**
To be updated during formal execution.

**Status:**
NOT EXECUTED

**Defect ID:**
N/A

**Comments:**
If no such feature is available, the absence will be recorded as an observation and will not automatically be treated as a defect without a defined requirement.

---

## TC-CART-036 – Verify Cart state after successful order placement

**Scenario:** TS-CART-18

| Field         | Details                               |
| ------------- | ------------------------------------- |
| Test Case ID  | TC-CART-036                           |
| Priority      | Medium                                |
| Preconditions | An order has been successfully placed |
| Test Data     | Successfully placed order             |

**Steps:**

1. Complete an order successfully.
2. Navigate back to the Cart.
3. Observe the Cart contents.

**Expected Result:**
The Cart should reflect the application's expected post-order state.

**Actual Result:**
To be updated during formal execution.

**Status:**
NOT EXECUTED

**Defect ID:**
N/A

**Comments:**
The actual post-order Cart behavior will be recorded during formal execution.

---

# 5. Test Execution Summary

| Metric           | Result |
| ---------------- | -----: |
| Total Test Cases |     36 |
| Passed           |      0 |
| Failed           |      0 |
| Blocked          |      0 |
| Not Executed     |     36 |
| Defects Raised   |      0 |

> The Cart & Checkout test cases have been prepared from the approved test scenarios. Formal execution results will be updated after testing against the live Automation Exercise application.

---

# 6. Execution Status Definitions

| Status       | Meaning                                      |
| ------------ | -------------------------------------------- |
| PASS         | Actual result matches expected result        |
| FAIL         | Actual result does not match expected result |
| BLOCKED      | Test cannot be executed because of a blocker |
| NOT EXECUTED | Test has not yet been executed               |

---

# 7. Defect Handling

A defect will be reported only when:

* The test case is actually executed.
* The observed behavior differs from the expected result.
* The issue is reproducible.
* The expected behavior can be reasonably established.
* The issue is documented with appropriate details.
* A Jira defect is created and linked to the relevant test case.

Any exploratory observation that does not have a clearly established expected behavior will not automatically be classified as a defect.

Detailed defect reports will be maintained in:

`05-defect-reports.md`

---

# 8. Retesting and Regression

If a genuine defect is identified and subsequently fixed:

* The failed test case will be executed again for retesting.
* The test result will be updated in this document.
* Related functionality will be tested for regression.
* Retesting and regression results will be documented separately in:

`06-retesting-regression.md`

Until a defect is actually identified and fixed, no retesting or regression result will be recorded.

---

# 9. Test Data

The following data categories will be used during Cart & Checkout testing:

| Data Type                | Description                                             |
| ------------------------ | ------------------------------------------------------- |
| Product 1                | Madame Top For Women – ₹400                             |
| Product 2                | Summer White Top – ₹1,000                               |
| Single quantity          | Quantity 1                                              |
| Multiple quantity        | Quantity 3                                              |
| Valid login credentials  | Registered test account                                 |
| Order comment            | `Please handle the product carefully do not fold`       |
| Payment test data        | Test payment data supported by the application          |
| Blank payment fields     | Empty Name, Card Number, CVC, Expiration Month and Year |
| Invalid Name on Card     | Numeric input                                           |
| Invalid Card Number      | Alphabetic input                                        |
| Invalid CVC              | Alphabetic input                                        |
| Invalid Expiration Month | Alphabetic input                                        |
| Invalid Expiration Year  | Alphabetic input                                        |

**Note:**
Test data will be selected appropriately during execution. Real payment card information or other sensitive personal information will not be used in the public test documentation.

---

# 10. Execution Environment

| Field            | Details                                                             |
| ---------------- | ------------------------------------------------------------------- |
| Application URL  | https://www.automationexercise.com/                                 |
| Browser          | Google Chrome 152.0.7977.82                                         |
| Operating System | Windows 11 Home Single Language, Version 25H2 (OS Build 26200.9278) |
| Execution Period | August–September 2026                                               |

---

# 11. Traceability

| Test Scenario | Related Test Cases                                              |
| ------------- | --------------------------------------------------------------- |
| TS-CART-01    | TC-CART-001, TC-CART-002, TC-CART-003                           |
| TS-CART-02    | TC-CART-004                                                     |
| TS-CART-03    | TC-CART-005                                                     |
| TS-CART-04    | TC-CART-006                                                     |
| TS-CART-05    | TC-CART-007                                                     |
| TS-CART-06    | TC-CART-008, TC-CART-009                                        |
| TS-CART-07    | TC-CART-010, TC-CART-011                                        |
| TS-CART-08    | TC-CART-012                                                     |
| TS-CART-09    | TC-CART-013                                                     |
| TS-CART-10    | TC-CART-014, TC-CART-015                                        |
| TS-CART-11    | TC-CART-016                                                     |
| TS-CART-12    | TC-CART-017, TC-CART-018                                        |
| TS-CART-13    | TC-CART-019, TC-CART-020                                        |
| TS-CART-14    | TC-CART-021, TC-CART-022                                        |
| TS-CART-15    | TC-CART-023                                                     |
| TS-CART-16    | TC-CART-024, TC-CART-025, TC-CART-026, TC-CART-027, TC-CART-028 |
| TS-CART-17    | TC-CART-029                                                     |
| TS-CART-18    | TC-CART-030, TC-CART-031, TC-CART-036                           |
| TS-CART-19    | TC-CART-032                                                     |
| TS-CART-20    | TC-CART-033                                                     |
| TS-CART-21    | TC-CART-034                                                     |
| TS-CART-22    | TC-CART-035                                                     |

---

# 12. Notes

Test cases are derived from:

* Cart & Checkout exploratory testing observations
* Approved Cart & Checkout test scenarios
* Application functionality
* Standard functional testing practices
* Positive and negative test conditions
* Input validation scenarios

Official Automation Exercise test cases are not copied as project test cases.

Exploratory observations are not automatically treated as defects. A defect will be reported only when the observed behavior can be confirmed to violate an applicable requirement or clearly defined expected behavior and the issue is reproducible.

Actual results and execution statuses will be recorded based on formal testing performed against the live application.

Retesting and regression results will be documented separately if a genuine defect is fixed in a future execution cycle.
