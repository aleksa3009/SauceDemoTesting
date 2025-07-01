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