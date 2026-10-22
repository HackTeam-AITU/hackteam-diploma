# HackTeam — User Research

**Issue:** [HACK-3 — Conduct User Interviews and Analyze Hackathon Team Formation](https://hackteam-aitu-2027.youtrack.cloud/issue/HACK-3)  
**Prepared:** 22 October 2026  
**Status:** Draft research protocol — data collection pending.

## Purpose and scope

HackTeam is a proposed web platform for student hackathon management and team formation. Its planned concepts include multi-criteria matching, a preliminary collaboration stage called Trial Sprint, and an optional Project Reliability Profile. Their usefulness and practical limitations are research questions.

This document provides research objectives, a planned interview methodology, consent considerations, interview questions, a response template, an analysis framework, and candidate requirements to investigate. Real interview records have not yet been supplied for inclusion. Findings and final requirements will be added after actual discussions.

## 1. Research objectives

- Understand how students find and select teammates for hackathons and related student projects.
- Investigate concrete experiences involving skills, availability, commitment, responsibilities, communication, deadlines, and member withdrawal.
- Explore perceived benefits, limitations, acceptable duration, and conditions for a proposed Trial Sprint.
- Explore whether a Project Reliability Profile would inform team selection, which evidence participants would trust, and what privacy controls they would expect.
- Use documented feedback to propose requirements and an initial MVP scope, separating evidence from assumptions and proposed solutions.

## 2. Participants and method

Plan 3–5 individual, semi-structured discussions, approximately 20–30 minutes each. This is a suggested interview length, not an acceptance criterion.

Recruit students with a concrete, preferably recent experience of joining, forming, or attempting to form a hackathon team. Where available, include different experiences, such as a team leader and a student whose attempt to join a team was unsuccessful. Project-team experience can provide additional context; label it separately from hackathon experience.

The target user groups also include hackathon organizers and team leaders. The issue does not require interviewing every group. An organizer interview may add another perspective, but it must be identified as such rather than treated as a student interview.

HACK-3 also permits a substantive discussion with a real client or organizer as an alternative. This guide is primarily designed for the 3–5 student discussion route. A client discussion would need questions adapted to the client's actual responsibilities and operational experience.

Use the same core questions, with neutral follow-up prompts. Discuss past experience before introducing HackTeam's proposed concepts. Do not present the proposed features as proven improvements. Record skipped, declined, or inapplicable questions explicitly.

Suggested timing: introduction and consent, 2 minutes; past experience, 12–15 minutes; concept feedback, 7–10 minutes; closing, 1–2 minutes. Allow longer if the participant agrees.

## 3. Consent and privacy

Suggested introduction:

> I am researching how students find teammates and work together during hackathons for the HackTeam diploma project. The discussion takes approximately 20–30 minutes. Participation is voluntary; you may skip any question or stop at any time. With your permission, I will take notes and use de-identified summaries in our project documentation, which will be reviewed by the project team. I will omit names, contact details, and identifying details about teammates. May I continue and take notes? May I include de-identified excerpts of your answers?

Record consent before collecting interview answers. If consent is not given, do not conduct or document the interview as research data. Seek separate permission for any audio recording; notes are sufficient for this protocol.

Use participant IDs such as P01 and P02. Do not place names, contact details, consent recordings, or raw audio in GitHub. Keep consent evidence and any necessary identifying information separately from research notes. Explain any intended audience beyond the project team before asking for consent. Do not claim complete anonymity merely because a name has been removed.

Interviews may be conducted in the participant's preferred language. Preserve the meaning when preparing English summaries. Label translations. Use quotation marks only for accurately captured wording; otherwise label the text as a paraphrase.

## 4. Core interview questions

### Past experience — ask before presenting the proposed features

**Q01 — Context**  
Tell me about the most recent time you joined, formed, or tried to join a hackathon team. What was your role, and what happened?  
Optional probes: Was this a hackathon or another student project? Did you ultimately join a team?

**Q02 — Search process**  
Walk me through how you looked for teammates on that occasion. Which channels or tools did you use?  
Optional probes: What did you try first? What happened next? Approximately how long did the search take?

**Q03 — Selection criteria**  
How did you decide whom to work with? What information did you have, and what information was missing?

**Q04 — Search difficulties and workarounds**  
What, if anything, was difficult about finding or choosing teammates? Describe a specific example and how you handled it.  
Optional probe: If the process went smoothly, what made it work well?

**Q05 — Availability and expectations**  
How did your team discuss available time and what each person expected from the hackathon? What happened in practice?  
Optional probe: Were any differences discovered later? Do not assume that differences occurred.

**Q06 — Responsibilities and tools**  
How were responsibilities and tasks divided? How did you keep track of who was doing what?  
Optional probes: Who made these decisions? Were responsibilities changed? Which tools did you use?

**Q07 — Communication**  
How did the team communicate? What worked well, and what, if anything, caused difficulty?  
Optional probe: What effect did a specific incident have on the work?

**Q08 — Deadlines**  
How did the team handle deadlines? Tell me about a deadline that was met or missed and what contributed to that outcome.

**Q09 — Changes in participation**  
Did anyone's participation change during the project? If so, what happened, and how did the team respond?  
Optional probes: Did someone become unavailable or leave? What was the impact? Record “not experienced” if this did not occur.

### Trial Sprint — introduce only after Q01–Q09

Read this neutral description:

> One proposed option is a Trial Sprint: prospective teammates complete a small shared task before deciding whether to confirm the final team. The format and duration have not been fixed.

**Q10 — Perceived usefulness**  
In what situations, if any, would this be useful to you? In what situations would it be unnecessary? Why?

**Q11 — Duration and participation conditions**  
How much active work time, if any, would you be willing to spend on this? Over what calendar period, and at what point before the hackathon would it be practical?  
Optional probes: What would make you decline? Ask for the participant's own estimate before suggesting any duration.

**Q12 — Decision evidence and limitations**  
What would you need to learn from this shared task to decide whether to continue with the team? What might the task fail to reveal or make more difficult?

### Project Reliability Profile

Read this neutral description:

> Another proposed option is a Project Reliability Profile: a record of project participation and task completion supported by available evidence. Its contents and verification rules have not been decided.

**Q13 — Relevance and evidence**  
Would this information influence your choice of teammates? Why or why not? Which information would you consider relevant, and what evidence would you trust?

**Q14 — Privacy and control**  
Which information, if any, would you be comfortable sharing? Who should be able to see it, and what control would you want over it?

**Q15 — Interpretation and fairness**  
What could make this profile misleading or unfair? How should missing information or incorrect records be handled?

### Closing

**Q16 — Priority and missing topics**  
Looking back at your experience, what one change would most improve finding or working with teammates? Is there anything important that I have not asked?

### Neutral follow-up prompts

- Can you describe a specific example?
- What happened next?
- How did you handle that?
- What was the impact?
- What made you reach that conclusion?

Do not suggest a desired answer. Avoid praise that rewards agreement with the proposed features. A negative opinion, a successful existing process, and a lack of interest are useful findings too.

## 5. Interview record — copy once per participant

```text
Participant ID:
Interview date and duration:
Interviewer:
Interview language and format:
User group / role:
Relevant experience (broad, non-identifying summary):
Experience context: Hackathon / Other student project

Consent to participate and take notes: Granted / Declined
Consent to use de-identified excerpts: Granted / Declined
Audio recording: Not used / Separately consented
Consent record reference (kept separately, without personal details here):

For each answer, distinguish paraphrased notes from exact wording.
Use Not asked / Declined / Not applicable / Unclear when appropriate.

Q01 — Most recent team formation experience:
Q02 — Search process, channels, and tools:
Q03 — Selection criteria and missing information:
Q04 — Difficulties, successful practices, and workarounds:
Q05 — Availability and expectations:
Q06 — Task allocation and tracking:
Q07 — Communication:
Q08 — Deadlines:
Q09 — Changes in participation:
Q10 — Trial Sprint usefulness and lack of usefulness:
Q11 — Trial Sprint active work time, calendar period, timing, and conditions:
Q12 — Trial Sprint decision evidence, risks, and limitations:
Q13 — Profile relevance and trusted evidence:
Q14 — Profile privacy and participant control:
Q15 — Profile fairness and correction of records:
Q16 — Highest priority and missing topics:

Exact excerpts, if permitted and accurately captured:
- Question ID:
  Original wording:
  English translation, if needed (label as translated):

Post-interview analyst notes — separate from participant answers:
- Reported past experiences and supporting question IDs:
- Opinions about proposed features and supporting question IDs:
- Interviewer assumptions / interpretations:
- Candidate requirements or solutions (not validated merely by being proposed):
- Contradictions, uncertainty, and unanswered questions:
- Context affecting interpretation:
```

## 6. Findings classification and later analysis

Suggested topic labels: search channels; skills and roles; availability; expectations and commitment; responsibilities; communication; deadlines; withdrawal; successful practices; Trial Sprint; profile evidence; privacy; fairness; MVP priorities. These are coding categories, not confirmed findings.

Classify each item as:

- **Reported experience:** an account of a particular past event; it has not necessarily been independently verified.
- **Participant opinion:** a preference or judgement, including reactions to proposed features.
- **Researcher assumption:** an interpretation that still needs supporting evidence.
- **Proposed solution:** a candidate requirement or feature, with its evidence and remaining uncertainty.

After interviews, use a traceable findings table:

| Finding ID | Finding and evidence type | Participant and question IDs | Supporting and conflicting accounts | Candidate requirement / MVP implication | Remaining uncertainty |
|---|---|---|---|---|---|

For this small study, “supported finding” means supported within the recorded interviews. Do not generalize it to all students. Report counts with a clear denominator and distinguish not asked, no issue experienced, and disagreement. Record conflicting feedback rather than forcing a consensus.

For Trial Sprint, preserve individual duration estimates and distinguish active work time from elapsed calendar time. Positive reactions indicate perceived usefulness; they do not demonstrate that a Trial Sprint improves team performance. Assessing effectiveness would require a separate evaluation.

## 7. Limitations to report

Document the actual sample size and roles, recruitment method, interview context, missing perspectives, reliance on memory and self-report, and possible interviewer or translation effects. A small convenience sample does not establish prevalence across the student population. Feedback about concepts is not evidence of actual adoption or improved team outcomes.

## 8. Results and evidence status

### 8.1 Current evidence

No real interview records have been supplied for this version. There are no participant accounts, interview dates, consent confirmations, or verified quotations to report here. This describes the material available for this document, rather than making a claim about research conducted elsewhere by the project team.

Consequently, no empirical findings, participant counts, agreement rates, or validated user preferences are reported. In particular, there is no empirically established Trial Sprint duration and no evidence in this document demonstrating that Trial Sprint improves team performance.

### 8.2 Findings summary

Data collection and analysis are pending. After real discussions, replace this status summary with de-identified accounts of user problems, expectations, successful existing practices, workarounds, and conflicting opinions. Link each finding to participant IDs and question IDs using the analysis table in Section 6.

For each proposed finding, state whether it is a reported past experience, a participant opinion, or a researcher interpretation. Do not generalize a small convenience sample to all students.

### 8.3 Trial Sprint and Project Reliability Profile

Real feedback on both proposed concepts is pending. Analyze their perceived benefits, lack of usefulness, limitations, participation conditions, and alternatives. For Trial Sprint, distinguish active work time from elapsed calendar time. For project history, record evidence preferences, visibility expectations, fairness concerns, and correction needs.

Positive opinions would establish perceived usefulness within the sample, rather than prove adoption or improved outcomes. A separate evaluation would be needed to assess the effectiveness of the proposed team formation method.

## 9. Assumptions, candidate requirements, and MVP implications

The following are questions and design candidates derived from the project scope. They are not conclusions from completed interviews. Actual feedback may support, contradict, refine, or defer them.

| ID | Assumption to investigate | Candidate functional requirement | Questions | MVP decision status |
|---|---|---|---|---|
| C01 | Skills, role expectations, and availability may influence team selection. | Allow participants to describe relevant skills, desired roles, and availability for a particular event. | Q03-Q05 | Investigate useful fields and acceptable visibility before making them mandatory. |
| C02 | Explicit responsibilities and deadline tracking may help teams coordinate. | Provide a workspace with identifiable task owners, task statuses, and deadlines. | Q06-Q09 | Already within the proposed project scope; details and priority remain to be assessed with users. |
| C03 | Preliminary collaboration may help some unfamiliar teams, while creating extra effort for others. | Support a small shared task followed by an explicit decision about team confirmation. | Q10-Q12 | Effort, timing, participation rules, and evaluation criteria remain undecided. |
| C04 | Unclear team entry requirements may make it difficult for prospective members to assess suitability. | Explain required roles, expected contributions, and relevant participation conditions. | Q02-Q05, Q16 | Validate the information needs of prospective members and team leaders. |
| C05 | Prior participation records may inform decisions but introduce trust, privacy, and fairness concerns. | If project history is implemented, explain the evidence behind records and support visibility and correction controls. | Q13-Q15 | Treat as a candidate extension. Missing history must not automatically be treated as poor reliability. |

After collecting real feedback, connect each recommendation to source answers and explain the reported consequence, current workaround, conflicting accounts, and reason for including or excluding the function from the MVP. Avoid choosing priorities solely because they match the original product idea.

## 10. HACK-3 acceptance criteria status

This table describes the document rather than the live status of YouTrack or GitHub.

| Acceptance criterion | Status in this draft |
|---|---|
| At least 3-5 real user discussions or a substantive real client discussion are documented. | Pending real discussion records. |
| Research methodology and interview questions are included. | Included as a planned protocol with 16 core questions. |
| Key user problems and expectations are identified. | Pending empirical analysis. Topics and assumptions are provided. |
| Feedback on Trial Sprint is collected and analyzed. | Pending real feedback. |
| Validated findings are separated from assumptions. | Assumptions are explicit; no validated findings are claimed. |
| A structured summary of research findings is included. | Pending real data; an analysis framework is provided. |
| Conclusions are connected to functional requirements. | Pending empirical conclusions; candidate requirements are labeled as provisional. |
| No interview results or user statements are fabricated. | No participant results or quotations are claimed in this draft. |
| The document is committed to GitHub and reviewed through a Pull Request. | Pending publication and review; no commit, PR, or review is claimed here. |

This preparation document alone does not satisfy the completed-research acceptance criteria of HACK-3. A draft Pull Request can be used to discuss the protocol while data collection remains pending.

## 11. Next actions

1. Recruit real participants, or prepare for the permitted substantive discussion with a real client or organizer.
2. Obtain consent and collect actual responses using the template in Section 5.
3. Prepare de-identified summaries, preserving references to the questions and the distinction between quotations and paraphrases.
4. Analyze supporting and conflicting accounts, identify findings supported by the interviews, and retain unresolved questions explicitly.
5. Revise functional requirements and MVP priorities using the actual findings.
6. Update this document with the actual method, sample, results, and limitations. Remove outdated pending-status statements only when the corresponding work is documented.
7. Submit the document for peer review through a Pull Request and complete the acceptance criteria before closing HACK-3.

## Project context

- [HACK-3 task](https://hackteam-aitu-2027.youtrack.cloud/issue/HACK-3): task description and acceptance criteria supplied in the project conversation.
- [HackTeam project README](https://github.com/HackTeam-AITU/hackteam-diploma/blob/main/README.md): proposed project scope and features.
