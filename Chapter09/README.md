# User Stories and Test Cases

## What are User Stories?

**Definition:**
User stories are short, simple descriptions of a feature told from the perspective of the person who desires the new capability, usually a user or customer of the system. They are a critical part of agile development methodologies, particularly Scrum, as they help to capture requirements in a concise and understandable way.

**Purpose:**
- To capture user requirements and desired functionality.
- To ensure that development is aligned with user needs and business goals.
- To facilitate communication between stakeholders and the development team.

**Format:**
A common format for user stories is:

**Components:**
- **Title:** A brief summary of the user story.
- **Description:** A detailed explanation of the user story using the standard format.
- **Acceptance Criteria:** Conditions that must be met for the story to be considered complete.

## What are Test Cases?

**Definition:**
Test cases are specific conditions under which a new functionality is tested to determine if it meets the requirements and works as intended. They describe an input, action, or event and the expected response to determine if the feature is working correctly.

**Purpose:**
- To verify that the software meets the specified requirements.
- To identify defects or issues in the software.
- To ensure that the software behaves as expected under various conditions.

**Components:**
- **Test Case ID:** A unique identifier for the test case.
- **Description:** A brief description of what the test case will verify.
- **Precondition:** Any prerequisites that must be met before the test case can be executed.
- **Test Steps:** The specific steps to execute the test case.
- **Expected Result:** The expected outcome of the test case if the software is working correctly.

## User Stories and Test Cases

## User Story 1: User Registration

**User Story:**
As a new user, I want to register an account so that I can access member-only features.

**Acceptance Criteria:**
1. The registration form must include fields for username, email, password, and confirm password.
2. All fields are mandatory.
3. The email must be in a valid format.
4. The password must be at least 8 characters long.
5. The confirm password must match the password.
6. A success message is displayed upon successful registration.
7. An error message is displayed if the registration fails due to invalid input or existing user.

**Test Cases:**

| Test Case ID | Description                                                  | Precondition  | Test Steps                                                                 | Expected Result                         |
|--------------|--------------------------------------------------------------|---------------|--------------------------------------------------------------------------|-----------------------------------------|
| TC-REG-001   | Validate successful registration with valid input            | None          | 1. Open registration form<br>2. Enter valid username, email, and password<br>3. Submit form | Registration successful message displayed |
| TC-REG-002   | Validate registration failure with invalid email format      | None          | 1. Open registration form<br>2. Enter valid username, invalid email, and valid password<br>3. Submit form | Error message for invalid email displayed |
| TC-REG-003   | Validate registration failure when password and confirm password do not match | None          | 1. Open registration form<br>2. Enter valid username, valid email, and non-matching passwords<br>3. Submit form | Error message for password mismatch displayed |

## User Story 2: Add Item to Shopping Cart

**User Story:**
As a customer, I want to add items to my shopping cart so that I can purchase them later.

**Acceptance Criteria:**
1. Items can be added to the cart from the product page.
2. The cart icon updates to show the number of items added.
3. A confirmation message is displayed when an item is added to the cart.
4. The cart retains items added during the same session.

**Test Cases:**

| Test Case ID | Description                                                  | Precondition | Test Steps                                                                 | Expected Result                         |
|--------------|--------------------------------------------------------------|--------------|--------------------------------------------------------------------------|-----------------------------------------|
| TC-CART-001  | Validate adding an item to the cart                          | User is on a product page | 1. Click "Add to Cart" button for a product<br>2. Observe cart icon | Item added to cart, cart icon updates, confirmation message displayed |
| TC-CART-002  | Validate cart icon update after adding multiple items        | User is on a product page | 1. Add multiple items to the cart<br>2. Observe cart icon | Cart icon updates to reflect total number of items added |
| TC-CART-003  | Validate cart retains items during the same session          | User has added items to the cart | 1. Add items to cart<br>2. Navigate to a different page<br>3. Return to cart | Cart retains previously added items     |

## User Story 3: Password Reset

**User Story:**
As a user, I want to reset my password if I forget it so that I can regain access to my account.

**Acceptance Criteria:**
1. A "Forgot Password" link is available on the login page.
2. The link directs to a password reset form that requires the user's email.
3. An email with a reset link is sent to the user's email if it is registered.
4. The reset link leads to a form where the user can enter a new password.
5. The new password must be at least 8 characters long.
6. A success message is displayed after the password is successfully reset.
7. An error message is displayed if the email is not registered.

**Test Cases:**

| Test Case ID | Description                                                  | Precondition | Test Steps                                                                 | Expected Result                         |
|--------------|--------------------------------------------------------------|--------------|--------------------------------------------------------------------------|-----------------------------------------|
| TC-RESET-001 | Validate password reset with registered email                | User is on login page | 1. Click "Forgot Password" link<br>2. Enter registered email<br>3. Check email<br>4. Click reset link<br>5. Enter new password<br>6. Submit form | Password reset successful message displayed |
| TC-RESET-002 | Validate error message with unregistered email               | User is on login page | 1. Click "Forgot Password" link<br>2. Enter unregistered email<br>3. Submit form | Error message for unregistered email displayed |
| TC-RESET-003 | Validate password reset failure with invalid new password    | User has clicked reset link | 1. Enter new password less than 8 characters<br>2. Submit form | Error message for invalid password displayed |

---

These examples illustrate how user stories are defined along with their corresponding test cases to ensure the functionality meets the requirements and acceptance criteria.
