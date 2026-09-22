# What the Water Keeps
## Complete screenplay development draft · Chapters 2–5 · Version 1.1

**Draft status:** Complete authored draft for table reading and prototyping. Scene IDs and required events are fixed; performance and interaction durations need playtesting.

**Reading key:** Character names introduce dialogue. P-numbers identify interactions. Choice flags record local responses and never affect ending availability. Unchosen replies do not play. Crowd sounds add no scripted speaking roles. Recorded speech receives subtitles and transcripts.

---

## Chapter 2 — Things Worth Keeping

### C2S1 — Effects department

**Time / viewpoint:** Alice, thirteen. Daniel is absent. Objective scene.

**Location:** Kitchen above Ruth's shop, borrowed for an afternoon while Mara sorts boxes from their move. Their own home remains offscreen.

A portable recorder lies between two mugs. Alice holds a spoon above a baking tray. Mara, seventeen, writes an address on a parcel.

ALICE: Don't breathe for a second.

Mara lets the strip of parcel tape hang from her fingers. She waits.

ALICE: It's for the spaceship.

MARA: Ready.

Alice drops the spoon. A disappointingly small clink.

ALICE: Small spaceship.

Mara puts down her pen. She bends the tray gently. It makes a low, elastic boom. Alice looks at her.

MARA: Our old oven did that. Every time I wanted something cooked evenly.

**P03: Record three sound takes and arrange their slates.** Alice records the tray, a wet glass rim, and paper shaken beside the microphone. Each has a named visual source and a waveform; hearing pitch is unnecessary. The slate must precede its matching effect. The player can audition freely. No quality score.

ALICE [tray slate]: Engine. Take two. Better engine.

ALICE [glass slate]: Unfriendly planet.

MARA: You haven't met it.

ALICE: It's making that noise.

ALICE [paper slate]: Rain. Indoors. Don't tell anyone.

If an effect precedes its slate, Alice listens to the whole pair, then says:

ALICE: Name first. Otherwise future me has to guess.

On completion, the three sounds make a modest, convincing little journey. Mara stops addressing the parcel to listen.

MARA: Oh. That's good.

ALICE: You sound surprised.

MARA: I didn't know what you were making.

ALICE: There's meant to be a landing. At the end.

Mara leans closer to the speaker. Alice leaves it playing, pleased without having to ask again.

Mara reaches for a box marked SCHOOL. Alice turns it away with her foot.

MARA: They've sent your timetable.

ALICE: Put it with the bad news.

MARA: There's a music room. And a bus that stops outside.

ALICE: Are we definitely staying this time?

Mara takes a moment before answering.

MARA: Yes. Mum's signed the lease. I've got the shifts. We're staying.

ALICE: All right.

She lets Mara open the box.

**Local choice C2S1_REPLY:** “Play it again” sets `c2s1_replayed`; “Save it” sets `c2s1_saved`.

If replay:

ALICE: Listen to the landing this time.

MARA: I heard the landing.

ALICE: You were doing an address.

If save:

ALICE: I'll do the voices later.

MARA: I can do someone very tired.

**Reconverge:** Alice names the recording `SPACE FILM — NO FILM YET`. Mara passes her the timetable, right way up.

### C2S2 — Official distance

**Time / viewpoint:** Daniel, thirteen, later that summer.

**Location:** Measuring tree, footpath, and rise above the dock.

Jonah holds the end of a cloth tape beside a notch in the tree. Daniel squats beside another mark. Alice examines three stones as if buying fruit.

JONAH: That one counts.

DANIEL: It hit the fence.

JONAH: After travelling.

ALICE: He's got you there.

**P04: Measure a cooperative throw.** Daniel and Jonah stretch the tape between the tree's marked starting point and each landing marker. Alice throws toward the empty beach, away from people. The player aligns the tape ends and writes the distance. No aiming challenge or performance rank. Larger text gives the same readings as the tape.

For a slack tape:

JONAH: Pull your end. Unless you're measuring the hill as well.

For a displaced start:

ALICE: From the tree. That was the whole treaty.

On the first correctly measured throw:

DANIEL: Fourteen metres, twenty.

ALICE: Write fifteen.

DANIEL: Why?

ALICE: Looks friendlier.

Daniel writes the actual distance. Alice peers over his shoulder.

ALICE: You've got handwriting like a receipt.

DANIEL: Thank you.

JONAH: Was it a compliment?

DANIEL: I'm taking it.

Alice offers Daniel the last stone. He weighs it, then sets the notebook down. His throw lands much closer.

ALICE: Plenty of room to improve.

DANIEL: That's what I was leaving.

