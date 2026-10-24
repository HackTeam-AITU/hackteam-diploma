# HackTeam — Diploma Project

**Stage:** First pre-defense — research, requirements, architecture, and UX prototyping  
**University:** Astana IT University  
**Program:** Software Engineering  
**Academic supervisor:** Myrzakerimova Alua Bauyrzhankyzy  
**Status as of 24 October 2026:** Main pre-defense documentation is present. Software implementation and experimental validation remain future work.

## Project overview

HackTeam is a proposed web-based hackathon management and student team formation platform. It supports finding teammates, organizing events, managing team work, and submitting projects. Its research focus is a transparent **multi-criteria team formation method** with an optional **Trial Sprint** for observing initial team collaboration before final membership confirmation.

The project does not assume that recommendations or Trial Sprint will improve real-world team outcomes. These hypotheses must be evaluated using appropriate baselines, recorded data, and a clearly stated methodology.

## Official diploma project title

**English:** Development and Evaluation of a Multi-Criteria Method for Student Team Formation with Preliminary Assessment of Team Interaction in a Hackathon Management Web System

**Russian:** Разработка и исследование метода многокритериального формирования студенческих команд с предварительной оценкой командного взаимодействия в веб-системе управления хакатонами

**Kazakh:** Хакатондарды басқару веб-жүйесінде командалық өзара әрекеттесуді алдын ала бағалау арқылы студенттік командаларды көпкритерийлі қалыптастыру әдісін әзірлеу және зерттеу

## Problem and users

Student teams may struggle with incomplete information about skills, required roles, availability, commitment, and collaboration preferences. HackTeam proposes a more structured team discovery and decision process, while retaining participant choice and privacy protections.

**Primary users:** hackathon participants, student team leaders, and hackathon organizers. Mentors, judges, and administrators are additional roles; advanced workflows may be deferred from the initial MVP.

## Planned core functionality

- Registration, authentication, profile and role management.
- Hackathon discovery, event information, registration, and organizer tools.
- Team posts, invitations, membership, and team confirmation.
- Transparent candidate eligibility checks and multi-criteria matching with explanations.
- Optional Trial Sprint: limited shared tasks, deadlines, reflection, and voluntary final team decision.
- Basic team workspace, task management, and project submission.
- Access control, data integrity, and support for planned testing and research evaluation.

**Optional/future:** comprehensive reliability scoring, detailed analytics, advanced judging, real-time communication, external integrations, AI-based recommendations, and native mobile applications. None is required to demonstrate the core research approach.

## Scientific direction and evaluation

The preliminary method first applies mandatory eligibility constraints, then ranks eligible candidates using normalized criteria and documented weights. The existing proposed formula is:

`S = w1 × R + w2 × A + w3 × E + w4 × P`

Here `R` denotes skill/role coverage; `A`, availability overlap; `E`, relevant experience complementarity; and `P`, alignment of working preferences. The proposed weights are non-negative and total one. The criteria definitions and weights require design validation; scores do not predict someone's character or guarantee success.

The evaluation plan distinguishes three approaches:

| Approach | Description | Intended comparison |
|---|---|---|
| B0 | Skill-based matching | Reference baseline |
| B1 | Multi-criteria matching | Value and limitations of additional matching criteria |
| B2 | The same B1 recommendations, followed by optional Trial Sprint | Potential decision-support value of preliminary collaboration |

Planned measures include role coverage, availability overlap, matching runtime, changes in team selection, participant feedback, and limits of observed collaboration. Initial user research consists of **three exploratory student interviews**, not a representative trial or experimental validation.

See [Research Design and MVP Refinements](docs/research-design-refinements.md) and [Verification and Evaluation Plan](docs/evaluation-plan.md).

## Proposed technology and architecture

The [Technology Comparison](docs/technology-comparison.md) supports the following **preliminary** choices:

| Area | Proposed approach |
|---|---|
| Backend | Java + Spring Boot |
| Database | PostgreSQL |
| API | REST/JSON; OpenAPI for documentation |
| Architecture | Modular monolith with separated application modules |
| Frontend | React + TypeScript under consideration; not separately evaluated in the technology comparison |
| Collaboration | GitHub, feature branches, Pull Requests, YouTrack |

These choices describe the intended implementation; the project does not currently claim a functioning production deployment.

## Team and responsibilities

- **Rakhmetulla Madina Bauyrzhankyzy:** participant profiles, matching method, Trial Sprint, and research evaluation.
- **Talasbek Kassymbek Arystanbekuly:** hackathon management, team workspace, task coordination, UX prototyping, and project submission.
- **Yergalyuly Daniyar:** backend architecture, security, organizer functionality, integration, analytics, and technical planning.

Cross-module integration, verification, and academic documentation are shared responsibilities. Contributions are traceable through issue ownership, commits, reviews, and merged Pull Requests.

## First pre-defense documentation

The following documentation is available or prepared for inclusion in the `docs/` directory:

| Area | Document |
|---|---|
| Research problem, objectives and scope | [Project Proposal](docs/project-proposal.md) |
| Scientific background | [Literature Review](docs/literature-review.md) |
| Three student interviews and limitations | [User Research](docs/user-research.md) |
| Existing platforms and differentiation | [Competitor Analysis](docs/competitor-analysis.md) |
| Backend, database and API comparison | [Technology Comparison](docs/technology-comparison.md) |
| Functional/non-functional requirements | [Requirements Specification](docs/requirements.md) |
| Context, use case and component architecture | [System Architecture](docs/architecture.md) and [editable diagrams](diagrams/README.md) |
| UX/UI prototype, desktop and mobile views | [UX/UI Prototype](docs/ux-prototype.md) · [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=5-2) |
| Verification and research protocol | [Evaluation Plan](docs/evaluation-plan.md) |
| Roadmap, dependencies, responsibilities and risks | [Project Management and Risks](docs/project-management-risks.md) |
| Reviewed feedback and response | [Supervisor Feedback](docs/supervisor-feedback.md) |
| Specific design refinements and pending validation | [Research Design Refinements](docs/research-design-refinements.md) |

The architecture folder includes editable `.drawio` source files and PNG exports. The Figma prototype demonstrates planned interactions; it is not the implemented application.

## Current progress and limitations

**Documented:** literature, proposal, three interviews, competitor and technology analysis, software requirements, architecture diagrams, interactive UX/UI prototype, planned test scenarios, evaluation methodology, milestone and risk register. The supervisor-feedback wording has been agreed to in principle, according to the project team; the review summary and follow-up design refinements are documented separately.

**Not yet claimed complete:** application backend/frontend implementation, integrated workflows, passing test results, actual Trial Sprint pilot, research participant outcome measurements, and proof of improved team quality. Proposed scheduling and scoring details require implementation and validation.

## Project management and review workflow

**YouTrack:** https://hackteam-aitu-2027.youtrack.cloud/projects/HACK  
**GitHub:** https://github.com/HackTeam-AITU/hackteam-diploma

Each substantial change should be associated with a YouTrack issue, prepared in a dedicated branch, submitted via a Pull Request, and reviewed before merging to `main`. All implementation and research results will be reported with their actual evidence rather than inferred from a plan.

## Planned next stages

1. Confirm MVP scope, API contracts, data model, and main integration checkpoints.
2. Implement secure account and participant functionality plus hackathon and team basics.
3. Implement explainable matching and a reproducible skill-based baseline.
4. Implement optional Trial Sprint and core team workspace/submission flows.
5. Run integration/security tests and real UX walkthroughs.
6. Conduct research comparisons and any ethically approved participant pilot.
7. Document limitations, completed work, and final academic outcomes.

For milestones and risk ownership, see [Project Management and Risk Assessment](docs/project-management-risks.md).
