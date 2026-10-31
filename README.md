# Web System for Student Hackathon Management with Multi-Criteria Team Formation

## 1. Project Overview & Problem Statement

- Project Title: Web System for Student Hackathon Management with Multi-Criteria Team Formation.
- Brief Description: A proposed centralized web platform for student hackathon administration and multi-criteria team formation.
- Problem Statement: Hackathon administration can involve separate registration forms, spreadsheets and messaging tools. HackMatch will connect event administration with participant profiles, explainable teammate recommendations and participant confirmation. The preliminary survey informs feature priorities, while the literature review and existing-system comparison inform the proposed design. The survey does not establish that algorithmic matching improves team performance. See [evidence of relevance](docs/relevance.md) and [existing-system comparison](docs/existing-systems.md).
- Target Users:
  - Hackathon organizers managing events, registrations, teams, announcements and judging.
  - Student participants registering individually or as teams and seeking suitable teammates.
  - Judges evaluating assigned submissions against event rubrics.
- Aim: To design, implement and evaluate a centralized web platform that combines hackathon administration with multi-criteria team formation.
- Objectives:
  1. Validate user needs and compare existing platforms and matching approaches.
  2. Design the system architecture, database, API contracts and user scenarios.
  3. Implement team recommendations based on skills, roles, interests and availability.
  4. Implement event registration, profiles, team management, submissions and judging.
  5. Evaluate technical correctness, usability and matching quality against a baseline.

## 2. Team Members & Supervisor

| Member | Responsibilities |
| --- | --- |
| Elkham Mamedov | Requirements analysis, QA, integration and documentation |
| Ilnur Saipiyev | Backend, database and matching algorithm |
| Alisher Askar | Frontend |

Supervisor: Nurtas Nadirov.

## 3. Scope & Development Status

### In scope

- Accounts, authentication, role-based access and participant profiles.
- Event creation, rules, registration, schedules and announcements.
- Multi-criteria teammate recommendations and team formation for solo participants.
- Invitations, participant confirmation and organizer adjustments.
- Project submission through repository and demo links.
- Rubric-based judging and results.
- Documentation, testing and evaluation.

### Out of scope

- Native mobile applications.
- Execution of submitted code within the platform.
- Payment processing and prize distribution.

Current status: Analysis, literature review, requirements engineering, architectural design and initial technical setup. Documentation and prototype materials are available; application implementation and evaluation trials are pending.

## 4. Selected Technology Stack

| Area | Selected technology |
| --- | --- |
| Frontend | Next.js, React, TypeScript, Tailwind CSS |
| Backend | Node.js, Express |
| Database | PostgreSQL |
| Matching module | Rule-based baseline and weighted multi-criteria strategy |
| Version control | Git and GitHub |
| Task tracking | YouTrack |
| Interface design | Figma |
| API testing | Postman |

The backend and matching module are planned components. See [technology comparison](docs/technology-comparison.md) for alternatives and selection reasons.

## 5. Links & Resources

