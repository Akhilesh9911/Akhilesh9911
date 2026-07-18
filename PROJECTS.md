# 🚀 Projects Portfolio

Detailed documentation of all my projects and their implementations.

---

## 1. 🎯 HireForge AI — Career Acceleration Platform

### Overview
An AI-powered platform designed to help job seekers at every stage of their career journey—from resume optimization to job tracking and interview preparation.

### Problem Statement
Job seekers struggle with:
- Creating effective resumes that pass ATS screening
- Preparing for technical interviews
- Tracking multiple job applications
- Understanding personalized career paths

### Solution
HireForge AI provides an integrated ecosystem with AI-powered insights at every step.

### Key Features

#### 1. **Resume Intelligence**
- Automatic resume parsing and analysis
- AI-powered enhancement suggestions using Google Gemini API
- ATS compatibility scoring
- Resume templates for different roles
- PDF & DOC format support

#### 2. **Interview Preparation**
- AI-generated mock interview questions
- Answer evaluation with feedback
- Topic-wise question categories
- Performance analytics
- Practice tracking

#### 3. **Application Tracking**
- Centralized job application management
- Status tracking (applied, interview, rejected, offered)
- Interview scheduling
- Follow-up reminders
- Application analytics dashboard

#### 4. **Career Insights**
- Personalized career path recommendations
- Skills gap analysis
- Market demand assessment
- Salary insights by role & location
- Learning recommendations

#### 5. **Document Generation**
- AI-generated cover letters
- Professional portfolio samples
- Customizable templates
- One-click downloads

### Technical Architecture

#### Backend Structure
```
Spring Boot 3.x Application
├── Controllers (REST endpoints)
├── Services (Business logic)
├── Repositories (Database access)
├── Security (JWT, RBAC)
├── DTOs (Data transfer objects)
├── Entities (JPA models)
└── Utils (Helpers & converters)
```

#### Database Schema
- **Users** - User authentication & profiles
- **Resumes** - Resume storage & versions
- **JobApplications** - Application tracking
- **Interviews** - Interview data
- **MockQuestions** - Interview questions
- **UserAnswers** - Interview responses
- **CareerInsights** - Personalized recommendations
- **Documents** - Generated documents
- **Logs** - Audit & activity logs

#### Security Implementation
- **Authentication:** JWT tokens with expiration
- **Authorization:** Role-based access control (RBAC)
- **Password Security:** BCrypt hashing
- **API Security:** CORS configuration, request validation
- **Data Protection:** Encryption for sensitive fields

### Technology Stack
| Component | Technology |
|---|---|
| Language | Java 17 |
| Framework | Spring Boot 3.x |
| Security | Spring Security, JWT |
| ORM | Hibernate, JPA |
| Database | MySQL 8.0 |
| File Processing | Apache PDFBox, Apache POI |
| AI Integration | Google Gemini API |
| Containerization | Docker, Docker Compose |
| Build Tool | Maven |
| API Testing | Postman |

### API Endpoints (25+)

**Authentication:**
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `POST /api/auth/refresh-token` - Token refresh

**Resume Management:**
- `POST /api/resumes/upload` - Upload resume
- `GET /api/resumes` - Get user resumes
- `POST /api/resumes/{id}/analyze` - AI analysis
- `PUT /api/resumes/{id}` - Update resume

**Job Applications:**
- `POST /api/applications` - Add application
- `GET /api/applications` - Get all applications
- `PUT /api/applications/{id}` - Update status
- `DELETE /api/applications/{id}` - Remove application

**Interviews:**
- `POST /api/interviews` - Schedule interview
- `GET /api/interviews/upcoming` - Get upcoming interviews
- `POST /api/interviews/{id}/questions` - Get mock questions
- `POST /api/interviews/{id}/evaluate` - Evaluate answers

**Career Insights:**
- `GET /api/insights/recommendations` - Get career recommendations
- `GET /api/insights/skills-gap` - Skills analysis
- `GET /api/insights/market-trends` - Market insights

### Performance Metrics
- **Response Time:** < 200ms average
- **Database Queries:** Optimized with proper indexing
- **Concurrent Users:** Supports 1000+ concurrent sessions
- **Uptime:** 99.9% availability target

### Deployment
- **Platform:** Docker containers
- **Orchestration:** Docker Compose for local development
- **CI/CD:** GitHub Actions for automated builds
- **Environment:** Development, Staging, Production

### Future Enhancements
- [ ] LinkedIn integration for auto-fill profiles
- [ ] Real-time job scraping from multiple sources
- [ ] Video interview preparation with recording
- [ ] Salary negotiation assistant
- [ ] Network building recommendations
- [ ] Microservices architecture migration

---

## 2. 👥 CRM System

### Overview
A customer relationship management platform for businesses to manage the entire customer lifecycle.

### Link
**Live Deployment:** [crm-system-fullstack.vercel.app](https://crm-system-fullstack.vercel.app)

### Key Features
- Customer & contact management
- Lead tracking & conversion
- Sales pipeline with deal management
- Task & activity tracking
- Admin user management
- Real-time synchronization

### Tech Stack
`Java` `Spring Boot` `Hibernate/JPA` `MySQL` `REST APIs` `React.js`

---

## 3. 🌿 Soybean Leaf Disease Detection

### Overview
Machine learning project using YOLOv8 for detecting crop diseases.

### Publication
**IEEE CNC-2025:** "YOLOv8-Based Soybean Leaf Disease Detection"

### Tech Stack
`Python` `YOLOv8` `OpenCV` `Deep Learning` `TensorFlow`

### Key Achievements
- High accuracy disease detection
- Real-time inference
- Published in IEEE conference

---

## 📊 Project Comparison

| Feature | HireForge AI | CRM | Soybean Detection |
|---|---|---|---|
| Type | Backend + AI Platform | Full-Stack Web App | ML/AI Research |
| Scale | Medium (10K users) | Medium | Research Grade |
| Deployment | Docker | Vercel (Live) | Published |
| Tech Focus | Java Backend + AI | Full-Stack | Python ML |
| Status | Production Ready | Live | Published in IEEE |

---

## 🎓 Learning Outcomes

### Software Architecture
- Monolithic vs Microservices design
- API design & REST principles
- Database normalization & optimization
- Security & authentication patterns

### Best Practices
- Clean code principles
- SOLID principles
- Design patterns (Factory, Singleton, etc.)
- Error handling & logging
- Version control & Git workflows

### DevOps & Deployment
- Docker containerization
- Docker Compose orchestration
- GitHub Actions CI/CD
- Environment configurations
- Deployment strategies

---

## 🏆 Achievements

✅ Built production-grade systems with 15,000+ lines of code
✅ Integrated AI APIs for intelligent features
✅ Implemented enterprise security patterns
✅ Created scalable architectures
✅ Deployed applications in containers
✅ Published research in IEEE conference
✅ Demonstrated full-stack capabilities

---

**All projects demonstrate:**
- Production-ready code quality
- Scalability & performance
- Security & best practices
- Full-stack development skills
- Problem-solving abilities
- AI/ML integration expertise
