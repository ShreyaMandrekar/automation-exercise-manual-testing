# Products Test Scenarios – Automation Exercise

## 1. Module Overview

**Application:** Automation Exercise
**Module:** Products
**Testing Type:** Manual Functional Testing
**Testing Approach:** Exploratory-based test design

This document contains test scenarios identified from exploratory testing of the Products module. The scenarios cover the Products page, product search, category filtering, brand filtering, product details, quantity handling, Add to Cart functionality, cart information, and product review validation.

---

## 2. Test Scenario Summary

| Scenario ID | Test Scenario                                       | Priority |
| ----------- | --------------------------------------------------- | -------- |
| TS-PROD-01  | Verify Products page accessibility and UI elements  | High     |
| TS-PROD-02  | Verify product listing and product card information | High     |
| TS-PROD-03  | Verify product search with valid keywords           | High     |
| TS-PROD-04  | Verify product search with partial keywords         | Medium   |
| TS-PROD-05  | Verify product search with a non-existing keyword   | Medium   |
| TS-PROD-06  | Verify behavior when the search field is blank      | Medium   |
| TS-PROD-07  | Verify product filtering using Categories           | High     |
| TS-PROD-08  | Verify product filtering using Brands               | High     |
| TS-PROD-09  | Verify Product Details page                         | High     |
| TS-PROD-10  | Verify product quantity behavior                    | Medium   |
| TS-PROD-11  | Verify Add to Cart functionality                    | High     |
| TS-PROD-12  | Verify Cart details after adding a product          | High     |
| TS-PROD-13  | Verify Product Review form fields and validation    | Medium   |
| TS-PROD-14  | Verify invalid email validation in Product Review   | Medium   |
| TS-PROD-15  | Verify successful Product Review submission         | Medium   |

---

# 3. Detailed Test Scenarios

## TS-PROD-01 – Verify Products Page Accessibility and UI Elements

**Objective:**
Verify that the Products page is accessible and contains the expected product-related UI elements.

**Precondition:**
User is on the Automation Exercise application.

**Test Conditions:**

* Navigate to the Products section.
* Verify the Products page is displayed.
* Verify the Search Product field.
* Verify the Categories section.
* Verify the Brands section.
* Verify product listings are displayed.

**Expected Result:**
The Products page should be accessible and the available product-related UI elements should be displayed and usable.

---

## TS-PROD-02 – Verify Product Listing and Product Card Information

**Objective:**
Verify that product cards display the relevant product information and actions.

**Test Conditions:**

* Observe the products displayed on the Products page.
* Verify the product image.
* Verify the product price.
* Verify the Add to Cart option.
* Verify the View Product option.
* Hover over a product card and observe the displayed overlay.

**Expected Result:**
Product cards should display the product image, price, Add to Cart option, and View Product option. Hovering over a product card should display the observed product overlay without affecting the availability of the product actions.

---

## TS-PROD-03 – Verify Product Search with Valid Keywords

**Objective:**
Verify that the product search functionality displays products matching a valid search keyword.

**Test Data Examples:**

* `jeans`
* `tshirt`
* `saree`

**Test Conditions:**

* Enter a valid product-related keyword in the Search Product field.
* Click the search button.
* Observe the search results.

**Expected Result:**
Products relevant to the entered search keyword should be displayed and the search results should be shown appropriately.

---

## TS-PROD-04 – Verify Product Search with Partial Keywords

**Objective:**
Verify that the product search functionality handles partial product keywords.

**Test Data Examples:**

* `top`
* `tops`
* `sare`

**Test Conditions:**

* Enter a partial product keyword.
* Perform the search.
* Observe the displayed products.

**Expected Result:**
The application should display products relevant to the entered search term according to its search behavior.

**Note:**
The search behavior observed during exploratory testing will be recorded during formal execution.

---

## TS-PROD-05 – Verify Product Search with a Non-Existing Keyword

**Objective:**
Verify the behavior of the Products page when no products match the entered search keyword.

**Test Data:**
A product keyword that does not correspond to an available product.

**Test Conditions:**

* Enter a non-existing product keyword.
* Perform the search.
* Observe the product listing area.

**Expected Result:**
No unrelated products should be displayed when the search keyword does not match any available product. The application should handle the empty result state without displaying incorrect product results.

**Note:**
The presence or absence of a specific “No products found” message will be recorded as an observation during execution.

---

## TS-PROD-06 – Verify Behavior When the Search Field Is Blank

**Objective:**
Verify the behavior of the product search when no search keyword is entered.

**Test Conditions:**

* Leave the Search Product field blank.
* Perform the search.
* Observe the Products page.

**Expected Result:**
The application should process the blank search without displaying an incorrect search result, and the resulting product listing should be recorded during execution.

---

## TS-PROD-07 – Verify Product Filtering Using Categories

**Objective:**
Verify that products can be filtered using the available product categories and subcategories.

**Categories Observed:**

### Women

* Dress
* Tops
* Saree

### Men

* T-shirt
* Jeans

### Kids

* Dress
* Tops & Shirts

**Test Conditions:**

* Expand a main product category.
* Select a subcategory.
* Observe the displayed products and page heading.
* Repeat the test for applicable categories and subcategories.

**Expected Result:**
Selecting a category or subcategory should display products relevant to the selected category and update the product listing appropriately.

---

## TS-PROD-08 – Verify Product Filtering Using Brands

**Objective:**
Verify that products can be filtered according to the selected brand.

