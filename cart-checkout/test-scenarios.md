# Cart & Checkout Test Scenarios – Automation Exercise

## 1. Module Overview

**Application:** Automation Exercise
**Module:** Cart & Checkout
**Testing Type:** Manual Functional Testing
**Testing Approach:** Exploratory-based test design

This document contains test scenarios identified from exploratory testing of the Cart and Checkout module. The scenarios cover cart behavior, product quantity and price calculation, product removal, checkout access, cart persistence after login, address information, order review, order comments, payment validation, order confirmation, and invoice generation.

---

## 2. Test Scenario Summary

| Scenario ID | Test Scenario                                            | Priority |
| ----------- | -------------------------------------------------------- | -------- |
| TS-CART-01  | Verify Cart page accessibility and empty cart behavior   | High     |
| TS-CART-02  | Verify product display in Cart                           | High     |
| TS-CART-03  | Verify multiple products can be added to Cart            | High     |
| TS-CART-04  | Verify product information displayed in Cart             | High     |
| TS-CART-05  | Verify product quantity in Cart                          | High     |
| TS-CART-06  | Verify product price and total calculation in Cart       | High     |
| TS-CART-07  | Verify product removal from Cart                         | High     |
| TS-CART-08  | Verify Continue On Cart functionality                    | Medium   |
| TS-CART-09  | Verify Proceed To Checkout functionality                 | High     |
| TS-CART-10  | Verify checkout access for a logged-out user             | High     |
| TS-CART-11  | Verify cart persistence after login                      | High     |
| TS-CART-12  | Verify Checkout page and order summary                   | High     |
| TS-CART-13  | Verify Delivery Address and Billing Address display      | High     |
| TS-CART-14  | Verify Order Comment field behavior                      | Medium   |
| TS-CART-15  | Verify Payment page fields and controls                  | High     |
| TS-CART-16  | Verify mandatory validation of Payment fields            | High     |
| TS-CART-17  | Verify Payment field input format handling               | High     |
| TS-CART-18  | Verify successful order confirmation                     | High     |
| TS-CART-19  | Verify Order Confirmation page information               | High     |
| TS-CART-20  | Verify Download Invoice functionality                    | Medium   |
| TS-CART-21  | Verify Continue functionality after order completion     | Medium   |
| TS-CART-22  | Verify post-order order history or tracking availability | Low      |

---

# 3. Detailed Test Scenarios

## TS-CART-01 – Verify Cart Page Accessibility and Empty Cart Behavior

**Objective:**
Verify that the Cart page is accessible and displays the appropriate state when no products are present.

**Precondition:**
Cart does not contain any products.

**Test Conditions:**

* Navigate to the Cart page.
* Observe the cart content.
* Verify the empty-cart message.
* Verify the available navigation option.

**Expected Result:**
The Cart page should be accessible and should display an appropriate message when the cart is empty. The user should be able to navigate to the Products section from the available link.

---

## TS-CART-02 – Verify Product Display in Cart

**Objective:**
Verify that a product added to the cart is displayed correctly.

**Precondition:**
A product has been added to the Cart.

**Test Conditions:**

* Open the Cart page.
* Observe the added product.
* Verify that the product is displayed in the cart table.

**Expected Result:**
The added product should be displayed correctly in the Cart with its relevant cart information.

---

## TS-CART-03 – Verify Multiple Products Can Be Added to Cart

**Objective:**
Verify that multiple different products can be added to the Cart.

**Test Conditions:**

* Add one product to the Cart.
* Add another different product.
* Open the Cart page.
* Observe all products.

**Expected Result:**
All successfully added products should be displayed separately in the Cart.

---

## TS-CART-04 – Verify Product Information Displayed in Cart

**Objective:**
Verify that relevant product information is displayed for products present in the Cart.

**Test Conditions:**

* Add a product to the Cart.
* Open the Cart page.
* Observe the product information.

**Expected Result:**
The Cart should display the relevant product information, including product details, unit price, quantity, and total price.

---

## TS-CART-05 – Verify Selected Product Quantity in Cart

**Objective:**
Verify that the product quantity selected before adding the product is correctly reflected in the Cart.

**Test Conditions:**

* Open a product's details page.
* Increase the product quantity.
* Add the product to the Cart.
* Open the Cart.
* Observe the displayed quantity.

**Expected Result:**
The Cart should display the quantity corresponding to the quantity selected before adding the product.

---

## TS-CART-06 – Verify Product Price and Total Calculation in Cart

**Objective:**
Verify that the product total and overall Cart total are calculated correctly.

**Test Conditions:**

