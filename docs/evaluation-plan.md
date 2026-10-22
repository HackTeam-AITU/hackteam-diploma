# HackTeam — Verification and Evaluation Plan

**Project:** HackTeam — Hackathon Management and Student Team Formation Web System

**Document Type:** Software Verification and Research Evaluation Plan

**Related Issue:** HACK-9 — Prepare Verification and Evaluation Plan

**Academic Institution:** Astana IT University

**Program:** Software Engineering

**Academic Supervisor:** Myrzakerimova Alua

**Prepared by:** Rakhmetulla Madina

**Date:** October 22, 2026

**Document Version:** 0.1

**Document Status:** Initial Draft — Pending Team and Supervisor Review

**Execution Status:** Planned — No Test or Experimental Results Reported

---

## 1. Introduction

### 1.1 Purpose

This document defines the proposed software verification and research evaluation strategy for the HackTeam diploma project.

It establishes how the platform's functional behavior, non-functional characteristics, security, reliability, usability, and research-oriented components will be verified and evaluated.

The plan serves two complementary purposes:

1. **Software Verification:** Determine whether the implemented system satisfies its documented functional and non-functional requirements.
2. **Research Evaluation:** Investigate the behavior, effectiveness, limitations, and potential value of the proposed Multi-Criteria Matching method and Trial Sprint mechanism.

The document specifies planned test scenarios, requirement traceability, evaluation metrics, baseline approaches, experimental procedures, data collection methods, and threats to validity.

All described activities are prospective. No software testing results, participant observations, or experimental findings are claimed at this stage.

### 1.2 Project Context

HackTeam is a proposed web-based platform supporting student hackathon management and team formation.

Its principal functionality includes:

- Authentication and authorization.
- Participant profiles.
- Skills, roles, experience, and availability information.
- Team creation and membership management.
- Multi-Criteria Matching.
- Trial Sprint activities.
- Hackathon registration and management.
- Team workspaces and task coordination.
- Project submission.
- Basic participation history.
- Research evaluation support.

The proposed research contribution consists of evaluating a transparent multi-criteria team formation method and investigating whether preliminary collaboration provides additional useful information before final team confirmation.

### 1.3 Related Documents

This plan is based on:

- `docs/project-proposal.md`
- `docs/literature-review.md`
- `docs/requirements.md`

The Software Requirements Specification is the principal source of requirement identifiers and acceptance criteria.

The plan will be revised when system architecture, implemented functionality, and research procedures are approved.

### 1.4 Scope of Verification

Verification will cover essential MVP functionality across all three developers' modules.

The plan includes positive, negative, boundary, security, and integration testing.

Optional functionality will be tested when implemented but is not required to demonstrate initial MVP completion.

### 1.5 Scope of Research Evaluation

Research evaluation will investigate:

1. The behavior of skill-only matching.
2. The behavior of multi-criteria matching.
3. The potential usefulness of Trial Sprint after initial matching.
4. Participant perceptions of recommendation transparency and suitability.
5. Selected observable indicators of preliminary collaboration.
6. Computational performance of the matching method.

The evaluation will not claim to predict individual character, guarantee successful collaboration, or establish long-term team performance from a short trial.

---

## 2. Verification and Evaluation Objectives

### 2.1 Software Verification Objectives

**VO-01:** Verify correct authentication and authorization behavior.

**VO-02:** Verify participant profile creation, modification, and access restrictions.

**VO-03:** Verify team creation, invitations, membership rules, and team confirmation.

**VO-04:** Verify correct and reproducible multi-criteria matching behavior.

**VO-05:** Verify the Trial Sprint lifecycle, task handling, feedback, and confirmation procedures.

**VO-06:** Verify hackathon creation, registration, and deadline enforcement.

**VO-07:** Verify team workspace and project submission functionality.

**VO-08:** Verify privacy and protection of restricted participant information.

**VO-09:** Measure selected performance and capacity characteristics.

**VO-10:** Verify that the implemented functionality corresponds to documented acceptance criteria.

### 2.2 Research Evaluation Objectives

**EO-01:** Compare the proposed multi-criteria matching method against a skill-based baseline.

**EO-02:** Measure selected team composition characteristics produced by different recommendation methods.

**EO-03:** Investigate whether Trial Sprint provides useful additional information for team confirmation decisions.

**EO-04:** Assess participants' perceived recommendation suitability and transparency.

**EO-05:** Examine preliminary collaboration indicators, including task completion, deadline adherence, and participant feedback.

**EO-06:** Evaluate matching execution time under controlled conditions.

**EO-07:** Identify limitations and threats to the validity of the evaluation.

### 2.3 Proposed Success Criteria

Software verification will be considered satisfactory for a defined release candidate when:

- All applicable Must Have requirements have verification evidence.
- All applicable mandatory acceptance criteria pass.
- No unresolved critical security or data integrity defects remain.
- Core end-to-end workflows complete successfully.
- Any unmet proposed performance targets are documented.
- Known limitations and deferred functionality are clearly identified.

Research evaluation will be considered properly conducted when:

- The evaluated methods and comparison conditions are documented.
- Evaluation metrics are operationally defined.
- Real participant data is collected only through approved procedures.
- Test data and research data are clearly distinguished.
- Results are analyzed without inventing or selectively reporting evidence.
- Negative and inconclusive outcomes are documented.
- Threats to validity are discussed.

