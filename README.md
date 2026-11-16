# Swag Labs — Automated UI Testing Project

**Project:** Automated UI Testing for Swag Labs (SauceDemo)  
**Target website:** https://www.saucedemo.com/v1/index.html  
**Test language:** Java 17  
**UI automation tool:** Selenium WebDriver 4  
**Test framework:** TestNG  
**Build tool:** Apache Maven  
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
2. **inventory** — product listing page (browse products)
3. **Cart** — shopping cart (review items, remove items, proceed to checkout)
4. **Checkout** — checkout flow (enter synthetic details, review order, order confirmation)
5. **Side menu** — side navigation menu (navigate between sections, logout)
6. **Footer** — page footer (links, copyright, company information)

### 1.4 Scope

#### In Scope
- Select and assess Swag Labs as the target test website.
- Document functional and non-functional requirements.
- Design manual test cases and expected results.
- Implement UI automation using Java, Selenium WebDriver 4, and TestNG.
- Use Page Object Model (POM) design pattern.
- Cover the six sections listed above: Login, Home page, Cart, Checkout, Side menu, Footer.
- Document a conceptual SQL data model and API interaction plan for academic purposes.
- Create and execute a Postman collection covering the main Swag Labs API interactions.
- Record test outcomes and known limitations after implementation.

#### Out of Scope
- Modifying the Swag Labs website.
- Accessing or modifying any private database or backend of the demo site.
- Placing real orders or using real payment information.
- Performance or security testing.

### 1.5 Tools & Framework
| Tool | Version | Purpose |
|------|---------|---------|
| Java | 17 | Test language |
| Selenium WebDriver | 4 | UI automation |
| TestNG | 7.9+ | Test framework (DEPI requirement) |
| Apache Maven | 3.8+ | Project management & build |
| WebDriverManager | Latest | Auto-downloads ChromeDriver |
| POM Pattern | — | Page Object Model for maintainability |
| Postman | Latest | API testing & collection documentation |
| Allure Report | 2.25+ | Test reporting with screenshots *(bonus)* |

### 1.6 Literature Review
Reference document: `literature_review_purpose.pdf` (included in project folder).  
This review covers automated UI testing principles, Selenium WebDriver best practices, Page Object Model (POM) design pattern, and test framework selection criteria for academic software testing projects.

### 1.7 Four-Week Plan

| Week | Planned Work | Deliverables | Status |
|------|--------------|--------------|--------|
| Week 1 — Selection and Planning | Confirm Swag Labs as target; verify availability; identify supported journeys; agree on requirements, roles, and project structure. | Target-site decision; approved scope; requirements draft; environment checklist. | ✅ Done |
| Week 2 — Core Journeys | Write manual test scenarios and acceptance criteria for login, product selection, and cart actions. | Reviewed manual test cases; expected results; test-data plan. | ✅ Done |
| Week 3 — Checkout and Design | Document checkout behavior, validation cases, conceptual database entities, and API interaction plan. | Checkout scenarios; database/API design; UI/UX flow and state map. | 🔄 In Progress |
| Week 4 — Implementation and Reporting | Implement and run the approved UI tests using TestNG + Selenium 4; review results; prepare documentation and presentation materials. | Source code; execution evidence; final report; presentation and demonstration video. | ⏳ Next |

### 1.8 Success Criteria
- Swag Labs is documented as the selected target website and its demo status is confirmed.
- Each in-scope section (Login, Home page, Cart, Checkout, Side menu, Footer) has steps and expected results.
- Test outcomes are traceable to the documented scenarios (via Google Sheets).
- The final report distinguishes verified behavior from assumptions and unavailable features.
- No real customer or payment data is used.
- Automation framework follows POM design pattern with TestNG.

### 1.9 Risk Assessment and Mitigation

