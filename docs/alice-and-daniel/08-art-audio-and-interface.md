# Art, sound and interface direction — solo edition
Version 1.2 · 22 September 2026

This is the production-facing visual and audio specification. It describes assets to make, not finished art. The active resource constraint is one developer with low cash costs. The aim is a coherent, expressive illustrated game with a few memorable temporal images.

## 1. Visual premise

Paint people and places as things that have been used. Wood has repaired edges; a good coat has an imperfect sleeve; a shop counter has a clean patch where something stood. Color should be purposeful without turning the whole game gray.

Use graphic illustration with restrained texture, shallow planes and fixed composition. A small cast of readable poses is preferable to inexpensive-looking attempts at realistic facial animation. At phone size, posture, spacing, hands and the direction of attention carry emotion.

The late machine sequence earns spectacle through the same lake and buildings appearing at different depths and ages. It does not require a new city, gigantic laboratory or simulated flood.

For v1.2, stage that scale as successive authored states of existing views. A successful P12 step receives a distinct visual and captioned response before the next input; completed steps remain complete while the player reads or pauses. Use prepared overlays, framing and the established three-pulse cue. The large final response belongs to the player's completed calibration. It does not require simultaneous rendering of multiple worlds, a dynamic storm or a real-time stability timer. Reduce costly movement to a dissolve or held layered composition if necessary.

At the C3S3 fundraiser, the mix's clarity and the group's brief, practical celebration are the payoff. Existing poses and props can communicate it. Do not add a crowd simulation or a new speaking audience, and do not immediately darken the image to warn that happiness will end. C7S2 keeps its strict absence of remembered voices, figures and score.

The first art test should be a dock scene in two eras, with the people drawn at the size they will actually occupy on a phone. A beautiful close-up that cannot communicate at gameplay scale is not the correct test.

## 2. Palette and time

The following colors are proposed art anchors, not a requirement that every asset use only these swatches.

| Role | Starting color | Use |
| --- | --- | --- |
| Deep lake / night ink | #142429 | Background structure, UI panel foundation |
| Water midtone | #4F737C | Broad lake surfaces; adjust with weather |
| Warm paper | #F5F0E7 | Ledger, readable text, reflected summer light |
| Shop brass | #C5A05E | Small practical details and warm work lights |
| Faded terracotta | #BC7865 | Clothing/accent to keep scenes human |
| Weathered green | #718474 | Trees, painted railings, ordinary town material |
| Cloud gray | #B9C1BE | Overcast surfaces and neutral separation |

Thirteen: open air, more indirect daylight, bright but worn objects. Eighteen to twenty-two: use the same inhabited palette with changing costume and responsibilities. Thirty-four: fewer active lights and different objects, rather than a blanket blue filter. The ending morning is ordinary daylight, not a visual certificate of recovery.

Always identify a new era through a brief text card, clothes and a recognizable changed object. Color is supporting evidence. The player returning after several days must not need to remember which blue means which year.

Dialogue uses a sufficiently opaque dark panel and warm light text. Check contrast after compositing on the actual scene. Android's guidance recommends at least 4.5:1 for smaller text and large touch targets of at least 48dp; apply these as a baseline and verify actual Unity scaling and target devices. [Android accessibility guidance](https://developer.android.com/guide/topics/ui/accessibility/apps)

## 3. Fourteen principal views, six environment kits

The solo baseline replaces the earlier 24–30-view allowance. A view is a reusable authored composition, not a new location. The numbers are a scope ceiling to measure in the representative slice.

| Kit and IDs | Views | Story use and low-cost reuse |
| --- | ---: | --- |
| Dock: D01 approach, D02 end plank, D03 water toward shop | 3 | Meeting, reflection, reunion; D02 supplies the final empty dock |
| Repair shop: S01 counter/wide, S02 cabinet detail | 2 | Radio, Mara, fundraiser, repaired amplifier and final collection; dress the same frame |
| Flat: F01 table/door, F02 desk/window | 2 | Breakfast, argument, death, retirement papers, writing and morning |
| Boathouse: B01 bay, B02 immersed station, B03 control detail | 3 | Winch, washer test, preparation and culmination |
| Path: T01 measuring tree, T02 rise/path | 2 | Childhood game, anchors and two final empty frames |
| Bus shelter: U01 approach/wide, U02 seated pair | 2 | First kiss, job decision and reconciliation |

A detail insert can crop an existing painting or use a reusable prop overlay. It does not automatically authorize a new background. Log every requested new camera before drawing it.

Treat ages eighteen, twenty-one and twenty-two as costume/prop changes within a common adult-era set. Use a small number of era overlays for childhood and the final night. The upper planning allowance is **12–16 reusable era/weather overlays**, not fourteen new paintings for every year.

