# HackTeam — Project Proposal and Scope

**Project:** HackTeam — Hackathon Management and Student Team Formation Web System  
**Document Type:** Project Proposal and Scope  
**Related Issue:** HACK-1 — Prepare Project Proposal and Scope  
**Academic Institution:** Astana IT University  
**Program:** Software Engineering  
**Academic Supervisor:** Myrzakerimova Alua  
**Document Status:** Initial Proposal — Subject to Supervisor Review  
**Date:** October 21, 2026

---

## 1. Official Diploma Project Title

**English:**

Development and Evaluation of a Multi-Criteria Method for Student Team Formation with Preliminary Assessment of Team Interaction in a Hackathon Management Web System

**Russian:**

Разработка и исследование метода многокритериального формирования студенческих команд с предварительной оценкой командного взаимодействия в веб-системе управления хакатонами

**Kazakh:**

Хакатондарды басқару веб-жүйесінде командалық өзара әрекеттесуді алдын ала бағалау арқылы студенттік командаларды көпкритерийлі қалыптастыру әдісін әзірлеу және зерттеу

## 2. Project Overview

HackTeam is a proposed web-based platform designed to support the organization and management of student hackathons, with particular emphasis on team formation and preliminary assessment of team interaction.

The project addresses the difficulty students may experience when searching for teammates whose skills, preferred roles, availability, and working expectations are compatible.

The proposed system combines multi-criteria team formation with a preliminary collaboration mechanism called **Trial Sprint**. Before confirming a team, prospective members can participate in a short collaborative activity and review its outcomes.

HackTeam will also provide functionality for hackathon management, participant profiles, team workspaces, task coordination, project submission, and basic evaluation.

The project has two complementary dimensions:

1. **Software development:** designing and implementing a functional web system supporting the hackathon participation lifecycle.
2. **Research and evaluation:** developing and assessing a multi-criteria team formation method and investigating the potential value of preliminary collaboration activities.

The project does not depend on artificial intelligence as its primary mechanism. Its core functionality will be implemented through explicit business rules, structured data, and software algorithms.

## 3. Problem Statement

Student hackathons frequently require participants to form teams under limited time constraints.

Potential teammates may have different technical skills, levels of experience, preferred responsibilities, schedules, and expectations regarding collaboration.

Selecting teammates primarily according to technical expertise may not adequately account for these additional characteristics.

Several challenges motivate this project:

- Difficulty identifying participants with complementary skills and responsibilities.
- Limited information about the availability and working preferences of potential teammates.
- Uncertainty regarding communication and coordination before team formation.
- Lack of structured opportunities to evaluate preliminary collaboration.
- Fragmentation of hackathon registration, team coordination, task management, and submission processes.
- Limited access to verifiable records of previous project participation within a specific platform.

These challenges are treated as research motivations rather than universally established facts. Their prevalence and significance among the intended users must be examined through user research and analysis of existing systems.

**Research problem:**

How can a multi-criteria team formation method, combined with a preliminary collaborative activity, support the formation of student hackathon teams, and how can its usefulness be evaluated against simpler team selection approaches?

## 4. Target Users and Stakeholders

### 4.1 Students and Hackathon Participants

Students represent the primary target user group.

They should be able to:

- Create and maintain participant profiles.
- Specify technical skills, preferred team roles, and availability.
- Discover relevant hackathons.
- Explore suggested teammates.
- Participate in preliminary Trial Sprint activities.
- Join teams and coordinate work.
- Submit hackathon projects.
- Review records of their completed participation activities.

### 4.2 Hackathon Organizers

Organizers should be able to:

- Create and configure hackathon events.
- Publish event descriptions, rules, and deadlines.
- Manage participant registration.
- Review team participation and submitted projects.
- Coordinate event-related activities.
- Access basic event management information.

### 4.3 Mentors

Mentors are potential supporting users who may:

- Review team progress.
- Provide guidance and feedback.
- Support participants during preparation and project development.

Advanced mentor management is outside the initial MVP scope.

### 4.4 Judges and Evaluators

Judges are potential users responsible for reviewing hackathon submissions.

Possible functionality includes:

- Viewing submitted projects.
- Applying predefined evaluation criteria.
- Recording scores and feedback.

Advanced judging workflows may be implemented after the core system has been validated.

### 4.5 Academic Stakeholders

The academic supervisor and project evaluators are stakeholders interested in the system's technical correctness, research methodology, evaluation results, and individual contributions.

## 5. Project Aim

The primary aim of the project is to design, implement, and evaluate a web-based hackathon management system incorporating a multi-criteria method for student team formation and a Trial Sprint mechanism for preliminary assessment of team interaction.