These are procedural completion criteria, not claims that the proposed method will outperform the baselines.

---

## 3. Software Testing Strategy

### 3.1 Unit Testing

Unit testing will verify individual functions and business rules independently.

Primary targets include:

- Input validation.
- Matching score calculation.
- Criterion normalization.
- Matching weight validation.
- Candidate eligibility filtering.
- Team size restrictions.
- Deadline comparison.
- Trial Sprint state transitions.
- Task status transitions.
- Permission decision functions.

Unit tests should use deterministic inputs and explicitly defined expected outputs.

### 3.2 Integration Testing

Integration tests will verify interactions between application modules and persistence components.

Planned examples include:

- Authentication and profile management.
- Profiles and recommendation generation.
- Team creation and membership persistence.
- Trial Sprint and task management.
- Hackathon registration and team creation.
- Team workspace and project submission.
- Administrative role changes and access enforcement.

The tests must detect inconsistencies that isolated unit tests may not reveal.

### 3.3 Functional Testing

Functional tests will verify user-visible system behavior against the SRS.

They will cover:

- Successful workflows.
- Invalid inputs.
- Unauthorized operations.
- Missing or incomplete information.
- Duplicate requests.
- Deadline restrictions.
- Invalid state transitions.
- Empty result sets.

### 3.4 Security and Access Control Testing

Security verification will focus on:

- Authentication boundaries.
- Role-based authorization.
- Resource ownership.
- Session invalidation.
- Input validation.
- Protection of participant data.
- Trial Sprint feedback confidentiality.
- Research data export restrictions.
- Administrative permissions.

Security tests will be conducted against authorized test environments using synthetic accounts and test data.

### 3.5 Usability Testing

Usability evaluation will investigate whether representative participants can understand and complete essential tasks.

Potential tasks include:

1. Creating an account.
2. Completing a participant profile.
3. Discovering a hackathon.
4. Reviewing teammate recommendations.
5. Accepting or declining a team invitation.
6. Completing a Trial Sprint.
7. Confirming or declining a team.
8. Submitting a project.

Measurements may include task completion, observed difficulties, time on task, and participant feedback.

### 3.6 Performance Testing

Performance testing will examine:

- Standard API response times.
- Matching execution time.
- Behavior with larger candidate datasets.
- Application behavior under concurrent requests.
- Representative prototype capacity.

Proposed thresholds from the SRS are subject to technical validation.

No performance target is considered achieved until measured in a documented test environment.

### 3.7 Regression Testing

Regression tests will be rerun after changes affecting existing functionality.

The automated regression suite should cover critical business rules and essential application workflows.

Changes to the matching algorithm must also trigger relevant deterministic scoring and eligibility tests.

---

## 4. Testing Environment and Test Data

### 4.1 Environment Requirements

The testing environment should contain:

- A reproducible application build.
- An isolated test database.
- Documented application configuration.
- Representative test accounts.
- Synthetic participant profiles.
- Configured hackathon events.
- Matching algorithm test fixtures.
- Trial Sprint tasks and deadlines.
- Project submission test records.

The exact operating system, runtime, database configuration, and deployment infrastructure will be documented after architectural decisions are finalized.

### 4.2 Test Account Roles

Test accounts must cover the six roles defined in the SRS:

- Participant.
- Team Leader.
- Hackathon Organizer.
- Mentor.
- Judge.
- System Administrator.

Additional accounts should represent unauthorized users, unrelated team members, and participants with restricted access.

### 4.3 Test Data Categories

| Dataset | Purpose |
|---|---|
| Valid participant profiles | Normal profile workflows |
| Incomplete participant profiles | Missing-data handling |
| Duplicate accounts | Registration validation |
| Different skill combinations | Matching score verification |
| Overlapping schedules | Availability scoring |
| Non-overlapping schedules | Boundary and eligibility testing |
| Full teams | Membership constraint testing |
| Expired invitations | Invalid invitation testing |
| Trial Sprint activities | Collaboration workflow testing |
| Expired event deadlines | Registration and submission restrictions |
| Restricted feedback records | Privacy and authorization testing |

Synthetic data must not be presented as genuine participant research evidence.

### 4.4 Test Evidence

Each executed test should record:

- Test identifier.
- Requirement identifiers.
- Test environment.
- Test data.
- Execution date.
- Expected result.
- Actual result.
- Pass, Fail, Blocked, or Not Run status.
- Relevant logs, screenshots, or automated test reports.
- Defect reference where applicable.

---

## 5. Functional Test Scenarios

The following scenarios cover the Must Have functional requirements defined in `docs/requirements.md`.

The test cases are planned specifications, not executed results.

### 5.1 Authentication and Authorization

| Test ID | Requirements | Test Scenario | Expected Result |
|---|---|---|---|
| VT-01 | FR-01 | Register with valid participant data | Account is created without elevated permissions |
| VT-02 | FR-01 | Register with duplicate or invalid data | Request is rejected with appropriate validation |
| VT-03 | FR-02 | Authenticate using valid credentials | Authenticated session is established |
| VT-04 | FR-02 | Authenticate using invalid credentials | Authentication is rejected without sensitive disclosure |
| VT-05 | FR-03 | Log out and attempt to reuse the session | Terminated session cannot access protected resources |
| VT-06 | FR-05, FR-56 | Attempt protected actions with an unauthorized role | Server rejects unauthorized operations |

