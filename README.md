# SauceDemo – Manual E‑commerce Testing Project

A complete manual QA project showcasing end‑to‑end functional and exploratory testing of the SauceDemo (Swag Labs) demo web application.

---

## Project Overview

This repository contains all artifacts produced during a focused five‑day manual testing engagement on SauceDemo, covering:

- **Login & Authentication** flows  
- **Product Sorting & Filtering** (name and price)  
- **Shopping Cart** operations (add/remove items, persistence)  
- **Checkout Process**: Information entry, Order Overview, and Finish screen  
- **Negative & Boundary Scenarios**: Missing inputs, invalid characters, empty cart  
- **Exploratory Testing**: UI glitches, back‑button behavior, network conditions, edge‑case inputs  

By executing **36 structured test cases** and **15 exploratory sessions**, I identified **14 defects**, documented with clear reproduction steps and screenshots.

---

## Repository Structure

```bash
~/SauceDemoTesting/
├── TestPlan/
│   └── SauceDemo_Test_Plan.md
├── TestCases/
│   ├── SauceDemo_TestCases.xlsx
│   ├── Test_Cases_Overview.md
│   ├── Sorting_Test_Cases.md
│   ├── Overview_Test_Cases.md
│   ├── Logout_Test_Cases.md
│   ├── Login_Test_Cases.md
│   ├── Finish_Test_Cases.md
│   ├── Checkout_Test_Cases.md
│   ├── Cart_Test_Cases.md
│   └── Screenshots/
├── Test Data/
│   ├── login_credentials.md
│   └── checkout_users.csv
├── ExecutionResults/
│   ├── Module_Results_SauceDemo_Tests.md
│   ├── Module_Results_Login_TCs.md
│   ├── Module_Results_Logout_TCs.md
│   ├── Module_Results_Sorting_TCs.md
│   ├── Module_Results_Cart_TCs.md
│   ├── Module_Results_Checkout_Info_TCs.md
│   ├── Module_Results_Overview_TCs.md
│   ├── Module_Results_Finish_TCs.md
│   ├── Bug_Retest.md
│   └── Screenshots/
├── Reports/
│   ├── Daily_Report_01-07-2025.md
│   ├── Daily_Report_02-07-2025.md
│   ├── Daily_Report_03-07-2025.md
│   ├── Daily_Report_04-07-2025.md
│   └── Final_Report.md
└── README.md
```


---

## Tools & Environment

- **Operating System:** Ubuntu 22.04 LTS  
- **Browser:** Google Chrome 137.0 and 138.0 (desktop) & DevTools mobile emulation (iPhone X)  
- **Test Management:** Markdown files in VS Code & TestRail 
- **Bug Tracking:** GitHub Issues  
- **Screenshots:** Lightshot  and LibreOffice Draw
- **Version Control:** Git & GitHub

---

## Test Planning & Execution Flow

| Day    | Activities                                                                                         |
|--------|----------------------------------------------------------------------------------------------------|
| Day 1  | Draft Test Plan; set up repository structure; prepare test data; outline ~35 test cases           |
| Day 2  | Execute **Login** and **Sorting** test cases; record results; initial exploratory observations     |
| Day 3  | Execute **Cart** and **Checkout Info** test cases; capture failures; begin bug reporting           |
| Day 4  | Execute **Overview** and **Finish** test cases; retest logged bugs; extend exploratory testing     |
| Day 5  | Final defect triage & closure; compile Final Report; prepare portfolio assets; update README       |

All execution logs, timestamps, and findings reside under **Reports/** and **ExecutionResults/**.

---

## Test Coverage & Metrics

| Module               | Test Cases | PASS | FAIL | Bugs Logged |
|----------------------|-----------:|-----:|-----:|------------:|
| Login                |          7 |    5 |    2 |           2 |
| Sorting & Filtering  |          6 |    3 |    3 |           3 |
| Shopping Cart        |          7 |    4 |    3 |           3 |
| Checkout – Info      |          6 |    4 |    2 |           2 |
| Checkout – Overview  |          6 |    4 |    2 |           2 |
| Checkout – Finish    |          3 |    1 |    2 |           2 |
| Logout               |          1 |    1 |    0 |           0 |
| **Total**            |         36 |   22 |   14 |          13 |

- **Exploratory Tests Executed:** 15  
- **Total Bugs Reported:** 14  
- **Average Duration per TC:** ~10 min  

---

## Notable Defects

- **High Severity:**  
  - Cart clears unexpectedly after navigation (TC_CART_04)  
  - Missing field‑specific errors on checkout form (TC_CHECKOUT_INFO_02)  
- **Medium Severity:**  
  - SQL‑injection crash on login (TC_LOGIN_05)  
  - Sorting order inconsistencies (TC_SORT_04, TC_SORT_05)  
- **Low Severity:**  
  - Sort preference resets after reload (TC_SORT_06)  

All defects include detailed reproduction steps and screenshots in GitHub Issues.

---

## Exploratory Testing Highlights

1. **Special Characters Overflow:** Long strings in login fields broke layout on mobile.  
2. **Empty‑Cart Checkout:** Checkout proceeded without items; no warning shown.  
3. **Back‑Button Abuse:** Browser back navigated to completed steps without resetting state.  
4. **Network Throttling:** Slow‑3G mode caused unresponsive buttons and no loader.  
5. **Rapid Sort Toggling:** Frequently caused console errors and inconsistent UI.

---

## Recommendations

1. **Strengthen Field Validation:** Enforce required checks and display contextual error messages.  
2. **Ensure State Persistence:** Maintain cart contents and sort/filter settings across navigation and reloads.  
3. **Control Navigation Flow:** Prevent back‑navigation to completed checkout steps.  
4. **Improve UI Feedback:** Show loading indicators during slow network conditions.  
5. **Harden Against Injects:** Sanitize inputs to avoid client‑side crashes on malicious payloads.

---

## Conclusion

This project demonstrates a comprehensive manual testing approach for a web e‑commerce application. Over five days, 36 test cases were executed, 14 defects reported, and robust documentation delivered. The structured artifacts—test plans, cases, execution logs, bug reports, and final analysis—provide a strong showcase of manual QA skills ideal for a junior tester portfolio.

---
