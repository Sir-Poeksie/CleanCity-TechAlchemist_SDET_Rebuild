# Environment Matrix

**Project:** CleanCity Waste Pickup Scheduler – Group 15  
**Prepared by:** Mpumelelo Theophilas Nxazonke  
**Date:** 2025-11-06  
**Version:** 1.0  

---

## 1. Overview

This matrix lists all environments, configurations, and responsibilities to support development, QA, and production deployments.

---

## 2. Environment Details

| Environment | Purpose | URL / Access | Database | Responsible | Notes |
|------------|--------|-------------|---------|------------|-------|
| Local Dev | Individual developer testing | localhost:3000 | Local Postgres/Mongo | Developer | Auto-migrate DB |
| Integration | Shared QA & feature integration | int.clean.city | Integration DB | QA Lead | Automated test runs |
| Staging | Pre-production | staging.clean.city | Staging DB | DevOps | Smoke tests, load test runs |
| Production | Live environment | clean.city | Prod DB | Project Lead | Requires QA sign-off |

---

## 3. Configuration Settings

| Setting | Dev | Integration | Staging | Production |
|---------|-----|-------------|--------|------------|
| API Base URL | localhost:5000 | int.api.clean.city | staging.api.clean.city | api.clean.city |
| Auth Token Expiry | 1h | 1h | 2h | 2h |
| Debug Mode | ON | ON | OFF | OFF |
| Logging Level | Debug | Info | Warning | Error |

---

## 4. Notes

- Environment variables managed via `.env` files per environment  
- CI/CD pipeline deploys automatically to Integration & Staging  
- Production deploys require manual approval and QA sign-off  

---

**Approved By:** DevOps / QA Lead