### 5.2 Participant Profile Management

| Test ID | Requirements | Test Scenario | Expected Result |
|---|---|---|---|
| VT-07 | FR-06 | Create and update a valid profile | Changes persist correctly |
| VT-08 | FR-07 | Add, modify, and remove skills and preferred roles | Updated information is stored |
| VT-09 | FR-08 | Create valid and invalid availability intervals | Valid intervals persist; invalid intervals are rejected |
| VT-10 | FR-09 | Modify experience and preferences | Information is updated and optional fields are supported |
| VT-11 | FR-10 | Request another participant's private attributes | Protected information is not disclosed |
| VT-12 | FR-11 | Record and retrieve eligible participation history | Records are correctly associated and protected |

### 5.3 Team Formation and Invitations

| Test ID | Requirements | Test Scenario | Expected Result |
|---|---|---|---|
| VT-13 | FR-13 | Create a team for an eligible event | Team is created with the initiating participant as leader |
| VT-14 | FR-14 | Define team role requirements | Valid requirements are stored |
| VT-15 | FR-15 | Invite an eligible participant | Valid invitation is created |
| VT-16 | FR-16 | Accept or decline an invitation | Membership reflects the participant's decision |
| VT-17 | FR-17 | Modify membership with authorized and unauthorized accounts | Only authorized modifications succeed |
| VT-18 | FR-18 | Attempt duplicate or conflicting membership | Configured membership constraints are enforced |

### 5.4 Multi-Criteria Matching

| Test ID | Requirements | Test Scenario | Expected Result |
|---|---|---|---|
| VT-19 | FR-19 | Request recommendations from eligible profiles | Ranked candidate list is produced |
| VT-20 | FR-19 | Request recommendations with no eligible candidates | Valid empty result is returned |
| VT-21 | FR-20 | Evaluate known normalized criterion inputs | Scores match the documented formula |
| VT-22 | FR-20 | Apply invalid weights or unsupported values | Invalid configuration is rejected |
| VT-23 | FR-21 | Include candidates violating mandatory constraints | Ineligible candidates are excluded |
| VT-24 | FR-22 | Repeat ranking with identical data and configuration | Ranking is reproducible |
| VT-25 | FR-23 | Inspect a recommendation explanation | Explanation matches actual scoring criteria |
| VT-26 | FR-24 | Decline a recommendation | No confirmed membership is created |
| VT-27 | FR-25 | Execute skill-only and multi-criteria baselines | Both methods produce reproducible comparison outputs |

### 5.5 Trial Sprint

| Test ID | Requirements | Test Scenario | Expected Result |
|---|---|---|---|
| VT-28 | FR-28 | Create a valid Trial Sprint | Trial is created for the correct temporary team |
| VT-29 | FR-29 | Accept or decline trial participation | Participation reflects explicit acceptance |
| VT-30 | FR-30 | Create and assign trial tasks | Tasks are correctly stored and assigned |
| VT-31 | FR-31 | Configure valid and invalid deadlines | Invalid deadlines are rejected |
| VT-32 | FR-32 | Update task status | Valid transitions persist; invalid states are rejected |
| VT-33 | FR-33, FR-39 | Complete tasks and inspect factual activity records | Eligible activities are accurately recorded |
| VT-34 | FR-34 | Submit structured participant reflection | Feedback is saved for the correct participant and trial |
| VT-35 | FR-35 | Confirm or decline final collaboration | Final membership follows the documented consent policy |
| VT-36 | FR-36 | Attempt unauthorized feedback access | Private feedback is protected |

### 5.6 Hackathon Management

| Test ID | Requirements | Test Scenario | Expected Result |
|---|---|---|---|
| VT-37 | FR-40 | Organizer creates a valid event | Event is stored |
| VT-38 | FR-41 | Organizer edits and publishes an event | Changes and publication state are persisted |
| VT-39 | FR-42 | Participant discovers published events | Only eligible visible events are returned |
| VT-40 | FR-43 | Participant registers for an event | Registration is recorded without duplication |
| VT-41 | FR-44 | Attempt registration outside the allowed period | Request is rejected |
| VT-42 | FR-45 | Organizer views registrations for assigned events | Authorized data is displayed; unrelated access is denied |

### 5.7 Team Workspace and Submissions

| Test ID | Requirements | Test Scenario | Expected Result |
|---|---|---|---|
| VT-43 | FR-46 | Confirmed team opens its workspace | Authorized members can access it |
| VT-44 | FR-47 | Create, assign, and update team tasks | Task changes are stored and visible |
| VT-45 | FR-48 | Submit a valid project | Submission is linked to the correct team and event |
| VT-46 | FR-48 | Attempt unauthorized or late submission | Request is rejected |
| VT-47 | FR-49 | Retrieve submission confirmation and status | Correct submission state is displayed |

### 5.8 Administration and Research Data

