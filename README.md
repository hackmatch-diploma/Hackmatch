# HackMatch

Web System for Student Hackathon Management with Multi-Criteria Team Formation.

HackMatch is a planned web platform for student hackathon registration, participant profiles, voluntary teammate recommendations, project submission and judging. It connects these activities in one event workflow. The project is currently at the analysis, design and initial technical setup stage; application code is not included in this version.

## Team

| Member | Responsibilities |
| --- | --- |
| Elkham Mamedov | Requirements analysis, QA, integration and documentation |
| Ilnur Saipiyev | Backend, database and matching algorithm |
| Alisher Askar | Frontend |

Supervisor: Nurtas Nadirov.

## Users and scope

The intended users are student participants, hackathon organisers and judges. Planned outcomes are a responsive web application, a matching module and an evaluated registration-to-submission workflow. Participant confirmation and event-level access control are part of the design. Native mobile applications, code execution and payment processing are outside the scope.

## Technologies

Next.js, React, TypeScript and Tailwind CSS for the frontend; Node.js and Express for the REST API; PostgreSQL for storage. Matching will include a rule-based baseline and a weighted multi-criteria strategy.

## Documentation

- [Project proposal](docs/project-proposal.md)
- [Evidence of relevance and survey analysis](docs/relevance.md)
- [Literature review](docs/literature-review.md)
- [Existing systems](docs/existing-systems.md)
- [Technology comparison](docs/technology-comparison.md)
- [Requirements](docs/requirements.md)
- [Architecture](docs/architecture.md)
- [UX prototype](docs/ux-prototype.md)
- [Prototype design notes](designproto/prototype.md)
- [Evaluation plan](docs/evaluation-plan.md)
- [Project management and risks](docs/project-management.md)
- [Supervisor feedback](docs/supervisor-feedback.md)
- [References](docs/references.md)
- [Word report](docs/report.docx)
- [Survey results](docs/Опросник/)
- [Architecture diagram sources and exports](diagrams/)

## Project tracking

[YouTrack board](https://hackmatch.youtrack.cloud/agiles/204-0/current)

## Repository structure

```text
README.md
docs/
  assets/
  Опросник/
  report.docx
  *.md
diagrams/
  source/
  exports/
designproto/
```

Application setup and test commands will be documented when runnable code is added.
