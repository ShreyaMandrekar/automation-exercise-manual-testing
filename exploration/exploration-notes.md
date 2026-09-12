# Automation Exercise – Exploration Notes

## 1. Purpose

This document records observations made during exploratory testing of the Automation Exercise web application. The purpose of this exploration was to understand the application's functionality, user flows, input fields, validations, and observed behavior before designing formal test scenarios and test cases.

## 2. Application Under Test

**Application:** Automation Exercise
**Testing Type:** Manual Exploratory Testing
**Module Explored:** Registration / Signup
**Testing Approach:** Exploratory testing based on direct interaction with the application.

---

## 3. Registration / Signup Module

### 3.1 Initial Signup Page

The Signup/Login page contains two sections:

* **Login to your account**
* **New User Signup**

The New User Signup section contains:

* Name
* Email Address
* Signup button

### 3.2 Initial Signup Field Observations

| Field         | Observation                                                                                                                                                                                 |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Name          | Required. Leaving the field blank displays a validation message asking the user to fill the field. Numeric characters were accepted during exploration.                                     |
| Email Address | Required. Leaving the field blank displays a validation message. Invalid email formats were rejected in some cases, including an email without `@` and an incomplete email ending with `@`. |
| Signup button | Clicking Signup with valid initial details opens the account creation form.                                                                                                                 |

---

## 4. Account Creation Form

After submitting the initial Signup form with valid details, the application displays the account creation form.

### 4.1 Account Creation Fields

| No. | Field          | Type / Control  | Observation                                                                                       |
| --: | -------------- | --------------- | ------------------------------------------------------------------------------------------------- |
|   1 | Title          | Radio button    | Mr. and Mrs. options are available. Blank selection was accepted during exploration.              |
|   2 | Name           | Text field      | Value is carried from the initial Signup step.                                                    |
|   3 | Email          | Email field     | Value is carried from the initial Signup step.                                                    |
|   4 | Password       | Password field  | Required. Blank value was not accepted. Short password values were accepted during exploration.   |
|   5 | Date of Birth  | Dropdown fields | Day, month and year controls are available.                                                       |
|   6 | Newsletter     | Checkbox        | Unselected by default. Registration worked with both selected and unselected states.              |
|   7 | Special Offers | Checkbox        | Unselected by default. Registration worked with both selected and unselected states.              |
|   8 | First Name     | Text field      | Required during account creation.                                                                 |
|   9 | Last Name      | Text field      | Required during account creation.                                                                 |
|  10 | Company        | Text field      | Input was accepted during exploration.                                                            |
|  11 | Address        | Text field      | Required. Blank value was not accepted. Numeric and text values were accepted during exploration. |
|  12 | Address 2      | Text field      | Blank value was accepted.                                                                         |
|  13 | Country        | Dropdown        | India was selected by default. Multiple country options were available.                           |
|  14 | State          | Text field      | Required. Blank value was not accepted.                                                           |
|  15 | City           | Text field      | Required. Blank value was not accepted.                                                           |
|  16 | Zipcode        | Text field      | Required. Blank value was not accepted. Character input was accepted during exploration.          |
|  17 | Mobile Number  | Text field      | Required. Blank value was not accepted. Character input was accepted during exploration.          |

---

## 5. Newsletter and Special Offers

### Newsletter

* Control type: Checkbox
* Default state: Unselected
* Selecting the checkbox: Registration remained successful.
* Leaving the checkbox unselected: Registration remained successful.
* Observed as an optional field during exploration.

### Special Offers

* Control type: Checkbox
* Default state: Unselected
* Selecting the checkbox: Registration remained successful.
* Leaving the checkbox unselected: Registration remained successful.
* Observed as an optional field during exploration.

---

## 6. Country Dropdown

The Country field is presented as a dropdown.

The following options were observed:

1. India
2. United States
3. Canada
4. Australia
5. Israel
6. New Zealand
7. Singapore

**Default selection observed:** India

---

## 7. Successful Registration Flow

A complete registration was performed using test data.

### Test Data Used

| Field          | Test Data                           |
| -------------- | ----------------------------------- |
| Title          | Mr.                                 |
| Name           | QA Tester                           |
| Email          | [Test@123.com](mailto:Test@123.com) |
| Password       | 123                                 |
| Date of Birth  | 7 September 2009                    |
| Newsletter     | Selected                            |
| Special Offers | Selected                            |
| First Name     | QA                                  |
| Last Name      | Tester                              |
| Company        | Software                            |
| Address        | Thane                               |
| Address 2      | Thane 2                             |
| Country        | India                               |
| State          | Maharashtra                         |
| City           | Kalyan                              |
| Zipcode        | 561302                              |
| Mobile Number  | 857-345-2345                        |

### Observed Result

1. The Create Account button was clicked after entering the registration details.
2. An Account Created confirmation page appeared.
3. The page displayed a successful account creation message.
4. A Continue button was displayed.
5. Clicking Continue redirected to the Home page.
6. The logged-in user's name, **QA Tester**, was displayed.
7. Logout and Delete Account options were available.