| Test ID | Requirements | Test Scenario | Expected Result |
|---|---|---|---|
| VT-48 | FR-56 | Authorized administrator changes a role | Role assignment is updated correctly |
| VT-49 | FR-56 | Participant attempts self-promotion | Unauthorized privilege escalation is rejected |
| VT-50 | FR-58 | Authorized researcher requests an approved export | Permitted research dataset is produced |
| VT-51 | FR-58 | Unauthorized account requests research data | Access is rejected |
| VT-52 | FR-59 | Perform a relevant administrative operation | Protected audit record is created |
| VT-53 | FR-60 | Accept or decline voluntary research participation | Consent decision is recorded and respected |

These scenarios provide planned coverage for every Must Have functional requirement in SRS version 0.1.

Should Have and Could Have functionality will receive additional tests if implemented.

---

## 6. Non-Functional Requirement Verification

| Test ID | Requirement | Verification Method | Proposed Acceptance Evidence |
|---|---|---|---|
| NVT-01 | NFR-01 | Credential storage inspection and authentication tests | No plaintext passwords or exposed secrets |
| NVT-02 | NFR-02 | Session lifecycle and CSRF tests | Invalidated sessions cannot access protected actions |
| NVT-03 | NFR-03 | Authorization and ownership tests | Unauthorized access is rejected |
| NVT-04 | NFR-04 | Input validation and malicious-input tests | Controlled errors and safe rendering |
| NVT-05 | NFR-05 | Data collection and API response inspection | Unnecessary private data is not exposed |
| NVT-06 | NFR-06 | Trial Sprint feedback access tests | Unauthorized feedback access is rejected |
| NVT-07 | NFR-07 | Deployment transport configuration inspection | Public authenticated traffic uses encrypted transport |
| NVT-08 | NFR-08 | Load testing | Proposed 95th-percentile response time under two seconds at 50 concurrent users |
| NVT-09 | NFR-09 | Matching benchmark | Proposed response within three seconds for up to 500 eligible profiles |
| NVT-10 | NFR-10 | Failure and transaction consistency tests | Failed operations leave consistent records |
| NVT-11 | NFR-11 | Backup and restoration exercise | Essential records can be restored |
| NVT-12 | NFR-12 | Prototype capacity testing | Representative workflows operate with 100 test users and 20 events |
| NVT-13 | NFR-13 | Task-based usability pilot | Core workflows are evaluated and usability defects documented |
| NVT-14 | NFR-14 | Keyboard and labeling inspection | Essential interfaces remain keyboard operable |
| NVT-15 | NFR-15 | Browser and responsive interface testing | Essential flows work in the selected environments |
| NVT-16 | NFR-16 | Automated tests and code review inspection | Modular structure and critical business rule tests are present |
| NVT-17 | NFR-17 | Error handling and logging inspection | Errors remain diagnosable without exposing secrets |
| NVT-18 | NFR-18 | Research data access and consent inspection | Collection and access follow approved procedures |

### 6.1 Performance Testing Conditions

The proposed performance thresholds originate from the SRS and remain subject to review.

Each benchmark must document:

- Application version.
- Hardware and software environment.
- Candidate or user dataset size.
- Number of concurrent users.
- Test duration.
- Number of repetitions.
- Timing methodology.
- Observed failures.
- Median and 95th-percentile response times where applicable.

The performance test must distinguish backend processing time from total browser interaction time.

### 6.2 Reliability Testing

Reliability testing will examine interrupted requests, duplicate operations, and inconsistent state transitions.

Examples include:

- Two simultaneous attempts to accept a final team position.
- Repeated submission of the same registration request.
- Failure during membership creation.
- Interrupted project submission.
- Unauthorized modification of task history.

The system should preserve data integrity according to its defined transaction and duplication policies.

---

## 7. Detailed Matching Algorithm Verification

### 7.1 Proposed Scoring Formula

The initial matching model is defined as:

`S = w1 × R + w2 × A + w3 × E + w4 × P`

Where:

- `R` = skill and role coverage.
- `A` = availability overlap.
- `E` = experience complementarity.
- `P` = working preference alignment.

Each normalized criterion is expected to lie in the interval `[0, 1]`.

The proposed weights must be non-negative and sum to one.

### 7.2 Deterministic Example

For illustration, consider the following test-only configuration:

- `w1 = 0.40`
- `w2 = 0.30`
- `w3 = 0.20`
- `w4 = 0.10`

| Criterion | Candidate A | Candidate B |
|---|---:|---:|
| Role coverage | 0.80 | 0.60 |
| Availability | 0.50 | 1.00 |
| Experience | 1.00 | 0.50 |
| Preferences | 0.50 | 1.00 |
| **Expected score** | **0.72** | **0.74** |

Expected result: Candidate B ranks above Candidate A for this test configuration.

These inputs and weights are illustrative fixtures, not validated weights for HackTeam.

### 7.3 Algorithm Boundary Cases

Additional unit tests should examine:

- All criteria equal to zero.
- All criteria equal to one.
- Invalid negative weights.
- Weights that do not sum to one.
- Missing optional profile information.
- Equal scores.
- No eligible candidates.
- Mandatory role requirements not satisfied.
- Conflicting availability.
- Repeated requests with identical data.

### 7.4 Reproducibility

The implementation must preserve enough configuration information to reproduce its outputs.

The test report should record the algorithm version, weights, normalization rules, input dataset, and resulting candidate order.

