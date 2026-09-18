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

---

# Cart & Checkout – Exploratory Observations

## Cart Page

The Cart section is accessible from the main navigation of the Automation Exercise application.

### Empty Cart

When the Cart was opened without any products added, the following message was displayed:

**“Cart is empty! Click here to buy products”**

The word **“here”** was displayed as a hyperlink.

Selecting the **“here”** link redirected to the Products section.

### Cart with a Product

A product was added to the cart from the Product Details page.

After opening the Cart:

* The added product was displayed successfully.
* Product information was displayed in tabular form.
* The Cart page displayed a **Proceed To Checkout** button.
* A **Continue On Cart** button was also available.

Selecting **Continue On Cart** kept the user on the Cart page.

---

## Multiple Products in Cart

Two different products were added to the Cart:

1. **Madame Top For Women** – ₹400
2. **Summer White Top** – ₹1,000

Both products were displayed correctly in the Cart.

The quantities were initially set to 1 for both products.

The total amount displayed for the two products was calculated correctly:

**₹400 + ₹1,000 = ₹1,400**

No unexpected calculation behavior was observed.

---

## Removing Products from Cart

The remove functionality was explored with two products in the Cart.

### Removing One Product

When the first product was removed:

* The first product was removed successfully.
* The second product remained displayed in the Cart.

### Removing the Last Product

When the remaining product was removed:

* The Cart became empty.
* The message **“Cart is empty! Click here to buy products”** was displayed.
* The **“here”** hyperlink was available for navigation back to Products.

The Cart correctly handled removal of both individual and final products during exploration.

---

## Cart Quantity and Price Calculation

The quantity and price calculation behavior was explored using **Madame Top For Women**.

The product price was **₹400** per item.

The quantity was increased from 1 to 3 before proceeding to the Cart.

The Cart displayed:

* Product: Madame Top For Women
* Unit price: ₹400
* Quantity: 3
* Total: ₹1,200

The calculation was correct:

**₹400 × 3 = ₹1,200**

A second product, **Summer White Top**, was also present with quantity 1 and a total of ₹1,000.

The combined total displayed was:

**₹1,200 + ₹1,000 = ₹2,200**

The Cart total matched the expected calculation during exploration.

---

## Checkout Access

The **Proceed To Checkout** functionality was explored with a product in the Cart.

When Proceed To Checkout was selected while the user was not logged in:

* The Checkout page was displayed.
* A message indicated that the user must **login/register an account to proceed with checkout**.
* A **Register/Login** hyperlink was available.
* Selecting the hyperlink redirected to the Signup/Login section.
* A **Continue On Cart** button was also displayed.
* Selecting Continue On Cart kept the user on the Cart page.

Checkout therefore required the user to be logged in before proceeding with the order.

---

## Cart Persistence After Login

A product had been added to the Cart before logging in.

After navigating to the Signup/Login section and successfully logging in:

* The previously added product remained in the Cart.
* The product was available when returning to the Checkout flow.

The previously added Cart item was therefore retained after login during the observed flow.

---

# Checkout Page

After logging in, selecting **Proceed To Checkout** opened the Checkout page.

The Checkout page displayed:

* Delivery Address
* Billing Address
* Review Your Order section

---

## Delivery and Billing Address

The Checkout page displayed the Delivery Address and Billing Address side by side.

During exploration:

* The Delivery Address was displayed.
* The Billing Address was displayed.
* Both addresses contained the same address details.
* No Edit or Change option was visible.
* The displayed address information appeared static during the observed checkout flow.

No address modification functionality was observed during exploration.

---

## Review Your Order

The **Review Your Order** section displayed the products in tabular form.

For the tested order:

* **Madame Top For Women**
  * Quantity: 3
  * Price: ₹400 per item
  * Total: ₹1,200
* **Summer White Top**
  * Quantity: 1
  * Price: ₹1,000
  * Total: ₹1,000

The overall total displayed was:

**₹2,200**

