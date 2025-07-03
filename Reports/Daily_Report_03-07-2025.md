# Daily Report – Day 3 (03-07-2025)

**Tester:** Aleksa Aleksić  
**Project:** SauceDemo – E-commerce End-to-End Manual Testing  
**Date:** 03.07.2025

---

## Activities:
- Executed **all 14** failed test cases across Login, Sorting, Cart, Checkout Info, Overview and Finish modules in both desktop and mobile emulation.    
- Captured **14** screenshots—one for each failed test—and saved them in `ExecutionResults/Screenshots/`.  
- Created **14** detailed bug reports in GitHub Issues (with reproduction steps, environment details, severity, priority and screenshots).  
- Conducted exploratory testing immediately after scripted execution to uncover additional issues.

---

## Environment:
- **OS:** Ubuntu 22.04 LTS  
- **Browser:** Chrome 137.0.7151.119 (desktop) & Chrome DevTools emulator for mobile phones  
- **Defect Tracking:** GitHub Issues
- **Screenshots Tracking:** LibreOfficeDraw and Flameshot  

---

## Exploratory Testing Details:
1. **Special characters in login fields:**  
   Tried entering special characters like `!@#$%^&*()` in both username and password fields.  
   - *Observation:* The app accepts input but displays a generic error message on login attempt, with no specific feedback.

2. **Back button behavior on Checkout Overview page:**  
   Clicked “Back to Products” from the overview screen after removing an item from the cart.  
   - *Observation:* Returned to inventory page, but the cart icon still showed the old item count until manual refresh.

3. **Submitting checkout form with all fields empty:**  
   Tried to proceed without entering any information in the checkout form.  
   - *Observation:* An error message appeared, but it did not highlight which fields were missing — confusing for the user.

4. **Refreshing the page during the checkout process:**  
   Performed `Ctrl + R` while on the Overview step.  
   - *Observation:* After refresh, the cart data was preserved, but sorting and filter states reset to default.

5. **Switching sorting filters rapidly:**  
   Clicked quickly between different sorting options (e.g., Price high to low, Name Z–A).  
   - *Observation:* Sometimes the UI did not update immediately, and product order became inconsistent. 

---

## Next Steps:
- **Day 4:** Retest all 14 reported bugs against any fixes; update GitHub Issues with retest results.  
- Capture any new defects discovered during retest and exploratory continuation.  
- Continue exploratory testing focusing on form validation edge cases and error‑handling flows over the next two days.  
- Prepare Daily Report – Day 4 with detailed bug statuses and additional exploratory findings.  