The proposed approach will be investigated to determine whether it provides measurable benefits compared with simpler team formation methods.

## 6. Project Objectives

### 6.1 Research Objectives

**RO1.** Identify relevant difficulties associated with student hackathon team formation through user research and analysis of existing solutions.

**RO2.** Examine scientific literature related to team formation, multi-criteria decision-making, collaboration, and team performance assessment.

**RO3.** Define measurable criteria for evaluating potential team composition.

**RO4.** Develop a transparent multi-criteria matching method suitable for implementation in a web application.

**RO5.** Design the Trial Sprint mechanism and identify observable indicators of preliminary collaboration.

**RO6.** Define baseline approaches and evaluation metrics for comparing team formation methods.

**RO7.** Conduct an evaluation using available participant feedback and system-generated observations, subject to data availability and ethical considerations.

### 6.2 Software Development Objectives

**DO1.** Define functional and non-functional system requirements.

**DO2.** Design the overall application architecture and principal system components.

**DO3.** Implement authentication, authorization, and participant profile management.

**DO4.** Develop hackathon creation, discovery, registration, and management functionality.

**DO5.** Implement multi-criteria teammate recommendation.

**DO6.** Implement Trial Sprint task coordination and basic interaction assessment.

**DO7.** Provide team collaboration and project submission functionality.

**DO8.** Implement a basic Project Reliability Profile based on verifiable in-system participation events.

**DO9.** Verify core functionality through automated and manual testing.

**DO10.** Document the implementation, limitations, and evaluation results.

## 7. Proposed Solution

HackTeam is designed to combine team formation and hackathon management within a unified application.

The proposed participation workflow consists of the following stages:

1. **Participant registration:** A student creates an account and provides necessary profile information.
2. **Hackathon discovery:** The student browses available hackathon events.
3. **Profile configuration:** The student identifies technical skills, preferred roles, experience, availability, and relevant preferences.
4. **Team candidate recommendation:** The system evaluates potential teammate combinations using predefined criteria.
5. **Preliminary team selection:** Participants examine recommendations and express interest in collaborating.
6. **Trial Sprint:** Prospective teammates complete a short, structured collaborative activity.
7. **Team confirmation:** Participants review the preliminary collaboration experience and decide whether to finalize the team.
8. **Hackathon participation:** Confirmed teams coordinate tasks, monitor deadlines, and develop their projects.
9. **Project submission:** Teams submit their project information and deliverables.
10. **Participation history:** The system records eligible completed activities for later reference.

Team formation remains a participant-controlled process. The system provides recommendations and supporting information rather than guaranteeing successful collaboration or automatically imposing final team membership.

## 8. Core Platform Features

### 8.1 Participant Profile Management

Participant profiles will contain information relevant to team formation, subject to appropriate privacy controls.

The proposed attributes include:

- Technical skills.
- Preferred team roles.
- Self-reported experience.
- Availability for collaboration.
- Preferred working arrangements.
- Hackathon participation interests.

The system will allow participants to update their profile information.

### 8.2 Multi-Criteria Team Formation

The platform will evaluate potential teammate combinations using multiple explicitly defined criteria.

Candidate criteria include:

- Skill and role coverage.
- Availability overlap.
- Experience complementarity.
- Alignment of relevant working preferences.

The initial matching method will use a transparent scoring model. The exact definitions, normalization procedures, and weights will be specified during algorithm design.

### 8.3 Trial Sprint

Trial Sprint is a short preliminary collaboration stage performed before the final confirmation of a team.

Potential teammates will work on a small set of tasks intended to provide an opportunity to observe coordination, participation, and task completion.

Trial Sprint results will serve as additional information for participants and as potential observations for research.

### 8.4 Project Reliability Profile

The Project Reliability Profile will summarize verifiable participation activities recorded within HackTeam.

Possible information includes:

- Participation in confirmed teams.
- Completion of assigned tasks.
- Submission of agreed deliverables.
- Recorded completion of activities by agreed deadlines.

The MVP will prioritize factual activity records rather than an opaque numerical reliability or trustworthiness score.

The profile will not be interpreted as an objective measurement of a participant's character or future performance.

### 8.5 Hackathon Management

Organizers will be able to create and manage hackathon events.

The functionality will include event descriptions, participation requirements, registration periods, deadlines, and team participation information.

### 8.6 Team Workspace

Confirmed teams will have access to a shared workspace supporting basic collaboration.

The workspace will provide:

