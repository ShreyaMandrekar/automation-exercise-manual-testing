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
* Continue Shopping
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
| Test Data     | Madame Top For Women – ₹1,000; Quantity 4 |

**Steps:**

1. Open the Cart.
2. Identify the product and its displayed unit price and quantity.
3. Observe the product total.
4. Verify whether the product total equals unit price multiplied by quantity.

**Expected Result:**
The product total should equal the unit price multiplied by the selected quantity.

**Actual Result:**
For Madame Top For Women, the unit price was ₹1,000 and the quantity was 4. The displayed total price was ₹4,000, which correctly equals ₹1,000 × 4.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
Product total price was calculated and displayed correctly based on unit price and quantity.

---

## TC-CART-009 – Verify overall order total with multiple products at Checkout

**Scenario:** TS-CART-06

| Field         | Details                                                                 |
| ------------- | ---------------------------------------------------------------------- |
| Test Case ID  | TC-CART-009                                                             |
| Priority      | High                                                                    |
| Preconditions | Multiple products are available in the Cart                             |
| Test Data     | Madame Top For Women – ₹1,000 × 4; Summer White Top – ₹400 × 1          |

**Steps:**

1. Add multiple products to the Cart with the required quantities.
2. Open the Cart.
3. Verify the individual product totals.
4. Click **Proceed To Checkout**.
5. Observe the order total displayed on the Checkout page.

**Expected Result:**
The Checkout page should display the overall order total correctly by combining the individual product totals and quantities.

**Actual Result:**
The Cart page displayed the individual product totals but did not display a separate overall combined total. After clicking **Proceed To Checkout**, the Checkout page displayed the overall order total as **₹4,400**, calculated from ₹4,000 for Madame Top For Women and ₹400 for Summer White Top.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The overall order total was not displayed separately on the Cart page. The application displayed the combined total on the Checkout page, where the amount was calculated correctly.

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
Madame Top For Women was removed successfully from the Cart. The Summer White Top remained in the Cart with its existing quantity and product details.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
Selected product was removed successfully while the remaining product stayed in the Cart with its quantity and details unchanged.

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
After removing the last remaining product, Summer White Top, the Cart became empty and displayed:
“Cart is empty! Click here to buy products.”

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
Last remaining product was removed successfully and the expected empty Cart message was displayed.

---

## TC-CART-012 – Verify Continue Shopping button in Add to Cart confirmation popup

**Scenario:** TS-CART-08

| Field         | Details                                      |
| ------------- | -------------------------------------------- |
| Test Case ID  | TC-CART-012                                  |
| Priority      | Medium                                       |
| Preconditions | Product details or Products page is accessible |
| Test Data     | Any available product                        |

**Steps:**

1. Open the Products page or any product details page.
2. Select a product and click **Add to Cart**.
3. Observe the Add to Cart confirmation popup.
4. Click the **Continue Shopping** button.
5. Observe the page after the popup is closed.

**Expected Result:**
The Add to Cart confirmation popup should provide a **Continue Shopping** option. Clicking **Continue Shopping** should close the popup and allow the user to continue browsing products without navigating to the Cart.

**Actual Result:**
After adding a product to the Cart, the application displayed an Add to Cart confirmation popup with a **Continue Shopping** button. Clicking **Continue Shopping** closed the popup and kept the user on the current page, allowing continued shopping. When the product was added from the Products page, the user remained on the Products page; when added from the product details page, the user remained on the product details page.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
Continue Shopping functionality worked correctly. The user remained on the current shopping page after closing the Add to Cart confirmation popup.

---

## TC-CART-013 – Verify Proceed To Checkout from Cart

**Scenario:** TS-CART-09

| Field         | Details                                 |
| ------------- | --------------------------------------- |
| Test Case ID  | TC-CART-013                             |
| Priority      | High                                    |
| Preconditions | User is logged in and at least one product is present in Cart |
| Test Data     | Any Cart product                        |

**Steps:**

1. Open the Cart.
2. Click Proceed To Checkout.
3. Observe the resulting flow.

**Expected Result:**
Clicking **Proceed To Checkout** should successfully navigate the logged-in user to the Checkout page.

**Actual Result:**
After clicking **Proceed To Checkout** as a logged-in user, the application successfully redirected to the Checkout page. The page displayed the Delivery Address and Billing Address sections, followed by the Review Your Order section showing the products in tabular form with the total amount. An order comment section was also displayed.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
Proceed To Checkout successfully navigated the logged-in user to the Checkout page, where the expected checkout sections were displayed.

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
After logging out and clicking **Proceed To Checkout** with a product in the Cart, the application displayed a Checkout popup stating **“Register / Login account to proceed on checkout.”** The popup provided a **Register / Login** hyperlink that redirected to the Signup/Login page, along with a **Continue On Cart** button.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
Logged-out users were prevented from proceeding directly to checkout and were provided with a Register/Login option to continue.

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
Clicking the **Register / Login** hyperlink in the checkout popup successfully redirected the user to the **Signup / Login page**.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The Register / Login hyperlink redirected the user to the Signup / Login page successfully.

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

