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