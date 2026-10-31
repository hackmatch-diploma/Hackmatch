# Project Management and Risks

Project documentation and future application components are maintained in the Hackmatch repository. The project README links to the YouTrack board.

Project organisation: https://github.com/orgs/hackmatch-diploma/repositories

Documentation and project overview: https://github.com/hackmatch-diploma/Hackmatch



YouTrack: https://hackmatch.youtrack.cloud/agiles/204-0/current

The development workflow links work items to an owner, acceptance criteria, deadline and relevant code or documentation changes. Feature branches and pull requests provide review points; release tags will identify submitted versions.

## Risk assessment approach

Likelihood and impact are rated from 1 (low) to 3 (high). Their product determines priority: 6 to 9 is high, 3 to 4 medium, and 1 to 2 low. The ratings are initial estimates. Each risk has an owner, an observable trigger, preventive measures and a contingency response. Risks will be reviewed weekly and when a trigger occurs.

## R1 Insufficient or inconsistent research data

Priority: 3 x 2 = 6 high. Owner: Elkham Mamedov. A small exploratory sample, non-participants and contradictory answers may produce misleading requirements. Trigger: inconsistent experience answers remain unresolved or no organiser is interviewed.

Mitigation: Validate responses with consent; recruit experienced participants and conduct 3-5 user discussions. Record the recruitment method and exclusions.

Contingency: Report preliminary results only; avoid subgroup claims; prioritise requirements confirmed by an organiser.

## R2 Infeasible team constraints

Priority: 3 x 3 = 9 high. Owner: Ilnur Saipiyev. Team size, availability and role demand may conflict with the available pool. Trigger: the feasibility check cannot place all eligible participants.

Mitigation: Separate mandatory rules from preferences; validate role supply and size arithmetic before matching. Test small and odd participant pools.

Contingency: Leave affected participants explicitly unassigned and show the cause; let the organiser change optional criteria with confirmation. Never silently violate a mandatory rule.

## R3 Incorrect or incomplete profiles

Priority: 3 x 2 = 6 high. Owner: Ilnur Saipiyev. Self-reported skill levels and missing availability may generate misleading recommendations. Trigger: required profile fields are missing or users reject suggestions because the data is wrong.

Mitigation: Use controlled skill labels, explicit unknown values, required availability and a profile confirmation step. Explain which fields drive the suggestion.

Contingency: Exclude incomplete profiles from automatic allocation, request corrections and offer manual team discovery.

## R4 Poor matching outcomes or low trust

Priority: 2 x 3 = 6 high. Owner: Ilnur Saipiyev. Optimising one weighted score may leave weak teams or produce unwanted assignments. Trigger: low acceptance, reduced minimum role coverage or complaints about explanations.

Mitigation: Keep matching opt-in; expose reasons; compare minimum and mean coverage and acceptance against the baseline; test alternative weights.

Contingency: Revert to the baseline or organiser-assisted allocation; retain participant confirmation and reassignment.

## R5 Authorisation failure or data exposure

Priority: 2 x 3 = 6 high. Owner: Ilnur Saipiyev. Missing event-level checks may expose profiles or permit score and team changes by the wrong user. Trigger: a cross-role or cross-event negative test succeeds.

Mitigation: Enforce access checks on every endpoint; minimise public profile fields; test judge assignments; keep secrets outside Git.

Contingency: Block the affected endpoint, revoke exposed credentials when applicable, assess affected records and repair before reopening access.

## R6 Concurrent membership or deadline errors

Priority: 2 x 3 = 6 high. Owner: Ilnur Saipiyev. Simultaneous invitations or last-minute submissions may create duplicate membership, overfull teams or disputed deadlines. Trigger: a concurrency or deadline boundary test fails.

Mitigation: Use transactions and membership uniqueness rules, server-side time checks and repeatable integration tests. Display event timezone and submission confirmation.

Contingency: Suspend the affected workflow; reconcile records from the audit trail and backups; let the organiser resolve affected cases with a recorded decision.

## R7 Integration and schedule overrun

Priority: 3 x 2 = 6 high. Owner: Elkham Mamedov. A three-person team may lose time when frontend and backend contracts diverge or matching expands in scope. Trigger: a core milestone slips by more than one week or an API contract remains unresolved.

Mitigation: Agree versioned API contracts; integrate one end-to-end flow early; implement the baseline before optimisation; review dependencies weekly.

Contingency: Freeze optional features, deliver the core registration-to-submission flow and revise remaining milestones with the supervisor.

## R8 Deployment or database failure

Priority: 2 x 3 = 6 high. Owner: Ilnur Saipiyev. Hosting outages, failed migrations or missing backups may block the demonstration or lose submissions. Trigger: health checks fail, a migration fails or a backup cannot be restored.

Mitigation: Use a reproducible deployment, migration checks, health monitoring and database backups; rehearse a restore before the demonstration.

Contingency: Restore the last verified backup or run the prepared local demonstration with anonymised data; record the outage and verify integrity before resuming.

## Milestones

The project proceeds through four milestones: validated requirements and user evidence; architecture, API contracts and interface design; an integrated registration-to-submission workflow with baseline matching; and evaluation, defect correction and release preparation. Dependencies include access to user representatives, consented profile data, an available deployment environment and supervisor review.
