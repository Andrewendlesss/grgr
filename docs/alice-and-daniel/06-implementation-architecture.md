# What the Water Keeps — implementation architecture

Version 1.2 · 22 September 2026 · Engineering proposal, not an implemented game

This document turns the authored design into a buildable first project for the user's confirmed **solo development and low-cash-cost approach**. Start with the chapter-one prototype and P02; expand a proven workflow across the remaining scenes. Specialist work is optional and purchased only for a bounded need. It does not require a custom game engine, a general-purpose quest editor, or a backend. The timing allocations in the design remain unverified.

## 1. Technical decisions and ownership

The [v1.2 gameplay revision](12-gameplay-and-playtest-plan.md) changes authored evidence, feedback and bounded interaction choices. Retain this architecture. P02's existing transition manifest still owns its completion path and its separate ReleaseCatch/CollectClamp transactions. Read-only inspections and wrong-hypothesis responses must not grant effects. P01 diagnostic selections and P07 mix settings belong to each puzzle's existing local state; any new resumable values must be explicitly specified before implementation. Reuse solved P11 data at P12 rather than requiring a second alignment puzzle. These are prospective content changes, not implemented reducers or verified save migrations.

Use **Unity 6.3 LTS, C#, Universal Render Pipeline, and ink** for the first export spike. Choose a provisional exact editor patch and compatible package versions after Android and Windows builds run; commit that version record and dependency lockfile. Confirm or revise that selection during the Mac/iPhone feasibility milestone **IMP-018**, before committing to iOS production. Mac access does not block the first Android prototype. Unity lists 6.3 support through December 2027. Unity also recommends its Update releases for new/mid-cycle production: our LTS choice is a provisional reproducibility decision, not a claim that LTS is always preferable. Revisit at the production-slice gate and fund the upgrade already reserved in the production plan. [Unity release support](https://unity.com/releases/unity-6/support)

Use uGUI with TextMesh Pro for the slice's screen-space interface; Unity's Input System supplies action bindings. Use Unity Localization for string tables and local asset lookup. Keep story audio and content bundled for offline play. Do not add remote content delivery, accounts, telemetry SDKs, an advertising SDK, or cloud saving to establish the core loop. There is no runtime AI service or API bill. Use direct references first, without a dependency-injection framework, general event bus, or custom Addressables deployment. Check Unity Personal eligibility against the actual revenue/funding situation before treating the editor as a zero-cost tool; the production plan records the dated license research.

| Decision | Reason and consequence | Revisit when |
|---|---|---|
| Fixed-camera 2.5D scenes | Painted surfaces, shallow geometry, small animation library; author explicit aspect-ratio crops | A necessary interaction cannot be staged readably |
| Local camera-to-texture reflections | A controlled view of selected past content; bounded rendering work | Measured device performance misses the slice gate |
| ink owns narrative flow; C# owns world facts | Writers can test conversations; puzzle truth has one owner | Never duplicate a fact to avoid an inconvenient interface |
| Plain C# reducers and explicit references | Small team can debug the whole change path | A measured dependency problem justifies another abstraction |
| Local, versioned combined saves | No online dependency; honest reinstall limitations | A funded platform port requires tested sync |
| One installed content set | No live-content lifecycle during initial production | Final package size requires a separately tested delivery plan |

These are project decisions. The sources establish platform capabilities, not this game's performance or commercial suitability.

## 2. Project layout and module boundaries

Create the actual Unity project only after the first implementation milestone begins. Proposed repository layout:

```text
game/WaterKeeps/
  Assets/_Game/
    Bootstrap/                 composition root and persistent services
    Runtime/Domain/            GameSession, commands, reducers, invariants
    Runtime/Narrative/         NarrativeAdapter and ink tag parser
    Runtime/Presentation/      dialogue, ledger, hotspots, shot/actor drivers
    Runtime/Reflection/        view composition and alignment presentation
    Runtime/Persistence/       SaveRepository, migrations, validation
    Runtime/Platform/          lifecycle, build information, input routing
    Content/Scenes/C01/        scene definitions and camera/prop bindings
    Content/Narrative/         chapter ink sources and compiled imports
    Content/Localization/      strings, locale settings, font assets
    Content/Audio/             cue definitions and delivered runtime clips
    Art/                       runtime-ready textures, meshes, animation
    Editor/                    content validation and export utilities
    Tests/EditMode/            reducers, migration, content contracts
    Tests/PlayMode/            UI/scene integration and resume fixtures
  Packages/                    pinned manifest and package lock
  ProjectSettings/             exact editor and rendering configuration
source-assets/                 authored masters using large-file storage
docs/alice-and-daniel/          this planning package
```

