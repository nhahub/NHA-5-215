# Project Planning

This plan defines the project scope, team responsibilities, schedule, and success criteria for
automated UI testing of Swag Labs (SauceDemo).

## Project overview

**Project name:** Automated UI Testing for Swag Labs (SauceDemo)  
**Target website:** https://www.saucedemo.com/v1/index.html  
**Test language:** Java 17  
**UI automation tool:** Selenium WebDriver  
**Test framework:** JUnit 5 with Maven  
**Driver management:** WebDriverManager (auto-downloads ChromeDriver)

## Objective

Plan and implement an automated UI test suite for the main shopper journeys on Swag Labs.
The suite verifies that users can sign in, browse products, add a product to the cart,
and complete the checkout steps using synthetic test data.

Swag Labs is a public demo site intended for testing, so no production system or real customer
data is affected.

## Scope

### In scope

- Select and assess Swag Labs as the target test website.
- Document functional and non-functional requirements.
- Design manual test cases and expected results.
- Implement UI automation using Java, Selenium WebDriver, and JUnit 5.
- Cover the following sections:
  1. **Login** — sign-in page (valid, locked-out, invalid credentials)
  2. **Home page** — product listing page
  3. **Cart** — shopping cart (review items, remove items, proceed to checkout)
  4. **Checkout** — checkout flow (enter synthetic details, review order, order confirmation)
  5. **Side menu** — side navigation menu (navigate between sections, logout)
  6. **Footer** — page footer (links, copyright, company information)
- Document a conceptual SQL data model and API interaction plan for academic purposes.
- Record test outcomes and known limitations after implementation.

### Out of scope

- Building or changing the Swag Labs website.
- Accessing or modifying any private database or backend of the demo site.
- Placing real orders or using real payment information.
- Performance, security, or API testing (out of scope for this UI automation project).

## Team and responsibilities (Group G1)

| Team member | Role | Responsibilities |
|-------------|------|------------------|
| Omnia Ahmed Mohamed | Team Leader (G1) | Coordinate the project, assign tasks, track progress, review deliverables, and prepare the final report. |
| Mohamed Ali Abdelrahman | Sub Leader | Support the team leader, coordinate automation engineers, and review test implementation. |
| Abdallah Hosain Abdel Wahab Abdel Hamed | QA Automation Engineer | Implement product, cart, and checkout automation scenarios; review waits and suite execution. |
| Eman Abd Elhady Hassan | QA / Test Analyst | Prepare manual test cases, expected results, test data, evidence, and documentation. |
| Reham Hesham Roshdy Mohamed | QA / Test Analyst | Prepare manual test cases, expected results, test data, evidence, and documentation. |
| Mai Ramadan Mahmoud Ahmed | QA / Test Analyst | Prepare manual test cases, expected results, test data, evidence, and documentation. |

## Four-week plan

| Week | Planned work | Deliverables |
|------|--------------|--------------|
| 1 — Selection and planning | Confirm Swag Labs as target; verify availability; identify supported journeys; agree on requirements, roles, and project structure. | Target-site decision; approved scope; requirements draft; environment checklist. |
| 2 — Core journeys | Write manual scenarios and acceptance criteria for login, product selection, and cart actions. | Reviewed manual test cases; expected results; test-data plan. |
| 3 — Checkout and design | Document checkout behavior, validation cases, conceptual database entities, and API interaction plan. | Checkout scenarios; database/API design; UI/UX flow and state map. |
| 4 — Implementation and reporting | Implement and run the approved UI tests; review results; prepare documentation and presentation materials. | Source code; execution evidence; final report; presentation and demonstration video. |

## Success criteria

- Swag Labs is documented as the selected target website and its demo status is confirmed.
- Each in-scope journey (login, products, cart, checkout) has steps and expected results.
- Test outcomes can be traced to the documented scenarios.
- The final report distinguishes verified behavior from assumptions and unavailable features.
- No real customer or payment data is used.

## Open items

- Course-required Java version, test framework, and build tool: confirmed (Java 17, JUnit 5, Maven).
- Swag Labs test credentials: documented (standard_user / secret_sauce, etc.).
- Supported checkout and order-confirmation behavior: verified against Swag Labs demo.
