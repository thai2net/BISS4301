# How to Report a Bug

**Definition:**
Reporting a bug involves documenting an issue encountered during testing to ensure it can be addressed by the development team. A well-documented bug report should provide enough information for the developers to understand, reproduce, and fix the issue.

**Components of a Bug Report:**
1. **Bug ID:** A unique identifier for the bug.
2. **Summary:** A brief summary of the issue.
3. **Description:** A detailed description of the issue, including steps to reproduce it.
4. **Severity:** The impact of the bug on the system (e.g., Blocker, Critical, Major, Minor).
5. **Priority:** The urgency of fixing the bug (e.g., High, Medium, Low).
6. **Environment:** Information about the test environment (e.g., OS, browser, version).
7. **Steps to Reproduce:** Detailed steps to recreate the issue.
8. **Expected Result:** What should happen if the bug did not exist.
9. **Actual Result:** What actually happens due to the bug.
10. **Attachments:** Screenshots, logs, or other files that help illustrate the issue.

## Sample Bug Reports

### Sample Bug Report 1: Login Button Not Working

**Bug ID:** BUG-001

**Summary:** Login button does not respond on the login page.

**Description:**
When attempting to log in, the login button does not respond to clicks. This issue prevents users from accessing their accounts.

**Severity:** Blocker

**Priority:** High

**Environment:**
- OS: Windows 10
- Browser: Chrome 92.0.4515.159
- Application Version: 1.0.0

**Steps to Reproduce:**
1. Open the login page at `http://example.com/login`.
2. Enter a valid username and password.
3. Click the "Login" button.

**Expected Result:**
The user should be logged in and redirected to the dashboard.

**Actual Result:**
Nothing happens when the login button is clicked.

**Attachments:**
- Screenshot: [login_issue.png](http://example.com/screenshots/login_issue.png)

### Sample Bug Report 2: Incorrect Total Price in Shopping Cart

**Bug ID:** BUG-002

**Summary:** Total price displayed in the shopping cart is incorrect.

**Description:**
The total price in the shopping cart does not update correctly when items are added or removed. This can lead to users being charged the wrong amount.

**Severity:** Major

**Priority:** High

**Environment:**
- OS: macOS Big Sur
- Browser: Safari 14.1.2
- Application Version: 2.3.1

**Steps to Reproduce:**
1. Add item A ($10) to the cart.
2. Add item B ($20) to the cart.
3. Remove item A from the cart.

**Expected Result:**
The total price should be $20.

**Actual Result:**
The total price remains $30.

**Attachments:**
- Screenshot: [cart_total_issue.png](http://example.com/screenshots/cart_total_issue.png)

### Sample Bug Report 3: Page Crash on Profile Update

**Bug ID:** BUG-003

**Summary:** Profile update causes page crash.

**Description:**
Updating the user profile with specific data causes the page to crash, resulting in loss of unsaved changes.

**Severity:** Critical

**Priority:** Medium

**Environment:**
- OS: Ubuntu 20.04
- Browser: Firefox 90.0.2
- Application Version: 3.4.0

**Steps to Reproduce:**
1. Log in to the application.
2. Navigate to the profile update page.
3. Enter a long string (over 500 characters) in the "Bio" field.
4. Click "Save Changes".

**Expected Result:**
The profile should be updated successfully, and a confirmation message should be displayed.

**Actual Result:**
The page crashes, and the changes are not saved.

**Attachments:**
- Screenshot: [profile_update_crash.png](http://example.com/screenshots/profile_update_crash.png)
- Error Log: [error_log.txt](http://example.com/logs/error_log.txt)

---

These examples illustrate how to document bugs effectively to ensure they can be understood, reproduced, and fixed by the development team.
