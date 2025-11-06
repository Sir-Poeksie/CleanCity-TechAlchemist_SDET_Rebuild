# CleanCity Waste Pickup Scheduler – Test Cases & Scenarios

**Document:** `docs\qa\04_Test_Cases_and_Scenarios.md`
**Purpose:** Define detailed test cases and scenarios for functional (FR), non-functional (NFR), and system requirements.
**Scope:** All modules including Authentication, Waste Pickup, Dashboard, Notifications, Community, Admin, Accessibility, Security, Performance, Awareness, and Compliance.
**Prepared by:** Mpumelelo Theophilas Nxazonke, QA Lead / SDET
**Date:** 05 November 2025
**Version:** 1.0

---

## Table of Contents

- [CleanCity Waste Pickup Scheduler – Test Cases \& Scenarios](#cleancity-waste-pickup-scheduler--test-cases--scenarios)
  - [Table of Contents](#table-of-contents)
  - [Authentication Module](#authentication-module)
  - [Waste Pickup Module](#waste-pickup-module)
  - [Dashboard Module](#dashboard-module)
  - [Notifications Module](#notifications-module)
  - [Admin Module](#admin-module)
  - [Accessibility Module](#accessibility-module)
  - [Security Module](#security-module)
  - [Performance Module](#performance-module)
  - [Awareness Module](#awareness-module)

---

## Authentication Module

| TC ID  | FR ID  | User Story | Scenario / Steps                                                | Expected Result                              | Priority | Test Type  |
| ------ | ------ | ---------- | --------------------------------------------------------------- | -------------------------------------------- | -------- | ---------- |
| TC-001 | FR-001 | US-001     | Navigate to registration page → Enter valid data → Submit form  | User account is created successfully         | High     | Functional |
| TC-002 | FR-002 | US-001     | Submit incomplete or invalid registration form                  | Appropriate validation error messages appear | High     | Functional |
| TC-003 | FR-003 | US-001     | Complete registration                                           | Default role assigned to new user            | High     | Functional |
| TC-004 | FR-004 | US-002     | Enter valid login credentials → Submit                          | User is redirected to dashboard              | High     | Functional |
| TC-005 | FR-005 | US-002     | Enter invalid login credentials → Submit                        | Error message displayed                      | High     | Functional |
| TC-006 | FR-006 | US-002     | Login → Close and reopen browser                                | Session persists if still valid              | High     | Functional |
| TC-008 | FR-008 | US-002     | Click logout                                                    | User session terminated, redirected to login | High     | Functional |
| TC-009 | FR-009 | US-004     | Access restricted page with insufficient role                   | Access denied                                | High     | Functional |
| TC-011 | FR-011 | US-003     | Request password reset → Follow email link → Enter new password | Password updated successfully                | Medium   | Functional |
| TC-070 | FR-070 | US-001     | Attempt duplicate registration                                  | System blocks duplicate account creation     | High     | Functional |
| TC-085 | FR-085 | US-005     | Attempt login without accepting T&C                             | System prevents login                        | High     | Functional |

---

## Waste Pickup Module

| TC ID  | FR ID  | User Story | Scenario / Steps                                    | Expected Result                     | Priority | Test Type  |
| ------ | ------ | ---------- | --------------------------------------------------- | ----------------------------------- | -------- | ---------- |
| TC-012 | FR-012 | US-008     | Schedule pickup → Select date/type/quantity/address | Pickup scheduled successfully       | High     | Functional |
| TC-013 | FR-013 | US-008     | Schedule pickup with <24h notice                    | System displays validation error    | High     | Functional |
| TC-014 | FR-014 | US-008     | Check pickup slot availability                      | Real-time availability displayed    | High     | Functional |
| TC-015 | FR-015 | US-008/012 | Attempt duplicate pickup                            | System prevents duplicates          | High     | Functional |
| TC-016 | FR-016 | US-009     | View pickup history                                 | Past pickups displayed correctly    | Medium   | Functional |
| TC-017 | FR-017 | US-010     | Cancel pending pickup                               | Pickup marked cancelled             | High     | Functional |
| TC-018 | FR-018 | US-010     | Modify scheduled pickup in advance                  | Changes saved successfully          | High     | Functional |
| TC-019 | FR-019 | US-009     | View past pickups                                   | Historical pickups correctly listed | Medium   | Functional |
| TC-022 | FR-022 | US-011     | Submit post-pickup feedback                         | Feedback stored and acknowledged    | Medium   | Functional |
| TC-071 | FR-071 | US-011     | Rate pickup service                                 | Rating recorded                     | Medium   | Functional |
| TC-072 | FR-072 | US-011     | Add comments to feedback                            | Comments saved                      | Medium   | Functional |

---

## Dashboard Module

| TC ID  | FR ID  | User Story | Scenario / Steps               | Expected Result                    | Priority | Test Type  |
| ------ | ------ | ---------- | ------------------------------ | ---------------------------------- | -------- | ---------- |
| TC-023 | FR-023 | US-017     | Login → Navigate to dashboard  | User stats displayed               | High     | Functional |
| TC-024 | FR-024 | US-017     | View pickup summary            | Correct summary displayed          | High     | Functional |
| TC-025 | FR-025 | US-017     | View visual metrics            | Graphs/charts display correct data | High     | Functional |
| TC-026 | FR-026 | US-018     | Earn points through pickups    | Points incremented correctly       | Medium   | Functional |
| TC-027 | FR-027 | US-018     | Earn badges                    | Badges awarded per criteria        | Medium   | Functional |
| TC-064 | FR-064 | US-017     | Check dashboard visualizations | Data visualizations accurate       | High     | Functional |
| TC-068 | FR-068 | US-018     | Leaderboard display            | Top users correctly ranked         | Medium   | Functional |
| TC-069 | FR-069 | US-018     | Gamification point tracking    | Points updated accurately          | Medium   | Functional |

---

## Notifications Module

| TC ID  | FR ID  | User Story | Scenario / Steps               | Expected Result                  | Priority | Test Type  |
| ------ | ------ | ---------- | ------------------------------ | -------------------------------- | -------- | ---------- |
| TC-021 | FR-021 | US-013     | Notify user on pickup status   | Notification received            | Medium   | Functional |
| TC-038 | FR-038 | US-013     | Pickup status update           | Notification triggered correctly | Medium   | Functional |
| TC-039 | FR-039 | US-013     | Email notifications            | Email sent                       | Medium   | Functional |
| TC-065 | FR-065 | US-015     | Weekly summary email           | Correct summary sent             | Low      | Functional |
| TC-073 | FR-073 | US-014     | Community replies notification | Notifications received           | Medium   | Functional |
| TC-086 | FR-086 | US-016     | Admin notified on cancellation | Admin receives correct alert     | Medium   | Functional |

---

## Admin Module

| TC ID  | FR ID  | User Story | Scenario / Steps       | Expected Result                | Priority | Test Type  |
| ------ | ------ | ---------- | ---------------------- | ------------------------------ | -------- | ---------- |
| TC-033 | FR-033 | US-025     | Approve/reject pickups | Pickup status updated          | High     | Functional |
| TC-034 | FR-034 | US-026     | Assign pickups         | Assignment recorded            | High     | Functional |
| TC-035 | FR-035 | US-027     | Manage users           | User management functions work | High     | Functional |
| TC-036 | FR-036 | US-024     | Moderate posts         | Posts correctly moderated      | Medium   | Functional |
| TC-037 | FR-037 | US-029     | Admin announcements    | Announcement visible           | Medium   | Functional |
| TC-056 | FR-056 | US-028     | Audit logs             | Logs recorded correctly        | Medium   | Functional |
| TC-074 | FR-074 | US-028     | Admin action audit     | Correct audit entries          | Medium   | Functional |
| TC-080 | FR-080 | US-024     | Admin post moderation  | Posts moderated per rules      | Medium   | Functional |

---

## Accessibility Module

| TC ID  | FR ID  | User Story | Scenario / Steps           | Expected Result               | Priority | Test Type      |
| ------ | ------ | ---------- | -------------------------- | ----------------------------- | -------- | -------------- |
| TC-044 | FR-044 | US-030     | Navigate using keyboard    | WCAG 2.1 AA compliance met    | High     | Non-functional |
| TC-045 | FR-045 | US-030     | Test screen reader support | Visual impairments supported  | High     | Non-functional |
| TC-046 | FR-046 | US-030     | Check keyboard navigation  | Full accessibility compliance | High     | Non-functional |

---

## Security Module

| TC ID  | FR ID  | User Story | Scenario / Steps                          | Expected Result               | Priority | Test Type |
| ------ | ------ | ---------- | ----------------------------------------- | ----------------------------- | -------- | --------- |
| TC-048 | FR-048 | US-035     | Wait for session timeout → Attempt action | User logged out               | Medium   | Security  |
| TC-049 | FR-049 | US-035     | Check password hashing                    | Password stored securely      | Medium   | Security  |
| TC-061 | FR-061 | US-007     | Secure API endpoints                      | Unauthorized requests blocked | High     | Security  |
| TC-062 | FR-062 | US-007     | Rate limiting                             | API enforces limits           | High     | Security  |
| TC-075 | FR-075 | US-006     | GDPR data deletion                        | User data removed on request  | High     | Security  |
| TC-076 | FR-076 | US-006     | GDPR data access                          | User can access personal data | High     | Security  |

---

## Performance Module

| TC ID  | FR ID  | User Story | Scenario / Steps        | Expected Result               | Priority | Test Type      |
| ------ | ------ | ---------- | ----------------------- | ----------------------------- | -------- | -------------- |
| TC-050 | FR-050 | US-031     | Test on mobile device   | UI renders correctly          | High     | Non-functional |
| TC-051 | FR-051 | US-031     | Test on tablet          | UI renders correctly          | High     | Non-functional |
| TC-052 | FR-052 | US-031     | Test on desktop         | UI renders correctly          | High     | Non-functional |
| TC-087 | FR-087 | US-034     | Automated system backup | Backup completes successfully | High     | Non-functional |

---

## Awareness Module

| TC ID  | FR ID  | User Story | Scenario / Steps    | Expected Result                  | Priority | Test Type      |
| ------ | ------ | ---------- | ------------------- | -------------------------------- | -------- | -------------- |
| TC-040 | FR-040 | US-032     | View eco-tips       | Tips displayed                   | Low      | Non-functional |
| TC-041 | FR-041 | US-033     | Take quizzes        | Scores recorded                  | Low      | Non-functional |
| TC-042 | FR-042 | US-032     | View infographics   | Infographics displayed correctly | Low      | Non-functional |
| TC-043 | FR-043 | US-033     | Track eco-awareness | Tracking updated                 | Low      | Non-functional |