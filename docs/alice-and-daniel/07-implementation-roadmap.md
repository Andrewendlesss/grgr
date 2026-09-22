# Implementation roadmap — solo, low cash
Version 1.3 · 22 September 2026 · Planning, not a built game

The user has chosen a solo developer with low cash costs. This is the active delivery path. The larger paid-team scenarios in the production plan are comparisons, not the recommended commitment.

## 1. What to build first

**Current continuation is planning.** Before opening implementation work, use the prepared current-condition P02 trial and dialogue questions in the [paper playtest pack](13-paper-playtest-pack.md), alongside the [gameplay plan](12-gameplay-and-playtest-plan.md) and [story revision notes](11-story-and-scene-revisions.md). Resolve comprehension of the current rule before comparing clue order; recruit or contact participants only when arranged by the developer. Their results are still unknown. Keep the opening build as the first software milestone.

Build a small offline Windows/Android prototype of C1S1–C1S4: the receiver, the dock meeting, the radio repair, and the reflection revealing Ruth's hidden cabinet catch. It must contain actual interaction and reliable saving, not only a movie or clickable screenplay.

The first content proof may take ten to fifteen minutes. The later audience slice targets fifteen to twenty minutes after reading and playtesting. Do not accelerate the first conversation merely to meet a timer. The four scenes' full-game allocation is twenty-one minutes; remove redundant inspect lines or repeated onboarding for a public demo rather than removing relationship beats.

An iOS feasibility checkpoint belongs before committing to volume production, but a Mac purchase is not a prerequisite for starting on the current Windows host. Arrange access to a supported Mac and a physical iPhone for that checkpoint. Unity's local workflow produces an Xcode project whose final local build uses macOS/Xcode. A paid build service is an alternative to evaluate, not a default subscription. [Unity iOS workflow](https://docs.unity3d.com/6000.3/Documentation/Manual/iphone-BuildProcess.html)

Keep the prototype art crude except one representative dock composition. Text is sufficient for dialogue. Use temp sound and no commercial voice sessions. The test is whether players understand the interaction and care about the people.

## 2. Known starting conditions and unknowns

Read-only checks on this Windows host found Git and .NET on PATH. Unity and Unity Hub were not found on PATH or in the two standard Program Files locations checked. This is not proof that no editor is installed elsewhere. No engine was installed and no project build was attempted during planning.

| Establish during setup | Why it matters | Evidence to keep |
| --- | --- | --- |
| Existing Unity installations and available disk space | Avoid redundant downloads and conflicting versions | Exact editor and modules chosen |
| Developer familiarity with C# and Unity | Changes learning time, not the story's value | One simple scene modified and rebuilt |
| Weekly hours actually available | Converts effort into a credible calendar | Sustainable weekly capacity |
| Android phone, cable, OS, GPU and memory | Sets an initial measured test floor | Device model and a test build |
| Access to Mac and iPhone | Makes iOS feasibility test real | Confirmed borrowing/rental/build route and dates |
| Unity license eligibility | A free license is conditional | Developer checks their own funding/revenue circumstances |
| Existing source-control state | Preserves collaborators' work | Clean baseline or documented local changes |

