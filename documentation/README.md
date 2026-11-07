# Project Documentation

**Project:** Automated UI Testing for Swag Labs (SauceDemo)  
**Target website:** [Swag Labs (SauceDemo)](https://www.saucedemo.com/v1/index.html)  
**Test language:** Java 17  
**UI automation tool:** Selenium WebDriver  
**Test framework:** JUnit 5 with Maven  

This folder contains the project documentation for the automated UI testing of Swag Labs,
a public demo e-commerce site used for testing and learning purposes.

## Documents

Open the document that matches the section you need to review.

- [Project Planning](project-planning.md)
- [Stakeholder Analysis](stakeholder-analysis.md)
- [Database and API Design](database-and-api-design.md)
- [UI/UX Design](ui-ux-design.md)

## Current scope

The project plans to test key e-commerce user journeys on Swag Labs using Java and Selenium:

- **Sign in** — valid credentials, locked-out user, invalid credentials
- **Products** — browse product list, sort products, add product to cart
- **Cart** — review cart contents, remove items
- **Checkout** — complete checkout with synthetic test data and reach order confirmation

SQL and API material is documented conceptually for the course. UI automation against Swag Labs
does not require direct access to the site's database or API. No real customer or payment data is used.
