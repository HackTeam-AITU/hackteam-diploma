# HackTeam — Supervisor Feedback and Team Response

**Institution:** Astana IT University  
**Program:** Software Engineering  
**Project:** HackTeam — Hackathon Management and Student Team Formation Web System  
**Academic supervisor:** Myrzakerimova Alua Bauyrzhankyzy  
**Students:** Rakhmetulla Madina Bauyrzhankyzy; Talasbek Kassymbek Arystanbekuly; Yergalyuly Daniyar  
**Stage:** First pre-defense  
**Document prepared:** 24 October 2026  
**Feedback status:** Student-drafted feedback approved in principle by the supervisor, as reported by the team; this is not a signed or verbatim statement.  
**Implementation status:** Documentation refinements prepared; GitHub review/merge of these refinements must be recorded separately.

## 1. Purpose and scope of review

This record addresses the first pre-defense requirement to document substantive supervisor feedback on key deliverables **and** the team's decisions and improvements resulting from the review. The feedback wording was prepared by the students and, according to the team, agreed to by the academic supervisor. It is presented as an approved summary rather than a direct quotation, signature, or independent record of a meeting. The date and medium of the supervisor's confirmation have not been separately documented.

The review concerns research, requirements, architecture, UX design, and project planning. It does not evaluate a completed application or results of experiments that have not yet been performed.

### Deliverables considered

| Area | Existing project evidence |
|---|---|
| Problem and scope | [Project Proposal](project-proposal.md) |
| Scientific basis | [Literature Review](literature-review.md) |
| User needs | [User Research](user-research.md) — three exploratory student interviews |
| Alternatives | [Competitor Analysis](competitor-analysis.md) and [Technology Comparison](technology-comparison.md) |
| Software design | [Requirements Specification](requirements.md) and [System Architecture](architecture.md) |
| User experience | [UX/UI Prototype](ux-prototype.md) — interactive Figma prototype and exported screens |
| Research/testing | [Verification and Evaluation Plan](evaluation-plan.md) |
| Planning | [Project Management, Milestones and Risks](project-management-risks.md) |

All these deliverables were created before this feedback response; their prior existence is **not** presented as evidence of changes caused by the review.

## 2. Academic supervisor feedback — approved summary

### 2.1 General assessment

HackTeam addresses the relevant issue of forming student teams for hackathons when prospective teammates may differ in skills, roles, availability, and expectations about collaboration. The proposed web system integrates hackathon management with a transparent multi-criteria team formation approach and a preliminary collaboration mechanism named **Trial Sprint**.

The team has prepared an organized set of initial research and design materials, including a project proposal, literature review, user interviews, competitor and technology comparisons, requirements, architecture diagrams, UX/UI prototype, evaluation plan, and project roadmap. The responsibilities of the three developers are distinguishable, and the use of YouTrack and reviewed GitHub Pull Requests provides traceability of the work.

These materials form a reasonable foundation for implementation. However, a documented proposal and prototype do not yet demonstrate software correctness, superiority of the matching method, or the effectiveness of Trial Sprint. The scientific contribution must be supported by a reproducible method and appropriate evaluation rather than by ordinary platform functionality alone.

### 2.2 Strengths

- The project addresses a concrete user need and connects software features to a documented problem statement.
- The research focus is identifiable: transparent multi-criteria matching and assessment of preliminary team interaction.
- The initial student research identifies priorities, while openly recognizing limitations of a three-interview sample.
- Architecture, functional requirements, and technology comparison provide a starting point for technical implementation.
- The UX prototype covers the intended participant and organizer journeys.
- Project milestones, team responsibilities, risks, and planned verification activities are documented.

### 2.3 Substantive recommendations

**SF-01 — Scientific contribution.** Specify the matching procedure more precisely: eligibility constraints, normalized criteria, weights, ranking rules, missing-data handling, and explainability. Distinguish a proposed deterministic decision-support method from claims about predicting a person's reliability or eventual success.

**SF-02 — Research evaluation.** Preserve a clear comparison between **B0 (skill-based matching)**, **B1 (multi-criteria matching)**, and **B2 (multi-criteria matching plus Trial Sprint)**. Use comparable inputs and documented metrics, and report negative or inconclusive results rather than assuming improvement.

**SF-03 — Trial Sprint.** Define a feasible, voluntary short collaboration workflow, participant consent and decision points, observable evidence, and limitations. A brief exercise should not become an automatic or opaque reliability rating.

**SF-04 — Scope and feasibility.** Prioritize essential team discovery, invitations, hackathon, task, submission, and evaluation-support workflows. Defer nonessential reputation scoring, advanced analytics, external integrations, and other optional features until the core system operates correctly.

**SF-05 — Architecture and privacy.** Align module boundaries, API contracts, role-based access control, ownership rules, database integrity, and appropriate controls on personal and research data. Validate architectural decisions during implementation.

**SF-06 — User validation.** Review the participant and organizer paths in the prototype and collect actual feedback on navigation, matching explanations, Trial Sprint choices, validation errors, and mobile readability. Do not present a design prototype as a tested application.

**SF-07 — Project tracking.** Maintain clear responsibilities, milestone dependencies, risk mitigation, review records, and evidence of implemented improvements. Distinguish planned changes from revisions actually reviewed and merged.

### 2.4 Overall assessment

