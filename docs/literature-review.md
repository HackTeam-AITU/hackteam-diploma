# Literature Review: Multi-Criteria Student Team Formation and Preliminary Collaboration Assessment

**Project:** HackTeam — Hackathon Management and Student Team Formation Web System  
**Document Type:** Literature Review  
**Related Issue:** HACK-4 — Prepare Literature Review  
**Academic Institution:** Astana IT University  
**Program:** Software Engineering  
**Academic Supervisor:** Myrzakerimova Alua  
**Prepared by:** Rakhmetulla Madina  
**Date:** October 22, 2026  
**Document Status:** Initial Academic Draft — Subject to Peer and Supervisor Review

---

## Abstract

The formation of effective student teams is an important challenge in collaborative learning, software engineering education, and hackathon participation. Conventional team formation strategies may rely on self-selection, random assignment, or individual characteristics such as technical skills. However, successful collaboration also involves coordination, availability, communication, mutual understanding, and the ability to manage disagreements.

This literature review analyzes twelve scientific publications addressing computational team formation, multi-criteria optimization, student collaboration, team dynamics, and hackathon participation. The reviewed studies include algorithmic models, computational experiments, classroom investigations, systematic and scoping reviews, and qualitative and quantitative analyses of hackathon teams.

The review identifies three complementary research directions: transparent multi-criteria team formation, participant involvement in team selection, and preliminary assessment of collaborative interaction.

Based on this synthesis, the HackTeam diploma project proposes a web-based approach combining multi-criteria teammate recommendations with a structured preliminary collaboration mechanism called Trial Sprint.

The review does not establish that the proposed combination is unprecedented or empirically superior. Instead, it provides a theoretical foundation for defining the system, developing research hypotheses, and designing future comparisons with alternative team formation approaches.

**Keywords:** team formation, multi-criteria decision-making, student teams, hackathons, collaboration, team compatibility, Trial Sprint, multi-objective optimization, software engineering.

---

## 1. Introduction

Team-based collaboration is a central component of software engineering education, project-based learning, and hackathon participation. Students are frequently expected to combine different technical competencies, coordinate responsibilities, communicate under time constraints, and produce shared project outcomes.

However, forming a team does not necessarily ensure effective collaboration.

Students may have complementary technical skills but incompatible schedules, unclear working expectations, or insufficient knowledge of one another's competencies. Furthermore, existing team formation approaches may prioritize observable participant characteristics without directly examining preliminary collaboration.

The scientific literature describes several approaches to this problem. Computational methods use optimization algorithms to construct teams according to predefined criteria. Other research investigates the influence of team formation procedures on cohesion, conflict, task performance, and participant satisfaction.

Hackathon-specific studies additionally demonstrate the importance of time-sensitive coordination, task allocation, shared understanding, and flexible communication practices.

The HackTeam project proposes to integrate these perspectives into a web-based system.

Its two principal research components are:

1. **Multi-Criteria Matching:** A transparent method for recommending prospective teammates based on multiple relevant characteristics, including technical skills, preferred roles, availability, and working preferences.

2. **Trial Sprint:** A short preliminary collaboration stage in which prospective teammates coordinate and complete a limited set of tasks before deciding whether to confirm their team.

The central research question is:

**Can combining multi-criteria teammate recommendations with preliminary collaborative activities provide useful additional information for student hackathon team formation?**

The effectiveness of this approach remains to be investigated.

### 1.1 Purpose of the Review

This review aims to:

- Examine existing scientific approaches to student team formation.
- Identify commonly used criteria and computational algorithms.
- Analyze approaches to evaluating team composition and collaboration.
- Investigate collaboration challenges observed in hackathon environments.
- Identify limitations and open questions relevant to HackTeam.
- Establish a theoretical foundation for the proposed matching method and Trial Sprint mechanism.
- Support the design of appropriate evaluation methods and baselines.

### 1.2 Scope

The review focuses on scientific literature related to:

- Algorithm-supported student team formation.
- Multi-criteria and multi-objective optimization.
- Skill-based matching and role complementarity.
- Participant availability and working preferences.
- Team conflict, cohesion, and psychological safety.
- Preliminary collaboration and team development practices.
- Communication and coordination during hackathons.
- Empirical evaluation of team formation methods.

The review addresses both technical and social aspects of the problem.

---

## 2. Literature Selection and Review Methodology

### 2.1 Review Approach

A targeted narrative literature review was prepared using twelve relevant scientific publications.

The review is organized around the HackTeam project's principal research objectives rather than a single academic discipline.

Relevant publications were identified through scholarly references, academic publisher pages, and scientific publication records. Bibliographic details and DOI identifiers were checked against available publisher or academic records.

This review should not be interpreted as an exhaustive systematic literature review. A comprehensive database-wide search, formal risk-of-bias assessment, and reproducible screening protocol have not been completed.

### 2.2 Selection Criteria

Publications were selected according to the following considerations:

1. Relevance to team formation, team dynamics, or hackathon collaboration.
2. Scientific publication in a peer-reviewed journal or research proceedings.
3. Availability of verifiable bibliographic information.
4. A sufficiently described research problem and methodological approach.
5. Potential applicability to HackTeam's system design or evaluation.

Recent research was prioritized, while older foundational publications were retained where they provided important conceptual frameworks.

### 2.3 Publication Distribution

