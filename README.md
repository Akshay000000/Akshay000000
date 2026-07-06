<div align="center">

# Bhaskara Akshay Sriram

### CS + AI/DS @ IIIT Kottayam '27 &nbsp;·&nbsp; Builder · Open Source Contributor · Researcher

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/akshay-sriram-6b8215296/?skipRedirect=true)
[![LeetCode](https://img.shields.io/badge/LeetCode-FFA116?style=for-the-badge&logo=leetcode&logoColor=black)](https://leetcode.com/u/akshaysriram/)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:akshaysriram.b@gmail.com)
[![Azure Certified](https://img.shields.io/badge/Azure_AI_Engineer_Associate-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)](https://learn.microsoft.com/en-us/users/akshaysriram-1455/credentials/certification/azure-ai-engineer)
[![Portfolio](https://img.shields.io/badge/Portfolio-ff6a00?style=for-the-badge&logo=vercel&logoColor=white)](https://portfolio-akshay-sriram.vercel.app)
[![CNCF](https://img.shields.io/badge/CNCF-Meshery_Contributor-00C896?style=for-the-badge&logo=cncf&logoColor=white)](https://github.com/meshery/meshery)

</div>

---

## `> whoami`

```
B.Tech CSE (AI & Data Science) — IIIT Kottayam, Class of 2027
Microsoft Certified: Azure AI Engineer Associate
Certified Meshery Contributor (CMC) — Layer5 / CNCF
LFX Mentorship 2026 Applicant — Meshery AI Adapter + Agentic CI Pipelines
Competitive Programmer — 350+ LeetCode problems solved
Hackathon Builder — Varroc Eureka 3.0 & Smart India Hackathon
Powerlifting Champion — IIIT-K Sports Meet 2026
```

I build **end-to-end AI systems** — from multi-LLM inference backends and real-time computer vision pipelines to full-stack dashboards and cloud-native tooling. Currently contributing to the CNCF Meshery ecosystem and applying for LFX Mentorship 2026 Term 2.

> **Check out my full portfolio:** [portfolio-akshay-sriram.vercel.app](https://portfolio-akshay-sriram.vercel.app)

---

## `> ls projects/`

### AEO Diagnostic + Meshery AI Adapter Prototype
> **Live Demo:** [aeo-diag-akshay.vercel.app](https://aeo-diag-akshay.vercel.app) &nbsp;|&nbsp; `Python · FastAPI · Groq · Cohere · Ollama · React · Render · Vercel`

A production multi-LLM backend with two modes — AI Engine Optimization scoring and a Meshery AI Adapter proof of concept.

**AEO Diagnostic:**
- Queries Groq (Llama 3.3, Llama 3.1) and Cohere Command-A **simultaneously** using Python `ThreadPoolExecutor`
- Sub-3-second multi-provider responses with mention detection, position ranking, and sentiment scoring
- Structured JSON output pipeline with robust response parsing across inconsistent LLM formats

**Meshery AI Adapter Prototype** *(CNCF open source contribution):*
- FastAPI endpoint accepts **natural language infrastructure intent** and returns valid Meshery design manifests
- Output aligned with `designs.meshery.io/v1beta1` schema
- **BYOM provider switching** across Groq, Cohere, and Ollama (local inference) — zero code changes
- Multi-provider parallel mode queries all cloud providers simultaneously and returns best valid schema
- Built as proof of concept for [issue #19092](https://github.com/meshery/meshery/issues/19092)

---

### Two-Wheeler Driving Behavior Scorer
> **Varroc Eureka 3.0 Hackathon** &nbsp;|&nbsp; `Python · OpenCV · YOLOv8 · FastAPI · React · NumPy`

Real-time ADAS system that scores two-wheeler riding behavior **0–100** with live video analysis.

- 60fps WebSocket video streaming with React + FastAPI dashboard
- Constant-Acceleration **Kalman filter** on ego-motion-compensated centroids via Lucas-Kanade optical flow
- Calibration-free speed estimation using fleet-shared MPP (`m/px = w_real / w_bbox`)
- **6 behavioral metrics**: hard brake, aggressive acceleration, lane weave, tailgating, sudden stop, helmet non-compliance
- Helmet detection via Otsu blob analysis with 30-frame majority vote + Re-ID by proximity
- Written about in depth: [Medium blog post](https://medium.com/@akshaysriram.b/building-a-real-time-two-wheeler-driving-behavior-scorer-from-hackathon-idea-to-production-adas-c426b0bd5690)

---

### Cal Clone — Scheduling Platform
> `Next.js 14 · TypeScript · PostgreSQL · Prisma · Tailwind CSS · Nodemailer`

Full-stack Cal.com-style scheduling app with production-grade architecture.

- Event type CRUD with unique URL slugs & per-day availability rules with timezone support
- Real-time **double-booking prevention** via half-open interval overlap checks in Prisma serializable transactions
- Normalized **6-table PostgreSQL schema** with composite indexes on `(event_type_id, date, status)` for fast slot queries
- Denormalized `end_time` for efficient overlap detection
- Automated email notifications for confirmations, cancellations & 24-hour reminders via secure Cron jobs
- 11 REST API endpoints · JWT authentication · Deployed on Vercel

---

## `> cat open_source.log`

**Meshery / Layer5 (CNCF)** &nbsp;|&nbsp; *Active Contributor — 2026–Present*
> `TypeScript · React · Go · GitHub Actions`

- **PR [#1493](https://github.com/layer5io/sistent/pull/1493)** approved in Sistent — Layer5's React/TypeScript CNCF design system (added `AssignmentTurnedInIcon`)
- **Certified Meshery Contributor (CMC)** — completed all 5 exam units (mesheryctl, Extensibility, Models, Server, UI)
- Reported and documented **2 production bugs** in Layer5 Cloud platform:
  - CMC exam submission flow — backend records attempt but frontend shows "Not Attempted"
  - Certificate rendering — `Cannot read properties of null (reading 'map')` on production-v1.0.73
  - Both acknowledged by [@leecalcote](https://github.com/leecalcote) on Slack
- Submitted attendance PRs to `meshery/meshery` for weekly Newcomers meetings
- Active engagement on issues [#19092](https://github.com/meshery/meshery/issues/19092) (AI Adapter), [#19012](https://github.com/meshery/meshery/issues/19012) (CI Pipelines), [#19419](https://github.com/meshery/meshery/issues/19419) (GitHub Actions), [#18751](https://github.com/meshery/meshery/issues/18751), [#18753](https://github.com/meshery/meshery/issues/18753)
- Responded to leecalcote's call for Meshery MCP Server volunteer maintainers on the Layer5 developers mailing list

---

## `> cat experience.log`

**Estimation of Failure of Airplane Engines** &nbsp;|&nbsp; *Student Researcher — DIAT, Pune (Dr. Yogeshwar Singh)*
- Built UI dashboard for data preprocessing and fusion workflows
- Deployed ML models for **Remaining Useful Life (RUL)** estimation on the NASA C-MAPSS dataset with multi-sensor time-series data

**Non-Invasive Detection of Diabetes** &nbsp;|&nbsp; *Research — IIT Bombay (Dr. Mahesh Parihar)*
- Trained classification models (Logistic Regression, KNN, Decision Trees) on Pima Indians Diabetes Dataset
- Achieved **96% accuracy** with ROC-AUC benchmarking

---

## `> cat stack.json`

```json
{
  "languages":     ["C", "C++", "Python", "JavaScript", "TypeScript", "Java", "SQL", "Go"],
  "ai_ml":         ["LLM APIs (Groq, Cohere, OpenAI, Ollama)", "TensorFlow", "Keras", "OpenCV", "YOLOv8", "Scikit-learn"],
  "web":           ["React", "Next.js 14", "FastAPI", "Node.js", "Tailwind CSS", "Prisma", "WebSockets"],
  "databases":     ["PostgreSQL", "MongoDB", "SQL"],
  "devops":        ["Git", "Docker", "GitHub Actions", "Vercel", "Render"],
  "cloud":         ["Microsoft Azure (AI Engineer Associate ✓)"],
  "core_cs":       ["System Design", "OOPS", "OS", "DBMS", "Compiler Design", "Computer Networks"]
}
```

---

## `> cat achievements.txt`

```
CNCF Open Source — Certified Meshery Contributor (CMC), PR #1493 merged in Sistent
LFX Mentorship 2026 Applicant — Meshery AI Adapter + Agentic CI Pipelines (CNCF)
Varroc Eureka 3.0 Hackathon — Built real-time ADAS scoring system (National Level)
Smart India Hackathon 2024 — Participant
Powerlifting — Winner, Intra IIIT-K Sports Meet 2026
Basketball — Winners, School-level & Intra IIIT-K Sports Meet 2023
350+ LeetCode problems solved (DSA)
Microsoft Azure AI Engineer Associate — Certified (Valid: July 2025 – July 2026)
```

---

## `> contact --me`

Got a project idea, research opportunity, or just want to connect?

**Email** — [akshaysriram.b@gmail.com](mailto:akshaysriram.b@gmail.com)
**Medium** — [medium.com/@akshaysriram.b](https://medium.com/@akshaysriram.b)
