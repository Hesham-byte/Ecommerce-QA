# Test Plan — AutomationExercise.com

## 1\. Introduction

This test plan describes the scope, approach, resources, and schedule for testing the e-commerce practice website **AutomationExercise.com**. The site provides full-fledged functionality (product browsing, search, cart, user accounts, newsletter subscription, and contact) for QA engineers to practice manual and automation testing.

## 2\. Objectives

*   Validate that all core e-commerce flows (browse, search, view product, add to cart, manage cart) work as expected.
*   Validate user account features (signup, login) including error handling.
*   Validate newsletter subscription, contact us, and navigation.
*   Identify and document defects via bug reports.
*   Ensure the site is stable across supported browsers.

## 3\. Scope

### In Scope

| Module         | Description                                                                                             |
| -------------- | ------------------------------------------------------------------------------------------------------- |
| Home Page      | Layout, categories, brands, features items, recommended items                                           |
| Navigation     | Header links (Home, Products, Cart, Signup/Login, Test Cases, API Testing, Video Tutorials, Contact us) |
| Products       | Product listing, search, product detail page                                                            |
| Cart           | Add to cart, quantity, view cart, totals, remove items                                                  |
| Subscription   | Footer newsletter signup                                                                                |
| Login / Signup | Valid/invalid login, new user signup, duplicate email                                                   |
| Contact Us     | Contact form submission                                                                                 |

### Out of Scope

*   API Testing / API endpoints (separate test effort)
*   Third-party integrations (payment gateways, shipping)
*   Performance, load, and security testing (separate test efforts)

## 4\. Test Approach

Manual functional testing is performed using black-box techniques, including:

*   **Equivalence Partitioning & Boundary Value Analysis** — for search, quantity, and form validation
*   **Positive / Negative Testing** — valid vs. invalid credentials and email formats
*   **Exploratory Testing** — to discover unexpected behavior in navigation and cart flows
*   **Regression Testing** — re-running the full suite after any fixes

## 5\. Test Environment

| Component       | Specification                                                        |
| --------------- | -------------------------------------------------------------------- |
| Application URL | https://www.automationexercise.com                                   |
| Browsers        | Chrome, Firefox, Edge, Safari (latest versions)                      |
| OS              | Windows 10/11, macOS, Android/iOS (responsive checks)                |
| Test Data       | Generated unique emails, standard product names, sample search terms |

## 6\. Test Deliverables

*   `test-cases.xlsx` — 20 test cases with steps, test data, and expected results
*   `test-summary.md` — results summary after execution
*   `bug-reports/` — defect reports for any failed cases
*   `test-plan.md` — this document

## 7\. Test Case Breakdown

| Module       | Test Cases                                  |
| ------------ | ------------------------------------------- |
| Home Page    | TC\_001, TC\_002, TC\_003, TC\_004, TC\_013 |
| Products     | TC\_005, TC\_006, TC\_007, TC\_008          |
| Cart         | TC\_009, TC\_010, TC\_011, TC\_012          |
| Subscription | TC\_014, TC\_015                            |
| Login        | TC\_016, TC\_017                            |
| Signup       | TC\_018, TC\_019                            |
| Contact Us   | TC\_020                                     |

## 8\. Entry / Exit Criteria

### Entry Criteria

*   Application is accessible at the test URL.
*   Test data and environment are prepared.
*   Test cases are written and reviewed.

### Exit Criteria

*   All test cases executed.
*   All high-severity defects resolved or accepted with justification.
*   Test summary report completed and signed off.

## 9\. Defect Management

Defects found during testing are logged in `bug-reports/` with:

*   Unique ID, severity, priority
*   Steps to reproduce
*   Expected vs. actual result
*   Environment (browser/OS)
*   Screenshot/attachment (if available)

## 10\. Risks & Mitigations

| Risk                                      | Impact               | Mitigation                                    |
| ----------------------------------------- | -------------------- | --------------------------------------------- |
| Dynamic content/cookies between test runs | Inconsistent results | Use fresh session / incognito per test run    |
| Duplicate account emails                  | Signup test failures | Generate unique emails per run                |
| Site availability                         | Testing blocked      | Schedule during stable hours, retry mechanism |

## 11\. Schedule

| Phase                            | Duration |
| -------------------------------- | -------- |
| Test planning & test case design | 1 day    |
| Test execution (full suite)      | 1–2 days |
| Defect reporting & regression    | 1 day    |
| Test summary & sign-off          | 0.5 day  |