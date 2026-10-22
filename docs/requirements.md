# HackTeam — Software Requirements Specification

**Project:** HackTeam — Hackathon Management and Student Team Formation Web System

**Document Type:** Software Requirements Specification (SRS)

**Related Issue:** HACK-6 — Define System Requirements

**Academic Institution:** Astana IT University

**Program:** Software Engineering

**Academic Supervisor:** Myrzakerimova Alua

**Prepared by:** Rakhmetulla Madina

**Date:** October 22, 2026

**Document Status:** Initial Draft — Pending Team and Supervisor Review

**Version:** 0.1

---

## 1. Introduction

### 1.1 Purpose

This Software Requirements Specification (SRS) defines the proposed functional and non-functional requirements of the HackTeam web platform.

The document establishes expected system behavior, user roles, feature priorities, acceptance criteria, and preliminary quality requirements.

Its purpose is to provide a consistent foundation for system architecture, implementation planning, software verification, and research evaluation.

The specification covers the responsibilities of all three diploma project participants.

Requirements are considered proposed until they have been reviewed and agreed upon by the development team and, where necessary, the academic supervisor.

### 1.2 Project Overview

HackTeam is a proposed web-based platform for supporting student hackathon participation, team formation, preliminary collaboration assessment, event management, and project coordination.

The system combines two principal research-oriented components:

1. **Multi-Criteria Matching:** A transparent recommendation method considering technical skills, preferred roles, availability, experience, and working preferences.

2. **Trial Sprint:** A structured preliminary collaboration process in which prospective teammates complete limited shared activities before deciding whether to confirm a team.

The platform also supports participant profiles, hackathon discovery, team management, collaborative workspaces, project submission, and selected organizer workflows.

The system must not claim to guarantee successful team compatibility or predict individual reliability.

Artificial intelligence is not required for the core system.

### 1.3 Scope

The initial implementation focuses on a functional web prototype suitable for student hackathons.

The scope includes:

- Account registration and authentication.
- Role-based access control.
- Participant profiles.
- Skill, experience, and availability information.
- Team creation and invitations.
- Multi-criteria teammate recommendations.
- Trial Sprint activities.
- Team confirmation.
- Hackathon creation and registration.
- Team workspaces and task coordination.
- Project submission.
- Basic participation history.
- Research evaluation support.

Advanced analytics, extensive judging workflows, mobile applications, and AI-based recommendations are not essential to the initial MVP.

### 1.4 Related Project Documents

The specification is based on the following existing project documents:

- `docs/project-proposal.md`
- `docs/literature-review.md`

It also reflects the HACK-6 task description and its acceptance criteria.

User research findings, architectural decisions, and supervisor feedback must be incorporated when those artifacts become available and have been reviewed.

No completed user interviews or validated user research findings are assumed in this document.

### 1.5 Terminology

| Term | Definition |
|---|---|
| SRS | Software Requirements Specification |
| FR | Functional Requirement |
| NFR | Non-Functional Requirement |
| MVP | Minimum Viable Product |
| Acceptance Criterion | An observable condition used to verify a requirement |
| Multi-Criteria Matching | Recommendation based on multiple participant characteristics |
| Trial Sprint | A preliminary collaboration activity before final team confirmation |
| Team Leader | A participant with management permissions within a specific team |
| Role Coverage | Representation of skills or roles required by a team |
| Availability Overlap | Common time intervals available to participants |
| Project Reliability Profile | Factual participation and task history recorded by the system |
| RBAC | Role-Based Access Control |
| Baseline | A reference method used for research comparison |

---

## 2. Requirements Classification

### 2.1 Functional Requirements

Functional requirements describe operations and behavior that the system must support.

Each functional requirement uses the identifier format:

`FR-01`, `FR-02`, `FR-03`, etc.

### 2.2 Non-Functional Requirements

Non-functional requirements describe the quality characteristics and constraints of the system.

Each non-functional requirement uses the identifier format:

`NFR-01`, `NFR-02`, `NFR-03`, etc.

### 2.3 Prioritization Method

Requirements are classified using the MoSCoW prioritization approach.

| Priority | Definition | Implementation Expectation |
|---|---|---|
| Must Have | Essential functionality required to demonstrate the core system | Included in the planned MVP |
| Should Have | Important functionality that can be deferred without preventing core workflows | Implement after essential workflows |
| Could Have | Optional functionality that provides additional value | Consider after the MVP is stable |

Priorities reflect the current proposal and must be confirmed with all three developers before implementation.

### 2.4 Requirement Verification

Each mandatory requirement must have an observable acceptance condition.

Verification may include:

- Unit tests.
- Integration tests.
- End-to-end tests.
- Authorization tests.
- Manual acceptance tests.
- Usability evaluations.
- Performance measurements.
- Inspection of application behavior.

A requirement is not considered implemented solely because its source code exists.

---

## 3. System Users and Roles

HackTeam defines six principal system roles.

### 3.1 Participant

A Participant is a student who uses the platform to discover hackathons, manage their profile, find teammates, join teams, and participate in projects.

Primary capabilities include:

- Account management.
- Participant profile management.
- Skill and availability configuration.
- Hackathon discovery.
- Teammate recommendations.
- Team invitations.
- Trial Sprint participation.
- Team collaboration.
- Project participation.

### 3.2 Team Leader

A Team Leader is a participant who has additional management permissions within a particular team.

The role is contextual and does not grant administrative access to the entire platform.

Primary capabilities include:

- Managing team invitations.
- Defining required team roles.
- Coordinating team membership.
- Managing team tasks.
- Coordinating project submissions.
- Initiating Trial Sprint activities where permitted.

### 3.3 Hackathon Organizer

A Hackathon Organizer creates and manages hackathon events.

Primary capabilities include:

- Event creation and configuration.
- Registration management.
- Deadline configuration.
- Viewing registered teams.
- Managing event-related information.
- Reviewing submitted projects.

### 3.4 Mentor

A Mentor supports participating teams through guidance and feedback.

Potential capabilities include:

- Viewing assigned teams.
- Reviewing permitted project information.
- Providing feedback.
- Supporting project development.

Advanced mentor workflows are optional for the initial MVP.

### 3.5 Judge

A Judge evaluates submitted hackathon projects according to organizer-defined criteria.

Potential capabilities include:

- Viewing assigned submissions.
- Reviewing project deliverables.
- Recording evaluation scores.
- Providing structured feedback.

Advanced judging and leaderboard functionality may be deferred.

### 3.6 System Administrator

A System Administrator manages platform-level access and essential system operations.

Primary capabilities include:

- Managing role assignments.
- Reviewing access permissions.
- Handling restricted administrative operations.
- Supporting platform security.
- Reviewing permitted operational records.

Administrative operations must not provide unrestricted access to private participant feedback without an explicitly authorized purpose.

### 3.7 Preliminary Role Permission Matrix

| Capability | Participant | Team Leader | Organizer | Mentor | Judge | Administrator |
|---|---|---|---|---|---|---|
| Manage own profile | Yes | Yes | Yes | Yes | Yes | Yes |
| Discover hackathons | Yes | Yes | Yes | Yes | Yes | Yes |
| Join a team | Yes | Yes | If eligible | If eligible | If eligible | If eligible |
| Manage own team membership | Limited | Yes | No | No | No | Administrative only |
| Manage team tasks | Assigned tasks | Yes | No | Limited | No | Administrative only |
| Create a hackathon | No | No | Yes | No | No | Authorized only |
| Manage event registration | No | No | Yes | No | No | Authorized only |
| Submit a team project | If authorized | Yes | No | No | No | Administrative only |
| Review assigned teams | No | Own team | Event scope | Assigned scope | Assigned scope | Authorized only |
| Score submissions | No | No | If authorized | No | Yes | Authorized only |
| Manage platform roles | No | No | No | No | No | Yes |

Permissions are scoped to the relevant account, team, event, or assignment.

The final access control design must be validated during architecture development.

---

## 4. Functional Requirements

## 4.1 Authentication and Account Management

### FR-01 — User Registration

**Priority:** Must Have

The system shall allow a new user to register an account using the required identity and authentication information.

**Acceptance Criteria:**

- A user providing valid registration data can create an account.
- Duplicate account identifiers are rejected.
- Invalid input produces a clear validation response.
- A successful registration does not grant administrative permissions.

### FR-02 — User Authentication

**Priority:** Must Have

The system shall allow registered users to authenticate using valid credentials.

**Acceptance Criteria:**

- Valid credentials create an authenticated session.
- Invalid credentials are rejected.
- Authentication errors do not disclose whether sensitive account information exists.
- Protected resources require authentication.

### FR-03 — User Logout

**Priority:** Must Have

The system shall allow authenticated users to terminate their sessions.

**Acceptance Criteria:**

- Logout invalidates the current authenticated session.
- Protected resources cannot be accessed through the terminated session.
- The user is redirected or returned to an unauthenticated state.

### FR-04 — Account Recovery

**Priority:** Should Have

The system should provide a secure account recovery mechanism.

**Acceptance Criteria:**

- Eligible users can request account recovery.
- Recovery credentials or links are time-limited.
- Invalid or expired recovery credentials cannot be reused.

### FR-05 — Role-Based Authorization

**Priority:** Must Have

The system shall restrict protected functionality according to assigned roles and resource ownership.

**Acceptance Criteria:**

- Unauthorized users cannot access protected operations.
- Participants cannot access another user's private resources.
- Team leaders can manage only teams within their authorized scope.
- Organizers and judges cannot access unrelated restricted event resources.

---

## 4.2 Participant Profile Management

### FR-06 — Profile Creation and Editing

**Priority:** Must Have

The system shall allow authenticated participants to create, view, and update their profiles.

**Acceptance Criteria:**

- A participant can save valid profile information.
- Updated information is retained after reauthentication.
- Invalid profile updates are rejected.
- One user cannot modify another user's profile without authorization.

### FR-07 — Skills and Preferred Roles

**Priority:** Must Have

The system shall allow participants to specify technical skills and preferred hackathon roles.

**Acceptance Criteria:**

- Participants can add, update, and remove skills.
- Participants can select one or more preferred roles.
- Saved information is available to the matching component according to privacy settings.

### FR-08 — Availability Management

**Priority:** Must Have

The system shall allow participants to specify their availability for team collaboration.

**Acceptance Criteria:**

- Participants can provide valid time intervals.
- Invalid intervals are rejected.
- Updates replace or modify the participant's previously recorded availability.
- The matching component can use permitted availability data.

### FR-09 — Experience and Working Preferences

**Priority:** Must Have

The system shall allow participants to provide relevant experience and working preference information.

**Acceptance Criteria:**

- Participants can edit supported experience and preference fields.
- Optional fields may remain incomplete.
- Missing optional information is handled explicitly during matching.

### FR-10 — Profile Visibility Controls

**Priority:** Must Have

The system shall restrict access to profile information according to defined visibility settings.

**Acceptance Criteria:**

- Public profile information is distinguishable from private information.
- Unauthorized users cannot retrieve protected attributes.
- Private attributes are not included in public search results or API responses.

### FR-11 — Participation History

**Priority:** Must Have

The system shall maintain factual records of eligible participation activities completed within HackTeam.

**Acceptance Criteria:**

- Confirmed participation events can be recorded.
- Existing records are associated with the correct account.
- Users cannot independently modify verified system-generated records.
- The history does not automatically assign subjective personality or reliability scores.

### FR-12 — Account Verification

**Priority:** Should Have

The system should support verification of account contact information.

**Acceptance Criteria:**

- A verification mechanism can confirm control of the configured contact address.
- Expired or invalid verification credentials are rejected.
- Verification status is stored consistently.

---

## 4.3 Team Creation and Membership Management

### FR-13 — Team Creation

**Priority:** Must Have

The system shall allow an eligible participant to create a team for a selected hackathon.

**Acceptance Criteria:**

