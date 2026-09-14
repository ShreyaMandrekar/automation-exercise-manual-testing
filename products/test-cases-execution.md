# Products Test Cases & Execution – Automation Exercise

## 1. Module Information

| Field            | Details                                    |
| ---------------- | ------------------------------------------ |
| Application      | Automation Exercise                        |
| Module           | Products                                   |
| Testing Type     | Manual Testing                             |
| Test Level       | System Testing                             |
| Test Approach    | Functional, Positive, Negative, Validation |
| Test Case Status | Not Executed                               |
| Tester           | Shreya Mandrekar                           |

---

## 2. Objective

The objective of these test cases is to verify the Products functionality of the Automation Exercise application, including:

* Products page accessibility
* Product listing and product card information
* Product search
* Partial keyword search
* Non-existing product search
* Blank search behavior
* Category filtering
* Brand filtering
* Product Details page
* Product quantity behavior
* Add to Cart functionality
* Cart product information
* Product Review form
* Mandatory-field validation
* Review email validation
* Successful Product Review submission

All Actual Results and Status values will be updated after executing the test cases against the live application.

---

## 3. Preconditions

Unless otherwise specified:

1. Automation Exercise website is accessible.
2. Tester has access to a web browser.
3. Products page is accessible.
4. Test data is prepared before execution.
5. A product is available for test cases requiring product details.
6. The browser is not displaying stale search results from a previous test case unless specifically required.

---

# 4. Test Case Execution

## TC-PROD-001 – Verify Products page is accessible

**Scenario:** TS-PROD-01

| Field         | Details                   |
| ------------- | ------------------------- |
| Test Case ID  | TC-PROD-001               |
| Priority      | High                      |
| Preconditions | Application is accessible |
| Test Data     | N/A                       |

**Steps:**

1. Open Automation Exercise.
2. Navigate to the Products section.
3. Observe the Products page.

**Expected Result:**
The Products page should open successfully and display the available product-related sections and product listings.

**Actual Result:**
The Products section was opened successfully. All products were loaded, and the “All Products” heading was displayed. The Search Product field, Categories section, and Brands section were also visible.

**Status:** PASS

**Defect ID:** N/A

**Comments:**
Products page loaded successfully with the expected product listing and main product-related UI sections.

---

## TC-PROD-002 – Verify Products page UI elements

**Scenario:** TS-PROD-01

| Field         | Details                     |
| ------------- | --------------------------- |
| Test Case ID  | TC-PROD-002                 |
| Priority      | High                        |
| Preconditions | Products page is accessible |
| Test Data     | N/A                         |

**Steps:**

1. Open the Products page.
2. Verify the Search Product field.
3. Verify the Categories section.
4. Verify the Brands section.
5. Verify the product listing area.
6. Verify the promotional banner if displayed.

**Expected Result:**
The Products page should display the available product-related UI elements correctly and they should be accessible for interaction where applicable.

**Actual Result:**
The Products page displayed the Search Product field, Categories section with Women, Men and Kids and their respective subcategories, Brands section with available brands, and the product listing area. The promotional banner was also displayed. All observed UI elements were displayed properly, and no UI issue was observed.

**Status:** PASS

**Defect ID:** N/A

**Comments:**
The Products page UI elements were displayed correctly during execution with no visible UI issues.

---

## TC-PROD-003 – Verify product card information

**Scenario:** TS-PROD-02

| Field         | Details                     |
| ------------- | --------------------------- |
| Test Case ID  | TC-PROD-003                 |
| Priority      | High                        |
| Preconditions | Products page is accessible |
| Test Data     | N/A                         |

**Steps:**

1. Observe the products displayed on the Products page.
2. Select a product card.
3. Verify the product image.
4. Verify the product price.
5. Verify the Add to Cart option.
6. Verify the View Product option.

**Expected Result:**
Product cards should display the product image, price, Add to Cart option, and View Product option.

**Actual Result:**
Product cards were displayed on the Products page with the product image, product name, price, Add to Cart button, and View Product option. Both Add to Cart and View Product were functioning correctly. No abnormal behavior was observed.

**Status:** PASS

**Defect ID:** N/A

**Comments:**
Product card information and available product actions worked as expected during execution.

---

## TC-PROD-004 – Verify product card hover behavior

**Scenario:** TS-PROD-02

| Field         | Details                     |
| ------------- | --------------------------- |
| Test Case ID  | TC-PROD-004                 |
| Priority      | Medium                      |
| Preconditions | Products page is accessible |
| Test Data     | Any displayed product       |