---

## 8. Logout Flow

### Action

The Logout option was selected from the logged-in user's navigation.

### Observed Result

* The user was successfully logged out.
* The application redirected to the Signup/Login page.

---

## 9. Account Deletion Flow

### Action

The Delete Account option was selected while logged in.

### Observed Result

* An account deletion confirmation page appeared.
* The page indicated that the account had been permanently deleted.
* A Continue button was displayed.
* Clicking Continue redirected to the Home page.

---

## 10. Observations Requiring Further Formal Testing

The following behaviors were observed during exploration and should be investigated more systematically when formal test cases are created:

* Name field accepted numeric characters.
* Email validation behavior should be tested with different valid and invalid formats.
* A short password value was accepted during exploration.
* Date of Birth field behavior should be tested with valid, invalid and boundary values.
* Address field accepted numeric and text input.
* Zipcode field accepted character input during exploration.
* Mobile Number field accepted character input during exploration.

These observations are **not automatically classified as defects**. They require comparison against the expected requirements and formal test execution before a defect is reported.

---

## 11. Exploration Summary

The Registration module was explored from the initial Signup page through:

**Signup → Account Creation → Successful Registration → Logged-in State → Logout → Account Deletion**

The exploration identified the available registration fields, input controls, mandatory/optional behavior observed during exploration, validation behavior, dropdown values, and the complete account lifecycle.

Formal test scenarios and detailed test cases will be created after completing the exploratory phase.

---

# Login / Logout – Exploratory Observations

## Login Page

The Login section is available through the Signup/Login page.

The Login form contains:

* Email Address field
* Password field
* Login button

## Valid Login

* A registered email address and the corresponding correct password were entered.
* Clicking the Login button successfully redirected to the Home page.
* The logged-in user's name was displayed on the Home page.

## Invalid Credentials

* An incorrect email address with a password displayed:
  `Your email or password is incorrect.`
* A correct registered email address with an incorrect password displayed the same message:
  `Your email or password is incorrect.`
* An unregistered email address also displayed:
  `Your email or password is incorrect.`
* The application therefore uses the same error message for different invalid-credential combinations.

## Email Format Validation

The Login email field performs browser-level email validation.

Observed behavior:

* Entering `test` displayed:
  `Please include an @ in the email address. 'test' is missing an '@'.`
* Entering `test@` displayed:
  `Please enter a part following '@'. 'test@' is incomplete.`
* An email containing a space in the middle was rejected with:
  `The part followed by @ should not contain the symbol ' '.`
* Entering only spaces in the email field did not allow login and displayed a validation message.

## Mandatory Field Validation

* When both Email Address and Password fields were blank and Login was clicked, validation was first displayed for the Email Address field:
  `Please fill out this field.`
* After entering a valid email address while leaving Password blank, clicking Login displayed:
  `Please fill out this field.`
  for the Password field.
* Validation therefore occurs sequentially, with the first missing mandatory field being validated before the next missing field.

## Password Behavior

* Entered password characters are masked and displayed as dots.
* No eye/show-password icon was available.
* The password could not be viewed in plain text through the Login form.

## Logout and Re-login

* After successful login, selecting Logout redirected the user to the Signup/Login page.
* After logout, the user could log in again using valid credentials.
* A subsequent successful login again redirected to the Home page and displayed the logged-in user's name.

## Browser Back Button After Logout

* After logging out and being redirected to the Signup/Login page, pressing the browser Back button did not restore the logged-in session.
* The application remained in a logged-out state.
* The logged-in user's authenticated state was not restored through browser navigation.

## Email Case Behavior

* A registered email address entered using uppercase characters with the correct password was rejected.
* The application displayed:
  `Your email or password is incorrect.`
* This behavior was recorded as an observation and not classified as a defect because no explicit requirement was available stating that email addresses must be treated as case-insensitive.

## Leading and Trailing Spaces

* An email address entered with leading and/or trailing spaces was accepted.
* Login was successful and the user was redirected to the Home page.
* This behavior was recorded as an observation. No defect was raised because the observed behavior did not prevent successful authentication and no explicit requirement was available defining how surrounding whitespace must be handled.

## Exploratory Testing Conclusion

The Login functionality was explored across successful authentication, invalid credentials, email-format validation, mandatory-field validation, password masking, logout/re-login, browser navigation after logout, email case handling, and whitespace handling.

The observations from this exploration will be used as input for designing the formal Login test scenarios and test cases.

---

# Products – Exploratory Observations

## Products Page

The Products section is accessible from the main navigation of the Automation Exercise application.

The Products page contains:

* A promotional banner displaying **“Special Offer / Big Sale / Up to 50% Off”**
* Search Product field
* Product listings
* Product cards with product image, price, Add to Cart and View Product options
* Product Categories section
* Brands section

The promotional banner was visible during exploration but was not clickable.

## Product Cards

Each product card displayed:

* Product image
* Product price
* Add to Cart option
* View Product option

When hovering over a product card, an orange overlay appeared containing product information and an Add to Cart option.

