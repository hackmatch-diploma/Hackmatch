# Web System for Student Hackathon Management with Multi-Criteria Team Formation

## 1. Project Overview & Problem Statement

- **Project Title:** Web System for Student Hackathon Management with Multi-Criteria Team Formation
- **Brief Description:** A centralized web platform designed to streamline student hackathon administration while automating skill-balanced, multi-criteria team formation for participants and solo registrants.
- **Problem Statement:** Organizing student hackathons presents significant administrative and algorithmic challenges. On the administrative side, organizers struggle with fragmented workflows across disconnected tools (e.g., Google Forms, spreadsheets, messaging apps) to manage registrations, teams, submissions, and evaluations. On the participant side, team formation is often inefficient and biased toward existing social connections rather than complementary skills. Unaffiliated participants ("solo registrants") face high barriers to entry, often being assigned randomly or left out entirely. Existing platforms lack automated, multi-criteria team formation algorithms that match participants based on skill sets, experience levels, preferred roles, and project preferences.
- **Target Users:**
  - **Hackathon Organizers:** Academic staff, student organizations, or event administrators managing event schedules, registrations, team allocations, announcements, and evaluation workflows.
  - **Student Participants:** Individual students or pre-formed teams seeking missing skill sets, project tracks, or suitable teammates based on technical criteria.
  - **Judges / Mentors:** Faculty members or industry experts evaluating project submissions against scoring rubrics.
- **Aim:** To design, implement, and evaluate a centralized web platform that streamlines end-to-end hackathon administration while automating balanced, skill-based team formation via a multi-criteria algorithm.
- **Objectives:**
  1. **Requirements & Research:** Conduct user interviews and comparative analyses of existing hackathon platforms and matching algorithms to establish system requirements.
  2. **System Architecture & Design:** Design a scalable web application architecture with database schemas, API contracts, and user interaction scenarios.
  3. **Multi-Criteria Matching Algorithm:** Formulate and implement a team formation algorithm that processes participant profiles (skills, roles, project preferences, availability) to suggest or create balanced teams.
  4. **Platform Core Features Development:** Implement participant profile management, organizer management dashboards, real-time team discovery, and submission/scoring modules.
  5. **Testing & Evaluation:** Validate system performance, usability, and matching algorithm quality against a baseline solution using clear evaluation metrics.

---

## 2. Team Members & Supervisor

- **Team Members:**
  - **Elkham Mamedov** – Requirements Analysis, Quality Assurance, Integration & Documentation
  - **Ilnur Saipiyev** – Backend Development, Database Engineering & Matching Algorithm Optimization
  - **Alisher Askar** – Frontend Development & Responsive UI Implementation
- **Supervisor:** Nurtas Nadirov

---

## 3. Scope & Development Status

- **Project Scope:**
  - **In-Scope:**
    - **User Management:** Authentication, authorization, Role-Based Access Control (RBAC), and detailed skill/profile building.
    - **Hackathon Event Management:** Event creation, track setting, registration timelines, schedule updates, and announcements.
    - **Multi-Criteria Team Formation:** Algorithmic teammate recommendations for incomplete teams and auto-grouping for solo registrants based on complementary skill matrices and role coverage.
    - **Submission & Evaluation Portal:** Project submission links (repository, demo), assigned judging scoring sheets, and leaderboard generation.
    - **System Documentation & Testing:** Source code repository management, YouTrack task traceability, end-to-end API testing, and architectural design.
  - **Out-of-Scope:**
    - Native mobile applications (desktop and mobile responsive web application only).
    - In-platform live code execution or sandbox (verification relies on external GitHub/demo links).
    - Payment or prize distribution integrations.
- **Current Development Status:** Phase 1 – System Analysis, Literature Review, Requirements Engineering, Architectural Design, and Initial Technical Setup (Pre-Defense 1).

---

## 4. Finalized Technology Stack

