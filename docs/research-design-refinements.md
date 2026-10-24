# HackTeam — Research Design and MVP Refinements

**Prepared for:** First pre-defense, 24 October 2026  
**Context:** Refinements following supervisor-approved review recommendations (see [Supervisor Feedback](supervisor-feedback.md))  
**Document type:** Design clarification; not an implemented or empirically validated algorithm  
**Project owners:** Madina (matching and Trial Sprint), Kassymbek (hackathon workflows and UX), Daniyar (backend, integration, security)

## 1. Research contribution and boundaries

The proposed research contribution is a **transparent method for multi-criteria student team formation**, supported by an optional **Trial Sprint** preliminary collaboration stage within a functional hackathon management web system. The web platform is the practical environment in which the method can be built and tested, not the sole scientific contribution. AI-based recommendations are not required for the core method.

Two claims must be evaluated separately:

1. Whether adding non-skill criteria affects measurable team composition indicators and participants' selection decisions compared with a skill-based approach.
2. Whether a limited Trial Sprint gives prospective teammates useful additional information before confirming membership, relative to using matching recommendations alone.

Neither claim is regarded as proven by the initial interviews or UX prototype.

## 2. Proposed deterministic matching pipeline

This section clarifies the planned procedure described in the [Project Proposal](project-proposal.md) and [Evaluation Plan](evaluation-plan.md).

**Step 1 — Confirm event and user context.** Identify the hackathon, its registration and team constraints, the team requirements, and the participant's privacy choices.

**Step 2 — Apply hard eligibility rules.** Exclude or flag candidates who do not meet mandatory event eligibility, team-size or membership constraints, or explicit opt-in requirements. Ineligible candidates must not be made eligible by a high preference score. The exact rules will be derived from the approved requirements and event-specific policies.

**Step 3 — Calculate normalized criteria for eligible candidates.** Use the preliminary criteria in the proposal:

- `R` — coverage of required skills and team roles;
- `A` — overlap between declared availability and relevant team/event time windows;
- `E` — complementarity of relevant experience, without treating newcomers as inherently unreliable;
- `P` — alignment of stated working preferences.

All criteria are planned on a comparable range from `0` to `1`. Detailed normalization functions require separate implementation specification and test cases. Self-reported experience must not be mistaken for independently verified competence.

**Step 4 — Calculate recommendation score.** The initial design remains:

`S = w1 × R + w2 × A + w3 × E + w4 × P`

Weights are non-negative and sum to `1`. The weights `(0.40, 0.30, 0.20, 0.10)` used in the existing Evaluation Plan are **test fixtures**, not empirically validated optimum values.

**Step 5 — Explain the recommendation.** Present major contributing factors, known exclusions, and material gaps in profile information. An unknown attribute must be marked as **unknown**; it must not silently be interpreted as an actual observed value of zero. Any provisional handling of missing data must be documented and tested.

**Step 6 — Return stable results and preserve participant choice.** For identical eligible input data and configuration, ranking must be reproducible. Ties require a documented deterministic rule. Neither a score nor participation in Trial Sprint can automatically force team membership.

## 3. Specific algorithm verification checks

The following test design is now explicit:

| Test ID | Condition | Expected design behavior |
|---|---|---|
| MAT-01 | Same eligible profiles, weights, and configuration | Identical scores and stable ranking |
| MAT-02 | One required eligibility condition fails | Candidate excluded or identified as ineligible before ranking |
| MAT-03 | All weights non-negative and sum to one | Configuration accepted |
| MAT-04 | Negative weights or sum different from one | Invalid configuration rejected |
| MAT-05 | Missing optional profile criterion | Missing data visibly distinguished and handled by a documented rule |
| MAT-06 | Equal candidate scores | Deterministic tie behavior |
| MAT-07 | A candidate has no prior project history | No automatic untrustworthy label or penalty without a justified criterion |
| MAT-08 | Candidate withdraws or event registration closes | Eligibility re-evaluated according to event rules |
| MAT-09 | Criterion weights change | Ranking differences traceable to changed settings |
| MAT-10 | Recommendation explanation shown | User can inspect major matching factors rather than an opaque score |

These cases extend the **test specification**; they do not assert that application tests have run.

## 4. Evaluation approach and evidence boundaries

The three proposed conditions correspond to the [Evaluation Plan](evaluation-plan.md):

| Condition | Mechanism | What it helps evaluate |
|---|---|---|
| `B0` | Skill/role-based matching | Reference method |
| `B1` | Multi-criteria ranking (skills, roles, availability, experience, preferences) | Effect of adding criteria to rankings and composition |
| `B2` | The same B1 initial rankings, then optional Trial Sprint | Additional information contributed by preliminary collaboration |

**Offline comparison (B0 vs B1):** use the same candidate pool, event, eligibility constraints, recorded input data, and repeatable configurations. Report role coverage, availability overlap, ranking changes, runtime, and sensitivity to weights. Since B1 directly optimizes some of these criteria, increased coverage alone does **not** prove better real-world teamwork.

**Optional pilot (B1 vs B2):** initial candidate rankings must remain comparable. Study whether participants revise or confirm decisions after Trial Sprint, perceived usefulness, participation burden, task completion, and communication clarity. Do not equate self-reported confidence with objectively measured team success.

