# project-swipe-clean.md
# Case study content — Swipe Clean / Avast Cleaner iOS
# Images referenced by filename — map to /assets/swipe-clean/

---

## TAGLINE

Swipe Clean is a new way to review and clean your photo gallery in Avast Cleaner for iOS — one photo at a time, using swipe gestures. I led the design end-to-end, from strategy and concept through to usability testing.

---

## METADATA BLOCK

**My role**
- End-to-end product design: strategy, concept, UI
- Designed photo categorization and set logic system
- Collaborated with UX researchers, engineers, and PM

**Results**
- Feature in final stages before shipping
- Usability testing confirmed swiping rated as faster, more fun, and more satisfying than existing manual cleaning methods

---

## HERO IMAGE

File: Overview.png
(Full-width overview of Swipe Clean flows)

---

## BODY

---

### [PULL QUOTE]
Users came, cleaned once, and never came back — and we kept asking the same question about why.

The retention problem in Avast Cleaner wasn't a mystery. Cleaning is a task people perform reactively, when storage pressure forces their hand. Without that pressure, there's no reason to return. Our research made the emotional dimension of this plain: users who didn't manage their photos regularly described feeling overwhelmed, guilty, and avoidant about it. They knew their gallery was a mess, felt ashamed of it, and dealt with the feeling by buying more cloud storage rather than actually cleaning. The challenge we kept coming back to was whether cleaning could become something users actually wanted to do — not a chore triggered by a full phone, but something they'd reach for on their own. That meant finding a way to make the act of cleaning itself enjoyable enough to repeat.

---

### [PULL QUOTE]
The grid wasn't overwhelming because users had too many photos. It was overwhelming because the photos had no meaning in that form.

Our existing cleaning interface showed photos as a grid of small thumbnails organized by month — which could contain anywhere from a handful to several thousand images. At thumbnail size, making a decision about any individual photo is nearly impossible. There's no context, no narrative, no way to orient yourself within the mass of images. Users would open it, feel immediately lost, and close it again. Swiping one photo at a time would solve part of the problem, but not the underlying one. To make cleaning feel manageable, we first needed to give the gallery structure that users could actually navigate.

---

IMAGE: Main_screen_-_Content_not_cliped.png
(Swipe Clean main screen showing all category rows: Utility photos, Moments, Retrace your steps, Holidays, Events, People, Pets, Months — each with sets of photos organized by date and location)

---

### Categorization

### [PULL QUOTE]
We organized the entire gallery into categories users already recognized — then broke each one into sets small enough to finish in a single session.

The categorization system was the core design work of the project. I defined eight categories — Utility photos, Moments, Trips, Holidays, Events, People, Pets, and Months — each with its own logic for detecting and grouping photos using metadata like location, date, time, and content recognition. Within each category, photos are further divided into sets bounded by a strict rule: every set must contain between 10 and 80 photos. Below 10, a set is merged with its nearest neighbour. Above 80, it is subdivided by time or location into smaller groups.

The 80-photo ceiling was a deliberate design constraint. A set that can be swiped in a few minutes delivers immediate, tangible value — the space saved number updates, the set disappears, progress is visible. A set with hundreds of photos becomes the same overwhelming experience we were trying to fix. The limit is what makes the value immediate — a set small enough to finish in one sitting means the space saved number updates before the user puts their phone down. This was independently confirmed by our qualitative research, where users — before seeing any solution — described wanting exactly this: bite-sized cleanup prompts, something that made the task feel achievable rather than endless. The set size limit was the design answer to that unprompted request.

---

IMAGE: Main_condition.png
(Sets creation rule: every set must have more than 10 and fewer than 80 photos)

---

IMAGE: Creating_smaller_sets_rules_1_-_1_day_trip.png
(Example of how a large trip set is subdivided by location or time into manageable sets)

---

The category names and section headings were written to feel like reviewing memories, not managing storage. "Retrace your steps" for trips, "Moments" for algorithmically surfaced highlights, "Holidays throughout the years" for recurring celebrations. A user scrolling through Swipe Clean should feel like they're browsing their own photo library — with the side effect of freeing up space as they go.

---

IMAGE: Main_screen_top.png
(Top of Swipe Clean main screen after cleaning sessions: Space saved counter with graph showing cumulative progress, followed by category rows)

---

### Swiping

### [PULL QUOTE]
The interaction needed to feel immediately obvious — and in testing, users compared it to dating apps within the first few photos.

The swiping interaction had one job: make each decision feel fast and consequence-free. Photos go to Trash, not permanent deletion — nothing is gone until the user decides to empty it. This separation was important because users in research consistently said they wanted control over deletion. The swipe is a sort, not a delete. Making that distinction clear in the interaction itself — and in the copy — was the difference between an experience that felt safe to use quickly and one that felt risky.

Feedback was designed to be immediate and legible at a glance. Color, motion, and a running counter all confirm what just happened without requiring the user to stop and read anything. In usability testing, the icon set and counter were described as a no-brainer — users picked up the pattern within the first two photos and kept going without hesitation. Several compared it to a game. That was exactly the response we were looking for.

---

IMAGE: Swipe_overlays_.png
(Swiping interaction diagram: swipe left = Move to trash with blue overlay, swipe right = Keep with green overlay, center buttons for accessibility)

---

IMAGE: Swipe_left_interaction_1_.png
(Swipe left interaction sequence: photo rotates and slides left out of frame with Move to trash overlay)

---

IMAGE: Swipe_right_interaction_2.png
(Swipe right interaction sequence: photo rotates and slides right out of frame with Keep overlay)

---

IMAGE: Trashed___Kept_counters.png
(Swipe detail screen showing trash counter on left and keep counter on right building up as user swipes through set)

---

### End of set and deletion

Deletion lives in Trash rather than at the end of the swipe flow for a simple reason: Avast Cleaner already had a dedicated Trash section where all other deletions happened. Embedding deletion inside Swipe Clean would have split the same action across two different places in the app. Keeping it consistent meant directing users to Trash after swiping — the same place they'd go for anything else.

The end of each set is a moment of payoff — the first place where the value of what the user just did becomes concrete. The number of photos sorted and the space that will be freed are shown before any permanent action is taken, giving users a reason to keep going without pressure to commit immediately. The choice to continue cleaning or go to Trash and delete is deliberately left open — the experience is designed to reward either decision.

---

IMAGE: End_of_swiping_photo_set_screen_1.png
(End of set screen: "51 photos moved to trash" with space to be freed, Go to trash button and Continue cleaning option)

---

IMAGE: Go_to_trash_flow_1.png
(End of set → Trash screen with all swiped photos selected → Delete all)

---

IMAGE: Deleting_photos_from_trash.png
(Trash → deletion → "You've cleaned 668 MB" success screen → back to Swipe Clean main with updated space saved counter)

---

IMAGE: Photos_in_trash_info_on_main_screen.png
(Dynamic trash prompt on Swipe Clean main screen when accumulated trash exceeds 500MB, nudging user to empty it)

---

### [PULL QUOTE]
Cleaning a gallery full of memories should feel like revisiting them — not filing paperwork.

Every interaction in Swipe Clean is designed to work in the same direction: reduce friction, deliver value immediately, and make the next session feel like something worth coming back to. Sets are small enough to finish. Categories are familiar enough to navigate. Copy frames the experience as browsing, not maintenance. The space saved counter makes progress visible across sessions. Whether the sum of these decisions produces the habitual engagement we set out to build is what the data will confirm — but every design choice was made with that single goal in mind.

---