## Product Search

The Search Product field was used to explore product search behavior.

Observed behavior:

* Searching for `tops` displayed matching top-related products.
* Searching for `top` displayed the same set of products observed for `tops`.
* Searching for `sare` displayed saree-related products.
* Searching for `tshirt` displayed T-shirt-related products.
* Searching for `jeans` displayed jeans-related products.
* The entered search text remained visible in the search field after the search was performed.
* When a search was performed, the page heading changed from **“All Products”** to **“Search Products”**.
* Only products matching the search term were displayed.
* The Categories and Brands sections remained visible while displaying search results.
* Searching for a non-existing product resulted in a blank product area. No explicit “No products found” or similar message was displayed.
* Performing a blank search refreshed the page and displayed the available products again.

These search behaviors were recorded as observations and were not classified as defects because no explicit requirement for search-result messaging or search matching behavior was available.

## Product Categories

The Categories section is available on the left side of the Products page.

The main categories observed were:

* Women
* Men
* Kids

### Women Category

Expanding the Women category displayed:

* Dress
* Tops
* Saree

Selecting a Women subcategory displayed products related to that subcategory.

For example, selecting **Dress** displayed dress-related products and changed the page heading to **“Women Dress Product”**.

### Men Category

Expanding the Men category displayed:

* T-shirt
* Jeans

Selecting a Men subcategory displayed products related to the selected category.

For example, selecting **Jeans** displayed jeans-related products and changed the product listing accordingly.

### Kids Category

Expanding the Kids category displayed:

* Dress
* Tops & Shirts

Selecting a Kids subcategory displayed products related to the selected category.

Category selection successfully changed the displayed products and the corresponding page heading.

## Brands

The Brands section is available on the left side of the Products page.

The following brands were observed:

1. Polo
2. H&M
3. Madame
4. Mast & Harbour
5. Babyhug
6. Allen Solly Junior
7. Kookie Kids
8. Biba

The number of products available for a brand was displayed in parentheses beside the brand name.

Selecting a brand filtered the product listing to products associated with that brand.

For example, selecting **Polo**:

* Changed the page heading to **“Brand Polo Product”**
* Displayed products associated with the Polo brand
* Displayed products across applicable product categories

## Product Details

Selecting **View Product** opened the product detail page.

The product detail page displayed:

* Product image
* Product name
* Category
* Price
* Rating
* Quantity
* Add to Cart button
* Availability
* Condition
* Brand
* Write Your Review section

The review section contained:

* Name
* Email
* Review
* Submit button

## Product Quantity

The quantity control was explored on the product detail page.

Observed behavior:

* The default quantity was displayed.
* The quantity could be increased during exploration.
* The quantity control did not allow the quantity to be reduced below its minimum value during the observed interaction.

The exact boundary behavior should be covered through formal test cases.

## Add to Cart

The Add to Cart functionality was tested from the product detail page.

Observed behavior:

1. A product was opened using View Product.
2. The quantity was selected.
3. Add to Cart was clicked.
4. A confirmation popup appeared indicating that the product had been added to the cart.
5. A **Continue Shopping** button was available.
6. A **View Cart** link was available.
7. Selecting View Cart opened the Cart page.
8. The added product was displayed in the cart with the selected quantity.
9. Product information including condition and brand was visible in the cart.

## Product Review

The Write Your Review section was explored using different input combinations.

Observed validation behavior:

* Submitting the form with all fields blank displayed the browser validation message:
  `Please fill out this field.`
* After entering a Name while leaving Email blank, submitting the form displayed the same mandatory-field validation for the Email field.
* Entering an invalid email address without `@` triggered browser-level email validation.
* After entering a valid email while leaving the Review field blank, submitting the form displayed mandatory-field validation for the Review field.
* After entering valid Name, Email and Review values, submitting the review displayed the green confirmation message:
  **“Thank you for your review”**

The review form therefore performs mandatory-field and email-format validation during the observed interaction.

## Observations Requiring Further Formal Testing

The following behaviors were observed during exploratory testing and should be investigated more systematically during formal test execution:

* Search matching behavior for different search terms and partial terms.
* Behavior when no products match a search.
* Behavior of a blank search.
* Category filtering for Women, Men and Kids.
* Brand filtering and product count displayed beside brands.
* Product quantity increase and minimum quantity behavior.
* Cart quantity consistency after adding a product.
* Product information displayed in the cart.
* Product review mandatory-field validation.
* Product review email-format validation.
* Successful review submission.

These observations are **not automatically classified as defects**. They should be compared with expected requirements or application behavior during formal test execution before raising any defect.

## Exploratory Testing Conclusion

The Products module was explored across:

**Products Page → Search → Categories → Brands → Product Details → Quantity → Add to Cart → Cart → Product Review**

The exploration identified the main product listing components, search behavior, category and brand filtering, product detail information, quantity behavior, Add to Cart flow, and product review validation.

The observations from this exploration will be used as input for designing the formal Products test scenarios and detailed test cases.