**Steps:**

1. Open the Products page.
2. Move the mouse pointer over a product card.
3. Observe the product card.

**Expected Result:**
The product card should display the available hover overlay without preventing access to the product actions.

**Actual Result:**
When hovering over a product card, an orange overlay appeared over the product card and highlighted the product information and Add to Cart option. The hover behavior worked correctly without preventing access to the product actions.

**Status:** PASS

**Defect ID:** N/A

**Comments:**
Product card hover behavior worked as expected during execution.

---

## TC-PROD-005 – Verify product search with valid keyword

**Scenario:** TS-PROD-03

| Field         | Details                     |
| ------------- | --------------------------- |
| Test Case ID  | TC-PROD-005                 |
| Priority      | High                        |
| Preconditions | Products page is accessible |
| Test Data     | `jeans`                     |

**Steps:**

1. Open the Products page.
2. Enter `jeans` in the Search Product field.
3. Click the search button.
4. Observe the search results.
5. Verify the displayed products.

**Expected Result:**
Products relevant to the `jeans` search keyword should be displayed.

**Actual Result:**
Entered jeans in the Search Product field and performed the search successfully. Only jeans-related products were displayed. The page heading changed from “All Products” to “Search Products”, and jeans remained in the search field. The Categories and Brands sections remained visible. No unexpected behavior was observed.

**Status:** PASS

**Defect ID:** N/A

**Comments:**
Valid keyword search using jeans worked as expected.

---

## TC-PROD-006 – Verify product search with T-shirt keyword

**Scenario:** TS-PROD-03

| Field         | Details                     |
| ------------- | --------------------------- |
| Test Case ID  | TC-PROD-006                 |
| Priority      | High                        |
| Preconditions | Products page is accessible |
| Test Data     | `tshirt`                    |

**Steps:**

1. Open the Products page.
2. Enter `tshirt` in the Search Product field.
3. Click the search button.
4. Observe the search results.

**Expected Result:**
Products relevant to T-shirts should be displayed for the entered search keyword.

**Actual Result:**
Entered tshirt in the Search Product field and performed the search successfully. Only T-shirt-related products were displayed. The page heading changed to “Search Products”, and tshirt remained in the search field. The Categories and Brands sections remained visible. No unexpected behavior was observed.

**Status:** PASS

**Defect ID:** N/A

**Comments:**
Search using the keyword tshirt displayed the expected T-shirt-related products.

---

## TC-PROD-007 – Verify product search with Saree keyword

**Scenario:** TS-PROD-03

| Field         | Details                     |
| ------------- | --------------------------- |
| Test Case ID  | TC-PROD-007                 |
| Priority      | High                        |
| Preconditions | Products page is accessible |
| Test Data     | `saree`                     |

**Steps:**

1. Open the Products page.
2. Enter `saree` in the Search Product field.
3. Click the search button.
4. Observe the search results.

**Expected Result:**
Products relevant to sarees should be displayed.

**Actual Result:**
Entered saree in the Search Product field and performed the search successfully. Only saree-related products were displayed. The page heading changed to “Search Products”, and saree remained in the search field. The Categories and Brands sections remained visible. No unexpected behavior was observed.

**Status:** PASS

**Defect ID:** N/A

**Comments:**
Search using the keyword saree displayed the expected saree-related products.

---

## TC-PROD-008 – Verify product search with partial keyword

**Scenario:** TS-PROD-04

| Field         | Details                     |
| ------------- | --------------------------- |
| Test Case ID  | TC-PROD-008                 |
| Priority      | Medium                      |
| Preconditions | Products page is accessible |
| Test Data     | `top`                       |

**Steps:**

1. Open the Products page.
2. Enter `top` in the Search Product field.
3. Click the search button.
4. Observe the displayed products.

**Expected Result:**
The application should display products relevant to the entered partial search term according to its search behavior.

**Actual Result:**
Entered top in the Search Product field and performed the search successfully. Products related to tops were displayed. The page heading changed to “Search Products”, and top remained in the search field. The Categories and Brands sections remained visible. No unexpected behavior was observed.

**Status:** PASS

**Defect ID:** N/A

**Comments:**
Partial keyword search using top displayed the expected top-related products.

---

## TC-PROD-009 – Verify product search using alternative partial keywords

**Scenario:** TS-PROD-04

| Field         | Details                     |
| ------------- | --------------------------- |
| Test Case ID  | TC-PROD-009                 |
| Priority      | Medium                      |
| Preconditions | Products page is accessible |
| Test Data     | `tops`, `sare`              |

