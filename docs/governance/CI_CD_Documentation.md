# CI/CD Documentation – CleanCity Waste Pickup Scheduler

**Purpose:** Outline the continuous integration and deployment pipeline for QA and Dev teams.

**Prepared by:** Mpumelelo Theophilas Nxazonke  
**Date:** 2025-11-06  
**Version:** 1.0  

---

## 1. Pipeline Overview

- **CI/CD Tool:** GitHub Actions  
- **Triggers:** On `push` to feature/main branches, on PR creation  
- **Stages:**  
  1. **Code Checkout**  
  2. **Install Dependencies** (`npm install`)  
  3. **Unit & Integration Tests** (Jest)  
  4. **E2E Tests** (Cypress/Selenium)  
  5. **API Tests** (Postman/Newman)  
  6. **Security & Static Analysis** (Snyk, ESLint)  
  7. **Build & Artifact Generation**  
  8. **Deployment** (Staging → Production)

---

## 2. Environment Strategy

- **Staging:** Full replica of production for testing.  
- **Production:** Deployment via CI/CD with automated smoke tests.  
- **Rollback:** Versioned releases with automated rollback on failure.

---

## 3. Reporting & Notifications

- Test reports published to `mochawesome-report/` and GitHub Actions artifacts.  
- Failure alerts sent to Dev/QA Slack channels.  
- CI/CD logs retained for audit & traceability.