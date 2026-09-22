# What the Water Keeps — gameplay and playtest plan

Version 1.3 · 22 September 2026 · Current interaction specification; unbuilt and untested

The game should make the player want to try an idea, see it work, and discover what that success makes possible. This current specification retains v1.2's six interaction revisions and adds bounded revisions to P03, P08, P09 and P10, integrated in [the game design](02-game-design.md) and screenplay. These are not optional patches to apply again. P04 and P06 remain brief; every quiet scene need not become a harder puzzle. The story facts, 28 shared scene slots, 12 puzzle IDs and three ending meanings remain fixed. The [architecture](06-implementation-architecture.md) still owns state, commands and durable saves.

“Compelling” means voluntary curiosity, satisfying action, attachment and earned surprise. A player should also feel comfortable stopping at a checkpoint. No grind, attendance streak, random reward schedule, withheld ending, completion pressure or real-time threat is added. Nothing in this document establishes that the game is already fun.

## 1. What changes, and why

The strongest current mechanic is knowledge moving between two views of the same place. Its main risk is that the interface or a character explains the solution before the player has a reason to discover it. More buttons would not fix that. The revision gives each substantial action a question, an observable consequence and a reason to reconsider an initially plausible idea.

| Interaction | Risk in earlier draft | Current revision | Visible reward |
| --- | --- | --- | --- |
| P01 radio | Match a part to a symptom that already names the broken part | Test competing explanations for an interruption; change one part and test again | The same movement that broke reception now leaves a complete weather sentence audible |
| P02 catch | Watch an answer, then follow a hotspot instruction | Establish the present obstruction first; infer where an old action fits beneath a changed surface | An inaccessible object becomes reachable through something the player understood |
| P03 sound journey | Match slates and discover the author's one permitted order | Audition transitions and keep any of six three-clip arrangements | Alice's finished piece plays in the player's order; Mara notices its ending |
| P05 winch | Jonah supplies the notch answer; a five-step list follows | Compare contradictory evidence, ask about the replacement, then test the present guide | A misleading old arrow makes sense; working with Jonah seats the receiver |
| P07 playback | Move three controls into prescribed bands | Meet a clear practical constraint while choosing among audibly different, valid mixes | The selected mix, including the mug crash, works for the fundraiser |
| P08 test trace | Follow a laboratory recipe, then pass a terminology quiz | Move the object, replay the event and verify erasure against the surviving object | The player sees exactly what remains and what cannot be recovered |
| P09 itinerary | Allocate a pre-solved budget and follow the only valid route | Pick a real preference between two affordable, workable journeys | Alice prepares her own departure; the selected tradeoff gets a response |
| P10 packing | Sort possessions into ethically obvious answers | Choose how Daniel begins helping, then face the same unagreed commitment | A small cooperative action can coexist with unresolved anger |
| P11 anchors | Repeat the same alignment three times | Use the same invariant rule against three different changes in the scenery | Familiar places become one usable source map |
| P12 contact | Put named things into identically named slots | Diagnose source, identity and return requirements in a chosen order; reuse earlier solutions | Separate environmental layers become a coherent space; an answer occurs that was never recorded |

