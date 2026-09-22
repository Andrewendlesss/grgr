# Implementation planning fixtures

These small JSON files make the proposed contracts reviewable before a Unity project exists. They are **not working game content, compiled ink, save files, or a runnable implementation**. Names describe proposed APIs and do not prove that those APIs have been written.

| File | Purpose |
|---|---|
| `P02.scene.example.json` | Concrete authoring handoff for the first reflection puzzle |
| `scene-contract.schema.json` | JSON Schema shape checks for that puzzle manifest |
| `ending-flow.example.json` | Explicit commitment, interruption, and branch checkpoints |
| `backlog.json` | Dependency-ordered solo implementation tickets, estimates, and acceptance checks |

The P02 schema checks required fields, types, allowable event origins, and safe identifier patterns. A future content validator must additionally check that targets and checkpoints exist, every reachable stage has a path to completion, evidence can be replayed, Return remains available, ledger grants are idempotent, and disabled present-world interaction cannot be bypassed. A schema cannot prove those properties or validate how the scene feels.

The ending fixture is a separate illustrative contract; it is not covered by the scene schema. The full narrative consequences remain in the story bible and screenplay. Technical labels such as `source_erased` describe implementation state; they are not words shown to players.

Validation performed on 22 September 2026: all JSON fixtures parsed; PowerShell `Test-Json` accepted `P02.scene.example.json` against `scene-contract.schema.json`. Additional checks confirmed that P02's declared stages are reachable, its transitions name declared stages, and the ending fixture contains all three outcomes with no default selection or timeout. The backlog's 24 ticket IDs and dependency references were valid, its graph had no cycle, and its first sixteen estimates summed to 77–125 focused hours. These are document/data checks, not evidence of a working runtime or tested game behavior. The ending and backlog files do not yet have dedicated schemas.

`contentVersion` identifies the content contract, not a shipped build. Values in the files are editorial examples. Tuning values and UI text require phone testing and script/localization approval before becoming runtime data. All examples are local, contain no credentials, and imply no cloud dependency.

Version 1.2 retains the P02 transition and ending fixtures. Its changes concern clue presentation and feedback, with separate catch-opening and clamp-collection effects preserved. The backlog adds the new observation criteria; its numeric effort ranges still come from v1.1 and require review after the paper trial. Document 12 is the detailed design companion. No new runtime is implied.
