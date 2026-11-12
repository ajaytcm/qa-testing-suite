# Test Plan — Demo Web Shop (SauceDemo)

## 1. Objective
Verify the core shopping flows of the demo web shop work as expected: login, product browsing/sorting, cart, and checkout. Produce executed test cases, a defect log, and a summary report.

## 2. Scope
**In scope:** Login (valid, invalid, locked-out user) · Inventory list and sorting · Product detail · Add/remove cart items · Cart badge accuracy · Checkout form validation · Order completion.
**Out of scope:** Payments (demo site takes no real payment), performance/load testing, mobile apps, browser matrix beyond one desktop browser.

## 3. Approach
- Manual, black-box functional testing from the user's point of view.
- Test cases designed with: equivalence classes (valid/invalid inputs), boundary values (empty fields, quantity limits), negative testing (wrong password, missing checkout fields), and end-to-end happy paths.
- Every failure is logged as a defect with steps to reproduce, expected vs. actual, severity and priority.

## 4. Test environment
- URL: https://www.saucedemo.com (practice site)
- Browser: Chrome (current version), desktop, Windows
- Test users: listed on the site's login page (`standard_user`, `locked_out_user`, `problem_user`, all with the site's published demo password)

## 5. Entry / exit criteria
- **Entry:** site reachable, test users known, test cases reviewed.
- **Exit:** all 15 cases executed; all Critical/High defects logged; summary report written with a release recommendation.

## 6. Risks
- Demo site behaviour can change without notice — re-run the login smoke cases first each session.
- `problem_user` is intentionally broken by design; defects found under that user are recorded as "by design (demo)" and not counted as real failures.