Jonah measures it without comment. He nudges the marker closer to the correct landing spot when Alice, trying to help, puts it too far away.

DANIEL: Just one more.

Alice looks for another flat stone. Say the line as an ordinary request to continue the game; the finale will reuse this exact recording, without a sinister new performance.

**Optional inspection — tangled tape; single-use, no narrative-choice flag or reward.** Before the call from Ruth, inspecting the tape plays:

ALICE: You've stood on it.

DANIEL: Oh.

He lifts his foot. They try winding from opposite ends, stop, and pass one end back. Jonah waits with a hand out for the case.

JONAH: I'll hold it. You turn.

They finish together. This can be staged with the tape prop and held character poses; no special animation is required for the text prototype.

Ruth appears on the rise with a tea towel over her shoulder. She waves once, firmly.

RUTH: Food!

JONAH: What kind?

RUTH: The disappearing kind!

Jonah runs. Alice follows, then doubles back for Daniel's notebook. She tosses it to him at ordinary catching distance.

ALICE: Evidence.

They run uphill. Hold briefly on the tree notch, the tape's metal end, and the iron footing beside the rise. These are practical objects, not ominous inserts.

### C2S3 — Something to collect

**Time / viewpoint:** Daniel, thirty-four. The final evening continues.

**Location:** Repair shop.

Mara tries the door, finds it unlocked, and enters wearing her transport-work jacket. Daniel clears a stool by lifting three things together. One immediately slides back.

MARA: I've only got twenty minutes.

DANIEL: Tea?

MARA: Nineteen if you make it.

He puts the kettle on.

MARA: Have you found the recorder?

DANIEL: Yes.

MARA: Good.

He doesn't fetch it. She looks toward the back bench.

DANIEL: I'm using the original levels. As a reference.

MARA: You said you needed the files.

DANIEL: I do. There are copies.

MARA: Then keep the copies.

Daniel reaches for a drawer and stops at a cable attached to it. Mara takes off her jacket. She has realised this will take longer.

MARA: Alice died twelve years ago, Dan. You can finish cleaning a microphone socket.

The kettle clicks. Neither rushes to fill the silence.

DANIEL: It's fixed.

MARA: I know. You fixed it straight away.

**Local choice C2S3_REPLY:** “I should have returned it” sets `c2s3_acknowledged`; “What do you need it for?” sets `c2s3_asked_use`.

If acknowledgment:

DANIEL: I should have returned it.

MARA: Yes.

DANIEL: I'll get the case.

If question:

DANIEL: What do you need it for?

MARA: Mum's telling me about the move. Apparently I've had the boxes wrong all this time.

DANIEL: You've started?

MARA: On my phone. I'd like to use mine.

DANIEL: You don't.

**Reconverge:** Daniel opens the wrong drawer, then the right one. The case contains an old service slip. Mara moves the case to the counter to make room for the recorder; this is the case she will leave behind, not the device itself.

DANIEL: Let me check which card goes with it.

MARA: I'll be here.

She sits. From outside: the winch rattles, then Jonah knocks twice on the window. Daniel points toward the back and raises one finger. Mara pours her own tea.

### C2S4 — Brake on

**Time / viewpoint:** Daniel, thirty-four, minutes later.

**Location:** Boathouse / machine bay.

Jonah stands beside a winch. The suspended receiver is secured just above a padded cradle. He has brought a replacement brake shoe and a sandwich wrapped in paper.

JONAH: Which one do you want first?

DANIEL: The brake.

JONAH: Fair enough. Sandwich after.

He puts the sandwich on a clean shelf, away from the equipment.

**P05: Compare the guide, then seat the receiver.** From the open shore-facing bay, Daniel views the boathouse guide plate in an earlier lake reflection. The earlier bay is empty; no new person or location is introduced. Its painted arrow appears useful, but the fixed structural notch reveals that the present replacement plate faces the other way. This is an authored temporal comparison, not a claim that old instructions are automatically correct.

DANIEL: The arrow was on this side.

JONAH: I replaced the plate. Turned it round to fit the bracket.

DANIEL: So that arrow—

JONAH: Is the old one. Go by the notch.

The player releases the reflection and matches the current guide to the notch, then completes the labelled, abstract load-and-brake sequence. Inspect the brake, take the load, release the transport catch, lower into the cradle, reapply the brake. Each step has a tactile label and visual state. Incorrect input does not release the load; Jonah keeps the safety line secured. The comparison replaces repeated instruction cards within this scene's existing timing allowance; it is not an additional puzzle slot or real equipment-training procedure.

JONAH [if brake not checked]: Look at the shoe before you put weight on it.

JONAH [at load transfer]: There. Now the catch is free.

