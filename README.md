# Hi, I'm Norman-Ian Böttcher 👋

**Software Architect · Java · Cloud-Native Systems**

I design backend systems that stay correct when things go wrong: late commits, partial failures, retries, systems that are down at the worst moment.
Most of my work sits where a clean domain model meets messy distributed reality.

I've spent 5+ years building and evolving Java backends in production, and I'm increasingly focused on the architecture level: making trade-offs explicit, documenting why a decision was made, and choosing the boring solution whose failure modes are understood.

---

### 🧭 What I work on

- **Software architecture**: service boundaries, domain-driven design, modular monoliths vs. microservices, architecture decision records, monolith to cloud native migrations
- **Data consistency in distributed systems**: transactional outbox, change data capture, idempotent consumers, at-least-once delivery
- **Cloud architecture**: containerized workloads, infrastructure as code, cost- and operations-aware design
- **Making systems operable**: observability, failure modes, migration paths that don't require a big bang

### 🛠️ Toolbox

| Area | Technologies |
|---|---|
| Languages | Java (17+), Typescript, Python, React, Vue |
| Frameworks | Spring Boot, Spring Data, Jakarta EE |
| Data | PostgreSQL, MariaDB, Oracle |
| Cloud & Ops | Podman, Docker, Kubernetes, Red Hat Enterprise Linux, Jenkins, GitHub Actions |
| Quality | JUnit 5, Testcontainers, assertJ |
| Observability | Prometheus & Grafana |

---

### 📌 Featured

#### [change-detection-pitfalls](https://github.com/normanboettcher/java-playground)
> *Don't believe me, run it.*

Deterministic reproductions of how change detection silently loses data, and why the cursor, not the timestamp, is the real problem.

- Polling on `updated_at` or an auto-increment ID losing late-committed rows
- A transactional outbox reintroducing the same bug through an ID cursor
- Consume-and-delete, `FOR UPDATE SKIP LOCKED` with multiple pollers, idempotent consumers
- Tests control transaction order across multiple JDBC connections: same result on every run, on PostgreSQL and MariaDB

```bash
mvn verify
```

Companion to my LinkedIn series on change detection and the transactional outbox.

---

### ✍️ Writing

I write about architecture decisions and the subtle bugs behind them, focusing on trade-offs rather than buzzwords.

- [Why I chose a transactional outbox over the "obvious" solutions]([LINK])

### 🧠 How I think about architecture

- **Decisions over diagrams.** A diagram shows *what*. An ADR explains *why*, and what was rejected.
- **Ask what a failure costs.** For every shortcut: if this goes wrong, do I lose data, or do I just get it later? "Later" is a trade-off. "Lost" is a bug.
- **Distribution is a cost, not an architecture.** I start with a modular monolith and enforced boundaries. A module becomes a service only when something forces it: independent scaling, a different release cadence, or a separate team.
---

### 🤝 Let's connect

I'm always happy to talk about software architecture, cloud design, and hard consistency problems in Java systems.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/norman-boettcher-software-engineering/)
[![Email](https://img.shields.io/badge/Email-Contact-C2410C?logo=maildotru&logoColor=white)](mailto:norman.boettcher@web.de)

<sub>Based in Hanover, Germany · Working in English and German</sub>