The selected literature includes:

| Publication Year | Number of Publications |
|---|---:|
| 2020 | 1 |
| 2022 | 3 |
| 2023 | 3 |
| 2024 | 5 |
| **Total** | **12** |

Eleven publications were published between 2022 and 2024. The remaining publication, Gómez-Zará et al. (2020), was retained because of its foundational taxonomy of technology-supported team formation systems.

The selected collection does not claim complete coverage of research published in 2025 or 2026.

### 2.4 Analytical Framework

Each publication was examined using six criteria:

- **Research Problem:** The principal question or challenge addressed.
- **Methodology:** The study design and data collection approach.
- **Algorithms or Approaches:** The computational, theoretical, or analytical methods used.
- **Main Findings:** The outcomes supported by the available publication.
- **Limitations:** Constraints affecting interpretation or generalizability.
- **Relevance to HackTeam:** The specific contribution to the proposed system and research methodology.

Full-text findings were used where accessible. Where complete publications were restricted, conclusions were limited to information supported by available abstracts and publication records.

---

## 3. Review of Scientific Publications

### 3.1 Wang et al. (2024): Algorithm-Supported Educational Team Formation

**Publication:** Enhancing Teamwork and Collaboration: A Systematic Review of Algorithm-Supported Pedagogical Methods.

**Research Problem:** Wang et al. (2024) investigated the application of computational approaches to educational team formation and collaborative learning. The study examined how algorithms can support the creation of student groups according to participant characteristics.

**Methodology:** The authors conducted a systematic literature review of twenty scientific publications. The review analyzed student grouping criteria, computational approaches, implementation considerations, and reported educational outcomes.

**Algorithms and Approaches:** The reviewed studies included genetic algorithms, clustering techniques, and other computational methods. The authors distinguished traditional instructor-led and student-led grouping from algorithm-supported approaches.

**Main Findings:** The review identified the potential of computational methods to support structured team formation. It also highlighted the importance of considering both static participant characteristics and dynamic information related to team interaction. The reviewed literature indicated that dynamic characteristics received comparatively limited attention.

**Limitations:** The study was restricted to a selected collection of educational publications and learning environments. Its conclusions cannot automatically be generalized to software development hackathons. The authors also discussed practical challenges associated with implementation, usability, and student data privacy.

**Relevance to HackTeam:** This publication establishes a foundation for investigating multi-criteria student team formation. It motivates the proposed use of several participant attributes during matching and the exploration of additional interaction-related information through Trial Sprint.

However, the publication does not directly validate the proposed HackTeam workflow.

### 3.2 Bowers et al. (2023): Soft Skills and Schedule Compatibility

**Publication:** Forming Student Teams to Incorporate Soft Skills and Commonality of Schedule.

**Research Problem:** Bowers et al. investigated how student team formation can incorporate common availability and interpersonal competencies alongside other grouping requirements.

**Methodology:** The authors developed an analytical team formation approach for educational environments using mixed-integer programming and text-based analysis of student characteristics.

**Algorithms and Approaches:** A discrete optimization model ensured that team members shared a minimum number of available time slots. A separate text analysis approach supported the representation of leadership and interpersonal skills.

**Main Findings:** The authors presented a model capable of incorporating schedule compatibility and soft-skill considerations into structured team assignments. They reported practical educational benefits from using the proposed analytical approach.

**Limitations:** The approach depends on the availability and accuracy of participant information. Text-derived indicators may not fully represent interpersonal competence. In addition, the model was developed for educational teams rather than time-constrained hackathon participation. Detailed quantitative findings require access to the full article.

**Relevance to HackTeam:** The study directly motivates the inclusion of availability overlap as a matching criterion. It also demonstrates that practical team formation can be modeled through a combination of optimization objectives and constraints.

HackTeam can adapt this principle without attempting to infer complex psychological characteristics from participant profiles.

### 3.3 Maguire and Keceli (2024): Team Formation, Diversity, and Conflict

**Publication:** The Impact of Formation and Diversity on Student Team Conflict.

**Research Problem:** Maguire and Keceli investigated whether different team formation procedures affect conflict, cohesion, social loafing, and overall team functioning.

**Methodology:** Over two years, the authors compared parallel sections of a university management course. One section used instructor-assigned teams designed to increase diversity, while students in the other section selected their own teammates.

**Algorithms and Approaches:** The study compared team assignment strategies rather than introducing a computational optimization algorithm.

**Main Findings:** Instructor-assigned diverse teams did not demonstrate increased conflict. Student-selected teams did not show higher cohesion. Team formation procedures were also associated with differences in social loafing and team functioning.

**Limitations:** The research was conducted within a particular educational setting. The available abstract does not provide complete statistical details for every outcome. The study does not evaluate short-term hackathon teams or Trial Sprint activities.

**Relevance to HackTeam:** The findings indicate that team formation should not be evaluated solely through participant characteristics. Team functioning, cohesion, and perceived contribution are relevant additional dimensions.

For HackTeam, this motivates collecting limited, structured participant feedback during preliminary collaboration while avoiding unsupported claims about individual reliability.

### 3.4 Huerta et al. (2024): Psychological Safety and Team Conflict

**Publication:** An Exploration of Psychological Safety and Conflict in First-Year Engineering Student Teams.