DANIEL [receiver seated]: Brake on.

JONAH: And hands out.

They step back. Nothing dramatic happens. The receiver is simply in place.

DANIEL: That sounds better.

Jonah checks the new brake once under weight, then lets go.

JONAH: It is better.

Jonah rubs grease off one finger and checks his phone.

JONAH: I can stay for the test. Then I've got to go.

DANIEL: Tonight?

JONAH: Yes, tonight. Bath, bed, argument about which cup water comes in.

DANIEL: How many cups?

JONAH: Two. I'm meant to bring the blue one back. It's in the van.

Daniel smiles, properly. Jonah sees the sandwich untouched.

JONAH: Half now. Other half when you remember people need food.

Daniel unwraps it.

DANIEL: What is it?

JONAH: The disappearing kind.

They both recognise Ruth's line. Jonah picks up the old brake shoe before either has to explain.

---

## Chapter 3 — Room for Two

### C3S1 — Missing the bus

**Time / viewpoint:** Daniel, eighteen.

**Location:** Bus shelter / street, after rain.

Alice holds two takeaway cartons. Daniel holds her recorder inside his jacket to keep it dry. The shelter roof drips in a pattern just behind his neck.

ALICE: You're being rained on indoors.

DANIEL: I know.

She shifts along. He sits beside her.

ALICE: Mine's too hot. Swap.

DANIEL: They're the same thing.

ALICE: Just try mine.

They exchange cartons. She takes a bite, immediately regrets it, and manages a dignified nod.

DANIEL: Same?

She nods, gives back his carton, and laughs at herself. He shifts his jacket so her recorder stays dry between them.

The bus time changes on the display: DUE becomes 6 MIN.

DANIEL: Mara'll be pleased.

ALICE: She's off today. This is someone else's failure.

A comfortable pause. Daniel hands back the recorder. Their fingers meet. Alice keeps her hand there a moment.

ALICE: Was this a date?

DANIEL: I was hoping you hadn't already decided.

ALICE: That's a terrible answer.

DANIEL: Yes. I'd like it to be.

**Local choice C3S1_REPLY:** “Ask to kiss her” sets `c3s1_kiss`; “Take her hand” sets `c3s1_hand`. Both begin the same relationship.

If kiss:

DANIEL: Can I kiss you?

ALICE: Put the curry down first.

He does. She leans in. The kiss is brief, a little awkward, then less awkward.

If hand:

Daniel offers his open hand between them. Alice puts hers in it.

ALICE: You've got sauce on your thumb.

DANIEL: It's a very complete evening.

She wipes his thumb with her napkin, then kisses him.

**Reconverge:** A bus passes. They both look up too late.

ALICE: Was that ours?

DANIEL: I think so.

She settles against him.

ALICE: Tragic.

### C3S2 — The owner's name

**Time / viewpoint:** Daniel, thirty-four.

**Location:** Repair shop.

Mara has emptied her tea. The recorder, ledger, and service slip lie on the counter. Daniel plugs ordinary headphones into the recorder, then disconnects them so both can listen through its speaker.

DANIEL: Fourteenth of June. Alice's recorder. That's what I've got.

MARA: Look underneath.

An inscription: **Mara. Red button. A.**

MARA: She gave it to me when she bought the new one. For the job.

DANIEL: I remember the new one.

MARA: You should. She told everyone what it cost.

**P06: Reconcile the service record.** Compare the ledger entry, the original service slip, and the ownership inscription. The slip reads **12 JUNE / MIC SOCKET**. The ledger reads **14 JUNE / ALICE / RECORDER**. Correct the intake date to the twelfth and the owner to Mara. Retain the original entry legibly; do not erase it.

DANIEL [examining date]: Fourteenth was when I finished it.

MARA: The day you called.

DANIEL: I copied the old owner across.

MARA: It still works like that at the depot. Change one number, suddenly the bus belongs to someone in another county.

If the player selects Alice as owner again:

MARA: It started with her. She gave it to me.

On correction, Daniel closes the service entry with **RETURNED TO OWNER**. He passes the recorder across. **The handover is unconditional and occurs here.** Mara has the device for the remainder of the scene. The empty case stays on the counter.

She finds one old file while checking the controls.

MARA: Is this the fundraiser?

RECORDED ALICE, eighteen: Wait. Don't start yet. Jonah's got—

A crash, followed by Alice laughing. Mara laughs with the recording.

DANIEL: There's a clean take.

MARA: She used this one.

DANIEL: Did she?

MARA: It got everyone to look up.

Daniel checks his copied file list: **PERFECT TAKE**. He changes its label to **FUNDRAISER — USED TAKE**.

DANIEL: All right.

