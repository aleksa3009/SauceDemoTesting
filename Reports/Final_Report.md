# Final Report – SauceDemo Manual Testing Project

**Project:** Manual Testing of Core UI Modules on SauceDemo  
**Tester:** Aleksa Aleksić  
**Duration:** 01-07-2025 to 05-07-2025  
**Base URL:** [https://www.saucedemo.com](https://www.saucedemo.com)

---

## 1. Introduction

This report documents a manual UI and functional testing project focused on the core functionalities of the SauceDemo demo web application. Over five consecutive workdays, a total of **36 test cases** were executed across modules such as Login, Sorting, Cart, Checkout, and Order Completion.

The project involved structured test case writing and execution, bug reporting, exploratory testing, and professional documentation. Special attention was paid to UI consistency, error handling, user flow stability, and business rule validation. All tests were executed manually using Google Chrome, with detailed execution logs in Markdown format and screenshots for all FAIL scenarios.

---

## 2. Scope & Objectives

**Scope:**

- Manual testing of the following modules:
  - Login and Logout
  - Product Sorting
  - Shopping Cart
  - Checkout: Information, Overview, and Finish pages
- Validation of edge cases, input validation, navigation logic, and state persistence
- Exploratory testing to uncover hidden issues or behavior inconsistencies

**Objectives:**

1. Validate all critical user flows under typical and edge conditions.
2. Detect and report any usability or functionality issues with detailed steps.
3. Create a professional test artifact suite including test cases, execution logs, and bug reports.
4. Demonstrate complete manual test process suitable for a junior QA portfolio.

---

## 3. Test Environment & Tools

**Operating System:**

- Ubuntu 22.04 LTS

**Tools & Utilities:**

- **Browser:** Google Chrome 137.0.7151.119 and 138.0.7204.92 
- **Test Management:** Markdown files (`*.md`) via VS Code
- **Bug Tracking:** GitHub Issues
- **Screenshots:** Lightshot and LibreOffice Draw
- **Documentation:** Markdown (`.md`), TestRail, GitHub Repository

---

## 4. Folder Structure & Artifacts


~/SauceDemoTesting/
├── TestPlan/
│ └── SauceDemo_Test_Plan.md
├── TestCases/
│ └── SauceDemo_TestCases.xlsx
├── Test Data/
│ ├── login_credentials.md
│ └── checkout_users.csv
├── TestCases/
│ ├── Test_Cases_Overview.md
│ ├── Sorting_Test_Cases.md
│ ├── Overview_Test_Cases.md
│ ├── Logout_Test_Cases.md
│ ├── Login_Test_Cases.md
│ ├── Finish_Test_Cases.md
│ ├── Checkout_Test_Cases.md
│ ├── Cart_Test_Cases.md
│ └── Screenshots/
├── ExecutionResults/
│ ├── Module_Results_SauceDemo_Tests.md
│ ├── Module_Results_Login_TCs.md
│ ├── Module_Results_Logout_TCs.md
│ ├── Module_Results_Sorting_TCs.md
│ ├── Module_Results_Cart_TCs.md
│ ├── Module_Results_Checkout_Info_TCs.md
│ ├── Module_Results_Overview_TCs.md
│ ├── Module_Results_Finish_TCs.md
│ ├── Bug_Retest.md
│ └── Screenshots/
├── Reports/
│ ├── Daily_Report_01-07-2025.md
│ ├── Daily_Report_02-07-2025.md
│ ├── Daily_Report_03-07-2025.md
│ ├── Daily_Report_04-07-2025.md
| ├── Daily_Report_04-07-2025.md
│ └── Final_Report.md
└── README.md

---

## 5. Test Case Coverage

Total of **36 test cases** executed:

| Module                | TC Count |
|-----------------------|----------|
| Login                 | 7        |
| Product Sorting       | 6        |
| Shopping Cart         | 7        |
| Checkout – Info       | 6        |
| Checkout – Overview   | 6        |
| Checkout – Finish     | 3        |
| Logout                | 1        |

All test cases were written with detailed structure:
- **Test ID**, **Title**, **Preconditions**, **Steps**, **Expected Result**, **Actual Result**, **Status**, **Type**, **Priority**

---

## 6. Execution Summary

| Module                | Executed | PASS | FAIL | Bugs Logged |
|-----------------------|----------|------|------|-------------|
| Login                 | 7        | 5    | 2    | 2           |
| Product Sorting       | 6        | 3    | 3    | 3           |
| Shopping Cart         | 7        | 4    | 3    | 3           |
| Checkout – Info       | 6        | 4    | 2    | 2           |
| Checkout – Overview   | 6        | 4    | 2    | 2           |
| Checkout – Finish     | 3        | 4    | 2    | 2           |
| Logout                | 1        | 1    | 0    | 0           |

- **Total Executed:** 36  
- **Total PASS:** 22  
- **Total FAIL:** 14  
- **Total Bugs Reported:** 14  
- **Retest Outcome:** 6 Fixed, 8 Still Reproducible

---

## 7. Defect Overview

- **Bug Reports:** 14 total, written in GitHub Issues with screenshots
- **Retest Completed:** 04-07-2025 with updated statuses in `Bug_Retest.md`

**Common Bug Patterns:**

- No validation for required fields (e.g., missing FirstName, ZIP)
- Sort order inconsistency
- Unexpected behavior on empty cart or after checkout
- Navigation issues when using browser back button
- Missing or unclear error messages

---

## 8. Exploratory Testing Highlights

Five exploratory tests were performed during Days 3, 4 and 5, yielding valuable insights:

1. **Attempting checkout with empty cart**  
   - Unexpected behavior: Navigation proceeds to checkout info page.  
   - No message shown that the cart is empty.

2. **Browser back navigation after order completion**  
   - Returned to previous checkout screen, violating expected flow integrity.

3. **Rapid switching of sorting options**  
   - Caused intermittent item shuffling, indicating unstable client-side sort logic.

4. **Using special characters in ZIP code field**  
   - No validation; user can proceed with `!@#$$`.

5. **Leaving all checkout fields blank**  
   - Only a generic "Error" toast shown; does not specify which field is missing.

---

## 9. Lessons Learned & Recommendations

1. **Improve Field Validation:** Inputs like First Name, ZIP Code, and Cart should enforce stricter client- and server-side validation.
2. **Fix Sorting Logic:** High-to-low sorting yielded inconsistent order—logic needs adjustment or client sorting needs review.
3. **Better Error Messages:** Generic toasts or silent errors should be replaced with contextual field-level feedback.
4. **Browser Navigation Control:** Prevent users from re-accessing completed order pages via browser back.
5. **Test Data Preparation Matters:** Edge cases discovered were only possible due to thoughtful test data variation.

---

## 10. Conclusion

This SauceDemo manual testing project provides complete end-to-end validation of critical e-commerce flows, including login, shopping cart, and checkout. It demonstrates the tester’s ability to write structured test cases, execute and log test runs, perform exploratory testing, and document bugs effectively.

All test results, bugs, screenshots, and reports are fully traceable in the GitHub project repository, making this an ideal candidate for inclusion in a QA Junior portfolio. The project showcases a professional testing approach with an emphasis on quality, reproducibility, and communication.

---
