# Existing system comparison

Devpost provides hackathon listings, project submissions and participant discovery. Its participant documentation describes ways to find teammates, but does not establish a weighted automatic allocation process based on skills, interests and availability. Devpost for Teams allows projects to advertise roles and participants to request membership.

Devfolio supports event participation and team creation or joining, including invitation-based workflows. The reviewed guidance does not establish multi-criteria automatic grouping. CATME Team-Maker collects student survey information and allows instructors to configure grouping criteria, including skills and schedules. However, it focuses on educational team allocation rather than full hackathon administration. gruepr also supports survey-based team formation, constraints and manual adjustments, but its main focus is educational grouping.

My Dream Team, studied by Gomez-Zara et al. (2019), explored profile-based collaborator discovery. ResearchConnect (Jadhav et al., 2026) integrates researcher profiles, clustering and ideation, but its evaluation does not demonstrate deployment in a live student hackathon.

The proposed system will combine event registration, profile-based suggestions, participant confirmation, organiser adjustments, announcements and submissions. These functions are planned rather than completed. Its usefulness must be evaluated against the existing alternatives and a simpler manual baseline.

| Comparison Criteria | Devpost | Devfolio | CATME | gruepr | Proposed System |
| --- | --- | --- | --- | --- | --- |
| Hackathon event workflow | Yes | Yes | No | No | Planned |
| Participant skill profiles | Basic | Basic | Survey-based | Survey-based | Planned |
| Multi-criteria grouping | Not established | Not established | Yes | Yes | Planned |
| Weighted skill matching | Not established | Not established | Configurable criteria | Configurable criteria | Planned |
| Explainable suggestions | Not established | Not established | Instructor settings | Organizer settings | Planned |
| Solo registrant support | Discovery/manual | Join/invite | Instructor-led | Instructor-led | Planned |
| Manual adjustment | Team management | Team management | Instructor controls | Instructor controls | Planned |
| Project submissions | Yes | Yes | No | No | Planned |

## Justification for developing the proposed system

The proposed project addresses a specific combination of needs in student hackathons: managing the event workflow and helping participants form teams while preserving their freedom of choice. In the reviewed comparison, hackathon platforms mainly support event participation and project submission, whereas educational team-formation tools focus on allocating students to groups. The proposed system brings these functions into one workflow: participant profiles provide information for team suggestions, accepted suggestions become event teams, and those teams proceed to project submission and judging.

Our preliminary survey provides a local reason for this design. Of the 13 consenting respondents, seven selected registration and participant profiles as useful features, five selected judging criteria and feedback, and four selected teammate search and suggestions. Six respondents preferred choosing teammates themselves, while three preferred receiving suggestions and making the final decision personally. These findings support a platform that offers optional recommendations alongside manual team formation. However, the small sample and inconsistent answers require further validation with participants and organisers.

The distinctive contribution is the integration of explainable, multi-criteria team recommendations into the complete student hackathon workflow. Recommendations will consider complementary skills, preferred roles, interests and availability, explain the criteria used, and allow participants to accept or decline. Organisers will be able to review allocations and resolve cases where team constraints cannot be satisfied.

The development involves more than combining registration forms and dashboards. It requires implementing and evaluating a matching strategy, detecting infeasible constraints, maintaining consistent team membership during simultaneous invitations, and enforcing permissions across participants, organisers and judges. Separate forms, spreadsheets and messaging tools do not automatically enforce these connected rules. A dedicated implementation provides a consistent data model and lets the team compare matching strategies under the same conditions.

A dedicated implementation is justified by the need to connect event-scoped profiles, team constraints, participant decisions and submission permissions in a consistent data model. A configurable matching module also permits a controlled comparison of rule-based and weighted recommendations. The evaluation will compare the complete workflow with manual administration and measure whether this integration reduces effort while maintaining valid teams and participant choice.

[References](references.md)
