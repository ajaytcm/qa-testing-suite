# Defect Log — Demo Web Shop

**Execution cycle 2026-11-12: 15 of 15 test cases passed — no defects were found, so this log has no live entries. The two rows below are format examples only.**

One row per defect. Severity = how badly it breaks the product. Priority = how soon it should be fixed. Status flow: New → Assigned → Fixed → Retest → Closed (or Reopened).

| ID | Title | Steps to reproduce | Expected | Actual | Severity | Priority | Status |
|----|-------|--------------------|----------|--------|----------|----------|--------|
| DEF-001 | *(example format)* Cart badge does not update after removing an item | 1. Add two items 2. Open cart 3. Remove one item | Badge shows 1 | Badge still shows 2 until page refresh | Medium | High | Example — replace with your real finding |
| DEF-002 | *(example format)* Checkout accepts a postal code of only spaces | 1. Add an item 2. Checkout 3. Enter names and three spaces as postal code 4. Continue | Error: valid postal code required | Checkout advances to overview | Low | Medium | Example — replace with your real finding |

## How to write a good defect

1. **Title** names the feature and the failure in one line.
2. **Steps to reproduce** are numbered and exact — another tester must reach the same failure.
3. **Expected vs. actual** are stated separately; never mix them into the steps.
4. **Evidence:** note the browser, the test user, and the data used; attach a screenshot when the tool allows it.
5. After a fix, **retest the exact steps**, then run the related cases (regression) before closing.