- Team membership information.
- Task creation and assignment.
- Task status tracking.
- Deadlines.
- Shared project information.

### 8.7 Project Submission and Evaluation

Teams will be able to submit project details and relevant deliverables.

A basic review workflow will support the recording of submission information and predefined evaluation results.

More advanced judging and scoring functionality may be developed as an extension.

## 9. Proposed Multi-Criteria Matching Method

The research component will investigate a method for ranking potential teammate combinations using several measurable attributes.

An initial weighted scoring model may be expressed as:

**S = w1 × R + w2 × A + w3 × E + w4 × P**

Where:

- **S** represents the candidate compatibility score.
- **R** represents skill and role coverage.
- **A** represents availability overlap.
- **E** represents experience complementarity.
- **P** represents alignment of relevant working preferences.
- **w1, w2, w3, w4** represent non-negative criterion weights whose sum equals 1.

Individual criteria will be normalized to a comparable scale before aggregation.

This formula is a preliminary design proposal, not a validated matching algorithm.

The exact scoring rules will be defined in a separate algorithm specification.

The research will consider:

1. How each criterion should be measured.
2. How criterion weights should be selected.
3. How missing or uncertain profile information should be handled.
4. How candidate rankings respond to changes in weights.
5. How matching results compare with a skill-only baseline.
6. How understandable and useful participants find the recommendations.

Sensitive personal attributes will not be used as matching criteria.

The method will provide decision support rather than automatically determining whether individuals are capable of working together.

## 10. Trial Sprint Mechanism

The Trial Sprint mechanism is intended to provide prospective teammates with a structured opportunity to collaborate before confirming their final team composition.

### 10.1 Proposed Process

**Stage 1 — Trial Team Formation**

Participants who express mutual interest are grouped into a temporary team.

**Stage 2 — Task Assignment**

The team receives or creates a small collaborative activity with a defined objective and deadline.

**Stage 3 — Collaborative Execution**

Participants coordinate responsibilities and update task progress.

**Stage 4 — Activity Recording**

The system records relevant events, such as task status changes, agreed deadlines, and completion information.

**Stage 5 — Participant Reflection**

Participants may provide structured feedback regarding communication, task coordination, and the usefulness of the trial activity.

**Stage 6 — Team Confirmation**

Participants decide whether to continue as a confirmed team.

### 10.2 Potential Assessment Indicators

The following indicators may be investigated:

- Completion of agreed tasks.
- Completion relative to agreed deadlines.
- Distribution of recorded contributions.
- Participant-reported communication quality.
- Participant-reported satisfaction with preliminary collaboration.
- Willingness to continue working with the proposed team.

These indicators are not assumed to provide a complete or objective measure of team compatibility.

Task outcomes may be influenced by task difficulty, external obligations, individual circumstances, and differences in available time.

### 10.3 Trial Sprint Limitations

A short collaborative activity cannot reliably reproduce every challenge of a full hackathon.

A successful Trial Sprint does not guarantee later team success.

Similarly, incomplete preliminary tasks should not automatically be interpreted as evidence that a participant is unreliable.

The project will therefore treat Trial Sprint as a decision-support and research mechanism, rather than a definitive assessment of individuals.

## 11. Research Hypotheses

The project proposes the following hypotheses for future evaluation.

**H1 — Multi-Criteria Matching**

Considering multiple team formation criteria may lead to higher perceived team suitability than using technical skills alone.

**H2 — Team Composition**

A multi-criteria method may improve selected team composition indicators, such as role coverage and availability overlap, compared with a defined baseline.

**H3 — Trial Sprint**

Preliminary collaborative activities may help participants identify coordination difficulties and make more informed decisions about final team membership.

**H4 — Integrated Workflow**

Combining team formation, preliminary collaboration, and hackathon management within a single system may improve perceived workflow convenience compared with separately managed activities.

These hypotheses have not yet been empirically validated.

Their assessment will depend on the availability of participants, evaluation data, appropriate comparison conditions, and a documented research protocol.

## 12. Preliminary Research and Evaluation Approach

The evaluation will combine functional software verification with an exploratory assessment of the proposed team formation approach.

### 12.1 Research Activities

Planned activities include:

- Literature review.
- Comparative analysis of existing platforms.
- Student interviews or questionnaires.
- Requirements analysis.
- Algorithm implementation.
- Baseline comparison.
- Trial Sprint pilot activities.
- Collection of participant feedback.

No interview findings or experimental results are claimed at the proposal stage.

### 12.2 Baseline Comparison

A skill-only matching method is proposed as an initial comparison baseline.

Where feasible, the same candidate information and team formation constraints will be used for both baseline and multi-criteria methods.

