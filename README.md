# 🧪 CleanCity: Waste Pickup Scheduler (Enterprise QA Build)

### A Fullstack SDET Testbed for Applied QA Engineering and DevOps Automation

---

## 🎯 Overview

**CleanCity Waste Pickup Scheduler** is an enterprise-grade QA training and testing platform that simulates an end-to-end municipal waste management system for African cities.

Originally developed as a React-based educational app, it has evolved into a **full lifecycle QA laboratory** integrating manual, automated, performance, and security testing — providing an environment for **Fullstack SDET, CI/CD, and DevOps pipeline training**.

---

## 🧩 Purpose

This platform supports **QA Engineers, Test Automation Developers, and SDETs** in mastering professional-grade testing strategies and frameworks by providing:

* Complex user flows with real-world edge cases
* Layered test architecture for TDD, BDD, and CI/CD integration
* Intentional bugs for root cause analysis and debugging practice
* Structured documentation aligned to ISO/IEC/IEEE 29119 and ISTQB standards
* Modular automation design ready for Selenium, Cypress, Jest, JMeter, and OWASP ZAP

---

## 🚀 System Features

### Functional Modules

| Module                  | Description                                                                               |
| ----------------------- | ----------------------------------------------------------------------------------------- |
| **Home / Request Page** | Waste pickup request form with client-side validation (with intentional logic gaps).      |
| **Dashboard**           | Aggregated view of pickup requests; filtering by status, city, and waste type.            |
| **Feedback Page**       | Capture missed pickups; request ID validation and form persistence.                       |
| **Awareness Page**      | Displays waste management tips and educational resources; used for accessibility testing. |
| **Admin Panel**         | Admin controls for updating pickup status and managing user feedback.                     |

---

## 🧱 Tech Stack

| Layer                  | Technology                                                    |
| ---------------------- | ------------------------------------------------------------- |
| **Frontend**           | React 18.2.0 + React Router DOM 6.3.0                         |
| **Styling**            | CSS3 / Responsive Grid                                        |
| **Data Persistence**   | LocalStorage (mock backend, extensible to Node.js or FastAPI) |
| **Testing Frameworks** | Jest, Cypress, Selenium, JMeter, OWASP ZAP                    |
| **CI/CD Integration**  | GitHub Actions + Netlify Deployment + Static QA Reports       |
| **Documentation**      | Markdown, ADRs, and QA Compliance Framework under `/docs/`    |

---

## ⚙️ Installation & Setup

### Prerequisites

* Node.js (v14+)
* npm or yarn
* Modern browser (Chrome, Edge, or Firefox)

### Local Setup

```bash
git clone <repository-url>
cd cleancity-waste-scheduler
npm install
npm start
```

Access the app at: [http://localhost:3000](http://localhost:3000)

### Build for Production

```bash
npm run build
```

The build will be generated in the `/build` directory.

---

## 🌐 Deployment

### Option 1: Netlify (Recommended)

1. Run `npm run build`
2. Log into [Netlify](https://www.netlify.com/)
3. Drag and drop the `/build` folder
4. Deployed automatically with live URL

### Option 2: GitHub + CI/CD

* Push your branch
* Connect your repository to Netlify or GitHub Pages
* Set build command: `npm run build`
* Publish directory: `build/`

---

## 🧪 Testing and QA Framework

The project integrates a **layered testing strategy** combining:

* **Manual Testing:** Exploratory, functional, accessibility
* **Automated Testing:** Jest (unit/integration), Cypress (E2E), Selenium (cross-browser)
* **Performance Testing:** JMeter
* **Security Testing:** OWASP ZAP and threat modeling
* **Continuous QA:** Test metrics tracked through GitHub Actions and CI reports

All [QA assets](./docs/qa/) are structured under:

```
/docs/qa/
  ├── 01_Test_Policy.md
  ├── 02_Test_Strategy.md
  ├── 03_Test_Plan.md
  ├── 04_Test_Cases_and_Scenarios.md
  ├── 05_Automation_Framework_Design.md
  ├── 06_Test_Reports/
  ├── 07_Performance_Testing.md
  ├── 08_Security_Compliance.md
  ├── 09_Accessibility_Compliance.md
  └── 10_QA_Charter_and_Code_of_Ethics.md
```

---

## 🧩 Core Test Scenarios

### Functional

1. **Form Validation** – Required fields, invalid inputs
2. **Filtering Logic** – By city, date, or waste type
3. **Data Persistence** – localStorage data integrity
4. **Admin Controls** – Status updates and CRUD operations
5. **UI Responsiveness** – Cross-device layout testing

### Non-Functional

* **Accessibility (WCAG 2.1 AA)**: alt-text, tab order, ARIA roles
* **Performance (JMeter)**: Load up to 500 simulated users
* **Security (OWASP)**: Input sanitization, XSS, CSRF testing

---

## 📦 QA Reporting Pipeline

| Report Type                 | Description                                       |
| --------------------------- | ------------------------------------------------- |
| **Defect Log (V2.0)**       | Updated bug registry linked to GitHub Issues      |
| **Summary Report (V2.0)**   | Execution outcomes by environment and test phase  |
| **Metrics & Audit (V2.0)**  | QA maturity and coverage tracking                 |
| **Comprehensive QA Report** | Final QA deliverable aligned to release readiness |

---

## 🧭 Governance and Compliance

The repository follows **enterprise QA governance principles** defined under `/docs/governance/`:

* **CI/CD Documentation**
* **QA Governance Policy**
* **Continuous Improvement Report**
* **Quality Assurance Maturity Model**
* **Release Notes**
* **Project Charter**
* **Code of Ethics**

---

## 📊 SDET Learning Focus

This repo is an integrated part of the **Fullstack SDET & DevOps Roadmap**, providing hands-on practice in:

* Test Design & Coverage Analysis
* Framework Architecture (TDD/BDD)
* CI/CD Pipeline QA Integration
* Performance and Security Auditing
* Enterprise Documentation Lifecycle

---

## 📚 Resources

| Area            | Tool / Standard         |
| --------------- | ----------------------- |
| Test Frameworks | Jest, Cypress, Selenium |
| API Testing     | Postman, Newman         |
| Performance     | JMeter                  |
| Security        | OWASP ZAP               |
| Accessibility   | Axe-core, Lighthouse    |
| Documentation   | Markdown, ADRs          |
| CI/CD           | GitHub Actions, Netlify |

---

## 🧾 License

This repository is for **educational and professional SDET portfolio purposes**, under academic licensing with attribution to the PLP QA Academy and enterprise rebuild extensions by Theophilas (2025).

---

## 💬 Support & Contributions

* Open issues under `docs/qa/06_Test_Reports/Bugs_to_Raise_V2.0.md`
* Refer to `docs/governance/CONTRIBUTING.md` for PR guidelines
* For documentation alignment, follow the structure in `repo_structure.md`

---

## 🧩 Versioning

| Version | Date | Description |
|---------|------|-------------|
| **V1.0 (2024)** | PLP QA Training Base Build | [View Original README](PLP_Readme.md) |
| **V1.5 (2025)** | CleanCity QA Extension |             |
| **V2.0 (2025–2026)** | Enterprise Rebuild — Fullstack SDET Cycle |             |