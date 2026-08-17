<h1 align="center">Hi 👋, I'm Akhilesh Chitare</h1>

<h3 align="center">
Java Backend Developer | Spring Boot · Microservices · Spring Security · Docker | IEEE Published
</h3>

<p align="center">
Backend developer building secure, scalable systems using Java 17 and Spring Boot.
6 months of internship experience. 3 deployed projects. 1 IEEE publication.
</p>

---

## 👨‍💻 About Me

- 🎓 B.Tech, Computer Science & Engineering — G.H. Raisoni College of Engineering and Management, Nagpur (2026, CGPA 8.31)
- 💼 Java Developer Intern at **AB Infotech Solutions Pvt. Ltd.** (Dec 2025 – Jun 2026) — built production CRM backend APIs
- 🚀 Built **HireForge AI** — evolved from Spring Boot monolith to a **6-service microservices system** with Spring Cloud Gateway, Netflix Eureka, Docker, and GitHub Actions CI/CD
- 🔐 Hands-on with Spring Security, JWT, Hibernate/JPA, REST APIs, Spring Data JPA, BCrypt, Bean Validation
- 📡 Microservices: Spring Cloud Gateway · Netflix Eureka · Service Discovery · API Gateway · Load Balancing
- 📰 Co-author, **IEEE CNC-2025** publication — YOLOv8-based soybean leaf disease detection with severity grading
- 🎯 Goal: Build production-ready, scalable backend systems

---

## 🚀 Tech Stack

### Backend
<p align="left">
<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/java/java-original.svg" width="45" title="Java"/>
<img src="https://www.vectorlogo.zone/logos/springio/springio-icon.svg" width="45" title="Spring Boot"/>
<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original-wordmark.svg" width="45" title="MySQL"/>
<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/docker/docker-original-wordmark.svg" width="45" title="Docker"/>
<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/git/git-original.svg" width="45" title="Git"/>
<img src="https://www.vectorlogo.zone/logos/getpostman/getpostman-icon.svg" width="45" title="Postman"/>
</p>

**Core:** Java 17 · Spring Boot · Spring Framework · Spring MVC · Spring Web · Spring Security · Spring Data JPA · Hibernate (ORM) · REST APIs · JWT Authentication · BCrypt · Bean Validation · Lombok

**Microservices:** Spring Cloud Gateway · Netflix Eureka · Service Discovery · API Gateway · Load Balancing · Spring RestClient

**Database:** MySQL · SQLite · RDBMS · SQL · Database Design · JPA Repositories

**DevOps:** Docker · Docker Compose · Maven · Git · GitHub · GitHub Actions · CI/CD

**Engineering:** OOP · Object-Oriented Design · Design Patterns · SOLID Principles · Clean Code · DSA · SDLC · Problem Solving

**Tools:** IntelliJ IDEA · Postman · Swagger/OpenAPI · Apache PDFBox · Apache POI

---

## 📌 Projects

### 🚀 HireForge AI — AI-Powered Resume Analyzer & Job Toolkit

> Evolved from a Spring Boot monolith to a **6-service microservices architecture**