| Risk | Likelihood | Impact | Mitigation |
|------|------------|--------|------------|
| ChromeDriver version mismatch with installed Chrome | Medium | High | Use WebDriverManager for automatic driver management. |
| Swag Labs demo site temporarily unavailable | Low | High | Verify site availability in Week 1; document downtime. |
| Element locators change on demo site | Medium | Medium | Use Page Object Model (POM) for centralized locator updates. |
| Flaky tests due to page load timing | Medium | Medium | Implement explicit waits (WebDriverWait) instead of Thread.sleep. |
| Checkout flow creates demo orders | Low | Low | Use synthetic data only; orders are test/demo data. |
| Swag Labs API endpoints not fully documented | Medium | Medium | Document observable network requests via browser dev tools; note limitations in report. |

### 1.10 Expected Deliverables
- Manual test cases documented in Google Sheets
- Bug reports documented in Google Sheets (with screenshots/video evidence)
- Source code (Java + Selenium 4 + TestNG + Maven + POM)
- Test execution evidence (Allure reports with screenshots)
- Postman collection (API testing for Swag Labs interactions)
- Test summary report (manual + automation + API metrics)
- Final project report
- Presentation slides (5–10 minutes)

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

### Prerequisites
- Java JDK 17 or later
- Apache Maven 3.8 or later
- Google Chrome browser installed
- Internet connection (WebDriverManager downloads ChromeDriver automatically)

### Project Structure (POM Pattern)
```
src/
├── main/java/
│   └── pages/          ← Page Object classes
│       ├── LoginPage.java
│       ├── HomePage.java
│       ├── CartPage.java
│       ├── CheckoutPage.java
│       ├── SideMenuPage.java
│       └── FooterPage.java
└── test/java/
    └── tests/          ← TestNG test classes
        ├── LoginTest.java
        ├── HomePageTest.java
        ├── CartTest.java
        ├── CheckoutTest.java
        ├── SideMenuTest.java
        └── FooterTest.java
```

### How to Run the Tests
```bash
git clone <repository-url>
cd <folder-name>
mvn clean test
```

### Key Maven Dependencies (`pom.xml`)
```xml
<!-- Selenium WebDriver 4 -->
<dependency>
    <groupId>org.seleniumhq.selenium</groupId>
    <artifactId>selenium-java</artifactId>
    <version>4.18.1</version>
</dependency>

<!-- TestNG -->
<dependency>
    <groupId>org.testng</groupId>
    <artifactId>testng</artifactId>
    <version>7.9.0</version>
    <scope>test</scope>
</dependency>

<!-- WebDriverManager -->
<dependency>
    <groupId>io.github.bonigarcia</groupId>
    <artifactId>webdrivermanager</artifactId>
    <version>5.7.0</version>
    <scope>test</scope>
</dependency>

<!-- Allure TestNG (Bonus) -->
<dependency>
    <groupId>io.qameta.allure</groupId>
    <artifactId>allure-testng</artifactId>
    <version>2.25.0</version>
    <scope>test</scope>
</dependency>
```

---

## 5. Deliverables Submission (GitHub)

Per DEPI guidelines, the following must be uploaded to the team GitHub repository:
1. Manual test cases exported from Google Sheets
2. Bug reports exported from Google Sheets
3. Test automation framework (Java + Selenium 4 + TestNG + Maven)
4. Postman collection file (.json)
5. Test summary report
6. Presentation of the overall effort

---

## 6. References
- Swag Labs (SauceDemo): https://www.saucedemo.com/v1/index.html
- Selenium WebDriver: https://www.selenium.dev/
- TestNG Documentation: https://testng.org/
- Apache Maven: https://maven.apache.org/
- WebDriverManager: https://github.com/bonigarcia/webdrivermanager
- Allure Report: https://allurereport.org/
- Postman: https://www.postman.com/

---

## 7. Note
This is a student academic project for educational purposes as part of the DEPI Software Testing track. Swag Labs is a public demo website intended for testing practice. No real customer or payment data is used.
