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