---

## 8. Research Evaluation Design

### 8.1 Research Question

The primary research question is:

**Does combining multi-criteria teammate recommendations with preliminary collaboration assessment provide additional useful information for student hackathon team formation?**

The study should distinguish algorithmic matching quality from the effects of Trial Sprint.

### 8.2 Comparison Approaches

Three approaches are proposed.

| Approach | Description | Purpose |
|---|---|---|
| **B0 — Skill-Based Matching** | Candidates ranked using skill and role information | Initial baseline |
| **B1 — Multi-Criteria Matching** | Candidates ranked using skills, roles, availability, experience, and preferences | Evaluate additional matching criteria |
| **B2 — Multi-Criteria Matching + Trial Sprint** | The same initial recommendations as B1, followed by preliminary collaboration before final confirmation | Evaluate the potential added information from Trial Sprint |

The initial candidate rankings for B1 and B2 should be identical when generated from the same profiles and matching configuration.

B2 differs by introducing a collaborative decision-support stage, not by automatically changing the original algorithm.

This separation is essential for valid interpretation.

### 8.3 Two-Part Evaluation

#### Part A — Offline Algorithm Comparison

The same synthetic or appropriately authorized profile dataset will be used for B0 and B1.

The evaluation will compare:

- Required role coverage.
- Availability overlap.
- Candidate ranking behavior.
- Algorithm execution time.
- Sensitivity to criterion weights.

Synthetic data can demonstrate mathematical and computational behavior but cannot prove real-world team compatibility.

#### Part B — Trial Sprint Pilot

Volunteer participants may review recommended teammates and complete structured preliminary collaboration activities.

Potential measurements include:

- Perceived suitability before Trial Sprint.
- Confidence in team selection before Trial Sprint.
- Task completion and coordination observations.
- Participant feedback after Trial Sprint.
- Confidence in final team selection after Trial Sprint.
- Willingness to continue working with the proposed team.

If adequate recruitment and resources are available, a comparison condition without Trial Sprint may be introduced.

Otherwise, a single-group before-and-after pilot may be used as an exploratory feasibility study.

A before-and-after design alone cannot establish that observed changes were caused by Trial Sprint.

### 8.4 Experimental Participants

Participants should be recruited voluntarily from the intended student population.

Eligibility and exclusion criteria should be defined before recruitment.

Potential eligibility requirements include:

- Enrollment as a student.
- Interest in hackathon participation.
- Ability to complete the selected evaluation activities.
- Informed agreement to the research procedures.

The final sample size will be determined according to feasibility, recruitment, research objectives, and supervisor guidance.

No participant recruitment or experimental data collection is claimed to have occurred.

### 8.5 Experimental Conditions

To support fair comparison:

1. Matching algorithms should receive equivalent permitted input data.
2. Both methods should use the same team size and eligibility constraints.
3. Baseline definitions must be fixed before results are inspected.
4. Initial scoring configurations must be documented.
5. Trial Sprint tasks should be similar in difficulty and duration.
6. Participants should receive consistent task instructions.
7. Evaluation questions should use comparable wording.
8. Results should distinguish profile-based scores from participant perceptions.
9. Missing data and withdrawals should be reported.
10. The analysis should document possible prior familiarity between teammates.

Where feasible, random allocation to evaluation conditions can reduce selection bias.

If random assignment is not feasible, the evaluation must explicitly acknowledge potential confounding.

---

## 9. Evaluation Metrics

### 9.1 Team Formation Success Rate

**Definition:** The proportion of initiated team formation attempts that result in a confirmed team within a predefined observation window.

**Formula:**

`Team Formation Success Rate = Confirmed Team Formations / Eligible Team Formation Attempts × 100%`

The study must define what constitutes an eligible attempt and prevent duplicate attempts from inflating the denominator.

This metric describes confirmation activity, not long-term team success.

### 9.2 Project Completion Rate

**Definition:** The proportion of eligible confirmed teams that submit a completed project according to predefined event requirements.

**Formula:**

`Project Completion Rate = Completed Eligible Submissions / Eligible Confirmed Teams × 100%`

This metric can only be calculated when actual project completion data is available.

It may remain unavailable during a short preliminary pilot.

### 9.3 Task Completion Within Deadlines

**Definition:** The proportion of eligible assigned tasks completed by their agreed deadlines.

**Formula:**

`On-Time Task Completion Rate = Tasks Completed On Time / Eligible Assigned Tasks With Deadlines × 100%`

The evaluation should document whether tasks have similar difficulty and clearly agreed completion conditions.

### 9.4 Team Member Replacement Frequency

**Definition:** The number of membership replacements observed after team confirmation.

Potential reporting formats include:

- Total replacements.
- Average replacements per confirmed team.
- Proportion of teams experiencing at least one replacement.

The measurement period must be documented.

A short observation period may not provide meaningful evidence for this metric.

### 9.5 Participant Satisfaction

**Definition:** Participants' reported satisfaction with the matching or preliminary collaboration process.

A proposed five-point questionnaire scale may be used:

1. Strongly disagree.
2. Disagree.
3. Neither agree nor disagree.
4. Agree.
5. Strongly agree.

Possible statements include:

