# Test Plan: SauceDemo – Manual End-to-End E‑commerce Testing

**Author:** Aleksa Aleksić  
**Date:** 01.07.2025  
**Project:** SauceDemo Manual E‑commerce Testing  
**Base URL:** https://www.saucedemo.com

---

## 1. Introduction  
This document is the formal test plan for manual end‑to‑end functional testing of the SauceDemo (Swag Labs) e‑commerce demo site. It covers the complete purchase workflow—from login through product sorting, cart operations, checkout information, order overview and finish pages—on both desktop and mobile emulation. The goal is to validate happy‑path and negative scenarios, verify UI behavior, data correctness, form validations and navigation, and log any defects found.

---

## 2. Scope

**In Scope:**  
- Functional manual tests of the UI workflows:  
  - **Login** (valid/invalid users, injections, missing fields)  
  - **Sorting & Filtering** (A→Z, Z→A, price low→high, high→low)  
  - **Shopping Cart** (add/remove items, badge count, persistence)  
  - **Checkout: Information** (form validation with CSV profiles)  
  - **Checkout: Overview & Finish** (totals, tax, navigation, success page)  
  - **Exploratory** (responsive layout, console errors, edge cases)  
- Verification of price calculations (item subtotal, tax rate, total).  
- Form–field validation messages and prevention of submission on invalid input.  
- UI behavior on desktop Chrome and Chrome Mobile Emulation.  
- Recording response times for page loads and filter actions (>3 s flagged).  
- Defect logging in GitHub Issues with steps, screenshots, severity.

**Out of Scope:**  
- Any API–level or automated testing.  
- Real payment gateway interactions (demo app simulates).  
- Load, performance beyond basic response timing.  
- Accessibility or security testing.

---

## 3. Objectives  
- Ensure all major user flows complete without errors.  
- Validate correct ordering and calculation of prices, tax, and totals.  
- Confirm form validations prevent bad data and display proper error messages.  
- Verify filtering and sorting reorder items as expected.  
- Log any UI defects, layout issues, or JavaScript errors.  
- Produce a full set of test artifacts: test cases, execution logs, screenshots, bug reports, summary.

---

## 4. Roles & Responsibilities

| Role        | Name            | Responsibility                                        |
|-------------|-----------------|------------------------------------------------------|
| Tester      | Aleksa Aleksić  | Draft plan, write & execute test cases, log defects  |
| Reviewer    | QA Mentor/Self  | Review test artifacts, provide feedback              |
| Stakeholder | Product Owner   | Triage & prioritize defects, review final report     |

---

## 5. Test Items

| Module              | Description                                                      |
|---------------------|------------------------------------------------------------------|
| Login               | standard_user, locked_out_user, problem_user, injections, blank  |
| Sorting & Filtering | A→Z, Z→A, price↑, price↓, stability of order                    |
| Shopping Cart       | Add/remove items, badge count, persistence after navigation      |
| Checkout Info       | Form fields (First, Last, ZIP) with valid & invalid CSV profiles |
| Checkout Overview   | Item totals, tax calculation (fixed rate), cancel/finish buttons |
| Finish              | Success page, back navigation, “Back to Products” behavior       |
| Exploratory         | Responsive UI, attempt out‐of‐order clicks, console error checks |

---

## 6. Test Approach & Strategy

1. **Test Types:** Functional, negative, boundary, exploratory  
2. **Design:** Risk-based, covering both happy paths and error conditions  
3. **Data-driven:** Use a CSV of 5 checkout profiles (valid + edge cases)  
4. **Execution Order:**  
   1. **Login** → 2. **Sorting/Filtering** → 3. **Cart** →  
   4. **Checkout Info** → 5. **Overview & Finish** → 6. **Exploratory**  
5. **Environment:** Chrome desktop + Chrome DevTools mobile emulation (e.g. iPhone X)  
6. **Defect Mgmt:** GitHub Issues, include steps, screenshots, severity  
7. **Performance:** Measure page load & filter action times; flag >3 s  
8. **Test Case Design:** Each test case will be written in detail in the Markdown format and shown in screenshots from TestRail, including the expected result and edge case scenarios.

