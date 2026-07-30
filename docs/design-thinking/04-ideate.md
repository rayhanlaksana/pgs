# Ideate

Following on from [03-define.md](03-define.md).

Divergent thinking pass — quantity over quality, nothing filtered or ranked
yet. Organized by the three problem statements from Define. Ideas are rough
phrases, not designs, and many will contradict or overlap each other. That's
fine at this stage.

## 1. Overarching — persistent record + surfacing who needs attention

### What form could "the record" take?
1. Auto-generated session log — timestamp + duration captured automatically, provider just adds a one-line note after
2. Voice memo per session — provider talks for 30 seconds right after, transcribed later (or left as audio)
3. Structured form per session (fields: what we did, cues given, homework, next time) instead of freeform text
4. Chat-thread-as-record — the record IS the DM/message history, just tagged/pinned per session rather than a separate app
5. Photo/video snapshot per session as the "log" — visual record instead of written
6. Shared doc per client (like a living Google Doc) both sides can see and edit
7. Calendar-integrated record — every calendar event for a session has a note field attached, so the record lives where scheduling already happens
8. Template-driven quick-log — tap 3-4 preset chips ("good form", "tired", "increased weight") instead of typing anything
9. Client-facing recap auto-sent after each session (SMS/email) that doubles as the record for both sides
10. Streak/calendar-heatmap view as the record — less "what was said," more "did it happen" at a glance
11. Dedicated "medical/PT restriction" field on the per-client record — persistent, not tied to a single session, so an outside provider's restriction doesn't get buried in session-by-session notes or lost in texts

### What would surfacing "who needs attention" look like?
1. Traffic-light status per client (green/yellow/red) on a single dashboard
2. Sorted list — most-overdue-for-check-in at the top, auto-resorts
3. Push notification / daily digest: "3 clients haven't logged in 7+ days"
4. Inbox-zero metaphor — clients "pile up" until acknowledged, then get archived off the list
5. Calendar view with color-coded dots per client per day (session happened / skipped / no data)
6. Simple badge count on an app icon, like unread messages
7. Weekly auto-generated "who needs a nudge" email summary to the coach
8. Client photo grid, greyed-out/faded the longer since last contact
9. Map or timeline view showing gaps (last-seen date per client, sorted by staleness)
10. "You have 2 things to review" home-screen banner, mixing check-ins + videos + flags into one queue

### Laziest-possible version a busy client would actually use
1. One-tap emoji reaction after a session ("👍 / 😐 / 👎") — no typing at all
2. Reply to an auto-sent text with a single word/emoji to log
3. Passive tracking via wearable/phone motion — no explicit logging needed
4. Voice note instead of typing
5. Provider logs everything; client only has to confirm/deny with a tap
6. Weekly single question ("How'd this week go? 1-5") instead of per-session logging
7. Log by exception only — client does nothing unless something's wrong, silence = "fine"

## 2. Injury/Rehab — honest, in-the-moment disclosure

1. Pain scale slider (1-10) required before moving to next exercise
2. Body-map tap — tap the region that hurts instead of describing it in words
3. Mandatory check-in gate — can't mark a set "done" without answering a pain/effort prompt first
4. Anonymous-feeling input — pain report goes to a log, not a live person, removing the social pressure of "telling someone"
5. Pre-set honest-sounding options ("felt it a little," "had to stop," "pushed through pain") instead of open text, so there's a script for admitting it
6. Two-question RPE + pain-location combo after every set, not just at session end
7. "Traffic light" self-check before each exercise: green/yellow/red, red auto-pauses the program
8. Passive signal instead of self-report — video/wearable flags compensating form automatically, removing reliance on disclosure at all
9. Delayed/async disclosure — a private note that only surfaces to the coach, not visible to family watching, lowering the stakes of admitting pain in front of others
10. Gamify honesty — reward accurate reporting over "toughing it out" (streaks for logging, not just for performing)
11. Safe word / one-tap "stop and flag" button always visible during a session
12. Coach sets expected pain threshold per exercise in advance, client just confirms above/below it (comparison is easier than raw self-assessment)
13. Post-session async survey sent automatically, so disclosure happens later/privately rather than in the charged moment

## 3. Coach video review — feedback pinned to a moment

1. Timeline scrubber with comment pins (like Frame.io / YouTube-timestamp comments)
2. Draw/annotate directly on a paused video frame (telestration, like sports broadcast replay)
3. Voice-over comments recorded while scrubbing through the video in real time
4. Side-by-side comparison view — client's rep vs. a reference/ideal rep, comment on the diff
5. Preset tag library ("hips too high," "good depth," "rushed the eccentric") to drop at a timestamp — tap, not type
6. Slow-motion/frame-by-frame stepping with a comment box docked at the bottom, always visible while scrubbing
7. Emoji/sticker reactions pinned to a moment for fast, low-effort feedback
8. Auto-detected rep splitting — video auto-chunks into individual reps, coach reviews/comments per rep instead of scrubbing
9. Template checklist per exercise (e.g. squat: depth / knee track / back angle) triggered as prompts at logical points in the video
10. Batch review mode — queue of all pending client videos, swipe through and leave a quick pin-comment on each without re-opening screens each time
11. Async voice memo per video instead of granular pins — faster than typing, still tied to "this video" if not to the exact frame
12. AI-assisted first pass — auto-flag likely problem frames (e.g. joint angle outliers) for the coach to confirm/comment on, cutting down scrubbing time

## Notes to carry into Prototype

- **Rep-splitting + pain-gate combo**: "Auto-detected rep splitting" (video
  review #8) and "pain scale slider before moving to next exercise"
  (injury/rehab #1) solve different problem statements but share a
  mechanism — if reps are already being segmented for review, that same
  segmentation point is a natural place to also gate a pain/effort check.
  Worth prototyping as one combined flow rather than two separate features.
- **Medical-coordination gap**: Empathy flagged that informal PT/medical
  restrictions get lost in texts. None of the injury/rehab ideas above
  address this directly — it's covered (for now) by record idea #11
  (persistent medical-notes field). Revisit in Prototype to confirm that's
  sufficient rather than needing its own flow.