- A valid team creation request creates a team associated with the selected event.
- The creator becomes the initial team leader.
- Team creation respects event eligibility and team size rules.
- Invalid requests are rejected without creating partial records.

### FR-14 — Team Role Requirements

**Priority:** Must Have

The system shall allow team leaders to define desired roles and skill requirements.

**Acceptance Criteria:**

- Team leaders can specify supported role requirements.
- Requirements are saved and associated with the correct team.
- Unauthorized users cannot modify another team's requirements.

### FR-15 — Team Invitations

**Priority:** Must Have

The system shall allow authorized team leaders to invite eligible participants.

**Acceptance Criteria:**

- An invitation identifies the destination team and invited participant.
- Only an eligible recipient can accept the invitation.
- Duplicate pending invitations are handled consistently.
- Invitations cannot exceed configured team constraints.

### FR-16 — Invitation Responses

**Priority:** Must Have

The system shall allow invited participants to accept or decline team invitations.

**Acceptance Criteria:**

- An invited participant can accept a valid pending invitation.
- The system rejects expired, invalid, or unauthorized invitations.
- Declining an invitation does not add the participant to the team.
- Accepted membership respects event and team restrictions.

### FR-17 — Membership Management

**Priority:** Must Have

The system shall allow authorized users to view and manage team membership.

**Acceptance Criteria:**

- Team members can view the permitted membership list.
- A team leader can perform authorized membership operations.
- A non-leader cannot perform leader-only operations.
- Membership changes are reflected consistently.

### FR-18 — Duplicate Membership Prevention

**Priority:** Must Have

The system shall enforce the configured policy for membership in teams participating in the same hackathon.

**Acceptance Criteria:**

- An attempt to violate the configured membership restriction is rejected.
- Repeated requests cannot create duplicate membership records.
- The restriction is enforced by the backend and not only by the interface.

---

## 4.4 Multi-Criteria Matching

### FR-19 — Candidate Recommendation

**Priority:** Must Have

The system shall generate teammate recommendations for an eligible participant or team.

**Acceptance Criteria:**

- The system can produce a ranked list from eligible candidate profiles.
- Candidates not satisfying mandatory eligibility conditions are excluded.
- An empty eligible candidate set produces a valid empty result rather than an application failure.

### FR-20 — Multi-Criteria Evaluation

**Priority:** Must Have

The system shall evaluate candidate suitability using multiple defined criteria.

The initial proposed criteria include:

- Skill and role coverage.
- Availability overlap.
- Experience complementarity.
- Working preference alignment.

**Acceptance Criteria:**

- Each configured criterion produces a defined value.
- Criterion values are normalized before aggregation.
- Weights follow the documented scoring configuration.
- Identical input data and configuration produce reproducible scores.

### FR-21 — Matching Constraints

**Priority:** Must Have

The system shall enforce mandatory matching constraints separately from preference-based scoring.

**Acceptance Criteria:**

- Ineligible or unavailable candidates are excluded when mandatory rules apply.
- Team size restrictions are enforced.
- Invalid candidate combinations are rejected regardless of their preference scores.

### FR-22 — Candidate Ranking

**Priority:** Must Have

The system shall rank eligible candidates using the calculated recommendation scores.

**Acceptance Criteria:**

- Candidate results are ordered according to the specified score.
- Equal-score cases are handled deterministically.
- The ranking can be reproduced using the same inputs and configuration.

### FR-23 — Recommendation Explanation

**Priority:** Must Have

The system shall provide understandable explanations of the principal criteria contributing to a recommendation.

**Acceptance Criteria:**

- Users can view the relevant matching factors.
- Explanations correspond to the actual scoring model.
- The interface does not claim guaranteed interpersonal compatibility.

### FR-24 — Participant-Controlled Team Confirmation

**Priority:** Must Have

The system shall require an authorized participant action before finalizing team membership.

**Acceptance Criteria:**

- A recommendation alone does not create confirmed membership.
- Appropriate participant acceptance is required.
- A declined recommendation does not automatically create membership.
- Confirmed membership is visible to authorized users.

### FR-25 — Baseline Matching Support

**Priority:** Must Have

The system shall support comparison of the proposed multi-criteria method with a skill-only baseline for research evaluation.

**Acceptance Criteria:**

- Both methods can be applied to the same eligible candidate dataset.
- The configured evaluation results can be reproduced.
- The comparison does not silently change candidate eligibility conditions.

### FR-26 — Candidate Search and Filters

**Priority:** Should Have

The system should allow participants to filter eligible candidates using supported profile attributes.

**Acceptance Criteria:**

- Supported filters affect the candidate list.
- Unauthorized profile attributes are not exposed.
- Invalid filters return a controlled validation response.

### FR-27 — Matching Configuration

**Priority:** Should Have

The system should support controlled adjustments to matching criterion weights for research experiments.

**Acceptance Criteria:**

- Authorized experiment configurations can define valid weights.
- Invalid configurations are rejected.
- Applied configurations are recorded for reproducibility.

---

## 4.5 Trial Sprint Mechanism

### FR-28 — Trial Sprint Creation

**Priority:** Must Have

The system shall allow authorized users to initiate a Trial Sprint for a temporary team.

**Acceptance Criteria:**

- A valid request creates a Trial Sprint linked to the correct temporary team.
- Only authorized users can initiate it.
- Invalid state transitions and duplicate conflicting trials are rejected.

### FR-29 — Voluntary Trial Participation

**Priority:** Must Have

The system shall require prospective participants to accept participation in a Trial Sprint.

**Acceptance Criteria:**

- A participant can accept or decline an invitation.
- Declining does not activate trial membership.
- Only accepted participants receive trial collaboration permissions.

### FR-30 — Trial Task Management

**Priority:** Must Have

The system shall allow authorized Trial Sprint participants to create and assign preliminary collaborative tasks.

**Acceptance Criteria:**

- Valid tasks can be created and assigned.
- Assigned users can view their tasks.
- Unauthorized users cannot modify trial tasks.

### FR-31 — Trial Deadlines

**Priority:** Must Have

