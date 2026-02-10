# Smart Procurement & Vendor Management System (SPVMS)

This repository contains the full codebase (Frontend & Backend) for the SPVMS portal, developed as part of the Infosys Springboard Virtual Internship.

---

## ⚖️ MIT License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## 📋 Agile Documentation

We followed an **Agile Methodology** to develop the system iteratively. The project was divided into 7 key Sprints to ensure a robust and scalable architecture.

### 👤 User Stories
- **As a Procurement Officer (e.g., aman_proc):** I want to create Purchase Requests (PR) and view only my own records to ensure data privacy and accountability. [cite: 2026-02-09]
- **As an Admin:** I want to manage system configurations, review vendor compliance, and approve/reject procurement requests.
- **As a Vendor:** I want to upload quotation documents and track my compliance status.

### 🚀 Sprint Breakdown

#### Sprint 1: Framework Design & Data Modeling
- **Focus:** Infrastructure setup and core entity modeling.
- **Tasks:** - Set up JDK, Spring Boot with Maven, and MySQL database.
  - Developed JPA/Hibernate Entity Models: `User`, `Role`, `Vendor`, `Item`, `PR`, and `PO`.
  - Established relationships (One-to-Many, Many-to-One) and ID generation strategies.

#### Sprint 2: Security & Role-Based Access Control (RBAC)
- **Focus:** Securing endpoints and managing permissions.
- **Tasks:**
  - Implemented Spring Security with a custom `SecurityConfig` filter chain.
  - Defined access rules for `Admin`, `Finance`, `Procurement`, and `Vendor`.
  - Implemented Logout functionality and tested unauthorized access scenarios.

#### Sprint 3: Document Management & Compliance
- **Focus:** Handling digital assets and vendor verification.
- **Tasks:**
  - Built APIs for Vendor Document upload (PDF/Images) and storage.
  - Integrated compliance verification flags and status history tracking.
  - Developed a document download API for procurement review.

#### Sprint 4: Purchase Request (PR) Workflow
- **Focus:** Core procurement request logic.
- **Tasks:**
  - Implemented PR Line Item management (Add/Update/Delete).
  - Built logic for linking PRs with specific Vendor Quotes.
  - Automated estimated cost calculation and price/quantity validation. [cite: 2026-01-06]

#### Sprint 5: Logistics & Delivery Support
- **Focus:** Post-order fulfillment tracking.
- **Tasks:**
  - Added support for recording delivery dates and partial deliveries.
  - Implemented remarks for damaged/returned items.
  - Created a Delivery Confirmation API to update PO status accordingly.

#### Sprint 6: Analytics & Reporting
- **Focus:** Data-driven insights via SQL.
- **Tasks:**
  - Developed complex SQL queries for Monthly Spending and Vendor Performance.
  - Implemented PR approval timeline and Order Fulfillment rate reports.
  - Optimized heavy reports using Stored Procedures.

#### Sprint 7: Performance Tuning & Optimization
- **Focus:** System benchmarking and speed.
- **Tasks:**
  - Analyzed slow queries and added missing database indexes.
  - Optimized Hibernate queries and tuned the HikariCP connection pool.
  - Benchmarked read/write performance for high-traffic scenarios.

---

## 📂 Project Structure
```text
SPVMS-Final-Submission/
├── backend/           # Spring Boot Application (JPA, Security, REST APIs)
├── frontend/          # React.js Application (Dashboards, UI Components)
├── README.md          # Agile Documentation
└── LICENSE            # MIT License File