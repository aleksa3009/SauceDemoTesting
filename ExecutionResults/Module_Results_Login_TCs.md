# ExecutionResults/Module_Results_Login_TCs.md

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