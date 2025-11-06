Excellent — your structure is already **95% aligned** with an enterprise-grade QA/SDET repo 👏.
That gives us the perfect foundation to generate the 3 requested deliverables.

---

## 🧩 Deliverable 1: `docs/governance/Migration_Plan_CleanCity.md`

````markdown
# 🧭 Migration Plan – CleanCity Group 15

**Project Repository:** `CleanCity-Group15`  
**Location:** `C:\Users\Theophilas\Desktop\DevProjects\CleanCity-Group15`  
**Author:** QA/SDET Migration Team  
**Version:** 1.0.0  
**Date:** 2025-11-06  

---

## 1. Objective

To migrate the CleanCity Waste Scheduler from a single-layer QA project into a fully governed, enterprise-compliant **SDET repository** supporting:
- Structured QA documentation hierarchy  
- TDD and BDD testing workflows  
- Continuous Integration (CI/CD) automation  
- Governance and reporting consistency  

---

## 2. Repository Migration Overview

| Category | Action | Result |
|-----------|--------|--------|
| Source Code | Existing `src/` retained; subdirectories realigned for modular design | Components, backend, shared utilities clearly separated |
| Testing | Cypress and Jest tests consolidated into `/tests/` folders | Unit, Integration, E2E, Security, Performance tiers |
| Documentation | Final reports and business docs merged under `/docs/` | Structured in `business-dev/`, `qa/`, and `governance/` |
| Reports | HTML reports from Jest/Cypress relocated | Stored under `/docs/qa/06_Test_Reports/` |
| Pipelines | CI/CD definitions under `/pipelines/` and `.github/workflows/` | Enables automated testing and reporting |
| Governance | Policy and project-level oversight centralized | `/docs/governance/QA_Governance_Policy.md` |

---

## 3. Component & Test Mapping

| Component | Location | Test File | FR Reference |
|------------|-----------|------------|---------------|
| Home | `src/components/Home.js` | `_tests_/Home.test.js` | FR-012 |
| Dashboard | `src/components/Dashboard.js` | `_tests_/Dashboard.test.js` | FR-023–FR-028 |
| Awareness | `src/components/Awareness.js` | `_tests_/Awareness.test.js` | FR-036–FR-040 |
| Profile | `src/components/profile/Profile.js` | `_tests_/Profile.test.js` | FR-045–FR-048 |
| Admin | `src/components/Admin.js` | `_tests_/Admin.test.js` | FR-053–FR-056 |
| Blog | `src/components/blog/*.js` | `_tests_/Blog*.test.js` | FR-060–FR-065 |

Each test begins with annotations linking to functional requirements:
```js
// @requirement: FR-012
// @feature: Waste Pickup Scheduling
````

---

## 4. Test Framework Distribution

| Framework                     | Purpose                      | Directory                        | Report Output                                  |
| ----------------------------- | ---------------------------- | -------------------------------- | ---------------------------------------------- |
| Jest + React Testing Library  | Unit and Integration Testing | `/src/_tests_/` → `/tests/unit/` | `/docs/qa/06_Test_Reports/jest-report.html`    |
| Cypress + Mochawesome         | End-to-End UI Testing        | `/cypress/e2e/` → `/tests/e2e/`  | `/docs/qa/06_Test_Reports/mochawesome.html`    |
| Selenium (optional)           | Browser Compatibility        | `/tests/e2e/selenium/`           | `/docs/qa/06_Test_Reports/selenium-summary.md` |
| Performance (Lighthouse, axe) | Accessibility + Load         | `/tests/performance/`            | `/docs/qa/07_Performance_Testing.md`           |

---

## 5. Folder Mapping Summary

| Current Location       | New Location                | Notes                                                   |
| ---------------------- | --------------------------- | ------------------------------------------------------- |
| `/cypress/e2e/`        | `/tests/e2e/`               | E2E suites retained under structured BDD/feature format |
| `/src/_tests_/`        | `/tests/unit/`              | All Jest + RTL tests                                    |
| `/final_docs/`         | `/docs/qa/`                 | Legacy QA documentation archived here                   |
| `/docs/*.md`           | `/docs/business-dev/`       | PRD, BRD, and SRS relocated                             |
| `/mochawesome-report/` | `/docs/qa/06_Test_Reports/` | Keep only generated HTML + JSON                         |
| `/jest-report/`        | `/docs/qa/06_Test_Reports/` | Coverage summary                                        |

---

## 6. CI/CD & Governance Integration

| Area            | Tool                                 | Location                       |
| --------------- | ------------------------------------ | ------------------------------ |
| Build + Test    | GitHub Actions                       | `.github/workflows/ci.yml`     |
| Report Upload   | Node scripts (mochawesome/jest-html) | `/pipelines/ci.yml`            |
| Governance Docs | QA Policies + Maturity Model         | `/docs/governance/`            |
| Audit Trails    | Commit History + RTM                 | `/docs/business-dev/06_RTM.md` |

---

## 7. Commit Conventions

Follow **Conventional Commits + QA extensions**:

```
feat: add community feedback analytics (FR-072)
fix: resolve dashboard filter bug (FR-024)
test: add e2e scenarios for admin request management (FR-053)
docs: migrate final_docs/Test_Plan.md to enterprise structure
ci: add Jest + Cypress reporting to CI workflow
qa: improve accessibility compliance for awareness page (FR-071)
```

**Branch format:**

```
feature/<module>     → feature/admin-dashboard
bugfix/<scope>       → bugfix/login-redirect
test/<area>          → test/e2e-profile
docs/<section>       → docs/test-strategy-update
```

---

## 8. Migration Verification Checklist

| Task | Status | Owner |
|------|--------|-------|
| Folder structure verified in VS Code | [x]| Dev Lead |
| Tests run successfully (Jest + Cypress) | [ ] | QA |
| Reports generated in `/docs/qa/06_Test_Reports/` | [ ] | QA |
| GitHub Actions runs pipeline | Pending setup | DevOps |
| Documentation updated | [ ] | Tech Writer |
| Governance policy approved | Review | PM |

---

## 9. Post-Migration Notes

* Use `/pipelines/ci.yml` to trigger all test suites per push or PR.
* Archive older reports monthly under `/docs/qa/Archive/`.
* Future upgrade: integrate Playwright and Allure for richer dashboards.

---

**Approved By:** Mpumelelo Theophilas Nxazonke - Project QA Lead 
**Date:** 2025-11-06
**Version:** 1.0