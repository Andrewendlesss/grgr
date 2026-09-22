# Continue on another computer
Version 1.3 · 22 September 2026

## Location of the work

Repository: [Andrewendlesss/grgr](https://github.com/Andrewendlesss/grgr)  
Branch: `codex/alice-daniel-creative-direction`  
Open draft: [PR #2](https://github.com/Andrewendlesss/grgr/pull/2)  
Start document: `docs/alice-and-daniel/README.md`

The planning files are on the named branch and draft PR, not merged into main. The remote repository is the portable source of truth. A local ZIP is only a convenience.

For a fresh checkout:

```sh
git clone --branch codex/alice-daniel-creative-direction https://github.com/Andrewendlesss/grgr.git
```

For an existing checkout, inspect its current changes before switching; fetch the branch without replacing unrelated work.

## User instructions that carry forward

- Keep expanding and improving the story and game design. The latest instruction is to continue planning, research engaging gameplay, and increase emotional variety: triumph, awe, warmth, sadness, nostalgia, melancholy, shock and surprise.
- Keep an original dramatic voice with subtext, layered revelations and distinct characters. Do not put creative influence labels in the game or planning copy.
- Start planning implementation.
- **Solo developer; keep cash costs low.**
- Preserve the three ending meanings and the original final sentence.
- An earlier handoff was prepared for a move between computers. The latest request is to keep planning and improving. Do not assume that planned production or technical details have been implemented or tested.
- No installation, purchase, voice commission, store submission, merge or playable build has been performed.

## What is complete

The current v1.3 continuation strengthens the opening with a player-caused experiment, replaces four more low-value tasks (P03, P08, P09, P10), and sharpens Mara's recorder confrontation (P06). Alice's work excitement and Mara's practical support have more room. Both travel choices preserve the private reunion callback, and work-start/departure arithmetic is corrected. The [paper playtest pack](13-paper-playtest-pack.md) is prepared, with staged P02 cards, private facilitator instructions, blank records and scene questions.

The v1.2 primary-source research (10), emotional contrast and six earlier interaction revisions remain. Documents 11 and 12 record and explain the current revisions; the canonical screenplays and game design already contain them. Do not apply the notes as another patch. Canon, ending meanings, the final sentence, 28 slots, 12 interactions, six kits and 14 main views are retained. The old hour ranges remain v1.1 estimates awaiting a targeted re-estimate.

**No paper trial, table read or player test has been performed.** Research supports design hypotheses; it does not demonstrate this game is fun. This continuation changes planning and authored text only.

### Earlier completed planning

The package contains the revised story bible, all seven scripted chapters and all three endings, the 28 scene plan, 12 interaction designs, a performance guide, implementation architecture, solo roadmap and art/audio/interface specification.

The v1.1 revision strengthens ordinary obligations and Alice's own concerns, plants the previously missing spoken “Just one more,” fixes recorder-case/phone/food continuity, and makes P05 compare an old reflected plate with Jonah's changed present equipment. Optional beats remain small and carry no morality score.

Implementation planning includes a concrete P02 manifest/schema, ending flow example, and 24 planned backlog tickets. The first 16 tickets total 77–125 hours before 20% reserve. They are not completed tasks.

## Technical decisions

Provisional stack: Unity 6.3 LTS, C#, URP, ink, text-led dialogue, local offline content. Pin a tested patch after an Android/Windows export; verify or revise for iOS at IMP-018 with Mac/iPhone access.

Use GameSession as authoritative world state and SessionCoordinator to stage commands. Save combined world/ink state durably before acknowledging consequential progress. ReleaseCatch opens the cabinet; CollectClamp separately grants the clamp exactly once.

Use one selected recorded view and a bounded reflection effect. P05 reuses that system. Do not build a general time-travel simulator, runtime AI story service, backend, custom quest editor or paid cloud dependency.

## Environment and validation limits

The prior host was Windows. Git and .NET were found. Unity/Hub were not found on PATH or the two standard Program Files locations checked; installation elsewhere was not ruled out. Recheck on the new machine.

P02 JSON was checked against the supplied schema with PowerShell Test-Json. JSON syntax, basic P02 reachability, ending invariants and backlog dependency/estimate checks were performed. These do not establish that Unity APIs compile or that mobile saves/rendering work.

No Unity project, compiled ink, shader, device build, real save migration, benchmark or store account setup exists yet. Platform sources are dated 22 September 2026; recheck when building.

## Checks completed in the v1.2 continuation

- Local document links and whitespace checks passed. All 28 unique shared scene IDs, 12 puzzle IDs and two Alice viewpoint scenes are retained.
- The complete E1/E2/E3 screenplay passages and the original final sentence are unchanged from the incoming branch snapshot.
- JSON files parse; all 24 backlog tickets remain planned; dependency references and their graph are valid. Retained first-sixteen estimates still sum to 77–125 hours, not a new estimate.
- The P02 manifest, its schema and the ending fixture are unchanged. Their earlier schema validation was not repeated in this continuation.
- The proposed P07 rule accepts seven of 27 configurations. This checks the authored table logic, not whether the audio actually sounds clear.
- Editorial review checked the radio's fault/test continuity, requested rather than automatic solution hints, changed P11 station comparisons, full ending consequences and Alice's knowledge/agency.

These are document and data checks. No executable game, device measurement, human table read or player study was produced.

## Checks completed in the v1.3 continuation

- Reviewed the player-caused opening, both P08 probe orders, P03's six accepted arrangements, both travel routes and P10's reconverging approaches against the canonical dialogue.
- Corrected the job timing: acceptance at day zero, travel on the eighth evening, first call on day nine, argument four days after acceptance. Both routes include the private platform correction before selection.
- Compared the paper cards with the P02 manifest, including early Return, replay, the required observed fact, one-step assistance and separate release/collection. These are desk checks, not participant sessions.
- Preserved the six v1.2 detailed interaction specifications and the complete three ending passages. Current metadata, architecture notes and backlog criteria now point to the v1.3 content. Effort ranges remain unrevised.
- Checked 61 local document links, JSON syntax for all four examples, four P02 transition traces, 28 scene IDs, 12 interaction IDs, the two Alice viewpoints and the backlog dependency graph. The first-sixteen estimate remains 77–125 hours. The unchanged schema's full validation was not repeated because the validator module was unavailable on this host.

Whitespace checks passed. No build, audio audition, human table read or playtest has occurred.

## Exact next actions

1. Read the index, research summary, current screenplays, revision notes and gameplay plan. The v1.3 revisions are already integrated; continue this story rather than restarting its concept.
2. Use the ready P02 cards in document 13 for a current-condition trial when participants are arranged. Keep its answer key private. Establish whether people infer the changed-surface solution and whether the observation gate obstructs an already correct inference; resolve that before comparing clue orders. Record actual notes; five people would not establish market demand.
3. Use document 13’s focused scene protocol, including P03 creation, Mara’s recorder exchange, both P08 probe orders, both travel choices and both packing approaches. Read the larger emotional sequence from the fundraiser through each ending in separate sessions. Test distinct voices, room for joy, knowledge order and the reset explanation.
4. Revise the particular source of confusion or disengagement, then re-estimate affected tickets. Retain earned successes; do not add filler or new systems to increase length.
5. When implementation begins, complete IMP-001 on the actual development host: tools, device route, weekly capacity and iOS feasibility. This session did not establish those facts.
6. Prove an empty device build, then implement only C1S1–S4 and P02 under `game/WaterKeeps/`, preserving stable IDs and the combined save protocol.
7. Exercise C1S1 with early Return, optional replay and muted/resumed presentation. Test P02 with early return, replay, muted assistance, incorrect hypotheses and restart after clamp collection. ReleaseCatch opens the cabinet; CollectClamp grants its item separately and once.
8. Observe the playable opening before commissioning final assets. Re-estimate full-game effort and cash from measured work. The paid-team budget is not the selected path.

## Remaining editorial and production work

- Table-read the revised dialogue; optional beats have not been timed.
- Playtest the 151–153 minute allocation and adjust advertised length rather than padding.
- Confirm the 14-view art plan can stage every scene clearly on a phone.
- Measure the complete save protocol and reflection cost on devices.
- Convert prose to stable runtime content without inventing missing APIs.
- Validate accessibility with actual users/devices; do not claim full nonvisual support from a checklist.
- Obtain any eventual specialist art/audio/localization quotes before allocating cash.
- Review the emergency and fatal ending staging before final animation/recording.

Recommended continuation prompt:

> Continue from docs/alice-and-daniel/09-handoff.md on branch codex/alice-daniel-creative-direction. Read the integrated v1.3 scenes/gameplay specifications, primary-source research and prepared paper playtest pack. Keep the solo, low-cash scope and all ending invariants. Continue targeted story/gameplay improvements; use the prepared tests when participants are arranged, or execute the smallest opening prototype if implementation is now requested. Improve player inference, emotional contrast and character voice. Report only tests and builds actually performed.
