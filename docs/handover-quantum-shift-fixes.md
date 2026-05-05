# Quantum Shift opt-in page · fixes needed (handover)

**Date:** 5 May 2026
**Page:** `aob/quantum-shift.html` (also at `landing-pages/quantum-shift/index.html` in the repo)
**Live preview:** `localhost:3000/aob/quantum-shift.html` (run `node serve.mjs` from `landing-pages/`)
**Repo:** https://github.com/tglav109/aob (latest commit on `main`)
**Brand rules (CLAUDE.md):** Marcellus + Roboto, gold #cc9924, teal #354d4c, ink #1a1a18, off-white #f9f8f5. **No em dashes anywhere on the page.**

---

## Background context for the next chat

The page is the opt-in for **Quantum Shift, Sunday 17 May 2026** · a free one-day live breathwork event with Anthony Abbagnano and Amy Rachelle. Two live sessions: Part 1 at 9:30 to 11:30am UK, Part 2 at 5 to 7pm UK. Free to attend, recording sold for $49.99 after the event. The page funnels into Alchemy Regulation Method Coach (Level 1 of the ARM Training School) which opens shortly after the event.

The page has had multiple rounds of feedback from Amy Rachelle, Anna Myers, Renars Garda, and Jenny Suessmann (Monday board item `Review QS launch page`, ID `11919487989`). The current version has incorporated most of that feedback, but the page has drifted in places and now contains structural duplication, repeated content, and one section that has lost the warmth of Amy's original framing.

---

## What's working · do NOT touch

These elements are landing well. Leave them alone.

| Section | Element |
|---|---|
| **Hero H1** | *"A full day to teach your nervous system what regulation feels like."* |
| **Hero subhead** | *"Two live breathwork sessions. By Sunday evening, regulation is a state you can find in your own body on demand. Not a concept you read about."* |
| **Coping section eyebrow + H2** | "Coping strategies" / **"Coping is not regulating."** |
| **Founder thumbnails above the fold** | Anthony + Amy with "Led live by" pill |
| **Session pills** | Part 1 9:30 to 11:30am UK · Part 2 5 to 7pm UK |
| **Closing italic gold inside the dark "What Quantum Shift is" section** | *"People leave this day different. Not because they learned something. Because they felt something their body will not forget."* |
| **Reserve form section** | Form embed and surrounding copy |
| **Testimonials block** | Nick (featured) + Tanya Lopez + Steph Magenta |
| **No em dashes anywhere** | Verified |

---

## Critical fixes needed

### Fix 1 · Coping section: restore Amy's original body copy

The H2 stays as **"Coping is not regulating."** (we keep the new framing). But the body copy below it has drifted from Amy's original version, which she explicitly approved on the Monday board. Restore Amy's exact text below the H2. Her original is at the end of this document under "Amy's verbatim copy · restore this."

The current body has my interpretation of her voice; it lost the warmth she wrote in.

### Fix 2 · "The breath is the only autonomic function" appears TWICE

It appears once in the body copy at the end of the Coping section, AND again as the **first image-break quote** (the one over the orange-shirt people-in-circle photo).

Pick one location. **Recommend:** keep it in the Coping section body (where it belongs as the bridge to "what we will do on Sunday"). **Replace the image-break quote** with a different felt-experience anchor.

Suggested replacement for image break 1:
> *"Your nervous system runs on your breath. You just have not been taught how to drive."*

### Fix 3 · Outcome cards section needs its own clear identity

Current 4 cards: *You stop reacting from survival* / *Get grounded* / *Train your nervous system* / *No more mean talk*. Each card uses the eyebrow **"WHAT CHANGES"** four times in a row, which feels lazy and repetitive.

**Make this a standalone section with its own H2.** Suggested:

```
EYEBROW: After Sunday
H2: What changes in your body, your relationships, your day.
[Then the 4 cards]
```

And **remove the eyebrow "WHAT CHANGES" from each individual card.** Just have the card title + body. The single section H2 covers the framing.

Also: card 3 ("Train your nervous system") repeats the hero H1 nearly verbatim. Replace with something more specific:
- *"Sleep harder, react softer"*
- *"A baseline that holds"*
- *"Your physiology, recalibrated"*

### Fix 4 · Two image-break quotes back-to-back say the same thing

Current after the outcome cards:
- **Image break 2** (ASHA aerial): *"You will regulate fully, measurably, in real time. Not as a concept. As a felt experience in your own body."*
- **Image break 3** (group photo at ASHA): *"By Sunday evening, you will know what regulation feels like. Because your body will have been there."*