**Steps:**

1. Search for `tops`.
2. Observe the displayed products.
3. Clear the search field.
4. Search for `sare`.
5. Observe the displayed products.

**Expected Result:**
The application should process each partial search term and display products relevant to the entered search term according to its search behavior.

**Actual Result:**
Searched for tops and clicked the search button. All relevant tops products were displayed and the page heading changed to “Search Products”. The Categories and Brands sections remained visible.

Searched for sare and clicked the search button. Relevant saree products were displayed and the page heading remained “Search Products”. The Categories and Brands sections remained visible. No unexpected behavior was observed in either search.

**Status:** PASS

**Defect ID:** N/A

**Comments:**
Partial keyword searches using tops and sare displayed the expected related products.

---

## TC-PROD-010 – Verify search with a non-existing keyword

**Scenario:** TS-PROD-05

| Field         | Details                            |
| ------------- | ---------------------------------- |
| Test Case ID  | TC-PROD-010                        |
| Priority      | Medium                             |
| Preconditions | Products page is accessible        |
| Test Data     | A keyword with no matching product |

**Steps:**

1. Open the Products page.
2. Enter a non-existing product keyword.
3. Click the search button.
4. Observe the product listing area.

**Expected Result:**
No unrelated products should be displayed when the search keyword does not match any available product. The application should handle the empty result state without displaying incorrect product results.

**Actual Result:**
Entered xyzabc123 in the Search Product field and clicked the search button. The page heading changed to “Search Products”. No products were displayed and the product area appeared blank/white. The Categories and Brands sections remained visible. No “No products found” message was displayed. No unexpected error occurred.

**Status:** PASS

**Defect ID:** N/A

**Comments:**
The application handled the non-existing search without displaying unrelated products. The absence of a specific “No products found” message was recorded as an observation and was not classified as a defect because no explicit requirement for such a message is available.

---

## TC-PROD-011 – Verify blank search behavior

**Scenario:** TS-PROD-06

| Field         | Details                     |
| ------------- | --------------------------- |
| Test Case ID  | TC-PROD-011                 |
| Priority      | Medium                      |
| Preconditions | Products page is accessible |
| Test Data     | Blank search                |

**Steps:**

1. Open the Products page.
2. Leave the Search Product field blank.
3. Click the search button.
4. Observe the resulting product listing.

**Expected Result:**
The application should process the blank search without displaying an incorrect search result, and the resulting product listing should be recorded during execution.

**Actual Result:**
Left the Search Product field blank and clicked the search button. The page refreshed and all products were displayed again. The heading remained “All Products”, and the Categories and Brands sections remained visible. No unexpected behavior was observed.

**Status:** PASS

**Defect ID:** N/A

**Comments:**
Blank search refreshed the Products page and displayed all products as expected.

---

## TC-PROD-012 – Verify search result heading and search field behavior

**Scenario:** TS-PROD-03

| Field         | Details                     |
| ------------- | --------------------------- |
| Test Case ID  | TC-PROD-012                 |
| Priority      | Medium                      |
| Preconditions | Products page is accessible |
| Test Data     | `jeans`                     |

**Steps:**

1. Open the Products page.
2. Enter `jeans` in the Search Product field.
3. Perform the search.
4. Observe the Search Product field.
5. Observe the page heading.
6. Observe the Categories and Brands sections.

**Expected Result:**
The entered search term should remain available in the search field where supported. The search results should be identified appropriately, and the surrounding Categories and Brands sections should remain available unless the application is designed to hide them.

**Actual Result:**
Before searching, the page heading was “All Products”. After entering jeans in the Search Product field and clicking the search button, the heading changed to “Search Products”. The jeans keyword remained in the search field, and only jeans-related products were displayed. The Categories and Brands sections remained visible. No unexpected behavior was observed.

**Status:** PASS

**Defect ID:** N/A

**Comments:**
The search heading and search field behaved as expected during a valid product search.

---

## TC-PROD-013 – Verify Women category filtering

**Scenario:** TS-PROD-07

| Field         | Details                     |
| ------------- | --------------------------- |
| Test Case ID  | TC-PROD-013                 |
| Priority      | High                        |
| Preconditions | Products page is accessible |
| Test Data     | Women → Dress               |

**Steps:**

1. Open the Products page.
2. Expand the Women category.
3. Verify the available Women subcategories.
4. Select Dress.
5. Observe the displayed products.
6. Observe the page heading.

