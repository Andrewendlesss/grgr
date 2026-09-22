# What the Water Keeps — production and release plan

**Planning baseline: 22 September 2026.** This document describes work to commission and build; it does not claim a playable game exists. Estimates are illustrative USD planning assumptions, not supplier quotations, sales forecasts, or a funded schedule. Re-estimate after the prototype. Platform facts were checked against the official sources linked below and must be checked again before submission.

## 1. The product to build

Create a complete premium narrative puzzle adventure for Android and iOS, with an initial production target of roughly **2.5–3 hours** for a first playthrough. The current scene allocation totals approximately 151–153 minutes inside an unverified 140–170-minute planning envelope. These are design allocations, not measured playtimes. Use landscape framing, illustrated surfaces, shallow 3D staging, fixed cameras, and one-finger interaction. Preserve mouse and controller equivalents so a Windows/Steam edition remains practical.

The production promise is **an intimate relationship made playable through reflections of different years**. Three major visual sequences carry the spectacle: the first stable reflection, the machine opening the lake's layers, and the empty places at the ending. Reuse familiar environments in all three.

| Scope item | Production ceiling |
| --- | --- |
| Story | Seven chapters, 28 shared scene slots; final slot branches |
| Locations | Six primary location sets, with authored age/weather variants |
| Cast | Five principals: Daniel Vale, Alice Mercer, Ruth Vale, Jonah Reed, Mara Mercer |
| Play | Twelve substantial interactions, plus short everyday gestures |
| Viewpoints | Daniel, with two short Alice sequences |
| Endings | Three authored branches from a shared final encounter |
| Text | First-draft script approximately 10,000–11,000 words including direction; provisional 12,000-word ceiling for all translatable text |
| Business model | One purchase includes the entire story and every ending |
| Connectivity | Story and local saving work offline after installation |

Word count is a ceiling, not a duration formula. The original three-to-four-hour recommendation remains an aspiration only if meaningful play earns that length. The shorter current allocation preserves all 28 scene slots and twelve substantial interactions; it does not justify proportionally reducing the budget for the same authored assets and systems. Re-estimate effort from measured production tasks, and advertise only a length supported by observed playthroughs.

Maintain a timing sheet for every scene: performed dialogue, player reading, puzzle solving, everyday gestures, observation, traversal, and transitions. Mark mutually exclusive variants and endings so they are not added together. At the production-slice gate, replace allocations with observed ranges; at alpha, reconcile complete first-playthrough timings across unfamiliar players. If the finished draft is shorter but emotionally complete, revise the stated length. Do not add filler or puzzle friction to reach a duration target.

The six environment kits are dock/shore, Ruth's repair shop, kitchen/flat above the shop, boathouse/machine bay, tree/footpath/rise, and bus shelter/street. The two Alice viewpoints occupy C2S1 and C4S2. Count narration, optional text, UI, and local variants when exporting the actual translation workload; stage directions are translator context, not words players read.

Exclude free exploration of a large town, procedural memory generation, multiplayer, live events, elaborate crafting, and cinematic facial animation from this edition. Additions consume the same art and testing time needed to make the existing relationship convincing.

## 2. Technical recommendation

Use **Unity 6.3 LTS, C#, URP, and ink**, subject to a successful Android/iOS export in the first week. Unity lists 6.3 LTS support through December 2027. A fifteen-month schedule beginning near this plan's date puts release near that expiry and support beyond it, so migration to an appropriate supported release is a funded prerequisite for beta completion. Pin exact editor/package versions after the slice and maintain a separate upgrade branch. [Unity release support](https://unity.com/releases/unity-6/support).

Reserve **one person-month from the existing fourteen engineer person-months** for engine/SDK migration, dependency updates, save compatibility, and device validation; this is not an extra unpriced task. Regression coordination remains within the existing five producer/QA person-months and external QA allowance. At alpha, select and test a supported release against then-current Apple/Google submission requirements; beta cannot exit until signed mobile builds, narrative saves, reflection rendering, and the device matrix pass. If migration exceeds the reservation, revise the schedule and contingency openly before promising a release date.