Begin with four assembly boundaries: Domain, Runtime, Editor, Tests. Domain has no Unity scene-object references. Avoid creating an assembly for every folder. Commit Unity `.meta` files with assets; exclude generated caches, local preferences, exported builds, signing material, and temporary recordings. Record asset creator, license, source location, and delivery version in the asset register.

The bootstrap scene owns one `SessionCoordinator`, `SaveRepository`, audio router, input router, and UI root. Load one location kit plus its current dressing at a time. A `SceneDefinition` binds a story scene such as `C1S4` to a location, era, initial shot, ink entry, puzzle, and checkpoint. A `ScenePresenter` constructs visuals from committed state. It never decides that a cabinet has opened because an animation finished.

`GameSession` holds scene/checkpoint identifiers, world and puzzle facts, local choice callbacks, narrative snapshot, current display packet, and ending commitment. `SessionCoordinator` serializes all progression commands. `NarrativeAdapter` wraps the ink runtime; it can mutate a **staged** narrative instance only under the coordinator. `SaveRepository` deals with bytes and validity, not character intentions. Presenters receive read-only snapshots and send commands.

## 3. Content identifiers and authoring pipeline

Keep existing scene IDs `C1S1`–`C7S4` and puzzle IDs `P01`–`P12`. Add stable line IDs such as `C1S4.L001`, choice IDs `C1S4.CH001.A`, checkpoints `C1S4.CP03`, cue IDs `AUD.SHOP.CATCH`, and prop IDs `PROP.SHOP.CABINET`. IDs never derive from translated text, list position, an object's display name, or a Unity instance ID. Reserve deleted IDs; do not renumber a chapter after inserting dialogue.

Every line record includes speaker, source text, scene/era, listener, intention, performance note where necessary, and optional audio cue. Choices receive separate display IDs and stable outcome IDs. The screenplay remains the readable editorial source until a scene is converted; after conversion, ink plus its exported line table becomes that scene's executable narrative source. Update the screenplay from the same approved revision to prevent two competing scripts.

ink tags carry identifiers and presentation requests: line, speaker, shot, pause point, or a named interaction handoff. They cannot execute arbitrary methods or write a world variable. Validate against an allowlist. Emit a localization key from the line ID; the compiled ink text is the English fallback and authoring preview, while the shipped presenter resolves the table entry. Do not compile a different story graph for every language. Branch on IDs and facts, never translated text. Avoid concatenating grammatical sentence fragments.