**Expected Result:**
The selected Women subcategory should display relevant products and the product listing should update appropriately.

**Actual Result:**
Under Categories, selected Women and clicked Dress. The page heading changed to “Women Dress Product” and the available dress products were displayed. The Categories and Brands sections remained visible. No unexpected behavior was observed.

**Status:** PASS

**Defect ID:** N/A

**Comments:**
Women → Dress category filtering displayed the expected dress products and heading.

---

## TC-PROD-014 – Verify Women category subcategories

**Scenario:** TS-PROD-07

| Field         | Details                     |
| ------------- | --------------------------- |
| Test Case ID  | TC-PROD-014                 |
| Priority      | High                        |
| Preconditions | Products page is accessible |
| Test Data     | Women → Dress, Tops, Saree  |

**Steps:**

1. Expand the Women category.
2. Verify Dress is available.
3. Verify Tops is available.
4. Verify Saree is available.
5. Select each subcategory.
6. Observe the displayed products.

**Expected Result:**
The Women category should display the observed subcategories, and selecting each subcategory should display relevant products.

**Actual Result:**
Under the Women category, the Dress, Tops, and Saree subcategories were selected individually. The respective headings changed to “Women Dress Product”, “Women Tops Product”, and “Women Saree Product”, and the corresponding products were displayed for each subcategory. The Categories and Brands sections remained visible in all three subcategory views. The promotional banner and Search Product field were not displayed on the subcategory pages. The category page layout and product display worked as observed, with no unexpected behavior.

**Status:** PASS

**Defect ID:** N/A

**Comments:**
Women subcategory filtering for Dress, Tops, and Saree displayed the corresponding products and category headings as expected.

---

## TC-PROD-015 – Verify Men category filtering

**Scenario:** TS-PROD-07

| Field         | Details                     |
| ------------- | --------------------------- |
| Test Case ID  | TC-PROD-015                 |
| Priority      | High                        |
| Preconditions | Products page is accessible |
| Test Data     | Men → Jeans                 |

**Steps:**

1. Open the Products page.
2. Expand the Men category.
3. Verify the available Men subcategories.
4. Select Jeans.
5. Observe the displayed products and page heading.

**Expected Result:**
The selected Men subcategory should display relevant products and update the product listing appropriately.

**Actual Result:**
Under the Men category, expanded the subcategories and selected Jeans. The page heading changed to “Men Jeans Product” and the relevant jeans products were displayed. The breadcrumb was displayed above the product section, and the Categories and Brands sections remained visible. No unexpected behavior was observed.

**Status:** PASS

**Defect ID:** N/A

**Comments:**
Men → Jeans category filtering displayed the expected jeans products and heading.

---

## TC-PROD-016 – Verify Men category subcategories

**Scenario:** TS-PROD-07

| Field         | Details                     |
| ------------- | --------------------------- |
| Test Case ID  | TC-PROD-016                 |
| Priority      | High                        |
| Preconditions | Products page is accessible |
| Test Data     | Men → T-shirt, Jeans        |

**Steps:**

1. Expand the Men category.
2. Verify T-shirt is available.
3. Verify Jeans is available.
4. Select each subcategory.
5. Observe the displayed products.

**Expected Result:**
The Men category should display the observed subcategories, and selecting each subcategory should display relevant products.

**Actual Result:**
Under the Men category, the T-shirt and Jeans subcategories were selected individually. The corresponding page heading was displayed for each selection, and the relevant T-shirt and jeans products were shown. The breadcrumb was displayed above the product section. The Categories and Brands sections remained visible for both subcategories. No unexpected behavior was observed.

**Status:** PASS

**Defect ID:** N/A

**Comments:**
Men subcategory filtering for T-shirt and Jeans displayed the corresponding products and category headings as expected.

---

## TC-PROD-017 – Verify Kids category filtering

**Scenario:** TS-PROD-07

| Field         | Details                     |
| ------------- | --------------------------- |
| Test Case ID  | TC-PROD-017                 |
| Priority      | High                        |
| Preconditions | Products page is accessible |
| Test Data     | Kids → Dress, Tops & Shirts |

**Steps:**

1. Open the Products page.
2. Expand the Kids category.
3. Verify Dress is available.
4. Verify Tops & Shirts is available.
5. Select each subcategory.
6. Observe the displayed products.

**Expected Result:**
The Kids category should display the observed subcategories, and selecting each subcategory should display relevant products.