**Research Problem:** Huerta et al. examined psychological safety and its relationship with conflict during collaborative engineering education.

**Methodology:** The authors conducted a qualitative investigation involving 82 first-year engineering students. Written reflections and focus groups were analyzed using a thematic approach informed by team conflict dynamics.

**Algorithms and Approaches:** The study used qualitative analysis rather than computational team optimization.

**Main Findings:** The research demonstrated the importance of interpersonal interaction and communication conditions in engineering student teams. Students' willingness to share ideas and address disagreements could change throughout collaboration. Task-related, process-related, and interpersonal conflicts were important aspects of team experience.

**Limitations:** The findings were generated in a semester-long educational environment. The study did not experimentally evaluate team formation algorithms or establish a reliable method for predicting long-term collaboration from short activities.

**Relevance to HackTeam:** The research motivates the inclusion of voluntary communication and coordination feedback in Trial Sprint.

Psychological safety should not be reduced to an automatic score derived from brief system activity. Participants should retain control over sensitive feedback.

### 3.5 Hagvall Svensson et al. (2024): Negotiating Team Norms

**Publication:** How Do Students Negotiate Groupwork? The Influence of Group Norm Exercises and Group Development Norms.

**Research Problem:** Hagvall Svensson et al. investigated how students negotiate working expectations and whether explicit group norm exercises promote constructive collaboration.

**Methodology:** The authors conducted a qualitative study involving seven student groups participating in exercises focused on developing team charters. Recorded discussions, observations, and interviews supported the analysis.

**Algorithms and Approaches:** The research applied framing theory to investigate how students establish, negotiate, and sometimes challenge group norms.

**Main Findings:** Structured group norm exercises could help students clarify expectations and reconsider existing practices. However, the exercises sometimes reinforced dominant perspectives and discouraged disagreement. Explicit rules did not automatically ensure inclusive participation.

**Limitations:** The study involved a small number of groups in a specific educational context. Not all collaborative activities outside the exercises were systematically recorded. Its findings should not be interpreted as evidence that a short team agreement guarantees successful collaboration.

**Relevance to HackTeam:** This research supports incorporating an optional Team Agreement into Trial Sprint.

Participants could discuss communication expectations, responsibilities, deadlines, and approaches to resolving disagreements. Subsequent reflection could help determine whether the agreement was useful in practice.

### 3.6 Sanchez-Anguix et al. (2023): Comparing Computational Team Formation Methods

**Publication:** Comparing Computational Algorithms for Team Formation in the Classroom: A Classroom Experience.

**Research Problem:** Sanchez-Anguix et al. examined the comparative effectiveness of alternative team evaluation heuristics in educational team formation.

**Methodology:** The authors implemented computational team formation using Integer Linear Programming and evaluated approaches based on Belbin team roles and the Myers-Briggs Type Indicator. The study involved students in university educational activities.

**Algorithms and Approaches:** Integer Linear Programming generated team assignments according to a selected evaluation function. The research compared different criteria for evaluating potential team compositions.

**Main Findings:** Both approaches produced generally favorable student evaluations, although some satisfaction and collaboration indicators differed between the compared heuristics. The authors emphasized that the distribution of participant characteristics can influence the effectiveness of an evaluation method.

**Limitations:** The investigation involved long-term educational projects rather than short hackathons. The evaluated heuristics were approximations of team suitability, not reliable predictors of actual future performance.

**Relevance to HackTeam:** This study supports separating the matching algorithm from the criteria used to evaluate candidates.

HackTeam can initially implement a transparent weighted scoring function and investigate different criterion weights. Personality-based grouping is not required for the proposed MVP.

### 3.7 Gómez-Zará et al. (2020): Taxonomy of Team-Assembly Systems

**Publication:** A Taxonomy of Team-Assembly Systems: Understanding How People Use Technologies to Form Teams.

**Research Problem:** Gómez-Zará et al. investigated how digital systems distribute control over team formation between computational methods and human users.

**Methodology:** The authors developed a conceptual taxonomy and conducted a scoping review of 126 scientific publications concerning technology-supported team assembly.

**Algorithms and Approaches:** Four categories were identified: self-assembled teams, staffed teams, optimized teams, and augmented teams. The categories distinguish different levels of user agency and participation.

**Main Findings:** Team formation systems differ not only in their optimization objectives but also in how users interact with recommendations and make final decisions.

The framework demonstrates the importance of considering user control when designing team formation technologies.

**Limitations:** The taxonomy focuses on two principal dimensions and does not comprehensively represent every factor influencing collaboration, including time constraints, geographical location, and particular interface capabilities.

**Relevance to HackTeam:** HackTeam is conceptually closest to an augmented team formation approach because the system recommends candidates while participants make final membership decisions.

The project should provide understandable recommendation explanations and allow users to accept or decline proposed collaborations.

This publication also motivates the evaluation of perceived recommendation transparency and participant autonomy.

### 3.8 Gómez-Zará et al. (2022): Multi-Objective Team Optimization

**Publication:** In Search of Diverse and Connected Teams: A Computational Approach to Assemble Diverse Teams Based on Members' Social Networks.

**Research Problem:** Gómez-Zará et al. investigated how teams can be formed while balancing participant diversity with familiarity based on previous social connections.

**Methodology:** The authors formulated the problem as multi-objective optimization and applied NSGA-II. They evaluated the method using empirical datasets related to student groups, scientific collaboration, and GitHub development teams.