**Repos:**
- Monolith: [github.com/Akhilesh9911/hireforge-ai](https://github.com/Akhilesh9911/hireforge-ai)
- Microservices: [github.com/Akhilesh9911/hireforge-ai-microservices](https://github.com/Akhilesh9911/hireforge-ai-microservices)

**Architecture:**

| Service | Responsibility |
|---|---|
| API Gateway | JWT validation, routing, X-User-Id header injection |
| Eureka Server | Service discovery and registry |
| Auth Service | Registration, login, JWT issuance |
| Resume Service | PDF/DOCX parsing, Gemini API integration |
| Interview Service | AI-generated interview questions |
| Job Tracker Service | CRUD job application tracking |

**Key Engineering:**
- JWT validation centralized at API Gateway — downstream services fully decoupled from auth via `X-User-Id` header injection
- Custom `OncePerRequestFilter` with HMAC-SHA signing and BCrypt password encoding
- Multi-format resume parsing pipeline — PDF (Apache PDFBox) + DOCX (Apache POI) → Google Gemini API (gemini-2.5-flash) for ATS scoring and skills gap analysis
- Containerized all 6 services with multi-stage Dockerfiles (eclipse-temurin:17-jdk-alpine) and Docker Compose with MySQL health checks
- GitHub Actions CI/CD matrix pipeline building and verifying all 6 services in parallel

**Tech:** Java 17 · Spring Boot · Spring Security · JWT · Spring Data JPA · Hibernate · MySQL · Spring Cloud Gateway · Netflix Eureka · Spring RestClient · Apache PDFBox · Apache POI · Google Gemini API · Docker · Docker Compose · GitHub Actions · Maven

---

### 💼 CRM System — Customer Relationship Management Platform

> Production-grade CRM backend built during internship at AB Infotech Solutions

**Repo:** [github.com/Akhilesh9911/crm-system-fullstack](https://github.com/Akhilesh9911/crm-system-fullstack) | **Live:** [crm-system-fullstack.vercel.app](https://crm-system-fullstack.vercel.app)

**Key Engineering:**
- Multi-module Spring Boot backend — Leads, Contacts, Deals, Tasks, Activities, Notifications
- Normalized **8-table MySQL schema** with FK constraints and cascade rules
- **5-stage deal pipeline** (PROSPECTING → PROPOSAL → NEGOTIATION → CLOSED_WON/LOST) with dedicated `PATCH /deals/{id}/stage` endpoint
- Immutable **Activity audit log** tracking all entity lifecycle events automatically
- **RBAC** (USER/ADMIN) with Spring Security, JWT stateless auth, and `@PreAuthorize` method-level security
- **Cross-entity global search API** across Leads, Contacts, Deals, Tasks with case-insensitive matching
- **4 analytics dashboard endpoints** — pipeline summary, deals-by-stage, leads-by-month, tasks-by-priority
- JavaMailSender integration for transactional emails and secure password reset with time-limited tokens

**Tech:** Java 17 · Spring Boot · Spring Security · JWT · Spring Data JPA · Hibernate · MySQL · JavaMailSender · Lombok · Maven

---

### 🌿 Soybean Leaf Disease Detection — IEEE CNC-2025

> Co-authored research paper published at IEEE International Conference on Communication Networks and Computing (CNC-2025)

**Publication:** [ieeexplore.ieee.org/document/11484568](https://ieeexplore.ieee.org/document/11484568)
**Repo:** [github.com/Akhilesh9911/Soyabean_Leaf_Disease_Detection](https://github.com/Akhilesh9911/Soyabean_Leaf_Disease_Detection)

**Key Engineering:**
- Custom CNN (PyTorch) for binary classification — Healthy / Yellow Mosaic Disease — with ImageNet-normalized preprocessing and softmax confidence scoring
- YOLOv8-based severity grading model with data augmentation and hyperparameter tuning
- Multi-stage image validation pipeline — dimension, aspect ratio, contrast, RGB channel dominance, texture variance checks before inference
- Severity scoring: None (Healthy) · Low (<60%) · Moderate (60–80%) · High (>80% confidence)
- Flask web application with session-based authentication, SQLite-based analysis history, per-user statistics dashboard, and secure password reset with time-limited tokens
- Deployed on Render via Gunicorn

**Tech:** Python · PyTorch · Flask · OpenCV · SQLite · Gunicorn · Render

---

## 🎯 Current Focus

- ✔ Building production-ready Java backend systems
- ✔ Deepening microservices and distributed systems knowledge
- ✔ Writing clean, maintainable, SOLID code
- ✔ Improving DSA and problem-solving skills
- ✔ Open to entry-level Java Backend Developer / Software Developer roles

---

## 🤝 Connect With Me

<p align="left">
<a href="https://www.linkedin.com/in/akhilesh00/">
<img src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" width="35"/>
</a>
</p>

📧 akhileshchitare04@gmail.com
🔗 [linkedin.com/in/akhilesh00](https://www.linkedin.com/in/akhilesh00/)
💻 [github.com/Akhilesh9911](https://github.com/Akhilesh9911)

---

## ⚡ Fun Fact
🧩 Competitive Rubik's Cube solver — sub-30s average