---

## 7. Environment & Tools

- **Browsers:** Chrome (latest) on Windows 10 & Ubuntu 22.04  
- **Mobile Emulation:** Chrome DevTools device toolbar  
- **Test Data:**  
  - `TestData/checkout_users.csv` (5 profiles)  
  - `TestData/login_credentials.md`  
- **Test Cases:** TestRail & Markdown `TestCases/SauceDemo_Test_Cases.md`  
- **Bug Tracking:** GitHub Issues  
- **Screenshots:** Lightshot or Snagit  
- **Editor:** VS Code  
- **Version Control:** Git + GitHub (SSH)  
- **Documentation:** Markdown in `TestPlan/` and `Reports/`

---

## 8. Entry Criteria

- Folder structure created in `~/SauceDemoTesting/`  
- Browsers & tools installed and configured  
- Test data CSV and login credentials file prepared  
- GitHub repo and Issues board ready  
- Test case template in place

---

## 9. Exit Criteria

- All planned test cases executed with PASS/FAIL noted  
- All defects logged in GitHub Issues with full details  
- Exploratory findings documented  
- Daily reports (`Reports/Daily_Report_DD-MM-YYYY.md`) completed  
- Final summary report (`Reports/Final_Report.md`) drafted

---

## 10. Risks & Mitigation

| Risk                                       | Likelihood | Impact | Mitigation                           |
|-------------------------------------------|------------|--------|--------------------------------------|
| Demo site resets or changes               | Medium     | High   | Check site version daily; adjust TC  |
| Flaky mobile emulation behaviors          | Low        | Medium | Run key tests on real desktop screen |
| Miscalculations of tax or totals          | Medium     | High   | Manual re‑calculation in overview TC |
| Missing validation for edge‑case inputs   | High       | Medium | Include negative & boundary tests    |
| Issues with image loading or rendering    | Medium     | Medium | Cross-check on different screen sizes and devices |
| Sluggish behavior on larger product lists | Low        | Medium | Monitor page performance during sorting and filtering |

---

## 11. Deliverables

- **Test Plan:** `TestPlan/SauceDemo_Test_Plan.md`  
- **Test Cases:** `TestCases/SauceDemo_Test_Cases.md` & Screenshots from TestRail  
- **Test Data:** `TestData/checkout_users.csv`, `login_credentials.md`  
- **Execution Results:** Screenshots & logs in `ExecutionResults/`  
- **Bug Reports:** GitHub Issues 
- **Daily Reports:** `Reports/Daily_Report_DD-MM-YYYY.md`  
- **Final Report:** `Reports/Final_Report.md`

---

## 12. Schedule

### Day 1: Planning & Setup (≈5 h)
| Activity                         | Duration |
|----------------------------------|----------|
| Environment & folder setup       | 1 h      |
| Test Plan drafting               | 2.5 h    |
| Test Data CSV & credentials list | 1 h      |
| Test Case skeletons in Excel     | 0.5 h    |

### Day 2: Login & Sorting (≈5 h)
| Execute Login TCs                | 2 h      |
| Execute Sorting/Filtering TCs    | 1.5 h      |
| Exploratory & bug logging        | 1.5 h      |

### Day 3: Cart & Checkout Info (≈4 h)
| Cart tests                       | 2 h      |
| Checkout Info tests              | 1 h      |
| Exploratory & bug logging        | 1 h      |

### Day 4: Overview & Finish (≈4 h)
| Overview tests                   | 2 h      |
| Finish flow tests                | 1 h      |
| Exploratory & bug logging        | 1 h      |

### Day 5: Exploratory & Retest (≈5 h)
| Exploratory tests                | 1 h      |
| Retest defects                   | 1.5 h      |
| Finalize execution logs          | 1.5 h      |
| Daily report                     | 1 h      |

### Day 6: Final Review & Reporting (≈4 h)
| Coverage review                  | 1 h      |
| Issue triage & cleanup           | 1 h      |
| Final report drafting            | 1 h      |
| Repo README & CV update          | 1 h      |

---