**Algorithms and Approaches:** NSGA-II generated non-dominated candidate solutions. Its effectiveness was evaluated against alternative optimization algorithms, including SPEA-2, Pareto Local Search, and Hybrid Particle Swarm Optimization.

**Main Findings:** The proposed method generated multiple team assignments with different trade-offs between diversity and familiarity. Computational experiments demonstrated favorable performance according to optimization quality indicators.

**Limitations:** The method requires participant attributes and social network information, which may not be available in real applications. Its computational evaluation does not establish that generated teams will perform better in actual collaborative projects.

**Relevance to HackTeam:** This research demonstrates the importance of considering trade-offs among competing team formation objectives.

For an initial MVP, HackTeam proposes a simpler weighted scoring model because of its transparency and implementation feasibility. More advanced multi-objective optimization may be investigated in subsequent evaluations.

### 3.9 Schulten et al. (2022): Communication During Online Hackathons

**Publication:** How Do Participants Collaborate During an Online Hackathon? An Empirical, Quantitative Study of Communication Traces.

**Research Problem:** Schulten et al. examined communication behavior during a time-limited online hackathon, addressing the difficulty of observing digital collaboration at scale.

**Methodology:** The researchers conducted an archival analysis of Slack communication during a 48-hour event. The cleaned dataset included 14,324 messages from 1,212 Slack users, including participants and event officials, across 253 channels.

**Algorithms and Approaches:** The study combined descriptive statistics, temporal communication analysis, Gini coefficient measurements, and qualitative inspection of communication tool mentions.

**Main Findings:** Communication activity was associated with event checkpoints and submission deadlines. Messaging participation was unevenly distributed, and the official platform was frequently used for organizational coordination. Participants also mentioned additional communication tools.

**Limitations:** The study examined one online hackathon and only the communication accessible through its official Slack environment. Message volume could not reliably measure individual contribution or overall team performance.

**Relevance to HackTeam:** The findings motivate progress checkpoints and task-related coordination during Trial Sprint.

However, HackTeam should not equate message frequency with productivity, motivation, or reliability. Observable task outcomes and voluntary feedback provide more appropriate starting points for evaluation.

### 3.10 O'Toole et al. (2023): Transactive Memory Systems in Hackathon Teams

**Publication:** Transactive Memory Systems, Temporary Teams, and Conflict: Innovativeness During a Hackathon.

**Research Problem:** O'Toole et al. investigated how transactive memory systems relate to the innovativeness of temporary teams and how task and relationship conflict influence that relationship.

**Methodology:** The authors tested a theoretical model using a sample of 202 teams participating in Global Game Jam, a 48-hour game development hackathon.

**Algorithms and Approaches:** The study applied the concept of transactive memory systems, describing the way team members understand and coordinate one another's specialized knowledge.

**Main Findings:** The research investigated whether task conflict strengthens, and relationship conflict weakens, the relationship between transactive memory systems and team innovativeness. The accessible journal abstract describes these proposed moderating relationships and the empirical study design. Detailed statistical effect estimates require access to the full publication.

**Limitations:** The findings relate to a specific game development hackathon setting. The study did not evaluate automated team selection or preliminary collaboration before final team formation.

**Relevance to HackTeam:** This research motivates helping prospective teammates understand each other's expertise before committing to a team.

Trial Sprint could include a short introduction of skills, role coordination, collaborative tasks, and structured reflection.

The study does not establish that such a mechanism automatically develops transactive memory systems or improves team performance.

### 3.11 Mendes et al. (2022): Socio-Technical Collaboration in Online Hackathons

**Publication:** Socio-Technical Constraints and Affordances of Virtual Collaboration: A Study of Four Online Hackathons.

**Research Problem:** Mendes et al. investigated how online hackathon teams coordinate activities and how technologies and event structures influence collaboration.

**Methodology:** The authors conducted a qualitative multiple-case study involving ten teams from four online hackathons. They collected twenty-seven interviews with participants and analyzed collaboration practices.

**Algorithms and Approaches:** The study examined socio-technical coordination rather than automated team formation. Its analytical focus included communication, task distribution, shared awareness, and technology-supported collaboration.

**Main Findings:** Teams frequently distributed tasks according to technical skills or individual interests. Participants combined synchronous and asynchronous communication methods to maintain awareness of progress. Continuous audio communication sometimes reproduced aspects of working in a shared physical environment. However, fragmented tools and reduced informal interactions created additional difficulties.

**Limitations:** The study relied on interviews with a relatively small number of teams. Participants' retrospective accounts may contain recall bias, and the findings are not necessarily representative of all hackathon formats.

**Relevance to HackTeam:** The results support lightweight team workspaces, clear responsibility assignment, task status tracking, and flexible communication arrangements.

They also suggest that preparation before a hackathon may help participants coordinate more efficiently, although the effectiveness of structured Trial Sprint activities remains untested by this study.

### 3.12 Bergtold and Shanoyan (2024): Comparing Group Formation Strategies

**Publication:** Assessment of Group Formation Methods on Performance in Group-Based Learning Activities.

**Research Problem:** Bergtold and Shanoyan investigated how different student group formation methods influence group project performance.

**Methodology:** The authors conducted a classroom experimental study using two upper-level agricultural economics courses. Group formation strategies were evaluated through academic project outcomes and statistical comparisons.