* Add a product to the Cart.
* Observe its unit price and quantity.
* Verify the product total.
* Add another product if required.
* Verify the overall Cart total.

**Expected Result:**
The product total should correspond to its unit price multiplied by the selected quantity. The overall Cart total should correctly reflect the combined totals of the products in the Cart.

---

## TS-CART-07 – Verify Product Removal from Cart

**Objective:**
Verify that a product can be removed from the Cart.

**Test Conditions:**

* Add one or more products to the Cart.
* Open the Cart.
* Remove one product.
* Observe the Cart.
* Remove the remaining product if applicable.

**Expected Result:**
The selected product should be removed from the Cart. If all products are removed, the Cart should display the appropriate empty-cart state.

---

## TS-CART-08 – Verify Continue On Cart Functionality

**Objective:**
Verify the behavior of the Continue On Cart option.

**Precondition:**
At least one product is present in the Cart.

**Test Conditions:**

* Open the Cart.
* Click Continue On Cart.

**Expected Result:**
The user should remain on the Cart page and the existing Cart contents should remain available.

---

## TS-CART-09 – Verify Proceed To Checkout Functionality

**Objective:**
Verify that the user can proceed from the Cart to the Checkout page.

**Precondition:**
At least one product is present in the Cart.

**Test Conditions:**

* Open the Cart.
* Click Proceed To Checkout.
* Observe the resulting page.

**Expected Result:**
The application should proceed to the Checkout flow or display the appropriate authentication requirement based on the user's login state.

---

## TS-CART-10 – Verify Checkout Access for a Logged-Out User

**Objective:**
Verify the checkout behavior when an unauthenticated user attempts to proceed with an order.

**Precondition:**
User is not logged in and a product is present in the Cart.

**Test Conditions:**

* Open the Cart.
* Click Proceed To Checkout.
* Observe the Checkout page.
* Verify the displayed login/register option.
* Click the Register/Login link.

**Expected Result:**
The application should inform the logged-out user that login or registration is required to proceed with checkout. The Register/Login option should redirect the user to the Signup/Login page.

---

## TS-CART-11 – Verify Cart Persistence After Login

**Objective:**
Verify that products added before login remain available after the user logs in.

**Precondition:**
A product has been added to the Cart while the user is logged out.

**Test Conditions:**

* Add a product to the Cart.
* Attempt to proceed to Checkout.
* Log in using valid credentials.
* Return to the Checkout flow.
* Observe the Cart contents.

**Expected Result:**
The product previously added to the Cart should remain available after successful login.

---

## TS-CART-12 – Verify Checkout Page and Order Summary

**Objective:**
Verify that the Checkout page displays the products and order information correctly.

**Precondition:**
User is logged in and products are present in the Cart.

**Test Conditions:**

* Proceed to Checkout.
* Observe the Review Your Order section.
* Verify the products.
* Verify quantities and prices.
* Verify the total amount.

**Expected Result:**
The Checkout page should display the products in the order, their quantities, prices, individual totals, and the overall order total correctly.

---

## TS-CART-13 – Verify Delivery Address and Billing Address Display

**Objective:**
Verify that Delivery Address and Billing Address information is displayed during Checkout.

**Precondition:**
User is logged in and has proceeded to Checkout.

**Test Conditions:**

* Observe the Delivery Address section.
* Observe the Billing Address section.
* Compare the displayed address information.

**Expected Result:**
The Checkout page should display the Delivery Address and Billing Address sections with the available address information.

---

## TS-CART-14 – Verify Order Comment Field Behavior

**Objective:**
Verify that the user can enter an optional comment during Checkout.

**Precondition:**
User is on the Checkout page.

**Test Conditions:**

* Locate the Order Comment field.
* Leave the field blank and continue.
* Repeat the process with a valid comment.
* Observe the subsequent order flow.

**Expected Result:**
The user should be able to proceed without entering a comment. A valid comment should also be accepted without preventing the order process.

**Note:**
Whether the comment is displayed or carried forward to a later page will be recorded as an observation during execution.

---

## TS-CART-15 – Verify Payment Page Fields and Controls

**Objective:**
Verify that the Payment page contains the required payment fields and order confirmation control.

**Precondition:**
User has completed the Checkout information and proceeded to Payment.

**Test Conditions:**

* Verify Name on Card field.
* Verify Card Number field.
* Verify CVC field.
* Verify Expiration Month field.
* Verify Expiration Year field.
* Verify Pay and Confirm Order button.

**Expected Result:**
The Payment page should display all required payment fields and the Pay and Confirm Order control.

---

## TS-CART-16 – Verify Mandatory Validation of Payment Fields

**Objective:**
Verify that the Payment form prevents submission when mandatory fields are blank.

