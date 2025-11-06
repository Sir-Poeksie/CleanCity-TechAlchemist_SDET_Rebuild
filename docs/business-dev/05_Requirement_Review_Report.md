# Requirements Review Report

**Project:** CleanCity Waste Pickup Scheduler – Group 15  
**Prepared by:** Mpumelelo Theophilas Nxazonke  
**Date:** 2025-11-06  
**Version:** 1.0  

---

## 1. Purpose

This document summarizes the review of functional and non-functional requirements to ensure:

- Completeness of requirements
- Testability for QA and automation
- Alignment with business objectives

---

## 2. Reviewed Documents

| Document | Version | Review Date | Reviewer | Notes |
|----------|--------|------------|---------|-------|
| 02_BRD.md | 1.0 | 2025-11-04 | QA Lead | Business objectives defined; minor clarifications needed |
| 03_PRD.md | 1.0 | 2025-11-04 | Product Owner | Functional flows confirmed; APIs listed |
| 04_SRS_FRS.md | 1.0 | 2025-11-05 | Fullstack SDET | FRs mapped to testable scenarios |

---

## 3. Review Findings

| Requirement ID | Description | Issue / Gap | Action / Resolution |
|----------------|------------|------------|------------------|
| FR-001 | User authentication | Password complexity not explicit | Add rule to SRS |
| FR-014 | Schedule Pickup | No API response format defined | Update API contract |
| FR-032 | Dashboard filters | Ambiguous sorting behavior | Confirm sorting rules with PO |

---

## 4. Conclusion

- All critical requirements are **reviewed and approved** for design and testing.  
- Minor gaps have been documented and will be addressed in the next PRD/SRS update.  
- Requirements are now **ready for traceability in RTM**.

---

**Approved By:** Product Owner / QA Lead  
**Next Review Date:** 2025-12-06
