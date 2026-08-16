# Ecommerce-QA

Manual QA documentation for the e-commerce practice website [AutomationExercise.com](https://www.automationexercise.com).

## Contents

| File / Folder | Purpose |
| --- | --- |
| `test-plan.md` | Test plan: scope, approach, environment, schedule |
| `test-cases.xlsx` | 20 test cases covering home, products, cart, subscription, login/signup, contact |
| `test-summary.md` | Execution results summary and sign-off report |
| `bug-reports/` | Defect reports (add per-defect files here) |

## Test Coverage

- **Home Page** — layout, navigation, categories, brands, recommended items
- **Products** — listing, search (valid/invalid), product details
- **Cart** — add to cart, quantity, totals, remove items
- **Subscription** — footer newsletter (valid/invalid email)
- **Login / Signup** — valid/invalid login, new signup, duplicate email
- **Contact Us** — form submission

## Workflow

1. Review `test-plan.md` for scope and approach.
2. Execute test cases from `test-cases.xlsx`.
3. Log failures as defect files under `bug-reports/`.
4. Record results in `test-summary.md` and obtain sign-off.

## Requirements

- A browser (Chrome, Firefox, Edge, or Safari)
- Access to https://www.automationexercise.com
- Spreadsheet software to view/edit `test-cases.xlsx`