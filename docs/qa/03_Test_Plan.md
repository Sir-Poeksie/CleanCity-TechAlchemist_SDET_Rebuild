# CleanCity Waste Pickup Scheduler – QA Test Plan

## 1. Introduction

This document defines the **detailed QA Test Plan** for the CleanCity Waste Pickup Scheduler project. It is based on the Test Policy and Strategy and provides **test scope, objectives, approach, resources, schedule, and deliverables**.

## 2. Scope

**In Scope:**  

- Authentication & Authorization  
- Waste Pickup Scheduling & Management  
- Notifications & Community Module  
- Admin Console & Analytics Dashboard  
- Accessibility, Performance, and Security  

**Out of Scope:**  
- Third-party system integration not yet approved  
- Non-critical visual styling  

## 3. Objectives

- Validate functional requirements (FR-001 to FR-087)  
- Ensure regression-free builds  
- Validate performance, accessibility, and security  

## 4. Approach

| Activity | Description | Tools |
|----------|------------|-------|
| TDD Unit Testing | Test-first development; developers write unit tests before code | Jest |
| Unit Testing | Test individual functions/components | Jest |
| BDD Acceptance Testing | Scenarios written in collaboration with PO/BA in Gherkin syntax | Cypress + Cucumber |
| Integration Testing | Test module interactions | Jest, Cypress |
| System Testing | End-to-end validation | Cypress, Selenium |
| Regression Testing | Validate stable builds | Cypress, GitHub Actions |
| Performance Testing | Load & stress test | JMeter |
| Security Testing | Validate auth, roles, OWASP | Manual & scripts |
| Accessibility Testing | WCAG 2.1 AA compliance | Manual + tools |

## 5. Test Schedule

| Phase | Start Date | End Date | Duration |
|-------|------------|---------|----------|
| Test Preparation | 2025-11-05 | 2025-11-12 | 1 week |
| BDD Scenario Definition | YYYY-MM-DD | YYYY-MM-DD | Continuous per sprint |
| TDD Test Creation | YYYY-MM-DD | YYYY-MM-DD | Continuous per sprint |
| Unit & Integration Testing | YYYY-MM-DD | YYYY-MM-DD | 2 weeks |
| System Testing | YYYY-MM-DD | YYYY-MM-DD | 2 weeks |
| Regression & Automation | YYYY-MM-DD | YYYY-MM-DD | Continuous |
| UAT / Acceptance | YYYY-MM-DD | YYYY-MM-DD | 1 week |
| Test Closure | YYYY-MM-DD | YYYY-MM-DD | 2 days |

## 6. Entry & Exit Criteria

**Entry Criteria:**

- Stable code deployed to test environment  
- RTM and Test Cases approved  
- Test environments ready  

**Exit Criteria:**  

- All critical defects resolved  
- ≥90% test case execution complete  
- Test reports reviewed and signed off  

## 7. Resource Planning

| Role | Resource | Responsibility |
|------|---------|----------------|
| Fullstack SDET | 1 | Automated & manual testing |
| QA Lead | 1 | Review & oversee testing |
| Developer | Multiple | Fix defects |
| Product Owner | 1 | Requirement validation & UAT |

## 8. Test Deliverables

- Test Cases & Test Scripts  
- Test Execution Report  
- Defect Log / GitHub Issues  
- RTM & Traceability Dashboard  
- Test Summary Report  

## 9. Risks & Mitigation

| Risk | Impact | Mitigation |
|------|--------|------------|
| Late code delivery | High | Daily CI/CD builds & smoke tests |
| Unstable environment | High | Use Docker & snapshots |
| Missing requirements | Medium | Continuous review with PO/BA |
| Complex workflows | Medium | Automated regression pack & exploratory testing |

## 10. Tools & Automation

- Jest, Cypress, Selenium, Postman, JMeter, GitHub Actions, RTM dashboards  

## 11. Approval

| Role | Name | Signature | Date |
|------|------|----------|------|
| QA Lead | TBD |          |      |
| Product Owner | TBD |          |      |
| Project Manager | TBD |          |      |