The project is suitable for continued development on the basis of the initial documentation. The next stage should concentrate on a working MVP, implementation of the proposed methods, integration and security testing, and research evaluation. Final conclusions must be supported by actual observations and appropriately stated limitations.

## 3. Student decisions and substantive refinements

The team accepts the above recommendations and has prepared two concrete documentation refinements for review with this record:

1. **[Research Design and MVP Refinements](research-design-refinements.md)** — makes the algorithm workflow, comparison logic, voluntary Trial Sprint, MVP priorities, privacy constraints, and acceptance checks more explicit.
2. **[Updated repository README](../README.md)** — replaces an obsolete "technology selection is in progress" statement with the documented *proposed* stack, reflects the current first pre-defense deliverables, describes research boundaries, and links to the relevant documents.

The refinements below describe **prepared documentation changes**. They become merged project improvements only when the corresponding GitHub Pull Request is approved and merged.

| Feedback | Concrete refinement prepared | Evidence within the submitted changes | Owner | Status at document preparation |
|---|---|---|---|---|
| SF-01 | Defined an eligibility-first, deterministic ranking pipeline; separated hard constraints from weighted preferences and specified how uncertainty should be represented. | [Research refinements §2–3](research-design-refinements.md) | Madina | Document prepared; implementation pending |
| SF-02 | Made B0/B1/B2 comparison conditions and the difference between algorithmic and collaboration outcomes explicit. | [Research refinements §4](research-design-refinements.md) | Madina | Protocol clarified; experiments pending |
| SF-03 | Described consent, opt-in/skip, small task, observation, reflection, and final confirmation; no automatic moral/reliability score. | [Research refinements §5](research-design-refinements.md) | Madina | Workflow clarified; pilot pending |
| SF-04 | Established a staged MVP order and explicit deferred items. | [Research refinements §6](research-design-refinements.md) and [README](../README.md) | All members | Priorities documented; development pending |
| SF-05 | Defined backend authorization, privacy boundaries, ownership checks, and integration gates. | [Research refinements §7](research-design-refinements.md) | Daniyar | Technical checks specified; implementation pending |
| SF-06 | Defined concrete Figma walkthrough questions and evidence for future user reviews. | [Research refinements §8](research-design-refinements.md) | Kassymbek | Review protocol documented; observations pending |
| SF-07 | Added evidence and progress-status rules so completed documentation is not confused with implemented functionality. | [Research refinements §9](research-design-refinements.md) and [README](../README.md) | Daniyar | Reporting rules documented; future tracking ongoing |

## 4. How the feedback led to meaningful improvements

The review prompted the team to clarify three substantive aspects rather than merely change wording:

1. **Method and measurement:** recommendations now map to a specified eligibility-and-ranking pipeline and to explicit B0/B1/B2 comparison conditions, preventing evaluation of Trial Sprint as though it were a different ranking algorithm.
2. **Scope and ethical safeguards:** Trial Sprint is described as optional decision support with limited, transparent evidence; unavailable profile information, newcomers, and private feedback must not automatically produce negative reliability judgments.
3. **Verifiable delivery:** the MVP has clearer development gates, security and UX review conditions, and a distinction between existing documentation, prepared revisions, implemented software, and validated research findings.

These are **design and documentation refinements**. The team has not yet executed the experiments, run the pilot, completed the backend, or validated these proposed mechanisms in production.

## 5. Follow-up implementation and evaluation actions

| ID | Next verifiable action | Responsible member | Evidence needed to mark complete |
|---|---|---|---|
| A-01 | Implement deterministic filtering, scoring, explanations, and missing-data cases. | Madina | Algorithm source, tests, reproducible results |
| A-02 | Compare B0 and B1 on the same eligible candidate sets and record metrics. | Madina | Data description, versioned configurations, results |
| A-03 | Run a consent-based Trial Sprint pilot, if feasible, and report limitations. | Madina | Protocol, consent evidence, anonymized results |
| A-04 | Integrate login, ownership checks, team membership, and protected workflows. | Daniyar | API contracts, security and integration tests |
| A-05 | Build hackathon, workspace, and submission flows and connect them to team state. | Kassymbek | Functioning workflows and test evidence |
| A-06 | Review the Figma participant/organizer journeys with actual users or reviewers. | Kassymbek | Dated feedback and recorded revisions |
| A-07 | Track progress, risks, and feedback-linked Pull Requests in YouTrack/GitHub. | All members | Issue and PR links, updated milestones |

No implementation or research task in this table is claimed completed unless the linked evidence exists.

## 6. Review and revision record

| Field | Record |
|---|---|
| Academic supervisor | Myrzakerimova Alua Bauyrzhankyzy |
| Supervisor feedback wording | Agreed in principle, according to the team's report |
| Exact review/confirmation date | Not separately recorded |
| Verbatim comments or signed assessment | Not supplied; this document is a student-prepared summary |
| Team decisions | Recorded in §§3–5 |
| Documentation refinements | Prepared as part of the first pre-defense finalization work |
| GitHub PR for these refinements | To be added after the team opens and merges it |
| Software implementation and experimental findings | Planned; not claimed at this stage |

If the university requires written confirmation, the team should attach or reference the supervisor's actual confirmation without representing this record as her signature.

## 7. Conclusion

The supervisor-approved feedback summary and the team's response provide a traceable basis for refining HackTeam's method, MVP scope, security design, and verification strategy. The proposed changes are specific and testable; subsequent implementation and research results must be recorded separately as they occur.
