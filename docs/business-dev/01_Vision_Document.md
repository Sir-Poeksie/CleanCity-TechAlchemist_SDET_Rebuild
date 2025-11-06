# CleanCity Waste Pickup Scheduler – Vision Document

**Document Version:** 1.0
**Date:** 06-Nov-2025
**Prepared By:** Development & QA Team
**Project Name:** CleanCity – Waste Pickup Scheduler
**Intended Audience:** Stakeholders, QA Team, Developers, Product Owner, Security Officer

## 1. Version History

| Version | Date | Description | Author |
|---------|------|-------------|--------|
| 1.0 | 06-Nov-25 | Initial Draft | Dev & QA Team  |
| 1.1 | TBD | Updated metrics, scope, and risks | QA Lead |

---

## 2. Vision Statement

CleanCity is a **community-driven waste management platform** designed to make scheduling waste pickups **simple, engaging, and environmentally impactful**. The platform empowers residents to **track waste collection**, encourages sustainable behavior through **gamification and educational content**, and provides administrators with **tools for efficient operational management and reporting**.

---

## 3. Business Objectives

| Objective | Description | Traceability |
|-----------|------------|--------------|
| Simplify Waste Scheduling | Enable residents to request and track waste pickups easily | FR-012 → FR-019 |
| Community Engagement | Encourage sustainable behavior via gamification, tips, quizzes, and challenges | FR-029 → FR-052 |
| Data-Driven Insights | Provide dashboards and analytics for environmental impact tracking | FR-023 → FR-027 |
| Operational Efficiency | Support admin workflow for scheduling, approvals, user/content management | FR-053 → FR-064 |
| Accessibility & Usability | Ensure inclusive design compliant with WCAG 2.1 AA | FR-071 → FR-074 |

---

## 4. Scope

### 4.1 In-Scope

- Resident registration, login, profile management
- Waste pickup scheduling and tracking
- Admin dashboard for requests, users, and content moderation
- Community engagement features (posts, comments, challenges)
- Notifications, badges, and gamification
- Responsive design (desktop, tablet, mobile)
- Accessibility features (screen readers, keyboard navigation)

### 4.2 Out-of-Scope

- Integration with external city IoT devices or municipal ERP systems
- Payment or billing systems
- Third-party logistics or waste management APIs
- Predictive analytics beyond MVP dashboards

---

## 5. Key Stakeholders

| Stakeholder | Role / Responsibility |
|------------|----------------------|
| Residents | Primary users; schedule pickups and engage with gamification features |
| Administrators | Manage requests, content moderation, reporting, and operational oversight |
| Community Members | Share posts, tips, and participate in challenges |
| QA Team | Validate system functionality, security, usability, and accessibility |
| Product Owner / Sponsors | Strategic oversight, approve features, ensure project aligns with objectives |
| Security Officer | Ensure compliance with data protection policies |

---

## 6. Success Metrics (SMART)

| Metric | Target | Measurement |
|--------|--------|------------|
| User Adoption | 80% of community residents registered within 3 months | Registration analytics |
| Pickup Efficiency | 95% of scheduled pickups fulfilled on time | System logs and admin reports |
| Community Engagement | ≥50% of users participate in gamification features monthly | Platform activity tracking |
| System Reliability | <1% downtime per month | Monitoring dashboard & uptime logs |
| Accessibility Compliance | 100% WCAG 2.1 AA adherence | Accessibility audits and testing reports |

---

## 7. Risk Assessment

| Risk | Likelihood | Impact | Mitigation |
|------|------------|--------|------------|
| Low user adoption | Medium | High | Marketing campaigns, onboarding tutorials |
| Delayed pickups | Medium | High | Admin scheduling alerts, real-time notifications |
| Data loss in localStorage | Low | High | Implement backup, browser storage validation |
| Security vulnerabilities | Low | Critical | Input validation, XSS/CSRF prevention, QA security testing |
| Non-compliance with accessibility | Low | Medium | Accessibility testing with NVDA/JAWS and WCAG audits |

---

## 8. Assumptions

- Users have internet-enabled devices with modern browsers
- Residents are willing to engage in gamified features
- Admins are trained to manage content and approve requests
- MVP does not require third-party system integrations

---

## 9. Dependencies

- Browser localStorage for persistence
- Modern React.js SPA for frontend
- Responsive design framework (CSS Grid / Flexbox)
- QA tools for functional, accessibility, and performance testing (Jest, Selenium, Cypress, axe DevTools)

---

## 10. Optional Visuals

> **High-Level Workflow Diagram Example**  
> Resident schedules pickup → System validates → Admin approves/assigns → Pickup completed → Feedback & gamification points awarded  

---

## 11. Notes

- This vision document will guide **FRS, BRD, PRD**, and QA test planning.  
- All **success metrics are linked to functional requirements**, enabling traceability for testing.  
- Risk mitigation and scope boundaries ensure **realistic MVP delivery and testing focus**.  

---

**Prepared by:** Mpumelelo Theophilas Nxazonke  
**Date:** 06-Nov-2025  
**Document Version:** 1.0
