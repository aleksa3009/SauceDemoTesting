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