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