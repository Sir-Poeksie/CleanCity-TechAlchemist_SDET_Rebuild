# CleanCity Waste Pickup Scheduler – Jira-Ready Backlog

## Epics & User Stories

---

### **Epic 1: User Authentication & Security**

**Epic ID:** EP-001
**Description:** All features related to user account management, authentication, roles, and security compliance.

| Story ID | User Story | Module | Priority | Linked FRs |
| -------- | ---------- | ------ | -------- | ---------- |
| US-001   | As a user, I want to register an account so that I can use the platform | Authentication | High | FR-001, FR-002, FR-003, FR-070 |
| US-002   | As a user, I want to log in and maintain session so that I can access my data securely | Authentication | High     | FR-004, FR-005, FR-006, FR-007, FR-008 |
| US-003   | As a user, I want to reset my password securely | Authentication | Medium   | FR-011, FR-077 |
| US-004   | As an admin, I want to manage roles and restrict access so that unauthorized users cannot access sensitive modules | Authentication | High | FR-009, FR-010, FR-084 |
| US-005   | As a user, I want to accept terms & conditions and privacy policy | Authentication | High | FR-085 |
| US-006   | As a system, I want GDPR-compliant data storage and allow users to delete accounts | Security | High | FR-075, FR-076 |
| US-007   | As a system, I want secure API endpoints and rate-limiting | Security | High | FR-061, FR-062 |

**Sub-tasks for US-001:**

* ST-001: Implement registration form validation (FR-002)
* ST-002: Assign default role on registration (FR-003)
* ST-003: Prevent duplicate registration (FR-070)

**Sub-tasks for US-002:**

* ST-004: Implement login & session management (FR-004, FR-006)
* ST-005: Display login errors (FR-005)
* ST-006: Redirect after login (FR-007)
* ST-007: Logout functionality (FR-008)

---

### **Epic 2: Waste Pickup Management**

**Epic ID:** EP-002
**Description:** Users can schedule, modify, cancel, and track waste pickups.

| Story ID | User Story                                                                   | Module       | Priority | Linked FRs                     |
| -------- | ---------------------------------------------------------------------------- | ------------ | -------- | ------------------------------ |
| US-008   | As a user, I want to schedule pickups with date, type, quantity, and address | Waste Pickup | High     | FR-012, FR-013, FR-014, FR-015 |
| US-009   | As a user, I want to view pickup history                                     | Waste Pickup | Medium   | FR-016, FR-019                 |
| US-010   | As a user, I want to cancel or modify pickups in advance                     | Waste Pickup | High     | FR-017, FR-018                 |
| US-011   | As a user, I want post-pickup feedback submission                            | Waste Pickup | Medium   | FR-022, FR-071, FR-072         |
| US-012   | As a system, I want to prevent duplicate pickups and validate 24h notice     | Waste Pickup | High     | FR-013, FR-015, FR-078         |

**Sub-tasks for US-008:**

* ST-008: Form creation & validation
* ST-009: Real-time slot availability (FR-014)
* ST-010: Minimum 24h validation (FR-013)
* ST-011: Duplicate pickup check (FR-015)

**Sub-tasks for US-010:**

* ST-012: Cancel pending pickup (FR-017)
* ST-013: Modify pickups >24h in advance (FR-018)

---

### **Epic 3: Notifications**

**Epic ID:** EP-003
**Description:** Notify users/admins about pickups, updates, and community activity.

| Story ID | User Story                                                | Module        | Priority | Linked FRs             |
| -------- | --------------------------------------------------------- | ------------- | -------- | ---------------------- |
| US-013   | As a user, I want notifications for pickup status changes | Notifications | Medium   | FR-021, FR-038, FR-039 |
| US-014   | As a user, I want notifications for community replies     | Notifications | Medium   | FR-073                 |
| US-015   | As a system, I want to send weekly summary emails         | Notifications | Low      | FR-065                 |
| US-016   | As an admin, I want notifications for cancelled pickups   | Notifications | Medium   | FR-086                 |

---

### **Epic 4: Dashboard & Gamification**