1. Ensure the user is logged out.
2. Add a product to the Cart.
3. Open the Cart and note the product, quantity, and price.
4. Navigate to the Signup/Login page.
5. Log in using valid credentials.
6. Return to the Cart.
7. Observe whether the previously added product is still present.

**Expected Result:**
The product previously added to the Cart should remain available after successful login, with its quantity and relevant details retained.

**Actual Result:**
While logged out, the **Sleeveless Dress** was added to the Cart with quantity 1 and a total price of ₹1,000. After logging in with valid credentials and returning to the Cart, the Sleeveless Dress was still present with the correct quantity and price. The previously existing Blue Top and Men Tshirt were also retained in the Cart.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The product added to the Cart before login persisted after successful login, with its quantity and price retained. Previously existing Cart products were also preserved.

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
The Checkout page displayed the **Review Your Order** section with the Blue Top and Sleeveless Dress. Each product was displayed with its image, description, unit price, quantity, and total. The Blue Top had a price of ₹500 with quantity 1, and the Sleeveless Dress had a price of ₹1,000 with quantity 1. The overall order total was displayed as ₹1,500.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
Review Your Order displayed the products and their relevant price, quantity, and total information correctly. The overall order total was also calculated and displayed correctly.

---

## TC-CART-018 – Verify Delivery Address display

**Scenario:** TS-CART-13

| Field         | Details                                |
| ------------- | -------------------------------------- |
| Test Case ID  | TC-CART-018                            |
| Priority      | High                                   |
| Preconditions | User is logged in and on Checkout page |
| Test Data     | Registered test account                |

**Steps:**

1. Locate the Delivery Address section.
2. Observe the displayed address information.

**Expected Result:**
The Delivery Address section should display the available address information associated with the user.

**Actual Result:**
The Delivery Address section displayed the user's address information, including Title, First Name, Last Name, Company, Address, Address 2, City, State, Zip Code, Country, and Mobile Number. No Edit/Change option was visible.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The Delivery Address section displayed the available address details associated with the logged-in user. No Edit/Change option was visible.

---

## TC-CART-019 – Verify Billing Address display

**Scenario:** TS-CART-13

| Field         | Details                                |
| ------------- | -------------------------------------- |
| Test Case ID  | TC-CART-019                            |
| Priority      | High                                   |
| Preconditions | User is logged in and on Checkout page |
| Test Data     | Registered test account                |

**Steps:**

1. Locate the Billing Address section.
2. Observe the displayed address information.

**Expected Result:**
The Billing Address section should display the available address information associated with the order.

**Actual Result:**
The Billing Address section displayed the user's address information, including Title (Mr.), First Name, Last Name, Company, Address, Address 2, City, State, Zip Code, Country, and Mobile Number. No Edit/Change option was visible.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The Billing Address section displayed the available address details associated with the logged-in user. No Edit/Change option was available to modify the displayed billing address.

---

## TC-CART-020 – Verify Order Comment field accepts blank input

**Scenario:** TS-CART-14

| Field         | Details                  |
| ------------- | ------------------------ |
| Test Case ID  | TC-CART-020              |
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
The Order Comment field was left blank, and the application allowed the user to proceed further with the order flow without entering a comment.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The Order Comment field is optional, as the application allowed the order flow to continue without entering any comment.

---

## TC-CART-021 – Verify Order Comment accepts text

**Scenario:** TS-CART-14

| Field         | Details                                           |
| ------------- | ------------------------------------------------- |
| Test Case ID  | TC-CART-021                                      |
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
The comment Please handle the product carefully do not fold was entered successfully in the Order Comment field. After clicking Place Order, the application allowed the user to proceed to the Payment page. The entered comment was not carried forward or displayed on the Payment page.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
The Order Comment was accepted and did not prevent the order flow from proceeding. The comment was not visibly carried forward to the Payment page; this was recorded as an observation and was not treated as a defect because the test case does not define comment persistence as a required behavior.

---

## TC-CART-022 – Verify Payment page fields

**Scenario:** TS-CART-15

| Field         | Details                                         |
| ------------- | ----------------------------------------------- |
| Test Case ID  | TC-CART-022                                     |
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
The Payment page displayed the Name on Card, Card Number, CVC, Expiration Month, and Expiration Year fields. The Pay and Confirm Order button was also displayed.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
All required payment fields and the Pay and Confirm Order control were available on the Payment page.