**Algorithms and Approaches:** The study compared random assignment, GPA-based grouping, mathematics ability-based grouping, and student self-selection. Integer programming supported the construction of some group assignments.

**Main Findings:** The results varied across assignments and learning contexts. Group formation based on academic characteristics provided advantages in selected comparisons. Student self-selection was sometimes more beneficial after participants had opportunities to become familiar with one another's abilities and working practices.

**Limitations:** The study was conducted in one university and evaluated academic project grades rather than short-term hackathon performance. It did not directly measure all aspects of internal team interaction.

**Relevance to HackTeam:** This research supports comparing different team formation methods rather than assuming that one approach is universally superior.

It also motivates investigating whether preliminary collaborative experiences can help students make more informed teammate selections.

---

## 4. Comparative Analysis of Existing Research

### 4.1 Literature Comparison Matrix

The following matrix summarizes the twelve reviewed publications.

| ID | Publication | Main Method | Key Contribution | Main Limitation | Relevance to HackTeam |
|---|---|---|---|---|---|
| S1 | Wang et al. (2024) | Systematic review | Synthesizes algorithm-supported student grouping | Educational scope and heterogeneous evidence | Multi-criteria matching foundation |
| S2 | Bowers et al. (2023) | Mixed-integer programming | Incorporates shared availability and soft skills | Depends on profile and schedule data | Availability overlap |
| S3 | Maguire & Keceli (2024) | Comparative classroom study | Investigates formation, conflict, cohesion, and social loafing | Limited educational context | Team interaction evaluation |
| S4 | Huerta et al. (2024) | Qualitative analysis | Explores psychological safety and team conflict | Semester-long student context | Voluntary collaboration feedback |
| S5 | Hagvall Svensson et al. (2024) | Qualitative framing analysis | Explains negotiation of team norms | Small number of groups | Team Agreement and reflection |
| S6 | Sanchez-Anguix et al. (2023) | Integer linear programming | Compares team evaluation heuristics | Context-dependent evaluations | Transparent algorithm criteria |
| S7 | Gómez-Zará et al. (2020) | Conceptual taxonomy | Classifies user and algorithm roles in team formation | Limited taxonomy dimensions | Human-controlled recommendations |
| S8 | Gómez-Zará et al. (2022) | NSGA-II | Optimizes competing team objectives | Optimization metrics do not establish team success | Alternative matching methods |
| S9 | Schulten et al. (2022) | Communication trace analysis | Identifies hackathon communication patterns | Incomplete visibility of team interaction | Trial Sprint checkpoints |
| S10 | O'Toole et al. (2023) | Empirical model testing | Investigates expertise coordination and team conflict | Specific temporary-team context | Skill awareness and coordination |
| S11 | Mendes et al. (2022) | Multiple-case study | Describes virtual hackathon collaboration | Small qualitative sample | Team workspace and task management |
| S12 | Bergtold & Shanoyan (2024) | Classroom experiment | Compares four team formation strategies | Academic grades as primary outcomes | Baseline selection and evaluation |

### 4.2 Comparison of Team Formation Approaches

The reviewed literature distinguishes several team formation strategies.

**Random Assignment**

Random assignment provides a simple baseline that does not explicitly optimize participant compatibility. It is useful for experimental comparison but does not incorporate individual team preferences or required role coverage.

**Self-Selection**

Self-selection provides participants with substantial autonomy. However, decisions may depend on existing social relationships and incomplete information about potential teammates.

**Single-Criterion Matching**

A single-criterion method can rank candidates according to technical skills, academic performance, or another predefined attribute.

Its principal limitation is the exclusion of other potentially relevant team formation criteria.

**Multi-Criteria Weighted Scoring**

A weighted scoring method combines several normalized criteria into one evaluation function.

Its advantages include transparency, straightforward implementation, and the ability to examine sensitivity to criterion weights.

However, the method depends on carefully selected criteria, meaningful normalization, and justified weights.

**Mathematical Optimization**

Integer programming can assign participants to teams under explicit constraints.

It is appropriate when organizers must allocate an entire participant pool while satisfying team size, role, or availability requirements.

**Multi-Objective Optimization**

Methods such as NSGA-II can generate alternative solutions with different trade-offs among competing objectives.

They may provide more flexible optimization but introduce additional computational and interpretability requirements.

### 4.3 Comparison of Collaboration Assessment Approaches

The reviewed research also demonstrates that team collaboration can be assessed through different types of evidence.

| Assessment Approach | Potential Benefit | Limitation |
|---|---|---|
| Participant profiles | Available before collaboration | Often self-reported |
| Task completion records | Observable task-related evidence | Influenced by task difficulty |
| Deadline adherence | Indicates completion relative to agreements | Influenced by availability and circumstances |
| Communication activity | Reveals selected interaction patterns | Does not establish contribution quality |
| Participant feedback | Captures subjective experience | May contain response bias |
| Team outcomes | Measures final project achievement | Influenced by numerous external factors |
| Preliminary collaboration | Provides early shared experience | Limited duration and predictive validity |

A central conclusion is that no single indicator should be treated as a definitive measure of team compatibility.

---

## 5. Critical Synthesis of the Literature

### 5.1 Computational Suitability Is Not Equivalent to Team Success

