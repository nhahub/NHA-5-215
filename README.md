# Swag Labs — Automated UI Testing Project

**Project:** Automated UI Testing for Swag Labs (SauceDemo)  
**Target website:** https://www.saucedemo.com/v1/index.html  
**Test language:** Java 17  
**UI automation tool:** Selenium WebDriver  
**Test framework:** JUnit 5 with Maven  
**Course:** DEPI — Software Testing Project  
**Group:** G1  

---

## 1. Project Proposal

### 1.1 Project Title
Automated UI Testing for an E-Commerce Demo Website (Swag Labs / SauceDemo) using Java and Selenium.

### 1.2 Project Background / Problem Statement
Manual testing of e-commerce user journeys (login, product browsing, cart, checkout) is time-consuming, repetitive, and prone to human error. As websites grow, regression testing becomes increasingly difficult to perform consistently. This project addresses the need for automated UI testing by implementing a Selenium-based test suite that verifies critical shopper journeys on Swag Labs, a public demo e-commerce site designed for testing practice.

### 1.3 Objective
Design and implement an automated UI test suite covering the main shopper journeys on Swag Labs:

1. **Login** — sign-in page (valid credentials, locked-out user, invalid credentials)
2. **Home page** — product listing page (browse products)
3. **Cart** — shopping cart (review items, remove items, proceed to checkout)
4. **Checkout** — checkout flow (enter synthetic details, review order, order confirmation)
5. **Side menu** — side navigation menu (navigate between sections, logout)
6. **Footer** — page footer (links, copyright, company information)

### 1.4 Scope

#### In Scope
- Select and assess Swag Labs as the target test website.
- Document functional and non-functional requirements.
- Design manual test cases and expected results.
- Implement UI automation using Java, Selenium WebDriver, and JUnit 5.
- Cover the six sections listed above: Login, Home page, Cart, Checkout, Side menu, Footer.
- Document a conceptual SQL data model and API interaction plan for academic purposes.
- Record test outcomes and known limitations after implementation.

#### Out of Scope
- Modifying the Swag Labs website.
- Accessing or modifying any private database or backend of the demo site.
- Placing real orders or using real payment information.
- Performance, security, or API testing (out of scope for this UI automation project).

### 1.5 Planned Tools
- Java 17
- Selenium WebDriver
- JUnit 5 (JUnit Jupiter)
- Apache Maven
- WebDriverManager (auto-downloads ChromeDriver)

### 1.6 Literature Review
Reference document: `literature_review_purpose.pdf` (included in project folder).  
This review covers automated UI testing principles, Selenium WebDriver best practices, Page Object Model (POM) design pattern, and test framework selection criteria for academic software testing projects.

### 1.7 Four-Week Plan

| Week | Planned Work | Deliverables |
|------|--------------|--------------|
| Week 1 — Selection and Planning | Confirm Swag Labs as target; verify availability; identify supported journeys; agree on requirements, roles, and project structure. | Target-site decision; approved scope; requirements draft; environment checklist. |
| Week 2 — Core Journeys | Write manual test scenarios and acceptance criteria for login, product selection, and cart actions. | Reviewed manual test cases; expected results; test-data plan. |
| Week 3 — Checkout and Design | Document checkout behavior, validation cases, conceptual database entities, and API interaction plan. | Checkout scenarios; database/API design; UI/UX flow and state map. |
| Week 4 — Implementation and Reporting | Implement and run the approved UI tests; review results; prepare documentation and presentation materials. | Source code; execution evidence; final report; presentation and demonstration video. |

### 1.8 Success Criteria
- Swag Labs is documented as the selected target website and its demo status is confirmed.
- Each in-scope section (Login, Home page, Cart, Checkout, Side menu, Footer) has steps and expected results.
- Test outcomes are traceable to the documented scenarios.
- The final report distinguishes verified behavior from assumptions and unavailable features.
- No real customer or payment data is used.

### 1.9 Risk Assessment and Mitigation

| Risk | Likelihood | Impact | Mitigation |
|------|------------|--------|------------|
| ChromeDriver version mismatch with installed Chrome | Medium | High | Use WebDriverManager for automatic driver management. |
| Swag Labs demo site temporarily unavailable | Low | High | Verify site availability in Week 1; document downtime. |
| Element locators change on demo site | Medium | Medium | Use Page Object Model for centralized locator updates. |
| Flaky tests due to page load timing | Medium | Medium | Implement explicit waits (WebDriverWait) instead of Thread.sleep. |
| Checkout flow creates demo orders | Low | Low | Use synthetic data only; orders are test/demo data. |

### 1.10 Expected Deliverables
- Source code (Java + Selenium + JUnit 5 + Maven)
- Test execution evidence (screenshots, reports)
- Final project report
- Presentation slides and demonstration video
- Documentation (planning, stakeholder analysis, UI/UX design, database/API design)

---

## 2. Team Members — Group G1

| # | Name | Role |
|---|------|------|
| 1 | Omnia Ahmed Mohamed | Team Leader |
| 2 | Mohamed Ali Abdelrahman | Sub Leader |
| 3 | Abdallah Hosain Abdel Wahab Abdel Hamed | Member |
| 4 | Eman Abd Elhady Hassan | Member |
| 5 | Reham Hesham Roshdy Mohamed | Member |
| 6 | Mai Ramadan Mahmoud Ahmed | Member |

---

## 3. Demo Test Data (Synthetic — Not Real)

| Username | Password | Expected Result |
|----------|----------|-----------------|
| standard_user | secret_sauce | Successful login |
| locked_out_user | secret_sauce | Login blocked (error message) |
| problem_user | secret_sauce | Login succeeds (unusual UI behavior) |
| performance_glitch_user | secret_sauce | Login succeeds (slower page loads) |
| invalid_user | secret_sauce | Login blocked (invalid credentials) |

*All checkout data used in tests is synthetic and for academic purposes only.*

---

## 4. Requirements to Run
- Java JDK 17 or later
- Apache Maven 3.8 or later
- Google Chrome browser installed
- Internet connection (WebDriverManager downloads ChromeDriver automatically)

### How to Run the Tests
```bash
git clone <repository-url>
cd <folder-name>
mvn clean test
```

---

## 5. References
- Swag Labs (SauceDemo): https://www.saucedemo.com/v1/index.html
- Selenium WebDriver: https://www.selenium.dev/
- JUnit 5 User Guide: https://junit.org/junit5/docs/5.11.0/user-guide/
- Apache Maven: https://maven.apache.org/
- WebDriverManager: https://github.com/bonigarcia/webdrivermanager

---

## 6. Note
This is a student academic project for educational purposes. Swag Labs is a public demo website intended for testing practice. No real customer or payment data is used.
