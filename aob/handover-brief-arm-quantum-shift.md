# Handover Brief: Quantum Shift event & ARM Online launch

**Owner:** Tania Glavey (BuilderBee) for Alchemy of Breath
**Last updated:** 1 May 2026
**Prepared for:** Success Advisors, marketing operations, future-self

---

## TL;DR

Two connected assets shipping in May 2026.

1. **Quantum Shift** — a free one-day live breathwork event on **Sunday 17 May 2026**, hosted by Anthony Abbagnano and Amy Rachelle. Two sessions (morning and evening). Free to attend live. Recording sold for **$49.99** for those who cannot make it. The event is a top-of-funnel traffic driver into ARM.
2. **ARM (Alchemy Regulation Method)** — the rebrand of the old Calm Code. A complete training in breath and nervous system regulation. Online cohort launching **June 2026** at a **founding rate of $299** (saves $400 off the $699 standard). In-person residential at ASHA, Tuscany, **10–16 May 2026** (€1,701–€2,738 all-inclusive). Six-stage methodology. Trauma-informed. ICF / SHRM / CIPD recognised at L1.

The funnel: **Quantum Shift opt-in → felt experience of regulation → ARM Online waitlist or Discovery Call → enrolment.**

---

## The two pages

### Page 1: Quantum Shift opt-in

| Field | Value |
|---|---|
| **Local file** | `aob/quantum-shift.html` |
| **Repo path** | (not yet pushed under a separate path; lives in working `aob/` folder) |
| **Suggested live URL** | `go.alchemyofbreath.com/quantum-shift` (to be confirmed by AoB) |
| **GHL form ID (registration)** | `JXFlOEgAhMoElAqLBG1L` (form name: "AOB \| Event: QS Optin \| ARM") |
| **Recording purchase link** | `link.alchemyofbreath.com/payment-link/quantum-shift-recording` — **placeholder, replace with real Stripe/GHL payment link before launch** |
| **Date of event** | Sunday 17 May 2026 |
| **Format** | Full-day live event, two sessions (morning + evening). Times TBC. |
| **Hosts** | Anthony Abbagnano (Founder), Amy Rachelle, ND (Co-founder) |
| **Live attendance price** | Free |
| **Recording price** | $49.99 |
| **Primary CTA** | "Register for free" (scrolls to inline form) |
| **Secondary CTA** | "Get the recording · $49.99" (external Stripe link) |
| **Onward funnel** | "What happens next" section links to ARM Online (`go.alchemyofbreath.com/alchemy-regulation-method-online`) |

#### Page sections, in order