Mara puts the recorder into her bag without its case and fastens the bag.

If the player chose acknowledgment rather than asking its use in C2S3, play this line here so every path gives Mara a purpose beyond collection:

MARA: Mum's telling me about our old house. I started on my phone. This'll be better.

Daniel nods. He does not ask for a copy. Their mother remains offscreen; this is an ordinary family project, with no new illness or loss implied.

MARA: Come round Sunday. I've got a shelf that seems confident until you put anything on it.

DANIEL: Send a photo.

MARA: I'll send the shelf a photo of you. See if that helps.

She leaves. The door catches; she knows to lift it.

### C3S3 — Three things at once

**Time / viewpoint:** Daniel, eighteen.

**Location:** Repair shop opening onto the dock. A small fundraiser for repairs to public jetty access; incidental visitors remain background.

Ruth sorts coins into an old biscuit tin. Mara checks the evening bus timetable. Jonah carries too many enamel mugs. Alice crouches beside two modest speakers.

RUTH: Prices are on the cards, Daniel.

DANIEL: I know.

RUTH: Then stop giving change from a different price.

DANIEL: It was a child.

RUTH: So are half the customers. That's why everything's cheap.

Alice waves him over.

ALICE: Tell me if you can hear the words from there.

DANIEL: Which words?

ALICE: The announcement. Stand by the door?

She presses record.

ALICE: Wait. Don't start yet. Jonah's got—

The mugs fall onto a tray. A spectacular crash; nothing breaks. Alice laughs before reaching to help.

JONAH: They're fine.

RUTH: Are you?

JONAH: Less fine.

**P07: Build an intelligible three-layer playback mix.** Daniel balances Alice's announcement, the recorded water, and a simple rhythm Alice made from workshop taps. Captions explicitly show whether speech is clear or masked. The mix is accepted across a broad range once the announcement remains intelligible; there is no single “artistic” solution.

ALICE [playback announcement]: We're raising money to repair the lower jetty. The cakes have prices. The broken radio is a demonstration, unless someone makes Ruth a very good offer.

RUTH: It's a very good radio.

ALICE: It will be.

If speech is masked:

MARA: I can hear weather. Not money.

If only speech remains:

ALICE: A bit of the water back in. Otherwise I sound like the bus station.

MARA: Careful.

On completion, the recorded crash attracts several glances. The announcement follows clearly. A visitor places money in the tin.

ALICE [quietly, to Daniel]: Keep that take.

DANIEL: With the mugs?

ALICE: Especially the mugs.

Jonah bows. Ruth hands him the broom.

RUTH: Thanks.

Mara folds the timetable.

MARA: Last bus in twenty. Anyone who needs it, start saying goodbye now.

Alice leans against Daniel while checking her recording. He rests his chin briefly on her hair. Then Ruth passes him a tray, and they both get back to work.

### C3S4 — Breakfast furniture

**Time / viewpoint:** Daniel, twenty-two. The last day, morning.

**Location:** Kitchen above the shop.

Alice draws a rectangle on the back of an envelope. Daniel puts two plates down, avoiding the pencil.

ALICE: Bed here.

DANIEL: Door opens into it.

She redraws the door opening outward.

DANIEL: That's not how doors work.

ALICE: We haven't signed anything. They could improve.

He turns the envelope. A letting agent's measurements show a small flat near her work.

DANIEL: Bed there. Table folds down.

ALICE: Where do your tools go?

DANIEL: Under the bed.

ALICE: Mine too?

DANIEL: We may have to buy a taller bed.

She takes his toast instead of her own. He notices, looks at the plates, and accepts the exchange.

ALICE: Sorry. Did you want that one?

DANIEL: You can have it.

She puts the larger half back on his plate anyway. Leave the small action unremarked.

ALICE: Trial month. We can admit it if it's awful.

DANIEL: The flat or us?

ALICE: Ideally the flat.

He reaches for his work ledger, left open beside the telephone.

DANIEL: There's a pressure gauge I said I'd look at.

ALICE: Today?

DANIEL: I said this week.

He reads the entry, considers it, and closes the book.

DANIEL: Tomorrow. I'll call him after breakfast.

ALICE: Thank you.

He puts the book beside the phone, where he will remember the call.

She kisses the corner of his mouth.

ALICE: I'm going down for a recording before the wind gets up. Back for lunch.

DANIEL: I'll get bread.

ALICE: The good one. If they've got it.

He passes her the clean tea towel. She wipes a little butter from his sleeve before giving it back.

---

## Chapter 4 — The Distance Between

### C4S1 — Ten seconds

**Time / viewpoint:** Daniel, thirty-four.

