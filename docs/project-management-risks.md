# HackTeam — Project Management, Milestones and Risk Assessment

**Related Issue:** HACK-11  
**Document Status:** Draft — Pending Team and Supervisor Review  
**Project:** HackTeam Diploma Project  
**Prepared by:** Yergalyuly Daniyar  
**University:** Astana IT University  
**Date:** October 24, 2026

## 1. Introduction

### 1.1 Purpose

This document defines the preliminary project management approach for HackTeam, including development milestones, team responsibilities, dependencies, potential risks, and mitigation strategies.

The main objective is to establish a realistic and traceable plan for implementing and evaluating the HackTeam platform within the academic schedule.

### 1.2 Project Overview

HackTeam is a proposed web-based platform for managing student hackathons and supporting team formation through a multi-criteria matching method and a preliminary collaboration mechanism called Trial Sprint.

The core functionality includes participant profiles, hackathon management, team formation, Trial Sprint, team workspaces, and project submission.

The platform will be developed by a team of three Software Engineering students.

## 2. Project Team and Responsibilities

| Team Member | Primary Responsibilities |
|---|---|
| Rakhmetulla Madina | Participant profiles, Multi-Criteria Matching, Trial Sprint, research methodology, and matching evaluation |
| Talasbek Kassymbek | Hackathon management, team workspace, task management, deadlines, UX prototyping, and project submission |
| Yergalyuly Daniyar | Backend architecture, authentication, authorization, database integration, organizer functionality, evaluation, analytics, and system integration |

**Academic Supervisor:** Myrzakerimova Alua

Each member is primarily responsible for their assigned components. Integration, system testing, architectural reviews, and final defense preparation will be performed collaboratively.

## 3. Project Development Milestones

The project is divided into several major development stages.

### 3.1 Milestone Overview

| ID | Milestone | Main Deliverables | Primary Owner | Completion Criteria |
|---|---|---|---|---|
| M1 | Project Research and Planning | Proposal, literature review, user research, competitor analysis | All members | Required research documents reviewed |
| M2 | Requirements and Architecture | Requirements, technology comparison, architectural diagrams | Madina, Daniyar | Requirements and architectural decisions documented |
| M3 | UX/UI Prototyping | Interactive prototype and user flows | Kassymbek | Essential user journeys demonstrated |
| M4 | Backend Foundation | Authentication, authorization, database schema, core API | Daniyar | Core endpoints pass initial integration tests |
| M5 | Participant and Team Formation | Profiles, invitations, team management, matching method | Madina, Kassymbek | Team formation scenarios satisfy defined acceptance criteria |
| M6 | Trial Sprint Implementation | Temporary team activities, tasks, deadlines, result recording | Madina | Main Trial Sprint workflow can be completed |
| M7 | Hackathon Management | Event management, team workspace, project submission | Kassymbek | Main hackathon participation workflow operates correctly |
| M8 | System Integration and Testing | Integrated platform, automated tests, defect reports | All members | Critical workflows pass agreed tests |
| M9 | Research Evaluation | Baseline comparison, pilot results, analysis | Madina with team support | Evaluation methods executed and limitations documented |
| M10 | Final Documentation and Defense | Technical report, final demonstration, defense materials | All members | Required academic deliverables prepared |

### 3.2 Current Progress

As of October 24, 2026, the repository contains the following research and design materials:

- Project Proposal and Scope
- Literature Review
- User Research
- Existing Platform Comparison
- Technology Comparison
- System Requirements
- System Architecture and Diagrams
- Verification and Evaluation Plan
- UX/UI Prototype Documentation

These materials support the initial pre-defense stage. Their presence in the repository does not replace supervisor approval or final academic evaluation.

Application implementation, system integration, and experimental evaluation are future activities.

### 3.3 Preliminary Development Roadmap

The following schedule describes a proposed sequence of work rather than officially approved university deadlines.

| Phase | Planned Activities | Dependencies |
|---|---|---|
| Phase 1 | Finalize requirements and architectural decisions | Supervisor and team review |
| Phase 2 | Implement backend foundation and database schema | Approved core requirements |
| Phase 3 | Develop participant profiles and hackathon management | Authentication and data model |
| Phase 4 | Implement team formation and multi-criteria matching | Participant profiles and team data |
| Phase 5 | Implement Trial Sprint and team workspace | Team membership and task management |
| Phase 6 | Integrate project submission and evaluation | Hackathon and team workflows |
| Phase 7 | Conduct system and security testing | Integrated functional modules |
| Phase 8 | Conduct research evaluation | Working matching and Trial Sprint mechanisms |
| Phase 9 | Finalize documentation and defense materials | Completed testing and evaluation |

Exact dates and stage durations must be coordinated with the academic supervisor and the university calendar.

## 4. Task Dependencies

Several components depend on the successful completion of earlier modules.

### 4.1 Core Dependencies

**Authentication and Authorization**

Must be implemented before protected user operations and administrative functionality can be reliably tested.

**Participant Profiles**

Required before multi-criteria matching can use participant skills, roles, and availability.

**Hackathon Management**

Required to associate registrations, teams, and project submissions with specific hackathons.

**Team Management**

Required before Trial Sprint activities can be assigned to temporary or confirmed team members.

**Trial Sprint**

Depends on participant identity, team collaboration data, task management, and result recording.