URP supports mobile and desktop rendering; ink provides a maintained authoring workflow and an official Unity integration under the MIT license. These fit authored cameras, a small narrative state graph, and a writer who needs to test conversations separately from art. This is a project-specific recommendation, not a claim that another engine cannot work. [Unity URP overview](https://docs.unity3d.com/6000.0/Documentation/Manual/urp/urp-introduction.html), [inkle's ink tools](https://www.inklestudios.com/ink/).

Build the reflection as a controlled composition of two scene states, masked by water, rather than a physically accurate second world. Render only the active view and necessary reflected detail. Prefer baked lighting, restrained particles, and authored distortion. Keep a reduced-effects option with identical puzzle information.

Separate the narrative state, puzzle state, presentation, and save system. Every scene, line, choice, and asset needs a stable identifier. Save ink state and world state together at safe checkpoints using a versioned format; preserve a previous valid save. Chapter replay uses an isolated replay slot. It cannot silently replace the player's continuing playthrough.

Run automated checks for missing localization keys, unreachable scenes, absent assets, invalid saves, and availability of all endings. Keep signing keys and account credentials outside the repository. Put large source art/audio in managed large-file storage; record their licenses and owners alongside the asset register.

Reserve a Mac and physical iPhone early. Unity's local iOS workflow generates an Xcode project, then builds it on macOS; its cloud build option is an alternative, not a substitute for device testing. [Unity iOS build process](https://docs.unity3d.com/6000.3/Documentation/Manual/iphone-BuildProcess.html).

Unity Personal eligibility currently depends on revenue/funding below its $200,000 threshold; financing can affect eligibility before sales. Budget paid seats if applicable and confirm the terms for the actual studio. The Unity Runtime Fee was canceled. [Unity Personal](https://unity.com/products/unity-personal), [Unity pricing updates](https://unity.com/products/pricing-updates).

## 3. Initial asset envelope

These are estimating units. A background variant reuses geometry/composition but still requires painting, lighting, dressing, and QA.

| Asset group | Initial estimate | Reuse/control |
| --- | --- | --- |
| Environment sets | 6 | Shared geography across ages |
| Framed scene views | 24–30 | Approximately 4–5 per set |
| Additional era/weather treatments | 18–24 | Overlays and dressing; not new sets |
| Character designs | 5 principals, about 12 age/costume looks | Shared rigs where proportions permit |
| Animation clips | 35–50 reusable, 12–18 scene-specific | Posture and hands before lip sync |
| Interactive props | 45–60 | Include ledger, recorder, machine pieces |
| Substantial interaction packages | 12 | Each includes clues, assistance, audio, save state |
| Everyday gesture beats | 15–20 | Use existing objects and input grammar |
| UI families | 8 | Dialogue, ledger, pause, settings, recap, hints, chapters, credits |
| Sound effects | 100–140 edited cues/variants | Foley libraries plus signature recordings |
| Ambience | 12–18 loops/layers | Distinguish eras without relying on color |
| Score | 25–35 original minutes, reused in stems | Silence is an authored state |
| Marketing | 1 key art family, icon, 8 screenshots, 2 trailers | Actual game footage |

Each asset ticket records its scene IDs, owner, dependencies, estimated days, platform memory cost, and review state. A location is finished only when its interaction, audio, subtitles, accessibility presentation, and resume behavior work on a phone.

## 4. Prototype: the first 15–20 minutes

Allow six to eight weeks with an engineer, a part-time artist, and a writer/designer. This is included in the schedules below. Use temporary art except one representative dock shot and one polished transition; no final voice recording yet.

| Play time | Beat | What it must demonstrate |
| --- | --- | --- |
| 0–2 min | Adult Daniel tests an impossible reflection | Input and visual hook without a lore lecture |
| 2–6 min | First stone; Daniel meets Alice | Natural awkwardness and readable childhood framing |
| 6–10 min | An ordinary shared task | Humor, voluntary attention, Alice wanting something concrete |
| 10–16 min | Return to the changed location; solve a reflection interaction | Observe, align, release, then act in the present |
| 16–20 min | Quiet consequence and ledger entry | Emotional curiosity; reliable saving and return |

Test with ten unfamiliar players, including at least five regular phone players. Observe before explaining. Ask them to recount the timeline, Alice's immediate desire, what reflection can do, and what they want to discover. Obtain recording consent if sessions are recorded.

**Provisional team-set gates:** eight of ten understand the core rule and current era; seven identify an Alice desire unrelated to Daniel; eight finish with no more than one requested hint; seven voluntarily want to continue. These small-sample targets guide revisions, not market forecasts. Record contrary reactions instead of reducing the result to a pass percentage.

Technical gate: complete the slice on one lower-performance Android target and the oldest proposed iPhone target; no crash, corrupted save, or lost choice in interruption tests; readable largest text setting; stable 30 fps during the reflection after twenty minutes of play. Measure frame time, memory, and heat on physical devices. The device floor remains provisional until these results exist.

If comprehension fails, simplify the interaction. If attachment fails, rewrite the ordinary scene. If production time exceeds the estimate, reduce camera/animation coverage. Repeat the slice once before committing to the full asset order; do not solve a weak slice by commissioning more content.

## 5. People, ownership, and schedule

For the recommended small-team scenario, allow **36 person-months across approximately 15 months to launch and two months of support**, an average of 2.1 full-time equivalents across the full period. Reserve two engineer person-months for that support period; production staffing peaks higher. People may combine roles, but every decision still needs an owner.

| Responsibility | Effort allowance | Accountable for |
| --- | --- | --- |
| Lead engineer/technical artist | 14 person-months | Builds, reflection system, tools, saving, performance |
| Art director/environment and character artist | 11 | Style, assets, animation integration, shot consistency |
| Writer/narrative and puzzle designer | 6 | Script, scene goals, interaction design, read-through revisions |
| Producer/QA and release coordination | 5 | Schedule, integration reviews, test coverage, accounts, vendors |

Specialist audio, voice, localization, and external QA are additional purchased services. The artist cannot simultaneously produce every background and direct a full animation department. Outsource defined packages, not ambiguous requests to “make it cinematic.”

| Phase | Calendar allowance | Exit evidence |
| --- | --- | --- |
| Prototype | Months 1–2 | Slice gates; first measured task costs |
| Production slice | Months 3–4 | One chapter at representative quality; complete scene pipeline; observed scene timing ranges |
| Main production | Months 5–10 | All seven chapters assembled; weekly phone builds |
| Alpha and revision | Months 11–12 | Complete timed runs; story/puzzle revisions closed; supported engine/SDK migration selected and tested |
| Beta | Months 13–14 | Migration regression passed; localized content, device coverage, store packages, candidate builds |
| Release readiness | Month 15 | Approved submissions, launch assets, support capacity |
| Support | Months 16–17 | Critical fixes, save compatibility, support documentation |

Narrative lock precedes expensive recording and localization, while emotional testing starts with temporary performances. Environment blockout precedes detailed painting. Saving and interruption behavior begin in the prototype. Reserve release-readiness time; never treat store submission as the last afternoon of production.

A founder-led version should expect roughly **20–28 months and 30 person-months**, with narrower animation, selective voice, and limited launch languages. A mostly solo version can take **30–42+ months**, depending on experience and outsourced art; this is a capacity scenario, not a promise that a beginner can ship by that date.

## 6. Illustrative budget and cash decisions

The following budgets assume commercial ownership of commissioned assets and compensation for work. Loaded monthly labor includes salary/contract compensation and ordinary employer overhead. Rates are arbitrary planning inputs to replace with local quotes; no vendor quotes have been obtained or verified. The revised duration target does not reduce the unchanged 28-scene/twelve-interaction scope or these budgets without measured evidence.

| Scenario | Labor calculation | External services/tools | 20% contingency | Illustrative total |
| --- | --- | --- | --- | --- |
| Founder-led | 30 person-months × $4,000 = $120,000 | $30,000 | $30,000 | **$180,000** |
| Recommended small team | 36 × $6,000 = $216,000 | $54,000 | $54,000 | **$324,000** |

For the $54,000 external allowance, provision $14,000 for audio/music, $6,000 for selective voice, $10,000 for two translated text languages plus review, $8,000 for external QA/accessibility testing, $6,000 for devices/tools/build services, $6,000 for trailers/key art/launch services, and $4,000 for administration, contracts, and platform accounts. These are allocation placeholders, not statements that vendors will accept these prices.

The founder-led external allowance requires fewer localized words/languages, lighter performance coverage, and more internal production. Keep all three endings and both Alice viewpoints. Cut extra cameras, incidental characters, elaborate effects, or release languages first.

If a founder defers 18 months of their own $4,000 allowance, cash outlay falls by $72,000 but the labor cost remains. Do not present unpaid personal time as free production. Keep living expenses visible in the funding plan.

Full voice coverage, additional languages, a Steam edition, paid acquisition, financing costs, and unusually expensive regional employment/tax obligations require separate estimates. The eight-week support allocation above is included in labor; contingency covers overruns. Plan ongoing OS compatibility work as a later maintenance budget. A Steam version provisionally adds 2–4 person-months plus platform QA; validate that after desktop input testing.

## 7. Art, performance, and localization workflow

Approve a small visual bible before volume production: palette by era, material samples, camera rules, character silhouettes, water treatment, and a phone-size text test. Start with warm, inhabited spaces. Melancholy should come from what changed, not a permanent gray filter.

Stage acting around glance, distance, interruptions, and practical actions. Record table reads before animating conversations. For selective voice, record complete important scenes—opening, a relationship confrontation, final encounter/endings—rather than apparently random individual lines. Define this presentation honestly in marketing. Reconsider full voice only after measuring the value and obtaining quotes, including pickups and age-specific casting.

Give the composer a scene and silence map. Deliver separate music stems and sound categories with independent volume controls. The recorder, repair-shop bell, wood, and water need distinctive sounds. Every audio clue receives a visual equivalent; no player needs headphones to solve the story.

Prepare localization from the first slice: stable string IDs, no text baked into paintings, flexible subtitle boxes, font licensing, speaker/context notes, and marked ambiguous pronouns. Use human translators and in-context editing for humor and understatement. Choose launch languages after audience tests and quotes; English plus two text languages is the recommended-budget assumption, not a commitment to particular territories. Reserve time for text expansion, fonts, screenshots, and linguistic QA on devices.

Commission a focused review of the emergency scene and final fatal branch before recording. The purpose is believable staging and clear consequences, while preserving the story's tragedy and the player's agency.

## 8. Accessibility and QA acceptance

Ship adjustable subtitles and dialogue text, speaker names, opaque text backgrounds, a transcript, independent audio sliders, hold/toggle options, reduced motion/flashes, puzzle assistance, and untimed dialogue. Era identification uses composition, costume, text, and sound as well as color. Offer a concise content note with optional detail for bereavement, sudden death, and drowning imagery.

All endings must remain available with assistance enabled. Pausing, backgrounding, losing touch contact, or receiving a call must never select an ending or advance a danger timer. Test assistive input and screen-reader access to menus and text; do not advertise full blind accessibility unless the visual puzzle path has been designed and tested for it.

Budget physical coverage for at least three iPhone performance/screen tiers, four Android device/GPU combinations, and one tablet per mobile platform, using loans or a test service where appropriate. Exercise aspect ratios, safe areas, largest text, low storage, headphone removal, muted audio, offline launch, suspend/resume, process termination, update migration, and reinstall expectations. Clearly state that local-only saves are lost on uninstall unless a tested backup/sync path exists.

Maintain a scene-by-scene test matrix, plus a save immediately before every substantial interaction and ending decision. Release gates: no known progression blockers or save corruption; all endings reachable from a fresh run; no missing localized keys; complete playthroughs on minimum targets; repeatable interruption recovery; acceptable sustained performance; credited and licensed final assets. Track observed crash-free sessions without claiming statistical reliability from a tiny beta.

## 9. Store requirements checked on 22 September 2026

The producer owns a dated compliance sheet and rechecks it at beta and submission. A build SDK requirement is distinct from the oldest OS the game supports.

| Store | Current primary-source facts | Work to schedule |
| --- | --- | --- |
| Apple App Store | Developer Program: $99 USD annually, with regional pricing. Since 28 April 2026, uploads require Xcode 26 or later and the applicable iOS/iPadOS 26 SDK or later. [Enrollment](https://developer.apple.com/programs/enroll/), [requirements](https://developer.apple.com/news/upcoming-requirements/) | Enrollment, signing, paid-app agreements/banking, device testing, screenshots, privacy disclosure, accurate age questionnaire, review notes |
| Google Play | Registration: $25 USD once. New personal accounts created after 13 November 2023 need a closed test with at least 12 continuously opted-in testers for 14 days before applying for production access. [Account setup](https://support.google.com/googleplay/android-developer/answer/6112435?hl=en), [testing](https://support.google.com/googleplay/android-developer/answer/14151465?hl=en-GB) | Identity/device verification where applicable, signing, internal then closed testing, production-access application, listing, content rating and Data safety answers |
| Google Play technical | Since 31 August 2026, new phone apps/updates must target Android 16/API 36 or higher. Build and verify 16 KB page-size compatibility, including native dependencies. [Target API](https://support.google.com/googleplay/android-developer/answer/11926878?hl=en), [page-size guidance](https://developer.android.com/guide/practices/page-sizes) | Validate engine/native libraries and final bundle; recheck annual target changes and console deadlines |
| Steam, if funded | $100 USD per app; recoupable after $1,000 adjusted gross revenue. First titles have a 30-day fee waiting period and at least two weeks of public Coming Soon visibility. [Fee](https://partner.steamgames.com/doc/gettingstarted/appfee), [onboarding](https://partner.steamgames.com/doc/gettingstarted/onboarding) | Identity/tax/banking, content survey, store/build reviews, Windows input/resolution QA, store assets and support |

Commission depends on the actual agreements and region. Apple's enrolled Small Business Program offers 15% for qualifying developers, subject to its $1 million proceeds and associated-account rules. Google now distinguishes June 2026 regional arrangements from remaining markets; do not assume one universal rate. Model the exact launch markets before approving revenue assumptions. [Apple program](https://developer.apple.com/app-store/small-business-program/), [Google service fees](https://support.google.com/googleplay/android-developer/answer/112622?hl=en).

An offline game still needs accurate privacy information. Audit every included SDK and prepare a plain-language policy matching actual collection; avoid adding accounts or analytics without a demonstrated need. Apple's review rules require a privacy-policy link in metadata and within the app. [App Review Guidelines, privacy](https://developer.apple.com/app-store/review/guidelines/#privacy).

## 10. Positioning and release sequence

Treat **$7.99 mobile and $12.99 Steam** as testable US list-price hypotheses, with platform-specific regional pricing. They are not validated prices or revenue forecasts. Test the finished slice and store presentation with people who purchase narrative games; ask what they think they are buying before asking what they would pay. Keep content equivalent across editions.

Use net receipts after regional pricing, discounts, taxes, refunds, platform fees, and any publisher share when calculating cost recovery. Formula: development and support cost divided by average net receipt per paid copy. Do not multiply a headline price by an imagined audience and call it a business case.

After the slice, prepare a concise pitch and a ten-second reflection clip. Show Alice's humor and an ordinary task alongside the mystery. Marketing should communicate playable interaction and finite length. Keep the childhood reveal and the endings out of trailers. Clear the working title before paying for final branding.

Release in stages: private prototype tests; production-slice audience tests; closed Android testing and TestFlight beta; mobile launch after both platforms pass readiness; eight weeks of fixes and support; then reassess Steam using measured porting effort, audience interest, and available cash. TestFlight/external review and store approvals need buffer; do not announce a firm date before candidate builds are credible. A polished Steam demo can precede a later desktop release once that edition is funded.

## 11. Immediate backlog

| Order | Owner | Concrete result and acceptance |
| --- | --- | --- |
| 1 | Producer + leads | Scope, available hours, cash ceiling, and decision owners recorded |
| 2 | Engineer | Empty signed builds run on Android and iPhone; Windows build also opens |
| 3 | Writer/designer | Prototype script with scene/line IDs and one complete puzzle specification |
| 4 | Artist + engineer | One phone-readable dock composition and reflection transition |
| 5 | Engineer | Save/resume, transcript, text scaling, toggle input, and hint stub |
| 6 | Writer + audio | Temporary read-through and sound cues integrated into the slice |
| 7 | Producer | Ten external test sessions booked; questionnaire and observation sheet ready |
| 8 | Team | Slice tested; actual production days and revisions logged |
| 9 | Producer + leads | Revised asset forecast, vendor quotes, and funded next milestone |

**Next commitment:** fund and build the slice. Full production begins only when the team has evidence that the relationship, the reflection mechanic, and the mobile production pipeline work together.