**Location:** Boathouse / machine bay, at the shallow shore opening.

Daniel places a marked washer against a source mark just beneath the water. Jonah keeps the disconnect within reach. The full contact assembly remains isolated.

JONAH: Say the test again.

DANIEL: Tap, observe, return. Repeat the tap. Erase that one trace.

JONAH: And you stay here.

DANIEL: I stay here.

**P08: Observe, repeat, return, erase.** Daniel taps the washer once. Its local impression is visible in the lake reflection. The player observes it, returns to the present, and runs its bounded repeat. A visible repeat indicator shows the same finite tap restarting. The actual washer remains still.

JONAH: I've stopped touching it.

DANIEL: It's reading what happened.

JONAH: And that setting keeps it happening?

DANIEL: Keeps playing that piece. It doesn't change this one.

Daniel touches the physical washer. Its position has not changed.

A short sensation test follows automatically under supervision. Jonah taps Daniel's wrist. The UI shows present contact and Daniel's delayed response side by side. No pain or restraint.

JONAH: Feel that?

DANIEL: No.

Jonah opens the return control. Daniel looks down.

DANIEL: Now.

JONAH: That's four seconds you didn't know someone was touching you.

DANIEL: Yes.

JONAH: Put it on the board. Big letters.

Daniel writes: **BODY SIGNALS CAN ARRIVE LATE. RETURN BEFORE LOSS OF CONTROL.**

For the final test, the player aligns only the washer's small source trace and confirms erasure. The tap disappears permanently from the receiver's index. An explicit notice states **THIS TRACE CANNOT BE RECOVERED** before confirmation.

JONAH: Do it again.

Daniel selects the old trace. Nothing appears.

DANIEL: That tap's gone. I'd have to make a new one.

JONAH: But the washer's still a washer.

DANIEL: Yes.

Jonah retrieves it and puts it on the bench. Daniel marks the erased test in the ledger; there is no undo control. Ordinary recordings and objects remain intact.

### C4S2 — The offer

**Time / viewpoint:** Alice, twenty-one. Daniel is absent. Objective scene.

**Location:** Bus shelter / street. Late summer; Mara is between shifts.

Alice has an application open on her phone. Mara eats from a lunch box balanced on a timetable folder.

ALICE: “Describe your relevant professional experience.”

MARA: Recording things.

ALICE: I was hoping for longer.

MARA: Recording things for several years.

Alice shows her the screen: a seven-week sound-assistant position away from Greyford. The offer is conditional only on accepting the stated dates.

ALICE: They liked the room recordings. The repair shop ones.

MARA: Those are good.

ALICE: The fan's in most of them.

MARA: They liked them with the fan.

**P09: Review and accept the job.** Alice compares the start date, pay, travel cost, and first accommodation payment. Work begins in nine days. She chooses the cheaper bus the evening before and allocates the stated advance to lodging; the displayed budget works. No mental arithmetic is required. Completion always accepts the opportunity. This is planning her chosen life, not deciding whether she deserves one.

ALICE [examining travel]: Earlier bus. Changes twice.

MARA: Once. That second line's the arrival platform.

Alice checks the column heading, then the fare. She turns her phone slightly away.

ALICE: I can do the sound. Apparently getting there is harder.

Mara turns the timetable folder so both can see. She marks the connection with the back of her pen, without taking the phone away from Alice.

Alice reaches the acceptance screen but lowers the phone.

MARA: What's the snag?

ALICE: Daniel thinks I'm doing the autumn bookings here.

MARA: Did you say you were?

ALICE: I said I'd see.

MARA: Have you told him what you've seen?

ALICE: I wanted it to be real first.

Mara looks at the offer, then back at her.

ALICE: I know.

**Local choice C4S2_REPLY:** “I want the work” sets `c4s2_work`; “I'm scared I'll be bad at it” sets `c4s2_nerves`.

If work:

ALICE: I want to find out what it's like when this is the whole day.

MARA: Then go and do the whole day.

If nerves:

ALICE: Here, everyone knows me. There, I could just be bad.

MARA: Then you'll know what to get better at.

**Reconverge:** Alice accepts. Confirmation stays onscreen long enough to read.

ALICE: Done.

MARA: Eat something.

Alice takes a piece from Mara's lunch box.

MARA: Didn't necessarily mean mine.

### C4S3 — Whose box

**Time / viewpoint:** Daniel, twenty-one, several days later.

**Location:** Kitchen / flat above the shop. Alice is packing equipment she has stored there.

Daniel comes upstairs carrying two spare shelves. Alice is wrapping her microphone stand.

DANIEL: I thought we could put these over the desk.

ALICE: Don't drill anything yet.

