# ExecutionResults/Module_Results_SauceDemo_Tests.md

## SauceDemo Test Execution (Chrome)

**Browser:** Chrome 137.0.7151.119  
**OS:** Ubuntu 22.04 LTS

---

### TC_LOGIN_01: Verify valid login with standard_user  
**Start Time:** 02-07-2025 13:15  
**Steps:** Enter credentials and click Login  
**Result:** PASS  
**End Time:** 02-07-2025 13:17  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_LOGIN_02: Verify login blocked for locked_out_user  
**Start Time:** 02-07-2025 13:18  
**Steps:** Enter locked_out_user / secret_sauce  
**Result:** PASS  
**End Time:** 02-07-2025 13:20  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_LOGIN_03: Verify login failure for missing username  
**Start Time:** 02-07-2025 13:21  
**Steps:** Leave username blank, enter password  
**Result:** FAIL  
**Actual:** Error message not displayed; generic placeholder shown  
![Screenshot](/SauceDemoTesting/ExecutionResults/Screenshots/TC_LOGIN_03_fail.png)  
**End Time:** 02-07-2025 13:23  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_LOGIN_04: Verify login failure for missing password  
**Start Time:** 02-07-2025 13:24  
**Steps:** Enter username, leave password blank  
**Result:** PASS  
**End Time:** 02-07-2025 13:26  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_LOGIN_05: Verify login with SQL injection attempt in username  
**Start Time:** 02-07-2025 13:27  
**Steps:** Enter `' ; DROP TABLE users; --` in username  
**Result:** FAIL  
**Actual:** Application crashed briefly, console error  
![Screenshot](/SauceDemoTesting/ExecutionResults/Screenshots/TC_LOGIN_05_fail.png)  
**End Time:** 02-07-2025 13:30  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_LOGIN_06: Verify login with XSS attempt in username  
**Start Time:** 02-07-2025 13:31  
**Steps:** Enter `<script>alert('XSS')</script>`  
**Result:** PASS  
**End Time:** 02-07-2025 13:33  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_LOGIN_07: Verify login with performance_glitch_user behaves slowly but successfully  
**Start Time:** 02-07-2025 13:34  
**Steps:** Enter performance_glitch_user / secret_sauce  
**Result:** PASS  
**End Time:** 02-07-2025 13:38  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_SORT_01: Verify products sorted A to Z by name  
**Start Time:** 02-07-2025 14:15  
**Steps:** Select Name (A to Z)  
**Result:** PASS  
**End Time:** 02-07-2025 14:17  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_SORT_02: Verify products sorted Z to A by name  
**Start Time:** 02-07-2025 14:18  
**Steps:** Select Name (Z to A)  
**Result:** PASS  
**End Time:** 02-07-2025 14:20  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_SORT_03: Verify products sorted by price low to high  
**Start Time:** 02-07-2025 14:21  
**Steps:** Select Price (low to high)  
**Result:** PASS  
**End Time:** 02-07-2025 14:23  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_SORT_04: Verify products sorted by price high to low  
**Start Time:** 02-07-2025 14:24  
**Steps:** Select Price (high to low)  
**Result:** FAIL  
**Actual:** Two items out of order  
![Screenshot](/SauceDemoTesting/ExecutionResults/Screenshots/TC_SORT_04_fail.png)  
**End Time:** 02-07-2025 14:27  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_SORT_05: Verify item order remains stable when sorting option changes  
**Start Time:** 02-07-2025 14:28  
**Steps:** Switch between sort options  
**Result:** FAIL  
**Actual:** Random shuffle observed on second sort  
![Screenshot](/SauceDemoTesting/ExecutionResults/Screenshots/TC_SORT_05_fail.png)  
**End Time:** 02-07-2025 14:31  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_SORT_06: Verify sort selection persists after page reload  
**Start Time:** 02-07-2025 14:32  
**Steps:** Sort then reload page  
**Result:** FAIL  
**Actual:** Sort resets to default  
![Screenshot](/SauceDemoTesting/ExecutionResults/Screenshots/TC_SORT_06_fail.png)  
**End Time:** 02-07-2025 14:35  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_CART_01: Verify add a single product to cart  
**Start Time:** 02-07-2025 15:15  
**Steps:** Click Add to cart on first item  
**Result:** PASS  
**End Time:** 02-07-2025 15:17  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_CART_02: Verify add multiple products to cart  
**Start Time:** 02-07-2025 15:18  
**Steps:** Add three items  
**Result:** PASS  
**End Time:** 02-07-2025 15:21  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_CART_03: Verify remove product from cart updates badge  
**Start Time:** 02-07-2025 15:22  
**Steps:** Remove one item  
**Result:** PASS  
**End Time:** 02-07-2025 15:25  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_CART_04: Verify cart contents persist after navigating away and back  
**Start Time:** 02-07-2025 15:26  
**Steps:** Navigate away and return  
**Result:** FAIL  
**Actual:** Cart emptied unexpectedly  
![Screenshot](/SauceDemoTesting/ExecutionResults/Screenshots/TC_CART_04_fail.png)  
**End Time:** 02-07-2025 15:29  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_CART_05: Verify cart badge count accurate after multiple add/remove operations  
**Start Time:** 02-07-2025 15:30  
**Steps:** Add 2, remove 1, add 1  
**Result:** PASS  
**End Time:** 02-07-2025 15:33  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_CART_06: Verify empty cart behavior  
**Start Time:** 02-07-2025 15:34  
**Steps:** Open cart with no items  
**Result:** FAIL  
**Actual:** No “empty cart” message displayed  
![Screenshot](/SauceDemoTesting/ExecutionResults/Screenshots/TC_CART_06_fail.png)  
**End Time:** 02-07-2025 15:36  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_CART_07: Verify attempt checkout with empty cart  
**Start Time:** 02-07-2025 15:37  
**Steps:** Click Checkout on empty cart  
**Result:** FAIL  
**Actual:** Navigated to checkout info page anyway  
![Screenshot](/SauceDemoTesting/ExecutionResults/Screenshots/TC_CART_07_fail.png)  
**End Time:** 02-07-2025 15:40  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_CHECKOUT_INFO_01: Verify valid checkout info with standard CSV profiles  
**Start Time:** 02-07-2025 15:45  
**Steps:** Enter valid data and Continue  
**Result:** PASS  
**End Time:** 02-07-2025 15:48  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_CHECKOUT_INFO_02: Verify missing FirstName triggers error  
**Start Time:** 02-07-2025 15:49  
**Steps:** Leave FirstName blank  
**Result:** FAIL  
**Actual:** Generic “Error” toast shown without field reference  
![Screenshot](/SauceDemoTesting/ExecutionResults/Screenshots/TC_CHECKOUT_INFO_02_fail.png)  
**End Time:** 02-07-2025 15:52  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_CHECKOUT_INFO_03: Verify missing LastName triggers error  
**Start Time:** 02-07-2025 15:53  
**Steps:** Leave LastName blank  
**Result:** PASS  
**End Time:** 02-07-2025 15:56  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_CHECKOUT_INFO_04: Verify missing ZIP triggers error  
**Start Time:** 02-07-2025 15:57  
**Steps:** Leave ZIP blank  
**Result:** PASS  
**End Time:** 02-07-2025 16:00  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_CHECKOUT_INFO_05: Verify special characters in name fields  
**Start Time:** 02-07-2025 16:01  
**Steps:** Enter !@# in names  
**Result:** PASS  
**End Time:** 02-07-2025 16:04  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_CHECKOUT_INFO_06: Verify invalid ZIP code formats  
**Start Time:** 02-07-2025 16:05  
**Steps:** Enter “ABCDE” in ZIP  
**Result:** FAIL  
**Actual:** No format validation, allowed to continue  
![Screenshot](/SauceDemoTesting/ExecutionResults/Screenshots/TC_CHECKOUT_INFO_06_fail.png)  
**End Time:** 02-07-2025 16:08  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_OVERVIEW_01: Verify item total equals sum of product prices  
**Start Time:** 02-07-2025 16:15  
**Steps:** Manually sum prices vs displayed  
**Result:** PASS  
**End Time:** 02-07-2025 16:18  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_OVERVIEW_02: Verify tax calculated correctly at fixed rate (e.g., 8%)  
**Start Time:** 02-07-2025 16:19  
**Steps:** Calculate tax manually  
**Result:** FAIL  
**Actual:** Tax off by 0.02  
![Screenshot](/SauceDemoTesting/ExecutionResults/Screenshots/TC_OVERVIEW_02_fail.png)  
**End Time:** 02-07-2025 16:22  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_OVERVIEW_03: Verify total price equals item total plus tax  
**Start Time:** 02-07-2025 16:23  
**Steps:** Sum item total + tax  
**Result:** PASS  
**End Time:** 02-07-2025 16:26  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_OVERVIEW_04: Verify cancel button returns to inventory page  
**Start Time:** 02-07-2025 16:27  
**Steps:** Click Cancel  
**Result:** PASS  
**End Time:** 02-07-2025 16:29  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_OVERVIEW_05: Verify finish button proceeds to confirmation page  
**Start Time:** 02-07-2025 16:30  
**Steps:** Click Finish  
**Result:** PASS  
**End Time:** 02-07-2025 16:32  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_OVERVIEW_06: Verify back button and browser navigation behave correctly  
**Start Time:** 02-07-2025 16:33  
**Steps:** Browser back, then Back to Products  
**Result:** FAIL  
**Actual:** Browser back returned to overview again  
![Screenshot](/SauceDemoTesting/ExecutionResults/Screenshots/TC_OVERVIEW_06_fail.png)  
**End Time:** 02-07-2025 16:36  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_FINISH_01: Verify complete purchase flow end to end  
**Start Time:** 02-07-2025 16:45  
**Steps:** Complete checkout workflow  
**Result:** PASS  
**End Time:** 02-07-2025 16:48  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_FINISH_02: Verify cancel during checkout returns to cart without clearing items  
**Start Time:** 02-07-2025 16:49  
**Steps:** Click Cancel on overview  
**Result:** FAIL  
**Actual:** Returned to inventory, cart cleared  
![Screenshot](/SauceDemoTesting/ExecutionResults/Screenshots/TC_FINISH_02_fail.png)  
**End Time:** 02-07-2025 16:52  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_FINISH_03: Verify browser back navigation after finish does not allow going back to overview  
**Start Time:** 02-07-2025 16:53  
**Steps:** Use browser back on success page  
**Result:** FAIL  
**Actual:** Navigated back to overview page  
![Screenshot](/SauceDemoTesting/ExecutionResults/Screenshots/TC_FINISH_03_fail.png)  
**End Time:** 02-07-2025 16:56  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_LOGOUT_01: Verify logout returns to login page and clears session  
**Start Time:** 02-07-2025 17:05  
**Steps:** Open menu, click Logout  
**Result:** PASS  
**End Time:** 02-07-2025 17:07  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119