Both quotes promise the same outcome with slightly different words. **Pick one. Cut the other.** Recommend keeping image break 3 (it's tighter and more time-bound).

### Fix 5 · Final CTA echoes the image break that precedes it

The final CTA H2 says: *"One Sunday. Two free sessions. A nervous system you can finally rely on."* Right after an image break that said: *"By Sunday evening, you will know what regulation feels like. Because your body will have been there."*

Same promise twice in 60 vertical pixels. Either:

- **Option A:** Keep the image break, replace the final CTA H2 with a felt closing line:
  > *"Coping has been your job long enough.<br/>Sunday, you can let your body do something else."*

- **Option B:** Cut the image break (per Fix 4 above) and let the final CTA stand on its own.

Recommend **Option A + Fix 4 keeps image break 3.** That gives you: image break with the outcome promise → final CTA with the emotional release.

### Fix 6 · Subhead under final CTA H2 is functional, not emotional

Current: *"Live with Anthony Abbagnano and Amy Rachelle. Part 1 at 9:30am UK, Part 2 at 5pm UK. Sunday 17 May."*

The reader has seen the date and times five times by now. This subhead is wasted space. Replace with a felt one-liner or remove entirely.

---

## Amy's verbatim copy · restore this in the Coping section

Use **exactly this text** below the H2 *"Coping is not regulating."* Do not paraphrase, do not tighten, do not "Claude-ify."

> Pushing through, thinking positive, staying busy. How does this feel in your body?
>
> Is it true nervous system regulation?
>
> They can be nervous system overrides when we aren't connected to the impact they can have on our body. And overrides have a cost: chronic stress, emotional reactivity, exhaustion that sleep does not fix, the version of yourself you keep meaning to take care of.
>
> These are not character flaws. They are the predictable result of a nervous system that has never been trained to hold what life brings, without regular release. In one day, that can change.
>
> The breath is the only autonomic function you can consciously control. It's the most direct access point to the biology of how you respond to everything. Not one day when things calm down. Let's do this - this Sunday. In this body. With us. Together.

**Source:** Amy Rachelle's comment on Monday board item 11919487989, 5 May 2026, 12:31 PM (timestamp `2026-05-05T12:31:53.000Z`).

**Note about em dashes:** Amy's original uses *"Let's do this - this Sunday"* with a regular hyphen + spaces, not an em dash. Keep it that way (or use a comma: *"Let's do this, this Sunday."*). Brand rule prohibits em dashes only.

---

## Suggested execution order for the next chat

1. Restore Amy's verbatim body copy in the Coping section (Fix 1)
2. Replace image break 1 quote so it stops duplicating the breath line (Fix 2)
3. Make the outcome cards a standalone section with its own H2 (Fix 3)
4. Cut image break 2 OR image break 3 (whichever you don't keep) (Fix 4)
5. Replace final CTA H2 with felt closing line (Fix 5)
6. Cut or rewrite final CTA subhead (Fix 6)
7. Re-verify zero em dashes
8. Push to git, copy to clipboard

---

## Other context the next chat will need

### Brand rules (mandatory)
- Marcellus headings, Roboto body
- Gold #cc9924, teal #354d4c, ink #1a1a18, off-white #f9f8f5
- **No em dashes (the long dash character or `&mdash;`) anywhere**. Use periods, commas, semicolons, or `&middot;` instead.
- Voice: warm, grounded, conversational, second-person. Mirror Amy's "Why this matters right now" copy as the gold standard.

### Files affected
- `aob/quantum-shift.html` (working version · edit this first, preview locally)
- `landing-pages/quantum-shift/index.html` (sync this from the working file before pushing to git)

### Custom values used (already wired)
- Page form ID: `JXFlOEgAhMoElAqLBG1L`
- Email custom values: `{{custom_values.logo}}`, `{{custom_values.btw_am_session_link}}`, `{{custom_values.qs_event_recording}}`

### Things confirmed not to change
- Founder bios already use Amy's preferred language ("Naturopathic Coach and Medical Medium", "& ASHA, Tuscany")
- Times are 9:30 to 11:30am UK / 5 to 7pm UK, UK time only (per Amy: "4am is a turn off")
- Registration close deadline removed (per Amy: people may only see it last min)
- ARM Coach card removed (per Anna: details not yet confirmed)
- Press strip removed (Goop was a hallucination per team; will re-add when real logos available)
- Footer email is `info@alchemyofbreath.com` (NOT hello@)

### Live commit hash
Run `git log --oneline -1` from `/Users/workspace/AoB/landing-pages` to see the current commit. The most recent push before this handover should be on or after `c93128a` ("Quantum Shift: incorporate full team feedback from Monday board review").

---

## What this doc does NOT cover

- Email sequence (separate file: `aob/emails/quantum-shift-email-sequence.md`, also at `docs/emails/quantum-shift-email-sequence.md`). 6 emails are written and approved.
- ARM page (`aob/index.html` / `landing-pages/alchemy-regulation-method/index.html`). Not in scope for this handover.
- Post-event nurture sequence. Not yet drafted.

---

## One last note for the next chat

Tania's preference is direct, opinionated copy review and quick action. She does not want a CRO essay. She wants:

1. Confirmation you understand the issue
2. A short, specific rewrite proposal
3. Implementation
4. Verification + clipboard copy

Do not over-explain. Do not give 5 options when 1 is best. Do not write 2,000-word audits unless asked. The page needs to ship, not theorise.