The system shall allow authorized users to define deadlines for Trial Sprint tasks.

**Acceptance Criteria:**

- Deadlines are saved with valid date and time values.
- Invalid deadlines are rejected.
- Task deadlines are visible to authorized team members.

### FR-32 — Trial Progress Tracking

**Priority:** Must Have

The system shall record task progress using defined states.

Proposed task states:

- To Do.
- In Progress.
- Done.

**Acceptance Criteria:**

- Authorized users can update task states.
- Updated states are persisted.
- Invalid state values are rejected.
- The trial workspace reflects the current task states.

### FR-33 — Trial Activity History

**Priority:** Must Have

The system shall maintain factual records of relevant Trial Sprint activities.

**Acceptance Criteria:**

- Task assignment and completion events are recorded.
- Recorded events are associated with authorized participants.
- Participants cannot arbitrarily rewrite protected historical records.

### FR-34 — Participant Reflection

**Priority:** Must Have

The system shall allow Trial Sprint participants to provide structured feedback about their collaboration experience.

**Acceptance Criteria:**

- Participants can submit supported feedback responses.
- Feedback is associated with the relevant trial.
- A participant cannot submit feedback on behalf of another participant.
- Optional feedback fields are not treated as mandatory personal evaluations.

### FR-35 — Final Trial Decision

**Priority:** Must Have

The system shall allow participants to confirm or decline continued collaboration after Trial Sprint.

**Acceptance Criteria:**

- A participant can record their decision.
- Final team confirmation follows the documented consent and membership policy.
- A participant who declines is not automatically added to the final team.
- Final outcomes are saved consistently.

### FR-36 — Trial Feedback Privacy

**Priority:** Must Have

The system shall restrict access to Trial Sprint feedback according to a documented access policy.

**Acceptance Criteria:**

- Private feedback is not accessible to unrelated users.
- Private feedback is not automatically published in a participant profile.
- Access control is enforced on the server.
- Research use requires the appropriate consent and access permissions.

### FR-37 — Team Agreement

**Priority:** Should Have

The system should allow temporary teams to define basic collaboration expectations before beginning a Trial Sprint.

**Acceptance Criteria:**

- A team can record agreed responsibilities and communication expectations.
- Authorized team members can view the agreement.
- Changes are recorded consistently.

### FR-38 — External Work Evidence

**Priority:** Should Have

The system should allow participants to attach permitted references to externally completed trial work.

**Acceptance Criteria:**

- Valid links or supported references can be submitted.
- Invalid inputs are rejected.
- The system does not automatically treat an external link as proof of completed work.

### FR-39 — Factual Reliability History

**Priority:** Must Have

The system shall derive Project Reliability Profile records only from explicitly defined and verifiable in-system activities.

**Acceptance Criteria:**

- Eligible completed activities appear in the correct participant history.
- Unsupported numerical trustworthiness scores are not generated.
- Private participant feedback is not automatically published.
- Records do not claim to predict personal character or future performance.

---

## 4.6 Hackathon Management

### FR-40 — Hackathon Creation

**Priority:** Must Have

The system shall allow authorized organizers to create hackathon events.

**Acceptance Criteria:**

- Valid event information creates an event record.
- Unauthorized users cannot create organizer-managed events.
- Required fields are validated before saving.

### FR-41 — Hackathon Editing and Publication

**Priority:** Must Have

The system shall allow authorized organizers to update and publish event details.

**Acceptance Criteria:**

- Draft events can be updated by authorized users.
- Published events are visible to eligible participants.
- Unauthorized modification attempts are rejected.

### FR-42 — Hackathon Discovery

**Priority:** Must Have

The system shall allow users to browse available hackathons.

**Acceptance Criteria:**

- Published events appear in event listings.
- Users can view permitted event details.
- Unpublished or restricted events are not exposed to unauthorized users.

### FR-43 — Hackathon Registration

**Priority:** Must Have

The system shall allow eligible users to register for available hackathons.

**Acceptance Criteria:**

- Registration succeeds within the permitted registration period.
- Repeated requests do not create duplicate registration records.
- Registered participants receive an identifiable registration state.

### FR-44 — Event Eligibility and Deadline Validation

**Priority:** Must Have

The system shall enforce configured eligibility restrictions and event deadlines.

**Acceptance Criteria:**

- Registration outside the permitted period is rejected.
- Configured capacity and eligibility limits are enforced.
- Invalid requests do not produce inconsistent event records.

### FR-45 — Organizer Participant Overview

**Priority:** Must Have

The system shall allow authorized organizers to view registered participants and teams for their events.

**Acceptance Criteria:**

- An organizer can view the permitted registration list for an assigned event.
- Unrelated organizers cannot access restricted event information.
- The displayed information reflects current registration records.

---

## 4.7 Team Workspace and Project Submission

### FR-46 — Team Workspace

**Priority:** Must Have

The system shall provide confirmed teams with a workspace for project coordination.

**Acceptance Criteria:**

- Confirmed teams can access their own workspace.
- Workspace membership reflects authorized team membership.
- Unrelated users cannot access protected team resources.

### FR-47 — Team Task and Deadline Management

**Priority:** Must Have

The system shall allow authorized team members to create, assign, and track project tasks.

**Acceptance Criteria:**

- Authorized users can create tasks and define deadlines.
- Task assignees can view relevant tasks.
- Changes to task status are persisted.
- Unauthorized modifications are rejected.

### FR-48 — Project Submission

**Priority:** Must Have

The system shall allow authorized teams to submit hackathon project information and deliverables.

**Acceptance Criteria:**

- A valid submission is associated with the correct team and event.
- Required fields are validated.
- Unauthorized users cannot submit on behalf of another team.
- Submissions respect configured event deadlines.

### FR-49 — Submission Confirmation

**Priority:** Must Have

The system shall provide an identifiable status after project submission.

**Acceptance Criteria:**

- Successful submissions produce a confirmation.
- Authorized users can view submission status.
- Failed submissions do not appear as successfully completed.

### FR-50 — Submission Updates

