# ExecutionResults/Module_Results_Login_TCs.md

## SauceDemo Test Execution (Chrome)

**Browser:** Chrome 137.0.7151.119  
**OS:** Ubuntu 22.04 LTS

---

### TC_FINISH_01: Verify complete purchase flow end to end  
**Start Time:** 02-07-2025 16:45  
**Steps:** Complete checkout workflow  
**Result:** PASS  
**End Time:** 02-07-2025 16:48  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_FINISH_02: Verify cancel during checkout returns to cart without clearing items  
**Start Time:** 02-07-2025 16:49  
**Steps:** Click Cancel on overview  
**Result:** FAIL  
**Actual:** Returned to inventory, cart cleared  
![Screenshot](/SauceDemoTesting/ExecutionResults/Screenshots/TC_FINISH_02_fail.png)  
**End Time:** 02-07-2025 16:52  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_FINISH_03: Verify browser back navigation after finish does not allow going back to overview  
**Start Time:** 02-07-2025 16:53  
**Steps:** Use browser back on success page  
**Result:** FAIL  
**Actual:** Navigated back to overview page  
![Screenshot](/SauceDemoTesting/ExecutionResults/Screenshots/TC_FINISH_03_fail.png)  
**End Time:** 02-07-2025 16:56  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---