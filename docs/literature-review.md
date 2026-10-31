# Literature Review

The literature review covers twelve academic publications about team formation, student collaboration and hackathon coordination. The studies differ in their settings and methods, so their findings should not be treated as directly interchangeable. Hastings et al. (2023) studied instructors' use of algorithmic team formation and showed why criteria and their effects should be understandable. Forshaw et al. (2026) examined fairness in student group formation and the trade-offs involved in different grouping approaches. Agarwal et al. (2022) explored genetic optimisation for balancing student competencies. Singh et al. (2025) used multi-criteria optimization to study team diversity and potential conflict. These studies inform the design of a matching algorithm, but technical balance does not automatically establish successful collaboration. Wu et al. (2026) considered perceived pressure in heterogeneous student grouping, while Xu et al. (2026) examined personality and collaboration in design education. Their settings differ from short student hackathons. Vinella et al. (2022) compared bottom-up, top-down and hybrid team formation in simulations, suggesting that participant choice deserves attention. Gomez-Zara et al. (2019) investigated online collaborator discovery and the role of existing social connections. Kohli et al. (2023) studied opt-in study-group matching in a large remote course. Jadhav et al. (2026) presented ResearchConnect, integrating profiles and research team suggestions. Hevenstone et al. (2026) discussed self-assigned and algorithmically assigned hackathon teams, including the possibility of structured changes. Mendes et al. (2022) examined collaboration problems in online hackathons. Research gap: existing studies and tools address algorithmic grouping, collaborator discovery or event coordination separately. This project will investigate how transparent multi-criteria suggestions can be combined with a complete student hackathon workflow and evaluated through measurable tasks. The project does not claim that multi-criteria grouping itself is new.

| Author & Year | Topic / Focus | Methodology | Relevance to Project |
| --- | --- | --- | --- |
| Hastings et al. (2023) | Instructor algorithmic team grouping | Survey of 77 instructors and 21 interviews | Supports transparent grouping criteria and understandable controls |
| Forshaw et al. (2026) | Fairness in student group formation | Review of 262 papers, 18 tools, interviews and focus groups | Frames fairness trade-offs and allocation constraints |
| Agarwal et al. (2022) | Balancing engineering student competencies | Vector Evaluated Genetic Algorithm; ~1,300 students | Informs weighted skill and role balancing |
| Singh et al. (2025) | Multicriteria team formation | Clustering and multicriteria integer programming; simulated profiles | Informs explicit role and diversity constraints |
| Wu et al. (2026) | Pressure in heterogeneous groups | 81-student class; NSGA-II grouping analysis | Highlights social effects beyond technical matching |
| Xu et al. (2026) | Personality in design student teams | Regression analysis; 50 students in 25 two-person teams | Motivates measuring collaboration separately from scores |
| Vinella et al. (2022) | Worker-centered team formation | Agent-based comparison of bottom-up, top-down and hybrid groups | Supports opt-in choice and hybrid matching |
| Gómez-Zará et al. (2019) | Online collaborator discovery | Field study; 43 participants and eight teams | Addresses discovery and existing social connections |
| Kohli et al. (2023) | Inclusive study group matching | Opt-in matching study in a large remote course | Informs opt-in matching for solo participants |
| Jadhav et al. (2026) | ResearchConnect profiles and ideation | Profile clustering; 250 research summaries | Related profile-based recommendations outside hackathons |
| Hevenstone et al. (2026) | Diversity and participant involvement | Comparison of two civic hackathons | Motivates participant agency and adjustments |
| Mendes et al. (2022) | Virtual hackathon coordination | Study of ten teams across four online hackathons | Motivates unified event and collaboration workflows |

## Empirical studies and experiments

The reviewed evidence includes computational experiments using real student data, a deployed matching system, observational field studies and a simulation experiment. Their methods, findings and limitations inform different parts of the proposed design.

## Agarwal and colleagues 2022   computational experiment with student data

Agarwal et al. (2022) used self-reported programming, spreadsheet and general computer competencies from approximately 1,300 first-year engineering students to form teams with a Vector Evaluated Genetic Algorithm. The paper compared algorithmic and manual allocations and reported a more uniform distribution of team-average skills. In one 47-student example, 100 generations with 1,500 candidate configurations took about 18 seconds. The algorithm prioritised programming when it could not minimise all objectives simultaneously. This result demonstrates a practical allocation method, but does not establish that the generated teams collaborated or learned better; evaluation of team effectiveness remained future work. For this project, the study motivates comparison against manual allocation, explicit reporting of runtime and measurement of trade-offs between criteria.

## Kohli and colleagues 2023   deployed study group matching

Method and setting. The authors trialled opt-in software matching in an introductory engineering and computer science course with more than 1,000 students during remote teaching. Students could request reassignment. Results. Underrepresented students were more likely to request matching; matched students reported comparable group experiences across backgrounds, and positive group experiences were associated with exam outcomes. Limitation. This was a course deployment, not a randomised student hackathon experiment; the associations do not prove a causal benefit of our proposed algorithm. The findings support voluntary participation, reassignment and separate measures of comfort and activity in HackMatch.

## Mendes and colleagues 2022   four real online hackathons

Method and sample. A multiple-case study examined 10 teams across four online hackathons on two continents, using 27 interviews. Results. Teams combined synchronous and asynchronous tools; responsibilities were often self-selected by skill or interest. Networking and informal mentor access decreased, while multiple tools created technical and information burdens. Limitation. This observational qualitative study did not compare matching algorithms or quantify a causal effect of a central platform. These findings inform the central event workflow, visible team roles and end-to-end evaluation in HackMatch.

## Hastings and colleagues 2023   instructor use of grouping algorithms

Method and sample. The researchers surveyed 77 instructors and conducted 21 follow-up interviews about criteria-based grouping, including CATME. Results. Instructors checked proposed teams against educational goals but sometimes struggled to translate those goals into tool settings. Student input was often absent. Limitation. The work describes instructor practice rather than experimentally proving higher team performance. These findings support visible matching criteria, organiser review and participant feedback in HackMatch.

## Vinella and colleagues 2022   simulation experiment

Method. The authors simulated bottom-up, top-down and hybrid team formation. Results. Self-organisation favoured the strongest teams, while the hybrid model better protected the weakest teams; mean quality did not differ significantly across models. Limitation. Outcomes were generated by an agent model and its assumptions, not observed in a live hackathon. The HackMatch evaluation therefore includes minimum and average role coverage and unassigned participants, alongside the strongest team outcomes.

[References](references.md)