**Actual Result:**
Under the Kids category, the Dress and Tops & Shirts subcategories were selected individually. The “Kids Dress Product” heading was displayed for Dress, and the corresponding dress products were shown. For Tops & Shirts, the heading changed accordingly and the relevant tops and shirts were displayed. The breadcrumb was displayed above the product section, and the Categories and Brands sections remained visible for both subcategories. No layout changes or unexpected behavior were observed.

**Status:** PASS

**Defect ID:** N/A

**Comments:**
Kids subcategory filtering for Dress and Tops & Shirts displayed the corresponding products and headings as expected.

---

## TC-PROD-018 – Verify brand filtering

**Scenario:** TS-PROD-08

| Field         | Details                     |
| ------------- | --------------------------- |
| Test Case ID  | TC-PROD-018                 |
| Priority      | High                        |
| Preconditions | Products page is accessible |
| Test Data     | Polo                        |

**Steps:**

1. Open the Products page.
2. Locate the Brands section.
3. Select Polo.
4. Observe the product listing.
5. Observe the page heading.
6. Verify the displayed products.

**Expected Result:**
The application should display products associated with the selected brand and update the product listing and page heading appropriately.

**Actual Result:**
Clicked on Polo under the Brands section. The page heading changed to “Brand Polo Product” and Polo-related products were displayed. The Categories and Brands sections remained visible. A breadcrumb was displayed above the product section, indicating Products and Polo. No unexpected behavior was observed.

**Status:** PASS

**Defect ID:** N/A

**Comments:**
Brand filtering for Polo displayed the expected Polo-related products and brand heading.

---

## TC-PROD-019 – Verify available brand list

**Scenario:** TS-PROD-08

| Field         | Details                     |
| ------------- | --------------------------- |
| Test Case ID  | TC-PROD-019                 |
| Priority      | Medium                      |
| Preconditions | Products page is accessible |
| Test Data     | N/A                         |

**Steps:**

1. Open the Products page.
2. Locate the Brands section.
3. Verify the observed brand names.
4. Verify that a product count is displayed beside the brands where applicable.

**Expected Result:**
The Brands section should display the available brands and associated product counts where provided by the application.

**Actual Result:**
The Brands section displayed all available brands, including Polo, H&M, Madame, Mast & Harbour, Babyhug, Allen Solly Junior, Kookie Kids, and Biba. The brand options were accessible, and selecting the brands displayed their respective products with the corresponding heading. No unexpected behavior was observed.

**Status:** PASS

**Defect ID:** N/A

**Comments:**
All listed brands were displayed and accessible, and brand selection displayed the corresponding products correctly.

---

## TC-PROD-020 – Verify brand product count consistency

**Scenario:** TS-PROD-08

| Field         | Details                     |
| ------------- | --------------------------- |
| Test Case ID  | TC-PROD-020                 |
| Priority      | Medium                      |
| Preconditions | Products page is accessible |
| Test Data     | Polo                        |

**Steps:**

1. Observe the product count displayed beside Polo in the Brands section.
2. Select Polo.
3. Count or otherwise verify the products displayed for the selected brand.
4. Compare the displayed count with the products shown.

**Expected Result:**
The product count displayed for the selected brand should be consistent with the products available for that brand.

**Actual Result:**
The Polo brand displayed a count of 6 next to the brand name. After selecting Polo, exactly 6 Polo-related products were displayed. The displayed brand count matched the number of products shown. No unexpected behavior was observed.

**Status:** PASS

**Defect ID:** N/A

**Comments:**
The Polo brand count matched the number of corresponding products displayed.

---

## TC-PROD-021 – Verify Product Details page

**Scenario:** TS-PROD-09

| Field         | Details                     |
| ------------- | --------------------------- |
| Test Case ID  | TC-PROD-021                 |
| Priority      | High                        |
| Preconditions | Products page is accessible |
| Test Data     | Any available product       |

**Steps:**

1. Open the Products page.
2. Select View Product for a product.
3. Observe the Product Details page.
4. Verify the product image.
5. Verify the product name.
6. Verify the category.
7. Verify the price.
8. Verify the rating.
9. Verify quantity.
10. Verify Add to Cart.
11. Verify Availability.
12. Verify Condition.
13. Verify Brand.
14. Verify the Write Your Review section.

**Expected Result:**
The Product Details page should display the available product information and actions correctly.

**Actual Result:**
Opened a product using View Product. The product details page displayed the product image, name, category, rating, price, quantity controls, Add to Cart button, availability, condition, brand, and Write Your Review section with Name, Email, Review, and Submit fields. The Categories and Brands sections were also visible. No unexpected behavior was observed.

