# Bug Retest Results – 04-07-2025

## Retest Execution Summary
Re-tested all previously logged bugs in Chrome 138.0 on Ubuntu 22.04 LTS.

---

### Bug ID: TC_LOGIN_03  
- **Retested in Chrome 138.0.7204.92  
- **Status:** Fixed  
- **Comment:** Now displays specific “Epic sadface: Username is required.” error message.

---

### Bug ID: TC_LOGIN_05  
- **Retested in Chrome 138.0.7204.92  
- **Status:** Still Reproducible  
- **Comment:** Application still crashes briefly on SQL injection attempt; console error persists.

---

### Bug ID: TC_SORT_04  
- **Retested in Chrome 138.0.7204.92  
- **Status:** Still Reproducible  
- **Comment:** Two items remain out of order when sorting high→low.

---

### Bug ID: TC_SORT_05  
- **Retested in Chrome 138.0.7204.92  
- **Status:** Still Reproducible  
- **Comment:** Product list still randomizes upon switching sort options.

---

### Bug ID: TC_SORT_06  
- **Retested in Chrome 138.0.7204.92  
- **Status:** Fixed  
- **Comment:** Sort selection now persists after page reload.

---

### Bug ID: TC_CART_04  
- **Retested in Chrome 138.0.7204.92  
- **Status:** Still Reproducible  
- **Comment:** Cart contents are still cleared when navigating away and back.

---

### Bug ID: TC_CART_06  
- **Retested in Chrome 138.0.7204.92  
- **Status:** Fixed  
- **Comment:** “Your cart is empty” message now displays correctly for empty carts.

---

### Bug ID: TC_CART_07  
- **Retested in Chrome 138.0.7204.92  
- **Status:** Fixed  
- **Comment:** Checkout button is now disabled when cart is empty.

---

### Bug ID: TC_OVERVIEW_02  
- **Retested in Chrome 138.0.7204.92  
- **Status:** Still Reproducible  
- **Comment:** Tax calculation remains off by 0.02.

---

### Bug ID: TC_OVERVIEW_06  
- **Retested in Chrome 138.0.7204.92  
- **Status:** Still Reproducible  
- **Comment:** Browser back button still navigates back to overview.

---

### Bug ID: TC_FINISH_02  
- **Retested in Chrome 138.0.7204.92  
- **Status:** Fixed  
- **Comment:** Cancel now returns to cart without clearing items.

---

### Bug ID: TC_FINISH_03  
- **Retested in Chrome 138.0.7204.92  
- **Status:** Still Reproducible  
- **Comment:** Browser back continues to allow return to overview.

---

### Bug ID: TC_CHECKOUT_INFO_02  
- **Retested in Chrome 138.0.7204.92  
- **Status:** Fixed  
- **Comment:** Specific “First Name is required” error now appears.

---

### Bug ID: TC_CHECKOUT_INFO_06  
- **Retested in Chrome 138.0.7204.92  
- **Status:** Still Reproducible  
- **Comment:** Invalid ZIP codes still accepted without validation.
