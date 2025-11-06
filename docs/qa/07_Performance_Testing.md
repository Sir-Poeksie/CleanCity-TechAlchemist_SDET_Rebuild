# CleanCity Waste Pickup Scheduler – Performance Testing

**Purpose:** Define the performance, load, stress, spike, and endurance testing approach for the CleanCity Waste Pickup Scheduler platform.

**Scope:** Web Portal, API endpoints, and database performance under expected, peak, and extreme load conditions.

**Prepared by:** Mpumelelo Theophilas Nxazonke
**Date:** 2025-11-05
**Version:** 1.1

---

## 1. Objectives

1. Validate system responsiveness, stability, and scalability under normal and peak load.
2. Identify and isolate bottlenecks in web, API, and database layers.
3. Ensure system can handle expected concurrent users without performance degradation.
4. Provide actionable recommendations for optimization and capacity planning.

---

## 2. Key Performance Metrics

| Metric               | Description                                                 | Target / Threshold               |
| -------------------- | ----------------------------------------------------------- | -------------------------------- |
| Response Time        | Time taken to serve a request or render a page/API response | < 2s for 95% of requests         |
| Throughput           | Number of requests processed per second                     | ≥ 500 req/sec under peak         |
| Concurrent Users     | Max simultaneous active users supported                     | ≥ 1000 users                     |
| Error Rate           | Percentage of failed requests                               | < 1%                             |
| Resource Utilization | CPU, Memory, Network, Database usage                        | CPU < 75%, Memory < 80%          |
| Latency              | Time delay for API calls across network layers              | < 250ms                          |
| Scalability          | System growth under increased load                          | Linear or sub-linear degradation |

---

## 3. Types of Performance Testing

| Test Type                 | Purpose                                    | Tool                 |
| ------------------------- | ------------------------------------------ | -------------------- |
| Load Test                 | Validate behavior under expected load      | JMeter               |
| Stress Test               | Identify breaking point under extreme load | JMeter               |
| Endurance / Soak Test     | Assess stability over prolonged operation  | JMeter               |
| Spike Test                | Measure system response to sudden bursts   | JMeter               |
| Database Performance Test | Evaluate query efficiency and indexing     | JMeter / DB Profiler |
| API Performance Test      | Validate endpoint response under load      | Postman / JMeter     |

---

## 4. Test Scenarios

| Scenario                   | Description                                       | Users / Load    | Expected Outcome                                    |
| -------------------------- | ------------------------------------------------- | --------------- | --------------------------------------------------- |
| User Login                 | Simultaneous login attempts                       | 500 concurrent  | Response ≤ 2s, no errors                            |
| Schedule Pickup            | High-frequency scheduling requests                | 1000 concurrent | Successful request processing, no duplicates        |
| Dashboard Rendering        | Multiple dashboards accessed concurrently         | 2000 concurrent | All widgets render correctly, response ≤ 3s         |
| API Endpoints              | `/api/pickups`, `/api/users`, `/api/feedback`     | 1000 req/sec    | No failed requests, CPU < 75%, DB < 80% utilization |
| Community Posts & Feedback | High volume of post creation / comment submission | 500 concurrent  | Posts created without errors, low latency           |
| Data Export                | CSV/JSON export under concurrent requests         | 100 concurrent  | Export completes under 5s per request               |
| Security Load              | API requests with authentication & authorization  | 500 concurrent  | Auth handled correctly, no breaches                 |

---

## 5. Test Environment

* **Hardware:** QA Servers simulating production-class CPU, Memory, Network
* **Software:** Staging environment mirroring production versions
* **Tools:** JMeter, Postman/Newman, DB Profiler, CPU/Memory monitoring
* **Network Simulation:** Latency and bandwidth throttling to replicate user conditions

---

## 6. Execution Plan

1. Baseline test: Establish normal system performance.
2. Load test: Incrementally increase users to expected capacity.
3. Stress test: Push beyond capacity to identify failure points.
4. Endurance test: Run high-load tests over 12–24 hours to detect memory leaks.
5. Spike test: Introduce sudden bursts to assess recovery and system stability.
6. Database profiling: Monitor query times and index usage during load.
7. API testing: Validate response times and error rates under concurrent requests.

---

## 7. Reporting & Metrics Collection

* **Graphs & Charts:** Response time distribution, throughput, error rate, resource utilization
* **Logs & Alerts:** Detailed JMeter / Postman logs, screenshots for errors
* **Analysis:** Identify bottlenecks by module, API, or DB query
* **Recommendations:** Scaling, caching, query optimization, and performance tuning