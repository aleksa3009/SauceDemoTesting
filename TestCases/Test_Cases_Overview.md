# SauceDemo Manual Testing – Test Cases

---

## Login Module

### TC_LOGIN_01  
**Title:** Verify valid login with standard_user  

**Preconditions:** On login page  

**Test Steps:**  
1. Open browser.  
2. Navigate to https://www.saucedemo.com.  
3. Enter username: `standard_user`.  
4. Enter password: `secret_sauce`.  
5. Click Login.  

**Expected Results:**  
- Redirect to inventory page.  

**Priority:** High  
**Type:** Functional  

---

### TC_LOGIN_02  
**Title:** Verify login blocked for locked_out_user  

**Preconditions:** On login page  

**Test Steps:**  
1. Enter username: `locked_out_user`.  
2. Enter password: `secret_sauce`.  
3. Click Login.  

**Expected Results:**  
- Display error message: “Epic sadface: Sorry, this user has been locked out.”  
- Stay on login page.  

**Priority:** High  
**Type:** Negative  

---

### TC_LOGIN_03  
**Title:** Verify login failure for missing username  

**Preconditions:** On login page  

**Test Steps:**  
1. Leave username empty.  
2. Enter password: `secret_sauce`.  
3. Click Login.  

**Expected Results:**  
- Display error message: “Epic sadface: Username is required.”  
- Stay on login page.  

**Priority:** High  
**Type:** Negative  

---

### TC_LOGIN_04  
**Title:** Verify login failure for missing password  

**Preconditions:** On login page  

**Test Steps:**  
1. Enter username: `standard_user`.  
2. Leave password empty.  
3. Click Login.  

**Expected Results:**  
- Display error message: “Epic sadface: Password is required.”  
- Stay on login page.  

**Priority:** High  
**Type:** Negative  

---

### TC_LOGIN_05  
**Title:** Verify login with SQL injection attempt in username  

**Preconditions:** On login page  

**Test Steps:**  
1. Enter username: `'; DROP TABLE users; --`.  
2. Enter password: `secret_sauce`.  
3. Click Login.  

**Expected Results:**  
- Error message about invalid credentials or generic failure.  
- No server errors or data breaches occur.  

**Priority:** Medium  
**Type:** Security / Negative  

---

### TC_LOGIN_06  
**Title:** Verify login with XSS attempt in username  

**Preconditions:** On login page  

**Test Steps:**  
1. Enter username: `<script>alert('XSS')</script>`.  
2. Enter password: `secret_sauce`.  
3. Click Login.  

**Expected Results:**  
- No script execution occurs.  
- Error message about invalid credentials.  

**Priority:** Medium  
**Type:** Security / Negative  

---

### TC_LOGIN_07  
**Title:** Verify login with performance_glitch_user behaves slowly but successfully  

**Preconditions:** On login page  

**Test Steps:**  
1. Enter username: `performance_glitch_user`.  
2. Enter password: `secret_sauce`.  
3. Click Login.  

**Expected Results:**  
- Login succeeds, but response time noticeably slower than normal user.  
- Redirect to inventory page.  

**Priority:** Medium  
**Type:** Functional / Performance  

---

## Sorting Module

### TC_SORT_01  
**Title:** Verify products sorted A to Z by name  

**Preconditions:** Logged in as standard_user on inventory page  

**Test Steps:**  
1. Select **Name (A to Z)** from sort dropdown.  

**Expected Results:**  
- Products reordered alphabetically ascending by name.  

**Priority:** High  
**Type:** Functional  

---

### TC_SORT_02  
**Title:** Verify products sorted Z to A by name  

**Preconditions:** Logged in as standard_user on inventory page  

**Test Steps:**  
1. Select **Name (Z to A)** from sort dropdown.  

**Expected Results:**  
- Products reordered alphabetically descending by name.  

**Priority:** High  
**Type:** Functional  

---

### TC_SORT_03  
**Title:** Verify products sorted by price low to high  

**Preconditions:** Logged in as standard_user on inventory page  

**Test Steps:**  
1. Select **Price (low to high)** from sort dropdown.  

**Expected Results:**  
- Products reordered ascending by price.  

**Priority:** High  
**Type:** Functional  

---

### TC_SORT_04  
**Title:** Verify products sorted by price high to low  

**Preconditions:** Logged in as standard_user on inventory page  

**Test Steps:**  
1. Select **Price (high to low)** from sort dropdown.  

**Expected Results:**  
- Products reordered descending by price.  

**Priority:** High  
**Type:** Functional  

---

### TC_SORT_05  
**Title:** Verify item order remains stable when sorting option changes  

**Preconditions:** Logged in as standard_user on inventory page  

