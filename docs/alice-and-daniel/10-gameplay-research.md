# What the Water Keeps — research for compelling play

**Version 1.2 · 22 September 2026.** Research and design hypotheses, not evidence that this game is already fun. Read with [game design](02-game-design.md), [gameplay and playtest plan](12-gameplay-and-playtest-plan.md), and the [solo roadmap](07-implementation-roadmap.md). The canonical interaction specifications remain in the game design document; this file explains the reasoning and its limits.

## The recommendation

Make the player want to continue because they have an idea they want to test, someone they want to help, or a question they want answered. Give them the satisfaction of doing those things. The most promising improvement is **more discovery and expression within the existing interactions**, followed by clearer, more varied payoffs.

The project already has a useful foundation: a legible reflection rule, persistent knowledge, forgiving input, characters with practical work, and a final encounter unlocked through earlier learning. Its main design risk is that twelve different objects conceal the same activity: follow instructions, match the obvious labels, receive dialogue. A second risk is emotional sameness: mournful conversations can make a tragedy feel flat long before the tragic climax.

For this finite premium story, the success criterion is voluntary interest: “I want to see what this means” or “I think I can work this out.” A satisfying stopping point and an easy return belong in that experience. The sources below do not supply a formula for addictiveness or a guarantee of commercial success.

## What the sources actually support

Six primary sources were read: an original research paper, two developer production articles, a designer's original essay, a first-person designer Q&A, and an original conference presentation. **Evidence** describes what a source reports. **Application** is a proposal for this project. These are deliberately separated.

### R1. Curiosity needs usable leads and time to understand them