Optimization studies demonstrate that computational methods can construct teams according to predefined objectives.

However, producing a mathematically favorable team composition does not guarantee effective collaboration.

Gómez-Zará et al. (2022) evaluated optimization quality, while Sanchez-Anguix et al. (2023) examined participant experiences under different team evaluation heuristics.

These approaches offer valuable but different types of evidence.

HackTeam must therefore distinguish algorithmic score quality from actual collaboration outcomes.

### 5.2 Participant Agency Is an Important Design Consideration

The taxonomy proposed by Gómez-Zará et al. (2020) demonstrates that team formation technologies distribute decision-making authority differently.

For HackTeam, recommendations should support users rather than impose team membership.

Participants should understand the general criteria behind recommendations and retain control over accepting or declining collaboration opportunities.

### 5.3 Team Interaction Cannot Be Reduced to Profile Characteristics

Maguire and Keceli (2024), Huerta et al. (2024), and Hagvall Svensson et al. (2024) emphasize that collaboration involves conflict management, psychological safety, negotiated expectations, and social interaction.

These characteristics may not be fully represented by technical skills or previous experience.

Their findings motivate studying collaboration after an initial recommendation has been generated.

### 5.4 Hackathon Collaboration Has Distinctive Constraints

Schulten et al. (2022), O'Toole et al. (2023), and Mendes et al. (2022) investigated temporary teams in hackathon environments.

These studies describe the relevance of limited time, distributed expertise, coordination, progress checkpoints, and communication practices.

However, their results do not establish that short preliminary collaboration can reliably predict future hackathon outcomes.

### 5.5 Evaluation Methods Must Match the Research Questions

The reviewed studies use different outcome measures, including student satisfaction, academic grades, computational optimization scores, communication activity, and product innovativeness.

Such outcomes are not directly interchangeable.

HackTeam should select evaluation measures that correspond to its specific objectives and should not interpret improvements in one indicator as proof of overall team success.

---

## 6. Research Gaps Relevant to HackTeam

The following gaps are identified relative to the selected literature.

They represent opportunities for investigation rather than claims that no prior research has addressed these questions.

### RG1 — Limited Integration of Static Matching and Preliminary Interaction Assessment

Several studies investigate algorithmic team formation using predefined participant characteristics.

Other studies investigate communication and collaboration after teams have already been formed.

Within the selected literature, there is limited direct evaluation of a workflow that combines initial multi-criteria recommendations with structured preliminary collaboration before final team confirmation.

**HackTeam Response:** Investigate whether Trial Sprint observations provide additional information beyond the original matching score.

### RG2 — Limited Evidence for Short Pre-Hackathon Collaboration as a Team Selection Mechanism

Hackathon research describes collaboration under strict time constraints.

However, the selected studies do not directly validate a short pre-hackathon collaborative task as a reliable method for determining team suitability.

**HackTeam Response:** Design a limited Trial Sprint and evaluate its usability, feasibility, and perceived usefulness.

### RG3 — Need for Transparent and Participant-Controlled Recommendations

Algorithmic team formation can reduce manual effort, but recommendation mechanisms may be difficult for users to understand.

The taxonomy developed by Gómez-Zará et al. (2020) highlights the significance of user participation and control.

**HackTeam Response:** Present understandable recommendation factors and preserve voluntary team confirmation.

### RG4 — Challenges in Measuring Preliminary Collaboration

Communication volume, task completion, deadline adherence, and participant satisfaction each capture different aspects of collaboration.

None should automatically be interpreted as an objective measure of personal reliability or long-term team success.

**HackTeam Response:** Use clearly defined task observations and optional feedback while documenting their limitations.

### RG5 — Limited Transferability Across Team Formation Contexts

Many reviewed studies examine semester-long academic projects, while others examine intensive hackathons.

Differences in duration, participant motivation, tasks, and evaluation conditions limit direct comparison.

**HackTeam Response:** Conduct context-specific evaluation with student hackathon participants where feasible and avoid unsupported generalization.

---

## 7. Theoretical Foundation for the Proposed HackTeam Approach

### 7.1 Multi-Criteria Matching Model

HackTeam proposes an initial weighted scoring model for ranking prospective teammate combinations.

The preliminary formula is:

`Score = w1 × R + w2 × A + w3 × E + w4 × P`

Where:

- **R:** Skill and role coverage.
- **A:** Availability overlap.
- **E:** Experience complementarity.
- **P:** Working preference alignment.
- **w1, w2, w3, w4:** Non-negative criterion weights.

The weights are intended to satisfy:

`w1 + w2 + w3 + w4 = 1`

Individual criteria will be normalized to comparable scales before aggregation.

The detailed scoring rules and weights will be specified in the algorithm design documentation.

The model remains preliminary and has not been experimentally validated.

### 7.2 Matching Constraints

Some requirements may be more appropriately represented as constraints rather than scoring criteria.

Potential constraints include:

- Maximum or minimum team size.
- Required team roles.
- Participation eligibility.
- Participant availability for essential activities.
- Duplicate team membership restrictions.

The project will distinguish mandatory requirements from preferences used to rank candidates.

### 7.3 Recommendation Transparency

The system should provide understandable explanations for recommendations.

Examples may include:

- Strong required-role coverage.
- High overlap in available time slots.
- Complementary technical skills.
- Similar preferred collaboration schedules.

