# Test Cases — Demo Web Shop (SauceDemo)

Execute each case exactly as written. Record the actual result and Pass/Fail in your execution copy. Precondition for all cases unless stated: browser open at https://www.saucedemo.com.

| ID | Title | Steps | Expected result |
|----|-------|-------|-----------------|
| TC-01 | Login with valid credentials | Enter `standard_user` and the site's demo password → Login | Inventory page opens; product list visible |
| TC-02 | Login with wrong password | Enter `standard_user` and a wrong password → Login | Error shown; user stays on login page |
| TC-03 | Login with empty username | Leave username blank, enter any password → Login | Error: username is required |
| TC-04 | Login with empty password | Enter username, leave password blank → Login | Error: password is required |
| TC-05 | Locked-out user | Login as `locked_out_user` with the demo password | Error states the user is locked out; no access |
| TC-06 | Sort products Z to A | On inventory page, choose sort "Name (Z to A)" | First product shown is the alphabetically last item; order is fully reversed |
| TC-07 | Sort products by price, low to high | Choose sort "Price (low to high)" | Products are in ascending price order; first item is the cheapest |
| TC-08 | Add one item to cart | Click "Add to cart" on any product | Button changes to "Remove"; cart badge shows 1 |
| TC-09 | Add and remove from cart page | Add two items → open cart → remove one | Cart shows 1 item; badge updates to 1; totals/list match |
| TC-10 | Cart badge accuracy | Add three different items one by one | Badge count matches the number of added items after each click (1, 2, 3) |
| TC-11 | Checkout with valid details | Cart → Checkout → enter first name, last name, postal code → Continue → Finish | Overview shows the correct items; completion page confirms the order |
| TC-12 | Checkout with missing first name | Checkout → leave first name blank → Continue | Error: first name is required; checkout does not advance |
| TC-13 | Checkout with missing postal code | Checkout → fill names, leave postal code blank → Continue | Error: postal code is required; checkout does not advance |
| TC-14 | Cancel checkout returns to cart | Start checkout → Cancel on the information page | User returns to the cart with items unchanged |
| TC-15 | Logout | Open menu → Logout | Login page shown; using the browser Back button does not restore the session |

## Execution record (fill in when you run the suite)

| ID | Result (Pass/Fail) | Actual result / defect ID if failed | Date |
|----|--------------------|-------------------------------------|------|
| TC-01 | Pass | Logged in as standard_user; inventory page showed all 6 products | 2026-11-12 |
| TC-02 | Pass | Error shown: "Username and password do not match any user in this service"; stayed on login page | 2026-11-12 |
| TC-03 | Pass | Error shown: "Username is required" | 2026-11-12 |
| TC-04 | Pass | Error shown: "Password is required" | 2026-11-12 |
| TC-05 | Pass | Error shown: "Sorry, this user has been locked out." | 2026-11-12 |
| TC-06 | Pass | Z to A order fully reversed; first item "Test.allTheThings() T-Shirt (Red)" | 2026-11-12 |
| TC-07 | Pass | Prices ascending $7.99 → $49.99; first item Onesie at $7.99 | 2026-11-12 |
| TC-08 | Pass | Button changed to "Remove"; cart badge showed 1 | 2026-11-12 |
| TC-09 | Pass | After removal the cart showed 1 item (Bike Light, $9.99); badge showed 1 | 2026-11-12 |
| TC-10 | Pass | Badge read 1, then 2, then 3 as the three items were added | 2026-11-12 |
| TC-11 | Pass | Overview: item total $55.97, tax $4.48, total $60.45; confirmation heading "Thank you for your order!" | 2026-11-12 |
| TC-12 | Pass | Error shown: "First Name is required"; checkout did not advance | 2026-11-12 |
| TC-13 | Pass | Error shown: "Postal Code is required"; checkout did not advance | 2026-11-12 |
| TC-14 | Pass | Cancel returned to the cart with the item unchanged | 2026-11-12 |
| TC-15 | Pass | Logout returned to the login page; browser Back did not restore the session | 2026-11-12 |
