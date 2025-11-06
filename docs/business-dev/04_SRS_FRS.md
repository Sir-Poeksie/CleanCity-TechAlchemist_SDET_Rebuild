# CleanCity Waste Pickup Scheduler – Functional & Software Requirements Specification (SRS/FRS)

## Document Control

**Version:** 1.0
**Date:** 06 November 2025
**Prepared By:** Mpumelelo Theophilas Nxazonke, QA Lead
**Project:** CleanCity – Waste Pickup Scheduler
**Intended Audience:** QA Teams, Developers, Project Managers, Stakeholders, Students

---

## 1. Introduction

### 1.1 Purpose

The purpose of this document is to define all functional and non-functional requirements for the **CleanCity web application**, a React-based waste management platform for communities. The platform enables residents to request, track, and manage waste pickups, while providing educational content, gamification, and analytics features. This document is the foundation for QA testing, development, and project planning.

### 1.2 Scope

CleanCity provides the following core functionality:

* **User Registration & Authentication**
* **Waste Pickup Scheduling**
* **Real-time Request Tracking & Notifications**
* **Community Engagement & Educational Content**
* **Gamification & Analytics Dashboards**
* **Admin Controls & Moderation**
* **Responsive, Accessible, and Secure Web Experience**

### 1.3 Target Users

* **Residents:** Schedule pickups, track requests, access educational content
* **Community Members:** Participate in discussions, challenges, and eco-awareness activities
* **Admins:** Manage users, requests, content, and analytics

### 1.4 Definitions

* **FR:** Functional Requirement
* **NFR:** Non-Functional Requirement
* **User:** Registered resident
* **Admin:** Platform manager with elevated permissions

---

## 2. System Overview

### 2.1 Application Architecture

* **Frontend:** React.js SPA
* **State Management:** React state and localStorage
* **Authentication:** Role-based (User/Admin)
* **Deployment:** Static hosting (Netlify/Vercel/GitHub Pages)
* **Modules:** Authentication, Waste Management, Dashboard, Community Features, Admin Panel, Notifications

### 2.2 Core Modules

1. **Authentication System** (FR-001 to FR-011)
2. **Waste Pickup Scheduling & Tracking** (FR-012 to FR-022)
3. **Dashboard & Analytics** (FR-023 to FR-030)
4. **Community Features & Content Management** (FR-036 to FR-052)
5. **Administrative Functions** (FR-053 to FR-064)
6. **Notifications System** (FR-065 to FR-068)
7. **Awareness & Education Features** (FR-036 to FR-040)

---

## 3. Functional Requirements

### 3.1 Authentication (FR-001 to FR-011)

* **FR-001:** Register with email, password, full name, phone (optional)
* **FR-002:** Validate input and show errors
* **FR-003:** Assign default role “User”
* **FR-004:** Login with email/password
* **FR-005:** Display errors on invalid credentials
* **FR-006:** Maintain session in localStorage
* **FR-007:** Redirect user to intended page after login
* **FR-008:** Logout function
* **FR-009:** Clear session on logout
* **FR-010:** Support “User” and “Admin” roles
* **FR-011:** Restrict admin access to admin users only

### 3.2 Waste Pickup Scheduling & Tracking (FR-012 to FR-022)

* **FR-012:** Schedule pickup with date, waste type, quantity, instructions, and address
* **FR-013:** Validate minimum 24-hour notice
* **FR-014:** Display available pickup slots
* **FR-015:** Prevent duplicate pickups for the same date
* **FR-016:** View history of pickups
* **FR-017:** Cancel pending pickups
* **FR-018:** Modify pickups >24 hours before scheduled time
* **FR-019:** Display status: Pending, Confirmed, Completed, Cancelled
* **FR-020:** Real-time updates for pickups
* **FR-021:** Send notifications for status changes
* **FR-022:** Allow post-pickup feedback submission

### 3.3 Dashboard & Analytics (FR-023 to FR-030)

* Personalized dashboards with metrics, stats, and achievements
* Environmental impact calculations (waste diverted, CO2 saved, trees saved)
* Charts for trends (daily, monthly, yearly)
* Community leaderboards
* Badges & point system for gamification

