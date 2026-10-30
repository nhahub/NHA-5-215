# Project Planning

This plan defines the project scope, team responsibilities, schedule, and success criteria while the target website remains to be selected.

## Project overview

This section records the project's identity, target, and proposed testing tools.

**Project name:** Automated UI Testing for an E-Commerce Website  
**Target website:** TBD  
**Planned test language:** Java  
**Planned UI automation tool:** Selenium WebDriver  
**Planned test framework:** JUnit 5 with Maven (proposed; confirm with the course requirements)

## Objective

Plan an automated UI test suite for the main user journeys of a selected public e-commerce website. The suite will verify that users can sign in, browse or search for products where supported, add a product to the cart, and complete the available checkout steps using test data.

The team will confirm the target website and its permitted test scenarios before finalizing the requirements, test cases, and implementation details.

## Scope

This section sets the project boundaries while the target website remains undecided.

### In scope

The project includes the planning and testing activities listed below.

- Select and assess a suitable e-commerce test website.
- Document functional and non-functional requirements.
- Design manual test cases and expected results.
- Plan UI automation using Java and Selenium WebDriver.
- Cover login, product selection, cart, and checkout journeys where the site supports them.
- Document a conceptual SQL data model and API interaction plan for academic purposes.
- Record test outcomes and known limitations after implementation.

### Out of scope

The project excludes changes to the target system and activities that could affect real customers.

- Building or changing the target e-commerce website.
- Accessing or modifying a third-party website's private production database.
- Placing real orders or using real payment information.
- Assuming that the selected website exposes a public API before verifying it.

## Team and responsibilities

The proposal assigns the following roles to the four team members.

| Team member | Role | Responsibilities |
|---|---|---|
| Omnia Ahmed Mohamed | Team Leader (G1) | Coordinate the project, assign tasks, track progress, review deliverables, and prepare the final report. |
| Mohamed Ali Abdelrahman | QA Automation Engineer | Assess the test environment, plan browser and driver setup, and contribute to login automation and page-object design. |
| Abdallah Hosain Abdel Wahab Abdel Hamed | QA Automation Engineer | Contribute to product, cart, and checkout scenarios and review waits and suite execution. |
| Eman Abd Elhady Hassan | QA/Test Analyst | Prepare manual test cases, expected results, test data, evidence, and documentation. |

## Four-week plan

The schedule preserves the proposal's four-week structure and makes website selection the first activity.

| Week | Planned work | Deliverables |
|---|---|---|
| 1 — Selection and planning | Select the target website; verify that it is available for testing; identify supported journeys; agree on requirements, roles, and project structure. | Target-site decision; approved scope; requirements draft; environment checklist. |
| 2 — Core journeys | Write manual scenarios and acceptance criteria for login, product selection, and cart actions that the target site supports. | Reviewed manual test cases; expected results; test-data plan. |
| 3 — Checkout and design | Document checkout behavior, validation cases, conceptual database entities, and any verified API interactions. | Checkout scenarios; database/API design; UI/UX flow and state map. |
| 4 — Implementation and reporting | Implement and run the approved UI tests; review the results; prepare documentation and presentation materials. | Source code; execution evidence; final report; presentation PDF and demonstration video. |

## Success criteria

Use these criteria to decide whether the project deliverables meet the plan.

- The target website and testing permission or demo status are documented.
- Each in-scope journey has steps and expected results.
- Test outcomes can be traced to the documented scenarios.
- The final report distinguishes verified behavior from assumptions and unavailable features.
- No real customer or payment data is used.

## Open items

Resolve these items before finalizing site-specific requirements and test designs.

- Target website and its test credentials: **TBD**
- Supported search, checkout, and order-confirmation behavior: **TBD**
- Course-required Java version, test framework, and build tool: **TBD**
- Whether the selected site exposes an API or test database: **TBD**