**Source:** Alex Beachum, [Demaking Outer Wilds](https://www.mobiusdigitalgames.com/news/demaking-outer-wilds), Mobius Digital, 30 July 2015.

**Evidence:** Beachum describes narrative clues that lead to other clues and major answers. His team tested comprehension using paper and text prototypes that removed spaceflight. Testers' note-taking supported a discovery record. Compressing the story too much overwhelmed some players, revealing a need for breathing room.

**Application:** Paper-test whether P02's observation suggests a present action; whether P05's changed plate invites comparison; and whether P11's familiar landmarks can become one apparatus map. Let the ledger retain evidence without automatically stating every deduction. After a major answer, allow an ordinary action or conversation before delivering another explanation.

**Limit:** This is a developer report from a different, much larger exploration game, not a controlled comparison. It supports a testing method and design hypothesis; it does not justify adding an open world or time-loop system here.

### R2. Feeling capable and having some control matter

**Source:** Richard M. Ryan, C. Scott Rigby and Andrew Przybylski, [The Motivational Pull of Video Games: A Self-Determination Theory Approach](https://selfdeterminationtheory.org/SDT/documents/2006_RyanRigbyPrzybylski_MandE.pdf), 2006, DOI 10.1007/s11031-006-9051-8.

**Evidence:** Across four studies, the authors examine game motivation and psychological need satisfaction. Perceived competence and autonomy are associated with enjoyment and preference; intuitive controls also relate to these experiences. Their multiplayer survey includes relatedness as a predictor of enjoyment and future play.

**Application:** Let players select the order of P01's inspections and P11's sectors, test a thought without resetting the scene, and hear a clear result. P07 can accept more than one satisfying mix. Show consequences of dialogue approaches without implying that every line changes the plot.

**Limit:** These findings do not establish the right difficulty, scene duration, or number of choices for this game. A multiplayer relatedness result is not proof that affection for an authored character has the same effect. No retention percentage can be inferred from this paper.

### R3. Fair puzzles should move the story

**Source:** Ron Gilbert, [Why Adventure Games Suck](https://grumpygamer.com/why_adventure_games_suck/), written 1989, posted 12 May 2004.

**Evidence:** Gilbert advocates clear goals, intelligible solutions, recognition of player intent, progress from puzzle completion, and avoiding failures that require foreknowledge. He also warns against adding empty puzzles to lengthen a game.

**Application:** P02 should establish the stuck cabinet before revealing Ruth's technique. Once the player understands the catch, a generous hotspot should accept the action. P05's incorrect alignment must reveal a concrete mismatch. P12 should pay off earlier understanding instead of withholding the reunion behind a new cipher.

**Limit:** These are practitioner rules of thumb; Gilbert's introduction explicitly says his views had evolved. His preference for broader exploration is not a mandate to discard this project's authored scene order. Local inspection choices and requested assistance are affordable ways to relieve a bottleneck.

### R4. Expression can coexist with approachable puzzles

**Source:** Zach Gage, [first-person puzzle-design AMA](https://www.reddit.com/r/puzzles/comments/17g7k3n/im_indie_game_designer_zach_gage_creator_of/), 25 October 2023. Relevant answers are posted by `stfj`, the account introducing the AMA.

**Evidence:** Gage describes his preference for puzzles with different routes through them, sometimes different valid outcomes. He discusses welcoming players, supporting curiosity, and accommodating differing preferences around challenge and timers. These are his design goals and observations, not experimental findings.

**Application:** P07 is the best inexpensive place for multiple valid outcomes because it already has stepped audio controls and broad acceptable ranges. P03 can let the player audition takes freely. A personal preference can affect playback or a brief response while leaving the canonical story intact.

**Limit:** His examples are largely repeatable newspaper-style or systemic puzzle games. This project needs neither a score chase nor endless variants. Keep authored facts and unique mechanical solutions where the story requires them.

### R5. Nostalgia needs a place the player enjoyed belonging to

**Source:** Kelsey in the Narrative Department, [A Very Narrative UPDATE!](https://www.mobiusdigitalgames.com/news/a-very-narrative-update), Mobius Digital, 7 July 2015.

**Evidence:** The post describes revising an excessively hostile hometown cast. The team wanted the player to feel part of the world and some nostalgia on departure, so characters gained clearer relationships and investment in the player's launch.

**Application:** P01 should include the pleasure of repairing something with Ruth. P03 needs Alice and Mara enjoying an imperfect creation. P04 permits competitive silliness; P07 lets a useful piece of work succeed. These make the later empty shop, dock and rise the absence of specific experiences the player shared.

**Limit:** This reports authorial intention and development decisions, not a measured nostalgia effect. Warmth alone cannot guarantee attachment. Sharp disagreements remain valuable when those relationships contain other experiences too.

### R6. Peaks need recovery, but timing must fit the genre

**Source:** Michael Booth, Valve, [The AI Systems of Left 4 Dead](https://steamcdn-a.akamaihd.net/apps/valve/2009/ai_systems_of_l4d_mike_booth.pdf), 2009. Relevant section: PDF pages 78–82 and 92, counting the title page as page 1.

**Evidence:** Booth describes intensity peaks and valleys, fatigue from constant combat, and a pacing system with buildup, peak, fade and relaxation. The presentation distinguishes modulation of pacing from modulation of difficulty.

**Application:** Hand-author contrast across this story: a playful successful task, an unsettling discovery, a quiet response, then renewed effort. P12 can culminate in a large audiovisual payoff followed by the fragile simplicity of Alice answering a new question.

**Limit:** This is a cooperative survival-horror design presentation. Applying its contrast principle to grief, dialogue and puzzle discovery is an inference. Do not copy its combat timing values, construct an adaptive director, or claim that low emotional intensity equals boredom.

## Translate the research into the existing game

The following are project-specific hypotheses. They preserve twelve puzzle IDs, twenty-eight shared scene slots, the two Alice-perspective scenes, six location kits, and the three ending meanings. They do not add content on top of the current time allocation.

| Interaction | Source of pleasure to emphasize | Concrete direction | What would show it is failing? |
|---|---|---|---|
| **P01 — radio** | Becoming useful with Ruth | Let the player investigate symptoms and test a repair; make the resulting clear speech a satisfying change | Players say they simply selected the highlighted replacement and cannot explain the fault |
| **P02 — hidden catch** | Applying knowledge across time | Show the present obstruction, provide the observable technique, then let the player act without compulsory recitation | Players understand the technique but fight the interface; or complete it without noticing why the reflection mattered |
| **P03 — sounds** | Playful making | Let players audition the three existing sources and enjoy the unlikely transformation into a tiny imagined journey | Players remember a sorting task but no joke, surprise, or affection between Alice and Mara |
| **P04 — measurement** | Friendly rivalry and noticing an unfair comparison | Allow the wrong origin to produce an inspectable discrepancy before the fair measurement | The scene feels like a compulsory school worksheet with a prescribed winner |
| **P05 — winch** | A fair reversal of an earlier lesson | Make copying the old arrow plausible, then reveal why the persistent notch is the reliable evidence | Players think the solution arbitrarily contradicts what P02 taught, or Jonah gives the answer before they can compare |
| **P06 — ledger** | Discovering a more accurate account | Keep the conflicting evidence readable together; let the correction lead straight into returning the recorder | The evidence test feels like grading Daniel's love or searching for a hidden morality answer |
| **P07 — playback** | Creative choice and a shared win | Accept distinct clear mixes with the existing stepped controls; preserve the accidental mug crash | Every legal result sounds identical, or a clarity meter substitutes for any audible/captioned cause |
| **P08 — washer** | Safely testing a disturbing possibility | Emphasize physical washer versus absent recorded movement; the player can check the difference | Players memorize mode names but cannot describe what was erased |
| **P09 — job** | Alice making a workable future | Keep each conflict about a visible logistical constraint; let acceptance feel like an achievement she wants | It becomes arithmetic filler, or players think a wrong itinerary can destroy her career |
| **P10 — packing** | An argument with tangible stakes | Use ownership and the unagreed hall bookings to expose the disagreement; keep the exchange shorter than its emotional aftermath | Sorting feels like a moral quiz, or props delay an argument the player already understands |
| **P11 — source map** | Recognizing an old place as a newly useful whole | Preserve any-order sectors; each alignment should contribute a legible part of the combined map | Players perform the same rotation three times without discovering a relationship |
| **P12 — contact** | Bringing learned abilities together | Make the selected source, Alice state and return carrier understandable as a working arrangement; reward completion with the encounter | Players copy symbols mechanically or encounter a new scientific rule at the last gate |

These are not twelve demands for higher difficulty. P03 and P07 earn their time through creation, P06 and P10 through changing a relationship, P08 through an experiment, and P12 through synthesis. The desired thinking differs even when all use the same accessible tap controls.

## A small chain of questions the player can carry

Keep an immediate task legible while allowing a larger uncertainty to persist. A player's unanswered question should have a visible reason to exist, and its answer should change what they understand or can do.

| First invitation | Useful answer | What remains open |
|---|---|---|
| C1S1: why does the receiver reveal something absent? | P02: recorded knowledge can guide present action | How far can a stored event be used? |
| C1S2: why was Alice crying at the lake? | C7S2: the common encounter explains the childhood glimpse | What will Daniel choose after understanding it? |
| C2S3: whose recorder has Daniel kept? | P06: the service evidence and Mara's account establish ownership | What else has he allowed his own account to eclipse? |
| P05: why does copying the past fail here? | The present plate changed; the fixed structural relation did not | Which familiar features still connect the shore? |
| P08: what actually disappears when a trace is erased? | The experiment separates event storage from the physical object | What would closing the whole lake cost? |
| P11–P12: can all this knowledge make contact possible? | C6S4: Alice responds to new information | What does care require once he knows her limits? |

This table is an editorial tool, not a new quest screen. Do not put future answers in the ledger, imply that Alice's death is a mystery to solve, or make the final childhood recognition a required puzzle. One emotional question can remain open for much longer than a mechanical task.

## Making emotional variety playable

**Triumph:** The player repairs, makes, helps, and eventually achieves contact. A successful P07 mix should receive a real use in the fundraiser; successful P12 calibration should produce an unmistakable transition. Let those successes stand for a moment before introducing their cost.

**Wonder and shock:** The surprise should revise a model the player had enough evidence to build. P05 can overturn “copy what I saw” while preserving the reflection rules. Responsive Alice can transform the meaning of a stored person without changing source/reset rules. More unexplained powers would weaken both surprises.

**Nostalgia:** Let childhood contain something worth replaying voluntarily: an awkward joke, a slightly ridiculous recording, a petty contest, the pleasure of being trusted with a tool. Later familiarity should come from exact props and spatial relationships already used, rather than an additional explanatory flashback.

**Melancholy and sadness:** Give the player enough control to remain present: finish an ordinary action, choose when to continue, inspect a meaningful object. An input need not solve grief to matter. C5S2's emergency remains free of a rescue-performance test.

**Epic scale:** Spend existing visual and sound resources where accumulated learning pays off. P12 can unite previously established source indicators through a short authored sequence using the existing bay and shore assets. A broader sense of possibility can come from composition, layers activating in response to the player's preparation, and a restrained musical expansion. This is a presentation proposal, not a new water simulation or additional location.

**Recovery:** After a major revelation, a short act with a clear purpose can carry the emotion while reducing information load. Preserve the tea, the scrape dressing, the empty-place sequence, and the ordinary actions in E3. A still scene with a changed meaning is doing work; mandatory waiting without a change is not.

## The cheapest useful validation

The companion [playtest plan](12-gameplay-and-playtest-plan.md) owns implementation candidates and detailed checks. Research suggests prioritizing these uncertainties before final assets:

1. **Can a new player infer?** Use rough cards/screens for P02 and P05. Ask for their expected action, then let them try it. Record the evidence they used and where they first began guessing. Do not teach the intended answer while measuring discoverability.
2. **Does a success feel earned?** After P01 or P02, ask “What made that work?” Pair their explanation with what they actually did. Quick completion can mean clear insight or empty instructions; elapsed time alone cannot distinguish them.
3. **Does expression matter?** Let different players finish P07 without being shown a target setting. Check whether they notice, prefer and understand their result. If they cannot, simplify instead of adding more controls.
4. **Do the emotional beats differ?** After an opening read/play session, ask for the moment they most enjoyed, the question they still care about, and any passage they wanted to skip. Collect their words before offering emotion labels.
5. **Does the knowledge chain survive interruption?** Resume after a checkpoint. A factual recap should restore the immediate task and available evidence without solving it. Check this with muted audio and enlarged text too.
6. **Does the player understand the cost?** Before the final choice, ask them to explain the previews. Misunderstanding an ending is a clarity defect, even if the resulting surprise is intense.

A first small round can identify specific breakdowns; it cannot estimate the audience's completion rate or prove broad appeal. Use fresh players when retesting a changed revelation, since someone who knows the answer is no longer testing discovery. Separate facilitator mistakes, unreadable clues, missing feedback and difficult inference before deciding to simplify a puzzle.

## Production decision and evidence limits

First prove **P02's discovery**, then **P05's changed-context deduction**, then **P07's expressive success**. Paper-test P11/P12's connection before investing in the climactic presentation. Keep the existing offline state model, checkpoint behavior, assists and explicit ending previews. Save-driven progress and short scene transitions are enough; this research calls for no backend, procedural story generator, combat system, skill tree, extra cast, or new paid dependency.

Source review date: 22 September 2026. Only directly reviewed primary page or PDF content supports the findings above. Practitioner experience and the empirical paper have different evidential limits; neither measures this game.

No player has tested these proposals in this revision. Timing, difficulty, emotional impact and device usability remain design questions. The next useful result is a player making an interesting inference and wanting to act on it, not a larger specification claiming that they will.