### 3.4 Community Features (FR-041 to FR-052)

* User-generated posts, comments, likes
* Chronological feeds and activity tracking
* Profile management & environmental stats
* Follow other users & join community challenges

### 3.5 Admin Panel (FR-053 to FR-064)

* Approve, reject, modify requests
* Assign pickup slots, filter/search requests
* Manage users: roles, suspend/delete accounts
* Moderate community posts and comments
* Announcements and content flagging

### 3.6 Notifications (FR-065 to FR-068)

* Bell icon with unread count
* Notifications for pickups, posts, and achievements
* Read/unread management and history

### 3.7 Awareness & Education (FR-036 to FR-040)

* Eco-tips carousel, interactive quizzes
* Infographics, statistics, and actionable buttons
* Track quiz scores and provide feedback

---

## 4. Non-Functional Requirements

### 4.1 Performance

* Page load <3s
* UI response <1s
* Handle large datasets in localStorage

### 4.2 Browser & Device Compatibility

* Chrome, Firefox, Safari, Edge (latest 2 versions)
* Mobile responsive (320px+)
* WCAG 2.1 AA compliance

### 4.3 Security

* XSS & injection test payloads included for QA
* Client-side password hashing
* No sensitive data in localStorage

### 4.4 Accessibility

* Keyboard navigation
* Alt text and ARIA labels
* Color contrast compliant

---

## 5. Data Storage & Models

### 5.1 localStorage Keys

```
cleanCity_users
cleanCity_currentUser
cleanCity_pickupRequests
cleanCity_pickupHistory
cleanCity_blogPosts
cleanCity_communityPosts
cleanCity_comments
cleanCity_adminUsers
cleanCity_systemSettings
cleanCity_analytics
cleanCity_leaderboard
cleanCity_notifications
```

### 5.2 Core Objects

#### User

```json
{
  "id": "uuid",
  "username": "email",
  "password": "hashed",
  "role": "user|admin",
  "profile": { "avatar": "", "bio": "" },
  "stats": { "totalPickups": 0, "points": 0, "badges": [] }
}
```

#### Pickup Request

```json
{
  "id": "uuid",
  "userId": "uuid",
  "wasteType": "General|Recyclable|Organic|Hazardous",
  "quantity": "Small|Medium|Large",
  "scheduledDate": "YYYY-MM-DD",
  "status": "Pending|Confirmed|Completed|Cancelled",
  "notes": ""
}
```

#### Blog Post

```json
{
  "id": "uuid",
  "title": "",
  "content": "",
  "author": "uuid",
  "publishDate": "YYYY-MM-DD",
  "status": "Draft|Published|Archived",
  "tags": []
}
```

---

## 6. Testing Considerations

* **Form validation** (boundary & edge cases)
* **localStorage integrity**
* **Cross-browser & mobile responsiveness**
* **Performance & load testing**
* **Accessibility testing (WCAG 2.1 AA)**
* **Security testing (XSS, injection)**

---

## 7. Test Data & Scenarios

* Predefined user accounts (regular and admin)
* Sample pickup requests (pending, confirmed, completed)
* Sample blog & community posts
* Edge cases: long inputs, special characters, Unicode
* Large dataset for performance/load tests
* Cross-browser/device scenarios

---

## 8. Business Rules

* Max 3 pickups per week
* Hazardous waste requires admin approval
* Email must be unique; passwords meet security rules
* Inactive accounts archived after 6 months
* Community content moderated; posts older than 1 year archived

---

## 9. Deployment & Technical Notes

* Build: `npm run build`
* Static hosting (Netlify/Vercel/GitHub Pages)
* HTTPS required; optional custom domain
* Environment variables via `.env.local`
* Client-side only; backend not implemented for demo purposes

---

## 10. References

* [README](./README.md)
* [Submission Guidelines](./submission.md)
* [Video Guide](./video-guide.md)
* [Technical Specs](./technical-specs.md)
* [Test Data](./test-data.md)
* [Jira Setup](./jira-setup.md)

---

This **SRS/FRS document** consolidates all functional, non-functional, technical, and testing requirements for CleanCity, providing a comprehensive reference for developers, QA engineers, and stakeholders.