---

## TC-CART-023 – Verify mandatory validation for blank Name on Card

**Scenario:** TS-CART-16

| Field         | Details                    |
| ------------- | -------------------------- |
| Test Case ID  | TC-CART-023                |
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
All payment fields were left blank and Pay and Confirm Order was clicked. The application displayed the browser validation message “Please fill out this field.” for the Name on Card field and prevented further submission.

**Status:**
PASS

**Defect ID:**
N/A

**Comments:**
Mandatory-field validation was triggered correctly for the blank Name on Card field, and the payment form did not proceed until the required field was entered.

---

## TC-CART-024 – Verify mandatory validation for blank Card Number

**Scenario:** TS-CART-16

| Field         | Details                    |
| ------------- | -------------------------- |
| Test Case ID  | TC-CART-024                |
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

## TC-CART-025 – Verify mandatory validation for blank CVC

**Scenario:** TS-CART-16

| Field         | Details                    |
| ------------- | -------------------------- |
| Test Case ID  | TC-CART-025                |
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

## TC-CART-026 – Verify mandatory validation for blank Expiration Month

**Scenario:** TS-CART-16

| Field         | Details                    |
| ------------- | -------------------------- |
| Test Case ID  | TC-CART-026                |
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

## TC-CART-027 – Verify mandatory validation for blank Expiration Year

**Scenario:** TS-CART-16

| Field         | Details                    |
| ------------- | -------------------------- |
| Test Case ID  | TC-CART-027                |
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

## TC-CART-028 – Verify Payment field input format handling

**Scenario:** TS-CART-17

| Field         | Details                     |
| ------------- | --------------------------- |
| Test Case ID  | TC-CART-028                 |
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

## TC-CART-029 – Verify successful order placement with supported payment data

**Scenario:** TS-CART-18

| Field         | Details                                        |
| ------------- | ---------------------------------------------- |
| Test Case ID  | TC-CART-029                                    |
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

## TC-CART-030 – Verify Order Confirmation message

**Scenario:** TS-CART-18

| Field         | Details                               |
| ------------- | ------------------------------------- |
| Test Case ID  | TC-CART-030                           |
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

## TC-CART-031 – Verify Order Confirmation page information

**Scenario:** TS-CART-19

| Field         | Details                            |
| ------------- | ---------------------------------- |
| Test Case ID  | TC-CART-031                        |
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

## TC-CART-032 – Verify Download Invoice functionality

**Scenario:** TS-CART-20

| Field         | Details                            |
| ------------- | ---------------------------------- |
| Test Case ID  | TC-CART-032                        |
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

## TC-CART-033 – Verify Continue after Order Confirmation

**Scenario:** TS-CART-21

| Field         | Details                            |
| ------------- | ---------------------------------- |
| Test Case ID  | TC-CART-033                        |
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

## TC-CART-034 – Verify post-order order history or tracking availability

**Scenario:** TS-CART-22

| Field         | Details                                                |
| ------------- | ------------------------------------------------------ |
| Test Case ID  | TC-CART-034                                            |
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

## TC-CART-035 – Verify Cart state after successful order placement

**Scenario:** TS-CART-18

| Field         | Details                               |
| ------------- | ------------------------------------- |
| Test Case ID  | TC-CART-035                           |
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
| Total Test Cases |     35 |
| Passed           |      0 |
| Failed           |      0 |
| Blocked          |      0 |
| Not Executed     |     35 |
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

`defects/defect-reports.md`

---

# 8. Retesting and Regression

If a genuine defect is identified and subsequently fixed:

* The failed test case will be executed again for retesting.
* The test result will be updated in this document.
* Related functionality will be tested for regression.
* Retesting and regression results will be documented separately in:

`regression/retesting-regression.md`

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
| TS-CART-12    | TC-CART-017                                                     |
| TS-CART-13    | TC-CART-018, TC-CART-019                                        |
| TS-CART-14    | TC-CART-020, TC-CART-021                                        |
| TS-CART-15    | TC-CART-022                                                     |
| TS-CART-16    | TC-CART-023, TC-CART-024, TC-CART-025, TC-CART-026, TC-CART-027 |
| TS-CART-17    | TC-CART-028                                                     |
| TS-CART-18    | TC-CART-029, TC-CART-030                                        |
| TS-CART-19    | TC-CART-031                                                     |
| TS-CART-20    | TC-CART-032                                                     |
| TS-CART-21    | TC-CART-033                                                     |
| TS-CART-22    | TC-CART-034                                                     |

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
