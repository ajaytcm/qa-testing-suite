# Test Summary Report — Demo Web Shop

## Cycle summary
- Build/site tested: SauceDemo (saucedemo.com), tested on November 12, 2026
- Environment: Chromium-based browser, desktop
- Test cases executed: 15 of 15

## Results
| Outcome | Count |
|---------|-------|
| Passed | 15 |
| Failed | 0 |
| Blocked | 0 |

## Defects
| Severity | Open | Closed | Total |
|----------|------|--------|-------|
| Critical | 0 | 0 | 0 |
| High | 0 | 0 | 0 |
| Medium | 0 | 0 | 0 |
| Low | 0 | 0 | 0 |

Defect IDs raised: none — no case failed in this cycle.

## Coverage notes
Flows covered: login (valid, wrong password, empty fields, locked-out user), product sorting (name Z–A, price low–high), add/remove cart items, cart badge accuracy, checkout happy path (item total $55.97, tax $4.48, total $60.45), checkout field validation (first name, postal code), cancel checkout, logout/session behaviour.
Not covered: the intentionally broken `problem_user` account (by design on this demo site), real payment processing (the demo takes none), and browsers other than the one used.

## Recommendation
Ready to release — all 15 designed cases passed with the expected results, including the negative and validation cases, and no defects were found in this cycle.
