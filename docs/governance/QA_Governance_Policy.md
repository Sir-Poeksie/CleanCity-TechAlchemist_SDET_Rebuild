# CleanCity Waste Pickup Scheduler – QA Governance Policy

**Project:** CleanCity Waste Scheduler – Group 15  
**Version:** 1.0  
**Effective Date:** 2025-11-06  
**Owner:** QA Governance Board  
**Prepared by:** Mpumelelo Theophilas Nxazonke  

---

## 1. Purpose

This document defines the **Quality Assurance Governance Framework** for the CleanCity project.  
It establishes policies, practices, and approval workflows to maintain test coverage, documentation integrity, and quality consistency throughout the software lifecycle.

---

## 2. Scope

This policy applies to all contributors—developers, QA engineers, automation testers, and maintainers—working within the CleanCity Group 15 repository.  
It governs:

- Testing standards (unit, integration, E2E)  
- Commit and branch structure  
- Documentation updates and reviews  
- CI/CD testing pipelines and approval gates  

---

## 3. Quality Governance Objectives  

| Objective | Description |
|------------|--------------|
| **Transparency** | Ensure all QA work (tests, reports, issues) is traceable to specific requirements (FR-IDs). |
| **Accountability** | Define ownership for QA deliverables, review, and release. |
| **Consistency** | Maintain a unified structure and process across the project. |
| **Compliance** | Ensure QA meets academic and enterprise audit standards (TDD, BDD, RTM). |

---

## 4. QA Governance Principles

- **Traceability:** RTM maintained for all requirements.  
- **Accountability:** Defects tracked via GitHub Issues and QA reports.  
- **Transparency:** Test progress, coverage, and metrics documented in QA reports.  
- **Compliance:** Ensure WCAG, OWASP, GDPR, and TDD/BDD adherence.  
- **Continuous Improvement:** Lessons learned captured in quarterly reviews.

---

## 5. QA Documentation Standards  

All QA deliverables must reside under `/docs/qa/` and follow this structure:

| Category | Folder | Example |
|-----------|---------|---------|
| Test Policy & Strategy | `/docs/qa/01_Test_Policy.md`, `/docs/qa/02_Test_Strategy.md` | Defines QA approach |
| Test Plans & Cases | `/docs/qa/03_Test_Plan.md`, `/docs/qa/04_Test_Cases_and_Scenarios.md` | Scenario design |
| Reports | `/docs/qa/06_Test_Reports/` | Jest/Cypress reports, metrics |
| Compliance | `/docs/qa/07_Performance_Testing.md`, `/docs/qa/08_Security_Compliance.md` | Quality gates |
| Governance | `/docs/governance/QA_Governance_Policy.md` | This document |

Each document must include:

- Version control header  
- Date of last review  
- Approver signature or initials  

---

## 6. Review & Approval Workflow  

| Stage | Description | Reviewer |
|--------|-------------|----------|
| **Development Commit** | Code pushed to feature branch | Developer |
| **Pull Request (PR)** | Code + Tests reviewed | QA Reviewer |
| **Pipeline Verification** | All CI/CD jobs pass (Unit + E2E) | Automation System |
| **QA Sign-Off** | Test results verified and documented | QA Lead |
| **Merge Approval** | Final merge to `main` | Project Lead |

---

## 7. Continuous Integration & Quality Gates  

Each PR triggers the GitHub Actions pipeline (`.github/workflows/ci.yml`) to:

- Run **Jest** (unit/integration)  
- Run **Cypress** (E2E)  
- Generate reports to `/docs/qa/06_Test_Reports/`  
- Fail the pipeline if coverage < **80%**

Results must be uploaded or linked in the PR comment before merge.

---

## 8. Git Commit & Branch Governance Policy  

### 8.1 Conventional Commit Format  

All commits must follow:

```
<type>(<scope>): <message>
```

**Types:**

- `feat:` — New feature  
- `fix:` — Bug fix  
- `test:` — Test-related changes  
- `docs:` — Documentation updates  
- `refactor:` — Code refactor (no feature change)  
- `ci:` — Pipeline or workflow updates  
- `qa:` — Quality or audit improvement  
- `chore:` — Maintenance or tooling  

**Example:**  
```
test(e2e): add login.feature and step definitions for FR-004–FR-007`
```

### 8.2 Branch Naming Convention  

| Purpose | Format | Example |
|----------|---------|----------|
| New feature | `feature/<module>` | `feature/dashboard-filter` |
| Bug fix | `bugfix/<area>` | `bugfix/login-auth` |
| Test enhancement | `test/<scope>` | `test/e2e-pickup-request` |
| Docs update | `docs/<section>` | `docs/test-plan-revision` |
| Hotfix | `hotfix/<id>` | `hotfix/FR-041-crash` |

### 8.3 Commit Verification Checklist  

Each pull request must:

- Reference at least one **Functional Requirement ID (FR-###)**  
- Pass **CI/CD pipeline tests** (unit + E2E)  
- Include report evidence in `/docs/qa/06_Test_Reports/`  
- Be reviewed by a QA and Developer reviewer  

---

## 9. Roles & Responsibilities  

| Role | Responsibility |
|------|----------------|
| **QA Lead** | Approves final QA deliverables and sign-off |
| **Fullstack SDET / Automation Engineer** | Implements automated/manual test suites, maintains CI/CD scripts |
| **Developer** | Writes unit tests and ensures test coverage |
| **Tech Writer** | Updates documentation per release |
| **Project Lead** | Final approver for merges into `main` |
| **Product Owner / BA** | Provides requirements and acceptance criteria |

---

## 10. Metrics & Continuous Improvement  

- Minimum coverage target: **80%**  
- Each sprint includes QA retrospection in `Continuous_Improvement_Report.md`  
- Metrics captured: defects by severity, test coverage, pass rate, accessibility score  

---

## 11. Review Cycle  

- QA Governance Policy is reviewed **quarterly** or after each major release.  
- Updates require approval from the **QA Governance Board**.  

---

**Approved By:** QA Governance Board  
**Effective Date:** 2025-11-06  
**Version:** 1.0