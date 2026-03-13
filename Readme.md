# 🚀 AI-Powered Dynamic Resume Evaluator

A professional-grade, containerized **ATS (Applicant Tracking System) Simulator**. This application evaluates resumes against specific high-tech roles using a dynamic keyword-matching engine, providing precise scoring and skill gap analysis.



## 🛠 Tech Stack
* **Backend:** Java 21 (Eclipse Temurin), Spring Boot 3.x
* **Frontend:** HTML5, JavaScript (Async/Await), Bootstrap 5
* **Database:** MongoDB (NoSQL)
* **Containerization:** Docker & Docker Compose
* **Build Tool:** Maven

---

## 🏗 System Architecture

The application is built on a modern, decoupled architecture designed for scalability:

1.  **Frontend Layer:** A responsive web interface that handles role selection, candidate data, and file uploads.
2.  **Logic Layer (The Engine):** A Spring Boot service that utilizes a **Universal Keyword Library** to match candidate skills against a target role's requirements.
3.  **Persistence Layer:** A MongoDB instance that stores every evaluation, creating a historical audit trail of candidates.
4.  **DevOps Layer:** The entire environment is defined as code via `Dockerfile` and `docker-compose.yml`, ensuring "it works on my machine" translates to "it works everywhere."



---

## 📋 Key Features

* **Dynamic Role-Based Analysis:** Unlike static scorers, this tool adjusts its criteria based on the selected role (e.g., Cybersecurity, DevOps, Data Science).
* **Precise Scoring Engine:** Uses weighted calculations to provide a 0-100% score rather than simple increments.
* **Real-time Skill Feedback:** Identifies and lists exactly which keywords were detected in the resume.
* **Fully Containerized:** One-command deployment for the entire stack.

---
## ♾️ DevOps & Automation Lifecycle

This project demonstrates a complete CI/CD mindset by integrating industry-standard DevOps tools:

### 🐳 Containerization (Docker)
- **Multi-Container Orchestration:** Uses `docker-compose` to link the Spring Boot application and MongoDB, ensuring network isolation and environment parity.
- **Optimized Builds:** Implements a layered Dockerfile approach to speed up build times.

### 🧪 Automated Testing (QA)
- **Unit Testing:** JUnit 5 used for validating the core scoring logic and keyword matching.
- **Integration Testing:** Automated REST-based tests to ensure the API and Database interact correctly.
- **UI/Browser Automation:** (Optional Addition) Ready for **Selenium** integration to perform end-to-end (E2E) testing on the resume upload flow.

### ⚙️ CI/CD & Build Management
- **Maven:** Manages the entire build lifecycle, from dependency resolution to packaging.
- **Automated Pipeline:** The project is structured to be easily integrated into Jenkins or GitHub Actions, where every "Push" triggers a full rebuild and test suite execution.

----------------
## 🚀 Getting Started (DevOps Pipeline)

### 1. Prerequisites
* Docker Desktop installed
* Maven installed (optional, for local builds)

### 2. Build and Package
Generate the executable JAR file:
```powershell
mvn clean package -DskipTests