# Step-by-Step — Run the Full Test Cycle

Time: about 60–90 minutes. You need: a browser, this repo's files, and a free account on saucedemo.com — no sign-up needed, the demo users are printed on the login page.

## Step 1 — Prepare (10 min)
1. Read `test_plan.md` so you know the scope and the exit criteria.
2. Print or open `test_cases.md` — you will fill the execution record at the bottom as you go.
3. Open https://www.saucedemo.com and note the demo usernames/password shown under the login box.

## Step 2 — Smoke test first (5 min)
Run TC-01 (valid login) only. If login itself fails, stop — nothing else can be tested. This is what "entry criteria" means in practice.

## Step 3 — Execute all 15 cases (40 min)
1. Work through TC-01 to TC-15 in order.
2. For each case: follow the steps exactly, compare what happens with the Expected result, then write Pass or Fail plus the actual result in the execution table.
3. If a case fails, stop and write the defect first (Step 4), then continue.
4. Try `problem_user` for one or two cases at the end if you have time — that account is broken *on purpose*, so record anything odd as "by design (demo)", not as a defect.

## Step 4 — Log defects (as you find them)
For every failure, add a row to `defect_log.md`:
- Title, numbered steps to reproduce, expected vs. actual, severity, priority, status = New.
- Severity guide: Critical = a main flow is blocked (can't log in, can't check out). High = a main flow works wrongly (wrong totals, wrong badge). Medium = a workaround exists. Low = cosmetic.
- The two example rows in the log show the format — replace them with your real defects, or delete them if you find none of those.

## Step 5 — Retest thinking (10 min)
For each defect, write down which related cases you would re-run after a fix (e.g. a cart-badge fix needs TC-08, TC-09, TC-10). Add this as a note under the defect. On a demo site you can't deploy a fix, so the cycle ends at logging + retest planning — in a real job this is where the fix comes back to you for retest.

## Step 6 — Write the summary (15 min)
Fill in `test_summary_report.md`: counts from your execution table, defect counts by severity, what you did not cover, and a one-line recommendation. Keep it factual — the summary is what a manager reads to decide on release.

## Step 7 — Upload your executed copies
Upload the updated `test_cases.md` (with your execution record), `defect_log.md`, and `test_summary_report.md` back to this repo. The executed versions — with your dates and real results — are the portfolio evidence.

## How to talk about this project in an interview
- "I write cases before executing, with expected results — a case without an expected result isn't a test."
- "I use negative and boundary cases on purpose: empty fields, wrong passwords, locked accounts — that's where real defects live."
- "A defect report has to be reproducible by someone else: exact steps, expected vs. actual, severity separated from priority."