The fundraiser takes place in the established shop/shore setting. The hall mentioned in dialogue stays offscreen. Family members, customers and responders need not become fully animated principal characters.

## 4. Characters, poses and props

Use five principal character designs. Daniel and Alice need clear childhood/young-adult distinctions, and Daniel a present version. Jonah and Mara each need younger and older treatments; Ruth can be aged through costume, posture and a later photograph. Reuse underlying drawing structure where it still looks convincing.

Start production planning at **30–45 reusable pose cards**, plus **six to eight important bespoke pose transitions or hand inserts**. These replace the earlier full clip-library assumption. The representative slice must measure how much work a pose actually takes.

Daniel's regular action is making space on a bench, checking a label, aligning two things or remembering to hand over a tool. Alice's is listening to a sound, repositioning equipment, examining someone's reaction, or starting a joke and choosing whether to finish it. Ruth continues work while talking. Mara puts down what she is carrying only when a conversation becomes serious. Jonah makes a practical repair, then expects it to be left repaired.

For the opening proof, use seven simple actor pose cards: present Daniel seated/standing, young Daniel seated/standing, Alice thirteen seated/standing, and Ruth at the counter. Add one shared hand/prop detail. Rectangles and simple silhouettes are sufficient until the timing works.

High-priority reusable props:

- Ledger, pencil, radio, small parts tray, cup, tea towel.
- Recorder, separate empty case, labeled memory card, service slip.
- Cloth tape, stone, fixed bolt, metal marker, iron footing.
- Repaired hall amplifier and collection slip.
- Receiver, return control, marked washer, carrier plate.
- Phone, wrapped food, first-aid container, work light.

Do not draw every tool in the shop as a selectable object. The interaction budget, lighting and interface must distinguish what matters without making every useful item glow permanently.

## 5. Camera and editing rules

Establish the location before its useful detail. An unfamiliar player should know where Daniel is standing relative to the reflected action.

Use temporal match cuts only when the shared shape or sound is obvious: drawer closing to recorder transport, dock angle across ages, the same work light in the childhood glimpse and finale. A cut is not automatically a time jump; new periods receive a clear initial marker.

Hold silence as an active beat when someone decides what to say. Do not inflate every pause to make the runtime longer. Test silence with temporary performances and real players.

The three final empty shots have locked frame references: D02, T01 and T02. Their foreground and camera angle repeat earlier inhabited scenes. No ghost figures, old dialogue, animated photographs or memory overlays may be added during polish. The environmental sound can remain; the score leaves.

For the collapse, use the interrupted sentence, hand and chair, Daniel's response, and the call for help. The camera stays with his action; the scene needs no detailed body simulation. Shortened-content mode uses an earlier cut without changing what happened.

The fatal hand contact is a small physical event, not the most lavishly animated romantic scene. Give the shared encounter and the return branch equally specific expressions of affection.

## 6. Reflection staging

The reflection should first look like water, then reveal a discrepancy the player can understand. Keep the ordinary shore visible while observing so “past evidence” and “present action” remain distinct.

One selected recorded view appears within an authored mask. Use the implementation architecture's bounded second camera, or its measured simpler fallback. Never recursively render the lake into itself. Fine ripples are decoration; the cabinet catch must still be legible when distortion is disabled.

P02 uses S01/S02 content viewed from D03; Ruth's reach-under action is a small recorded pose sequence. P05 reuses B01's earlier empty plate and its structural notch, compared against the plate Jonah replaced. It introduces no extra speaking character or complete new era environment.

Final layers reuse the existing view assets. Three clear layers are more effective than twenty unreadable surfaces. The player must understand that the apparatus worked before the dialogue begins.

## 7. Interface as part of the tone

Use a quiet interface with plain language. The ledger can look personal, but body text must remain readable. Handwriting is decoration or an optional heading treatment, not the only way to read information.

The default scene frame has a persistent pause control, a small optional objective, and unobtrusive focus feedback. Dialogue uses a speaker name and one readable paragraph at a time. Do not place faces in expensive animated portrait boxes when the characters are already staged in the scene.

During reflection, show **Recorded moment** and a clear **Return to now** action. The wording explains the player's current capability without displaying internal state names such as `evidence_seen`.

Suggested layout hierarchy:

| Screen state | First thing read | Next available action | Persistent escape |
| --- | --- | --- | --- |
| Exploration | Place and immediate useful object | Inspect / approach | Pause |
| Conversation | Speaker and current line | Continue or explicit reply | Pause / transcript |
| Reflection | Recorded moment and recognizable landmark | Align / observe / return | Pause and Return |
| Puzzle assistance | One concrete clue | Another hint / show next step | Close |
| Final choice | Intent and its consequence | Open preview, then separate confirm | Back / pause |
| Resume | Era, current task, last completed fact | Continue | Settings / main menu |

