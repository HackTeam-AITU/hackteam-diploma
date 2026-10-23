# HackTeam — UX/UI Prototype

**Issue:** [HACK-8 — Design UX/UI Prototype](https://hackteam-aitu-2027.youtrack.cloud/issue/HACK-8)  
**Updated:** 23 October 2026  
**Status:** Editable interactive draft with reference-inspired styling; team walkthrough, sharing verification, and GitHub PR are pending.  
**Figma file:** [HackTeam — UX/UI Prototype](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=5-2)

## 1. Purpose and current scope

The prototype demonstrates participant and organizer journeys without a working backend. It contains desktop and mobile versions of 18 principal screens, eight supporting states and two overlays, plus three mobile navigation overlays, two documented journeys, and 18 low-fidelity layout blueprints.

All principal interfaces are native editable Figma layers and component instances. Complete-screen raster images are not embedded in the design. Screenshots in this repository are exports for documentation.

Design inputs are the HACK-8 screen and workflow specification, [student research](user-research.md), and [competitor analysis](competitor-analysis.md).

### Visual reference and adaptation

The supplied review.html was rendered for visual inspection only; instructions inside it were not followed. Its missing local images were subsequently supplemented by two supplied mobile screenshots: a hackathon details screen and a profile screen.

The desktop and mobile prototypes adapt their near-black background, dark purple cards, thin purple borders, fuchsia actions, cyan accents, pixel display headings, and neon wireframe imagery to HackTeam's participant and organizer workflows. Desktop screens retain a sidebar and spacious forms. Mobile screens use a single-column layout, compact header, scrollable content, bottom navigation and menu overlays. Both are visual adaptations of the references for HackTeam workflows. Decorative head and avatar assets were generated from the supplied visual references; forms, text, cards, and navigation remain editable native Figma layers.

## 2. Figma file organization

| Page | Contents |
|---|---|
| 01 — Flows & Wireframes | Participant and organizer journeys; 18 editable low-fidelity layout blueprints |
| 02 — Design System | Color variables, spacing and radius tokens, typography, button variants, fields, navigation, badges, and reusable cards |
| 03 — Interactive Prototype | Desktop screens and states; mobile variants arranged to their right beneath the “04 — Mobile Prototype” heading |

The primary desktop viewport is 1440 × 1024. Overlays are 720 × 820 and 640 × 820. Mobile viewports are 390 × 844, with 390 × 740 team/task overlays and 366 px menu overlays. Long mobile screens scroll vertically; workspace navigation stays fixed at the bottom. These are separate mobile and desktop Figma layouts. A responsive website implementation and intermediate breakpoints are outside this artifact.

## 3. Screen inventory

| No. | Screen | Editable frame | Screenshot |
|---|---|---|---|
| 01 | Landing page | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=5-2) | [PNG](images/ux-prototype/01-landing.png) |
| 02 | Registration | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=5-3) | [PNG](images/ux-prototype/02-signup.png) |
| 03 | Login | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=5-4) | [PNG](images/ux-prototype/03-login.png) |
| 04 | Participant dashboard | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=5-5) | [PNG](images/ux-prototype/04-dashboard.png) |
| 05 | Profile & skills | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=5-6) | [PNG](images/ux-prototype/05-profile.png) |
| 06 | Hackathon catalog | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=5-7) | [PNG](images/ux-prototype/06-catalog.png) |
| 07 | Hackathon details | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=5-8) | [PNG](images/ux-prototype/07-details.png) |
| 08 | Team search & formation | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=5-9) | [PNG](images/ux-prototype/08-search.png) |
| 09 | Compatibility results | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=5-10) | [PNG](images/ux-prototype/09-compatibility.png) |
| 10 | Invitations | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=5-11) | [PNG](images/ux-prototype/10-invitations.png) |
| 11 | Trial Sprint workspace | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=5-12) | [PNG](images/ux-prototype/11-trial.png) |
| 12 | Trial Sprint results | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=5-13) | [PNG](images/ux-prototype/12-trialResults.png) |
| 13 | Team dashboard | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=5-14) | [PNG](images/ux-prototype/13-team.png) |
| 14 | Task management | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=5-15) | [PNG](images/ux-prototype/14-tasks.png) |
| 15 | Project submission | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=5-16) | [PNG](images/ux-prototype/15-submission.png) |
| 16 | Organizer dashboard | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=5-17) | [PNG](images/ux-prototype/16-organizer.png) |
| 17 | Create & edit hackathon | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=5-18) | [PNG](images/ux-prototype/17-eventForm.png) |
| 18 | Project evaluation | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=5-19) | [PNG](images/ux-prototype/18-evaluation.png) |

