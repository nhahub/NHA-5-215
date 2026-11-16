# Project Planning

This plan defines the project scope, team responsibilities, schedule, and success criteria for automated UI testing of Swag Labs (SauceDemo).

## Project Overview

**Project name:** Automated UI Testing for Swag Labs (SauceDemo)  
**Target website:** https://www.saucedemo.com/v1/index.html  
**Test language:** Java 17  
**UI automation tool:** Selenium WebDriver 4  
**Test framework:** TestNG  
**Design pattern:** Page Object Model (POM)  
**Build tool:** Apache Maven  
**Driver management:** WebDriverManager (auto-downloads ChromeDriver)  
**API testing tool:** Postman  
**Reporting:** Allure Report with screenshots *(bonus)*

## Objective

Plan and implement an automated UI test suite for the main shopper journeys on Swag Labs. The suite verifies that users can sign in, browse products, add a product to the cart, and complete the checkout steps using synthetic test data.

Swag Labs is a public demo site intended for testing, so no production system or real customer data is affected.

## Scope

### In Scope

- Select and assess Swag Labs as the target test website.
- Document functional and non-functional requirements.
- Design manual test cases and expected results (via Google Sheets).
- Document and report all bugs found during manual testing (with screenshots/video).
- Implement UI automation using Java, Selenium WebDriver 4, and TestNG.
- Apply POM design pattern for all page interactions.
- Cover the following sections:
  1. **Login** — sign-in page (valid, locked-out, invalid credentials)
  2. **inventory** — product listing page
  3. **Cart** — shopping cart (review items, remove items, proceed to checkout)
  4. **Checkout** — checkout flow (enter synthetic details, review order, order confirmation)
  5. **Side menu** — side navigation menu (navigate between sections, logout)
  6. **Footer** — page footer (links, copyright, company information)
- Document a conceptual SQL data model and API interaction plan for academic purposes.
- Create and execute a Postman collection covering the main Swag Labs API interactions.
- Record test outcomes and known limitations after implementation.
- Produce a test summary report with manual, automation, and API metrics.

### Out of Scope

- Building or changing the Swag Labs website.
- Accessing or modifying any private database or backend of the demo site.
- Placing real orders or using real payment information.
- Performance, security, or load testing.

## Team and Responsibilities (Group G1)

| Team Member | Role | Responsibilities |
|-------------|------|------------------|
| Omnia Ahmed Mohamed | Team Leader | Coordinate the project, assign tasks, track progress, review deliverables, and prepare the final report. |
| Mohamed Ali Abdelrahman | Sub Leader | Support the team leader, coordinate automation engineers, and review test implementation. |
| Abdallah Hosain Abdel Wahab Abdel Hamed | Member | Contribute to project tasks and documentation. |
| Eman Abd Elhady Hassan | Member | Contribute to project tasks and documentation. |
| Reham Hesham Roshdy Mohamed | Member | Contribute to project tasks and documentation. |
| Mai Ramadan Mahmoud Ahmed | Member | Contribute to project tasks and documentation. |

## Four-Week Plan

| Week | Planned Work | Deliverables | Status |
|------|--------------|--------------|--------|
| Week 1 — Selection and Planning | Confirm Swag Labs as target; verify availability; identify supported journeys; agree on requirements, roles, and project structure. | Target-site decision; approved scope; requirements draft; environment checklist. | ✅ Done |
| Week 2 — Core Journeys | Write manual scenarios and acceptance criteria for login, product selection, and cart actions. Record bugs with evidence. | Reviewed manual test cases; expected results; test-data plan; bug reports. | ✅ Done |
| Week 3 — Checkout and Design | Document checkout behavior, validation cases, conceptual database entities, and API interaction plan. Complete remaining manual test cases. | Checkout scenarios; database/API design; UI/UX flow and state map; full manual test suite. | 🔄 In Progress |
| Week 4 — Implementation and Reporting | Implement and run the approved UI tests using TestNG + Selenium 4 + POM; review results; prepare documentation and presentation materials. | Source code; Allure execution report; test summary report; final report; presentation. | ⏳ Next |

## Success Criteria

- Swag Labs is documented as the selected target website and its demo status is confirmed.
- Each in-scope journey (Login, Home page, Cart, Checkout, Side menu, Footer) has test cases with steps and expected results in Google Sheets.
- All bugs are documented with evidence (screenshots or video) in Google Sheets.
- Test outcomes can be traced to the documented scenarios.
- Automation framework follows POM design pattern with TestNG.
- The final report includes manual and automation execution metrics with charts.
- The final report distinguishes verified behavior from assumptions and unavailable features.
- No real customer or payment data is used.
- All deliverables are uploaded to the team GitHub repository.

## Deliverables Checklist

### Manual Testing
- [ ] Detailed test cases in Google Sheets (linked to user stories)
- [ ] Bug reports in Google Sheets (with screenshots/video, linked to test cases)
- [ ] Google Sheets exported and uploaded to GitHub

### Automation
- [ ] Project structure following POM pattern
- [ ] Test classes using TestNG annotations
- [ ] WebDriverManager integration for ChromeDriver
- [ ] Allure report configuration *(bonus)*

### API Testing
- [ ] Postman collection covering Swag Labs API interactions
- [ ] Postman collection exported as .json and uploaded to GitHub
- [ ] API test results documented in test summary report

### Reports & Presentation
- [ ] Test summary report (manual + automation metrics with charts)
- [ ] Final project report
- [ ] Presentation (5–10 minutes, PowerPoint or similar)
- [ ] GitHub repository with all deliverables including Postman collection

## Open Items

- Google Sheets: team to confirm all manual test cases and bugs are filled correctly before export.
- GitHub repository: confirm repository is accessible and all team members have push access.
- TestNG configuration (`testng.xml`): to be created during Week 4 implementation.
- Allure report setup: optional bonus — to be added after core automation is working.