**Project Submission**

Depends on hackathon information, deadlines, team membership, and authorization rules.

### 4.2 Integration Strategy

The team will define shared data structures and API contracts before independently implementing closely related modules.

Integration tests will verify interactions between components.

Shared interface changes will be reviewed through GitHub Pull Requests.

## 5. Risk Assessment Methodology

The project uses a qualitative risk assessment approach.

Each risk is evaluated by:

- **Likelihood:** Low, Medium, or High.
- **Impact:** Low, Medium, or High.
- **Priority:** Based on the combined likelihood and impact.

These ratings are preliminary team judgments, not experimentally measured probabilities.

## 6. Project Risk Register

| ID | Risk | Likelihood | Impact | Priority | Mitigation Strategy | Owner |
|---|---|---|---|---|---|---|
| R1 | Insufficient development time | High | High | Critical | Prioritize MVP functionality and defer optional features | All members |
| R2 | Integration conflicts between modules | Medium | High | High | Define API contracts early and perform regular integration testing | Daniyar |
| R3 | Backend or database design complexity | Medium | High | High | Use modular architecture, review schema design, and implement automated tests | Daniyar |
| R4 | Inaccurate or incomplete matching data | High | Medium | High | Validate user inputs, handle missing attributes, and document algorithm limitations | Madina |
| R5 | Insufficient participants for research evaluation | Medium | High | High | Recruit participants early and define a smaller pilot study if necessary | Madina |
| R6 | Trial Sprint fails to demonstrate measurable improvement | Medium | Medium | Medium | Report results objectively, including negative or inconclusive outcomes | Madina |
| R7 | Unauthorized access to participant data | Medium | High | High | Apply server-side authorization, privacy controls, and security testing | Daniyar |
| R8 | Unclear or changing requirements | Medium | Medium | Medium | Review requirements with the team and supervisor before major implementation decisions | All members |
| R9 | Delays in task completion or communication | Medium | High | High | Use YouTrack, clear ownership, regular progress updates, and peer reviews | All members |
| R10 | UX complexity reduces usability | Medium | Medium | Medium | Test key user journeys and simplify unnecessary interactions | Kassymbek |

### 6.1 Risk Response Strategy

High-priority risks will be reviewed regularly during project development.

If development falls behind schedule, optional functionality will be postponed before essential features are removed.

If participant recruitment is insufficient, the research will report the limitations of the available sample rather than inventing data or claiming unsupported conclusions.

If integration problems occur, the team will prioritize restoring the main end-to-end workflow before expanding functionality.

## 7. Project Management Tools

### 7.1 GitHub

GitHub is used for version control, documentation, source code, and peer review.

Repository:

https://github.com/HackTeam-AITU/hackteam-diploma

Each major task is developed in a separate branch.

Changes are submitted through Pull Requests and reviewed by another team member before merging into `main`.

### 7.2 YouTrack

YouTrack is used for task planning, assignment, prioritization, deadlines, and progress tracking.

Project:

https://hackteam-aitu-2027.youtrack.cloud/projects/HACK

Tasks are tracked through the following workflow:

**Queue → In Progress → Review → Done**

Testing stages may be used where applicable.

A task is marked as completed only after the relevant acceptance criteria have been satisfied.

### 7.3 Team Collaboration

The team will coordinate technical decisions, document important changes, and review each other's deliverables.

Any significant change affecting multiple modules should be communicated before implementation.

GitHub Pull Requests will provide a traceable record of reviews and revisions.

## 8. Supervisor Feedback and Project Control

The academic supervisor will review significant deliverables and provide feedback on the proposed methods, architecture, and research approach.

Feedback will be documented through:

- Date of consultation
- Reviewed deliverable
- Supervisor comments
- Required changes
- Implemented revisions
- Reference to the updated document or Pull Request

Only actual feedback received from the supervisor will be recorded as completed review activity.

The frequency of consultations and future milestones will be confirmed with the supervisor.

## 9. Success Criteria

The project will be evaluated against the following intended outcomes:

1. The essential HackTeam workflows are implemented.
2. Functional requirements have verifiable acceptance criteria.
3. Security and access-control requirements are tested.
4. The multi-criteria matching method is documented and implemented.
5. Trial Sprint supports a complete preliminary collaboration workflow.
6. The platform supports hackathon registration, team management, and project submission.
7. Automated and manual verification results are documented.
8. The research evaluation includes at least one justified baseline comparison.
9. Limitations and negative results are reported transparently.
10. Individual contributions are traceable through GitHub and YouTrack.

## 10. Conclusion

The project management plan defines the main development stages, team responsibilities, dependencies, and potential risks of HackTeam.

A modular architecture, clearly assigned responsibilities, continuous version control, and regular reviews are expected to support organized development.

The proposed roadmap will be refined according to the academic schedule, implementation progress, and supervisor feedback.

The project's success will depend on the quality of implementation, testing, research evaluation, and documented individual contributions.

## 11. Related Documentation

- [Project Proposal](project-proposal.md)
- [Literature Review](literature-review.md)
- [User Research](user-research.md)
- [Requirements Specification](requirements.md)
- [Technology Comparison](technology-comparison.md)
- [System Architecture](architecture.md)
- [Verification and Evaluation Plan](evaluation-plan.md)
- [UX/UI Prototype](ux-prototype.md)