- The teammate recommendations were understandable.
- The suggested participants appeared suitable for the required roles.
- The team formation process was easy to use.
- The Trial Sprint helped me understand how the team could collaborate.
- I felt able to decide whether to continue with this team.

Individual questions should be analyzed separately unless a valid combined scale has been established.

### 9.6 Matching Execution Time

**Definition:** The time required to generate a recommendation result under a specified test configuration.

Report:

- Median execution time.
- 95th-percentile execution time.
- Candidate dataset size.
- Matching configuration.
- Number of repetitions.
- Test environment.

This metric evaluates computational behavior, not team suitability.

### 9.7 Role Coverage

**Definition:** The proportion of required team roles satisfied by the candidate composition.

**Formula:**

`Role Coverage = Covered Required Role Slots / Total Required Role Slots`

A role-slot definition must be established before testing.

### 9.8 Availability Overlap

**Definition:** The amount of shared available time among proposed team members during a predefined planning period.

Possible measurement:

`Availability Overlap = Number of Shared Available Time Slots`

Time slot duration, timezone handling, and observation period must be consistent across compared methods.

### 9.9 Perceived Decision Confidence

**Definition:** Participants' perceived confidence in deciding whether to confirm a proposed team.

Confidence may be recorded before and after Trial Sprint using the same five-point response scale.

**Exploratory Change:**

`Confidence Change = Post-Trial Confidence − Pre-Trial Confidence`

An observed increase would represent a change in reported confidence, not proof of objectively improved team compatibility.

### 9.10 Metrics Summary

| Metric | Source | Measurement Stage | Main Limitation |
|---|---|---|---|
| Team formation success rate | Membership events | After confirmation window | Does not demonstrate performance |
| Project completion rate | Submission records | After hackathon completion | May be unavailable in early pilots |
| On-time task completion | Task records | During Trial Sprint or project | Task difficulty varies |
| Member replacement frequency | Membership history | After confirmation | Requires sufficient observation time |
| Participant satisfaction | Voluntary questionnaire | After recommendation or trial | Self-report bias |
| Matching execution time | System measurement | Algorithm benchmark | Hardware-dependent |
| Role coverage | Candidate/team dataset | Offline comparison | Depends on role definitions |
| Availability overlap | Participant schedule data | Offline comparison | Self-reported availability |
| Decision confidence | Participant questionnaire | Before and after Trial Sprint | Does not prove decision accuracy |

---

## 10. Data Collection and Management

### 10.1 Data Sources

Potential data sources include:

- Synthetic participant profiles.
- Consented participant profile attributes.
- Matching algorithm outputs.
- Team formation events.
- Trial Sprint task records.
- Project submission records.
- Voluntary questionnaires.
- Controlled usability observations.
- Software test logs and benchmark results.

### 10.2 Distinction Between Test and Research Data

**Synthetic Test Data**

Used for functional testing, boundary testing, and algorithm reproducibility.

**Real Research Data**

Collected from actual participants under appropriate informed consent and research procedures.

Synthetic observations must never be presented as actual participant experiences.

### 10.3 Proposed Research Dataset Fields

| Field | Description |
|---|---|
| Anonymous participant code | Pseudonymous identifier |
| Evaluation condition | B0, B1, or B2 |
| Matching configuration | Algorithm version and criterion weights |
| Recommendation rank | Candidate position |
| Role coverage | Calculated coverage |
| Availability overlap | Shared time measurement |
| Trial participation status | Whether the trial was completed |
| Task completion status | Recorded task outcomes |
| Confirmation decision | Participant's final choice |
| Satisfaction responses | Voluntary questionnaire responses |
| Execution time | Benchmark measurement |

Only approved data should be collected.

Directly identifying information should not be included in analytical datasets unless strictly required and authorized.

### 10.4 Research Consent

Research consent must be distinguished from ordinary platform account registration.

Participants should be informed about:

- Research purpose.
- Requested activities.
- Data collected.
- Potential risks.
- Voluntary participation.
- Withdrawal procedure.
- Data access.
- Retention policy.
- Reporting of aggregated results.

The exact consent and retention procedures must be finalized before empirical data collection.

### 10.5 Data Quality

The data preparation process should document:

- Missing values.
- Invalid records.
- Duplicate observations.
- Withdrawn participants.
- Incomplete questionnaires.
- Outliers.
- Exclusion criteria.
- Any transformations applied before analysis.

Exclusion decisions should not be based solely on whether results favor the proposed approach.

---

## 11. Analysis Plan

### 11.1 Descriptive Analysis

The initial analysis will report descriptive statistics such as:

- Counts and proportions.
- Means or medians.
- Standard deviations or interquartile ranges.
- Completion percentages.
- Response distributions.
- Matching execution time distributions.

Results will be accompanied by sample sizes.

### 11.2 Algorithm Comparison

B0 and B1 will be evaluated using equivalent candidate datasets and eligibility constraints.

Paired differences may be calculated for comparable recommendation tasks.

The analysis will examine whether the multi-criteria approach changes predefined outcomes such as role coverage, availability overlap, and recommendation rankings.

A higher composite matching score must not be used as independent proof of superiority when that score is defined by the proposed method itself.

### 11.3 Trial Sprint Analysis

For a before-and-after pilot, the analysis may compare participants' initial and final decision confidence.

