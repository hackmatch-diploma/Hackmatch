# Requirements Specification

Functional requirements: organisers should create and manage hackathons, set event rules, review registrations, publish announcements, inspect teams and evaluate submissions. Students should register, maintain skill and interest profiles, indicate preferred roles, review team suggestions and confirm or decline membership. The matching module should apply team-size constraints, consider complementary skills and explain suggestions.

Non-functional requirements: responsive pages, role-based access, secure storage of personal information, clear validation errors, reliable submission handling and understandable explanations of matching criteria. When no feasible team exists under the configured constraints, the system should report the issue rather than silently ignore the rule.

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
| NFR-01 | Role-based access | High | A participant account cannot reach organizer-only APIs; unauthorized requests return 403. |
| NFR-02 | Responsive interface | High | Registration and team screens are usable at 375 px and 1280 px widths without horizontal overflow. |
| NFR-03 | Explainability and invalid constraints | High | Every suggestion shows criteria used; impossible constraints produce a clear warning instead of an invalid team. |