**Status:** PASS

**Defect ID:** N/A

**Comments:**
Product details and available product information and actions were displayed correctly.

---

## TC-PROD-022 – Verify product quantity can be increased

**Scenario:** TS-PROD-10

| Field         | Details                            |
| ------------- | ---------------------------------- |
| Test Case ID  | TC-PROD-022                        |
| Priority      | Medium                             |
| Preconditions | Product Details page is accessible |
| Test Data     | Any available product              |

**Steps:**

1. Open a product's details page.
2. Observe the default quantity.
3. Increase the quantity.
4. Observe the displayed quantity.

**Expected Result:**
The quantity should increase according to the application's supported quantity behavior.

**Actual Result:**
The initial product quantity was 1. Clicking the upper arrow increased the quantity successfully. The selected product remained unchanged while the quantity was increased. The quantity control also provided an up arrow and down arrow for increasing and decreasing the quantity. The quantity could not be decreased below 1.

**Status:** PASS

**Defect ID:** N/A

**Comments:**
Product quantity increased correctly using the quantity control, while the selected product remained unchanged.

---

## TC-PROD-023 – Verify product quantity minimum behavior

**Scenario:** TS-PROD-10

| Field         | Details                            |
| ------------- | ---------------------------------- |
| Test Case ID  | TC-PROD-023                        |
| Priority      | Medium                             |
| Preconditions | Product Details page is accessible |
| Test Data     | Any available product              |

**Steps:**

1. Open a product's details page.
2. Observe the default quantity.
3. Attempt to decrease the quantity.
4. Continue attempting to decrease the quantity below the minimum.
5. Observe the quantity control.

**Expected Result:**
The quantity control should not allow the user to set a quantity below the minimum supported value.

**Actual Result:**
The quantity was decreased using the down arrow until it reached 1. Clicking the down arrow again did not reduce the quantity further. The quantity did not become 0 or a negative value, and no error message was displayed. 1 remained the minimum quantity.

**Status:** PASS

**Defect ID:** N/A

**Comments:**
The quantity control correctly maintained 1 as the minimum value and prevented further decrease.

---

## TC-PROD-024 – Verify Add to Cart functionality

**Scenario:** TS-PROD-11

| Field         | Details                            |
| ------------- | ---------------------------------- |
| Test Case ID  | TC-PROD-024                        |
| Priority      | High                               |
| Preconditions | Product Details page is accessible |
| Test Data     | Any available product              |

**Steps:**

1. Open a product using View Product.
2. Select the required quantity.
3. Click Add to Cart.
4. Observe the confirmation popup.

**Expected Result:**
The selected product should be added to the cart and an appropriate confirmation should be displayed.

**Actual Result:**
The product was added to the cart successfully with quantity 1. A confirmation popup displayed “Added! Your product has been added to cart.” The popup provided a View Cart link and a green Continue Shopping button. Clicking View Cart redirected to the cart page, while clicking Continue Shopping kept the user on the same product page. No unexpected behavior was observed.

**Status:** PASS

**Defect ID:** N/A

**Comments:**
The Add to Cart functionality worked correctly, and both View Cart and Continue Shopping options behaved as expected.

---

## TC-PROD-025 – Verify Continue Shopping option after Add to Cart

**Scenario:** TS-PROD-11

| Field         | Details                            |
| ------------- | ---------------------------------- |
| Test Case ID  | TC-PROD-025                        |
| Priority      | Medium                             |
| Preconditions | Product has been added to the cart |
| Test Data     | Any available product              |

**Steps:**

1. Add a product to the cart.
2. Observe the Add to Cart confirmation.
3. Click Continue Shopping.
4. Observe the resulting page.

**Expected Result:**
The Continue Shopping option should be available and should allow the user to continue browsing products.

**Actual Result:**
*To be updated during execution.*

**Status:** NOT EXECUTED

**Defect ID:** N/A

**Comments:**
*To be updated during execution.*

---

## TC-PROD-026 – Verify View Cart option after Add to Cart

**Scenario:** TS-PROD-11

| Field         | Details                            |
| ------------- | ---------------------------------- |
| Test Case ID  | TC-PROD-026                        |
| Priority      | High                               |
| Preconditions | Product has been added to the cart |
| Test Data     | Any available product              |

**Steps:**

1. Add a product to the cart.
2. Observe the Add to Cart confirmation.
3. Click View Cart.
4. Observe the Cart page.

**Expected Result:**
The View Cart option should open the Cart page successfully.

**Actual Result:**
*To be updated during execution.*

