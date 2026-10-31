# HackMatch UI/UX Prototype

Clickable interface prototype for the HackMatch web system, made in Figma before the frontend implementation.

**Figma file:** [HackMatch UI/UX prototype](https://www.figma.com/design/bwuI4WpM8lHKXQNkIWr8dK/HackMatch-UI-UX-proto?node-id=0-1&t=ooBEZV299CzvuOMi-1)

## Purpose

The prototype shows the main screens for the three user roles (organizer, participant, judge) and the navigation between them. It is used to:

* agree on the interface with the supervisor before coding;
* guide the frontend implementation;
* prepare the tasks for task-based usability testing described in the evaluation plan.

## Design Approach

* Two layouts for every screen: **375 px** (phone) and **1280 px** (desktop), in line with NFR-02.
* One consistent style: top navigation bar, cards for events and teams, forms with error messages shown directly under the field, one primary action per screen.
* Reusable components (button, input, card, modal, navigation bar) shared across screens, matching the reusable UI components in the frontend.

## Screens

| Screen | Role | Related requirements |
| --- | --- | --- |
| Login and registration | All | FR-02 |
| Participant profile (skills, experience, roles, interests) | Participant | FR-03 |
| Events list and event details | Participant | FR-02 |
| Team suggestions with explanations, confirm and decline | Participant | FR-04, FR-05, NFR-03 |
| Organizer dashboard (registrations, teams, announcements, results) | Organizer | FR-01, FR-06 |
| Create and edit event | Organizer | FR-01 |
| Project submission | Participant (team) | FR-07 |
| Judging sheet and leaderboard | Judge, organizer | FR-08 |

## User Flows

1. **Organizer:** creates an event, reviews registrations, runs team formation, adjusts teams manually.
2. **Participant:** registers, fills in the profile, reviews team suggestions with their criteria, confirms a team.
3. **Team and judge:** the team submits repository and demo links, the judge enters rubric scores, the organizer views the leaderboard.