**Test Conditions:**

* Leave all payment fields blank.
* Click Pay and Confirm Order.
* Observe the validation behavior.
* Complete fields sequentially as required and repeat the submission where applicable.

**Expected Result:**
The application should prevent order submission when a required payment field is blank and should display appropriate mandatory-field validation.

---

## TS-CART-17 – Verify Payment Field Input Format Handling

**Objective:**
Verify how the Payment form handles different input formats in payment fields.

**Test Conditions:**

Test the payment fields using inappropriate input formats such as:

* Numeric characters in Name on Card
* Alphabetic characters in Card Number
* Alphabetic characters in CVC
* Alphabetic characters in Expiration Month
* Alphabetic characters in Expiration Year

**Expected Result:**
The application should apply appropriate input validation to payment fields according to the supported field format and validation rules.

**Note:**
The actual behavior for each input format will be recorded during formal execution. Any acceptance of inappropriate input will be evaluated as a potential defect only if the expected validation behavior can be reasonably established and the issue is reproducible.

---

## TS-CART-18 – Verify Successful Order Confirmation

**Objective:**
Verify that an order can be successfully placed using valid payment information.

**Precondition:**
User is logged in and has completed the Checkout process.

**Test Conditions:**

* Enter valid payment information supported by the application.
* Click Pay and Confirm Order.
* Observe the order confirmation.

**Expected Result:**
The application should process the order successfully and display an order confirmation.

---

## TS-CART-19 – Verify Order Confirmation Page Information

**Objective:**
Verify that the Order Confirmation page displays the appropriate confirmation information.

**Precondition:**
An order has been successfully placed.

**Test Conditions:**

* Observe the Order Confirmation page.
* Verify the order status/message.
* Verify the Congratulations message.
* Verify the Continue option.
* Verify the Download Invoice option.

**Expected Result:**
The Order Confirmation page should indicate that the order has been successfully placed and should provide the available post-order options.

---

## TS-CART-20 – Verify Download Invoice Functionality

**Objective:**
Verify that the invoice can be downloaded after successful order placement.

**Precondition:**
An order has been successfully placed.

**Test Conditions:**

* Click Download Invoice.
* Observe the downloaded file.
* Open the downloaded invoice.
* Verify the available order/customer information.

**Expected Result:**
The invoice should be downloaded successfully and should contain the available order/customer information.

---

## TS-CART-21 – Verify Continue Functionality After Order Completion

**Objective:**
Verify the behavior of the Continue option displayed after successful order placement.

**Precondition:**
An order has been successfully placed.

**Test Conditions:**

* Click Continue on the Order Confirmation page.
* Observe the resulting page.

**Expected Result:**
The user should be redirected to the application's home page.

---

## TS-CART-22 – Verify Post-Order Order History or Tracking Availability

**Objective:**
Verify whether the application provides an accessible order history or order tracking section after an order has been placed.

**Precondition:**
User is logged in and has successfully placed an order.

**Test Conditions:**

* Return to the application after order completion.
* Observe the navigation options available to the logged-in user.
* Check for an Order History, My Orders, or Order Tracking section.
* Observe whether previously placed orders can be accessed.

**Expected Result:**
If the application provides an order history or tracking feature, previously placed orders should be accessible through the available navigation.

**Note:**
If no such feature is available in the application, the absence will be recorded as an observation and will not automatically be treated as a defect without a defined requirement.

---

# 4. Test Data

The following test data categories will be used during Cart and Checkout testing:

| Data Type                | Example / Description                                   |
| ------------------------ | ------------------------------------------------------- |
| Product 1                | Madame Top For Women – ₹400                             |
| Product 2                | Summer White Top – ₹1,000                               |
| Single quantity          | Quantity 1                                              |
| Multiple quantity        | Quantity 3                                              |
| Valid login credentials  | Registered test account                                 |
| Order comment            | Generic order comment                                   |
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

# 5. Scope for Test Execution

The following areas will be covered during formal Cart and Checkout testing:

* Empty Cart behavior
* Product display in Cart
* Multiple products
* Product information
* Product quantity
* Price and total calculation
* Product removal
* Continue On Cart
* Proceed To Checkout
* Checkout access for logged-out users
* Cart persistence after login
* Checkout page
* Delivery Address
* Billing Address
* Order review
* Order comments
* Payment page
* Payment mandatory-field validation
* Payment input format handling
* Order confirmation
* Confirmation page
* Invoice download
* Continue after order completion
* Post-order order history or tracking availability

Formal test cases will be created from these scenarios and executed against the live Automation Exercise application.

Any reproducible deviation from the expected behavior will be documented separately as a defect.

