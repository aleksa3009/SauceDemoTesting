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