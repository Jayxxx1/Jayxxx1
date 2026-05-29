# Chinnakrit (Jay)
### Full-Stack Systems & Workflow Engineer

I independently design, build, and operate production-grade workflow platforms that coordinate multi-role business operations. Currently maintaining custom ERP systems in manufacturing environments and institutional academic platforms deployed at Prince of Songkla University.

---

### 🏛️ Production Systems in Active Use

#### 1. [Boonraksa-ERP System](https://github.com/Jayxxx1/BoonraksaV2) — Custom ERP & Manufacturing Workflow
* **Role**: Sole Developer (from schema design to VPS deployment)
* **Scope**: 17 user roles (Sales, Stock, Graphic, QA, Embroidery, Sewing, Finance, Delivery) coordinating a 21-state apparel manufacturing pipeline.
* **Core Engineering**:
  - **Pure-Function RBAC**: Flat-mapped permissions (`getOrderActionMap`) evaluated instantly on React render loops and Express middleware. Includes shadow assignee overrides.
  - **Status Rank Guard**: Statuses mapped to numeric ranks (1-16) to prevent unauthorized status reversion, logging suspicious status actions.
  - **Atomic Transactions**: Multi-order grouping operations executed atomically via Prisma transactions.
  - **SLA Deadline Math**: Stage-aware deadline tracking adjusting dynamically based on queue volume.

#### 2. [PSU TPSF EILA](https://github.com/Jayxxx1/TPSF_EILA) — University Academic Assessment Platform
* **Role**: Sole Developer
* **Scope**: Deployed at Prince of Songkla University, digitizing multi-role committee assessment workflows.
* **Core Engineering**:
  - **Secure Dual-Transport Auth**: HttpOnly cookies prioritised over authorization headers, triggers security logs (IP + User-Agent) on token anomaly detection.
  - **Binary Stream PDF Scanner**: Scans uploaded PDFs for dangerous binary markers (`/JavaScript`, `/OpenAction`, `/Launch`, etc.) before storage rather than relying on extension checks.
  - **Row-Level Write Locks**: Implemented direct `pg-client` transaction blocks with explicit row-level state guards (`UPDATE ... WHERE status = 'SUBMITTED'`) to prevent concurrency race conditions.

#### 3. [Journal](https://github.com/Jayxxx1/journal) — Personal Developer Journaling & Sync System (In Progress)
* **Role**: Sole Developer
* **Focus**: Designing a highly secure, markdown-centric developer log system featuring local-first syncing and cryptographic privacy.
* **Core Engineering**:
  - **Local-First Sync**: Offline-first design with local storage and auto-syncing to remote database when connection is restored.
  - **Cryptographic Privacy**: Encrypting sensitive entry contents client-side before synchronization.
  - **Tag-Driven Analytics**: Automatic extraction of tags and metrics to build developer productivity charts.

---

### 🛠️ Technical Focus & Competencies

| Layer | Technologies & Frameworks |
| :--- | :--- |
| **Languages** | TypeScript, JavaScript (ES6+), SQL, C#, Python, HTML5, CSS3 |
| **Backend & Databases** | Node.js, Express, PostgreSQL, Prisma ORM, pg-client, Socket.IO, REST APIs |
| **Frontend Engineering** | React 18/19, Vite, TailwindCSS, React Router, Recharts, Web Push |
| **Infrastructure & DevOps** | Docker, Docker Compose, Nginx, PM2, GitLab CI/CD, AWS S3, Git |

---

### 📈 Profile Overview

* 📍 Based in Songkhla, Thailand
* 🎓 Computer Engineering Student, Prince of Songkla University (Expected 2026)
* ✉️ jay.chinnakrit@gmail.com
* 💻 [Portfolio Website](https://jayxxx1.github.io/Port/)

---
*“Systems before screens. Focus on domain logic, transactional state consistency, and policy-driven safety.”*