He notices the travel bag.

DANIEL: When did you hear?

ALICE: A few days ago.

DANIEL: How many?

ALICE: Four.

He puts the shelves down carefully.

DANIEL: You leave in five days.

ALICE: Yes.

DANIEL: You let me keep talking about September.

ALICE: I know. I should have told you.

**P10: Sort belongings into individual, shared, and deferred boxes.** Daniel packs only items both have identified. Alice's recording equipment belongs to her; his tools belong to him. Their jointly bought kitchen things may be agreed or deferred. Uncertainty has a legitimate box. The puzzle never awards points for giving away everything.

If Alice's equipment goes into the shared box:

ALICE: That's mine, Dan. We both use it, but it's mine.

DANIEL: Right.

If their kettle is deferred:

DANIEL: Kettle later?

ALICE: Please. I can't argue about a kettle as well.

On completion, Alice reaches for a roll of tape. Daniel hands it over.

DANIEL: I booked you for three weekends at the hall.

ALICE: Without asking me.

DANIEL: You said we needed the money.

ALICE: We do. That wasn't permission to book me.

**Local choice C4S3_REPLY:** “I thought it helped” sets `c4s3_help`; “I should have asked” sets `c4s3_ask`.

If help:

DANIEL: I thought I was helping.

ALICE: You were doing a lot. It's not the same as asking.

DANIEL: All right. I'll call them.

If acknowledgment:

DANIEL: I should have asked you first.

ALICE: Yes.

DANIEL: I'll call them.

**Reconverge:** Alice tears a piece of tape badly, folds it back, and starts again.

ALICE: I kept waiting for a way to tell you where you wouldn't be upset.

DANIEL: There isn't one.

ALICE: No. I made it worse.

He sits on the edge of the table.

DANIEL: Do you want me there?

ALICE: Visiting? Yes. Coming because you think I can't go alone? No.

DANIEL: I didn't say that.

ALICE: I know. I'm answering three arguments ahead. Sorry.

She sits opposite him. The packed bag remains between their feet. They have not solved everything. He pulls the tape's edge free for her.

### C4S4 — Two timetables

**Time / viewpoint:** Daniel, twenty-two, weeks before the last day.

**Location:** Bus shelter / street.

Alice steps off an arriving bus. Daniel waits with two cartons from the same takeaway. She looks at them, then him.

ALICE: Still hot?

DANIEL: Dangerously.

They hug. She keeps hold for a moment longer than he expects.

At the shelter she opens a carton. Daniel puts a folded bus timetable beside it.

DANIEL: I had something sensible prepared.

ALICE: Go on.

DANIEL: It's gone.

ALICE: I've got something stupid prepared. Could start there.

DANIEL: All right.

ALICE: I miss coming in without explaining where everything goes.

DANIEL: You keep moving everything.

ALICE: Only the things you put in the wrong place.

He laughs. Alice pushes the carton toward him so he can take the piece he has been looking at. They eat before Daniel returns to the timetable.

**Optional inspection — her equipment bag; single-use, no narrative-choice flag or reward.** Before the next conversation, selecting the worn bag plays:

DANIEL: How's the work?

ALICE: Yesterday? Awful. I used the wrong name all morning. Nobody told me until lunch.

DANIEL: For who?

ALICE: The person whose name is on the van.

He winces with her.

ALICE: The recording was good, though. They used it.

DANIEL: Good.

She nods. She can have a bad day and still want the job. If skipped, return directly to the timetable without summarizing this exchange.

DANIEL: I don't want you to come home because I can't work out how to leave.

ALICE: I don't want to keep important news until it's a fact you have to deal with.

DANIEL: I missed you. I was also angry.

ALICE: Both allowed.

DANIEL: What do you want now?

ALICE: Another contract. A place with a door on the bedroom. You, if we can stop making your choices and my choices into a contest.

She finds the flat listing on her phone. He unfolds the timetable fully: workdays, travel, a proposed arrangement for his local customers.

ALICE: You've made a timetable.

DANIEL: A proposal. You can draw on it.

She takes his pencil.

ALICE: Two nights here, not three. Otherwise we'll live together by post.

DANIEL: Two. I'll ask Jonah about covering collections.

ALICE: Ask.

DANIEL: Yes. Actual asking.

She writes **ONE MONTH FIRST** beside the listing.

ALICE: And we review it when we've actually tried it.

He nods. They eat. Her knee rests against his. The next bus arrives; this time neither needs it.

---

## Chapter 5 — The Ordinary Afternoon

### C5S1 — Eight o'clock

**Time / viewpoint:** Daniel, thirty-four. Later on the final evening.

**Location:** Boathouse / machine bay.

