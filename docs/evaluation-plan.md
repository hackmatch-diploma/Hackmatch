# Verification and Evaluation Plan

Evaluation will compare allocation quality, task completion and technical correctness. The student questionnaire provides preliminary preference data. Algorithm benchmarks and usability trials are planned after implementation.

## Algorithm comparison protocol

The algorithm comparison will use a versioned profile dataset with identical team-size, availability and role constraints for all methods. It will compare deterministic rule-based allocation, weighted multi-criteria allocation and organiser allocation where an organiser is available. Random allocation will provide an additional comparator over 30 recorded seeds. Real consented profiles and synthetic stress cases will be evaluated separately. Questionnaire responses describe preferences and will not be treated as complete matching profiles.

Benchmark records will include dataset size, hardware, code revision, weights, random seeds and runtime. Outcome measures are valid membership assignments, duplicate memberships, unassigned participants, required-role coverage, minimum team coverage, availability overlap and elapsed formation time. Mandatory-constraint violations will be counted separately from preference scores. Role coverage is the proportion of required roles filled, averaged over teams. The unassigned rate is the proportion of eligible participants left without a team. Organiser effort will be measured separately from algorithm execution time.

The evaluation targets are zero duplicate memberships and zero mandatory-constraint violations on feasible cases, with an explicit unresolved status for infeasible cases. Weighted matching is expected to preserve the assigned-participant count and improve mean role coverage relative to the rule-based baseline. Minimum team coverage and any trade-offs will be reported alongside averages.

## Usability and technical verification

A formative usability trial will involve 5-8 consenting students and at least one organiser. Participant tasks will cover registration, profile editing, understanding a suggestion, accepting or declining a team, and project submission. Organiser tasks will cover event creation and resolution of a team issue. Measures will include unaided completion, completion time, errors, requests for help and clarity ratings from 1 to 5. The formative target is at least 80% unaided task completion with no unresolved critical blocker. The small trial will identify usability problems rather than estimate population-wide effectiveness.

Each functional requirement will be checked through positive and negative API tests. Cases include duplicate registration, cross-event access, participant access to organiser APIs, concurrent team confirmations, full teams, impossible constraints, late submissions and judge access to unassigned projects. Interface checks will use the mobile and desktop widths in NFR-02. Defects and regression results will be recorded in YouTrack. Research records will include consent, collection dates, recruitment channels and question-specific response totals.
