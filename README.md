# Chinnakrit (Jay)
### Full-Stack Systems & Workflow Developer

I independently design, build, and operate production-grade workflow platforms that coordinate multi-role business operations. Currently maintaining custom ERP systems in manufacturing environments and institutional academic platforms deployed at Prince of Songkla University.

---

### 🏛️ Production Systems in Active Use

#### 1. [Boonraksa-ERP System](https://github.com/Jayxxx1/BoonraksaV2) — Custom ERP & Manufacturing Workflow
* **Role**: Sole Developer (from schema design to VPS deployment)
* **Scope**: 17 user roles (Sales, Stock, Graphic, QA, Embroidery, Sewing, Finance, Delivery) coordinating a 21-state apparel manufacturing pipeline.
* **Technical Highlights**:
  - **Pure-Function RBAC**: Flat-mapped permissions (`getOrderActionMap`) evaluated instantly on React render loops and Express middleware. Includes shadow assignee overrides.
  - **Status Rank Guard**: Statuses mapped to numeric ranks (1-16) to prevent unauthorized status reversion, logging suspicious status actions.
  - **Atomic Transactions**: Multi-order grouping operations executed atomically via Prisma transactions.
  - **SLA Deadline Math**: Stage-aware deadline tracking adjusting dynamically based on queue volume.

#### 2. [PSU TPSF EILA](https://github.com/Jayxxx1/TPSF_EILA) — University Academic Assessment Platform
* **Role**: Sole Developer
* **Scope**: Deployed at Prince of Songkla University, digitizing multi-role committee assessment workflows.
* **Technical Highlights**:
  - **Secure Dual-Transport Auth**: HttpOnly cookies prioritised over authorization headers, triggers security logs (IP + User-Agent) on token anomaly detection.
  - **Binary Stream PDF Scanner**: Scans uploaded PDFs for dangerous binary markers (`/JavaScript`, `/OpenAction`, `/Launch`, etc.) before storage rather than relying on extension checks.
  - **Row-Level Write Locks**: Implemented direct `pg-client` transaction blocks with explicit row-level state guards (`UPDATE ... WHERE status = 'SUBMITTED'`) to prevent concurrency race conditions.

#### 3. [Journal Workflow System](https://github.com/Jayxxx1/journal) — Thaijo Academic Article Publication & Peer Review Workflow (In Active Development)
* **Role**: Sole Developer
* **Scope**: Digitizes and tracks the complete peer review and publishing workflow for academic journals in cooperation with Thaijo.
* **Core Engineering & Logic**:
  - **Dynamic Reviewer Eligibility Validation**: Restricts reviewer selection based on institutional/affiliation bounds (reviewers cannot share the same campus/affiliation as authors). Automatically treats mixed-institution authorship as external to enforce policy guidelines.
  - **Emailed Action Token Triggers**: Implemented one-click action triggers directly in reviewer invitation emails (Accept/Decline) that route actions back to the database state-machine without requiring immediate platform authentication.
  - **Deferred Submission Billing**: Payment verification moved downstream (after initial editorial review and reviewer assignment) to optimize workflow queues and prevent costly refund loops for immediately rejected submissions.
  - **PDF Annotation Integration**: Peer review feedback is directly annotated onto article PDFs within the review pipeline.

---

### 🛠️ Technical Focus & Competencies

| Layer | Technologies & Frameworks |
| :--- | :--- |
| **Languages** | TypeScript, JavaScript (ES6+), PHP, Python, SQL, C#, HTML5, CSS3 |
| **Backend & Databases** | Node.js, Express, PostgreSQL, Prisma ORM, pg-client, Socket.IO, REST APIs |
| **Frontend Development** | React 18/19, Vite, TailwindCSS, React Router, Recharts, Web Push |
| **Infrastructure & DevOps** | Docker, Docker Compose, Nginx, PM2, GitLab CI/CD, AWS S3, Git |
| **AI & Agentic Workflows** | LLM Agents, Prompt Engineering, CLI Automation, Vibe Coding (Highly Proficient), Claude, Codex, NotebookLM |

---

### 📈 Profile Overview

* 📍 Based in Songkhla, Thailand
* 🎓 Information Technology (IT) Student, Prince of Songkla University (Graduating Academic Year 2568)
* ✉️ cnknz.working@gmail.com
* 💻 [Portfolio Website](https://jayxxx1.github.io/Port/)

---
*“Systems before screens. Focus on domain logic, transactional state consistency, and policy-driven safety.”*
