# Project Proposal

Title: Web System for Student Hackathon Management with Multi-Criteria Team Formation.

Team Members: Elkham Mamedov, Ilnur Saipiyev, Alisher Askar.

Supervisor: Nurtas Nadirov

**Elkham Mamedov:** responsible for requirements analysis, QA, integration and documentation.

**Ilnur Saipiyev:** responsible for the backend, database and matching algorithm.

**Alisher Askar:** responsible for the frontend.

**Project stage:** analysis, design and initial technical setup.

## Problem Statement

Organizing student hackathons presents significant administrative and algorithmic challenges. On the administrative side, organizers struggle with fragmented workflows, including handling participation registration, team formation, submissions, and evaluations across multiple disconnected tools (e.g., Google Forms, spreadsheets, messaging apps). On the participant side, team formation is often inefficient and biased. Students frequently form teams solely based on existing social connections rather than complementary skills, leading to unbalanced teams. Unaffiliated participants ("solo registrants") face high barriers to entry, often being assigned randomly or left out entirely. The reviewed alternatives do not establish a single workflow combining full hackathon administration, explainable multi-criteria recommendations and participant confirmation. This combination motivates the proposed design.

## Target Users

Hackathon organizers, including academic staff, student organizations, or event administrators who manage event schedules, registration, team allocations, announcements, and scoring/judging workflows

Student participants, whether individual students or pre-formed teams looking for missing skill sets, project tracks, or suitable teammates based on technical criteria.

Judges, mentors, or faculty members, who will be evaluating project submissions based on specific scoring rubrics.

## Aim

To design, implement, and evaluate a centralized web platform that streamlines end-to-end hackathon administration while automating balanced, skill-based team formation via a multi-criteria algorithm.

## Objectives

Requirements and Research. Conduct user interviews and comparative analyses of existing hackathon platforms and matching algorithms to establish system requirements.

System Architecture and Design. Design a scalable web application architecture with database schemas, API contracts, and user interaction scenarios.

Multi-criteria matching algorithm. Formulate and implement a team formation algorithm that processes participant profiles (skills, roles, project preferences, availability) to suggest or create balanced teams.

Platform core features development. Implement participant profile management, organizer management dashboards, real-time team discovery, and submission/scoring modules.

Testing and Evaluation. Validate system performance, usability, and matching algorithm quality against a baseline solution using clear evaluation metrics.

## Expected Outcomes

A fully operational web platform with responsive user interfaces and scalable RESTful APIs.

An algorithmic engine capable of generating multi-criteria match scores for team formation.

Unified handling of event creation, registration, team formation, project submission, and judging.

Complete technical and analytical documentation, including architecture diagrams, literature reviews, technology comparisons, and verification plans.

## Project Scope

In-Scope

User Management: authentication, authorization, role-based control, and detailed skill/profile building.

Hackathon event management: event creation, track setting, registration timelines, schedule updates, and announcements.

Multi-criteria team formation:

Algorithmic teammate recommendations for incomplete teams.

Auto-grouping mechanism for solo registrants based on complementary skill matrices and role coverage.

Submission and evaluation portal: project submission links (repository, demo), assigned judging scoring sheets, and leaderboard generation.

System documentation and testing: source code repository management, task traceability, end-to-end testing, and architectural design.

Out-of-Scope

Native mobile applications. The system will be implemented strictly as a responsive web application.

In-platform live code execution / sandbox. Code testing and verification will rely on external links (e.g., GitHub, live demo URLs).

Payment / prize distribution integrations. Financial transactions or sponsorship payment processing will not be included in the initial implementation.
