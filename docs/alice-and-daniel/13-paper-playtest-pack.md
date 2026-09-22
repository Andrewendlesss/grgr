# P02 paper playtest and scene table-read pack

Version 1.3 · Prepared materials; no participant sessions performed

This pack tests one question: **does carrying an observed method back to a changed place feel like the player's discovery?** It implements the current [P02 specification](12-gameplay-and-playtest-plan.md#p02--bring-back-the-method) and [manifest](specs/P02.scene.example.json). It changes no guards, commands or grants. Card wording is prototype presentation copy, not an additional canonical screenplay.

## 1. Facilitator preparation — keep this section private

Use the current present-obstruction-first sequence with five fresh participants, if available. Establish whether it communicates its rule and whether the evidence gate obstructs people who already understand. Resolve that before recruiting for a comparison of clue order. This is the focused alternative to document 12’s optional comparison; recruitment has not occurred.

Prepare cards P00–P11 below as separate sheets or individual phone screens. **Do not hand over this whole document:** Markdown headings do not conceal later cards or the answer key. Keep a separate facilitator copy and blank record. Show only the current card; previously acquired observations may be requested again. Present normal-sized or enlarged text as the participant prefers. This text-only version represents the muted path.

Read P00 verbatim, then P01. Do not explain what the reflection teaches. Accept equivalent language: “look underneath that new covering” means an inspection, without requiring a button name. Ask “Which part?” if intent is genuinely ambiguous. Never interpret “try something” as the successful action. Read feedback neutrally, without pointing, praising proximity to the answer or demanding continuous thinking aloud. Requested assistance is ordinary play.

Record voluntary reasons and confusion; ask about understanding afterward. Track time to locate reading, reasoning and waiting; impose no deadline. If stuck, say once: “You can keep trying, ask for help, or stop.” A help request receives help immediately. A stop request ends the trial.

Paper cannot establish touch accuracy, animation, sound, payoff excitement, save correctness or full-game appeal. Alignment is a text stand-in. Record card-handling time separately.

## 2. Participant cards — reveal individually

### P00 — Before we start

> You are Daniel, returning to a shoreline repair shop. You need the cabinet’s damping clamp for your equipment.
>
> Tell me what you would inspect or try. I will show the result. You may revisit information, ask for a hint, ask me to show the next step, or stop whenever you like. There is no score or time limit. You do not have to explain every thought.

### P01 — Present: the cabinet

> Night. The shop's loading doors face the lake. Through the cabinet's narrow inspection gap, you can see the clamp. It will not fit through the gap.
>
> There is a handle, a newer panel covering part of the old counter, and a seam along the panel's lower edge.
>
> Your receiver can align an earlier view of the loading doors in the lake's reflection.
>
> Inspect or try something here. Or use the receiver at the loading doors. Help is available.

### P02 — Present: handle

> The handle moves slightly, then stops against firm resistance. Pulling harder produces the same result. The clamp remains inside.
>
> What would you try next? You can inspect the cabinet or use the receiver.

### P03 — Present: later panel

> The panel's paint and fixings are newer than the counter around it. It covers the older fittings. A narrow seam remains beneath its lower edge. The fasteners do not offer a removable part here.
>
> What would you try next? You can inspect further or use the receiver.

### P04 — Receiver: alignment

> In the water: an earlier summer view of the shop's loading doors. Against it: the present doorframe.
>
> Align the two doorframes, then Observe. You may ask for assisted alignment. Return is available now.

### P05 — Recorded event: routine begins

> RECORDED EVENT — CANNOT INTERACT
>
> Ruth crosses behind the earlier counter. She tries the handle; it resists. The newer covering panel is absent.
>
> Return and Help remain available.

### P06 — Recorded event: observation

> RECORDED EVENT — CANNOT INTERACT
>
> Ruth's hand goes beneath the lower lip. The catch moves before the drawer opens. She continues her closing routine.
>
> Observation kept: “Her hand goes beneath the lower lip. The catch moves before the door.”
>
> Return and Help remain available.

### P07 — Return: present cabinet

> Night again. The newer panel covers the older fittings. The cabinet is still closed; the clamp is still inside.
>
> Your observation remains available. You may inspect or act here, review the observation, or replay the recorded event.

### P08 — Present: beneath the panel

> Beneath the newer panel's lower edge, you can reach the old catch. It holds the drawer shut.
>
> Release catch. Help is available.

### P09 — Present: cabinet open

> The catch releases. The drawer slides open.
>
> DANIEL: I moved this thing twice.
>
> Inside: the damping clamp, a dead pen, and an envelope labeled RETURN TO CUSTOMER.
>
> You can take the clamp or inspect what is here.

### P10 — Collected: checkpoint

> Daniel takes the clamp and sets the customer's envelope on the counter. A repaired hall amplifier nearby has a completed service tag and a number waiting for a reply.
>
> The cabinet sticks as he closes it. He leaves it slightly open.
>
> The clamp is collected. This is the end of this short trial. You can stop here.

### P11 — Early inspection acknowledgement

