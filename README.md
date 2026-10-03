# E-Commerce Web App — Manual & API Test Suite (2023)
**Personal QA Project**

## Contents

| File | Description |
|---|---|
| `Test_Cases.xlsx` | 82 manual test cases across Registration, Login, Product Search, Cart, and Checkout, each executed on Chrome, Firefox, and Edge. Includes a Summary tab with pass-count formulas per module/browser. |
| `ECommerce_API_Tests.postman_collection.json` | Postman collection (v2.1) with 21 requests across **Auth**, **Orders**, and **Inventory** endpoints. Each request has automated test scripts asserting status codes, response schemas, and error payloads. |
| `ECommerce_QA_Staging.postman_environment.json` | Companion Postman environment with placeholder variables (`base_url`, tokens, IDs) — import alongside the collection. |
| `Defect_Report.xlsx` | 16 logged bugs with severity/priority tagging, reproduction steps, expected vs. actual results, and status tracking. Includes a Summary tab with severity/status breakdown formulas. |

## How to use

1. **Manual testing** — open `Test_Cases.xlsx`. Each row is one test case; the Chrome/Firefox/Edge columns are color-coded (green = pass, red = fail) so cross-browser gaps are visible at a glance.
2. **API testing** — in Postman, import both `ECommerce_API_Tests.postman_collection.json` and `ECommerce_QA_Staging.postman_environment.json`, select the environment, fill in real `base_url`/ID values, then run the collection (or use the Collection Runner / Newman for CI).
3. **Defect tracking** — `Defect_Report.xlsx` cross-references the test cases that surfaced each bug (e.g., BUG-05 traces back to `TC-SRC-06`), so failures and defects stay linked.

## Coverage summary

- **82 manual test cases** — positive, negative, boundary, security (SQLi), and accessibility scenarios across 5 core flows.
- **21 API requests** — happy-path and negative cases for auth, order lifecycle, and inventory management, with schema and business-rule assertions.
- **16 defects logged** — 3 Critical, 5 High, 6 Medium, 2 Low; found across all three browsers plus the API layer.