**Priority:** Should Have

The system should allow eligible teams to update project submissions before the configured deadline.

**Acceptance Criteria:**

- Valid updates are saved before the deadline.
- Updates after the deadline are rejected unless explicitly permitted.
- Unauthorized users cannot modify another team's submission.

---

## 4.8 Judging, Mentoring, and Extended Event Features

### FR-51 — Basic Project Evaluation

**Priority:** Should Have

The system should allow authorized judges to record evaluation results according to predefined criteria.

**Acceptance Criteria:**

- Assigned judges can access permitted submissions.
- Evaluation criteria are defined by the relevant event.
- Invalid or unauthorized scores are rejected.
- Evaluation records are retained consistently.

### FR-52 — Results and Leaderboard

**Priority:** Could Have

The system could provide published event results and leaderboards.

**Acceptance Criteria:**

- Results are calculated according to the configured evaluation rules.
- Unpublished results remain restricted.
- Published rankings reflect recorded evaluation data.

### FR-53 — Mentor Feedback

**Priority:** Could Have

The system could allow assigned mentors to provide structured project feedback.

**Acceptance Criteria:**

- Mentors can view only authorized projects.
- Feedback is associated with the correct team.
- Unauthorized users cannot submit mentor feedback.

### FR-54 — Organizer Analytics

**Priority:** Could Have

The system could provide organizers with basic event statistics.

**Acceptance Criteria:**

- Analytics display permitted event data.
- Statistics are calculated consistently from stored records.
- Restricted participant information is not exposed.

### FR-55 — Notifications

**Priority:** Should Have

The system should provide notifications for relevant invitations, deadlines, and participation events.

**Acceptance Criteria:**

- Eligible events create notifications for the intended recipients.
- Unrelated users cannot access another user's notifications.
- Duplicate events do not produce uncontrolled duplicate notifications.

---

## 4.9 Administration and Research Support

### FR-56 — Administrative Role Management

**Priority:** Must Have

The system shall allow authorized administrators to manage platform-level role assignments.

**Acceptance Criteria:**

- Role assignments require authorized administrative access.
- Participants cannot grant themselves elevated permissions.
- Role changes are reflected in subsequent authorization checks.

### FR-57 — Account Restriction

**Priority:** Should Have

The system should allow authorized administrators to restrict accounts that violate documented platform rules.

**Acceptance Criteria:**

- Only permitted administrators can apply restrictions.
- Restricted accounts cannot perform prohibited operations.
- Restrictions can be reviewed through authorized procedures.

### FR-58 — Research Data Export

**Priority:** Must Have

The system shall support controlled export of the non-sensitive data required for authorized research evaluation.

**Acceptance Criteria:**

- Only authorized users can initiate research exports.
- Exported records correspond to the selected approved dataset.
- Unauthorized personal information is excluded.
- The exported data can be used to reproduce documented comparison metrics.

### FR-59 — Important Activity Audit Records

**Priority:** Must Have

The system shall record security-relevant administrative events.

**Acceptance Criteria:**

- Important role and permission changes are recorded.
- Audit records identify the operation and relevant timestamp.
- Unauthorized users cannot modify audit records.
- Sensitive authentication secrets are not stored in audit records.

### FR-60 — Research Participation Consent

**Priority:** Must Have

The system shall distinguish ordinary platform participation from voluntary participation in research activities.

**Acceptance Criteria:**

- Users receive the relevant research information before providing research consent.
- Research participation decisions are recorded.
- Declining optional research participation does not automatically prevent unrelated permitted platform use.
- Research data collection follows the recorded consent conditions.

---

## 5. Non-Functional Requirements

Non-functional requirements describe the expected quality and operational characteristics of HackTeam.

The following numerical performance and reliability thresholds are **proposed MVP evaluation targets**, not measured system performance or supervisor-approved commitments. They must be reviewed against available infrastructure and project resources.

### 5.1 Security

#### NFR-01 — Credential Protection

**Priority:** Must Have

The system shall protect stored authentication credentials using an established password hashing approach with appropriate configuration.

**Acceptance Criteria:**

- Plaintext passwords are not stored.
- Authentication succeeds using the stored verifier.
- Database inspection does not reveal plaintext passwords.
- Secrets are not exposed through logs or API responses.

#### NFR-02 — Session Security

**Priority:** Must Have

The system shall manage authenticated sessions securely.

**Acceptance Criteria:**

- Session credentials are not exposed through public responses.
- Logout invalidates the relevant session.
- Expired sessions cannot access protected resources.
- Session-based state-changing requests are protected against applicable cross-site request forgery risks.

#### NFR-03 — Access Control Enforcement

**Priority:** Must Have

The system shall enforce authorization at the server level.

**Acceptance Criteria:**

- Role and ownership restrictions are tested using authorized and unauthorized accounts.
- Unauthorized requests do not disclose protected data.
- Attempts to access another participant's private resources are rejected.

#### NFR-04 — Input Validation

**Priority:** Must Have

The system shall validate untrusted inputs and handle invalid requests safely.

**Acceptance Criteria:**

- Invalid types, lengths, and required-field omissions produce controlled errors.
- User-generated content cannot execute unauthorized code in rendered pages.
- Malformed requests do not corrupt application data.

### 5.2 Data Privacy

#### NFR-05 — Data Minimization

**Priority:** Must Have

The system shall collect only participant information required for the supported functionality.

**Acceptance Criteria:**

- Required and optional fields are documented.
- Sensitive data unrelated to team formation is not mandatory.
- Private information is excluded from unrelated responses and exports.

#### NFR-06 — Feedback Confidentiality

**Priority:** Must Have

The system shall protect private Trial Sprint feedback.

**Acceptance Criteria:**

- Unauthorized users cannot retrieve private feedback.
- Private feedback is not included in public profiles.
- Research access follows the documented consent and authorization rules.

#### NFR-07 — Secure Communication

**Priority:** Must Have

Deployed environments containing actual participant data shall use appropriately secured network communication.

**Acceptance Criteria:**

