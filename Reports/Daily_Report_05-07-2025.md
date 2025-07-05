# Daily Report – Day 5 (05-07-2025)

**Tester:** Aleksa Aleksić  
**Project:** SauceDemo Manual E‑commerce Testing  
**Date:** 05.07.2025

---

## Activities:
- Performed final review of **36** test cases, confirming PASS/FAIL statuses and updating execution logs.    
- Completed and proofread the `Final_Report.md`, incorporating metrics, lessons learned, and defect summaries.   
- Updated `README.md` with project overview, usage instructions, and links to test artifacts.  
- Performed final backup and pushed all folders/files to the GitHub repository, ensuring clean commit history.

## Environment:
- **OS:** Ubuntu 22.04 LTS  
- **Browser:** Chrome 138.0.7204.92 (desktop) & Chrome DevTools mobile emulation  
- **Test Management:** Markdown files under Git (VS Code)  
- **Defect Tracking:** GitHub Issues  
- **Version Control:** Git & GitHub  

## Exploratory Testing Highlights:
1. **Login field length limit:** Confirmed that username input is capped at 100 characters and truncates extra text.  
2. **Cart badge recovery:** Verified that removing all items and then adding again correctly resets badge count to 1.  
3. **Checkout form persistence:** Reloading the Checkout Info page retains previously entered valid data.  
4. **Overview back-button fix:** Confirmed browser back now redirects to inventory rather than overview.  
5. **Sorting persistence on mobile:** Sort selection is now maintained after page reload in mobile emulation.

## Next Steps:
- Share repository link and portfolio highlights with hiring contacts.  
- Prepare for QA interview by reviewing documented bugs and test strategies.  