**Status:** NOT EXECUTED

**Defect ID:** N/A

**Comments:**
*To be updated during execution.*

---

## TC-PROD-027 – Verify product quantity in Cart

**Scenario:** TS-PROD-12

| Field         | Details                                         |
| ------------- | ----------------------------------------------- |
| Test Case ID  | TC-PROD-027                                     |
| Priority      | High                                            |
| Preconditions | Product has been added with a selected quantity |
| Test Data     | Any available product and selected quantity     |

**Steps:**

1. Open a product's details page.
2. Set a quantity greater than the default quantity.
3. Add the product to the cart.
4. Open the Cart.
5. Observe the product quantity.

**Expected Result:**
The Cart should display the added product with the same quantity selected before adding it to the cart.

**Actual Result:**
*To be updated during execution.*

**Status:** NOT EXECUTED

**Defect ID:** N/A

**Comments:**
Record the selected quantity and displayed Cart quantity.

---

## TC-PROD-028 – Verify product information in Cart

**Scenario:** TS-PROD-12

| Field         | Details                            |
| ------------- | ---------------------------------- |
| Test Case ID  | TC-PROD-028                        |
| Priority      | High                               |
| Preconditions | Product has been added to the cart |
| Test Data     | Any available product              |

**Steps:**

1. Add a product to the cart.
2. Open the Cart.
3. Observe the added product.
4. Verify the available product information.
5. Verify the product condition and brand where displayed.

**Expected Result:**
The Cart should display the added product and its available product information correctly, including condition and brand where provided.

**Actual Result:**
*To be updated during execution.*

**Status:** NOT EXECUTED

**Defect ID:** N/A

**Comments:**
*To be updated during execution.*

---

## TC-PROD-029 – Verify Product Review mandatory-field validation

**Scenario:** TS-PROD-13

| Field         | Details                            |
| ------------- | ---------------------------------- |
| Test Case ID  | TC-PROD-029                        |
| Priority      | Medium                             |
| Preconditions | Product Details page is accessible |
| Test Data     | Blank Name, Email and Review       |

**Steps:**

1. Open a Product Details page.
2. Locate the Write Your Review section.
3. Leave Name blank.
4. Leave Email blank.
5. Leave Review blank.
6. Click Submit.
7. Enter a Name while leaving Email and Review blank.
8. Click Submit.
9. Enter a valid Email while leaving Review blank.
10. Click Submit.

**Expected Result:**
The review form should prevent submission when required fields are blank and should display appropriate validation feedback for the missing fields.

**Actual Result:**
*To be updated during execution.*

**Status:** NOT EXECUTED

**Defect ID:** N/A

**Comments:**
Record the exact validation message and the field on which validation is triggered.

---

## TC-PROD-030 – Verify invalid email validation in Product Review

**Scenario:** TS-PROD-14

| Field         | Details                            |
| ------------- | ---------------------------------- |
| Test Case ID  | TC-PROD-030                        |
| Priority      | Medium                             |
| Preconditions | Product Details page is accessible |
| Test Data     | `test`, `test@`                    |

**Steps:**

1. Open a Product Details page.
2. Enter a valid Name.
3. Enter `test` in the Email field.
4. Enter valid Review text.
5. Click Submit.
6. Repeat using `test@` as the email address.

**Expected Result:**
The application should prevent submission of invalid email formats and display appropriate email-format validation.

**Actual Result:**
*To be updated during execution.*

**Status:** NOT EXECUTED

**Defect ID:** N/A

**Comments:**
Record the exact browser/application validation messages displayed for each invalid email format.

---

## TC-PROD-031 – Verify successful Product Review submission

**Scenario:** TS-PROD-15

| Field         | Details                                    |
| ------------- | ------------------------------------------ |
| Test Case ID  | TC-PROD-031                                |
| Priority      | Medium                                     |
| Preconditions | Product Details page is accessible         |
| Test Data     | Valid Name, valid email, valid review text |

**Steps:**

1. Open a Product Details page.
2. Enter a valid Name.
3. Enter a valid Email.
4. Enter valid Review text.
5. Click Submit.
6. Observe the result.

**Expected Result:**
The review should be submitted successfully and an appropriate confirmation message should be displayed.

**Actual Result:**
*To be updated during execution.*

**Status:** NOT EXECUTED

**Defect ID:** N/A

**Comments:**
Record the exact confirmation message displayed after successful submission.

---

# 5. Test Execution Summary