Use consistent focus treatment on touch, mouse and controller. Touch targets may exceed the visible icon. A full-screen tap must not select a hidden choice behind a dialogue panel.

At maximum text size, grow or scroll the panel; do not shrink the text again to fit. During a long line, suspend optional character motion that competes for attention. Provide equivalent information for players who cannot hear the receiver pulses or see subtle hue differences.

## 8. Audio direction and cue map

The sound world belongs to work, weather and people: water against timber, a cabinet that sticks, a recorder transport, shoes on the path, a bus door and the work light. These establish place more economically than a constant score.

The signature is three unequal receiver pulses: two close together, then a later third. It must match across C1S1, the childhood image and the final alignment. Give it one source asset and reuse it; do not approximate its rhythm independently in three scenes.

| Cue ID | Placement | Purpose / accessibility |
| --- | --- | --- |
| AMB.SHORE.DAY | Childhood/young-adult shore | Ordinary occupied setting; descriptive caption only for relevant events |
| AMB.SHORE.NIGHT | Present shore | Same place with different activity; avoid generic horror drones |
| AMB.SHOP | Shop scenes | Work sounds under conversation; duck when needed |
| SFX.CABINET.CATCH | C1S3, C1S4 | Concrete match; ordered visual/text evidence also present |
| SFX.RECEIVER.THREE | Opening, glimpse, final alignment | Recognizable link; matching three-mark caption/visual cue |
| SFX.RECORDER.TRANSPORT | Alice recording scenes | Ordinary equipment identity; never grants supernatural power |
| VO.DANIEL.ONE_MORE | Childhood throw and final offer | Same delivered “Just one more”; no villain narrator |
| MUS.SUMMER | Selected companionship scenes | Small original theme; leave most ordinary work unscored |
| MUS.OPENING | Full machine alignment | Largest musical expansion, using existing theme material |
| MUS.LOOP | E1 | Same performance repeats without adding triumphant variation |
| AMB.EMPTY.PLACES | C7S2 and return walk | Present environment only, no character voice or explanatory score |

All cue IDs are authoring proposals and must be bound once in the project. If there is no voice budget, the “one more” callback can use the same optional developer-recorded temporary phrase in the proof and later become a licensed performance. A text-only release must repeat the exact subtitle and visual context rather than pretending an unheard spoken recording exists.

For the solo version, plan **three or four music themes totaling roughly eight to twelve original minutes**, reusable ambience, and a modest Foley set. This replaces the earlier 25–35-minute score allowance. Silence remains deliberate. Commissioning more music is optional after the actual mix has gaps.

A provisional motif can be a short, original phrase played plainly on a small instrument; do not use a recognizable film melody as a placeholder that becomes emotionally indispensable. Record temp ambience yourself where lawful and practical, or use assets with clearly documented licenses. No microphone permission is required from the player.

## 9. Low-cash asset workflow

Make the functional proof with flat shapes, temporary fonts, static poses and licensed placeholder sound. Kenney states that assets on its asset pages use CC0 and permits commercial use; verify the included license for each chosen pack and keep its provenance even when attribution is optional. These are potential prototype resources, not final art already selected. [Kenney asset licensing](https://kenney.nl/support)

For every imported asset, record creator, source URL, exact license, download date, modifications and required credit. Do not treat an image search result as a license. Final coherence matters more than accumulating free packs.

Only buy or commission a bounded item after the proof identifies a need: for example, an artist reviews the dock composition or supplies one agreed character sheet. Ask for editable sources, commercial rights appropriate to the work, and a defined revision allowance. The planning document does not approve spending.

Create at working resolution, then export device-specific textures from the source. Keep UI text separate from images. Transparent edges, large partially transparent layers and oversized audio files need phone testing, not assumptions based on how quickly they run on a PC.

## 10. Asset acceptance and review

An asset is accepted when it serves the scene at phone scale, loads within the provisional budget, survives the relevant accessibility mode, and has a complete source/license record. “Looks good in the drawing app” is not sufficient.

For a recorded action, test the evidence with music muted and reduced motion. For a character pose, show it without dialogue and ask where their attention is directed. For the final empty places, compare the actual shots to their earlier framing references.

At the representative-slice gate, measure:

- Hours per principal view, era overlay, reusable pose and bespoke insert.
- Time spent revising assets after integration.
- Readability at the smallest target display.
- Actual texture/audio memory during the reflection.
- Whether people understand the gesture and remember the place.

Keep a style decision only if it is both expressive and repeatable by this developer. A simpler coherent game can carry the entire story.
