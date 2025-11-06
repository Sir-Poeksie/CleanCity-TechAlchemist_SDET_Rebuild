# CleanCity Waste Pickup Scheduler – Automation Framework Design

**Purpose:** Define the architecture, components, and reusable practices for automated testing across the CleanCity Waste Pickup Scheduler project.
**Scope:** All automated test types: Unit, Integration, End-to-End (E2E), API, Performance, and Security.
**Prepared by:** [Your Name]
**Date:** [Insert Date]
**Version:** 1.0

---

## 1. Framework Overview

* **Testing Approach:** Hybrid (TDD + BDD)

  * **TDD:** Unit and service-level tests guide development.
  * **BDD:** Feature flows and user scenarios drive E2E testing.
* **Framework Type:** Modular, data-driven, Page Object Model (POM) for E2E, with utility libraries for API, unit, and performance tests.
* **Automation Tools:**

  * **Unit Testing:** Jest (React components / Node.js services)
  * **E2E:** Cypress for front-end flows, Selenium WebDriver for cross-browser and legacy flows
  * **API Testing:** Postman / Newman or REST-assured (JavaScript/Python)
  * **Performance Testing:** JMeter
  * **Security Testing:** OWASP ZAP for automated vulnerability scans
* **Reporting:** Mochawesome, Allure, or custom JSON/HTML reports integrated into CI/CD pipelines

---

## 2. Architecture Principles

* **Modularity:** Tests are divided by type (unit, integration, E2E, API) and by feature/module for maintainability.
* **Reusability:** Page Objects, helper methods, and test data are centralized for reuse across test suites.
* **Data-Driven Testing:** Test inputs and expected results stored in JSON/CSV files for flexible scenario execution.
* **Scalability:** Framework supports parallel execution, distributed test runners, and CI/CD integration.
* **Traceability:** Every automated test maps to a **Functional Requirement (FR), User Story (US), and Test Case (TC)** in the RTM.

---

## 3. Folder Structure

```
/automation
├── /e2e
│   ├── /pages         # Page Object Model classes
│   ├── /tests         # Cypress/Selenium test files
│   ├── /fixtures      # Test data (JSON/CSV)
│   └── /support       # Custom commands/helpers
├── /api
│   ├── /tests         # API test scripts
│   ├── /data          # JSON payloads for endpoints
│   └── /utils         # API request helpers
├── /unit
│   ├── /components    # Jest React component tests
│   └── /services      # Service & utility function tests
├── /performance
│   └── /scripts       # JMeter test plans
├── /security
│   └── /scripts       # OWASP ZAP automated scans
└── /config
    ├── cypress.config.js
    ├── selenium.config.js
    ├── jest.config.js
    ├── postman.env.json
    └── jmeter.properties
```

---

## 4. Reusable Components

* **Page Objects:** Encapsulate page elements and actions, ensuring maintainability.
* **Custom Commands:** Cypress / Selenium commands for repeated actions (login, navigation, form submission).
* **API Helpers:** Centralized methods for GET, POST, PUT, DELETE requests with authentication handling.
* **Data-Driven Tests:** JSON/CSV input for multiple scenarios per test case.
* **Assertions & Reporting:** Jest matchers, Cypress/Chai assertions, and Mochawesome/Allure reporting.
* **Utilities:**

  * Environment management (`dev`, `qa`, `prod`)
  * Logging & debugging helpers
  * Retry & wait strategies for dynamic UI/API behavior

---

## 5. Test Execution

* **Unit / Integration:** `npm run test:unit` → Jest
* **E2E:** `npm run test:e2e` → Cypress / Selenium
* **API:** `npm run test:api` → Postman / Newman
* **Performance:** `npm run test:perf` → JMeter
* **Security:** `npm run test:security` → OWASP ZAP
* **Parallel Execution:** Cypress parallel mode and Selenium Grid configured for large-scale regression runs

---

## 6. CI/CD Integration

* **Pipeline:** GitHub Actions or Jenkins
* **Triggers:** On pull request, merge to `main`, and scheduled nightly runs
* **Artifacts:** Screenshots, videos, JSON/HTML reports, and test logs
* **Notifications:** Slack/email integration for build/test results
* **Quality Gates:** Fail build if critical tests fail or code coverage drops below threshold

---

## 7. Best Practices

1. Maintain **one test case per FR/US/TC** mapping for traceability.
2. Use **modular, reusable components** for maintainability.
3. Keep **test data separate** from test logic.
4. Automate **critical paths and high-risk scenarios** first.
5. Review and update framework regularly as application evolves.
6. Integrate **security, performance, and accessibility checks** into automated pipelines where feasible.