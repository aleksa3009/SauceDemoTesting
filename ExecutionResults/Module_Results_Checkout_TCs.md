# ExecutionResults/Module_Results_Checkout_TCs.md

## SauceDemo Test Execution (Chrome)

**Browser:** Chrome 137.0.7151.119  
**OS:** Ubuntu 22.04 LTS

---

### TC_CHECKOUT_INFO_01: Verify valid checkout info with standard CSV profiles  
**Start Time:** 02-07-2025 15:45  
**Steps:** Enter valid data and Continue  
**Result:** PASS  
**End Time:** 02-07-2025 15:48  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_CHECKOUT_INFO_02: Verify missing FirstName triggers error  
**Start Time:** 02-07-2025 15:49  
**Steps:** Leave FirstName blank  
**Result:** FAIL  
**Actual:** Generic “Error” toast shown without field reference  
![Screenshot](/SauceDemoTesting/ExecutionResults/Screenshots/TC_CHECKOUT_INFO_02_fail.png)  
**End Time:** 02-07-2025 15:52  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_CHECKOUT_INFO_03: Verify missing LastName triggers error  
**Start Time:** 02-07-2025 15:53  
**Steps:** Leave LastName blank  
**Result:** PASS  
**End Time:** 02-07-2025 15:56  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_CHECKOUT_INFO_04: Verify missing ZIP triggers error  
**Start Time:** 02-07-2025 15:57  
**Steps:** Leave ZIP blank  
**Result:** PASS  
**End Time:** 02-07-2025 16:00  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_CHECKOUT_INFO_05: Verify special characters in name fields  
**Start Time:** 02-07-2025 16:01  
**Steps:** Enter !@# in names  
**Result:** PASS  
**End Time:** 02-07-2025 16:04  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_CHECKOUT_INFO_06: Verify invalid ZIP code formats  
**Start Time:** 02-07-2025 16:05  
**Steps:** Enter “ABCDE” in ZIP  
**Result:** FAIL  
**Actual:** No format validation, allowed to continue  
![Screenshot](/SauceDemoTesting/ExecutionResults/Screenshots/TC_CHECKOUT_INFO_06_fail.png)  
**End Time:** 02-07-2025 16:08  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