The evaluation will examine measurable differences without assuming that the proposed method must outperform the baseline.

### 12.3 Proposed Metrics

Potential research metrics include:

- Required team role coverage.
- Availability overlap.
- Participant-rated recommendation suitability.
- Trial Sprint task completion rate.
- On-time completion of agreed trial tasks.
- Participant satisfaction with the preliminary collaboration process.
- Perceived usability and transparency of the recommendations.

Technical evaluation may additionally consider:

- Functional test results.
- Authorization and data access controls.
- API correctness.
- Matching algorithm execution time under documented test conditions.
- Application reliability during representative use cases.

The final choice of metrics, instruments, sample size, and analysis methods will be documented in the Verification and Evaluation Plan.

### 12.4 Interpretation of Results

The evaluation will distinguish observed measurements from participant opinions and researcher interpretations.

A small or non-representative sample may limit the generalizability of findings.

The project will report negative, inconclusive, and positive outcomes where applicable.

## 13. Minimum Viable Product (MVP) Scope

The MVP will prioritize the smallest integrated implementation necessary to demonstrate the core workflows and support preliminary evaluation.

### 13.1 Essential MVP Functionality

**MVP-1 — Account Management**

- User registration and authentication.
- Basic role-based access control.
- Participant profile editing.

**MVP-2 — Hackathon Management**

- Hackathon creation and publication.
- Hackathon discovery.
- Basic participant registration.

**MVP-3 — Team Formation**

- Structured participant attributes.
- Multi-criteria candidate scoring.
- Candidate ranking with basic explanations.
- Participant-controlled team confirmation.

**MVP-4 — Trial Sprint**

- Creation of a temporary collaborative activity.
- Task assignment and deadlines.
- Task status updates.
- Basic completion history.
- Structured participant feedback.

**MVP-5 — Team Workspace**

- Team membership overview.
- Basic task management.
- Project information and deadlines.

**MVP-6 — Submission and Participation Records**

- Basic project submission.
- Submission status tracking.
- Factual records of completed in-system activities.

**MVP-7 — Evaluation Support**

- Recording of necessary test and evaluation data.
- Basic comparison of matching methods.
- Automated verification of selected core workflows.

### 13.2 Optional Functionality

The following capabilities are considered extensions rather than essential MVP requirements:

- Advanced judge scoring dashboards.
- Detailed organizer analytics.
- Automated reminder and notification systems.
- Advanced mentor collaboration workflows.
- Integration with external development platforms.
- Real-time communication and video collaboration.
- Sophisticated reputation and reliability scoring.
- AI-assisted recommendations or project analysis.
- Mobile applications.
- Large-scale optimization for simultaneous team formation.

Optional features will be considered only after core functionality and evaluation requirements have been addressed.

## 14. Expected Outcomes

### 14.1 Technical Outcomes

The expected technical outcomes include:

- A functional web-based HackTeam prototype.
- A documented multi-criteria team formation algorithm.
- An implemented Trial Sprint workflow.
- Participant profile and team management components.
- Basic hackathon management and project submission capabilities.
- Technical architecture and API documentation.
- Software verification results.

### 14.2 Research Outcomes

The expected research outcomes include:

- A structured analysis of the team formation problem.
- A review of relevant scientific literature.
- A documented matching method and evaluation criteria.
- A comparison of the proposed method with at least one baseline, where adequate data can be obtained.
- An assessment of Trial Sprint feasibility and participant experience.
- A discussion of limitations and opportunities for future research.

The project does not assume that the proposed method will demonstrate superior performance. Establishing its benefits and limitations is part of the research objective.

### 14.3 Practical Outcomes

The project is expected to provide a prototype that supports student team formation and basic hackathon coordination within one application.

Its potential practical value will be assessed through user feedback and evaluation activities rather than assumed in advance.

## 15. Project Team and Responsibilities

The project will be developed by three Software Engineering students at Astana IT University.

| Team Member | Primary Responsibilities |
|---|---|
| Rakhmetulla Madina | Participant profiles, multi-criteria matching, Trial Sprint design and implementation, research methodology, and algorithm evaluation. |
| Talasbek Kassymbek | Hackathon management, team workspace, task management, deadlines, and project submission functionality. |
| Yergalyuly Daniyar | Backend architecture, authentication, authorization, organizer functionality, project evaluation, analytics, and notifications. |

**Academic Supervisor:** Myrzakerimova Alua

The division above identifies primary ownership rather than exclusive responsibility.

Shared activities include requirements review, integration, testing, documentation, design decisions, and preparation for academic evaluation.