These explanations should reflect the actual scoring method rather than generating unsupported compatibility claims.

### 7.4 Trial Sprint Mechanism

Trial Sprint is proposed as a short preliminary collaboration process before final team confirmation.

The conceptual workflow is:

1. **Candidate Recommendation:** Participants receive and review suggested teammates.
2. **Temporary Team Formation:** Interested students voluntarily create a trial team.
3. **Skill and Role Awareness:** Participants introduce their competencies and preferred responsibilities.
4. **Team Agreement:** Participants clarify deadlines, communication practices, and expectations.
5. **Collaborative Task:** The team completes a limited shared activity.
6. **Progress Checkpoint:** Participants review task progress and identify obstacles.
7. **Individual Reflection:** Participants provide optional feedback about collaboration.
8. **Team Confirmation:** Participants decide whether to continue working together.

The proposed process is informed by the reviewed research on group norms, team coordination, temporary collaboration, and participant decision-making.

Its effectiveness remains a hypothesis requiring empirical investigation.

### 7.5 Preliminary Collaboration Indicators

Potential indicators include:

| Indicator | Proposed Measurement | Interpretation Limit |
|---|---|---|
| Task completion | Completed agreed tasks / total agreed tasks | Depends on task difficulty |
| Deadline adherence | Tasks completed within agreed deadlines | Depends on external circumstances |
| Role coordination | Participant feedback about responsibility clarity | Subjective |
| Communication experience | Optional structured participant response | Sensitive to response bias |
| Recommendation usefulness | Participant rating of initial recommendations | Perceived suitability only |
| Willingness to continue | Participant decision or response after the trial | Does not guarantee future success |

Indicators must not be combined into an opaque reliability score without further research and justification.

---

## 8. Proposed Research Questions and Hypotheses

### 8.1 Research Questions

**RQ1:** How does multi-criteria teammate recommendation compare with a skill-only baseline in terms of role coverage, availability overlap, and participant-perceived suitability?

**RQ2:** Does a structured Trial Sprint provide participants with useful additional information when deciding whether to confirm a team?

**RQ3:** How do participants evaluate the transparency, usability, and perceived fairness of HackTeam's recommendation workflow?

**RQ4:** Which practical and methodological limitations arise when collecting preliminary collaboration observations?

### 8.2 Research Hypotheses

**H1:** Multi-criteria matching may produce more suitable recommendations according to selected predefined measures than skill-only matching.

**H2:** Trial Sprint participation may improve participants' perceived ability to make informed team confirmation decisions.

**H3:** Providing explanations for recommendation criteria may increase participants' perceived transparency of the matching process.

**H4:** Structured preliminary collaboration may reveal coordination concerns not apparent from participant profiles alone.

These hypotheses are not validated findings.

### 8.3 Preliminary Evaluation Strategy

A feasible evaluation may include:

**Evaluation A — Algorithm Comparison**

Compare skill-only matching with the proposed multi-criteria method using the same candidate pool.

Potential metrics:

- Required role coverage.
- Availability overlap.
- Recommendation suitability ratings.
- Matching execution time.
- Sensitivity to criterion weights.

**Evaluation B — Trial Sprint Feasibility**

Conduct a small pilot involving volunteer prospective teammates.

Investigate:

- Task completion.
- Ease of coordination.
- Participant-reported communication experience.
- Perceived usefulness of the Trial Sprint.
- Willingness to confirm the suggested team.

Where possible, participants should evaluate their initial recommendations before and after the Trial Sprint using comparable questions.

**Evaluation C — System Verification**

Verify core functionality through:

- Unit testing.
- Integration testing.
- Role-based access tests.
- Validation of matching constraints.
- Trial Sprint workflow tests.
- Usability testing.

Detailed instruments, sample size requirements, analysis procedures, and acceptance thresholds will be developed separately in the Verification and Evaluation Plan.

---

## 9. Ethical and Methodological Considerations

### 9.1 Participant Consent

Users participating in research activities should receive an understandable description of the research purpose and data collected.

Participation in interviews, questionnaires, and pilot evaluations should be voluntary.

### 9.2 Privacy and Data Minimization

HackTeam should collect only information necessary for the intended functionality.

Sensitive feedback should not automatically become public profile information.

Participant access to personal records and research data must be controlled.

### 9.3 Avoiding Unsupported Reliability Judgments

A short collaborative activity cannot reliably determine a person's long-term reliability, competence, or character.

Missing a deadline or contributing fewer visible messages may be explained by numerous external factors.

Therefore, Trial Sprint results should be treated as contextual decision-support information rather than definitive personal assessments.

### 9.4 Evaluation Bias

Potential sources of bias include:

- Small or non-representative student samples.
- Self-reported participant characteristics.
- Prior familiarity between teammates.
- Different task difficulty levels.
- Subjective satisfaction ratings.
- Differences in individual availability and workload.

These factors should be considered when interpreting findings.

### 9.5 Reproducibility

The final research report should document:

- Matching formulas and criterion definitions.
- Weight selection procedures.
- Data preprocessing and normalization.
- Baseline configuration.
- Pilot task descriptions.
- Evaluation instruments.
- Data exclusion rules.
- Statistical or descriptive analysis procedures.

The project should also report negative or inconclusive findings rather than presenting only favorable outcomes.

---

## 10. Limitations of the Literature Review

