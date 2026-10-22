# HackTeam — Competitor Analysis

**Issue:** [HACK-5 — Analyze Existing Hackathon Platforms](https://hackteam-aitu-2027.youtrack.cloud/issue/HACK-5)  
**Research date:** 22 October 2026  
**Scope:** Four platforms and ten consistent qualitative criteria.  
**Method:** Review of publicly accessible official documentation and vendor product material.

## 1. Purpose and main conclusion

This comparison examines Devpost, HackerEarth, Devfolio, and TAIKAI to inform the HackTeam diploma project. It investigates both established hackathon workflows and potential analogues to multi-criteria team formation, Trial Sprint, preliminary interaction assessment, and a Project Reliability Profile.

Existing systems already document event management, team membership, project submission, evaluation, and participation records in various forms. In particular, Devfolio documents verifiable Onchain Credentials and TAIKAI advertises a verifiable participation badge. Consequently, neither team formation nor participation evidence alone establishes HackTeam's uniqueness. [F6] [T1]

HackTeam's proposed contribution is a clearly specified and evaluated student team formation workflow: explicit selection criteria, a limited preliminary shared task before final team confirmation, a transparent review of collaboration, and participation evidence with appropriate context and controls. This remains a proposal to implement and evaluate, rather than proof of superior outcomes or an absolute first in the market.

## 2. Selection and research method

### 2.1 Selected systems

| Platform | Product scope used in this comparison | Reason for inclusion |
|---|---|---|
| Devpost | The public Devpost hackathon platform. | Relevant public hackathon, team-up, portfolio, and judging workflows. [D1] [D2] [D3] |
| HackerEarth | HackerEarth Hackathons and its participant workflows. | Relevant team browsing, declared skills, staged submissions, and event operations. Recruiting-assessment functionality is excluded. [H1] [H2] [H3] [H4] |
| Devfolio | Participant and university-organizer functionality described in its current guide. | Direct overlap with student hackathons, profiles, teams, project portfolios, and credentials. [F1] [F2] [F3] [F4] [F5] [F6] |
| TAIKAI | Publicly documented participant and organizer platform capabilities. | Relevant skill-based matchmaking, project submission, evaluation, and participation evidence. [T1] [T2] [T3] |

Four systems satisfy the required 3-5 platform range. They overlap with the target workflow sufficiently to support a common comparison. This is a focused selection, not a census of hackathon platforms or a survey of all team formation research.

Public Devpost and Devpost for Teams are separate offerings. Private-edition capabilities are not attributed automatically to the public product. Similarly, HackerEarth recruitment assessments and participant-built projects hosted on a platform are not treated as native hackathon features. [D5]

### 2.2 Evidence procedure

1. Identify official help, product, and guide pages covering organizers, participants, teams, submissions, and history.
2. Check the pages listed in Section 10 and use the same ten definitions for every system.
3. Distinguish manual browsing and invitations from documented recommendation or optimization methods.
4. Search the official domains for availability, compatibility, trial tasks, preliminary collaboration, and workspace-related terms.
5. Classify a capability only to the level supported by the source. Preserve uncertain cases.
6. Use the local [user research](user-research.md) to discuss proposed requirements, not as evidence of a competitor's features.

The review was conducted on 22 October 2026. Official guides are evidence of documented functionality; marketing pages and vendor blogs are treated as product descriptions, not independent performance measurements. A feature may depend on event configuration, product edition, or commercial arrangements not tested here.

### 2.3 Verification labels

- **V — Documented:** the source explicitly describes the capability at the scope stated in the cell.
- **P — Partial:** a component or related workflow is documented; the complete composite criterion is not verified.
- **U — Unknown / not verified:** the reviewed material does not establish the capability. This does not mean it is absent.

No absence label is used without explicit evidence. A profile field is not proof of an automatic matcher; a project page is not proof of task assignment; a participation credential is not proof of contribution quality or future reliability.

## 3. Consistent evaluation criteria

| ID | Criterion | Operational definition |
|---|---|---|
| C01 | Hackathon creation and management | Documented event setup, registration, timelines, organizer operations, or managed delivery. |
| C02 | Participant profiles | Participant information such as skills, experience, project links, or a persistent profile. Scope is stated explicitly. |
| C03 | Skill-based team discovery or matching | Finding or recommending potential teammates using declared skills or required roles. Manual discovery and automatic matching are distinguished. |
| C04 | Multi-criteria team formation | An explicit team selection or formation method combining independent dimensions such as skills, roles, availability, and goals. Multiple admission filters alone do not establish this method. |
| C05 | Participant availability assessment | Capturing or evaluating usable work time, schedule overlap, or event-specific time commitments for team formation. A looking-for-a-team flag or RSVP alone is insufficient. |
| C06 | Preliminary team collaboration | A documented small shared task and interaction review before final team confirmation. Ordinary event participation, chat, or project judging alone is insufficient. |
| C07 | Project workspace and task management | Shared project information plus evidence of task owners, task states, or progress/deadline coordination. Partial project tools are identified separately. |
| C08 | Project submission and evaluation | Submission of project artifacts and documented judging, scoring, shortlisting, or evaluation workflows. |
| C09 | Team/project participation history | Persistent project or participation records; any documented verification is stated separately from a generic portfolio. |
| C10 | User experience and accessibility | Documented participant flows and accessibility controls. This desk review does not assign usability or accessibility conformance scores. |

## 4. Structured comparison matrix

Each column uses the definitions above. Source identifiers link directly to official pages.

| ID | Criterion | Devpost — public | HackerEarth — Hackathons | Devfolio | TAIKAI |
|---|---|---|---|---|---|
| C01 | Event creation and management | **V:** hosting, registration, submissions, and judging. [D1] | **V:** documented hosting and managed operations; detailed self-service setup not assessed. [H4] | **V:** university setup and organizer workflows. [F1] [F9] | **V:** event pages, registration, timelines, and organizer operations. [T2] |
| C02 | Participant profiles | **V:** public portfolios with projects and hackathon submissions. [D3] | **V, basic event scope:** registration information and declared skills; a richer persistent portfolio was not verified. [H2] | **V:** skills, experience, education, and links. [F2] | **V:** profiles used in teammate discovery. [T3] |
| C03 | Skill-based discovery or matching | **P:** manual participant introductions and team-up requests; structured skill filtering or automatic matching **U**. [D2] | **V, manual:** browse registrants with declared skills and invite them; automated ranking **U**. [H1] | **U** for current skill-based discovery/matching. Invite-code team joining is documented separately. [F3] | **V:** skill-based search/matchmaking is described; implementation and ranking details **U**. [T3] |
| C04 | Explicit multi-criteria formation | **U** in the reviewed team-building material. [D2] | **U:** browsing skills is not proof of a multi-criteria method. [H1] | **U:** evaluation of team applications does not establish an automatic formation method. [F3] | **U:** documented skill matchmaking does not establish availability/goal weighting or team optimization. [T3] |
| C05 | Time availability assessment | **U:** teammate-seeking status is not schedule assessment. [D2] | **U** for usable time or schedule-overlap assessment. [H1] [H2] | **U:** RSVP and event preparation do not establish temporal compatibility assessment. [F8] | **U** for usable time, overlap, or commitment assessment. [T3] |
| C06 | Preliminary shared task before confirmation | **U:** invitations do not establish a trial-task stage. [D2] | **U:** idea/prototype rounds are not a verified pre-confirmation collaboration trial. [H3] | **U:** application and team-joining stages do not establish a shared trial task. [F3] [F8] | **U:** ordinary matchmaking and event collaboration do not establish this stage. [T2] [T3] |
| C07 | Workspace and task management | **P:** shared project pages and member invitations; task ownership/status board **U**. [D2] [D3] | **P:** team project drafts and artifacts; assignment/progress board **U**. [H1] [H3] | **P:** project records and submission management; team task assignment/status workflow **U**. [F4] [F9] | **P:** communication, submissions, and an advertised project-management tool; detailed task-owner/state workflow **U**. [T2] |
| C08 | Submission and evaluation | **V:** project submissions and configured judging. [D1] [D4] | **V:** staged submission and shortlisting; judging also described by the vendor. [H3] [H4] | **V:** project management and online/offline/sponsor judging. [F5] [F9] | **V:** submission dashboard, evaluation/voting, and leaderboard. [T2] |
| C09 | Participation/project history | **V:** projects and submitted hackathons in a portfolio; task-level reliability assessment **U**. [D3] | **U** for persistent hackathon contribution history in the reviewed participant guides. [H1] [H2] [H3] | **V:** linked hackathon projects and verifiable credentials; task-level reliability assessment **U**. [F4] [F6] | **V:** project-linked participation badge; task-level reliability assessment **U**. [T1] |
| C10 | UX and accessibility evidence | **P:** documented participant journey; tested usability and accessibility conformance **U**. [D2] | **P:** documented registration/team journey; tested usability and accessibility conformance **U**. [H1] [H2] | **P:** documented keyboard controls and participant flows; a full conformance assessment **U**. [F7] [F8] | **P:** described participant/organizer flows; tested usability and accessibility conformance **U**. [T2] [T3] |

### Interpretation notes

- **Team formation is not a differentiator by itself.** Every selected system documents a membership or teammate workflow at some level. [D2] [H1] [F3] [T3]
- **C03 is deliberately narrower than generic team creation.** The current Devfolio team-joining guide establishes invitations and event-mode rules; it does not by itself establish a skill-based discovery tool. Unknown is retained for that question. [F3]
- **C04 is not inferred from C03.** Selecting people by skills or reviewing a team application is different from documenting a team formation method that combines availability, goals, and role complementarity.
- **C05 concerns work time.** Seeking a team, confirming attendance, or making an event commitment is not equivalent to assessing members' overlapping schedules.
- **C07 uses a composite definition.** A partial label acknowledges useful project tools while preserving uncertainty about participant task assignment and progress management.
- **C10 does not rank actual usability.** Devfolio documents keyboard features, but no keyboard, screen-reader, contrast, or user-task audit was performed on any platform. Unknown is not a claim of poor accessibility. [F7]

## 5. Documented strengths and evidence boundaries

### 5.1 Devpost

**Strengths:** a documented public-event lifecycle, portfolio continuity, participant team-up messages, and configurable judging. These provide a substantial baseline for a student hackathon platform. [D1] [D2] [D3] [D4]

**Boundary:** the reviewed public-team workflow describes human contact and project membership. It does not establish the multi-criteria method or preliminary interaction task defined in C04 and C06. Detailed participant task management was not verified. Features of Devpost for Teams must be evaluated separately rather than assumed to apply. [D2] [D5]

### 5.2 HackerEarth

**Strengths:** its guides describe practical team administration, visible declared skills, invitations, project artifacts, and staged submissions. The vendor additionally describes hosted event operations and judging. [H1] [H3] [H4]

**Boundary:** recruiting assessments are outside this comparison. Prototype shortlisting evaluates event submissions, which is not evidence of a trial collaboration step before confirming a team. Persistent task-level contribution history and detailed team scheduling remain unverified here. [H3]

### 5.3 Devfolio

**Strengths:** direct relevance to university events, structured participant profiles, mode-dependent team workflows, organizer project handling, and judging. Linked projects and credentials provide particularly relevant prior art for participation history. [F1] [F2] [F3] [F4] [F5] [F6] [F9]

**Boundary:** existing credentials reduce the defensibility of claiming that verifiable participation is new. Team application assessment is not proof of a formation algorithm. The current sources reviewed do not establish temporal compatibility scoring or a preliminary shared task. Keyboard documentation is useful evidence, not a comprehensive accessibility certification. [F3] [F6] [F7]

### 5.4 TAIKAI

**Strengths:** documented skill matchmaking, integrated event operations, and a verifiable participation badge overlap with important parts of HackTeam. Its organizer page also describes communication and project-management capabilities. [T1] [T2] [T3]

**Boundary:** the reviewed descriptions do not disclose an availability-and-goal matching method, trial-task interaction review, or detailed task-level reliability assessment. The vendor's broad project-management description needs further verification before comparing individual task-management operations. [T2] [T3]

These are boundaries of available evidence, not assertions that undocumented functionality cannot exist.

## 6. Team formation and related mechanisms

### 6.1 Discovery, membership, and selection

The sources support different levels of team assistance: Devpost documents introductions and team-up messages; HackerEarth documents manual browsing with declared skills; Devfolio describes team creation and invite codes; TAIKAI explicitly describes skill-based matchmaking. These are useful existing capabilities and should not be collapsed into a single yes/no label for automatic matching. [D2] [H1] [F3] [T3]

A fair evaluation of HackTeam must explain what its method adds beyond these baselines. Candidate inputs include role coverage, relevant technologies, time availability, and expectations. The scoring or optimization procedure, explanation of recommendations, and any benefits must be specified and evaluated separately.

### 6.2 Trial Sprint and preliminary interaction assessment

No equivalent to the defined C06 mechanism was verified in the reviewed sources. The defensible statement is:

> This documentation review did not verify a pre-confirmation shared-task and interaction-review mechanism equivalent to the proposed Trial Sprint in the selected four product scopes.

This is a bounded evidence statement. It does not establish global absence, market uniqueness, or scientific novelty. Search terms may not match product terminology, and unreviewed, private, or newer features may exist.

Related but different workflows must be acknowledged:

- Invitations and team membership establish who is in a project; they do not themselves demonstrate a shared trial task. [D2] [F3]
- HackerEarth's idea/prototype stages provide evaluation during an event; the guide does not establish a preliminary compatibility assessment before final team membership. [H3]
- General event collaboration, mentoring, communication, or recruiting assessment does not automatically meet C06.

The proposed Trial Sprint should specify the decision point, task scope, effort, participant choice, observable interaction criteria, and final confirmation process. The interviews in [user-research.md](user-research.md) support conditional interest and differing effort preferences, not demonstrated effectiveness.

### 6.3 Project Reliability Profile and participation evidence

There are documented analogues:

| Existing mechanism | Relevant similarity | What it does not establish for this comparison |
|---|---|---|
| Devpost portfolio with project and submitted-hackathon history. [D3] | Persistent work and event context visible to prospective teammates. | Verified individual task performance or future collaboration reliability. |
| Devfolio linked hackathon projects and Onchain Credentials. [F4] [F6] | Project continuity and independently verifiable participation/achievement evidence. | A complete, validated measure of individual contribution or future reliability. |
| TAIKAI Proof of Participation badge. [T1] | Verifiable evidence associated with projects in which a person participated. | Task-level contribution quality, team-interaction assessment, or predictive reliability. |

Accordingly, verified participation history cannot be described as absent from existing platforms. The proposed profile should distinguish participation, contribution claims, supporting evidence, and interpretation. A credential can support a claim without establishing that a person will be a suitable teammate in every future context.

## 7. Proposed HackTeam differentiation

The following are design and research proposals, not implemented or verified advantages.

| Proposed feature | Concrete scope to define and evaluate | Relationship to existing evidence |
|---|---|---|
| Multi-criteria team formation | Combine relevant roles/skills with event-specific availability and expectations; explain recommendations and how criteria affect decisions. | Skill discovery already exists. The reviewed sources did not verify the full C04 method, which remains an opportunity for investigation rather than a proven market gap. |
| Trial Sprint | A small shared task before final confirmation, with a limited effort budget and clear participation rules. | A defined C06 equivalent was not verified in this review. Existing project stages and team invitations remain relevant alternatives. |
| Preliminary interaction assessment | Review communication, responsiveness, coordination, and fulfillment of agreements transparently, followed by a participant decision. | It must be distinguished from judging a final project or using a single task as an opaque reliability score. Its predictive value remains untested. |
| Verified project participation history | Record the type and source of evidence, describe contribution context, provide visibility and correction controls, and avoid penalizing missing history. | Existing portfolios, credentials, and badges are direct related mechanisms; verification alone is insufficient differentiation. |

A student focus, a unified interface, or team invitations also cannot establish uniqueness. Devfolio explicitly addresses university organizers, and existing systems already combine several stages of the hackathon lifecycle. [F1] [D1] [T2]

## 8. Competitive positioning and need

### 8.1 Proposed positioning statement

> HackTeam is a proposed student hackathon management system that combines explicit, multi-criteria teammate selection with a short preliminary collaboration stage before final team confirmation. It aims to make selection reasons and observed interaction understandable while retaining participation evidence with user-controlled visibility and correction. The diploma project will evaluate this workflow against simpler team formation alternatives.

This statement describes the intended contribution without claiming to be the only or first platform with team matching, collaboration, or verified participation.

### 8.2 Why the proposed system is worth investigating

The local [user research](user-research.md) reports role-fit difficulties, schedule and expectation differences, coordination issues, and a preference for clearer team discovery. Those needs motivate the proposed workflow for the studied student context. Three interviews do not establish market-wide demand.

The comparison shows that event hosting, profiles, invitations, submissions, judging, and participation evidence are established capabilities. HackTeam therefore needs to justify how its proposed selection and interaction-assessment method improves decisions, rather than present baseline features as novel.

A focused prototype can connect profile information, hackathon selection, team discovery, invitations, a preliminary shared task, review, and final confirmation. Any measured benefit must come from a future evaluation. This comparison alone does not demonstrate faster formation, stronger teams, or better project outcomes.

### 8.3 Scope implications

- Treat basic event and project workflows as necessary platform capabilities, not evidence of novelty.
- Prioritize understandable team discovery and criteria aligned with the interview findings.
- Keep Trial Sprint small and transparent; do not infer a universal duration from limited preferences.
- Specify participation evidence and correction rules before introducing broad reliability ratings.
- Include keyboard navigation and clear interaction states as design goals, then test them. Do not claim accessibility superiority from a desk comparison.

## 9. Limitations and verification gaps

1. This is a public-documentation review, not hands-on testing of organizer accounts or every event configuration.
2. The four-product selection is relevant but not exhaustive. It does not replace an academic literature review of team formation or establish scientific originality.
3. Sources can change. The conclusions describe the documented scope reviewed on 22 October 2026, rather than guaranteed features for every future account, event, or plan.
4. Vendor materials may emphasize strengths. Their claims are not independent benchmarks, usability measurements, or proof of outcome improvements.
5. Unknown entries reflect incomplete verification. They must not be converted into statements of absence or used to give HackTeam an artificial numerical advantage.
6. No formal accessibility or comparative user-task study was conducted. Documented keyboard controls do not establish complete conformance.
7. Participation evidence does not by itself verify task quality, motivation, or future reliability. No such predictor was validated in this task.
8. Some dated announcements or participant-built project pages appeared in discovery searches. They were not used to claim that their described features are currently native platform capabilities.
9. The future HackTeam capabilities are proposals. They have not been scored as implemented competitor features.

### Follow-up questions for unresolved capabilities

The same questions could be checked in a product demonstration or additional documentation for each platform:

- Does team formation explicitly combine skills, role coverage, time availability, and goals? How are the results explained?
- Can participants state usable work time and compare schedule overlap?
- Is there a shared trial task and interaction review before final confirmation of the team?
- Which task-owner, state, deadline, and progress operations are native to the participant workspace?
- What exactly does participation evidence verify, and how are disputed or missing records handled?
- Which accessibility controls and conformance evidence are documented?

No vendor contact, product demonstration, or private-account test is claimed.

## 10. Source register

All sources below were reviewed on **22 October 2026**. Identifiers are used throughout the table and analysis. Descriptions identify the scope supported; an unknown feature is not disproved by a citation.

- **D1.** [Devpost — How hackathons on Devpost work][D1] — Official help. Supports: Public event hosting, registration, submissions, and judging; organizer responsibilities.
- **D2.** [Devpost — Participants page / forming a team][D2] — Official help. Supports: Participant discovery, looking-for-teammates status, team-up messages, and project invitations.
- **D3.** [Devpost — What is a Devpost portfolio and how do I use it?][D3] — Official help. Supports: Public portfolios, projects, and hackathons to which a user submitted.
- **D4.** [Devpost — Step 8: Setting up judging][D4] — Official help. Supports: Online/offline judging setup, judges, criteria, timing, and comments.
- **D5.** [Devpost — Frequently Asked Questions for Hackathon Organizers][D5] — Official product FAQ. Supports: Distinction between public Devpost and Devpost for Teams; features must not be transferred between editions.
- **H1.** [HackerEarth — Forming teams][H1] — Official help. Supports: Participant skill display, manual browsing, invitations, and team membership workflows.
- **H2.** [HackerEarth — Registering for a hackathon][H2] — Official help. Supports: Registration and optional declared skills.
- **H3.** [HackerEarth — Submitting a prototype][H3] — Official help. Supports: Idea/prototype stages, shortlisting, project drafts, project artifacts, and submission.
- **H4.** [HackerEarth — 11 Best Hackathon Platforms for Enterprise in 2026][H4] — Official vendor blog; own-product section only. Supports: Vendor description of its hosting, managed operations, judging, and reporting. Claims about competing products are excluded.
- **F1.** [Devfolio — Setting Up a Hackathon for Universities][F1] — Official guide. Supports: University event creation, organizer setup, and event verification.
- **F2.** [Devfolio — Your Devfolio Profile][F2] — Official guide. Supports: Skills, experience, education, links, and contact visibility.
- **F3.** [Devfolio — Create/Join a Team][F3] — Official guide. Supports: Team creation, invite codes, event-mode differences, and application requirements.
- **F4.** [Devfolio — Projects][F4] — Official guide. Supports: Portfolio projects and automatic linking of hackathon submissions to profiles.
- **F5.** [Devfolio — Organizer Judging][F5] — Official guide. Supports: Online, offline, and sponsor judging; project allocation and score reporting.
- **F6.** [Devfolio — Onchain Credentials][F6] — Official guide. Supports: Independently verifiable credentials and organizer-issued claims; a relevant analogue to participation evidence.
- **F7.** [Devfolio — Keyboard Accessibility][F7] — Official guide. Supports: Documented keyboard navigation, shortcuts, and command-palette actions; not a full accessibility audit.
- **F8.** [Devfolio — Participating in Hackathons][F8] — Official guide. Supports: Participant journey, RSVP, optional event staking, team formation, and submission stages.
- **F9.** [Devfolio — Projects Tab (Organizer Dashboard)][F9] — Official guide. Supports: Managing, searching, filtering, and exporting project submissions.
- **T1.** [TAIKAI — Hackathon Platform][T1] — Official product page. Supports: Project presentation, matchmaking, and a verifiable Proof of Participation badge.
- **T2.** [TAIKAI — Host an online hackathon for your organization][T2] — Official product page and FAQ. Supports: Event management, submissions, evaluation, communication, and an advertised project-management tool.
- **T3.** [TAIKAI — Ultimate hackathon guide for beginners in 2026][T3] — Official blog guide. Supports: Profiles and skill-based teammate search/matchmaking through the Matchmaking tab.

## 11. Search scope and completion boundary

Discovery included official-domain searches for team formation, skills, profiles, organizer judging, projects, availability, compatibility, task management, and participation history. Targeted trial searches used terms including “Trial Sprint,” “trial task,” and “team compatibility” on the selected official help or product domains.

Search results were treated as leads. Current guide and product descriptions were preferred to old announcements. A missing search result was not treated as proof that a feature is absent. User-generated project descriptions hosted on a platform were excluded as evidence of the platform's own capabilities.

| HACK-5 requirement | Coverage |
|---|---|
| Compare 3-5 relevant platforms. | Four product scopes are compared. |
| Use 6-10 consistent criteria. | Ten operational definitions and a common matrix are provided. |
| Include a structured comparison. | Section 4 covers every selected platform and criterion. |
| Support capabilities and limitations with verifiable sources. | Linked official sources and explicit evidence boundaries are provided. |
| Mark unverified features as unknown. | U entries and partial verification are explained; no unsupported absence labels are used. |
| Explain proposed differentiation and need. | Sections 6-8 distinguish existing mechanisms from proposed research contributions. |
| Avoid absolute uniqueness claims. | The positioning is bounded and does not claim global absence or priority. |
| Commit the document and obtain Pull Request review. | Publication and peer review remain separate workflow steps tracked in HACK-5. |

The research document is ready for team review as a source-based draft. HACK-5 should be closed only after its GitHub publication, peer review, and remaining acceptance criteria are satisfied.

[D1]: https://help.devpost.com/article/307-how-hackathons-on-devpost-work
[D2]: https://help.devpost.com/article/75-participants-page-forming-a-team
[D3]: https://help.devpost.com/article/115-what-is-a-devpost-portfolio-and-how-do-i-use-it
[D4]: https://help.devpost.com/article/131-setting-up-judging
[D5]: https://info.devpost.com/faqs-organizers
[H1]: https://help.hackerearth.com/forming-teams
[H2]: https://help.hackerearth.com/registering-for-a-hackathon
[H3]: https://help.hackerearth.com/submitting-a-prototype
[H4]: https://webflow.hackerearth.com/blog/hackathon-platforms
[F1]: https://guide.devfolio.co/docs/guide/setting-up-a-hackathon-for-universities
[F2]: https://guide.devfolio.co/docs/guide/your-dev-profile
[F3]: https://guide.devfolio.co/docs/guide/participating-in-hackathons/create-join-a-team
[F4]: https://guide.devfolio.co/docs/guide/Projects
[F5]: https://guide.devfolio.co/docs/guide/organizer-judging
[F6]: https://guide.devfolio.co/docs/guide/onchain-credentials
[F7]: https://guide.devfolio.co/docs/guide/keyboard-accessibility
[F8]: https://guide.devfolio.co/docs/guide/participating-in-hackathons
[F9]: https://guide.devfolio.co/docs/guide/organizer-dashboard/projects-tab
[T1]: https://taikai.network/en
[T2]: https://taikai.network/organizations
[T3]: https://taikai.network/blog/hackathon-beginners-guide