The project uses multiple repositories. Hackmatch contains shared documentation, diagrams, prototype materials and project-wide QA materials. Application code, configuration and component tests belong in the frontend and backend repositories.
[31.10.2026 22:33] Ильнур: - [Shared project repository](https://github.com/hackmatch-diploma/Hackmatch)
- [Frontend repository](https://github.com/hackmatch-diploma/hackmatch-frontend)
- [Backend repository](https://github.com/hackmatch-diploma/hackmatch-backend)
- [YouTrack board](https://hackmatch.youtrack.cloud/agiles/204-0/current)
- [Figma prototype](https://www.figma.com/design/bwuI4WpM8lHKXQNkIWr8dK/HackMatch-UI-UX-proto?node-id=0-1)
- [Pre-defense 1 snapshot](https://github.com/hackmatch-diploma/Hackmatch/releases/tag/pre-defense-1)

## 6. Documentation

- [Project proposal](docs/project-proposal.md)
- [Evidence of relevance and survey analysis](docs/relevance.md)
- [Literature review](docs/literature-review.md)
- [Existing-system comparison](docs/existing-systems.md)
- [Technology comparison](docs/technology-comparison.md)
- [Requirements specification](docs/requirements.md)
- [Architecture](docs/architecture.md)
- [Prototype design notes](designproto/prototype.md)
- [Evaluation plan](docs/evaluation-plan.md)
- [Project management and risks](docs/project-management.md)
- [Supervisor feedback](docs/supervisor-feedback.md)
- [References](docs/references.md)
- [Word report](docs/report.docx)
- [Survey results](docs/Опросник/)
- [Architecture diagram sources and exports](diagrams/)

## 7. Repository Structure & Deliverables Index

Shared documentation and design materials are maintained in this repository. Frontend and backend application code is maintained in the separate repositories linked above.

```text
Hackmatch/
├── README.md
├── .gitignore
├── docs/
│   ├── project-proposal.md
│   ├── relevance.md
│   ├── literature-review.md
│   ├── existing-systems.md
│   ├── technology-comparison.md
│   ├── requirements.md
│   ├── architecture.md
│   ├── evaluation-plan.md
│   ├── project-management.md
│   ├── supervisor-feedback.md
│   ├── references.md
│   ├── report.docx
│   └── Опросник/
├── diagrams/
│   ├── source/
│   └── exports/
└── designproto/
    ├── prototype.md
    ├── assets/
    └── UI-UX_protolink_figma.pdf
```

Editable SVG diagrams are stored in diagrams/source/ and PNG exports in diagrams/exports/. Prototype screenshots are stored in designproto/assets/.

Project-wide manual test cases, requirement coverage and integration test reports will be added under tests/ as they are prepared. Backend and frontend automated tests and configuration files belong in their respective application repositories.

## 8. Requirements Specification Summary

The tables below summarise the current [requirements specification](docs/requirements.md).

### Functional requirements

| ID | Requirement | Priority | Verifiable acceptance criterion |
| --- | --- | --- | --- |
| FR-01 | Create hackathon events | High | The organizer saves an event with title, dates, rules and team size; it appears in the event list. |
| FR-02 | Register for an event | High | Eligible students submit a registration and see confirmation; duplicate submission is blocked. |
| FR-03 | Edit participant profile | High | Students have skills, experience, preferred roles and interests; values remain after login. |
| FR-04 | Suggest teammates | High | System returns candidate teams using specified criteria and configured minimum/maximum size. |
| FR-05 | Confirm or decline a team | High | Students confirm or reject an invitation; team membership updates accordingly. |
| FR-06 | Manage teams manually | Medium | The organizer can reassign a participant; the updated team remains within valid constraints. |
| FR-07 | Submit a project | High | Team submits repository and demo links before deadline; submission is visible to the organizer. |
| FR-08 | View judging results | Medium | An authorized judge submits rubric scores and the organizer sees the results. |

### Non-functional requirements
[31.10.2026 22:33] Ильнур: | ID | Requirement | Priority | Verifiable acceptance criterion |
| --- | --- | --- | --- |
| NFR-01 | Role-based access | High | A participant account cannot reach organizer-only APIs; unauthorized requests return 403. |
| NFR-02 | Responsive interface | High | Registration and team screens are usable at 375 px and 1280 px widths without horizontal overflow. |
| NFR-03 | Explainability and invalid constraints | High | Every suggestion shows criteria used; impossible constraints produce a clear warning instead of an invalid team. |

## 9. System Architecture Overview

The proposed system follows a three-tier architecture:

1. Presentation tier: A responsive Next.js application using React, TypeScript and Tailwind CSS, communicating with the backend through a REST API.
2. Application tier: A Node.js and Express server containing authentication, event management, team management, submission and judging modules. An internal matching module supports rule-based and weighted strategies.
3. Data tier: PostgreSQL stores users, events, registrations, profiles, teams, memberships, invitations, announcements, submissions and scores.

See [architecture documentation](docs/architecture.md) and [diagrams](diagrams/).

## 10. Repository Access and Local Development

Clone the shared documentation repository:

git clone https://github.com/hackmatch-diploma/Hackmatch.git

Clone the application repositories separately:

git clone https://github.com/hackmatch-diploma/hackmatch-backend.git
git clone https://github.com/hackmatch-diploma/hackmatch-frontend.git

Installation, environment configuration, execution and testing instructions will be maintained in each application repository when runnable code is available. Node.js and PostgreSQL version requirements will be documented alongside that implementation.

## 11. Development Workflow

Each meaningful work item should have a YouTrack task with an owner, priority, deadline and acceptance criteria. Include the task ID in the branch name and commit message or pull request description, and link the pull request or commit from the task.

Develop changes in a task branch, open a pull request and obtain another team member's review before merging into main.

The pre-defense-1 tag identifies a fixed submission snapshot. Later commits may differ from that snapshot. Existing submission tags are retained.