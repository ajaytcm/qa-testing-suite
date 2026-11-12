# QA Testing Suite — Demo Web Shop

A complete manual-testing cycle on a public demo web shop, documented the way a QA team works: test plan → test cases → execution → defect log → test summary report.

**Skills shown:** test planning, test case design (positive, negative, boundary), execution records, defect reporting with severity/priority, regression retest, summary reporting.

## Files

- `test_plan.md` — scope, approach, entry/exit criteria, risks.
- `test_cases.md` — 15 test cases for login, inventory, cart and checkout.
- `defect_log.md` — defect log format with two example entries showing how a defect is written (replace/extend with the defects you actually find when you run the suite).
- `test_summary_report.md` — the closing report template: results, defect counts, recommendation.
- `INSTRUCTIONS.md` — how to run the whole cycle yourself, step by step.

## Target application

The practice site **SauceDemo** (saucedemo.com) — a free demo shop built for QA practice. Standard test users are listed on its login page (e.g. `standard_user` / `secret_sauce`).

## Method in one paragraph

Cases are written before execution, each with steps and an expected result. Every case is executed and marked Pass/Fail with the actual result recorded. Failures become defects in the log with steps to reproduce, severity and priority. After fixes (or at the end of the cycle), failed cases are retested and the summary report states plainly what passed, what failed, and whether the build is fit to release.