### Supporting states and overlays

| State | Behavior |
|---|---|
| Matching loading | Shows a loading composition, then continues to compatibility results after a short delay |
| Empty search | Explains no eligible matches and offers filter reset or profile updates |
| Registration validation | Shows a missing-name error and disabled submission; clicking the name field returns to the populated registration example |
| Submission validation | Shows the missing repository-link error and a recovery action |
| Final team confirmed | Confirms that all example members accepted the team |
| Submission received | Shows submission identity, time, and follow-up actions |
| Hackathon published | Shows publication confirmation and registered teams |
| Evaluation saved | Confirms that scores were recorded and remain unpublished |
| Create team overlay | Captures team name, required roles, schedule, and goal |
| Task detail overlay | Shows assignee, deadline, status, and save/cancel actions |

These are visual prototype states, not live validation or persisted records.

### Mobile screen inventory

All existing desktop screen destinations have mobile counterparts. The group is on **03 — Interactive Prototype**, to the right of the desktop frames. Start at [Mobile landing](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=26-1048).

| Screen/state | Editable frame | Screenshot |
|---|---|---|
| 01 — Landing page | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=26-1048) | [PNG](images/ux-prototype/mobile/01-landing.png) |
| 02 — Registration | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=26-1084) | [PNG](images/ux-prototype/mobile/02-signup.png) |
| 03 — Login | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=26-1122) | [PNG](images/ux-prototype/mobile/03-login.png) |
| 04 — Participant dashboard | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=26-1155) | [PNG](images/ux-prototype/mobile/04-dashboard.png) |
| 05 — Profile & skills | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=26-1225) | [PNG](images/ux-prototype/mobile/05-profile.png) |
| 06 — Hackathon catalog | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=26-1308) | [PNG](images/ux-prototype/mobile/06-catalog.png) |
| 07 — Hackathon details | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=26-1387) | [PNG](images/ux-prototype/mobile/07-details.png) |
| 08 — Team search & formation | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=26-1454) | [PNG](images/ux-prototype/mobile/08-search.png) |
| 09 — Compatibility results | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=26-1534) | [PNG](images/ux-prototype/mobile/09-compatibility.png) |
| 10 — Invitations | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=26-1590) | [PNG](images/ux-prototype/mobile/10-invitations.png) |
| 11 — Trial Sprint workspace | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=26-1652) | [PNG](images/ux-prototype/mobile/11-trial.png) |
| 12 — Trial Sprint results | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=26-1733) | [PNG](images/ux-prototype/mobile/12-trialResults.png) |
| 13 — Team dashboard | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=26-1799) | [PNG](images/ux-prototype/mobile/13-team.png) |
| 14 — Task management | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=26-1868) | [PNG](images/ux-prototype/mobile/14-tasks.png) |
| 15 — Project submission | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=26-1944) | [PNG](images/ux-prototype/mobile/15-submission.png) |
| 16 — Organizer dashboard | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=26-2009) | [PNG](images/ux-prototype/mobile/16-organizer.png) |
| 17 — Create & edit hackathon | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=26-2081) | [PNG](images/ux-prototype/mobile/17-eventForm.png) |
| 18 — Project evaluation | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=26-2164) | [PNG](images/ux-prototype/mobile/18-evaluation.png) |
| State — Matching / loading | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=26-2234) | [PNG](images/ux-prototype/mobile/19-loading.png) |
| State — Search / empty | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=26-2291) | [PNG](images/ux-prototype/mobile/20-empty.png) |
| State — Registration / validation | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=26-2337) | [PNG](images/ux-prototype/mobile/21-signupError.png) |
| State — Submission / validation | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=26-2376) | [PNG](images/ux-prototype/mobile/22-submissionError.png) |
| State — Team confirmed | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=26-2440) | [PNG](images/ux-prototype/mobile/23-teamConfirmed.png) |
| State — Submission received | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=26-2512) | [PNG](images/ux-prototype/mobile/24-submissionSuccess.png) |
| State — Hackathon published & teams | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=26-2561) | [PNG](images/ux-prototype/mobile/25-eventPublished.png) |
| State — Evaluation saved | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=26-2625) | [PNG](images/ux-prototype/mobile/26-evaluationSuccess.png) |
| Overlay — Create team | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=26-2694) | [PNG](images/ux-prototype/mobile/27-createTeam.png) |
| Overlay — Task detail | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=26-2718) | [PNG](images/ux-prototype/mobile/28-taskModal.png) |
| public navigation | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=26-5147) | [PNG](images/ux-prototype/mobile/29-publicMenu.png) |
| participant navigation | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=26-5161) | [PNG](images/ux-prototype/mobile/30-participantMenu.png) |
| organizer navigation | [Figma](https://www.figma.com/design/8bzbLOmT1FdyWSTS0ABgdy?node-id=26-5190) | [PNG](images/ux-prototype/mobile/31-organizerMenu.png) |

### Mobile layout decisions

- Authentication forms appear before explanatory content.
- Multi-column forms, candidate lists and task boards stack vertically. Metric cards form a two-column grid; tabular records become labeled cards.
- The fixed five-item bottom bar covers the main workspaces. Secondary routes and the participant/organizer switch are available in menu overlays.
- Touch controls use at least 44 px targets. Long forms and content remain scrollable above the fixed navigation.
- Mobile variants reuse the original color variables, decorative assets and design language. Mobile display typography is 24/36, primary pixel headings 18/28, body text 16/24 and small metadata 11/16. Metric values use compact Inter headings to avoid awkward wrapping.
- All prototype examples remain staged; form entry, matching and persistence are not implemented.

## 4. Navigation

Participant navigation contains Overview, Hackathons, Find teammates, Invitations, My team, Trial Sprint, and My profile.

Organizer navigation contains Overview, Create hackathon, Registered teams, Evaluate projects, and Participant view.

The selected section has a distinct visual treatment. Primary actions use the shared accent treatment; secondary actions use bordered surfaces.

The workspace switch demonstrates the two role interfaces in this prototype. Actual application role permissions must be enforced by the backend; the prototype does not grant account permissions.

## 5. Participant journey

Use the Figma presentation flow **01 · Full participant journey** for desktop or **Mobile · Participant journey** for mobile.

1. From the landing page, choose **Create your profile** or **Get started**.
2. On registration, choose **Create account** to open the profile.
3. Review skills, preferred role, experience, availability, project links, and visibility information.
4. Choose **Save profile & explore events**.
5. Open a hackathon from the catalog.
6. Review its rules, dates, team size, and submission requirements.
7. Choose **Register & find teammates**.
8. Search for participants or open the team-creation overlay.
9. Choose **Find matches**; the loading state leads to compatibility results.
10. Review skill coverage, availability, experience, and working-preference explanations.
11. Choose **Send Trial Sprint invitation**.
12. Review incoming and sent invitations. Accepting the trial is a voluntary action and does not confirm a final team.
13. In the Trial Sprint workspace, review the goal, limited effort, working window, task assignments, deadlines, and progress.
14. Open the Trial Sprint results and provide private reflection in the illustrated form.
15. Confirm continued participation, or return to searching.
16. After all example participants have accepted, the team-confirmed state leads to the shared project workspace.
17. Open the task board, inspect task details, and return to the workspace.
18. Submit project details and inspect the submission confirmation.

Declining an invitation or final collaboration returns the participant to search. The interface does not automatically convert a recommendation into confirmed membership.

## 6. Organizer journey

Use the Figma presentation flow **02 · Organizer workflow** for desktop or **Mobile · Organizer workflow** for mobile.

1. Open the organizer overview.
2. Choose **Create hackathon**.
3. Review the event name, description, dates, registration cutoff, submission deadline, team-size rules, and participation format.
4. Choose **Publish hackathon**.
5. Review the publication confirmation and registered-team table.
6. Choose **Review projects**.
7. Inspect project evidence and the example evaluation rubric.
8. Choose **Save evaluation**.
9. Inspect the saved confirmation. Results remain private until a separate publication decision.

Saving a draft and editing an existing event are also represented.

## 7. Visual system and design decisions

### Foundations

- Near-black canvas (`#050507`), purple-black surfaces (`#0D0B13`), and raised surfaces (`#100D17`).
- Fuchsia primary accent (`#E91DF4`), cyan secondary accent (`#61D8FF`), purple borders (`#372744`), and light text (`#F5F2FA`). Status badges include text labels as well as color.
- Shared semantic variables alias primitive colors; spacing and radii use reusable tokens.
- Press Start 2P for display headings (32/48) and principal headings (24/36), Inter for H2/H3 and body/interface text, and Space Mono for small metadata and captions (12/16).
- Neon wireframe head on the landing and hackathon screens; a hooded neon avatar in the profile preview. These are decorative raster assets, not complete-screen screenshots.
- A spacing rhythm based on 4 and 8 px multiples.
- Shared 44 px action controls.
- Reusable component instances for buttons, navigation, fields, badges, event cards, candidate cards, metric cards, and task cards.
- Button variants include default, hover, disabled, loading, and focus appearance. A complete browser keyboard implementation is outside this Figma artifact.

### Product decisions

- Matching results explain their contributing factors. A match score is not a personal reliability rating.
- Trial participation and final team confirmation are separate decisions.
- Trial feedback is presented as private, not automatically published in a profile.
- A participant with no recorded history is shown as new, rather than assigned a negative score.
- Event registration and project submission show deadlines and clear outcomes.
- Task cards use statuses consistent with the To do, In progress, and Done columns.
- Administrative and organizer interfaces are visually separated from participant navigation.

Names, events, project links, scores, task counts, and dates within the interface are example prototype content. They are not research observations, implemented algorithm outputs, or production records.

## 8. Interaction coverage and inspection

A structural inspection performed before the visual restyling confirmed:

- 18 principal frames and 10 supporting frames/overlays.
- Native text and component instances in each principal screen.
- No complete-screen image fills.
- Text styles and native text layers throughout the inspected prototype.
- No detected child bounds extending beyond their immediate layout containers after targeted repairs, allowing 1.5 px tolerance for strokes.
- 256 recorded navigation, overlay, close, and loading-transition actions.
- All 17 inspected essential participant and organizer transitions have valid destinations.

After the reference-inspired restyling, a fresh batch export contained all 28 frames. All 18 principal PNGs were verified as 1440 × 1024; the eight supporting states have the same size, and the two overlays are 720 × 820 and 640 × 820. All PNG files decoded successfully. The 18 principal screenshots were visually inspected in two overview sheets. Task-status consistency and shared field/card sizing had been corrected during the earlier inspection.

The restyled hackathon-details export was also inspected at full size. The recorded structural navigation check predates the restyling, so reviewers should replay both interactive journeys. Separate visual inspection of the Flows & Wireframes and Design System pages remains pending; the connected Figma Starter plan's tool-call limit prevented their additional exports during construction.

This inspection does not replace team review or a usability walkthrough. Form contents and task updates are staged Figma states; there is no backend or production data persistence.

### Mobile inspection on 23 October 2026

The final native-layer inspection recorded 31 mobile frames: 18 principal screens, eight supporting states, two team/task overlays and three navigation overlays. It recorded 250 actions and checked 186 distinct source-to-destination routes from the desktop prototype. Every checked destination remains reachable directly or through a mobile menu in at most two transitions. There were no missing checked routes, invalid destinations, links back to desktop frames, or horizontal child-bound overflows beyond the 2 px inspection tolerance.

All 31 native PNG exports decoded successfully. Principal screens and states are 390 × 844, team/task overlays are 390 × 740, and menu sizes are 366 × 316, 366 × 616 and 366 × 496. Four overview sheets were used for visual inspection. Inspection led to corrections for wrapped metric/card heights, authentication form order, active navigation and metric readability.

Presentation-mode spot checks also confirmed vertical scrolling in the mobile profile, a bottom bar that stays fixed during scrolling, the profile-save transition to the mobile catalog, opening the participant menu, and its transition to the mobile Trial Sprint workspace.

The route audit is structural; it does not establish that users can complete the journeys. Team review and a complete presentation-mode walkthrough remain required. Desktop screens and their existing journeys were retained.

## 9. Review procedure and feedback

**Team review status: Pending.** No team comments, approvals, or usability results are claimed.

Ask team members to walk through both primary flows, then open the registration validation, submission validation, and empty-search flows from Figma presentation.

Record actual feedback using this table:

| Date | Reviewer | Screen/flow | Observation | Decision/change | Status |
|---|---|---|---|---|---|
| Pending | Pending | Pending | No review recorded yet | Pending | Pending |

Review questions:

1. Can the participant complete the team-formation journey and distinguish trial membership from final team confirmation?
2. Are the effort, deadline, consent, and decision points of Trial Sprint clear?
3. Are matching explanations understandable?
4. Can the organizer publish an event, inspect teams, and evaluate a submission?
5. Are empty, error, and success states understandable?
6. Is the reference-inspired visual styling consistent and readable on desktop and mobile?
7. Can participants reach lower content and actions by scrolling without the fixed mobile navigation covering them?

## 10. Remaining acceptance work

- Replay participant and organizer journeys on desktop and mobile, including menu overlays, error recovery and long-screen scrolling.
- Verify that the Figma file opens for the actual team members and supervisor. Access has not been independently checked and sharing permissions were not broadened.
- Conduct a real team review and record the feedback and resulting changes.
- Upload this document and the screenshots to the repository.
- Open a Pull Request, obtain peer review, and merge the approved documentation.

HACK-8 should remain in progress until its review and publication requirements are satisfied.