This review has several limitations.

First, it contains a targeted selection of twelve publications rather than an exhaustive review of all available research.

Second, the selected publications represent different disciplines, research settings, and methodological traditions. Their findings should not be treated as directly comparable measurements of a single outcome.

Third, some studies focus on classroom collaboration, whereas others examine online hackathons or general computational team assembly.

Fourth, detailed methodological and statistical information from some restricted-access publications was not fully available. Their analyses were consequently limited to statements supported by accessible publication information.

Fifth, the selected corpus includes publications from 2020–2024 and may not reflect subsequent developments.

Finally, the literature does not directly validate the proposed combination of multi-criteria matching and Trial Sprint.

These limitations will be considered during system design and empirical evaluation.

---

## 11. Conclusion

The reviewed literature demonstrates that student team formation is a multidimensional problem involving computational optimization, participant characteristics, user decision-making, and actual collaborative interaction.

Research on algorithmic team formation provides a foundation for structured matching based on several criteria. Optimization methods can generate team configurations under explicit requirements, but the quality of an algorithmic score should not be equated with guaranteed team success.

Studies of team conflict, psychological safety, and group norm development demonstrate that collaboration depends on factors that cannot be fully captured by static participant profiles.

Hackathon-specific research additionally emphasizes the importance of shared expertise, task coordination, communication, and time-constrained collaboration.

Together, these findings motivate HackTeam's proposed approach: transparent multi-criteria teammate recommendations followed by a short preliminary Trial Sprint before final team confirmation.

The proposed contribution is not an assumed improvement over all existing solutions. Instead, HackTeam aims to design a technically feasible system and investigate whether preliminary collaborative assessment adds useful information to algorithm-supported team formation.

The literature review establishes a foundation for subsequent requirements analysis, algorithm development, Trial Sprint design, and empirical evaluation.

---

## 12. References

Bergtold, J. S., & Shanoyan, A. (2024). Assessment of group formation methods on performance in group-based learning activities. *Frontiers in Education, 9*, Article 1362211. https://doi.org/10.3389/feduc.2024.1362211

Bowers, A., Bowers, M. R., Bryan, N., Letizia, P., & Murphy, S. (2023). Forming student teams to incorporate soft skills and commonality of schedule. *INFORMS Journal on Applied Analytics, 53*(2), 111–127. https://doi.org/10.1287/inte.2022.1129

Gómez-Zará, D., Das, A., Pawlow, B., & Contractor, N. (2022). In search of diverse and connected teams: A computational approach to assemble diverse teams based on members' social networks. *PLOS ONE, 17*(11), Article e0276061. https://doi.org/10.1371/journal.pone.0276061

Gómez-Zará, D., DeChurch, L. A., & Contractor, N. S. (2020). A taxonomy of team-assembly systems: Understanding how people use technologies to form teams. *Proceedings of the ACM on Human-Computer Interaction, 4*(CSCW2), Article 181. https://doi.org/10.1145/3415252

Hagvall Svensson, O., Johansson, A., & Adawi, T. (2024). How do students negotiate groupwork? The influence of group norm exercises and group development norms. *Journal of Engineering Education, 113*(3), 533–554. https://doi.org/10.1002/jee.20596

Huerta, M. V., Sajadi, S., Schibelius, L., Ryan, O. J., & Fisher, M. (2024). An exploration of psychological safety and conflict in first-year engineering student teams. *Journal of Engineering Education, 113*(3), 635–666. https://doi.org/10.1002/jee.20608

Maguire, D., & Keceli, Y. (2024). The impact of formation and diversity on student team conflict. *Active Learning in Higher Education, 25*(3), 409–423. https://doi.org/10.1177/14697874221144998

Mendes, W., Richard, A., Tillo, T.-K., Pinto, G., Gama, K., & Nolte, A. (2022). Socio-technical constraints and affordances of virtual collaboration: A study of four online hackathons. *Proceedings of the ACM on Human-Computer Interaction, 6*(CSCW2), 1–32. https://doi.org/10.1145/3555221

O'Toole, J., Ciuchta, M. P., Neville, F., & Lahiri, A. (2023). Transactive memory systems, temporary teams, and conflict: Innovativeness during a hackathon. *Journal of Management, 49*(5), 1633–1661. https://doi.org/10.1177/01492063221102397

Sanchez-Anguix, V., Alberola, J. M., Del Val, E., Palomares, A., & Teruel, M. D. (2023). Comparing computational algorithms for team formation in the classroom: A classroom experience. *Applied Intelligence, 53*, 23883–23904. https://doi.org/10.1007/s10489-023-04748-5

Schulten, C., Nolte, A., Spikol, D., & Chounta, I.-A. (2022). How do participants collaborate during an online hackathon? An empirical, quantitative study of communication traces. *Frontiers in Computer Science, 4*, Article 983164. https://doi.org/10.3389/fcomp.2022.983164

Wang, X., Song, G., & Ghannam, R. (2024). Enhancing teamwork and collaboration: A systematic review of algorithm-supported pedagogical methods. *Education Sciences, 14*(6), Article 675. https://doi.org/10.3390/educsci14060675

---

**Document Status:** Initial literature review prepared for academic peer review. The analysis, methodological limitations, and research implications will be refined based on supervisor feedback and additional evidence obtained during the HackTeam project.