**Epic ID:** EP-004
**Description:** Personalized dashboards for users and admins, gamification, metrics, and analytics.

| Story ID | User Story                                                        | Module          | Priority | Linked FRs                     |
| -------- | ----------------------------------------------------------------- | --------------- | -------- | ------------------------------ |
| US-017   | As a user, I want a personalized dashboard with stats and pickups | Dashboard       | High     | FR-023, FR-024, FR-025, FR-064 |
| US-018   | As a user, I want gamification: points, badges, leaderboards      | Dashboard       | Medium   | FR-026, FR-027, FR-068, FR-069 |
| US-019   | As an admin, I want KPIs and analytics dashboard                  | Dashboard       | Medium   | FR-063, FR-081, FR-082         |
| US-020   | As a system, I want data export for pickups & users               | Dashboard/Admin | Medium   | FR-053, FR-079                 |

---

### **Epic 5: Community Features**

**Epic ID:** EP-005
**Description:** Users interact, post, comment, and participate in community challenges.

| Story ID | User Story                                              | Module    | Priority | Linked FRs             |
| -------- | ------------------------------------------------------- | --------- | -------- | ---------------------- |
| US-021   | As a user, I want to create posts and attach images     | Community | Medium   | FR-028, FR-067, FR-066 |
| US-022   | As a user, I want to comment, like, and reply on posts  | Community | Medium   | FR-029, FR-073         |
| US-023   | As a user, I want to join challenges and track progress | Community | Medium   | FR-032, FR-043         |
| US-024   | As an admin, I want to moderate posts                   | Admin     | Medium   | FR-036, FR-080         |

---

### **Epic 6: Admin Management**

**Epic ID:** EP-006
**Description:** Admin functions including user management, pickup assignment, and system logs.

| Story ID | User Story                                                       | Module | Priority | Linked FRs     |
| -------- | ---------------------------------------------------------------- | ------ | -------- | -------------- |
| US-025   | As an admin, I want to approve/reject pickups                    | Admin  | High     | FR-033         |
| US-026   | As an admin, I want to assign pickups by date/type/area          | Admin  | High     | FR-034         |
| US-027   | As an admin, I want to manage users (roles, suspend/delete)      | Admin  | High     | FR-035         |
| US-028   | As an admin, I want audit logs of actions                        | Admin  | Medium   | FR-056, FR-074 |
| US-029   | As an admin, I want to post announcements and push notifications | Admin  | Medium   | FR-037         |

---

### **Epic 7: Accessibility & Performance**

**Epic ID:** EP-007
**Description:** Ensure accessibility, device responsiveness, and system performance.

| Story ID | User Story                                          | Module        | Priority | Linked FRs             |
| -------- | --------------------------------------------------- | ------------- | -------- | ---------------------- |
| US-030   | As a user, I want WCAG 2.1 AA compliance            | Accessibility | High     | FR-044, FR-045, FR-046 |
| US-031   | As a user, I want mobile-friendly responsive design | Performance   | High     | FR-051, FR-050, FR-052 |

---

### **Epic 8: Awareness & Learning**

**Epic ID:** EP-008
**Description:** Educational features including eco-tips, quizzes, and infographics.

| Story ID | User Story                                       | Module    | Priority | Linked FRs     |
| -------- | ------------------------------------------------ | --------- | -------- | -------------- |
| US-032   | As a user, I want eco-tips and infographics      | Awareness | Low      | FR-040, FR-042 |
| US-033   | As a user, I want quizzes to track eco-awareness | Awareness | Low      | FR-041, FR-043 |

---

### **Epic 9: System Backup & Security**

**Epic ID:** EP-009
**Description:** Ensure system integrity, backups, and disaster recovery.

| Story ID | User Story                                                | Module               | Priority | Linked FRs     |
| -------- | --------------------------------------------------------- | -------------------- | -------- | -------------- |
| US-034   | As a system, I want automated backup & restore            | Security/Performance | High     | FR-087         |
| US-035   | As a system, I want password hashing & session management | Security             | Medium   | FR-049, FR-048 |