**Test Steps:**  
1. Select a sort option (e.g. A to Z).  
2. Select another sort option (e.g. Price low to high).  

**Expected Results:**  
- Product order changes according to selected sort each time without random shuffling.  

**Priority:** Medium  
**Type:** Functional  

---

### TC_SORT_06  
**Title:** Verify sort selection persists after page reload  

**Preconditions:** Logged in as `standard_user` on inventory page  

**Test Steps:**  
1. Select **Price (low to high)** from sort dropdown.  
2. Reload the browser page.  

**Expected Results:**  
- The sort dropdown remains set to **Price (low to high)**.  
- Product list remains sorted by price ascending.  

**Priority:** Low  
**Type:** Functional  

---

## Cart Module

### TC_CART_01  
**Title:** Verify add a single product to cart  

**Preconditions:** Logged in, inventory page  

**Test Steps:**  
1. Click **Add to cart** button on any product.  

**Expected Results:**  
- Cart badge updates to 1.  
- Button changes to **Remove** for that product.  

**Priority:** High  
**Type:** Functional  

---

### TC_CART_02  
**Title:** Verify add multiple products to cart  

**Preconditions:** Logged in, inventory page  

**Test Steps:**  
1. Add 3 different products to cart.  

**Expected Results:**  
- Cart badge shows count 3.  
- Products in cart page show those 3 items.  

**Priority:** High  
**Type:** Functional  

---

### TC_CART_03  
**Title:** Verify remove product from cart updates badge  

**Preconditions:** Cart has 3 items  

**Test Steps:**  
1. Click **Remove** button on one product.  

**Expected Results:**  
- Cart badge decrements by 1 (now 2).  
- Product removed from cart page.  

**Priority:** High  
**Type:** Functional  

---

### TC_CART_04  
**Title:** Verify cart contents persist after navigating away and back  

**Preconditions:** Cart has items  

**Test Steps:**  
1. Navigate to another page (e.g., About).  
2. Return to Cart page.  

**Expected Results:**  
- Cart items remain unchanged and accurate.  

**Priority:** Medium  
**Type:** Functional  

---

### TC_CART_05  
**Title:** Verify cart badge count accurate after multiple add/remove operations  

**Preconditions:** Inventory page  

**Test Steps:**  
1. Add 2 products, remove 1, add another.  

**Expected Results:**  
- Cart badge correctly reflects number of items.  

**Priority:** Medium  
**Type:** Functional  

---

### TC_CART_06  
**Title:** Verify empty cart behavior  

**Preconditions:** No items added  

**Test Steps:**  
1. Click cart icon to go to cart page.  

**Expected Results:**  
- Cart page shows “Your cart is empty” message or equivalent.  

**Priority:** Medium  
**Type:** Functional  

---

### TC_CART_07  
**Title:** Verify attempt checkout with empty cart  

**Preconditions:** No items in cart; on inventory page  

**Test Steps:**  
1. Click cart icon.  
2. On cart page with zero items, click **Checkout** (if enabled).  

**Expected Results:**  
- Either the **Checkout** button is disabled/not visible, or  
- Clicking shows an error/toast “Your cart is empty” and no navigation occurs.  

**Priority:** Medium  
**Type:** Negative  

---

## Checkout Info Module

### TC_CHECKOUT_INFO_01  
**Title:** Verify valid checkout info with standard CSV profiles  

**Preconditions:** Cart has items; on checkout info page  

**Test Steps:**  
1. Enter FirstName, LastName, ZIP from valid CSV profiles.  
2. Click Continue.  

**Expected Results:**  
- Navigate to overview page.  

**Priority:** High  
**Type:** Functional  

---

### TC_CHECKOUT_INFO_02  
**Title:** Verify missing FirstName triggers error  

**Preconditions:** On checkout info page  

**Test Steps:**  
1. Leave FirstName empty.  
2. Fill LastName and ZIP.  
3. Click Continue.  

**Expected Results:**  
- Error message: “First Name is required”.  
- Remain on checkout info page.  

**Priority:** High  
**Type:** Negative  

---

### TC_CHECKOUT_INFO_03  
**Title:** Verify missing LastName triggers error  

**Preconditions:** On checkout info page  

**Test Steps:**  
1. Leave LastName empty.  
2. Fill FirstName and ZIP.  
3. Click Continue.  

**Expected Results:**  
- Error message: “Last Name is required”.  
- Remain on checkout info page.  

**Priority:** High  
**Type:** Negative  

---

### TC_CHECKOUT_INFO_04  
**Title:** Verify missing ZIP triggers error  

**Preconditions:** On checkout info page  

**Test Steps:**  
1. Leave ZIP empty.  
2. Fill FirstName and LastName.  
3. Click Continue.  