- Authenticated production-like traffic uses encrypted transport.
- Sensitive credentials are not transmitted through unencrypted public endpoints.
- Security configuration is checked before a public deployment.

### 5.3 Performance

#### NFR-08 — Standard Operation Response Time

**Priority:** Should Have

Under the proposed MVP test environment, at least 95% of ordinary authenticated API requests should complete within two seconds under a documented workload of 50 concurrent test users.

**Acceptance Criteria:**

- A repeatable load test is defined.
- Measured response times are recorded.
- The 95th-percentile result is compared against the proposed two-second threshold.

#### NFR-09 — Matching Execution Time

**Priority:** Should Have

The matching component should return a ranked recommendation result within three seconds for a controlled dataset of up to 500 eligible candidate profiles in the agreed test environment.

**Acceptance Criteria:**

- Test data generation is documented.
- Matching configuration and hardware are recorded.
- Execution time is measured over repeated test runs.
- Results are compared with the proposed threshold.

### 5.4 Reliability and Recoverability

#### NFR-10 — Core Workflow Reliability

**Priority:** Must Have

The system shall preserve consistent records when core operations fail.

**Acceptance Criteria:**

- A failed team membership operation does not create partial membership.
- A failed submission does not create an incorrect success status.
- Repeated requests are handled according to the documented duplication policy.

#### NFR-11 — Backup and Recovery

**Priority:** Should Have

The system should support recovery of essential application data from a documented backup procedure.

**Acceptance Criteria:**

- A backup can be created in the agreed test environment.
- A documented restoration test reconstructs the required data.
- Recovery limitations are recorded.

### 5.5 Scalability

#### NFR-12 — Prototype Capacity

**Priority:** Should Have

The MVP should remain operational under a documented demonstration workload of at least 100 registered test users and 20 configured hackathon events.

**Acceptance Criteria:**

- Representative test accounts and events can be created.
- Main user workflows remain functional.
- Measured response times and failures are documented.
- The test environment and resource limits are reported.

### 5.6 Usability

#### NFR-13 — Essential Workflow Usability

**Priority:** Must Have

The user interface shall provide clear navigation, feedback, and validation for essential participant workflows.

**Acceptance Criteria:**

- Users receive visible feedback after successful and failed operations.
- Essential forms identify invalid inputs.
- A usability pilot evaluates registration, teammate recommendation, and team confirmation.
- Usability problems and task completion observations are documented.

No particular usability score is claimed before testing.

### 5.7 Accessibility

#### NFR-14 — Accessible Core Interfaces

**Priority:** Must Have

Essential interfaces shall support keyboard navigation and accessible labeling of interactive controls.

**Acceptance Criteria:**

- Essential actions can be completed using keyboard navigation.
- Form controls have understandable labels.
- Keyboard focus is visibly indicated.
- Core screens are examined for significant accessibility issues.

### 5.8 Compatibility

#### NFR-15 — Browser and Screen Compatibility

**Priority:** Should Have

The application should support the current stable versions of major desktop browsers and responsive layouts for common screen sizes.

**Acceptance Criteria:**

- Core flows are manually checked in at least two browser engines.
- Interfaces are tested at desktop and mobile viewport widths.
- Essential controls remain usable without unintended horizontal overflow.

### 5.9 Maintainability

#### NFR-16 — Code Maintainability and Testing

**Priority:** Must Have

The system shall use modular components and maintain testable boundaries between major functional modules.

**Acceptance Criteria:**

- Authentication, matching, Trial Sprint, and hackathon management responsibilities are identifiable.
- Core business rules are covered by automated tests.
- Changes undergo Pull Request review before integration into `main`.
- Setup and execution instructions are documented.

### 5.10 Observability

#### NFR-17 — Error Handling and Operational Logging

**Priority:** Must Have

The system shall provide controlled error responses and sufficient operational information for debugging without exposing sensitive data.

**Acceptance Criteria:**

- Unexpected failures generate diagnosable server-side records.
- Client responses do not reveal passwords, secrets, or internal stack traces.
- Logs include sufficient context to identify the affected operation.
- Sensitive personal information is not unnecessarily recorded.

### 5.11 Research Ethics

#### NFR-18 — Responsible Research Data Handling

**Priority:** Must Have

Research-related personal data shall be processed according to documented consent, access, and retention procedures.

**Acceptance Criteria:**

- Research participation is voluntary.
- Only approved users can access research datasets.
- Export procedures minimize directly identifying information.
- The research plan documents how data will be retained and handled after the study.

---

## 6. Core Business Rules

### BR-01 — Voluntary Team Membership

Recommendations shall not automatically create confirmed membership.

### BR-02 — Event-Specific Membership

Membership restrictions shall be enforced within the relevant hackathon context.

### BR-03 — Team Size Constraints

Team size shall follow the configuration of the selected hackathon.

### BR-04 — Matching Eligibility

Mandatory team and event requirements shall be checked before preference-based candidate ranking.

### BR-05 — Reproducible Matching

Matching results shall be reproducible for the same data, configuration, and version of the scoring method.

### BR-06 — Trial Sprint Voluntariness

Participation in preliminary collaboration shall require appropriate participant acceptance.

### BR-07 — Feedback Privacy

Private participant reflections shall not automatically become public reputation indicators.

### BR-08 — Factual Participation History

Participation records shall represent verifiable in-system activities rather than unvalidated character judgments.

### BR-09 — Submission Deadlines

Project submission eligibility shall follow event-defined deadlines and permissions.

### BR-10 — Scoped Permissions

All team, event, and evaluation permissions shall be checked against the relevant resource scope.

---

## 7. Principal User Stories

### US-01 — Participant Profile

**As a** student,  
**I want to** create a profile describing my skills and availability,  
**so that** other participants and the recommendation method can consider my relevant characteristics.

**Related Requirements:** FR-06, FR-07, FR-08, FR-09.

### US-02 — Teammate Recommendation

**As a** participant,  
**I want to** receive understandable teammate recommendations,  
**so that** I can identify candidates whose skills, roles, and schedules may complement mine.

