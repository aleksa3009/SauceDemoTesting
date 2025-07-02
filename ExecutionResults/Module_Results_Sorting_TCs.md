# ExecutionResults/Module_Results_Sorting_TCs.md

## SauceDemo Test Execution (Chrome)

**Browser:** Chrome 137.0.7151.119  
**OS:** Ubuntu 22.04 LTS

---

### TC_SORT_01: Verify products sorted A to Z by name  
**Start Time:** 02-07-2025 14:15  
**Steps:** Select Name (A to Z)  
**Result:** PASS  
**End Time:** 02-07-2025 14:17  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_SORT_02: Verify products sorted Z to A by name  
**Start Time:** 02-07-2025 14:18  
**Steps:** Select Name (Z to A)  
**Result:** PASS  
**End Time:** 02-07-2025 14:20  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_SORT_03: Verify products sorted by price low to high  
**Start Time:** 02-07-2025 14:21  
**Steps:** Select Price (low to high)  
**Result:** PASS  
**End Time:** 02-07-2025 14:23  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_SORT_04: Verify products sorted by price high to low  
**Start Time:** 02-07-2025 14:24  
**Steps:** Select Price (high to low)  
**Result:** FAIL  
**Actual:** Two items out of order  
![Screenshot](/SauceDemoTesting/ExecutionResults/Screenshots/TC_SORT_04_fail.png)  
**End Time:** 02-07-2025 14:27  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_SORT_05: Verify item order remains stable when sorting option changes  
**Start Time:** 02-07-2025 14:28  
**Steps:** Switch between sort options  
**Result:** FAIL  
**Actual:** Random shuffle observed on second sort  
![Screenshot](/SauceDemoTesting/ExecutionResults/Screenshots/TC_SORT_05_fail.png)  
**End Time:** 02-07-2025 14:31  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---

### TC_SORT_06: Verify sort selection persists after page reload  
**Start Time:** 02-07-2025 14:32  
**Steps:** Sort then reload page  
**Result:** FAIL  
**Actual:** Sort resets to default  
![Screenshot](/SauceDemoTesting/ExecutionResults/Screenshots/TC_SORT_06_fail.png)  
**End Time:** 02-07-2025 14:35  
**Environment:** Ubuntu 22.04 / Chrome 137.0.7151.119

---