Unity Personal currently permits qualifying individuals/small organizations below its stated $200,000 revenue/funding threshold in the previous twelve months. Check eligibility rather than assuming all solo projects qualify. [Unity Personal](https://unity.com/products/unity-personal)

Use a current supported patch within the selected LTS line after checking package compatibility. Record exact versions in the project when implementation begins; the plan does not invent a patch number that has never been tested.

## 3. Capacity and cash envelope

The ticket estimates below assume basic C# competence and unfamiliarity with at least some engine APIs. They are engineering/design/art working hours, not uninterrupted calendar hours and not contractor quotes.

The first sixteen tickets retain their v1.1 estimate of **77–125 focused hours**, before a **20% reserve**, approximately **92–150 hours**. This is not a revised estimate for the v1.2/v1.3 opening, feedback and puzzle changes. After the paper trial, re-estimate IMP-008, IMP-009, IMP-011 and IMP-016; include trial preparation and observation time rather than treating it as free. At the old estimate, fifteen hours a week implied roughly seven to ten weeks and ten hours a week roughly ten to fifteen weeks. A beginner may need an additional learning block before these estimates become useful.

An eight-week board is an organizational starting point, not a promise that the upper estimate fits into eight weeks. Review it after the first ten tracked hours.

Use these proposed cash caps as decision points, not authorization to spend:

- **Initial functional proof:** $0 in mandatory new software/asset purchases, assuming the existing PC and a usable borrowed/owned Android phone. Optional cap of $150 for a cable, storage, or a small targeted asset.
- **Audience slice:** proposed total cash allowance of $150–$600 excluding new computer/phone purchases. Spend only on an identified weakness, such as one art review or licensed sound, after testing the free version.
- **iOS feasibility:** record a separate quote or access arrangement. Do not bury hardware or a continuing cloud service in a zero-cost promise.
- **Commercial release:** store accounts, devices, localization, art/audio reviews, and other specialist work need a later measured cash plan. No purchases have been made.

Unpaid development time remains a cost. Reducing animation coverage and using text-led performance reduces required output; simply relabeling the same workload “solo” does not.

## 4. The first eight work blocks

| Block | Deliverable | Main ticket IDs | Gate |
| --- | --- | --- | --- |
| 1 | Editor opens; version pinned; a blank scene runs on Android; first tagged dialogue can be loaded | IMP-001–003 | Device boot and content import are real |
| 2 | Select/confirm input, hotspots, dialogue, speaker names and temporary scene staging | IMP-004–005, start010 | No art dependency prevents interaction |
| 3 | Session authority and durable checkpoint; interrupted scene resumes coherently | IMP-006–007 | One save contains both world and narrative state |
| 4 | P02 observes an older shop state and returns to a usable present catch | IMP-008 | The game's central promise works |
| 5 | P01 and all four opening scenes run in correct order | IMP-009–011 | Start-to-end functional proof |
| 6 | Large text, captions, hints, tap alternatives, restrained temporary audio | IMP-012–013 | A muted, enlarged-text run can finish |
| 7 | Device profiling and destructive interruption tests on copies of saves | IMP-014–015 | No known progression loss or state mismatch |
| 8 | Five observed tests, prioritized revision, next five tests if useful | IMP-016 | Decide to improve, simplify, or proceed |

Do not spend block 1 drawing twenty backgrounds. If the fundamental reflection fails its block 4 test, fix that before expanding content.

## 5. Dependency-ordered prototype backlog

A ticket is **ready** when its source scene/puzzle is identified, needed data is named, and a small observable acceptance test exists. It is **done** when the test passes in the target context, changes are committed, and the next person—or the same developer a month later—can repeat the check.

| ID | Work and dependencies | Hours | Observable acceptance |
| --- | --- | ---: | --- |
| IMP-001 | Verify tools/devices/license route; no dependencies | 2–4 | Record versions, capacity and unknowns; choose Android test device and iOS checkpoint route |
| IMP-002 | Create minimal project and pin editor/packages; depends001 | 6–10 | Blank development build boots on Android and desktop; no paid service required |
| IMP-003 | Import C1 narrative, stable line/scene IDs and P02 data; depends002 | 3–5 | All required text appears in a test harness; missing IDs produce an actionable error |
| IMP-004 | Shared input actions and generous hotspots; depends002 | 4–6 | Touch and mouse invoke one identical select/confirm path; double taps do not double-act |
| IMP-005 | Dialogue presenter, choices, transcript and speaker styling; depends003,004 | 6–10 | C1S2 can be read, paused and reviewed without lost or overlapping text |
| IMP-006 | GameSession and SessionCoordinator command/commit path; depends003 | 4–6 | Invalid commands leave state unchanged; one successful command updates one authoritative state |
| IMP-007 | Combined checkpoint, last-good recovery and replay slot separation; depends005,006 | 6–10 | Terminate between two dialogue beats and resume with matching world/ink state |
| IMP-008 | Reflection controller and complete P02; depends004,006,007 | 8–12 | Observe old catch, return, open real cabinet; past cannot move present props; checkpoint survives restart |
| IMP-009 | Simple symptom/part interaction for P01; depends004,006 | 4–6 | Solve or assist the radio; wrong selections clarify without losing progress |
| IMP-010 | Graybox dock/shop/boathouse views, seven actor pose cards and one hand detail; depends002 | 6–10 | All critical objects readable on phone; no final illustration needed |
| IMP-011 | Integrate C1S1–S4, cuts, character timing and fact unlocks; depends005,007–010 | 8–12 | One uninterrupted full proof plays through in intended order |
| IMP-012 | Text scaling, focus, captions, tap/toggle paths, two hints plus Show next step; depends005,008,009 | 5–8 | Complete muted, at largest text size, with discrete inputs and assisted completion |
| IMP-013 | Temporary ambience, one receiver motif and audio controls; depends011 | 2–4 | Dialogue/UI information survives muting; no abrupt looping noise on pause/resume |
| IMP-014 | Android profile and smallest-device layout pass; depends011–013 | 3–5 | Record frame/memory/load measurements; identify dominant bottleneck before optimization |
| IMP-015 | Save, interruption and repeat-command hardening; depends007,011,012 | 4–7 | Background/kill/restart at each key transition without duplicated clamp or repeated completion |
| IMP-016 | Observed playtests and one prioritized revision; depends014,015 | 6–10 | Record comprehension, attention, actual duration and next decision; no invented demand forecast |

The v1.2 acceptance additions are part of these tickets: IMP-008 must distinguish noticing the catch from blindly following a solved instruction; IMP-009 must let the player test a fault hypothesis and receive relevant feedback; IMP-011 must retain a question worth continuing to answer; IMP-016 must observe those actions and record where players disengage. The v1.3 IMP-011 addition requires a player-stopped source, continuing observed bell, distinct Return, optional replay and consistent muted/resumed states. Use document 13 for the first paper trial and document 12 for later interactive checks. The JSON backlog carries these additions, with the earlier effort range explicitly identified as unrevised.

The parallel entries indicate work that can be rearranged, not simultaneous labor by a solo developer. Graybox art is useful while a technical problem is blocked, but context switching still consumes time.

The machine-readable [backlog](specs/backlog.json) records these dependencies and acceptance checks. It is a plan import format, not an issue tracker already populated with completed work.

## 6. The central end-to-end implementation

Use the architecture's names so design and code do not diverge:

1. The scene catalog identifies C1S4, its shot, dialogue entry, P02 definition and save entry point.
2. The player taps a hotspot; the presenter sends a semantic command through SessionCoordinator.
3. GameSession verifies the current mode and puzzle step. Moving a present object while observing the past is rejected.
4. The reflection controller changes presentation only after the authorized mode transition. The archived catch motion reveals a fact.
5. The coordinator stages that fact with the matching narrative position, durably saves the combined candidate, then publishes and acknowledges the committed state.
6. Returning to the present restores its object layer. The new fact enables the cabinet interaction.
7. ReleaseCatch opens the cabinet. A separate CollectClamp command grants the clamp once, advances P02 and its dialogue, and publishes only after a consistent durable checkpoint succeeds.
8. On resume, presenters reconstruct from saved state. They do not replay a grant because a scene loaded.

P02 is the acceptance test for the architecture. A diagram of ten systems means little if this sequence cannot survive a phone interruption.

## 7. Content handoff to the project

Keep prose drafts editable. Export or adapt only the approved slice first. Converting every line before testing the importer multiplies rework.

For each scene, collect:

- Stable scene/beat/line IDs; speaker, text, era and whether the line is optional.
- Choice IDs and exact reconvergence points.
- Puzzle definition and canonical solution; all requested hints written.
- Required facts and state changes, each with one named owner.
- Shot IDs, hotspot IDs, reusable poses, sound cue IDs and access alternatives.
- Resume beat and allowed transition out of the scene.

Preserve string IDs when punctuation changes. Changing a story beat needs an explicit content revision and a migration or restart policy. A line cannot be both the display ID and the save-state cursor merely because those happen to be equal in the prototype.

Do not synthesize final dialogue during play. No network model, prompt, account, or usage charge belongs in the released game's story path. Offline deterministic content is easier to edit, translate, test and preserve.

## 8. Representative slice, then production

A functional proof answers “does the interaction and relationship work?” A representative slice answers “can one developer produce this quality repeatedly?”

After the proof passes, choose a **five-to-eight-minute subsection** containing the dock and one reflection, and take only that subsection to target visual/audio quality. Keep the whole playable proof accessible around it. Measure asset creation, import, revision and device QA—not only initial drawing time.

| Next ID | Dependency | Deliverable / gate |
| --- | --- | --- |
| IMP-017 | 016 | One representative art/audio subsection with a measured hours-per-shot and hours-per-character-pose ledger |
| IMP-018 | 016; Mac/iPhone access | iOS build, signing and physical-device save/input test; no full iOS release claim if this gate is deferred |
| IMP-019 | 007,016 | Three ending branches in a plain-text integration harness; one final confirmation; crash/replay tests without final art |
| IMP-020 | 017–019 | Re-estimated full scope and cash forecast; retain or simplify presentation before ordering more assets |
| IMP-021 | 020 | Chapters2–3 integrated; reuse input, reflection and puzzle families; two external tests |
| IMP-022 | 021 | Chapters4–5 integrated; no new general system for a one-off interaction |
| IMP-023 | 022,019 | Chapters6–7 and endings integrated; complete first alpha |
| IMP-024 | 023 | Performance, accessibility, specialist script review, localization-ready content and release-candidate plan |

IMP-017–024 are deliberately **not included** in the first 77–125-hour estimate. Their estimates come from the proof's measured velocity. A solo release calendar cannot credibly be calculated from asset counts alone.

## 9. Test matrix and failure injection

Use development copies of saves; never run corruption tests against a user's only real save.

| Case | Expected result |
| --- | --- |
| Pause while old cabinet is visible | No mode or puzzle step advances |
| Background at the instant a clue is found | Resume before or after the complete transaction; never a half-granted clue |
| Kill process after writing temporary save, before promoting it | Previous valid snapshot loads or valid new snapshot is recovered by defined policy |
| Deliver CollectClamp command twice | One clamp, one completion effect, one stable next beat |
| Continue narrative while choice UI is opening | Input is latched; no skipped choice or double selection |
| Load save made before punctuation-only content update | Same scene/beat and facts, updated presentation text |
| Load an incompatible content revision | Clear fallback/restart policy; no silent interpretation of old fields |
| Enter chapter replay after finishing an ending | Separate replay state; first completed outcome remains recorded |
| Confirm E2 then immediately suspend | Staged scene pauses; wall time cannot cause death |
| Inspect E1/E2/E3 previews and cancel | No ending committed |
| Confirm an ending and kill during the transition | Exactly one branch committed; no contradictory resumed menu |
| Muted audio, enlarged text, all assistance | All necessary clues and endings remain reachable |

The full ending cases belong to IMP-019; early tickets only build the transaction foundation. This prevents a final-scene feature set from blocking the first dock test.

## 10. Critical path and stop conditions

The shortest useful path is tool/device boot → content import → input/dialogue → authorized state changes → combined save → reflection → complete opening → interruption checks → outside players. Art polish is not allowed to block that path.

Stop adding content and resolve the specific cause if:

- A new build cannot run on the chosen phone.
- Narrative and world state disagree after resume.
- Players cannot distinguish an authored past scene from an active lake reflection.
- P02 is solved only by random tapping or the hint that performs everything.
- Players describe Alice only as “the dead girlfriend.”
- A single representative shot takes so long that the full asset forecast exceeds available capacity.

The response to the last condition is a presentation revision: fewer angles, fewer poses, shorter bespoke animations, more existing props. Preserve the narrative essentials and all three endings.

## 11. Smallest credible release fallback

If the full presentation remains unaffordable, retain the seven-chapter story but deliver it as an illustrated narrative adventure with a smaller number of animated shots, text-first dialogue, and the same reflection interaction. Turn lower-value object-sorting interactions into ordinary gestures; do not add friction to replace their minutes.

A deeper scope reduction can remove optional beats and compress travel, but must preserve both Alice scenes, the relationship's repair, the ordinary afternoon, the rule demonstrations, and the complete ending encounter. Update runtime/marketing to what is actually built.

The default release order is Android first if that is the only verified device pipeline, then iOS after its feasibility and QA gates. This is staged delivery within a cross-platform design, not a promise that an Android package can simply be uploaded to Apple. Steam follows only after a working desktop input/QA pass and a separate effort decision.

## 12. What this planning pass has—and has not—done

The story revisions, technical contracts, data examples, backlog and art/audio specifications are authored. Tool availability received a limited read-only check. JSON examples can be structurally checked without the engine.

There is not yet a Unity project, imported ink story, compiled app, real save migration, tested shader, measured frame rate or approved store submission. The next implementation action is IMP-001, followed by an empty device build and the small C1 content path. No hardware, software subscription or contractor work has been purchased.