1. Hero with date pill + dual CTAs + session pills
2. Why this matters (Amy's three paragraphs)
3. Image break with pull quote (the breath as autonomic access point)
4. What Quantum Shift is — including Anthony + Amy founder portraits
5. Four outcome cards (Relationships shift / Noise settles / Purpose clearer / Understand yourself differently)
6. Image break with pull quote ("you will regulate fully, measurably, in real time")
7. Two offer cards: Live Free / Recording $49.99
8. Inline registration form (`JXFlOEgAhMoElAqLBG1L`)
9. What happens next: ARM Coach L1 callout card linking to ARM page
10. Image break with closing quote ("One day. Two sessions. One breath at a time.")
11. Final CTA with both paths (free / recording)
12. Footer

### Page 2: ARM (Alchemy Regulation Method)

| Field | Value |
|---|---|
| **Local file** | `aob/index.html` |
| **Repo path (pushed)** | `landing-pages/arm/index.html` on `tglav109/aob`, branch `main` |
| **Public live URL** | `go.alchemyofbreath.com/alchemy-regulation-method-online` |
| **GHL form ID (waitlist)** | `0Y0M6NBIBRkgWW2k3h3R` (form name: "AOB \| Waitlist \| ARM") |
| **Discovery call URL** | `go.alchemyofbreath.com/book-your-discovery-call-page` |
| **GHL custom value** | `{{custom_values.breathwork_facilitator_training__discovery_call_url}}` (used in nurture emails) |
| **Online cohort start** | June 2026 (exact dates TBC) |
| **Online price** | **$299 founding rate** (was $699, saves $400) |
| **In-person dates** | 10–16 May 2026 |
| **In-person price** | €1,701 (camping) to €2,738 (private cottage), all-inclusive |
| **Call duration** | 45 minutes (free, no commitment) |

#### Page sections, in order

1. Hero with ambient gold sparks + flying fireflies. Two CTAs: "Try one breath" (reveals hidden orb section) + "See the method"
2. **#breathe section** — fully hidden by default. Click "Try one breath" → unhides + scrolls to + starts the box-breath orb animation with guided "Inhale / Hold / Exhale / Hold" labels
3. Trust strip (2,000+ practitioners · 40+ countries · 12+ years · 15ha ASHA)
4. Featured & Trusted By logo marquee
5. The Why — Anthony's "Have you ever been in a room…" opener
6. What this is — methodology overview with image
7. Methodology — six-stage interactive cards (Remember / Reframe / Resource / Regulate / Realign / Rise)
8. The Science — four stat cards (Vagal tone / HRV / Stress hormones / Flexibility) on dark background
9. Audiences ("Built for you. A system that uplifts you…") with practitioner tags
10. Bridge image with bold claim
11. Format & Pricing — two cards: Online ($299 founding rate) and In-Person (ASHA)
12. **Inline waitlist form** (`0Y0M6NBIBRkgWW2k3h3R`)
13. Trainers — 4 equal columns: Anthony, Amy, Pablo, Nick
14. Founders block (Anthony + Amy bios)
15. Get Started CTAs (waitlist modal + schedule a call)
16. FAQ
17. Footer
18. Hidden waitlist modal (also triggered from "Join the waitlist" CTAs in nav, format card, and Get Started)

---

## GHL setup checklist

### Forms

| Form name | Form ID | Used on |
|---|---|---|
| AOB \| Event: QS Optin \| ARM | `JXFlOEgAhMoElAqLBG1L` | Quantum Shift page (`#reserve`) |
| AOB \| Waitlist \| ARM | `0Y0M6NBIBRkgWW2k3h3R` | ARM page (`#waitlist` inline + waitlist modal) |
| Discovery Call Intake | `GXgyYQ4wG1W8zo0USmsh` | Triggers the FT nurture sequence |

### Recommended form questions

For QS opt-in (and any new event opt-in), keep it minimal to maximise conversion:

1. First name (required)
2. Email (required)
3. Time zone (required, dropdown: GMT, EST, PST, CET, AEST, Other)
4. What pulled you here? (optional dropdown)
   - I'm exhausted and want to feel different
   - I work with people and want this for them
   - A friend or colleague recommended it
   - I'm already exploring breathwork
   - Just curious
5. Are you a practitioner? (optional Yes/No, with optional follow-up "What kind of work?")

**Hidden fields** (populate silently from URL params):
- `utm_source`, `utm_medium`, `utm_campaign`
- `referrer_url`
- `event_tag` = `quantum-shift-2026-05-17` for QS, `arm-online-launch-2026-06` for ARM waitlist

### Custom values

| Custom value | Purpose |
|---|---|
| `{{custom_values.breathwork_facilitator_training__discovery_call_url}}` | Single source of truth for the discovery call URL across all FT/ARM emails. Update once, ripples to every email. |

### Tags

- `quantum-shift-attended-live` — set when contact attends live session
- `quantum-shift-registered` — set on QS opt-in form submission
- `quantum-shift-recording-purchased` — set on recording purchase
- `arm-waitlist` — set on ARM waitlist form submission
- `arm-online-enrolled` — set on enrolment
- `arm-asha-enrolled` — set on Retreat Guru booking webhook

---

## Funnel logic

```
                ┌──────────────────────────┐
                │   Quantum Shift LP       │
                │  /quantum-shift          │
                └────┬─────────────────┬───┘
                     │                 │
            Free live registration   Recording purchase ($49.99)
            JXFlOEgAhMoElAqLBG1L     Stripe/GHL payment link
                     │                 │
                     ▼                 ▼
               ┌────────────────────────────┐
               │  Live event 17 May 2026   │
               │  Two sessions: AM + PM    │
               └────────────┬──────────────┘
                            │
                            ▼
               ┌────────────────────────────┐
               │  Post-event email          │
               │  (segmented by their       │
               │   "what pulled you here"   │
               │   answer)                  │
               └────────────┬──────────────┘
                            │
                            ▼
               ┌────────────────────────────┐
               │  ARM page                  │
               │  /alchemy-regulation-      │
               │   method-online            │
               └────┬─────────────────┬─────┘
                    │                 │
            Join waitlist        Discovery call
            0Y0M6NBIBRkgWW2k3h3R book-your-discovery-call-page
                    │                 │
                    ▼                 ▼
               ┌────────────────────────────┐
               │  Enrolment                 │
               │  - Online ($299)           │
               │  - ASHA (€1,701-€2,738)    │
               └────────────────────────────┘
```

---

## Email automation outline (build in GHL Workflows)

### Trigger 1: QS registration

| When | Email |
|---|---|
| T+0 | Confirmation: live access link, calendar invite (.ics), what to expect |
| T+3 days before | "We meet on Sunday" reminder + tech check |
| T+1 day before | "Tomorrow at 10am [TZ] / 7pm [TZ]" reminder + final access link |
| T+2 hours before | "Starting in 2 hours" SMS-style email |
| T+immediately after | "Did you feel that?" follow-up: ARM Coach pitch (segmented by registration answers) |
| T+2 days after | Recording delivery email (only to recording purchasers) |
| T+3 days after | Final ARM Coach push for non-converters |

### Trigger 2: ARM waitlist signup

| When | Email |
|---|---|
| T+0 | Welcome to the waitlist, founding rate locked at $299 |
| T+3 days | What ARM is + the six-stage methodology overview |
| T+7 days | Anthony's story (the why behind ARM) |
| T+14 days | Practitioner stories (segmented by practitioner Y/N) |
| Launch day | "Doors are open. You're first in line." |

### Trigger 3: Discovery Call Intake (Facilitator Training)

The 6-email value-driven nurture series is already drafted. See `landing-pages/training/nurture-sequence.md` in the repo. Uses `{{custom_values.breathwork_facilitator_training__discovery_call_url}}`. Free Breathe the World invite + free Fundamentals course as value drops, with discovery call as the primary CTA in every email.

---

## Pricing reference

| Offer | Price | Notes |
|---|---|---|
| Quantum Shift live | Free | Both sessions on 17 May |
| Quantum Shift recording | $49.99 | Both sessions, full recording, lifetime access |
| ARM Online | $299 founding rate (~~$699~~) | Save $400 — Limited spots — Starts June 2026 |
| ARM at ASHA | €1,701 to €2,738 | All-inclusive (training + lodging + meals); 10–16 May 2026 |
| Facilitator Training | $6,700 super early bird (~~$7,200~~) | September 2026 intake; 8 months online + BreathCamp |
| Facilitator Training deposit | (removed) | Was $499; removed per Anthony's feedback |
| BreathCamp at ASHA | Separate registration | Required for FT certification |

---

## Brand and tone rules

- **No em dashes anywhere** in any copy. Use periods, commas, semicolons, or `&middot;` instead. Both pages currently have zero em dashes.
- **Marcellus** for headings (display serif). **Roboto** weight 300 for body. Weight 500 for buttons and eyebrows.
- **Gold:** `#cc9924`. **Teal:** `#354d4c`. **Ink:** `#1a1a18`. **Off-white:** `#f9f8f5`.
- **Voice:** Grounded, second-person, no hype. Mirror Amy's "Why this matters right now" copy on the QS page as the gold standard.
- **Em-dash trap warning:** Common when copy is dictated or pasted from Notion/Google Docs. Always grep `&mdash;\|—` before pushing.
- **Trauma-informed framing** on ARM page is mandatory — never describe ARM as "trauma catharsis" or "altered state practices." It is the foundation that makes the deeper modalities safer.
- **Hannah Goodman** (former AoB graduate) is to be referred to as "Alchemy of Breath facilitator," **not** "ARM Certified Facilitator." She's not currently active with AoB, so currently no testimonial is on the ARM page. Net new testimonials needed.

---

## Image library (filesafe.space CDN)

These images have been used across both pages. **Do not use** `961c6a1a-7eb2-44e8-b085-af1c069cc0e1.jpeg` — flagged by Anthony (former staff member appears in it).

| Asset ID | Description | Currently used on |
|---|---|---|
| `5f079a98-743b-4ae9-a49a-2306d51c3b6d.jpeg` | Release moment in breathwork session | ARM (What this is), QS (image break 1) |
| `69b2e9c0eba4870752ef7c19.jpg` | Breathwork session at ASHA | ARM (Stage 2 Reframe), QS (image break 2), FT page |
| `69b2e9c0cab7f74dd5790aaf.jpg` | Deep inner work | ARM (Stage 1 Remember) |
| `69b2e9c0ef84872e3bbf57e8.jpg` | Practitioners in session | ARM (Stage 4 Regulate) |
| `69b2e9c0eba487150def7c1e.jpg` | Practitioner community | ARM (Stage 5 Realign) |
| `69eb82499fe87a9994a74141.jpg` | Group at ASHA | ARM (Stage 6 Rise), QS (image break 3), FT |
| `69b2e9c0cab7f7d4b0790ab1.jpg` | Group breathwork | ARM (Stage 3), QS (ARM Coach card) |
| `69b2e9c0005051f0672b3bb0.jpg` | ASHA grounds | ARM (Bridge background) |
| Anthony portrait | `alchemyofbreath.com/wp-content/uploads/anthony-abbagnano-2-1.jpg` | ARM, QS, FT |
| Amy portrait | `alchemyofbreath.com/wp-content/uploads/amy-rachelle-1.jpg` | ARM, QS, FT |
| Pablo portrait | `69d4e1e2bec7abdef136e5de.jpeg` | ARM trainers grid |
| Nick portrait | `69d4e25c3d63f9b9380569e9.jpeg` | ARM trainers grid |

---

## Outstanding decisions / open items

These were raised during Anthony's review on 28 April. Some are addressed; some still need a call:

- ✅ "Start ARM" CTA wrong → changed to "Try one breath" (hero) and "Join the waitlist" (nav)
- ✅ Hide orb until "Try one breath" clicked → done; whole #breathe section hidden by default
- ✅ Remove four pillars → done
- ✅ Remove "altered state practices" from disclaimer → done
- ✅ Trauma-informed framing → added
- ✅ Cortisol → "Stress hormones" with all three named
- ✅ Six-stages intro de-muddled → "Imagine you are passing through six stages…"
- ✅ Science headline rewritten → "The dashboard of your nervous system. And how to use it."
- ✅ "Built for people who work with people" → "Built for you. A system that uplifts you…"
- ✅ "Led by practitioners. Grounded in experience." → "Over 100 years of breathwork experience. Combined."
- ✅ Hannah Goodman testimonial → removed (not currently active)
- ✅ Anthony's panic-attack opening quote → removed (per latest direction)
- ✅ ARM page links Quantum Shift correctly to ARM Online
- ✅ Pricing $299 from $699 → confirmed
- ✅ Call duration 45 minutes → confirmed
- 🟡 **Stage 1 image** — Anthony asked for a tighter crop on the Anthony+Cosimo group circle. Need source photo or zoom-cropped version.
- 🟡 **Stage 5 image** — Anthony wants people raising hands at the end of a breath gap. Need to check ASHA library for such a photo.
- 🟡 **Net new testimonials** — Hannah Goodman was the only one on the page and has been removed. Need 3+ new ones from current AoB facilitators / ARM students before we can reinstate a testimonial section higher in the funnel.
- 🟡 **Recording purchase URL** — currently a placeholder on the QS page (`link.alchemyofbreath.com/payment-link/quantum-shift-recording`). Need real Stripe/GHL payment link before launch.
- 🟡 **QS event session times** — currently shown as just "morning" and "evening." Need exact times in the host time zone for the email reminders and meta description.
- 🟡 **ARM Coach L1 page** — QS page links to ARM Online for "Learn about ARM Coach L1." If a separate dedicated L1 landing page is built, swap the link.
- 🔴 **SEO gaps on both pages** — both currently lack Open Graph + Twitter Card meta, JSON-LD structured data (Event for QS, Course for ARM), canonical URL, and favicon. These are easy to add and significantly boost organic discovery + share preview cards. Recommend adding before launch.
- 🔴 **Quantum Shift title tag is 95 characters** (over Google's ~60-char limit). Will get truncated in SERPs. Recommend shortening to "Quantum Shift · A Free One-Day Breathwork Event · 17 May 2026" or similar.
- 🟡 **Photos request** — Anthony wants photos to feature people, not landscapes. All current stage photos are people-only as of last revision; new photos requested for stages 1 and 5.

---

## Repo and deployment

- **Repo:** `https://github.com/tglav109/aob`
- **Branch:** `main`
- **Collaborators:** `tglav109` (owner, admin), `MalikJPalamar` (write access, accepted)
- **Local working directory:** `/Users/workspace/AoB/landing-pages/`
- **Local dev server:** `node serve.mjs` from `landing-pages/` root, serves at `http://localhost:3000/aob/`

| Local file | Repo path | Status |
|---|---|---|
| `aob/index.html` (ARM page) | `landing-pages/arm/index.html` | Pushed |
| `aob/training.html` (FT page) | `landing-pages/training/index.html` | Pushed |
| `aob/quantum-shift.html` (QS page) | (not yet pushed under new path) | **TO DO: push to `landing-pages/quantum-shift/index.html`** |
| `aob/nurture-sequence-facilitator-training.md` | `landing-pages/training/nurture-sequence.md` | Pushed |
| `aob/handover-brief-arm-quantum-shift.md` (this file) | (not yet pushed) | **TO DO: push** |

**Workflow:** Edit local file → preview at `localhost:3000/aob/<filename>.html` → `pbcopy < <filename>` → paste into GHL custom code block → publish from GHL.

---

## Day-of-event execution checklist (Quantum Shift)

### One week before

- [ ] Confirm Zoom / live platform link is generated and tested
- [ ] Reminder email scheduled in GHL Workflow
- [ ] Recording purchase link is live (Stripe/GHL)
- [ ] Test the entire funnel: opt-in → confirmation email → calendar invite → access link
- [ ] Confirm session times in host time zone and convert for ICS calendar invite
- [ ] Brief Anthony + Amy on flow (intro / breath / share / Q&A / ARM Coach soft close)

### Day before

- [ ] Final reminder email sent at 24h before
- [ ] Tech check with Anthony + Amy
- [ ] Backup link prepared in case of platform failure
- [ ] All registered attendees in a single GHL list

### Day of

- [ ] 2-hour reminder email
- [ ] Open the room 15 minutes early
- [ ] Welcome message in chat with the recording purchase link for late arrivals
- [ ] Anthony + Amy lead each session (morning + evening)
- [ ] Closing soft pitch for ARM Coach with the link

### Day after

- [ ] Tag everyone who attended live (`quantum-shift-attended-live`) for separate post-event nurture
- [ ] Recording uploaded and delivery email sent to recording purchasers
- [ ] Send "did you feel that?" email to live attendees with ARM Coach pitch
- [ ] Public share recap on social (3-4 graphics + behind-the-scenes)

---

## What success looks like

### Quantum Shift event

| Metric | Target |
|---|---|
| Opt-in conversion (LP → form submit) | 25%+ |
| Live attendance rate (registered → showed up) | 40%+ |
| Recording purchase rate (LP visitor → $49.99) | 1-2% |
| Post-event ARM waitlist conversion (attended → joined waitlist) | 15%+ |
| Discovery call booking rate (attended → call booked) | 5%+ |

### ARM Online launch

| Metric | Target |
|---|---|
| Waitlist size at launch | 300+ |
| Waitlist → enrolment conversion | 8-12% |
| Founding-cohort fill rate | First 50 seats sold within 7 days of launch |

### Funnel volume targets (60-day window from QS event to ARM Online launch)

| Stage | Volume |
|---|---|
| LP visitors (paid + organic) | 5,000 |
| QS opt-ins | 1,250 |
| Live attendees | 500 |
| ARM waitlist | 300+ |
| ARM enrolments | 30-40 |

---

## Contacts

- **Tania Glavey** (BuilderBee) — landing pages, automation, copy: tania@builderbee.co
- **Anthony Abbagnano** (Founder) — voice, story, final approval on copy
- **Amy Rachelle, ND** (Co-founder) — clinical/scientific accuracy, retreat logistics
- **Malik Palamar** (collaborator on GitHub) — technical co-pilot
- **AoB shared inbox** — hello@alchemyofbreath.com

---

## Files referenced

- `aob/index.html` — ARM page (lives at landing-pages/arm/index.html in repo)
- `aob/quantum-shift.html` — Quantum Shift event page
- `aob/training.html` — Facilitator Training page (lives at landing-pages/training/index.html in repo)
- `aob/nurture-sequence-facilitator-training.md` — 6-email sequence draft
- `aob/handover-brief-arm-quantum-shift.md` — this file
- `CLAUDE.md` — project rules and brand guardrails