Where appropriate, paired observations can be summarized and analyzed using methods consistent with the measurement scale and sample size.

If an adequately designed comparison group is available, differences between conditions may also be explored.

Statistical tests will be selected after the final experimental design is approved.

### 11.4 Statistical Interpretation

Where inferential testing is appropriate, the study should report:

- The statistical method.
- Sample size.
- Effect size where applicable.
- Confidence interval where feasible.
- Statistical significance results.
- Assumptions and limitations.

A small sample may support feasibility conclusions but not strong claims about effectiveness.

Exploratory findings should not be described as definitive evidence of causal improvement.

### 11.5 Reporting Negative or Inconclusive Findings

The evaluation must report:

- Outcomes supporting the hypotheses.
- Outcomes contradicting the hypotheses.
- Non-significant results.
- Missing observations.
- Implementation limitations.
- Incomplete or unsuccessful test scenarios.

Selective presentation of only positive results must be avoided.

---

## 12. Threats to Validity

### 12.1 Internal Validity

**Risk:** Differences between conditions may be caused by prior familiarity, skill differences, motivation, or task difficulty.

**Mitigation:** Use equivalent tasks and eligibility constraints, document participant characteristics, and use random allocation where feasible.

### 12.2 Construct Validity

**Risk:** Selected indicators may not measure the intended concept accurately.

For example, task completion does not fully measure compatibility, and message volume does not establish contribution quality.

**Mitigation:** Define indicators explicitly, use multiple sources of evidence, and avoid unsupported composite reliability scores.

### 12.3 External Validity

**Risk:** Results from a limited group of university volunteers may not generalize to other institutions or hackathons.

**Mitigation:** Describe the study population and avoid broad generalizations.

### 12.4 Statistical Conclusion Validity

**Risk:** Small samples may produce unstable estimates or insufficient statistical power.

**Mitigation:** Report effect sizes and uncertainty, avoid overstating insignificant or underpowered results, and treat small pilots as exploratory.

### 12.5 Selection Bias

**Risk:** Volunteers may be more motivated or experienced than typical participants.

**Mitigation:** Describe recruitment procedures and participant characteristics.

### 12.6 Learning and Familiarity Effects

**Risk:** Participants may report higher confidence after Trial Sprint simply because they spent more time together.

**Mitigation:** Measure prior familiarity, use appropriate comparisons if feasible, and avoid attributing all changes to the Trial Sprint mechanism.

### 12.7 Technical Measurement Bias

**Risk:** Matching performance may vary according to hardware, database state, and dataset structure.

**Mitigation:** Use repeatable configurations and report execution environments.

### 12.8 Missing or Incomplete Data

**Risk:** Withdrawals and incomplete trials may distort observed success rates.

**Mitigation:** Record missing data, report denominators, and document handling procedures.

---

## 13. Defect Management and Reporting

### 13.1 Defect Severity

| Severity | Description | Example |
|---|---|---|
| Critical | Serious security or data integrity failure | Unauthorized access to private feedback |
| High | Essential workflow cannot be completed | Eligible users cannot confirm team membership |
| Medium | Important behavior is incorrect but workaround exists | Incorrect sorting of eligible recommendations |
| Low | Minor usability or presentation problem | Misaligned interface element |

### 13.2 Defect Record

Each defect should contain:

- Unique defect ID.
- Related requirement and test case.
- Description.
- Reproduction steps.
- Expected result.
- Actual result.
- Severity.
- Environment.
- Supporting evidence.
- Assigned owner.
- Resolution status.

### 13.3 Planned Evidence Format

| Test ID | Date | Environment | Expected | Actual | Status | Evidence |
|---|---|---|---|---|---|---|
| VT-01 | Not executed | TBD | Account created | Not measured | Not Run | Pending |
| VT-21 | Not executed | TBD | Correct scores | Not measured | Not Run | Pending |
| VT-35 | Not executed | TBD | Correct final decision | Not measured | Not Run | Pending |
| NVT-09 | Not executed | TBD | Evaluate proposed threshold | Not measured | Not Run | Pending |

These rows illustrate the reporting format only.

No tests have been marked as passed without execution evidence.

---

## 14. Requirements Traceability Summary

The following matrix connects requirement groups from the SRS to planned tests.

### 14.1 Functional Requirements

| Requirement IDs | Testing Coverage |
|---|---|
| FR-01–FR-03 | VT-01–VT-05 |
| FR-05 | VT-06 |
| FR-06–FR-11 | VT-07–VT-12 |
| FR-13–FR-18 | VT-13–VT-18 |
| FR-19–FR-25 | VT-19–VT-27 |
| FR-28–FR-36 | VT-28–VT-36 |
| FR-39 | VT-33 |
| FR-40–FR-45 | VT-37–VT-42 |
| FR-46–FR-49 | VT-43–VT-47 |
| FR-56 | VT-06, VT-48–VT-49 |
| FR-58 | VT-50–VT-51 |
| FR-59 | VT-52 |
| FR-60 | VT-53 |

All Must Have functional requirements in SRS version 0.1 are covered by planned verification scenarios.

The remaining requirements are assigned Should Have or Could Have priorities and will be incorporated into the test suite if implemented.

