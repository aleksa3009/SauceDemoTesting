# Daily Report – Day 4 (04-07-2025)

**Tester:** Aleksa Aleksić  
**Project:** SauceDemo Manual E‑commerce Testing  
**Date:** 04.07.2025

---

## Activities:
- Prepared list of all **14** open bugs from GitHub Issues for retest.  
- Retested each bug in Chrome desktop and mobile emulation (iPhone X) over **2 hours**; recorded retest results in issue comments.  
- Closed all **14** defect reports  
- Continued exploratory testing focusing on less‑covered flows and edge cases. 
- Completed and finalized this Daily Report.

## Environment:
- **OS:** Ubuntu 22.04 LTS  
- **Browser:** Chrome 138.0.7204.92 (desktop) & Chrome DevTools mobile emulation  
- **Test Management:** Markdown under Git (VS Code)  
- **Defect Tracking:** GitHub Issues  

## Exploratory Testing Details:
1. **Checkout form HTML tags:**  
   Entered `<b>BoldName</b>` in the Last Name field.  
   - *Observation:* Tags rendered as plain text, no stripping or sanitization warning.

2. **Cart badge underflow:**  
   Rapidly removed all items then added one, then removed it.  
   - *Observation:* Badge briefly showed “-1” before resetting to zero.

3. **URL tampering:**  
   Manually changed URL from `/inventory.html` to `/checkout-step-one.html` without items in cart.  
   - *Observation:* Access granted to checkout info page, skipping cart validation.

4. **Keyboard navigation:**  
   Used Tab/Enter keys to navigate and activate “Add to cart” buttons.  
   - *Observation:* Focus indicator missing on mobile emulation; button activation inconsistent.

5. **Slow network simulation:**  
   Throttled network to “Slow 3G” during inventory sorting.  
   - *Observation:* Sorting dropdown hung for ~5 s with no loading indicator.

## Next Steps:
- **Day 5:** Final review of all test cases and closure of remaining bugs.  
- Finalize and proofread the **Final_Report.md** with metrics and lessons learned.  
- Prepare portfolio materials: select key test cases, bug examples, screenshots.  
- Update `README.md` with project overview and usage instructions.  
- Push final changes to GitHub and ensure repository is clean and public.
