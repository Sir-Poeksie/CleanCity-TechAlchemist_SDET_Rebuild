# CleanCity Waste Pickup Scheduler – Requirements Traceability Matrix (RTM)

CleanCity Waste Pickup Scheduler **full Requirements Traceability Matrix (RTM)** that will link:

* **Functional Requirements (FR-001 to FR-087)**
* **User Stories (US-001 to US-035)**
* **Test Cases (TC-001 to TC-087)**
* **Module / Epic mapping**
* **Priority & Status** (ready for Jira or QA tracking)

| FR ID  | Requirement Description | Epic ID | User Story ID | Test Case ID | Module | Priority | Status  |
| ------ | -------------------------------------------- | ------- | ------------- | ------------ | -------------------- | -------- | ------- |
| FR-001 | User registration | EP-001 | US-001 | TC-001 | Authentication | High | Pending |
| FR-002 | Registration form validation | EP-001 | US-001 | TC-002 | Authentication | High | Pending |
| FR-003 | Assign default role on registration | EP-001 | US-001 | TC-003 | Authentication | High | Pending |
| FR-004 | User login & session | EP-001 | US-002 | TC-004 | Authentication | High | Pending |
| FR-005 | Display login errors | EP-001 | US-002 | TC-005 | Authentication | High | Pending |
| FR-006 | Session persistence | EP-001  | US-002 | TC-006 | Authentication | High | Pending |
| FR-007 | Redirect after login | EP-001  | US-002 | TC-007 | Authentication | High | Pending |
| FR-008 | Logout functionality | EP-001 | US-002 | TC-008 | Authentication | High | Pending |
| FR-009 | Role-based access control | EP-001 | US-004 | TC-009 | Authentication | High | Pending |
| FR-010 | Restrict unauthorized access | EP-001 | US-004 | TC-010 | Authentication | High | Pending |
| FR-011 | Password reset | EP-001  | US-003 | TC-011 | Authentication | Medium | Pending |
| FR-012 | Schedule pickup (date/type/quantity/address) | EP-002 | US-008 | TC-012 | Waste Pickup | High | Pending |
| FR-013 | Minimum 24h notice validation | EP-002 | US-008 | TC-013 | Waste Pickup | High | Pending |
| FR-014 | Real-time slot availability | EP-002 | US-008 | TC-014 | Waste Pickup | High | Pending |
| FR-015 | Prevent duplicate pickups | EP-002 | US-008 | TC-015 | Waste Pickup | High | Pending |
| FR-016 | View pickup history | EP-002 | US-009 | TC-016 | Waste Pickup | Medium | Pending |
| FR-017 | Cancel pending pickups | EP-002 | US-010 | TC-017 | Waste Pickup | High | Pending |
| FR-018 | Modify pickups in advance | EP-002 | US-010 | TC-018 | Waste Pickup | High | Pending |
| FR-019 | View past pickups | EP-002  | US-009 | TC-019 | Waste Pickup | Medium | Pending |
| FR-021 | Notify user on pickup status | EP-003 | US-013 | TC-021 | Notifications | Medium | Pending |
| FR-022 | Post-pickup feedback submission | EP-002 | US-011 | TC-022 | Waste Pickup | Medium | Pending |
| FR-023 | User dashboard stats | EP-004 | US-017 | TC-023 | Dashboard | High | Pending |
| FR-024 | Pickup summary | EP-004 | US-017 | TC-024 | Dashboard            | High | Pending |
| FR-025 | Visual metrics | EP-004  | US-017 | TC-025 | Dashboard            | High | Pending |
| FR-026 | Gamification – points | EP-004  | US-018 | TC-026 | Dashboard            | Medium   | Pending |
| FR-027 | Gamification – badges                        | EP-004  | US-018        | TC-027       | Dashboard            | Medium   | Pending |
| FR-028 | Community posts                              | EP-005  | US-021        | TC-028       | Community            | Medium   | Pending |
| FR-029 | Commenting & liking posts                    | EP-005  | US-022        | TC-029       | Community            | Medium   | Pending |
| FR-032 | Join community challenges                    | EP-005  | US-023        | TC-032       | Community            | Medium   | Pending |
| FR-033 | Admin approve/reject pickups                 | EP-006  | US-025        | TC-033       | Admin                | High     | Pending |
| FR-034 | Admin assign pickups                         | EP-006  | US-026        | TC-034       | Admin                | High     | Pending |
| FR-035 | Admin manage users                           | EP-006  | US-027        | TC-035       | Admin                | High     | Pending |
| FR-036 | Admin moderate posts                         | EP-005  | US-024        | TC-036       | Admin                | Medium   | Pending |
| FR-037 | Admin announcements                          | EP-006  | US-029        | TC-037       | Admin                | Medium   | Pending |
| FR-038 | Notification for pickup updates              | EP-003  | US-013        | TC-038       | Notifications        | Medium   | Pending |
| FR-039 | Email notifications                          | EP-003  | US-013        | TC-039       | Notifications        | Medium   | Pending |
| FR-040 | Eco-tips & infographics                      | EP-008  | US-032        | TC-040       | Awareness            | Low      | Pending |
| FR-041 | Quizzes                                      | EP-008  | US-033        | TC-041       | Awareness            | Low      | Pending |
| FR-042 | Infographics                                 | EP-008  | US-032        | TC-042       | Awareness            | Low      | Pending |
| FR-043 | Track eco-awareness                          | EP-008  | US-033        | TC-043       | Awareness            | Low      | Pending |
| FR-044 | WCAG 2.1 AA compliance                       | EP-007  | US-030        | TC-044       | Accessibility        | High     | Pending |
| FR-045 | Accessibility for visually impaired          | EP-007  | US-030        | TC-045       | Accessibility        | High     | Pending |
| FR-046 | Keyboard navigation support                  | EP-007  | US-030        | TC-046       | Accessibility        | High     | Pending |
| FR-048 | Session timeout & security                   | EP-009  | US-035        | TC-048       | Security             | Medium   | Pending |
| FR-049 | Password hashing                             | EP-009  | US-035        | TC-049       | Security             | Medium   | Pending |
| FR-050 | Mobile responsive design                     | EP-007  | US-031        | TC-050       | Performance          | High     | Pending |
| FR-051 | Tablet responsive design                     | EP-007  | US-031        | TC-051       | Performance          | High     | Pending |
| FR-052 | Desktop responsive design                    | EP-007  | US-031        | TC-052       | Performance          | High     | Pending |
| FR-053 | Data export (pickups/users)                  | EP-004  | US-020        | TC-053       | Dashboard/Admin      | Medium   | Pending |
| FR-056 | Admin audit logs                             | EP-006  | US-028        | TC-056       | Admin                | Medium   | Pending |
| FR-061 | Secure API endpoints                         | EP-001  | US-007        | TC-061       | Security             | High     | Pending |
| FR-062 | Rate limiting on APIs                        | EP-001  | US-007        | TC-062       | Security             | High     | Pending |
| FR-063 | Admin KPIs & analytics                       | EP-004  | US-019        | TC-063       | Dashboard            | Medium   | Pending |
| FR-064 | Dashboard visualizations                     | EP-004  | US-017        | TC-064       | Dashboard            | High     | Pending |
| FR-065 | Weekly summary emails                        | EP-003  | US-015        | TC-065       | Notifications        | Low      | Pending |
| FR-067 | Attach images to posts                       | EP-005  | US-021        | TC-067       | Community            | Medium   | Pending |
| FR-068 | Leaderboard display                          | EP-004  | US-018        | TC-068       | Dashboard            | Medium   | Pending |
| FR-069 | Gamification point tracking                  | EP-004  | US-018        | TC-069       | Dashboard            | Medium   | Pending |
| FR-070 | Prevent duplicate registration               | EP-001  | US-001        | TC-070       | Authentication       | High     | Pending |
| FR-071 | Feedback rating system                       | EP-002  | US-011        | TC-071       | Waste Pickup         | Medium   | Pending |
| FR-072 | Feedback comments                            | EP-002  | US-011        | TC-022       | Waste Pickup         | Medium   | Pending |
| FR-073 | Community replies notifications              | EP-003  | US-014        | TC-073       | Notifications        | Medium   | Pending |
| FR-074 | Admin action audit                           | EP-006  | US-028        | TC-074       | Admin                | Medium   | Pending |
| FR-075 | GDPR data deletion                           | EP-001  | US-006        | TC-075       | Security             | High     | Pending |
| FR-076 | GDPR user data access                        | EP-001  | US-006        | TC-076       | Security             | High     | Pending |
| FR-077 | Password reset security                      | EP-001  | US-003        | TC-011       | Authentication       | Medium   | Pending |
| FR-078 | Duplicate pickup prevention                  | EP-002  | US-012        | TC-015       | Waste Pickup         | High     | Pending |
| FR-079 | Data export security                         | EP-004  | US-020        | TC-053       | Dashboard/Admin      | Medium   | Pending |
| FR-080 | Admin post moderation                        | EP-005  | US-024        | TC-036       | Admin                | Medium   | Pending |
| FR-081 | Analytics insights                           | EP-004  | US-019        | TC-063       | Dashboard            | Medium   | Pending |
| FR-082 | Export KPI reports                           | EP-004  | US-019        | TC-063       | Dashboard            | Medium   | Pending |
| FR-084 | Role restriction enforcement                 | EP-001  | US-004        | TC-010       | Authentication       | High     | Pending |
| FR-085 | Terms & conditions acceptance                | EP-001  | US-005        | TC-085       | Authentication       | High     | Pending |
| FR-086 | Notify admin on cancellations                | EP-003  | US-016        | TC-086       | Notifications        | Medium   | Pending |
| FR-087 | Automated system backup                      | EP-009  | US-034        | TC-087       | Security/Performance | High     | Pending |