The current official integration imports source as `InkFile`; its documented access is `InkFile.storyJson`. Older tutorials may assume a JSON `TextAsset`. Pin and test one integration revision and isolate this difference inside `NarrativeAdapter`. Use its preview tools for narrative testing, then exercise the actual game bridge. [inkle Unity integration](https://github.com/inkle/ink-unity-integration)

Pipeline: approved scene → assign IDs → ink conversion → compile → export source-string table → validate references and branches → connect placeholder staging → play on phone → performance read-through → art/audio integration → localization and in-context review. CI fails on duplicate IDs, missing required text, unbound props, unknown tags, undeclared outcomes, or a checkpoint that cannot resume. Narrative reachability testing needs authored expected paths; compilation alone cannot prove emotional or logical correctness.

## 4. One authority for narrative and puzzle state

The domain state owns facts including `P02.stage`, `cabinetOpen`, observed evidence, inventory, selected ending, and completed scene milestones. ink owns its flow position, visit counts, and conversation-local variables. Any fact needed by both is stored in Domain and exposed to ink through pure queries at a stable handoff. Do not mirror `cabinetOpen` in an ink variable and later try to reconcile two answers.

Conceptual contracts, to implement rather than copy as working APIs:

```text
SessionCoordinator.Submit(Command, expectedRevision) -> CommitResult
NarrativeAdapter.StageAdvance(snapshot, command, factView) -> NarrativeCandidate
PuzzleReducer.Reduce(world, command) -> WorldCandidate
SaveRepository.WriteValidated(SessionSnapshot) -> SaveReceipt
ScenePresenter.Render(ReadOnlySession, PresentationPacket)
```

A command carries its kind, stable target ID, arguments, expected session revision, and operation ID. Reject a command from an obsolete screen or disallowed mode; repeated operation IDs return the existing result. The coordinator blocks overlapping progression commands while committing. A rapid double tap cannot open two cabinets, choose two lines, or select two endings.

For a progression command: validate preconditions; clone candidate world and ink state; apply the reducer; advance ink only to the next visible line, choice, or explicit interaction handoff; collect an immutable presentation packet; check invariants; serialize the **combined** candidate; save; then replace the live snapshot and present the result. On error, discard the candidate. ink external functions must be pure queries; they must not write files, grant items, or play sounds while speculative narrative evaluation is running.

ink supports narrative-state JSON serialization, but that does not automatically make Unity world state transactional. The adapter wraps its save/load API inside our own combined snapshot. [ink runtime integration and saving](https://github.com/inkle/ink/blob/master/Documentation/RunningYourInk.md)

Store the currently displayed line/choice packet alongside the ink cursor that produced it. Restoring must show that packet before continuing; otherwise a cursor saved after `Continue()` can skip the visible line. Acknowledging dialogue can use a short write queue, but a consequential choice, clue, item, puzzle completion, scene transition, or ending confirmation is acknowledged only after durable save success. Read-only camera motion and slider preview do not generate saves. If storage fails, retain the previous state, show a plain retry message, and permit returning to the menu; do not pretend progress was kept.

## 5. Save format, interruptions, and recovery

Use a versioned JSON envelope containing `schemaVersion`, `contentVersion`, compiled-story hash, build ID, slot ID, save sequence, session revision, current scene/checkpoint, domain data, ink snapshot, display packet, and checksum. Hash the exact serialized payload bytes; a checksum detects corruption and is not an anti-cheat mechanism. Store settings separately so a damaged story save does not reset text size.

Keep a current and previous valid snapshot per playthrough slot. Write a new candidate to a temporary file on the same volume, flush and close it, reread and validate it, then replace the older slot file using the platform-tested operation. Never overwrite both valid copies together. On launch, validate both completed slot files and choose the highest valid sequence. Ignore unfinished temporary files; preserve failed files for optional local diagnostics. Do not promise filesystem atomicity until Android/iOS kill tests prove the chosen implementation. The product guarantee is recovery to the last validated checkpoint, not survival of every uncommitted frame.

Use Unity's persistent data directory, with an unchanging released bundle identifier. Updates, backups, and uninstall are different cases: test the first two and explain local-save loss if the app is removed without a supported backup. [Unity persistentDataPath](https://docs.unity3d.com/6000.3/Documentation/ScriptReference/Application-persistentDataPath.html)

Save at state boundaries throughout play; pause/focus callbacks request a flush and halt input, dialogue autoplay, Timeline playback, and audio as appropriate. A mobile process may disappear without another useful callback, so lifecycle callbacks supplement normal saves. Resume behind a pause/recap screen; clear held pointer state and stale confirmations. No elapsed real-world time affects danger, grief, relationship outcomes, or ending selection.

Migrations are explicit transformations `v1 → v2 → v3`, each tested on retained fixtures. A structurally loadable ink save can still point into changed story content. Compare compiled-story hashes. For unchanged flow, test restoration directly. For changed flow, use a curated checkpoint map: reconstruct a known narrative entry from saved domain facts and approved local choices, preserving the display packet only when its line still exists. Do not guess a nearby knot or silently start a new game. If neither migration nor the previous snapshot works, explain recovery choices and keep the damaged save until the player explicitly starts anew.

Chapter and ending replay create a separate replay session copied from an immutable chapter/pre-choice checkpoint. They cannot replace the main playthrough. Ending credits/completion can be derived from a committed ending checkpoint, so a crash between completion and a profile update cannot lose credit.

## 6. P02: one complete implementation path

P02 is the first full reflection puzzle in `C1S4`: observe Ruth's cabinet routine from the actual shore, return, open the present cabinet, collect the damping clamp, and set aside the unrelated envelope. This is the slice's architecture test.

| Stage | Player command and requirement | Committed change / presentation |
|---|---|---|
| `shore_ready` | Select loading-door anchor | Enter alignment view; show ordinary/recorded distinction |
| `aligning` | Adjust large control; Observe after readable alignment | `observing`; play recorded cabinet beat; present-world hotspots disabled |
| `observing` | Recorded beat reaches its authored evidence handoff | Add `OBS.SHOP.CATCH`; `evidence_seen`; duplicate event is harmless |
| `evidence_seen` | Return | `returned`; present view restored; observed note retained |
| `returned` | Inspect panel / select its lip | `panel_exposed`; enlarged diagram available |
| `panel_exposed` | Release catch | `cabinet_open`; recorded handle resistance is no longer relevant |
| `cabinet_open` | Take damping clamp and set envelope aside | `complete`; add clamp once; checkpoint and next-scene handoff |

Returning early from `observing` without evidence resumes `shore_ready`; reopening the recording remains free. Replay after evidence is allowed without duplicate ledger entries. The alignment control snaps inside a forgiving band; its numerical tolerance is a tuning parameter, not visible lore. Pointer drag, two large step buttons, keyboard, and controller all submit the same alignment intent. `Show next step` submits the next valid domain action, including granting the observation with its event-log description; it does not teleport a clamp into the inventory or bypass return.

The reflection animation may finish automatically, but progression is defined by the evidence handoff and its text equivalent. Reduced-motion mode shows clear ordered stills: Ruth reaches under the lip; the catch releases; the cabinet opens. At no point can a present handle be manipulated inside the recording. A first-time player who discovers the hidden catch without consulting the recording may inspect it, but the guided tutorial asks them to establish the recorded procedure before completing this first demonstration; later interactions should not depend on pretending the player is ignorant.

Save/restore fixtures cover every table row, early return, hint at every step, rapid repeated input, muted audio, largest text, and app termination immediately before/after clamp collection. Expected result: exactly one clamp, one observed note, unchanged source trace, and an accessible route forward. The accompanying [P02 example](specs/P02.scene.example.json) describes this contract; it is not an imported Unity scene or executable puzzle.

## 7. Final choice as an explicit commitment

`C7S3` opens only after the shared farewell and all consequence explanations. Its three cards remain available regardless of assistance or local dialogue. Inspection and focus never commit. Every card opens a readable consequence page with **Go back** and a distinct **Confirm this choice** action. E2 explicitly states that Daniel remains beyond safe return; there is no countdown. Confirmation uses a fresh input, not the release of the tap that opened the page.

Save an immutable pre-choice checkpoint. `ConfirmEnding(E1|E2|E3)` validates the current screen revision, sets `endingCommitment`, records a unique commitment operation ID and the chosen branch entry, and durably commits world plus ink together. Only then load `C7S4`. A kill before the commit restores the choice; a kill after it resumes the chosen branch. A write failure remains on the confirmation page. Backgrounding cancels an unconfirmed page rather than accepting it.

Within E3, `return_complete`, `source_erased`, and `machine_disabled` are separate resumable milestones along the already committed branch. Erasure is one domain command: it marks the source unavailable and clears future activation capabilities together. The visual treatment reconstructs from that state; interrupting an effect cannot erase only half the lake. E1 commits loop binding before its demonstration; E2's deterioration advances only with authored narrative beats. No physiological simulation or real-time deadline chooses either branch.

Ending replay starts from the isolated pre-choice copy. Test all three from a fresh authorized final scene, all assistance settings, every confirmation interruption point, and each coda checkpoint. Test the defining negative cases: selecting and backing out, closing the app, a disconnected controller, and slow reading never cause an ending.

## 8. Reflection rendering and device budgets

Use one main scene camera and one temporary reflection camera aimed at a minimal past-stage set, isolated by layers. Render that view to a texture displayed inside an authored water mask; a shallow distortion shader supplies ripples. Unity URP supports cameras targeting render textures. This supports our composition but does not make a second view free. [URP render-texture cameras](https://docs.unity.com/en-us/engine/6000.3/manual/cameras/urp/multiple/rendering-to-a-render-texture)

Load only the props and acting required by the recorded shot. Reuse geometry/materials where possible; do not instantiate an entire second location or recursively reflect water. Disable the reflection camera outside observation. Start with baked light, opaque scenery, minimal transparency, and no real-time shadow in the reflected set. Try a 512-pixel texture for distant ambience and 1024 for the catch close-up; verify finger/hand readability before lowering resolution. Reduced effects remove distortion and camera movement while preserving the identical evidence frames.

These are **prototype hypotheses**, not minimum-device promises:

| Measurement | Initial investigation target |
|---|---|
| Sustained presentation | 30 fps; 95th-percentile frame time ≤33.3 ms after a 20-minute warm run |
| CPU/GPU headroom | Investigate either CPU main-thread work or GPU work consistently above 25 ms; timings are not added together |
| Process memory | Investigate steady use over 450 MiB or transitions over 650 MiB on the proposed floor device |
| Reflection overhead | Compare identical shot on/off; investigate incremental GPU cost above 4 ms |
| Input feedback | Highlight/focus on next rendered frame; no unacknowledged blocking load |
| Resume/transition | Target resume under 3 seconds and scene transition under 2 seconds; profile actual devices |

Record device/OS/GPU, build hash, thermal condition, render scale, frame distribution, peak memory, and visible failures. Test a low Android target and oldest proposed iPhone first. Tighten or replace budgets from evidence before ordering art. If the device fails, cut reflection set detail and texture cost, then visual layers; never remove clue information or lengthen puzzle holds to conceal loading.

## 9. Input, accessibility, sound, and localization

Input actions are `Point`, `Select`, `Navigate`, `Back`, `Advance`, `Pause`, `Adjust`, and `Hint`. Enable one gameplay map and the appropriate UI map; suppress world clicks through overlays. Route uGUI through `InputSystemUIInputModule`, which maps device actions to UI interaction. Test touch cancellation, two simultaneous fingers, controller loss, and focus restoration. [Unity UI input support](https://docs.unity3d.com/Packages/com.unity.inputsystem@1.14/manual/UISupport.html)

Offer tap-select/tap-place and toggle alternatives, explicit focus order, large hit regions, text scaling with scroll rather than clipping, speaker names, transcript, opacity control, independent audio volumes, reduced motion/flashes, and every clue in text. Reflow against safe areas and both wide phones and tablets. Prototype menu/dialogue screen-reader behavior early with platform accessibility support; do not advertise complete nonvisual play until the reflection path has been designed and tested with those players.

Use cue IDs for mixer routing: voice, effects, ambience, and music. Dialogue presentation owns subtitle duration; optional autoplay waits for both the configured reading minimum and voice completion. Manual advance stops/fades the old voice before the next. Looping ambience resumes at an acceptable point; save narrative/music section, not exact audio samples. Audio events are presentation effects, not puzzle truth. Ducking never mutes the visual/text counterpart of a clue.

String tables use stable IDs across locales. Preload the current chapter and common UI; supply translator notes for ages, dry humor, referents, and what the speaker wants. Unity Localization supports shared-key table collections and configurable preloading. [Unity string tables](https://docs.unity3d.com/Packages/com.unity.localization@1.5/manual/StringTables.html) Test expanded pseudolocalization, missing-glyph detection, font licensing, and in-context line breaks before translation orders. Date/number formatting and sentence order belong to the locale; do not bake UI words into art.

## 10. Build pipeline and validation gates

First prove an unsigned development install on each target, then a signed internal mobile build using the team's accounts. iOS export must reach the Xcode/device step; a successful Windows editor run is insufficient. Keep signing identities, provisioning files, passwords, and service credentials outside Git. No automatic store submission in the initial pipeline.

For the solo prototype, run checks and builds locally and record results with the commit: content/schema checks, ink compilation, EditMode domain/save tests, and a lightweight PlayMode scene smoke test. Unity's test framework can run from the command line; verify the exact options against the pinned package. [Unity test runner](https://docs.unity3d.com/Packages/com.unity.test-framework@1.4/manual/reference-command-line.html) Automate cheap document/content checks first if useful. A paid cloud build runner is optional; do not pay for it before local builds work. Once repeatable, the same checks can gate pull requests using an appropriately licensed runner. Run Android builds after accepted integration batches; test iOS export/device builds at each milestone where Mac/iPhone access is available. Missing access remains an explicit unverified platform gate. Retain test results, build hashes, and dependency records. Release uploads remain an explicit developer action.

High-value automated cases: illegal actions rejected; repeat commands idempotent; reflection cannot mutate the present; hint and manual paths reach equivalent facts; save truncation recovers previous state; schema/content migration retains a chosen ending; ink exceptions roll back both candidates; each ending remains reachable; main/replay slots stay isolated. Inject failure after each save step and around ending commits. Physical tests cover process kill, low storage, phone interruptions, thermal load, safe areas, audio route changes, and offline launch. Human tests cover chronology comprehension, Alice's independent life, dialogue performance, and whether the reflected action is legible.

Build the system in this order: export spike → dialogue/input/settings shell → combined saves → P02 with placeholders → reflection treatment → phone interruptions → first ordinary scene → complete prototype. P05's later boat-house comparison reuses this reflection system; it does not justify a second implementation. A successful slice means a stranger can play, stop, return, understand the rule, and care about the people. Only then replicate the content pipeline across seven chapters.

The linked specifications are planning fixtures. Their JSON syntax and schema can be checked now; none demonstrate a working renderer, a valid compiled ink story, a robust mobile save implementation, or a playable game. Primary sources above were checked on **22 September 2026**; package compatibility and store requirements must be rechecked when implementation starts.