> You have found the lower seam. This first receiver test requires observing the recorded opening method before trying the catch here. Your inspection was valid; there is nothing else to search for at this edge yet.
>
> You can use the receiver or ask to show the next step.

**End of participant card bank. Do not display the following sections during play.**

## 3. Facilitator-only answer key and response mapping

Start at `shore_ready`, with no evidence and no clamp. The solution is to observe Ruth, Return, inspect the present panel lip, release the catch, then collect the clamp. Knowledge crosses between views; objects do not. Observation is required even after a correct guess. Do not conceal or waive this limitation.

Maintain one state, one evidence mark and one item mark. Inspections and note review outside the transition table are read-only feedback. They must not invent a checkpoint or grant.

| State / requested action | Exact response or card | Consequence |
| --- | --- | --- |
| `shore_ready`: inspect cabinet / handle / panel | P01 / P02 / P03 | No transition; order is free |
| `shore_ready`: inspect lower seam or correctly propose the catch | P11; log first-try inference and response to the gate | No transition; no evidence granted |
| `shore_ready`: take clamp through gap | “It is too large for the gap. The drawer must open.” | No transition |
| Present closed cabinet: remove screws | “The panel is a later repair. Its fasteners are not removable controls in this prototype.” | No transition; record whether this feels arbitrary |
| `shore_ready`: select loading-door anchor | P04 | `SelectAnchor` → `aligning`, CP01 |
| `aligning`: align and Observe | Accept an explicit alignment intention, or assisted alignment; P05 | `Observe` → `observing`, CP02 |
| `aligning`: Return | “You are back at the present cabinet. No opening method was observed.” Then P01 | `Return` → `shore_ready`, CP00 |
| `observing`: continue watching | P06, immediately after P05 unless interrupted | Authored `EvidenceHandoff` → `evidence_seen`, CP03; mark evidence once |
| `observing`: Return before P06 | Same early-return response and P01 | `Return` → `shore_ready`, CP00; evidence absent |
| `observing` / `evidence_seen`: speak to Ruth, pull present handle, take recorded clamp | “This is a recorded event. Ruth continues without responding. Present objects cannot be changed in this view. Return is available.” | No transition or grant |
| `evidence_seen`: Return | P07 | `Return` → `returned`, CP04; retain evidence |
| `returned`: review note | Only P06's quoted observation, labeled “Kept observation — present mode” | No transition or required reread |
| `returned`: replay | P05 then P06, labeled replay | `ReplayObservation` → `evidence_seen`, CP03; no second evidence grant |
| `returned`: inspect lower edge | P08 | `InspectPanelLip` → `panel_exposed`, CP05 |
| `panel_exposed`: release | P09 | `ReleaseCatch` → `cabinet_open`, CP06; **no clamp yet** |
| `cabinet_open`: inspect pen | “DANIEL: Not even one of the good ones.” | No transition |
| `cabinet_open`: take clamp | P10 | `CollectClamp` → `complete`, CP07; mark one clamp and envelope aside |
| `complete`: take clamp again | “You already have the clamp.” | No additional grant |

In `returned`, handle/panel inspections retain existing feedback; neither is required. Keep Return visible during recordings. Rereading resets nothing. Replay is offered at `returned`, retaining knowledge.

P05–P06 are consecutive authored beats, without a “continue” action. Read normally; honor Return before handoff. Never delay to manufacture an early-return attempt. Paper does not test build timing.

### Requested assistance

Supply requested assistance; never escalate automatically.

- **Hint 1:** “The handle did not open it for Ruth. Watch where her other hand goes.”
- **Hint 2:** “Return to the shop. The old lower lip is beneath the later panel; inspect that edge, then release the catch.”
- **Show next step:** perform one next valid step using the row below, then return control. Do not silently finish the whole puzzle.

| Current state | Show next step does |
| --- | --- |
| `shore_ready` | Select the loading-door anchor; P04 |
| `aligning` | Accept assisted alignment and Observe; P05 |
| `observing` | Present ordered routine text through P06; the authored handoff supplies evidence |
| `evidence_seen` | Return; P07 |
| `returned` | Inspect panel lip; P08 |
| `panel_exposed` | Release catch; P09 |
| `cabinet_open` | Collect clamp; P10 |

Hint 2 before observation does not bypass the evidence gate. State that requirement using P11 if the player attempts the lip early. After evidence exists, assistance does not demand another replay. At completion, independently check: evidence present; drawer opened before collection; exactly one clamp; envelope aside. These are facilitator records, not claims of durable software saves.

## 4. Blank observation sheet and debrief

Copy one sheet per session; leave it blank until a person actually plays.

| Session field | Entry |
| --- | --- |
| Anonymous label / content revision | |
| Prior puzzle familiarity / prior knowledge of this puzzle | |
| Text preference / interruptions / facilitator deviations | |
| Completion or participant-chosen stop | |

| Elapsed | State / card | Player's intended action or exact words | Result / requested help | Observer interpretation, kept separate |
| --- | --- | --- | --- | --- |
| | | | | |
| | | | | |
| | | | | |
| | | | | |