The team will use GitHub for version control and Pull Request reviews, and YouTrack for task tracking.

## 16. Assumptions, Constraints, and Limitations

### 16.1 Project Assumptions

- Students will be willing to provide limited profile information relevant to team formation.
- Some participants will be available for interviews, surveys, or pilot testing.
- Preliminary collaboration tasks can be designed within a manageable scope.
- The academic team can implement and evaluate a functional prototype within the available project period.

These assumptions require verification during project development.

### 16.2 Technical Constraints

- Development resources are limited to a three-person student team.
- The implementation must remain feasible within the academic schedule.
- Matching criteria depend on the quality and completeness of participant data.
- Evaluation outcomes may be affected by sample size and participation levels.
- The initial application will focus on web functionality rather than native mobile clients.

### 16.3 Research Limitations

- Self-reported skills may not accurately represent actual expertise.
- Matching scores cannot fully capture interpersonal compatibility.
- Trial Sprint observations cover only a limited collaboration period.
- Short-term observations may not predict long-term performance.
- Participant surveys may be affected by subjective interpretation and response bias.
- Results from a student pilot may not generalize to other populations.

### 16.4 Privacy and Ethical Considerations

The system will apply data minimization and access controls appropriate to the prototype.

Research participation and the use of participant feedback will be based on informed consent.

Personal information will not be publicly exposed merely because it is relevant to a matching criterion.

Trial Sprint feedback and participation records will not be presented as definitive judgments about a person's reliability or professional competence.

The team will document the collection, storage, access, and retention of relevant information before conducting empirical research.

## 17. Preliminary Risks and Mitigation

| Risk | Potential Impact | Proposed Mitigation |
|---|---|---|
| Insufficient research participants | Limited evaluation evidence | Recruit volunteers early and document sample limitations. |
| Incomplete participant profiles | Reduced matching quality | Validate required information and handle missing data explicitly. |
| Excessive feature scope | Delayed implementation | Prioritize MVP features and defer non-essential functionality. |
| Subjective collaboration feedback | Biased evaluation | Combine feedback with clearly defined observable indicators. |
| Integration difficulties | Delays and software defects | Define component interfaces and integrate incrementally. |
| Privacy concerns | Reduced trust or inappropriate disclosure | Apply access restrictions, data minimization, and consent procedures. |
| Unclear matching criteria | Poor reproducibility | Document formulas, normalization, weights, and baseline methods. |

A more detailed risk register will be maintained separately as part of project management documentation.

## 18. Scope Boundaries and Deliverables

### 18.1 In Scope

- Analysis of the student hackathon team formation problem.
- Design and implementation of the HackTeam web prototype.
- Multi-criteria teammate recommendation.
- Preliminary team interaction assessment through Trial Sprint.
- Core hackathon and team management workflows.
- Functional verification.
- Exploratory research evaluation and documentation.

### 18.2 Out of Scope

- Guaranteed prediction of team success.
- Psychological profiling of participants.
- Automated judgments about personal character.
- Enterprise-level event management.
- Production-scale infrastructure requirements.
- Mandatory AI-based matching.
- Native mobile applications in the initial release.

### 18.3 Planned Academic Deliverables

The project documentation and development process are expected to produce:

1. Project Proposal and Scope.
2. Evidence of User Research.
3. Literature Review.
4. Existing Systems Comparison.
5. Technology Comparison.
6. Functional and Non-Functional Requirements.
7. System Context, Use Case, and Component Diagrams.
8. UX Prototype.
9. Verification and Evaluation Plan.
10. Project Management and Risk Assessment.
11. Supervisor Feedback.
12. Subsequent implementation, testing, and evaluation artifacts.

The initial pre-defense focuses on the proposed solution, research foundation, planning, and design. A completed production application is not required at this stage.

## 19. Conclusion

HackTeam proposes an integrated approach to student hackathon participation by combining web-based event management, multi-criteria team formation, and preliminary collaboration assessment.

The central research contribution is the development and evaluation of a transparent team formation method supported by a Trial Sprint mechanism.

The project aims to investigate whether considering multiple participant characteristics and providing an opportunity for preliminary collaboration can support more informed team formation decisions.

The expected contribution is both practical and academic: a working software prototype and an evidence-based assessment of the proposed approach.

The project's success will be evaluated according to its documented requirements, implementation quality, research methodology, and observed results, rather than assumptions about the superiority of the proposed solution.

---

**Document Status:** Initial draft for academic supervisor review. Research findings, final technical decisions, and evaluation results will be added or revised as the project progresses.