| Metric           | Result |
| ---------------- | -----: |
| Total Test Cases |     31 |
| Passed           |      0 |
| Failed           |      0 |
| Blocked          |      0 |
| Not Executed     |     31 |
| Defects Raised   |      0 |

**Execution Summary:**

A total of 31 Products test cases have been designed based on the Products test scenarios and exploratory testing observations. Formal execution against the live Automation Exercise application has not yet been completed.

Actual results, execution statuses, and defect IDs will be updated during formal test execution.

---

# 6. Execution Status Definitions

| Status       | Meaning                                      |
| ------------ | -------------------------------------------- |
| PASS         | Actual result matches expected result        |
| FAIL         | Actual result does not match expected result |
| BLOCKED      | Test cannot be executed because of a blocker |
| NOT EXECUTED | Test has not yet been executed               |

---

# 7. Test Data

The following data categories will be used during Products testing:

| Data Type              | Example / Description                                                             |
| ---------------------- | --------------------------------------------------------------------------------- |
| Valid search keyword   | `jeans`, `tshirt`, `saree`                                                        |
| Partial search keyword | `top`, `tops`, `sare`                                                             |
| Non-existing keyword   | A keyword with no matching product                                                |
| Blank search           | Empty Search Product field                                                        |
| Category               | Women, Men, Kids                                                                  |
| Subcategory            | Dress, Tops, Saree, T-shirt, Jeans, Tops & Shirts                                 |
| Brand                  | Polo, H&M, Madame, Mast & Harbour, Babyhug, Allen Solly Junior, Kookie Kids, Biba |
| Product                | Any available product selected during execution                                   |
| Product quantity       | Default quantity and an increased quantity                                        |
| Valid review name      | Generic test name                                                                 |
| Valid review email     | Generic test email                                                                |
| Valid review text      | Generic review content                                                            |
| Invalid review email   | `test`, `test@`                                                                   |

**Note:**
Test data will be selected appropriately during execution. Real personal information or credentials will not be used in the public test documentation.

---

# 8. Execution Environment

| Field            | Details                             |
| ---------------- | ----------------------------------- |
| Application URL  | https://www.automationexercise.com/ |
| Browser          | To be updated during execution      |
| Operating System | To be updated during execution      |
| Execution Period | To be updated during execution      |

---

# 9. Traceability

| Test Scenario | Related Test Cases                                              |
| ------------- | --------------------------------------------------------------- |
| TS-PROD-01    | TC-PROD-001, TC-PROD-002                                        |
| TS-PROD-02    | TC-PROD-003, TC-PROD-004                                        |
| TS-PROD-03    | TC-PROD-005, TC-PROD-006, TC-PROD-007, TC-PROD-012              |
| TS-PROD-04    | TC-PROD-008, TC-PROD-009                                        |
| TS-PROD-05    | TC-PROD-010                                                     |
| TS-PROD-06    | TC-PROD-011                                                     |
| TS-PROD-07    | TC-PROD-013, TC-PROD-014, TC-PROD-015, TC-PROD-016, TC-PROD-017 |
| TS-PROD-08    | TC-PROD-018, TC-PROD-019, TC-PROD-020                           |
| TS-PROD-09    | TC-PROD-021                                                     |
| TS-PROD-10    | TC-PROD-022, TC-PROD-023                                        |
| TS-PROD-11    | TC-PROD-024, TC-PROD-025, TC-PROD-026                           |
| TS-PROD-12    | TC-PROD-027, TC-PROD-028                                        |
| TS-PROD-13    | TC-PROD-029                                                     |
| TS-PROD-14    | TC-PROD-030                                                     |
| TS-PROD-15    | TC-PROD-031                                                     |

---

# 10. Notes

These test cases were derived from:

* Products exploratory testing observations
* Products test scenarios
* Application functionality
* Standard functional testing practices
* Positive and negative test conditions
* Input validation scenarios

The test cases are independently designed for this QA portfolio project and are not copied from the official Automation Exercise test cases.

Expected results are based on the documented test scenarios and observed application behavior. Where an exact requirement is not available, the expected result is intentionally kept objective and the observed behavior will be evaluated during execution.

Exploratory observations are not automatically classified as defects.

A defect will be reported only when:

* The test case has actually been executed.
* The observed behavior differs from the applicable expected result.
* The behavior is reproducible.
* The issue can be clearly documented.
* A Jira defect is created where appropriate.

After execution, the failed test cases and corresponding Jira defect IDs, if any, will be recorded in this document.

Retesting and regression results will be documented separately if a genuine defect is fixed.