The evidence behind these decisions is collected in [the research notes](10-gameplay-research.md). Research relating perceived competence and autonomy to enjoyment supports testing understandable challenges and meaningful choices; it does not prescribe these exact puzzles or prove their success. [Ryan, Rigby and Przybylski, 2006](https://selfdeterminationtheory.org/SDT/documents/2006_RyanRigbyPrzybylski_MandE.pdf). Clear immediate goals, plausible solutions and progress through puzzles also follow the practical concerns in [Ron Gilbert's adventure-design essay](https://grumpygamer.com/why_adventure_games_suck/).

## 2. A progression of abilities, not a growing pile of controls

Keep the verbs small: **inspect, compare, try, test, return, commit**. Help must remain available before, during and after an attempt. Inspecting should produce a useful observation or a brief character beat; there is no need to click every decorative object.

| Learning step | Existing interactions | What the player learns | What changes next |
| --- | --- | --- | --- |
| Learn to investigate | P01, P02 | Separate what is observed from what is assumed; knowledge survives Return | The first useful explanation is no longer always correct |
| Transfer the rule | P03, P04, P05 | Sound can be shaped; a common reference matters; changed hardware can make an old instruction misleading | The player contributes judgment, not just memory |
| Remix it socially | P06, P07, P09, P10 | Compare conflicting records, make a valid expressive choice, arrange practical commitments | Correct facts do not settle what people owe each other |
| Learn the final operations | P08 | Distinguish object, stored event and observer; preview replay; understand erasure and return | Final capabilities are comprehensible before stakes rise |
| Master the established rule | P11, P12 | Find invariants across changed views; assemble a source, a verified identity and a live return | Technical success creates an encounter, not control over a person |

This table describes skills, not chapter order: P08 still occurs before P09 and P10. No new interaction is inserted. P03 remains playful creation rather than a disguised test of musical knowledge. P04 lets the children care about the result without requiring Daniel to win. P06 and P10 should remain short when their factual distinction is understood; do not make them longer to imitate a harder puzzle.

Emotional contrast comes from the consequence of play as well as the writing. Repair can feel satisfying; making an announcement can be funny and triumphant; remembering the same places can feel lonely; reaching contact can feel enormous. Quiet is not automatically a design defect. The problem is a scene that gives the player neither an interesting feeling nor a question worth pursuing. Adapting the build/peak/release pattern described in [Valve's pacing presentation](https://steamcdn-a.akamaihd.net/apps/valve/2009/ai_systems_of_l4d_mike_booth.pdf) to this authored story is a design inference, not evidence that a combat pacing model transfers unchanged.

## 3. Detailed interaction specifications

All times below remain the existing **allocations within scene totals**, not measured completion times. Instructions under Hint 1 and Hint 2 are proposed player-facing copy. Show next step follows the existing valid command path. Assistance changes no story meaning, credit, dialogue respect or ending availability.

### P01 — Make it keep playing

**Slot and allocation:** C1S3; approximately four minutes inside its seven-minute scene.

**Goal:** Make Alice's radio keep playing when it is moved. It already makes sound sometimes; “turn it on” is not the problem.

**Information gap:** Is the battery exhausted, the speaker broken, or the connection intermittent? The initial labels describe observations, not the answer. The battery check reports charge. The speaker test produces a short clear fragment. A large **Move the casing** test makes the fragment cut out. A close inspection can reveal a contact lifting as the casing moves; the part's name need not be known beforehand.

**Player action:** Inspect those tests in any order. Select one of Ruth's three safe replacement parts—battery, speaker or contact—then select Test. A substitution is a bounded temporary configuration, not a new inventory system. Only the replacement contact makes the movement test pass. The player may go straight to that explanation if they have understood the inspection; visiting all three tests is not a completion requirement.

**Feedback and plausible wrong ideas:**

- A fresh battery still cuts out on movement: “Charge holds. Moving the case still interrupts it.” This rules out one explanation.
- A replacement speaker reproduces the interruption: “The new speaker makes sound, then loses it at the same movement.” This identifies a shared cause, without shaming the player.
- Replacing the contact makes the same movement harmless. Use the interrupted weather sentence again, now reaching its end. Captions report the changed result at equal clarity with the sound.

Keep each test brisk and freely repeatable. Do not replay Ruth's full dialogue after every attempt. A wrong selection changes the temporary test result, never damages the radio or consumes a part. Ruth's response reacts to what was tested rather than asking the player to click a prescribed part immediately.

**Aha:** Something can have power and a working speaker yet fail when the connection moves. The player repairs a cause rather than purchasing a new object.

**Hint ladder:**

1. “Compare what happens while it sits still with what happens when the case moves.”
2. “The battery and speaker work. The contact lifts when the case moves; replace that piece.”
3. Show next step selects the contact or runs the outstanding test, then follows the ordinary completion path.

**Reward and agency:** Alice tries the movement herself and hears that the repair holds. Preserve the price exchange, Ruth's ordinary work and the radio-name joke. The player chooses their diagnostic route; the repaired radio and relationship beat are shared canon. The familiar test becoming reliable is the victory, with no repair score.

**Implementation bound:** Local part selection, test-result text and solved status fit the existing puzzle `localState`. Reuse the planned symptom/part controls. There is no circuit simulator, waveform analysis or physics-driven contact. Avoid storing a separate copy of “solved” in narrative state. The move test can use two stills and a caption at first.

### P02 — Bring back the method

**Slot and allocation:** C1S4; approximately four minutes inside its six-minute scene.

**Goal:** Retrieve the visible damping clamp from the cabinet. Show its inspection gap and resistant handle before asking the player to align a reflection. This gives the old shop routine a practical purpose.

**Information gap:** The fittings are covered by a later counter repair. Ruth opens the earlier cabinet without pulling harder. What stays in the same place beneath the altered surface?

**Player action:** Inspect the handle, later panel and lower seam in any order. These early inspections may describe the object; they cannot release the catch. Select the existing loading-door anchor, align it and observe Ruth. The evidence handoff records an observation such as: “Her hand goes beneath the lower lip. The catch moves before the door.” It does not add an automatic objective saying exactly which present hotspot to press. Return and apply that observation to the lower edge of the later panel.

The two worlds must be legible without a text quiz. The recording is labelled, Ruth does not answer, and present hotspots are unavailable while observing. Return stays visible even before the clue. Looking at the note or replaying the event is optional once `OBS.SHOP.CATCH` exists; there is no additional knowledge check.

**Feedback and plausible wrong ideas:**

- Pulling the handle gives stable resistance, not a randomly successful force attempt.
- Inspecting the panel fasteners reveals the later covering; they are not removable puzzle inventory. A screw hunt is not a hidden alternative solution.
- Selecting an apparent present object within the recording describes a recorded action or produces the existing mode explanation. It never changes the real object.
- The correct lower edge exposes the catch diagram. Releasing it opens the cabinet; collecting the clamp is the separate committed action already specified.

**Aha:** The appearance changed, but the opening method survived underneath. The player carries an understanding across time; no object crosses with it.

**Hint ladder:**

1. “The handle did not open it for Ruth. Watch where her other hand goes.”
2. “Return to the shop. The old lower lip is beneath the later panel; inspect that edge, then release the catch.”
3. Show next step follows the existing observation, return, panel, catch and collection requirements one valid action at a time.

**Reward and agency:** The drawer opens because the player transferred a method to a changed place. Preserve the dead pen, envelope and ordinary hall amplifier. The player can inspect, pause, return early or review the event without losing progress. This puzzle does not pretend to offer multiple physical solutions.

**Important tutorial limitation:** The existing prototype contract requires the observed fact before the catch can be exposed. A player may infer the answer from childhood or inspect the correct seam first; acknowledge that inspection and explain that this first receiver test establishes the recorded method. Do not imply Daniel cannot see an obvious seam. This is a documented tutorial gate, not a universal rule that correct deductions must await a ledger flag. Once evidence exists, neither ordinary resumption nor replay of the recording reimposes it. A separate chapter replay starts its own tutorial state; its existing Show next step path may deliver the ordered stills/text and fact without requiring a full animation rewatch. If players consistently understand the rule before this gate and find it obstructive, revise the manifest and tutorial together rather than adding more explanation to defend it.

**Implementation bound:** Keep the existing P02 stage graph and all consequential commands. Early descriptions are read-only inspection feedback. `ReleaseCatch` sets cabinet-open state; `CollectClamp` separately grants one clamp and sets aside the envelope. Evidence and grants remain idempotent and durably committed. No ledger-open flag, forced reread, extra puzzle checkpoint or alternate inventory grant is introduced. The [current manifest](specs/P02.scene.example.json) remains the technical example; these changes chiefly affect presentation and clue wording.

### P03 — Make a place out of three sounds

**Slot and allocation:** C2S1, Alice's first independent viewpoint; retain the four-minute interaction allocation inside seven minutes. Target two–three minutes of active creation, allowing the conversation its own room. Do not extend a satisfied player's session to fill the allowance.

**Goal and information gap:** Make Alice's small science-fiction sound journey. The tray, wet glass and paper suggest engine, planet and rain; their order changes what seems to happen. There is no correct story to deduce. The small initial spoon sound and Mara's tray demonstration introduce experiment through ordinary play.

**Actions and feedback:** Record each of the three existing sources once. Its source name, waveform, caption and spoken slate attach automatically; a slate is metadata, not another tile. Arrange one instance of each clip, audition either join or the whole piece, and swap any two with large discrete controls. All six permutations are accepted. Engine → planet → rain suggests arrival; rain → planet → engine suggests departure. These are examples, never labelled targets. Playback omits slates and audibly follows the submitted order; a matching ordered transcript supplies the same changes when muted.

**Payoff and agency:** **Keep this version** commits the current arrangement, plays it once and gives Mara one of three short responses keyed only to its final source. No approval meter, quality rank or preferred permutation appears. Preserve the title **SPACE FILM — NO FILM YET** and the existing replay/save reply afterward. Optional auditions are the player's curiosity, not a required quota.

**Help and cuts:** Hint 1: “Try listening across a join.” Hint 2 demonstrates the swap control without prescribing an order. **Arrange a version** supplies engine → planet → rain, still editable before keeping. Remove slate matching, invalid-order rejection, mandatory rerecording and a separate check that the slates precede effects. If three captures feel repetitive in a paper read, shorten the capture presentation rather than add a fourth source.

**Implementation bound:** Three existing clips, six orderings, three brief textual reactions; no new cast, effects, mixing engine or future-scene callback. Keep the order and completion in P03 local state and use the existing reply flags unchanged. A single clip-order playback helper and ordered transcript suffice; no six separately rendered audio assets.

### P05 — The old arrow is a hypothesis

**Slot and allocation:** C2S4; approximately five minutes inside its seven-minute scene.

**Goal:** Help Jonah seat the receiver in the cradle. The immediate question is how the current guide should face.

**Information gap:** The old reflection supplies an arrow, but Jonah's present replacement plate faces the other way. The fixed structural notch survives both views. The player must distinguish a durable reference from a replaceable marking.

**Player action:** Inspect the present bracket, the plate and the notch; observe the earlier empty bay through the shore-connected reflection; return; choose the present guide orientation. Jonah can be asked about the replacement at any point. His factual reply establishes that he reversed the plate to fit the bracket. “Go by the notch” belongs to Hint 2 or a requested explanation after an attempt, not an automatic answer before the player has compared the evidence.

**Feedback and plausible wrong ideas:** Copying the old painted arrow yields a clear mismatch between guide and fixed notch. The mechanism remains unpowered. Show both references together and label the disagreement; do not say only “wrong.” If the player asks Jonah first and infers the notch immediately, accept the answer without requiring every decorative inspection. The actual earlier-view observation remains the scene's reflection comparison.

Once the guide is correct, retain the fictional brake/load/catch/lower/brake sequence, but present dependency states rather than a five-item list to memorize. The brake shows whether it was checked; the catch shows whether it still bears the load; the cradle shows whether the receiver is seated. Trying to release a loaded catch produces “The catch still carries the weight.” Trying to lower before release shows the engaged catch. Jonah keeps the safety line secured. Unsafe inputs stop before motion and preserve completed steps.

This operation should be a brief, satisfying completion of the deduction. If the sequence takes more attention than the comparison, shorten its pauses and combine explanatory lines with feedback. Do not invent extra failures, damage, hand coordination or a physics problem to extend it.

**Aha:** An accurate picture of the past is not necessarily a valid instruction for changed equipment. Jonah knows the present; the reflection knows the previous arrangement. Both matter.

**Hint ladder:**

1. “Compare something that stayed fixed when the plate was replaced.”
2. “Jonah reversed the replacement plate. Match the present guide to the structural notch, not the old painted arrow.” After alignment, a requested hint explains the next unmet load dependency.
3. Show next step makes the next valid alignment or abstract safety action through the ordinary reducer.

**Reward and agency:** The receiver seats; the strained sound settles; Jonah verifies the brake. Allow that small competence beat before the sandwich and his departure boundary. Choosing to ask, inspect or test changes how the player reaches understanding; it does not turn Jonah into a reward dispenser or require six separately written conversation paths.

**Implementation bound:** Reuse the reflection, present hotspots, two guide orientations and a short finite sequence. No procedural machinery, extra environment, accident branch or real equipment tutorial. Description/test flags live in P05's local state; a completed mechanical step does not replay after resumption.

### P07 — Make a version you would keep

**Slot and allocation:** C3S3; approximately four minutes inside its seven-minute scene.

**Goal:** Let people understand the fundraiser announcement while keeping both the water and workshop-tap accompaniment. The accidental mug crash stays in every accepted take because Alice chooses to keep it.

**Information gap:** More sound is not automatically a better announcement. Which layer masks the words, and how much of the place's character can remain when those words are clear?

**Player action:** Use the existing three stepped controls; preview freely. Prototype voice steps are **Quiet / Clear / Carrying**, and the two accompaniment controls are **Off / Soft / Present**. These are adjustable mix settings, not displayed points. Captions describe the same change heard in playback. Submit when satisfied; the scene accepts a family of readable mixes, including a water-forward version, a rhythm-forward version and a restrained balance.

For a bounded first content implementation, the 27 possible settings can use an authored acceptance table. An initial testable rule is: both supporting layers must be at least Soft, voice must be Clear or Carrying, and Clear voice with both supports Present remains masked. This supplies seven accepted settings. It is a tuning hypothesis, not an acoustics claim; the actual mixed clips and caption labels must agree before accepting the table. If the audible result contradicts a label, fix the mix or table. Never tell a player an intelligible recording is unclear merely to manufacture a puzzle.

**Feedback and plausible wrong ideas:**

- Turning everything up may pass when the voice carries; it does not earn a higher rating. Let the player choose that sound if it is actually clear.
- Raising both backgrounds above a Clear voice masks the practical information. Caption the obscured phrase and let Mara's concise line report the problem.
- Muting both backgrounds makes the words intelligible but loses the requested accompaniment. Alice asks for some water and taps back, without resetting the work.
- A water-forward and a rhythm-forward accepted setting receive equally respectful responses. No character reveals a hidden artistically correct answer after submission.

**Aha:** There can be several good versions. The player can make something recognizably theirs while fulfilling a real purpose.

**Hint ladder:**

1. “Preview the announcement. Which layer covers the words about the fundraiser?”
2. “Keep some water and taps, but lower the covering layer or give the voice more room.”
3. Readable mix supplies one valid balanced setting. It does not label that preset the best, and the player may adjust it before submitting.

**Reward and agency:** The submitted mix is what the player hears during the successful announcement. The crash draws attention; people hear what the fundraiser needs and the ordinary work continues. Alice keeps the take. One bounded response can acknowledge which accompaniment is more prominent; both rejoin before the shared dialogue. Do not make donations depend on the mix or add a crowd simulation, money meter, timing challenge or hidden popularity score.

**Implementation bound:** Reuse the three planned volume controls and clips. Store the selected steps in P07 local state; captions and acceptance read those same steps. A small lookup table is sufficient. No waveform editor, custom audio-analysis system, procedural music, extra voice cast or seven separately recorded announcements. Muted play exposes every criterion and accepted variant through text; it cannot reproduce the pleasure of listening, which remains an accessibility limitation to assess with players.

### P08 — Test what the machine can change

**Slot and allocation:** C4S1; approximately five minutes inside eight. The scene must establish the final operations through visible differences, while leaving room for the troubling sensation test.

**Goal and information gap:** Does a control affect the present washer, its recorded tap, or Daniel's awareness? Begin with one washer tap, an observation and Return. The only selected event is that tap's marked interval at the shallow source. It is not a person and cannot contain a bound human consciousness.

**Actions and feedback:** Offer two probes in either order: **Move washer to bench** and **Run bounded repeat**. Moving the real washer leaves the recorded tap at its old location; the next observation retains that location. Bounded repeat shows the finite tap restarting twice while the physical washer stays still. If repeat comes first, moving the washer afterward makes the same contrast more obvious; if moving comes first, both repeat cycles occur at a visibly vacant source. Keep the present object visible in a small comparison view with an equivalent text description. Present the discrepancy before Daniel explains it. These two probes replace interval-card placement and the label quiz, rather than extend that sequence.

The supervised sensation test then occurs once: Jonah taps Daniel's wrist; Daniel cannot initially feel it; Jonah operates Return and sensation resumes. No player reaction time, refusal or failure governs this demonstration. The existing safety note follows. This distinction concerns the observer and must not suggest the washer tests activated a person.

**Erasure and payoff:** Preview **Erase this recorded tap permanently. The washer and other records remain.** The existing carrier-fold operation addresses the already selected tap without another alignment exercise. After confirmation, the player chooses **Try the same trace**. The view/index stays empty and its caption states that no archived tap remains; the washer is plainly on the bench. This quiet absence is the successful result, not a broken button. Do not produce a new tap as a victory flourish or offer an undo. Canon still completes this expendable erasure.

**Help and cuts:** Hint 1: “Compare where the washer is now with where the tap plays.” Hint 2: “The recording keeps the earlier event. Moving the washer does not move that event.” Show next step completes the next probe through the ordinary path. Remove terminology matching, hand-placing already marked endpoints, repeated alignment and a recap quiz. Existing labels, captions and the later safety note remain available for review.

**Implementation bound:** Washer in two existing positions, one selected trace, one bounded replay and the current erase/return presentation; no additional source or physics simulation. Probe order and completion belong to P08 local state. Preserve the existing `observedReturn`, `previewedReplay`, `erasedTestTrace` and `restoredSensation` flags. Save erasure before its empty result, and reconstruct that result after interruption. No new ending gate.

### P09 — Choose a workable first evening

**Slot and allocation:** C4S2, Alice's second and last independent viewpoint. Keep the four-minute combined interaction/dialogue allowance inside six minutes; route planning itself should take approximately sixty–ninety seconds.

**Goal and information gap:** Alice wants the seven-week job beginning nine days after acceptance. She is choosing how to get there, not whether she is allowed to leave. Two displayed routes depart on the evening before the first call and satisfy the same lodging check-in requirement:

| Route | Useful advantage | Genuine cost | Required fixture condition |
| --- | --- | --- | --- |
| Cheaper connecting bus | More money remains after travel and initial lodging | One transfer and a smaller arrival margin | Positive check-in buffer and positive remaining budget |
| Dearer direct bus | No transfer and a larger arrival margin | Less money remains | Positive check-in buffer and positive remaining budget |

**Action and feedback:** Show travel, lodging, remaining money and check-in margin in the same large-print summary. Selecting either card updates that summary and a short exchange with Mara immediately; change it freely before continuing. The timetable-column misunderstanding occurs before selection, so its private exchange remains on both routes. Neither selection creates a missed bus, late arrival or later penalty. The exact numeric fixture must demonstrate the inequalities above when runtime content is authored; this plan does not invent economic precision to make the choice look harder.

**Payoff, help and cuts:** Keep the existing excitement/nerves reply, then automatic acceptance and its readable confirmation. Help names the tradeoff; **Arrange itinerary** selects the cheaper viable card. Remove mental arithmetic, money-allocation tiles, the wrong-route failure state, mandatory card order and a separate acceptance challenge. No timer. Store only the route in P09 local state; preserve all current disclosure flags and Alice's later delay in telling Daniel.

### P10 — Help without deciding for her

**Slot and allocation:** C4S3; retain four minutes including the concurrent argument, inside six. This is a short scene with actions, not a four-minute ownership exam.

**Goal and information gap:** Help Alice pack while Daniel has not yet faced what he put her name on. The player knows she is leaving; the unexamined detail is the three hall bookings he made for both of them. Her name in his handwriting makes that assumption concrete.

**Action and immediate agency:** Choose one first approach. **Hold the equipment bag** produces a small accepted practical gesture while Alice continues packing; **Look at the hall bookings** makes her put the equipment down and face him. Each has two brief opening lines before the required booking conversation. These are alternative entrances, not two mandatory checklist items. There is no “good partner” score. The first approach is local; the existing `c4s3_help` / `c4s3_ask` reply remains the separate saved response.

**Feedback and payoff:** Reading the booking exposes the handwriting before Daniel's explanation. Once their lack of agreement is stated, the page gains **needs agreement** automatically. It does not approve, cancel or renegotiate the bookings; Daniel must call. Ownership is already correct, and the shared kettle waits without a classification challenge. After the existing reply, one **Pack agreed equipment** action finishes the physical task. They have managed a little cooperation; the argument and her delayed disclosure have not disappeared.

**Help, cuts and bounds:** Hint 1 points to the available bag and booking. Hint 2 says either can start the scene. **Continue packing** takes one normal route and leaves the existing reply available. Remove the three-bin sorting board, deliberately false ownership options, repeated inspection requirements and any requirement to choose an apology before proceeding. Use existing equipment, page, tape, kettle and held poses. No additional inventory, commitment simulator, shared lease or ending condition. Store only first approach/completion in P10 local state and retain existing response names.

### P11 — Recognize the places under their changes

**Slot and allocation:** C5S4; approximately six minutes inside its eight-minute scene.

**Goal:** Connect three source positions so the last morning can be found. The three required stations and their status are visible from the start; this is not a hunt for an unmarked fourth collectible.

**Information gap:** Each present view has changed in a different way. Which reference in Ruth's survey still identifies the same position and orientation?

**Player action:** Visit stations in any order, inspect the present landmark and its archived view, and confirm the reference/orientation on the existing discrete alignment control. Each successful sector saves independently. No repeated walk back to the apparatus is required between them.

| Station | Tempting but unreliable reference | Observation that resolves it | Distinct player action |
| --- | --- | --- | --- |
| Dock / triangle | Edge of the replacement plank | The old and new board surround the same unmoved bolt | Anchor the overlay on the bolt before choosing the aligned orientation |
| Tree / square | A distance mark mistaken for the measuring origin | The metal tape marker and notch identify the shared origin seen during P04 | Read the survey's origin against the current marker; turn the sector from that origin |
| Rise / circle | Visible grass edge or exposed outer edge of the footing | Moving the present grass exposes the existing iron footing's full reference | Compare the revealed footing with the archived outline and orient it |

All required information is supplied again locally. Remembering the childhood game may make recognition warmer and quicker, but forgetting an earlier line is not a penalty. Do not hide the bolt under a tiny hit target or require visual rotation without the existing text/auto-align equivalents.

**Feedback and plausible wrong ideas:** The mismatched landmark is named: “The board edge moved; the bolt did not,” “That mark measures a distance; the origin is beside it,” or “The grass is covering the fixed edge.” These are responses to a relevant attempt or requested help, not instructions automatically read before the first decision. An unsuccessful orientation leaves the evidence visible and other sectors solved. Do not erase traces or reset all three to create stakes.

**Aha:** The player already knows these places as lived spaces. The same places now make an apparatus possible, without their sentimental meaning being the matching criterion. The connected diagram is a practical discovery, not a revelation that emotions power the lake.

**Hint ladder:**

1. “Find the fixed reference at this station; ignore what could have been replaced, measured from it or grown over it.”
2. Name that station's reference and the needed orientation using its text diagram.
3. Auto-align completes only the selected sector through its ordinary state path. Previously solved sectors remain unchanged.

**Reward and agency:** The player chooses the order, understands three distinct changes and closes the source diagram. It indexes Alice's verified morning visit. Keep this success quiet; the large sensory expansion belongs to P12. Do not show the later empty-place farewell, insert ghost figures or play remembered voices as rewards.

**Implementation bound:** Three existing locations/overlays, the existing survey and three saved sector states. The grass move is a bounded present inspection state; there is no foliage physics. Use the same aligner with different authored reference data rather than three minigame controllers. A selected stable point and snapped orientation can be local puzzle values. No map traversal simulation or new landmark is required.

### P12 — Build contact with a way back

**Slot and allocation:** C6S3; approximately five minutes inside its eight-minute scene.

**Goal:** Establish contact with the latest stored Alice while keeping Daniel's live return available. Do not frame the objective as restoring a body or changing the last lunch.

**Information gap:** A view of one place is not the complete source; an earlier impression is not the verified last-morning state; an image of a work light is not Daniel's live return reference. The player must recognize the role of what was learned, not remember an arbitrary cipher.

**Player action:** Inspect the three channels in any order. Their candidate configurations and evidence are always available. Use the saved connected map from P11, the morning anchor identified in C6S1 and the return carrier learned in P08 and checked against the present work light. Test a proposed configuration while it is unpowered. Each ready channel stays ready. Symbols from earlier puzzles orient the interface; there is no extra memorized symbol-sequence test.

The completed P11 map is reused as one solved object. Showing its three established layers is a presentation payoff, not a requirement to solve the dock, tree and rise rotations again.

**Feedback and plausible wrong ideas:**

- A single dock fragment produces “One recorded view selected. The connected source is not loaded.” It cannot power contact.
- An older summer anchor produces “Earlier than the verified morning visit.” This explains a mismatch with the chosen goal; it does not invent a rule that earlier records could never be activated.
- A recorded light rather than the live return reference produces “Recorded reference selected. Live return is not verified.” P08's local summary explains why that matters.

These are authored setup alternatives, not unsafe live experiments. No responsive Alice is activated and dismissed while the player tries configurations. The source remains read-only. Failed configurations cost no time, health, trace, relationship or ending access.

**Aha:** Every part was encountered for another understandable reason. Together they let Daniel reach someone while retaining a way back; success does not give him ownership of what she will say.

**Hint ladder:**

1. “Check the role that is still missing: connected place, verified morning, or live return.”
2. Name its established evidence: P11's complete map, C6S1's morning anchor, or P08's carrier with the present work light. Use player-facing descriptions rather than puzzle IDs in the game.
3. Complete calibration supplies the remaining correct configurations through the same committed checks. It leaves the final contact action for the player to select.

**Reward and agency:** The player chooses the diagnostic order; the shared readiness labels are **Contact ready / Return available / No history alteration**. Each successful check develops an existing environmental layer and its matching textual status. The already established source geometry can look vast through composition, depth and sound. No larger world or new simulation is required. The final release begins contact; the score stops at Alice's breath. Her first new response is the change in kind. It is not a password reward.

**Implementation bound:** Three channel selections/statuses and one final activation boundary in P12 local state. Reuse the observation presentation, selectable diagrams, conditional text and normal command/commit path. The chosen inspection order requires no unique ending or six complete dialogue variants. Return remains available, danger has no real-time clock, and replay/erasure are reviewed but never executed by calibration. Store readiness and the contact transition consistently so reopening the app neither repeats an activation nor skips its first line.

## 4. Local agency that remains visible

An authored outcome does not make every input meaningless. The input must affect something the player can notice before the scene ends. Do not describe choices as changing history when they change approach, configuration or expression.

| Choice | Observable difference | Stored scope | Reconvergence |
| --- | --- | --- | --- |
| P01 test/part order | Different informative test results; route to the same repair | Local selection and current result | Successful movement test |
| P02 inspect/observe/return/review order | Player controls how they find and apply the recorded action | Existing evidence and stage | Clamp collection |
| P03 clip order | The completed piece follows that order; its final sound gets a specific response | Three-clip local permutation | Keeping the titled recording |
| P05 ask Jonah, compare, or test first | Different route to explaining the reversed plate | Bounded inspection/attempt state | Correct guide and seated receiver |
| P07 selected valid mix | Its sound, captions and one concise response | Three local control values | Shared announcement/fundraiser success |
| P08 probe order | The object/trace discrepancy appears through the chosen first test | Two local probe states; existing four canon flags | Verified erasure and restored awareness |
| P09 viable route | Arrival margin, remaining money and Mara's immediate exchange | One local route selection | Automatic acceptance after the existing reply |
| P10 first approach | Cooperation or the unagreed booking starts the exchange; the characters' posture follows | One local approach; existing reply flags kept separately | Shared argument and agreed packing |
| P11 station order | Discovery and completed sectors remain in the chosen order | Three independent sector states | Connected source map |
| P12 diagnostic order | The player resolves missing requirements in their chosen order | Three channel statuses | Final release into shared encounter |

Later scenes need not check a cross-product of these choices. P07's playback uses its stored mix when that take is presented within its scene. Existing apology, disclosure and packing callbacks remain separately bounded. A future callback is added only with a named line and owner; “remember every decision” is not a requirement.

Wrong hypotheses should be meaningful enough to test and cheap enough to abandon. Do not add arbitrary decoys solely to increase click count. A person who infers the correct answer immediately has played successfully. A person who chooses assistance has also played successfully.

## 5. The opening proof and its questions

The current C1S1–C1S4 allocation is still **3 + 5 + 7 + 6 = 21 minutes**, with puzzle time already included. An engaging **roughly 15–20-minute** first-play proof is an editorial hypothesis to investigate, not a retcon of that allocation or a deadline for a reader. Fast comprehension can make the proof shorter; assistance, rereading and a different reading pace can make it longer. Do not speed up lines or add padding to force the band.

| Scene | Question that sustains attention | What the player does | What should carry into the next scene |
| --- | --- | --- | --- |
| C1S1 | Why is the receiver still repeating a sound I stopped? | Starts the bell test, stops its ordinary playback, and sees/hears the trace continue; optional unit/water inspections, then Return | A demonstrated anomaly and Daniel's “Sound holds. Picture won't hold” reply to Jonah give a concrete reason to find the clamp |
| C1S2 | Why is Alice crying, and how do these two actually get along? | Chooses an awkward opening and disturbs the reflection | Curiosity plus the possibility of an ordinary friendship |
| C1S3 | What makes the radio stop, and can I fix it? | Tests and repairs it while people work | Competence, warmth, a familiar shop and Ruth's casual catch movement |
| C1S4 | Can the old routine help with something real now? | Observes, returns and opens the present cabinet | A learned rule and the desire to see what else that rule can reveal |

Do not bring forward Alice's death announcement merely to make the proof appear more dramatic. Do not add a combat tutorial, chase or cliff-hanger that promises a different game. The next scene already gives Alice independent creative work. A participant may choose to stop at C1S4; that is a legitimate end to the test, not a retention failure.

A first impression should reach a meaningful interaction promptly, but the opening proof is not a speed test. Record the time to the first player-initiated test and ask whether the preceding material gave them a reason to care. If an opening speech explains what an action can show, try removing the speech first.

## 6. Low-cash prototype and comparative tests

### Before building more systems

Paper or static-screen prototypes can test P01's causal explanation, P02's changed surface, P05's misleading arrow and P11's three references. Show only information the game would show at that point. A facilitator reveals the next card in response to the player's chosen action; they do not translate “I would look under the panel” into the answer before the player says it. Accept a clearly intended equivalent to a button label. This cannot test touch feel, animation readability, sound quality or save behavior.

The value of a low-cost clue/comprehension prototype is supported by the developers' account of a paper-to-text prototype for another discovery game; its results do not establish ours. [Mobius Digital: Demaking Outer Wilds](https://www.mobiusdigitalgames.com/news/demaking-outer-wilds).

Do one focused comparison if it resolves a real uncertainty. Choose fresh participants for each version of the **same** puzzle; solving version A teaches version B's answer. Keep text size, facts, art quality and available assists comparable. Three to five people per version can expose recurring confusion but cannot establish statistical superiority. Counterbalance assignment where practical, record experience differences, and report individual observations rather than a percentage that implies certainty.

| Comparison | Keep constant | Compare | Decision it can support |
| --- | --- | --- | --- |
| P01 explicit diagnosis versus test-first clues | Same fault, parts and success scene | Whether a player predicts a cause before selecting; whether tests change a mistaken explanation | How much causal information belongs in the opening label |
| P02 old instruction sequence versus present-obstruction-first sequence | Same stage graph, evidence and correct seam | Whether players explain why they returned; repeated wrong mode actions; perceived busywork | Whether clue order produces transferable understanding |
| P05 automatic notch answer versus answer in requested Hint 2 | Same visible notch and replacement information | Whether the reversed plate is inferable; whether Jonah seems helpful or obstructive | Whether dialogue is explaining too early or withholding too much |
| P07 one supplied valid mix versus several valid mixes | Same clips and clarity rule | Whether players notice and value their chosen result; whether they can distinguish accepted sounds | Whether the expressive work justifies its added content tuning |

These are a menu of small experiments, not a requirement to run every variant. Start with P02 because it is the game's central promise. Do not conduct a comparison when both versions would answer an already settled question. Paper trials can compare comprehension; the P07 sound judgment requires an actual audible mockup or build, and muted testing checks its parallel text path separately.

### First complete device proof

Keep IMP-001–IMP-016 in their existing order. IMP-008 incorporates P02 clue presentation; IMP-009 incorporates P01 test feedback; IMP-011 handles the revised scene beats; IMP-016 observes the whole opening. This revision does not create an implementation start, install tools or claim a playable build.

The existing first round is **five observed opening plays**. Include people with different puzzle familiarity and at least a muted/enlarged-text pass. Describe the task as “play as you normally would; you may stop or use help.” Avoid coaching during an attempt. Invite a brief explanation after a puzzle so thinking aloud does not become a mandatory parallel task that changes every participant's rhythm.

Ask concrete questions:

- “What were you trying to do when you chose that?”
- “What changed your explanation?”
- “What can this reflection do, and what can it not do?”
- “Where did you know the answer but still have to wait or click?”
- “What do you remember about Alice or Ruth besides their connection to Daniel?”
- “Which moment would you keep? Which would you shorten? What made you curious about the next scene?”

Do not ask “Wasn't that surprising?” or tell players which emotion they were expected to feel. Record the participant's answer before the designer's interpretation. If they call a quiet scene boring, locate the specific absence: no question, repeated information, unclear goal, waiting, or simply a scene they dislike. Sadness, concentration and silence alone are not measures of boredom.

### Small observation record

Use a local developer note or consented recording, not a backend. One row per meaningful event is enough: anonymous session label, build/content revision, scene/puzzle, elapsed time excluding interruptions, intended action in the player's words, observed action/result, hint level requested and a short quote. A few local debug events may supplement the observer: puzzle entered, attempt result, evidence acquired, Return, assistance requested, solved and resumed. Do not ship an analytics SDK or collect account IDs, microphone data or device fingerprints for this proof.

Record completion time alongside how it was spent: reading, reasoning, voluntary replay, unclear controls and system wait. A long thoughtful solve and a long unresponsive animation require different changes. Raw tap counts and minutes played are not success metrics.

### Targeted v1.3 checks when these scenes reach their milestone

These checks are prepared, not performed. They do not enlarge the opening proof or establish full-game enjoyment.

| Interaction | Concrete observation to collect | Change if the observation fails |
| --- | --- | --- |
| P03 | Have a participant keep any order, then ask what changed when they swapped two sounds; check all six orders mechanically when authored | If order barely changes the perceived piece, improve the joins/captions; if capture feels repetitive, shorten it before adding sounds |
| P08 | Run each probe order; after erasure ask what still exists and what could be recovered, without offering a multiple-choice vocabulary test | If “moving/erasing the real washer” persists, strengthen the simultaneous present/source comparison; do not add more labels to memorize |
| P09 | Ask which route they chose and what they gave up; verify both numeric itinerary fixtures actually cover lodging and check-in | If one is seen as the only sensible choice, adjust the margin/money tradeoff or retain a single short narrative action rather than pretend there is agency |
| P10 | Read both first approaches; ask what Daniel changed and what remains unresolved | If this is read as a quiz that earns forgiveness, remove the judgmental feedback; if two entrances add no felt difference, keep one and shorten |

P04 needs no extra difficulty, and P06's handwriting correction must not become a toll before Mara can recover her own property. If either clear distinction takes only one meaningful action, accept the shorter beat. Keep the current 151–153-minute whole-game allocation visibly unmeasured; removing clicks is not permission to replace them with held shots.

## 7. Decision gates and when to stop

These are **provisional editorial gates**, not population estimates. With five plays, report “four of five in this round,” not “80% of players will understand.” Assistance use is never itself a failure; look at whether the player wanted more control than the design allowed.

| Observation | Action |
| --- | --- |
| Fewer than four of five can explain that the recording reveals information but cannot move the present object | Pause chapter expansion; repair P02's causal presentation and mode feedback |
| Two or more independently know the answer yet describe the same forced step as busywork | Remove or shorten that step; if it is the P02 tutorial gate, revise the contract explicitly before changing implementation |
| Two or more who want to solve by inference resort to repeated undirected selections and cannot explain the result | Improve evidence and specific feedback before adding difficulty or more decoys |
| Players can explain a solve but say the result has no satisfying consequence | Change its immediate payoff or shorten the interaction; more explanation is unlikely to help |
| P01/P02 produce clear understanding and at least one self-identified satisfying action for most participants | Continue the existing representative-slice decision; do not keep testing solely to improve a number |
| Alice is described only as a mystery, a prize or the future dead girlfriend | Strengthen her ordinary objective and behavior in existing scenes; do not add a lore monologue |
| Muted or enlarged-text play hides a required observation or action | Repair that presentation before treating the interaction as ready |
| Save resumption duplicates the clamp, loses a solved step or puts an action in the wrong mode | Fix correctness first; an apparently exciting puzzle cannot pass with broken progression |

For the qualitative “most participants” gate, name the actual reported moments and any contrary accounts; do not convert it into an enjoyment score. A single severe accessibility or state-loss failure does not need to occur twice to matter.

After one bounded revision, test again **only to answer the remaining failure**. A second five-person round and a separate comparative experiment are additional scheduled work, not silently free inside IMP-016's current six-to-ten-hour estimate. Record recruitment, session, revision and analysis hours, then re-estimate. Stop an individual puzzle trial if the participant requests help or wants to end it; give assistance or end without making them perform frustration for the researcher.

Stop expanding scope if two focused revisions still leave the same puzzle dependent on facilitator explanation. Reduce its number of candidate interpretations or turn its low-value tail into a direct action. Do not introduce a new subsystem to rescue one weak interaction. Once the remaining uncertainty is art or performance, move to the existing five-to-eight-minute representative subsection; another paper puzzle session will not answer it.

The full-game emotional progression, P05/P07/P11/P12 play quality, 151–153-minute allocation and all ending experiences remain untested by a successful opening. Their later gates belong to the existing chapter integration and ending milestones. The opening proves a small promise, not the entire commercial game.

## 8. Scope and handoff delta

- **Unchanged:** seven chapters, 28 shared slots, 12 puzzle IDs, exactly two Alice-perspective scenes, all three endings and the final sentence. Death has no preventable puzzle solution. The recorded source stays read-only; dormant records are not continuously conscious. Contact begins only after P12 readiness and final activation.
- **Retained v1.2 content:** raw observations and test feedback in P01; clue order and non-solving observation text in P02; when P05's solution is spoken; multiple accepted P07 mixes; distinct P11 reference comparisons; P12 diagnostics and reuse of the completed map instead of repeated alignment work.
- **Changed in v1.3:** C1S1 gives the player the Stop playback action that reveals the anomaly and Jonah's concrete clamp goal; P03 accepts all six clip orders; P08 contrasts the moved object with its fixed past event; P09 offers two viable practical preferences; P10 begins with one of two physical approaches to the same argument. P04/P06 stay concise. All four revisions are integrated into their corresponding screenplay passages.
- **Deleted friction:** P03 slate-matching and wrong art orders; P08 terminology matching, endpoint placement and repeated alignment; P09 money tiles and single-route recipe; P10 moral sorting and forced inspection of both first approaches. Do not quietly preserve these obsolete steps in implementation.
- **No new general system:** all additions use existing stepped controls, local puzzle state, hotspots, conditional text, selected recorded views and the normal command/commit path. P03's three clips play in the saved order rather than requiring six new audio assets. The P07 acceptance table, the two itinerary fixtures and extra feedback lines are content work and still take time to author, caption and verify.
- **P02 contract:** no stage, command, evidence ID or grant change is required for this revision. Preserve the current manifest's evidence gate and separate `ReleaseCatch`/`CollectClamp` transactions. If a later test justifies removing that tutorial gate, update the game design, architecture, manifest, fixtures and save/content revision together; do not silently weaken a guard in a presenter.
- **Estimate status:** existing opening estimates are not revalidated by this document. Measure the revised P01 content and P02 staging during IMP-009/011. The later interactions, including v1.3's four revisions, belong to their existing chapter integration tickets and receive estimates after the opening proof. Removed UI tasks may save effort, but that saving is not measured. No free implementation time is assumed.

Before implementation, a short paper trial of P02 and a table read of the revised opening can reveal cheap-to-fix problems. Then build only the already planned opening proof. Every revision should earn its place through a clearer action, a more satisfying consequence or a stronger scene.
