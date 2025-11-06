# CleanCity Contributor Guidelines

**Project:** CleanCity Waste Scheduler – Sir Poeksie  
**Effective Date:** 2025-11-06  
**Version:** 1.0  

---

## 1. Purpose

This document guides all contributors on the **branching strategy, commit standards, and QA/documentation workflow** for CleanCity Group 15. Following these rules ensures consistency, traceability, and audit-ready history across the project.

---

## 2. Branching Strategy

All work must occur in dedicated branches following this CCR-based convention:

| Purpose | Branch Prefix | Example |
|---------|---------------|---------|
| Documentation / QA | `docs/CCR-###-topic` | `docs/CCR-000-governance-update` |
| New Feature | `feature/CCR-###-feature` | `feature/CCR-100-dashboard-filter` |
| Bug Fix | `bugfix/CCR-###-area` | `bugfix/CCR-200-login-auth` |
| Test Enhancement | `qa/CCR-###-scope` | `qa/CCR-300-e2e-profile` |
| Hotfix | `hotfix/CCR-###-issue` | `hotfix/CCR-999-critical-fix` |

**Notes:**
- CCR = CleanCity Rebuild identifier.
- Each branch must be scoped to a single logical change or feature.
- Always start new work from `main` or the relevant parent branch.

---

## 3. Commit Message Standards

All commits must use the **Conventional Commit + CCR format**:

```
<type>(<scope>): <message> (CCR-###)
```

**Commit Types:**
- `feat:` — New feature  
- `fix:` — Bug fix  
- `docs:` — Documentation changes  
- `test:` — Test addition or update  
- `refactor:` — Code change, no feature/bug impact  
- `ci:` — Pipeline/workflow updates  
- `qa:` — QA or audit improvement  
- `chore:` — Maintenance/tooling  

**Example:**
```
docs(governance): add QA Governance Policy and update repo structure (CCR-002)
```

**Tip:** Use the `.gitmessage` template in the repo root for automatic formatting.

---

## 4. QA & Documentation Workflow

1. **Documentation Updates**
   - All QA and documentation files live under `/docs/`.
   - Use incremental commits for each logical change for traceability (preferred).
   - Examples of directories:
     - `docs/governance/`
     - `docs/qa/`
     - `docs/business-dev/`

2. **Migration & Rebuild Phases**
   - Separate branches should handle:
     - Documentation & QA updates (`docs/CCR-000-*`)
     - Feature implementation or rebuild (`feature/CCR-100-*`)

3. **Test Reports**
   - Generated test outputs go into `/docs/qa/06_Test_Reports/`.
   - CI/CD pipelines should verify coverage ≥ 80% before merge.

---

## 5. Pull Request Requirements

Each PR must:

- Reference at least one **Functional Requirement ID (FR-###)**.
- Pass **CI/CD pipeline**: unit tests (Jest) + E2E (Cypress).
- Include evidence of reports in `/docs/qa/06_Test_Reports/`.
- Be reviewed by a **QA Reviewer**, **Developer**, and **Project Lead**.

---

## 6. Additional Notes

- Always pull latest `main` before starting a new branch.
- Keep commits atomic and descriptive.
- Tag major documentation or QA milestones using semantic tags:

```
git tag -a v2.0-docs -m "Documentation restructure completed (CCR-001–003)"
```

---

**References:**

- [QA Governance Policy](QA_Governance_Policy.md)
- [.gitmessage commit template](../.gitmessage)