The displayed totals matched the observed product quantities and prices.

---

## Order Comment

The Checkout page contained a field with the instruction:

**“If you would like to add a comment about your order, please write it in the field below.”**

### Blank Comment

The order comment field was left blank during one checkout attempt.

The order was allowed to proceed without entering a comment.

### Entered Comment

The following test comment was entered during another checkout attempt:

**“Please handle the product carefully do not fold”**

The order proceeded to the Payment page successfully.

The entered comment was not visibly displayed on the subsequent Payment page during the observed flow.

This behavior was recorded as an observation and was not classified as a defect because no explicit requirement was available stating that the comment must be displayed on the Payment page.

---

# Payment Page

After selecting the option to place the order, the Payment page was displayed.

The Payment page contained:

* Name on Card
* Card Number
* CVC
* Expiration Month
* Expiration Year
* Pay and Confirm Order button

Only dummy test data was used during payment exploration.

---

## Payment Mandatory Field Validation

The Pay and Confirm Order button was selected without entering payment details.

The browser displayed mandatory-field validation sequentially.

Observed behavior:

1. Name on Card displayed:
   **“Please fill out this field.”**
2. After entering a value in Name on Card, Card Number displayed:
   **“Please fill out this field.”**
3. After entering a value in Card Number, CVC displayed:
   **“Please fill out this field.”**
4. After entering a value in CVC, Expiration Month displayed:
   **“Please fill out this field.”**
5. After entering a value in Expiration Month, Expiration Year displayed:
   **“Please fill out this field.”**

The form therefore performed mandatory-field validation sequentially for the payment fields.

---

## Payment Input Format Observation

During exploration, values that were not appropriate numeric formats were entered into the payment fields to observe the application's validation behavior.

The following values were used:

| Field | Test Input |
|---|---|
| Name on Card | `123` |
| Card Number | `ABC` |
| CVC | `ABC` |
| Expiration Month | `AB` |
| Expiration Year | `ABCD` |

The payment form accepted these entered values and allowed the order to proceed to confirmation.

This behavior was recorded as an **exploratory observation** and was not automatically classified as a defect. Formal test cases should be used to determine the expected validation behavior for each payment field before raising a defect.

---

# Order Confirmation

After selecting **Pay and Confirm Order**:

* A confirmation message appeared near the payment section indicating that the order was confirmed.
* The application redirected to the order confirmation page.
* The page displayed:
  **“Order Placed!”**
* A confirmation message displayed:
  **“Congratulations, your order has been confirmed.”**
* A **Continue** button was displayed.
* A **Download Invoice** button was displayed.

The order was successfully completed during the observed flow.

---

## Download Invoice

The **Download Invoice** option was selected after successful order completion.

A text invoice file was downloaded successfully.

The downloaded invoice contained:

* Customer name
* Total purchase amount
* Thank-you message

The invoice displayed the customer's name and total purchase amount for the completed order.

---

## Continue After Order Completion

The **Continue** button on the order confirmation page was selected.

The application redirected the user to the Home page.

---

# Post-Order Order History / Tracking Observation

After completing the order, the application was explored for visible order-history or order-tracking functionality.

During the observed session:

* No separate order history section was visible in the navigation.
* No order tracking option was visible.
* The logged-in username was displayed but was not clickable for accessing an order/profile section.
* The completed order was not visibly listed anywhere in the observed navigation after returning to the application.

This was recorded as an exploratory observation and was **not classified as a defect**, because no explicit requirement was available stating that the application must provide order history or order tracking.

---

# Observations Requiring Further Formal Testing

The following behaviors were identified during Cart & Checkout exploratory testing and should be investigated through formal test cases:

