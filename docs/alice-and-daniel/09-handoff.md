# Continue on another computer
Version 1.1 · 22 September 2026

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

- Keep expanding and improving the story and game design.
- Start planning implementation.
- **Solo developer; keep cash costs low.**
- Preserve the three ending meanings and the original final sentence.
- The latest session was time-limited because the user was moving computers. Do not assume every production or technical detail was implemented or tested.
- No installation, purchase, voice commission, store submission, merge or playable build has been performed.

## What is complete

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

## Exact next actions

1. Read the index, architecture and solo roadmap. Do not regenerate the existing story from scratch.
2. Complete IMP-001 on the new host: editor availability, disk, C# familiarity, weekly capacity, Android device and future Mac/iPhone route.
3. Create the minimal project under `game/WaterKeeps/` only when implementation begins. Preserve the documentation and current branch history.
4. Prove an empty device build, then import only C1S1–S4 with stable IDs.
5. Implement input/dialogue, the authoritative session and combined checkpoints.
6. Build P02 with temporary art, including early return, muted assistance and restart after clamp collection.
7. Integrate the ordinary radio scene and complete the opening proof.
8. Observe outside players before commissioning final assets.
9. Re-estimate full-game time and cash from measured work. The original paid-team budget is not this user's selected path.

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

> Continue from docs/alice-and-daniel/09-handoff.md on branch codex/alice-daniel-creative-direction. Keep the solo, low-cash constraint. Inspect the new machine and complete IMP-001, then begin the smallest Unity prototype for C1S1–C1S4 and P02. Preserve the current story and all three endings. Report what actually builds or tests, and keep unverified work explicit.