### 14.2 Non-Functional Requirements

| Requirement IDs | Testing Coverage |
|---|---|
| NFR-01–NFR-07 | NVT-01–NVT-07 |
| NFR-08–NFR-09 | NVT-08–NVT-09 |
| NFR-10–NFR-12 | NVT-10–NVT-12 |
| NFR-13–NFR-15 | NVT-13–NVT-15 |
| NFR-16–NFR-18 | NVT-16–NVT-18 |

The final implementation report must update this matrix to indicate completed tests, outcomes, defects, and any deferred requirements.

---

## 15. Team Responsibilities

### 15.1 Rakhmetulla Madina

Primary responsibilities:

- Multi-Criteria Matching verification.
- Trial Sprint workflow testing.
- Research evaluation methodology.
- Evaluation metrics and instruments.
- Algorithm baseline comparison.
- Analysis and reporting of research results.

### 15.2 Talasbek Kassymbek

Primary responsibilities:

- Hackathon creation and registration tests.
- Team workspace testing.
- Task and deadline management verification.
- Project submission testing.
- Event workflow integration tests.

### 15.3 Yergalyuly Daniyar

Primary responsibilities:

- Authentication and authorization tests.
- Backend integration tests.
- Administrative access verification.
- Security and privacy testing.
- Performance and infrastructure verification.
- Test environment and operational support.

### 15.4 Shared Responsibilities

All developers are responsible for:

- Reviewing relevant testing procedures.
- Maintaining tests for their modules.
- Supporting integration and regression testing.
- Recording defects and verification evidence.
- Reviewing Pull Requests.
- Resolving critical issues before release.
- Preparing demonstration and evaluation materials.

---

## 16. Planned Evaluation Deliverables

Future implementation and research activities should produce the following artifacts:

| Deliverable | Expected Content |
|---|---|
| Test Suite | Automated and manual verification cases |
| Test Execution Report | Results, evidence, and defect summaries |
| Matching Benchmark | Execution times and dataset configuration |
| Algorithm Comparison | Baseline and multi-criteria results |
| Trial Sprint Pilot Protocol | Participant activities and evaluation instruments |
| Consent Materials | Research participation information and permissions |
| Evaluation Dataset | Approved and appropriately protected observations |
| Research Results | Metrics, analysis, and limitations |
| Final Evaluation Report | Interpretation of the findings and research conclusions |

The existence of this plan does not imply that these deliverables have already been produced.

---

## 17. Risks and Mitigation

| Risk | Potential Impact | Proposed Mitigation |
|---|---|---|
| Insufficient testing time | Incomplete verification | Prioritize Must Have workflows |
| Delayed implementation | Tests cannot be executed | Prepare test definitions before development |
| Insufficient research volunteers | Limited evaluation evidence | Recruit early and document sample limitations |
| Incomplete participant profiles | Weak algorithm comparison | Handle missing information explicitly |
| Unequal experimental conditions | Biased comparison | Standardize inputs and tasks |
| Short Trial Sprint duration | Limited predictive validity | Evaluate feasibility and perceived usefulness |
| Sensitive data exposure | Ethical and privacy concerns | Apply consent and access controls |
| Small sample size | Uncertain statistical estimates | Report limitations and uncertainty |
| Unrealistic performance thresholds | Unmet targets | Validate targets against resources |
| Poor requirements traceability | Unverified functionality | Maintain test-to-requirement mapping |

---

## 18. Review and Approval Checklist

- [x] Testing objectives are defined.
- [x] Unit, integration, functional, security, usability, and performance testing are included.
- [x] Main system test scenarios are documented.
- [x] Planned tests cover Must Have functional requirements.
- [x] Non-functional requirement verification is documented.
- [x] Baseline matching approaches are identified.
- [x] Evaluation metrics are explicitly defined.
- [x] Experimental conditions are described.
- [x] Data collection and privacy considerations are included.
- [x] Threats to validity are identified.
- [x] Expected outcomes are distinguished from validated findings.
- [x] Team responsibilities are documented.
- [ ] All three team members have reviewed the plan.
- [ ] Experimental procedures have been reviewed by the academic supervisor where required.
- [ ] Outstanding scope and methodology decisions have been recorded.
- [ ] The document has been approved through a GitHub Pull Request.

---

## 19. Conclusion

This Verification and Evaluation Plan establishes a structured approach for assessing the technical correctness and research-oriented functionality of the HackTeam platform.

The software verification component defines testing strategies, functional test cases, non-functional verification procedures, requirement traceability, and defect management practices.

The research evaluation component defines a comparative framework involving skill-only matching, multi-criteria matching, and multi-criteria matching combined with Trial Sprint.

The proposed evaluation distinguishes algorithmic composition metrics, participant experiences, observable collaborative activities, and potential project outcomes.

The plan emphasizes transparent procedures, reproducible measurements, appropriate participant consent, and cautious interpretation of findings.

No experimental outcomes or software performance results are claimed before testing has been conducted.

This document will guide subsequent software implementation, system verification, pilot evaluation, research analysis, and final diploma reporting.

---

**Document Status:** Draft version 0.1 prepared for team and academic supervisor review. Test procedures, experimental conditions, sample size, and evaluation thresholds will be refined as the HackTeam implementation and research design progress.