- **Frontend:** Next.js (React, TypeScript, Tailwind CSS) for reusable component architecture, real-time dashboards, and responsive forms.
- **Backend:** Node.js / Express.js REST API providing authentication, RBAC, event management, submission, and judging endpoints.
- **Database:** PostgreSQL for relational data storage (users, events, applications, teams, submissions, and scores).
- **Matching Module:** Integrated modular engine supporting both a simple rule-based baseline and a weighted multi-criteria matching strategy with explainable feedback.
- **DevOps & Tooling:** Git / GitHub (Version control), YouTrack (Task tracking), Figma (UI Mockups), Postman (API Testing).

---

## 5. Links & Resources

- **YouTrack Board:** [View Agile Board](https://hackmatch.youtrack.cloud/agiles/204-0/current)
- **Frontend Repository:** [hackmatch-frontend](https://github.com/hackmatch-diploma/hackmatch-frontend)
- **Backend Repository:** [hackmatch-backend](https://github.com/hackmatch-diploma/hackmatch-backend)

---

## 6. Repository Structure & Deliverables Index

The overall project documentation deliverables and complete technical report are organized inside this `.github` repository:

```text
.
├── README.md                      <-- Organization Landing Page & Main Project Overview
└── docs/
    └── report.docx                <-- Consolidated Technical Report
```

---

## 7. Requirements Specification Summary

### Functional Requirements Matrix

| ID        | Requirement Title           | Priority | Verifiable Acceptance Criterion                                                                                 |
| :-------- | :-------------------------- | :------: | :-------------------------------------------------------------------------------------------------------------- |
| **FR-01** | Create Hackathon Events     |   High   | The organizer saves an event with title, dates, rules, and team size; it appears in the active event list.      |
| **FR-02** | Register for Event          |   High   | Eligible students submit registration and see confirmation; duplicate submissions are blocked.                  |
| **FR-03** | Edit Participant Profile    |   High   | Students specify skills, experience, preferred roles, and interests; saved values persist across sessions.      |
| **FR-04** | Suggest Teammates           |   High   | System returns candidate teams using specified criteria and configured minimum/maximum size constraints.        |
| **FR-05** | Confirm / Decline Team      |   High   | Students confirm or reject team invitations; team membership updates accordingly.                               |
| **FR-06** | Manual Organizer Management |  Medium  | Organizer reassigns a participant; updated team remains within valid size and role constraints.                 |
| **FR-07** | Submit Deliverables         |   High   | Teams submit repository and demo links prior to the deadline; submission is visible on the organizer dashboard. |
| **FR-08** | View Judging Results        |  Medium  | Authorized judges submit rubric scores; organizer views aggregated results and leaderboard.                     |

### Non-Functional Requirements Matrix

| ID         | Requirement Title                    | Priority | Verifiable Acceptance Criterion                                                                                                              |
| :--------- | :----------------------------------- | :------: | :------------------------------------------------------------------------------------------------------------------------------------------- |
| **NFR-01** | Role-Based Access Control            |   High   | Participant accounts cannot reach organizer-only APIs; unauthorized requests return HTTP `403 Forbidden`.                                    |
| **NFR-02** | Responsive Interface                 |   High   | Registration, profile, and team screens are fully functional at 375 px (mobile) and 1280 px (desktop) viewports without horizontal overflow. |
| **NFR-03** | Explainability & Constraint Warnings |   High   | Match recommendations display criteria used; impossible constraints trigger clear error warnings instead of generating invalid teams.        |

---

## 8. System Architecture Overview

The system follows a three-tier architecture:

1. **Presentation Tier:** Next.js (React / Tailwind CSS) responsive web application communicating via REST API endpoints.
2. **Application Tier:** Node.js / Express/NestJS server containing authentication, event workflow handlers, submission modules, and an isolated matching module containing both rule-based baseline and weighted multi-criteria algorithms.
3. **Data Tier:** PostgreSQL relational database managing persistent entities (Users, Events, Registrations, Teams, Submissions, Rubric Scores).

---

## 9. Setup & Local Development Instructions

_(To be populated as runnable code is deployed to the frontend and backend repositories)_

### Prerequisites

- **Node.js**: v18.0.0 or higher
- **PostgreSQL**: v14.0 or higher
- **Git**

### Repository Access

```bash
# Clone the repository
git clone https://github.com/hackmatch-diploma/.github.git
```
