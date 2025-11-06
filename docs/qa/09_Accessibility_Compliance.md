# CleanCity Waste Pickup Scheduler – Accessibility Compliance

**Purpose:** Define accessibility standards, testing, and compliance measures to ensure the CleanCity Waste Pickup Scheduler platform is usable by all users, including those with disabilities.

**Scope:** Web portal, mobile web views, dashboards, forms, notifications, and community features.

**Prepared by:** Mpumelelo Theophilas Nxazonke
**Date:** 2025-11-06
**Version:** 1.0

---

## 1. Objectives

1. Ensure compliance with **WCAG 2.1 AA** accessibility standards.
2. Enable equal access for users with visual, auditory, motor, or cognitive impairments.
3. Validate that all UI components, forms, and interactions are perceivable, operable, understandable, and robust.
4. Integrate accessibility testing into development, QA, and CI/CD pipelines.

---

## 2. Accessibility Guidelines

| Principle      | Guideline                    | Description                                                                                |
| -------------- | ---------------------------- | ------------------------------------------------------------------------------------------ |
| Perceivable    | Text Alternatives            | Provide alt text for images, icons, and non-text content.                                  |
| Perceivable    | Color Contrast               | Ensure minimum 4.5:1 contrast for text and 3:1 for large text.                             |
| Perceivable    | Multimedia                   | Provide captions for audio/video content and transcripts where needed.                     |
| Operable       | Keyboard Navigation          | Ensure all interactive elements are navigable via keyboard (Tab, Shift+Tab, Enter, Space). |
| Operable       | Focus Indicators             | Visible focus outlines for all actionable items.                                           |
| Understandable | Consistent Layout            | Use consistent navigation, labels, and instructions across pages.                          |
| Robust         | ARIA Compliance              | Use semantic HTML and ARIA attributes to support screen readers.                           |
| Robust         | Assistive Technology Testing | Verify platform compatibility with screen readers and voice-over tools.                    |

---

## 3. Accessibility Testing Approach

| Test Type            | Tools                                                      | Scope                                                            |
| -------------------- | ---------------------------------------------------------- | ---------------------------------------------------------------- |
| Automated Checks     | axe DevTools, Lighthouse CI                                | Detect color contrast issues, missing alt text, ARIA violations. |
| Manual Testing       | Screen readers (NVDA, VoiceOver), Keyboard-only navigation | Validate UI accessibility for real user scenarios.               |
| Form Validation      | Manual & Automated                                         | Ensure error messages, labels, and instructions are accessible.  |
| Mobile Accessibility | Chrome DevTools, VoiceOver/iOS, TalkBack/Android           | Test responsiveness and accessibility on mobile devices.         |
| Focus & Tab Order    | Manual & Cypress E2E                                       | Verify logical tab order and focus management across pages.      |

---

## 4. Reporting & Compliance

* **Accessibility Test Reports:** Document automated and manual findings with severity, screenshots, and remediation steps.
* **Audit Logs:** Record accessibility test execution for QA traceability.
* **Compliance Dashboard:** Track WCAG 2.1 AA coverage for each page/component.
* **Continuous Review:** Accessibility checks integrated in CI/CD (Cypress + axe-core), reviewed quarterly or after major UI changes.

---

## 5. Integration with QA & Development

* All **functional UI development** must comply with accessibility guidelines.
* Accessibility defects logged in **GitHub Issues** and linked to corresponding test cases in the RTM.
* Regression and E2E automation tests include accessibility validations (e.g., axe-core in Cypress).