**Related Requirements:** FR-19, FR-20, FR-21, FR-22, FR-23.

### US-03 — Voluntary Team Selection

**As a** student,  
**I want to** accept or decline invitations and recommendations,  
**so that** I maintain control over my team membership.

**Related Requirements:** FR-15, FR-16, FR-24.

### US-04 — Trial Sprint

**As a** prospective team member,  
**I want to** collaborate on a short task before confirming my team,  
**so that** I can obtain additional experience of working with the proposed participants.

**Related Requirements:** FR-28 through FR-38.

### US-05 — Hackathon Management

**As a** hackathon organizer,  
**I want to** create events, configure registration, and manage deadlines,  
**so that** participants can join a structured hackathon.

**Related Requirements:** FR-40 through FR-45.

### US-06 — Project Submission

**As a** team leader,  
**I want to** submit our hackathon project and view its submission status,  
**so that** I can verify that our deliverables were recorded.

**Related Requirements:** FR-46 through FR-50.

### US-07 — Project Evaluation

**As a** judge,  
**I want to** review assigned submissions using defined criteria,  
**so that** I can provide structured evaluation results.

**Related Requirements:** FR-51, FR-52.

### US-08 — Research Evaluation

**As a** researcher,  
**I want to** compare multi-criteria matching with a baseline,  
**so that** I can investigate the behavior and limitations of the proposed method.

**Related Requirements:** FR-25, FR-27, FR-58, FR-60.

---

## 8. Essential System Workflows

### 8.1 Participant Registration

1. A visitor opens the registration interface.
2. The visitor provides required data.
3. The system validates the request.
4. The system creates the account if the information is valid.
5. The participant authenticates and gains access to permitted features.

**Failure Cases:**

- Duplicate identifier.
- Invalid data.
- Authentication failure.
- Unauthorized access.

### 8.2 Team Formation

1. A participant selects a hackathon.
2. The participant creates or searches for a team.
3. The team leader defines required roles.
4. The matching component evaluates eligible candidates.
5. The system displays ranked recommendations and explanations.
6. Participants review recommendations.
7. Invitations and voluntary acceptance determine membership.

### 8.3 Trial Sprint

1. A temporary team initiates a Trial Sprint.
2. Prospective participants accept the trial.
3. The team defines a limited collaborative activity.
4. Participants receive tasks and deadlines.
5. Task states and relevant events are recorded.
6. Participants provide optional structured feedback.
7. Participants decide whether to confirm continued collaboration.

### 8.4 Hackathon Participation

1. An organizer creates and publishes a hackathon.
2. Eligible participants register.
3. Participants form or join teams.
4. Teams coordinate work in their workspace.
5. Authorized team members submit project information.
6. The system records submission status.
7. Optional evaluation workflows may follow.

---

## 9. MVP and Optional Functionality

### 9.1 Essential MVP Modules

The proposed MVP includes:

| Module | Essential Functionality | Primary Owner |
|---|---|---|
| Identity and Access | Registration, authentication, authorization | Yergalyuly Daniyar |
| Participant Profiles | Skills, roles, availability, preferences | Rakhmetulla Madina |
| Team Formation | Creation, invitations, confirmation | Rakhmetulla Madina |
| Multi-Criteria Matching | Scoring, ranking, explanations, baseline comparison | Rakhmetulla Madina |
| Trial Sprint | Temporary teams, tasks, deadlines, feedback, confirmation | Rakhmetulla Madina |
| Hackathon Management | Event creation, discovery, registration | Talasbek Kassymbek |
| Team Workspace | Team tasks, deadlines, coordination | Talasbek Kassymbek |
| Project Submission | Submission records and confirmation | Talasbek Kassymbek |
| Administrative Controls | Essential scoped role and permission management | Yergalyuly Daniyar |
| Research Support | Matching comparison data and evaluation records | Shared, led by Rakhmetulla Madina |

Primary ownership does not exclude collaboration among team members.

### 9.2 Deferred Features

The following functionality may be deferred beyond the initial MVP:

- Password recovery and advanced account verification.
- Advanced candidate search filters.
- Configurable matching experiments exposed through the application.
- Extended Team Agreement workflows.
- External artifact integrations.
- Advanced judge management.
- Public leaderboards.
- Detailed mentor dashboards.
- Organizer analytics.
- Extensive notification workflows.
- External development platform integrations.
- Native mobile applications.
- AI-driven recommendations.
- Complex automated reputation scoring.

### 9.3 Scope Management

The proposed scope is substantial for a three-person student team.

If development capacity becomes insufficient, the team should preserve the core research workflows before adding optional functionality.

The initial implementation should prioritize:

1. Functional participant profiles.
2. Reproducible multi-criteria recommendations.
3. Voluntary team formation.
4. A working Trial Sprint lifecycle.
5. Basic hackathon management.
6. Project submission.
7. Data needed for verification and research evaluation.

Any reduction of a Must Have requirement should be documented, reviewed, and reflected in the Project Proposal and evaluation plan.

---

## 10. Requirement Verification and Traceability

### 10.1 Verification Matrix

| Requirement Group | Proposed Verification |
|---|---|
| FR-01–FR-05 | Authentication and authorization tests |
| FR-06–FR-12 | Profile validation, persistence, and privacy tests |
| FR-13–FR-18 | Membership, invitation, and constraint tests |
| FR-19–FR-27 | Algorithm unit tests, ranking comparisons, reproducibility tests |
| FR-28–FR-39 | Trial Sprint workflow and access control tests |
| FR-40–FR-45 | Event creation, discovery, and registration tests |
| FR-46–FR-50 | Workspace and submission integration tests |
| FR-51–FR-55 | Optional evaluation and notification tests when implemented |
| FR-56–FR-60 | Administrative access and research data handling tests |
| NFR-01–NFR-07 | Security and privacy verification |
| NFR-08–NFR-12 | Performance, reliability, and capacity testing |
| NFR-13–NFR-15 | Usability, accessibility, and compatibility checks |
| NFR-16–NFR-18 | Maintainability, logging, and research ethics inspection |