**Expected Results:**  
- Error message: “Postal Code is required”.  
- Remain on checkout info page.  

**Priority:** High  
**Type:** Negative  

---

### TC_CHECKOUT_INFO_05  
**Title:** Verify special characters in name fields  

**Preconditions:** On checkout info page  

**Test Steps:**  
1. Enter special characters (e.g. !@#) in FirstName or LastName fields.  
2. Fill all required fields.  
3. Click Continue.  

**Expected Results:**  
- Form validation either blocks submission or accepts depending on app design.  
- If blocked, proper error shown.  

**Priority:** Medium  
**Type:** Negative  

---

### TC_CHECKOUT_INFO_06  
**Title:** Verify invalid ZIP code formats  

**Preconditions:** On checkout info page  

**Test Steps:**  
1. Enter invalid ZIP codes (e.g., alphabets or too short).  
2. Fill other fields.  
3. Click Continue.  

**Expected Results:**  
- Error message about invalid postal code format.  

**Priority:** Medium  
**Type:** Negative  

---

## Overview Module

### TC_OVERVIEW_01  
**Title:** Verify item total equals sum of product prices  

**Preconditions:** On overview page with items  

**Test Steps:**  
1. Sum prices of all items.  
2. Compare with displayed item total.  

**Expected Results:**  
- Displayed item total equals sum of item prices.  

**Priority:** High  
**Type:** Functional  

---

### TC_OVERVIEW_02  
**Title:** Verify tax calculated correctly at fixed rate (e.g., 8%)  

**Preconditions:** On overview page  

**Test Steps:**  
1. Calculate tax manually as fixed % of item total.  
2. Compare with displayed tax.  

**Expected Results:**  
- Displayed tax matches manual calculation.  

**Priority:** High  
**Type:** Functional  

---

### TC_OVERVIEW_03  
**Title:** Verify total price equals item total plus tax  

**Preconditions:** On overview page  

**Test Steps:**  
1. Add item total and tax amounts manually.  
2. Compare with total displayed.  

**Expected Results:**  
- Total equals sum of item total + tax.  

**Priority:** High  
**Type:** Functional  

---

### TC_OVERVIEW_04  
**Title:** Verify cancel button returns to inventory page  

**Preconditions:** On overview page  

**Test Steps:**  
1. Click **Cancel**.  

**Expected Results:**  
- Redirect to inventory page.  
- Cart contents remain intact.  

**Priority:** Medium  
**Type:** Functional  

---

### TC_OVERVIEW_05  
**Title:** Verify finish button proceeds to confirmation page  

**Preconditions:** On overview page  

**Test Steps:**  
1. Click **Finish**.  

**Expected Results:**  
- Navigate to success page with message “THANK YOU FOR YOUR ORDER”.  

**Priority:** High  
**Type:** Functional  

---

### TC_OVERVIEW_06  
**Title:** Verify back button and browser navigation behave correctly  

**Preconditions:** On success page  

**Test Steps:**  
1. Click browser back button after order complete.  
2. Click “Back to Products” button.  

**Expected Results:**  
- Back navigation does not allow return to overview or checkout info.  
- “Back to Products” returns to inventory page.  

**Priority:** Medium  
**Type:** Functional  

---

## Finish Module

### TC_FINISH_01  
**Title:** Verify complete purchase flow end to end  

**Preconditions:** Logged in, items in cart  

**Test Steps:**  
1. Proceed through checkout info and overview steps.  
2. Click Finish on overview.  

**Expected Results:**  
- Confirmation page displayed.  
- Cart is emptied after order.  

**Priority:** High  
**Type:** Functional  

---

### TC_FINISH_02  
**Title:** Verify cancel during checkout returns to cart without clearing items  

**Preconditions:** On checkout overview page  

**Test Steps:**  
1. Click **Cancel** button.  

**Expected Results:**  
- Return to cart page.  
- Items remain in cart.  

**Priority:** Medium  
**Type:** Functional  

---

### TC_FINISH_03  
**Title:** Verify browser back navigation after finish does not allow going back to overview  

**Preconditions:** On success page  

**Test Steps:**  
1. Use browser back button after order completion.  

**Expected Results:**  
- User is redirected to login or inventory page, not overview or checkout pages.  

**Priority:** Medium  
**Type:** Functional  

---

## Logout Module

### TC_LOGOUT_01  
**Title:** Verify logout returns to login page and clears session  

**Preconditions:** Logged in as any user on inventory page  

**Test Steps:**  
1. Click the menu button (☰) in the top left.  
2. Click **Logout**.  

**Expected Results:**  
- Redirect to login page (`/index.html`).  
- Attempting to navigate back to inventory without logging in redirects back to login.  

**Priority:** Medium  
**Type:** Functional  