**Evidence quality:** the existing three interviews establish exploratory needs, not effect sizes or population-level demand. The planned evaluation must identify synthetic datasets separately from real consented participant data. Small samples require descriptive analysis and explicit uncertainty. Negative and inconclusive findings are reportable outcomes.

## 5. Trial Sprint — refined preliminary workflow

1. An eligible group receives a clear invitation to a proposed small collaborative exercise.
2. Each participant explicitly **accepts or declines**; declining does not automatically imply unreliability or prevent all other permitted team formation paths.
3. Participants see the task, deadline, expected effort, shared artifacts, and what feedback may be recorded.
4. The team conducts the activity through a simple task board or permitted external work link.
5. Observable information is recorded with context: assigned work, timestamps, deliverable completion, blockers, communication, and voluntary participant reflection.
6. Participants review the result and individually choose whether to confirm team membership.
7. Private feedback is accessible only to authorized participants; public reputation scores are not automatically inferred.

From the three interviews, participants expressed **different** effort preferences (approximately 1–4 hours of active work within roughly 1–3 days). These are exploratory design inputs, **not** a universally approved duration or a validated assessment interval. The pilot should test acceptability and permit different scenarios where feasible.

A Trial Sprint is **not** a psychological test, a character evaluation, or evidence that successful completion guarantees later collaboration quality.

## 6. MVP prioritization after review

The first usable end-to-end path should be:

`Account → Participant Profile → Discover Hackathon/Team → Eligibility and Matching → Apply/Invite → Optional Trial Sprint → Confirm Team → Basic Workspace → Submit Project`

Prioritization and dependency gates:

| Gate | Mandatory functional outcome | Dependency |
|---|---|---|
| G1 | Authentication, backend permissions, base schema | Backend foundation |
| G2 | Participant profiles and basic event/team discovery | G1 |
| G3 | Team creation, invitations, membership consistency | G1–G2 |
| G4 | Explainable matching and an initial skill-only baseline | G2–G3 |
| G5 | Optional Trial Sprint task, reflection, confirmation | G3–G4 |
| G6 | Team workspace, submission, and basic organizer workflow | G1–G5 as applicable |
| G7 | Integration tests, security verification, baseline comparison | Working components and approved research protocol |

**Deferred unless capacity permits:** detailed reputation scoring, broad third-party integrations, real-time video/chat, advanced judging/mentor dashboards, AI recommendations, dedicated Android/iOS applications, and large-scale optimization.

The core Trial Sprint remains part of the proposed academic project; what is deferred is extensive automation or a universal reliability score.

## 7. Architecture, security and ethical checks

The [Technology Comparison](technology-comparison.md) proposes **Java/Spring Boot**, **PostgreSQL**, **REST/JSON**, **OpenAPI**, and an initial **modular monolith**. **React/TypeScript** remains a candidate, not a separately validated decision. These are proposed choices, not a claim that the application has been implemented.

Implementation gates should check:

- Server-side authentication and role-/ownership-based permissions for event, team, trial, and submission operations.
- Transactional consistency of invitations, team membership, capacity limits, and submission deadlines.
- Appropriate access boundaries for private Trial Sprint feedback and participant profile fields.
- Clear separation between ordinary platform participation and voluntary research participation/consent.
- Test accounts, research data, retention decisions, and export permissions documented before collecting study results.
- API contracts and integration scenarios reviewed across the three owners.

## 8. UX review — observable acceptance evidence

The [UX/UI Prototype](ux-prototype.md) documents **18 principal desktop screens and mobile counterparts**, together with additional mobile states and navigation overlays. This is an interactive design artifact, not a deployed, tested web application.

A future review should ask participants and organizers to perform real walkthroughs of the following scenarios and record date, reviewer role, obstacle, decision, and revision:

1. Discover a hackathon, locate a suitable team, and understand matching explanations.
2. Send or respond to an invitation; distinguish provisional collaboration from confirmed membership.
3. Opt into or skip a Trial Sprint; understand task effort, deadlines, and who sees feedback.
4. Update a team task and submit a project; see clear validation and success states.
5. As organizer, create or edit an event, inspect teams, and navigate project evaluation.
6. Check mobile navigation, scrolling, error recovery, and text readability.

A review is only marked complete when actual observations are collected. Repository screenshots alone do not establish usability.

## 9. Evidence, traceability and next steps

**Already documented before this refinement:** proposal, comparison of alternatives, requirements, architecture, user research, prototype, evaluation plan, project roadmap and GitHub PR review history. These should not be falsely labelled as post-feedback work.

**Newly prepared design refinements:** this explicit eligibility/ranking procedure, test expectations, B0/B1/B2 interpretation boundary, voluntary Trial Sprint workflow, MVP gates, security checklist, and UX review protocol.

**Still planned:** implement algorithms and the system, execute tests and participant research, integrate components, and record actual outcome metrics.

**Evidence rule:** link any future completed item to its YouTrack issue, GitHub Pull Request, test output, approved supervisor decision, or user-research record. A draft protocol is evidence of planning, not of passing a test.