**Brands Observed:**

* Polo
* H&M
* Madame
* Mast & Harbour
* Babyhug
* Allen Solly Junior
* Kookie Kids
* Biba

**Test Conditions:**

* Select a brand from the Brands section.
* Observe the product listing.
* Verify the page heading.
* Verify that the displayed products are associated with the selected brand.
* Verify that the product count displayed beside the selected brand is consistent with the products shown.

**Expected Result:**
The application should display products associated with the selected brand and update the product listing appropriately.

---

## TS-PROD-09 – Verify Product Details Page

**Objective:**
Verify that selecting View Product displays the relevant product details.

**Test Conditions:**

* Select View Product for a product.
* Observe the Product Details page.

**Expected Result:**
The Product Details page should display the available product information and actions, including:

* Product image
* Product name
* Category
* Price
* Rating
* Quantity
* Add to Cart
* Availability
* Condition
* Brand
* Write Your Review section

---

## TS-PROD-10 – Verify Product Quantity Behavior

**Objective:**
Verify that the quantity of a product can be adjusted before adding it to the cart.

**Test Conditions:**

* Open a product's details page.
* Observe the default quantity.
* Increase the product quantity.
* Attempt to decrease the quantity.
* Observe the minimum quantity behavior.

**Expected Result:**
The quantity control should allow the quantity to be adjusted according to the application's supported behavior and should not allow the user to set a quantity below the minimum supported value.

---

## TS-PROD-11 – Verify Add to Cart Functionality

**Objective:**
Verify that a product can be successfully added to the cart.

**Precondition:**
A product is available on the Products page.

**Test Conditions:**

* Open a product using View Product.
* Select the required quantity.
* Click Add to Cart.
* Observe the confirmation message.
* Verify the Continue Shopping option.
* Verify the View Cart option.

**Expected Result:**
The selected product should be added to the cart and an appropriate confirmation should be displayed. Continue Shopping and View Cart options should be available.

---

## TS-PROD-12 – Verify Cart Details After Adding a Product

**Objective:**
Verify that the product added from the Products module is correctly displayed in the cart.

**Precondition:**
A product has been successfully added to the cart.

**Test Conditions:**

* Select View Cart after adding a product.
* Observe the product displayed in the cart.
* Verify the product quantity.
* Verify the available product information.

**Expected Result:**
The cart should display the added product with the selected quantity and relevant product information such as condition and brand.

---

## TS-PROD-13 – Verify Product Review Form Fields and Validation

**Objective:**
Verify that the Product Review form contains the required fields and validates mandatory input.

**Test Conditions:**

* Open a product's details page.
* Locate the Write Your Review section.
* Verify the Name field.
* Verify the Email field.
* Verify the Review field.
* Submit the form without entering any data.
* Enter the Name while leaving Email blank and submit.
* Enter valid Email while leaving Review blank and submit.

**Expected Result:**
The review form should prevent submission when required fields are blank and should display appropriate validation feedback.

---

## TS-PROD-14 – Verify Invalid Email Validation in Product Review

**Objective:**
Verify that the Product Review form validates the email address format.

**Test Conditions:**

* Enter a valid Name.
* Enter an invalid email address.
* Enter a Review.
* Submit the review.

**Examples of invalid email formats:**

* `test`
* `test@`
* Other invalid email formats

**Expected Result:**
The application should prevent submission of an invalid email address and display appropriate email-format validation.

---

## TS-PROD-15 – Verify Successful Product Review Submission

**Objective:**
Verify that a user can successfully submit a product review using valid information.

**Test Data:**

* Valid Name
* Valid email address
* Valid review text

**Test Conditions:**

* Open the Product Details page.
* Enter a valid Name.
* Enter a valid Email.
* Enter a review.
* Click Submit.

**Expected Result:**
The review should be submitted successfully and an appropriate confirmation message should be displayed.

---

# 4. Test Data

The following test data categories will be used during Products testing:

| Data Type              | Example / Description                                                             |
| ---------------------- | --------------------------------------------------------------------------------- |
| Valid search keyword   | `jeans`, `tshirt`, `saree`                                                        |
| Partial search keyword | `top`, `tops`, `sare`                                                             |
| Non-existing keyword   | A keyword with no matching product                                                |
| Blank search           | Empty Search Product field                                                        |
| Category               | Women, Men, Kids                                                                  |
| Subcategory            | Dress, Tops, Saree, T-shirt, Jeans, Tops & Shirts                                 |
| Brand                  | Polo, H&M, Madame, Mast & Harbour, Babyhug, Allen Solly Junior, Kookie Kids, Biba |
| Valid review name      | Generic test name                                                                 |
| Valid review email     | Generic test email                                                                |
| Valid review text      | Generic review content                                                            |
| Invalid review email   | `test`, `test@`                                                                   |

**Note:**
Test data will be selected appropriately during execution. Real personal information or credentials will not be used in the public test documentation.

---

# 5. Scope for Test Execution

The following areas will be covered during formal Products testing:

* Products page accessibility
* Product card information
* Product search
* Partial keyword search
* Non-existing product search
* Blank search behavior
* Category filtering
* Brand filtering
* Product Details page
* Product quantity
* Add to Cart
* Cart product information
* Product Review form
* Mandatory-field validation
* Review email validation
* Successful review submission

Formal test cases will be created from these scenarios and executed against the live Automation Exercise application.

Any reproducible deviation from the expected behavior will be documented separately as a defect.

