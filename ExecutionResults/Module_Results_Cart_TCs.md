# ExecutionResults/Module_Results_Cart_TCs.md

## SauceDemo Test Execution (Chrome)

**Browser:** Chrome 137.0.7151.119  
**OS:** Ubuntu 22.04 LTS

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