Ask without correcting their answers first:

1. “What were you trying to achieve, and what made the cabinet open?”
2. “What could you do in the recorded view? What required coming back?”
3. “When did you first think you knew the answer? Was anything still making you wait or repeat work?”
4. “Was there an action you wanted to try that these cards did not support?”
5. “Which moment, if any, felt satisfying? Which would you shorten?”
6. “At the end, was there anything you wanted to find out next?”

Record answers before explaining the intended rule. Distinguish an unsolicited correct deduction from following Hint 2. Both are legitimate completion; they answer different design questions.

## 5. Formative decisions

These are local revision triggers, not statistical claims. Keep uncollected results blank.

| Actual observation | Next decision |
| --- | --- |
| Fewer than four of five explain information-only recording and present action | Revise mode/clue presentation before expanding chapters |
| Two independently infer the lip early and call the evidence gate obstructive | Review the tutorial guard with the manifest, architecture and fixtures; do not waive it within this pack |
| Two wanting an unaided solve make repeated undirected choices | Revise the specific missing observation or feedback |
| Most explain the rule and name a satisfying action | Advance to the existing opening proof; preserve contrary accounts |
| A required fact is unreadable with the chosen text presentation | Repair that presentation before proceeding |

With fewer than five sessions, report individual observations and unresolved questions; do not claim the four-of-five gate passed. Help use alone is not failure. If comprehension works but satisfaction remains uncertain, a playable visual/audio response is the next useful evidence. More paper wording cannot establish that payoff.

## 6. Desk verification performed for this pack

These routes were manually checked against the unchanged manifest. **These are authored traces, not participant results or executed software tests.**

| Route | Manifest trace and expected result |
| --- | --- |
| Ordinary deduction | `shore_ready → aligning → observing → evidence_seen → returned → panel_exposed → cabinet_open → complete`; CP01–CP07, one evidence and one item |
| Early return | `aligning → shore_ready`; or `observing → shore_ready` before handoff. Both CP00, no evidence; re-entry follows ordinary route |
| Wrong mode / first-try answer | Recorded handle action leaves state unchanged. Early lip inspection leaves `shore_ready` unchanged; P11 acknowledges inference |
| Replay | `returned → evidence_seen → returned`; CP03/CP04, evidence retained once; inspection can follow without note review |
| Fully assisted | Same ordinary transitions, including authored evidence handoff; release reaches only `cabinet_open`; another request collects once |

## 7. Separate scene table read

For a short v1.3 pass, read these current canonical scenes as separate packets. State only the preceding facts needed to follow the exchange; do not announce the intended feeling. Each variant receives its own read, not a montage of unchosen replies.

| Passage / variant | What to present | Ask afterward |
| --- | --- | --- |
| C1S1 | The source begins, the player stops it, the receiver continues, then Return | “What did you change? What still happened? What does Daniel need next?” Paper can test understanding, not how striking the audiovisual event is. |
| C2S1 / P03 | One chosen sound order and its matching final-source reply; use another order on a separate pass | “What did Alice make? What did you choose? Would you change or replay it?” Printed sound captions cannot establish listening pleasure. |
| C3S2 / P06 | The correction, Mara's challenge and the unconditional return | “What was a mistake? What was Daniel responsible for? What does Mara want now?” |
| C4S1 / P08 | Move-then-repeat or repeat-then-move, followed by sensation and erasure | “Where is the washer? What repeats? What is gone? What did Daniel fail to feel?” Correct order comprehension is not evidence that the scene feels unsettling. |
| C4S2 / P09 | Private timetable correction, one chosen viable route, then one work/nerves reply | “Why choose that route? When does work begin? What does Mara offer? What does Daniel know?” |
| C4S3 / P10 into C4S4 | One first approach and one existing response, then the shared reconciliation | “What did each person assume or withhold? What did helping change? What still needs agreement?” Read other combinations separately if the initial response leaves ambiguity. |

For the larger emotional sequence, use the following separate reads rather than expecting one session to answer every question.

Use fresh readers where practical; ending knowledge would contaminate an opening curiosity trial. Select the current canonical passages linked from [the revision notes](11-story-and-scene-revisions.md): C3S3; C4S3–C4S4; C5S1; then C6S3–C7S3 and one ending per read. Read C1S2 before the final sequence to test recognition. Supply preceding story context neutrally, without naming the emotion or surprise being tested. Readers may decline later tragic material or stop.

Assign character voices and a stage-direction reader; read at a natural pace. Mark attention breaks without stopping to repair every line. After each passage ask: “What did each person want?”, “Where did that change?”, and “Which line or action felt unnecessary?” For the final sequence, ask what Alice knows now, what each ending costs, and which earlier detail changed meaning. Record answers before explaining intent.

On a second pass, revise only the repeated beat, unclear motivation or missing causal link identified. Keep a line only if it serves the immediate exchange; do not improve every character into the same eloquent speaker. A table read can expose confusion and repetitive dialogue. It cannot certify awe, nostalgia, grief or the fun of an unbuilt interaction.