Jonah checks the disconnect is open. Daniel is at a dry bench, comparing source diagrams. The equipment in the water is quiet.

JONAH: That's me.

DANIEL: There's another alignment—

JONAH: Tomorrow.

Daniel looks up. Jonah has already put on his coat.

JONAH: I said I'd help with the winch and the test. I did.

DANIEL: You did.

JONAH: I'm meant to do bedtime. I said I'd be there.

DANIEL: All right.

Jonah looks toward the water.

JONAH: You didn't feel my hand for four seconds. Don't do a live connection alone.

DANIEL: There's a return control.

JONAH: Then use it. Before you need someone else to use it.

Jonah picks up his bag, then remembers the practical thing he came in meaning to say.

JONAH: The hall called me again. About the amplifier.

DANIEL: It's finished.

JONAH: They need a collection time. I can't keep taking your calls.

DANIEL: I'll answer them.

JONAH: Tonight.

DANIEL: Tonight.

Daniel rests his pencil beside the diagram.

DANIEL: Thank you for coming.

JONAH: All right.

They share a tired smile.

JONAH: I'll call at eight. If you don't answer, I'm coming down.

DANIEL: I'll answer.

JONAH: Don't put the phone under something.

Daniel moves it onto the clear end of the bench while Jonah is still there.

He leaves. Daniel hears his footsteps recede along the path. The player may inspect the dry diagram before continuing. The live switch remains open until the later preparation scene; no hidden countdown starts here.

### C5S2 — Lunch

**Time / viewpoint:** Daniel, twenty-two. The last day, afternoon.

**Location:** Kitchen above the shop.

The bread is on the table. Alice has returned from the shore. Her recorder sits near her jacket. The flat diagram has acquired a stain from a mug.

ALICE: Now there's a lake in the bedroom.

DANIEL: Premium feature.

She turns the envelope over and begins again.

DANIEL: I called about the gauge. Tomorrow's fine.

ALICE: Good.

She tears bread for both plates. Daniel slides the butter within her reach. Their bodies know where to make room for each other.

She reaches under his shirt collar and removes a short piece of thread.

She drops the thread beside her plate and continues eating. Do not find a joke for the gesture.

They start lunch. Ordinary cutlery and distant traffic. No anticipatory heartbeat, distorted lake reflection, or musical warning.

ALICE: Did Jonah say he'd help move?

DANIEL: If we feed him.

ALICE: I'll make enough.

Daniel reaches for the butter. Alice points toward the other side of the table.

ALICE: Could you pass me the—

Her sentence stops. Her hand drops. Daniel catches her as she slips sideways. His plate overturns.

DANIEL: Alice?

He lowers her to the floor, reaches for the phone, and calls emergency services promptly. Keep the framing with his face and the overturned chair; do not turn her body into spectacle.

DANIEL [into phone]: I need an ambulance. She's collapsed. She's not responding. The repair shop by the lower jetty. Upstairs.

**No player prompt, timer, selectable response, or rescue challenge.** Cut on the call connecting to help. Professional responders' unsuccessful resuscitation occurs across the cut, conveyed without an instructional sequence.

Later: two responders leave the flat. One pauses beside Daniel, who has already heard the outcome. No unheard message is saved for a reveal. He sits at the table. The spare chair is upright again.

Mara arrives. He stands too quickly and cannot find a sentence. She understands his face.

MARA: Where is she?

Daniel cannot point immediately. Mara puts her bag down and stays beside him. Let their breathing and the room carry the scene. End before explanation becomes a speech.

### C5S3 — Zero hours

**Time / viewpoint:** Daniel, thirty-four.

**Location:** Kitchen above the shop, present.

The room has changed through use: a different table, a repaired cupboard, one wall painted incompletely behind a shelf. It has not been preserved as the room from the death scene.

Daniel brings up the uneaten half sandwich. He sits and eats several bites before opening a drawer for an old shoreline survey.

He finds a card in Ruth's writing: **RETIREMENT HOURS: ZERO. ASK DANIEL.** Below, smaller: **Except when he does it wrong.**

Beside it is an ordinary photograph of Ruth in a raincoat on a trip after retirement. Do not animate it. Daniel smiles at something just outside its frame.

An open ledger establishes that Ruth died when he was twenty-nine. Its entry is practical and spare: **Mum died. Shop closed this week. Jonah has the keys.** No second death scene, voice, or medical mystery follows.

His phone lights: a message from Mara, sent after getting home.

MARA [text]: Recorder works. Shelf still doesn't. Sunday, one-ish.

