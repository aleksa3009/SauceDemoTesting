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