* Empty Cart behavior and navigation to Products.
* Adding single and multiple products to the Cart.
* Removing individual products.
* Removing the final product from the Cart.
* Cart quantity and price calculations.
* Cart persistence after login.
* Checkout access for logged-out and logged-in users.
* Delivery and Billing Address display.
* Availability of address editing functionality.
* Review Your Order details and total calculation.
* Blank order comment behavior.
* Order comment handling after proceeding to Payment.
* Payment mandatory-field validation.
* Payment field input-format validation.
* Successful payment and order confirmation.
* Invoice download.
* Invoice content.
* Continue navigation after order completion.
* Availability of order history/tracking after order completion.

These observations are **not automatically classified as defects**. They should be compared with the applicable expected results and formally executed before raising any defect.

---

# Exploratory Testing Conclusion

The Cart & Checkout functionality was explored across:

**Empty Cart → Add Product → Multiple Products → Remove Product → Quantity & Calculation → Checkout → Login → Address → Review Order → Order Comment → Payment → Order Confirmation → Invoice → Continue**

The exploration covered the main Cart and Checkout user flow, product quantities and calculations, authentication requirement, address display, order review, order comments, payment validation, order confirmation, invoice download, and post-order navigation.

The observations from this exploration will be used as input for designing the formal **Cart & Checkout test scenarios and detailed test cases**.

The observations from this exploration will be used as input for designing the formal Products test scenarios and detailed test cases.

---

# Contact Us – Exploratory Observations

## Contact Us Page

The Contact Us section is accessible from the main navigation of the Automation Exercise application.

The Contact Us page contains:

* Name field
* Email field
* Subject field
* Your Message Here field
* Choose File option
* Submit button
* Feedback For Us informational section
* Feedback email address
* Test Case Templates link/button

The right side of the page displays feedback-related information and the email address:

**[feedback@automationexercise.com](mailto:feedback@automationexercise.com)**

A **Test Case Templates** link/button was also visible above the contact form.

---

## Contact Us Form Fields

The following fields and controls were observed during exploration:

| Field / Control   | Type                 | Observation                                                                                                               |
| ----------------- | -------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| Name              | Text field           | Optional during the observed interaction. Normal text, alphanumeric input, numbers and special characters were accepted.  |
| Email             | Email field          | Required. Blank and invalid email formats were rejected by browser-level validation.                                      |
| Subject           | Text field           | Optional during the observed interaction. Normal text, numbers and special characters were accepted.                      |
| Your Message Here | Multiline text field | Optional during the observed interaction. Normal and long text were accepted. No visible length restriction was observed. |
| Choose File       | File upload          | Optional during the observed interaction. Text and image files were accepted.                                             |
| Submit            | Button               | Submits the Contact Us form after required validation and confirmation handling.                                          |

---

## Name Field Behavior

The Name field was explored using different types of input.

Observed behavior:

* Leaving the Name field blank did not prevent the form from being submitted when a valid email address was provided.
* Normal text was accepted.
* Alphanumeric input was accepted.
* Numbers and special characters were also accepted.
* The form was successfully submitted with these observed Name values.

The Name field behavior was recorded as an observation and was not classified as a defect because no explicit requirement was available stating that the field must accept alphabetic characters only.

---

## Email Validation

The Email field was identified as a mandatory field during exploration.

### Blank Email

When the form was submitted without entering an Email value:

* The Name field was skipped.
* The Email field was highlighted.
* The browser displayed:
  **“Please fill out this field.”**

The form did not proceed until an Email value was entered.

### Invalid Email Without @

The value:

`test`

was entered in the Email field.

The browser displayed:

**“Please include an @ symbol in the email address. Test is missing an @ symbol.”**

### Incomplete Email Ending With @

The value:

`test@`

was entered.

The browser displayed a validation message indicating that a part following `@` was required and that the email address was incomplete.

### Valid Email

The value:

`test@example.com`

was entered.

The Email field accepted the value and the form was allowed to proceed.

The observed behavior indicates that the Email field performs browser-level mandatory and email-format validation.

---

## Subject Field Behavior

The Subject field was explored using different input types.

Observed behavior:

* Normal text was accepted.
* Numbers and special characters were accepted.
* The form was successfully submitted with these observed Subject values.
* Leaving the Subject field blank did not prevent successful submission when a valid Email was provided.

The Subject field was therefore observed as optional during exploration.

---

## Message Field Behavior

The **Your Message Here** field was explored using different message lengths and input values.

Observed behavior:

* Normal text was accepted.
* The form could be submitted with a normal message.
* A long message was also accepted.
* No visible character or length restriction was observed during exploration.
* Leaving the Message field blank did not prevent successful form submission when a valid Email was provided.

The Message field was therefore observed as optional during exploration.

---

## File Upload

The Choose File control was explored with and without a file.

### Without File

The form was submitted without selecting a file.

The submission was successful.

The file upload was therefore observed as optional.

### Text File

A text file was selected using the Choose File control.

The form accepted the selected file and was submitted successfully.

### Image File

An image file was selected using the Choose File control.

The form accepted the selected image file and was submitted successfully.

No visible file-type restriction was observed for the tested text and image files.

No file-size restriction was observed during the exploration.

---

## Contact Form Submission

The form was submitted using valid Email data with different combinations of optional fields.

Observed behavior:

* The form could be submitted with the Name field blank.
* The form could be submitted with the Subject field blank.
* The form could be submitted with the Message field blank.
* The form could be submitted without selecting a file.
* The form could be submitted with normal values in the available fields.
* The form could be submitted with an attached text file.
* The form could be submitted with an attached image file.

After successful submission, the application displayed:

**“Success, your detail has been submitted successfully.”**

A **Home** button was displayed below the success message.

---

## Submit Confirmation Dialog

When the Contact Us form was submitted with entered details, a confirmation dialog was displayed:

**“Please press OK to proceed.”**

### Selecting OK

When **OK** was selected:

* The confirmation dialog was closed.
* The Contact Us form was submitted successfully.
* The message **“Success, your detail has been submitted successfully.”** was displayed.
* A Home button was displayed.

### Selecting Cancel

When **Cancel** was selected:

* The submission was cancelled.
* The user remained on the Contact Us page.
* The previously entered form details remained populated.
* The success message was not displayed.
* The form could be submitted again.
* Selecting Submit again and then OK successfully submitted the form.

The entered form data was therefore retained after cancelling the confirmation dialog during the observed interaction.

---

## Home Navigation After Submission

After successful Contact Us form submission, the application displayed a **Home** button.

Selecting the Home button redirected the user to the Home page.

---

## Observations Requiring Further Formal Testing

The following behaviors were identified during Contact Us exploratory testing and should be investigated through formal test cases:

* Contact Us page accessibility.
* Display of all Contact Us fields and controls.
* Email mandatory-field validation.
* Email format validation.
* Optional behavior of Name, Subject and Message fields.
* Name input handling for different character types.
* Subject input handling for different character types.
* Long Message input handling.
* File upload with no file selected.
* File upload with text files.
* File upload with image files.
* Successful Contact Us form submission.
* Submit confirmation dialog.
* Confirmation dialog OK behavior.
* Confirmation dialog Cancel behavior.
* Retention of entered data after Cancel.
* Success message after submission.
* Home navigation after successful submission.

These observations are **not automatically classified as defects**. They should be compared with the applicable expected results and formally executed before raising any defect.

---

# Exploratory Testing Conclusion

The Contact Us functionality was explored across:

**Contact Us Page → Form Fields → Email Validation → Optional Fields → File Upload → Submit → Confirmation Dialog → OK / Cancel → Success Message → Home Navigation**

The exploration covered the main Contact Us form components, mandatory and optional field behavior, email validation, different input types, file upload behavior, confirmation handling, successful submission, data retention after cancellation, and navigation after successful submission.

No defect was classified during exploratory testing based solely on these observations. Any potential validation issue should be evaluated against the expected behavior during formal test execution.

The observations from this exploration will be used as input for designing the formal **Contact Us test scenarios and detailed test cases**.