### 10.2 Traceability to Project Objectives

| Project Objective | Relevant Requirements |
|---|---|
| Support student profiles | FR-06–FR-12 |
| Develop multi-criteria matching | FR-19–FR-27 |
| Provide preliminary collaboration | FR-28–FR-39 |
| Manage hackathons | FR-40–FR-45 |
| Support team collaboration | FR-46–FR-47 |
| Enable project submissions | FR-48–FR-50 |
| Enforce secure access | FR-05, FR-56, NFR-01–NFR-07 |
| Evaluate matching methods | FR-25, FR-58 |
| Protect participant information | FR-10, FR-36, FR-60, NFR-05–NFR-06, NFR-18 |

### 10.3 Requirement Completion Rules

An individual requirement may be marked as implemented only when:

1. Its expected behavior has been developed.
2. Its applicable acceptance criteria have been verified.
3. Relevant tests or inspection evidence are available.
4. No unresolved critical issue prevents its intended workflow.
5. Its implementation has undergone the team's agreed review procedure.

Documentation approval and actual software implementation are separate milestones.

---

## 11. Team Responsibilities and Review Process

### 11.1 Rakhmetulla Madina

Primary areas:

- Participant profiles.
- Team formation.
- Multi-criteria matching.
- Trial Sprint.
- Preliminary research methodology.
- Matching algorithm evaluation.

### 11.2 Talasbek Kassymbek

Primary areas:

- Hackathon management.
- Team workspaces.
- Task coordination.
- Project deadlines.
- Project submission workflows.

### 11.3 Yergalyuly Daniyar

Primary areas:

- Backend architecture.
- Authentication and authorization.
- Administrative and organizer support.
- Evaluation infrastructure.
- Analytics and notifications where prioritized.

### 11.4 Joint Review Requirements

All three team members must review the requirements affecting their modules.

The review should confirm:

- Module ownership.
- Feasibility of the essential MVP.
- Consistency of shared data and permissions.
- Agreement on cross-module workflows.
- Matching and Trial Sprint boundaries.
- Acceptance criteria and planned verification.
- Priority assignments.
- Compatibility with system architecture.

The academic supervisor may request changes to the documented scope.

---

## 12. Open Decisions and Assumptions

The following decisions are not yet confirmed.

| ID | Open Decision | Responsible Review |
|---|---|---|
| OD-01 | Final application architecture and technology stack | All developers |
| OD-02 | Supported authentication and account verification methods | Backend owner |
| OD-03 | Exact team size and membership policies | Team and organizer module owners |
| OD-04 | Matching normalization and criterion weights | Matching owner |
| OD-05 | Missing profile information handling | Matching owner |
| OD-06 | Trial Sprint duration and task templates | Trial Sprint owner |
| OD-07 | Visibility of individual Trial Sprint feedback | Team and supervisor |
| OD-08 | Basic judging workflow in the MVP | Organizer/backend owners |
| OD-09 | Final performance and capacity thresholds | All developers |
| OD-10 | Research sample size and evaluation procedures | Research owner and supervisor |
| OD-11 | Research consent and data retention procedures | Team and supervisor |
| OD-12 | Final scope adjustments after user research | All developers |

These decisions must not be represented as experimentally validated or already approved.

---

## 13. Risks and Dependencies

| Risk | Possible Impact | Mitigation |
|---|---|---|
| Excessive MVP scope | Implementation delays | Prioritize research-critical workflows |
| Unclear matching criteria | Inconsistent recommendation results | Specify formulas and normalization |
| Incomplete participant profiles | Reduced recommendation coverage | Handle optional and missing data |
| Insufficient pilot participants | Limited empirical evaluation | Recruit volunteers and report limitations |
| Complex Trial Sprint workflow | Poor usability | Keep initial activities short and structured |
| Inconsistent permissions | Security vulnerabilities | Centralize authorization checks |
| Unclear shared module contracts | Integration difficulties | Review interfaces before implementation |
| Unrealistic performance expectations | Failed acceptance tests | Validate numerical targets against infrastructure |
| Sensitive feedback exposure | Privacy and ethical concerns | Enforce access controls and consent |
| Incomplete acceptance criteria | Difficult verification | Require testable conditions for mandatory requirements |

---

## 14. Requirements Review Checklist

The following checklist will be used before final approval.

- [x] Functional requirements are documented.
- [x] Non-functional requirements are documented.
- [x] Six principal user roles are identified.
- [x] Functional and non-functional requirements have unique identifiers.
- [x] Requirements have proposed priorities.
- [x] Mandatory requirements have verifiable acceptance criteria.
- [x] Essential MVP functionality is distinguished from optional enhancements.
- [x] Requirements cover the planned modules of all three team members.
- [x] The specification identifies limitations and open decisions.
- [x] The draft is aligned with the existing Project Proposal.
- [ ] All three team members have reviewed the requirements.
- [ ] Open architectural and scope decisions have been resolved or formally deferred.
- [ ] Academic supervisor feedback has been incorporated where available.
- [ ] The specification has been approved through a GitHub Pull Request.

---

## 15. Conclusion

This Software Requirements Specification defines the proposed functional and non-functional requirements of the HackTeam web platform.

The document establishes system roles, essential workflows, prioritized capabilities, measurable acceptance criteria, and preliminary software quality expectations.

The most important research-oriented functionality consists of multi-criteria teammate recommendations and the Trial Sprint mechanism for preliminary collaboration assessment.

The specification also includes the necessary hackathon management, team coordination, identity, submission, and administrative functionality required for an integrated prototype.

Requirements are defined independently of a specific implementation technology wherever possible.

The document will serve as a reference for subsequent architecture design, development planning, verification, and research evaluation.

Because the project is still in its planning stage, requirements and numerical quality targets remain subject to team review, user research findings, technical feasibility, and academic supervisor feedback.

---

**Document Status:** Draft version 0.1, prepared for team review through GitHub. Approval of this document does not imply that the specified software functionality has already been implemented.