**Local choice C5S3_REPLY:** “I'll bring the drill” sets `c5s3_drill`; “I'll bring lunch” sets `c5s3_lunch`. These are fictional in-game messages, selected without opening another application.

If drill:

DANIEL [typed]: I'll bring the drill.

MARA [text]: Excellent. Bring yourself as well.

If lunch:

DANIEL [typed]: I'll bring lunch.

MARA [text]: The shelf won't eat much.

**Reconverge:** Another message is already waiting: **HALL: Is ten tomorrow still possible?** An amplifier with a completed repair tag was visible downstairs; this is a customer reply, not a new puzzle.

Daniel types: **Yes. Front door. Sorry I didn't get back to you.**

He sends it and puts the phone face up. This action happens on every route and never grants an ending. The small commitment remains something the ending can honor or leave unmet.

He finishes the sandwich. Under the retirement card is the survey he came for: dock, tree, rise. He takes that sheet downstairs, leaving the photograph and card together.

### C5S4 — Three fixed points

**Time / viewpoint:** Daniel, thirty-four.

**Location:** Dock / shore and the connected tree / footpath / rise kit. Full night.

Daniel lays Ruth's old shoreline survey beside the receiver. Three source positions require verification. Each matches a physical feature already seen in another year.

**P11: Align the three shoreline anchors.** The player visits the dock bolt beside the split plank, the measuring tree's old metal tape marker, and the iron footing on the rise. At each, inspect the physical mark and align its corresponding archived view through the receiver at the lake's shore. The lake carries the impressions; the tree, paper survey, and ordinary objects do not gain powers.

The matching criterion is position, not emotional significance. A large-print survey and clear shape labels provide the same information as the visual alignment. No colour-only distinctions. Each alignment locks independently and is retained on save.

At the dock:

DANIEL: New board. Same bolt.

The reflection shows the older plank around the unmoved fixing. No person appears in this technical inspection.

At the tree:

DANIEL: Marker's grown into it.

He brushes loose dirt from the visible metal, without cutting into the bark. The survey's starting line matches the position used for the childhood throws.

At the rise:

DANIEL: There you are.

Grass obscures part of the footing. He moves it aside; the receiver and survey agree.

For a mismatch at any station:

DANIEL: Wrong edge. Start from the fixed point.

With all three aligned, the source diagram closes into one connected shape. It is a technical success, quietly presented. Previously isolated fragments now share an addressable source. The receiver identifies a final recorded shore visit by Alice at twenty-two, on the morning already shown at breakfast.

Daniel looks toward the boathouse. He folds the survey along its old creases and puts it away.

DANIEL: Morning first.

He selects the indexed visit. Cut to C6S1 before its content begins.

---

## Continuity and implementation locks

- Alice's two objective viewpoint scenes are C2S1 and C4S2. All other scenes in this file are framed with Daniel. The past scenes are authored narrative, not claims that Daniel remembers unobserved events.
- Alice's childhood recorder later becomes Mara's gift when Alice upgrades at twenty-one. Its old files include the fundraiser at eighteen. Daniel receives it for repair at twenty-two; the incorrect service entry combines completion date with an outdated owner. He returns it in C3S2, with no later physical reappearance in his possession. C6 uses a lake impression, not a secretly retained recorder.
- The fundraiser's flawed take belongs to ordinary evidence of Alice's editorial choice. Mara's correction does not invalidate Daniel's love or make her an infallible authority on all memories.
- P08 destroys only the washer-tap trace. The washer, other traces, and ordinary recordings survive. This teaches the later erasure operation without executing it prematurely.
- Alice accepts the out-of-town job in every version. The couple's conflict and reconciliation occur regardless of local wording. Daniel is present at the last lunch in every version.
- The collapse is biological and sudden, not caused by the lake, an argument, or a missed player action. Later medical uncertainty must not introduce a hidden murder, preventable puzzle solution, or supernatural cause.
- Jonah's eight-o'clock call is a real commitment. The ending scripts must honour its consequences or establish Daniel's reply; it must not disappear merely because the final encounter ends. Pause and save never advance the danger.
- The three landmarks receive literal establishing shots here. The final empty-place sequence must be newly held present-day shots with no inserted figures, voices, memory overlays, or explanatory dialogue.
- The repaired hall amplifier is an existing-shop prop, visible from C1S4. C5S1 establishes Jonah's unpaid customer-cover burden; C5S3 confirms ten-o'clock collection. E3 honors the commitment before breakfast at eleven. Other endings leave the obligation unmet without adding a punitive customer scene.
- Mara leaves the recorder case on the counter in C3S2 while taking the recorder home. E3 establishes Daniel collecting the case before going upstairs and setting it aside for their Sunday arrangement; he does not still have her recorder.
