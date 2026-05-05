# Quantum Shift Email Sequence

**Event:** Quantum Shift, Sunday 17 May 2026
**Sessions:** Part 1 - 9:30 to 11:30am UK · Part 2 - 5 to 7pm UK
**Trigger form:** GHL form `JXFlOEgAhMoElAqLBG1L` (AOB | Event: QS Optin | ARM)
**Brand:** Alchemy of Breath. Marcellus + Roboto. Gold #cc9924, teal #354d4c, ink #1a1a18, off-white #f9f8f5. **Zero em dashes.**

---

## Sequence at a glance

| # | Send | Timing | From | Subject |
|---|------|--------|------|---------|
| 1 | T+0 | Immediate on form submit | Anthony Abbagnano | You're in. Here's what to know about Sunday. |
| 2 | T+2 days | After they have settled | Amy Rachelle | What nervous system regulation actually means |
| 3 | Friday 15 May, 9am UK | 48h before | Alchemy of Breath | Two days. Are you ready? |
| 4 | Saturday 16 May, 9:30am UK | 24h before | Anthony | 24 hours. |
| 5 | Sunday 17 May, 8:30am UK | 1h before Part 1 | Alchemy of Breath | We start in one hour. |
| 6 | Sunday 17 May, 4pm UK | 1h before Part 2 | Anthony & Amy | How was the morning? |

**Exit conditions:** Drop the contact from the sequence as soon as they buy the recording, unsubscribe, or get tagged `quantum-shift-attended-live`.

---

## Custom values used

| Custom value | What it is | Used in |
|---|---|---|
| `{{custom_values.logo}}` | AoB logo URL for email header | All 6 emails |
| `{{custom_values.btw_am_session_link}}` | Zoom link for both Part 1 and Part 2 | All 6 emails (button) |
| `{{custom_values.qs_event_recording}}` | Stripe/payment link for the $49.99 recording | All 6 emails (PS / button) |

**Hardcoded fallback** (in case custom values are not configured yet):
- Zoom: `https://us06web.zoom.us/j/88515813912?pwd=d2JjSjhsOWhneVZWQWVkc0h0aTh2QT09`
- Meeting ID: `885 1581 3912`
- Passcode: `Breathe`

---

## Will this sequence increase show rates?

Honest answer: this is a strong floor (industry-standard 35 to 45 percent show rate for free virtual events with reminders at 48h, 24h, 1h). Three additions could push it higher:

1. **SMS reminder 30 minutes before each session.** If GHL has the contact's phone, a single line text ("Quantum Shift starts in 30 mins. Tap here: link") lifts show rates 5 to 10 percent on its own.
2. **A second 24h reminder for evening attendees specifically** (e.g. "Coming to Part 2? See you at 5pm UK"). Splitting the audience by session preference gives each cohort a more relevant nudge.
3. **Personalize subject lines with the contact's stated reason for joining** (using the form's "What brought you here?" answer). For example: "You said you wanted to feel different. Sunday is the day."

Right now the sequence below is already pulling those levers it can without SMS / segmentation. We can layer those in once the foundation is live.

---

## Shared design system

All emails use the same wrapper. Inline CSS only. 600px max-width. Tables for layout (most email-client-safe). All buttons use `{{custom_values.btw_am_session_link}}` as the href so the link can be updated from one place.

### Zoom button
```html
<a href="{{custom_values.btw_am_session_link}}" style="display:inline-block;background:#cc9924;color:#ffffff;font-family:Roboto,Arial,sans-serif;font-weight:500;font-size:13px;letter-spacing:0.12em;text-transform:uppercase;padding:16px 36px;text-decoration:none;border-radius:0;">Open Zoom &rarr;</a>
```

### Recording purchase button (gold-outline, smaller)
```html
<a href="{{custom_values.qs_event_recording}}" style="display:inline-block;background:transparent;color:#cc9924;font-family:Roboto,Arial,sans-serif;font-weight:500;font-size:11px;letter-spacing:0.12em;text-transform:uppercase;padding:10px 22px;text-decoration:none;border:1px solid #cc9924;">Get the recording &middot; $49.99</a>
```

### Logo (header)
```html
<img src="{{custom_values.logo}}" alt="Alchemy of Breath" width="160" style="display:block;margin:0 auto;height:auto;" />
```

---

## EMAIL 1 of 6 · Confirmation (T+0)

**From:** Anthony Abbagnano `<info@alchemyofbreath.com>`
**Subject:** You're in. Here's what to know about Sunday.
**Preview text:** Both Zoom links, what to have ready, and one note about the recording.

### Plain-text version

```
Hi {{first_name}},

You're in. Glad you said yes.

Quantum Shift is a full day, two live sessions, on Sunday 17 May. You're welcome at one or both. Here is everything you need.

PART 1
Sunday 17 May, 9:30 to 11:30 AM UK
Zoom: {{custom_values.btw_am_session_link}}
Meeting ID: 885 1581 3912
Passcode: Breathe

PART 2
Sunday 17 May, 5 to 7 PM UK
Same link as above.

WHAT TO HAVE READY
- A yoga mat or blanket. Somewhere you can comfortably lie down.
- A journal and pen.
- Water or tea.
- A space where you won't be interrupted, for each session.
- Your phone on do-not-disturb.

The afternoon between sessions is intentional. Don't fill it with calls or commitments if you can. Rest, move, eat something nourishing, and let the morning settle. It's part of the process.

I'll send a few short reminders before Sunday so you don't have to keep this email open.

Anthony Abbagnano
Founder, Alchemy of Breath

P.S. If life gets in the way and you can't make it live, the full recording is yours for $49.99. Both sessions, lifetime access. Grab it here: {{custom_values.qs_event_recording}}
```

### HTML version

```html
<table cellpadding="0" cellspacing="0" width="100%" style="background:#f9f8f5;padding:32px 16px;">
  <tr><td align="center">
    <table cellpadding="0" cellspacing="0" width="600" style="max-width:600px;background:#ffffff;">
      <tr><td style="padding:32px 32px 16px;text-align:center;background:#1a1a18;">
        <img src="{{custom_values.logo}}" alt="Alchemy of Breath" width="160" style="display:block;margin:0 auto;height:auto;opacity:0.95;" />
        <p style="font-family:Roboto,Arial,sans-serif;font-weight:500;font-size:10px;letter-spacing:0.22em;text-transform:uppercase;color:#cc9924;margin:18px 0 0;">Quantum Shift &middot; Sunday 17 May 2026</p>
      </td></tr>

      <tr><td style="padding:40px 32px 8px;text-align:center;">
        <h1 style="font-family:'Marcellus',Georgia,serif;font-size:32px;line-height:1.2;letter-spacing:-0.02em;color:#1a1a18;margin:0;">You're in.</h1>
        <p style="font-family:'Marcellus',Georgia,serif;font-size:20px;line-height:1.4;color:#cc9924;font-style:italic;margin:14px 0 0;">Glad you said yes.</p>
        <div style="width:40px;height:2px;background:#cc9924;margin:28px auto;"></div>
      </td></tr>

      <tr><td style="padding:0 32px 16px;font-family:Roboto,Arial,sans-serif;font-size:16px;line-height:1.7;color:#1a1a18;">
        <p style="margin:0 0 18px;">Hi {{first_name}},</p>
        <p style="margin:0 0 24px;">Quantum Shift is a full day, two live sessions, on Sunday 17 May. You're welcome at one or both. Here is everything you need.</p>
      </td></tr>

      <tr><td style="padding:0 32px 16px;">
        <table cellpadding="0" cellspacing="0" width="100%" style="background:#f9f8f5;border:1px solid #d3cdb3;">
          <tr><td style="padding:24px 26px;">
            <p style="font-family:Roboto,Arial,sans-serif;font-weight:500;font-size:10px;letter-spacing:0.22em;text-transform:uppercase;color:#cc9924;margin:0 0 8px;">Part 1</p>
            <p style="font-family:'Marcellus',Georgia,serif;font-size:20px;color:#1a1a18;margin:0 0 16px;letter-spacing:-0.01em;">Sunday 17 May, 9:30 to 11:30am UK</p>
            <a href="{{custom_values.btw_am_session_link}}" style="display:inline-block;background:#cc9924;color:#ffffff;font-family:Roboto,Arial,sans-serif;font-weight:500;font-size:13px;letter-spacing:0.12em;text-transform:uppercase;padding:14px 32px;text-decoration:none;">Open Zoom &rarr;</a>
            <p style="font-family:Roboto,Arial,sans-serif;font-size:12px;color:#4a4a46;margin:16px 0 0;line-height:1.6;">Meeting ID: 885 1581 3912<br/>Passcode: Breathe</p>
          </td></tr>
        </table>
      </td></tr>

      <tr><td style="padding:0 32px 24px;">
        <table cellpadding="0" cellspacing="0" width="100%" style="background:#f9f8f5;border:1px solid #d3cdb3;">
          <tr><td style="padding:24px 26px;">
            <p style="font-family:Roboto,Arial,sans-serif;font-weight:500;font-size:10px;letter-spacing:0.22em;text-transform:uppercase;color:#cc9924;margin:0 0 8px;">Part 2</p>
            <p style="font-family:'Marcellus',Georgia,serif;font-size:20px;color:#1a1a18;margin:0 0 16px;letter-spacing:-0.01em;">Sunday 17 May, 5 to 7pm UK</p>
            <a href="{{custom_values.btw_am_session_link}}" style="display:inline-block;background:#cc9924;color:#ffffff;font-family:Roboto,Arial,sans-serif;font-weight:500;font-size:13px;letter-spacing:0.12em;text-transform:uppercase;padding:14px 32px;text-decoration:none;">Open Zoom &rarr;</a>
            <p style="font-family:Roboto,Arial,sans-serif;font-size:12px;color:#4a4a46;margin:16px 0 0;line-height:1.6;">Same link as above. Meeting ID: 885 1581 3912 &middot; Passcode: Breathe</p>
          </td></tr>
        </table>
      </td></tr>

      <tr><td style="padding:8px 32px 24px;font-family:Roboto,Arial,sans-serif;font-size:16px;line-height:1.7;color:#4a4a46;">
        <p style="margin:0 0 14px;color:#1a1a18;font-weight:500;font-size:11px;letter-spacing:0.22em;text-transform:uppercase;">What to have ready</p>
        <p style="margin:0 0 8px;">A yoga mat or blanket. Somewhere you can comfortably lie down.</p>
        <p style="margin:0 0 8px;">A journal and pen.</p>
        <p style="margin:0 0 8px;">Water or tea.</p>
        <p style="margin:0 0 8px;">A space where you won't be interrupted, for each session.</p>
        <p style="margin:0 0 18px;">Your phone on do-not-disturb.</p>
      </td></tr>

      <tr><td style="padding:0 32px 24px;">
        <table cellpadding="0" cellspacing="0" width="100%" style="background:#f9f8f5;border-left:3px solid #cc9924;">
          <tr><td style="padding:18px 22px;">
            <p style="font-family:'Marcellus',Georgia,serif;font-size:16px;line-height:1.6;color:#1a1a18;font-style:italic;margin:0;">The afternoon between sessions is intentional. Don't fill it with calls or commitments if you can. Rest, move, eat something nourishing, and let the morning settle. It's part of the process.</p>
          </td></tr>
        </table>
      </td></tr>

      <tr><td style="padding:0 32px 28px;font-family:Roboto,Arial,sans-serif;font-size:16px;line-height:1.7;color:#4a4a46;">
        <p style="margin:0 0 18px;">I'll send a few short reminders before Sunday so you don't have to keep this email open.</p>
        <p style="margin:0 0 4px;color:#1a1a18;">Anthony Abbagnano</p>
        <p style="margin:0;font-size:14px;color:#c5c3c2;">Founder, Alchemy of Breath</p>
      </td></tr>

      <tr><td style="padding:0 32px 32px;">
        <table cellpadding="0" cellspacing="0" width="100%" style="background:rgba(204,153,36,0.06);border:1px solid rgba(204,153,36,0.3);">
          <tr><td style="padding:20px 24px;font-family:Roboto,Arial,sans-serif;font-size:14px;line-height:1.6;color:#4a4a46;">
            <p style="margin:0 0 12px;"><strong style="color:#cc9924;font-weight:500;">P.S.</strong> If life gets in the way and you can't make it live, the full recording is yours for <strong style="color:#1a1a18;">$49.99</strong>. Both sessions, lifetime access.</p>
            <a href="{{custom_values.qs_event_recording}}" style="display:inline-block;background:transparent;color:#cc9924;font-family:Roboto,Arial,sans-serif;font-weight:500;font-size:11px;letter-spacing:0.12em;text-transform:uppercase;padding:10px 22px;text-decoration:none;border:1px solid #cc9924;">Get the recording &middot; $49.99</a>
          </td></tr>
        </table>
      </td></tr>

      <tr><td style="padding:24px 32px;background:#1a1a18;text-align:center;">
        <p style="font-family:Roboto,Arial,sans-serif;font-size:11px;color:rgba(255,255,255,0.5);margin:0 0 6px;letter-spacing:0.06em;">Alchemy of Breath &middot; <a href="https://alchemyofbreath.com" style="color:rgba(255,255,255,0.5);text-decoration:none;">alchemyofbreath.com</a></p>
        <p style="font-family:Roboto,Arial,sans-serif;font-size:11px;color:rgba(255,255,255,0.3);margin:0;">You are receiving this because you registered for Quantum Shift.</p>
      </td></tr>
    </table>
  </td></tr>
</table>
```

---

## EMAIL 2 of 6 · Educational Primer (T+2 days)

**From:** Amy Rachelle `<info@alchemyofbreath.com>`
**Subject:** What nervous system regulation actually means
**Preview text:** A short primer before Sunday. From Amy.

### Plain-text version

```
Hi {{first_name}},

I want to share something with you before Sunday. Not because you need it. Because it will make Sunday make more sense.

Most of what people call "nervous system regulation" today is wellness language for "feel better." Which is fine. But what you and I are doing on Sunday is more specific than that.

Your autonomic nervous system has two main states.

Sympathetic. The gas pedal. Heart up, breath up, attention narrow, jaw tight. The system that mobilises you to act, to fight, to flee, to perform. It is not bad. It is essential.

Parasympathetic. The brake. Heart down, breath down, attention soft, body settled. The system that digests, repairs, sleeps, connects, and lets you feel safe enough to be yourself.

Most of us are not stuck in panic. We are stuck in low-grade sympathetic activation. The kind that runs in the background of an ordinary Tuesday afternoon. The kind we have come to call normal.

Regulation is not relaxation. It is the capacity to move between these two states with intention. Up when you need to act. Down when you need to recover. Without getting stuck.

The breath is the only autonomic function you can consciously control. Which makes it the steering wheel for the entire system. Slow your exhale and your parasympathetic comes online. Lengthen your inhale and your sympathetic comes up. Match the breath to the state you want and the body follows.

This is what we will do on Sunday. Not as a concept. As a practice. In your own body. With my voice and Anthony's, in real time.

If anything in this email lands, you are exactly the right person to be there.

See you Sunday.

Amy Rachelle
Co-founder, Alchemy of Breath

Your Zoom link for both sessions: {{custom_values.btw_am_session_link}}
Meeting ID: 885 1581 3912 / Passcode: Breathe

P.S. The recording is $49.99 if you'd like to keep both sessions for life: {{custom_values.qs_event_recording}}
```

### HTML version

```html
<table cellpadding="0" cellspacing="0" width="100%" style="background:#f9f8f5;padding:32px 16px;">
  <tr><td align="center">
    <table cellpadding="0" cellspacing="0" width="600" style="max-width:600px;background:#ffffff;">
      <tr><td style="padding:32px 32px 16px;text-align:center;background:#1a1a18;">
        <img src="{{custom_values.logo}}" alt="Alchemy of Breath" width="160" style="display:block;margin:0 auto;height:auto;opacity:0.95;" />
        <p style="font-family:Roboto,Arial,sans-serif;font-weight:500;font-size:10px;letter-spacing:0.22em;text-transform:uppercase;color:#cc9924;margin:18px 0 0;">Quantum Shift &middot; Before Sunday</p>
      </td></tr>

      <tr><td style="padding:40px 32px 8px;text-align:center;">
        <h1 style="font-family:'Marcellus',Georgia,serif;font-size:30px;line-height:1.25;letter-spacing:-0.02em;color:#1a1a18;margin:0;">What regulation actually means.</h1>
        <p style="font-family:Roboto,Arial,sans-serif;font-size:13px;letter-spacing:0.06em;color:#cc9924;margin:14px 0 0;">A short primer from Amy</p>
        <div style="width:40px;height:2px;background:#cc9924;margin:28px auto;"></div>
      </td></tr>

      <tr><td style="padding:0 32px 16px;font-family:Roboto,Arial,sans-serif;font-size:16px;line-height:1.75;color:#1a1a18;">
        <p style="margin:0 0 18px;">Hi {{first_name}},</p>
        <p style="margin:0 0 18px;">I want to share something with you before Sunday. Not because you need it. Because it will make Sunday make more sense.</p>
        <p style="margin:0 0 18px;color:#4a4a46;">Most of what people call &ldquo;nervous system regulation&rdquo; today is wellness language for &ldquo;feel better.&rdquo; Which is fine. But what you and I are doing on Sunday is more specific than that.</p>
        <p style="margin:0 0 18px;color:#4a4a46;">Your autonomic nervous system has two main states.</p>

        <p style="margin:0 0 8px;color:#1a1a18;font-weight:500;">Sympathetic. The gas pedal.</p>
        <p style="margin:0 0 18px;color:#4a4a46;">Heart up, breath up, attention narrow, jaw tight. The system that mobilises you to act, to fight, to flee, to perform. It is not bad. It is essential.</p>

        <p style="margin:0 0 8px;color:#1a1a18;font-weight:500;">Parasympathetic. The brake.</p>
        <p style="margin:0 0 18px;color:#4a4a46;">Heart down, breath down, attention soft, body settled. The system that digests, repairs, sleeps, connects, and lets you feel safe enough to be yourself.</p>

        <p style="margin:0 0 18px;color:#4a4a46;">Most of us are not stuck in panic. We are stuck in low-grade sympathetic activation. The kind that runs in the background of an ordinary Tuesday afternoon. The kind we have come to call <em>normal</em>.</p>
      </td></tr>

      <tr><td style="padding:16px 32px 24px;">
        <table cellpadding="0" cellspacing="0" width="100%" style="background:#f9f8f5;border-left:3px solid #cc9924;">
          <tr><td style="padding:24px 28px;">
            <p style="font-family:'Marcellus',Georgia,serif;font-size:20px;line-height:1.5;letter-spacing:-0.01em;color:#1a1a18;font-style:italic;margin:0;">Regulation is not relaxation. It is the capacity to move between these two states with intention. Up when you need to act. Down when you need to recover. Without getting stuck.</p>
          </td></tr>
        </table>
      </td></tr>

      <tr><td style="padding:8px 32px 16px;font-family:Roboto,Arial,sans-serif;font-size:16px;line-height:1.75;color:#4a4a46;">
        <p style="margin:0 0 18px;">The breath is the only autonomic function you can consciously control. Which makes it the steering wheel for the entire system. Slow your exhale and your parasympathetic comes online. Lengthen your inhale and your sympathetic comes up. Match the breath to the state you want and the body follows.</p>
        <p style="margin:0 0 18px;color:#1a1a18;">This is what we will do on Sunday. Not as a concept. As a practice. In your own body. With my voice and Anthony's, in real time.</p>
        <p style="margin:0 0 28px;color:#cc9924;font-family:'Marcellus',Georgia,serif;font-size:18px;font-style:italic;">If anything in this email lands, you are exactly the right person to be there.</p>
      </td></tr>

      <tr><td style="padding:0 32px 24px;text-align:center;">
        <a href="{{custom_values.btw_am_session_link}}" style="display:inline-block;background:#cc9924;color:#ffffff;font-family:Roboto,Arial,sans-serif;font-weight:500;font-size:13px;letter-spacing:0.12em;text-transform:uppercase;padding:14px 32px;text-decoration:none;">Open Zoom for Sunday &rarr;</a>
        <p style="font-family:Roboto,Arial,sans-serif;font-size:12px;color:#c5c3c2;margin:14px 0 0;">Same link for both Part 1 and Part 2. Meeting ID 885 1581 3912 &middot; Passcode Breathe</p>
      </td></tr>

      <tr><td style="padding:0 32px 24px;font-family:Roboto,Arial,sans-serif;font-size:16px;line-height:1.7;color:#4a4a46;">
        <p style="margin:0 0 18px;">See you Sunday.</p>
        <p style="margin:0 0 4px;color:#1a1a18;">Amy Rachelle</p>
        <p style="margin:0;font-size:14px;color:#c5c3c2;">Co-founder, Alchemy of Breath</p>
      </td></tr>

      <tr><td style="padding:0 32px 32px;">
        <table cellpadding="0" cellspacing="0" width="100%" style="background:rgba(204,153,36,0.06);border:1px solid rgba(204,153,36,0.3);">
          <tr><td style="padding:20px 24px;font-family:Roboto,Arial,sans-serif;font-size:14px;line-height:1.6;color:#4a4a46;">
            <p style="margin:0 0 12px;"><strong style="color:#cc9924;font-weight:500;">P.S.</strong> Want to keep both sessions for life? The recording is yours for $49.99.</p>
            <a href="{{custom_values.qs_event_recording}}" style="display:inline-block;background:transparent;color:#cc9924;font-family:Roboto,Arial,sans-serif;font-weight:500;font-size:11px;letter-spacing:0.12em;text-transform:uppercase;padding:10px 22px;text-decoration:none;border:1px solid #cc9924;">Get the recording &middot; $49.99</a>
          </td></tr>
        </table>
      </td></tr>

      <tr><td style="padding:24px 32px;background:#1a1a18;text-align:center;">
        <p style="font-family:Roboto,Arial,sans-serif;font-size:11px;color:rgba(255,255,255,0.5);margin:0;letter-spacing:0.06em;">Alchemy of Breath &middot; <a href="https://alchemyofbreath.com" style="color:rgba(255,255,255,0.5);text-decoration:none;">alchemyofbreath.com</a></p>
      </td></tr>
    </table>
  </td></tr>
</table>
```

---

## EMAIL 3 of 6 · 48-Hour Reminder (Friday 15 May)

**From:** Alchemy of Breath `<info@alchemyofbreath.com>`
**Subject:** Two days. Are you ready?
**Preview text:** A few small things that will make Sunday land properly.

### Plain-text version

```
Hi {{first_name}},

Two days.

We want you showing up with space cleared. Not just in your diary, in your head. The work Anthony and Amy guide people through on days like this asks for your full presence. The more you can prepare for that, the more you'll get out of it.

Your Zoom link (same for both sessions): {{custom_values.btw_am_session_link}}
Meeting ID: 885 1581 3912
Passcode: Breathe

7 small things that will make Sunday land properly:

1. Find a quiet space where you won't be disturbed. Blanket, cushions, gentle lighting.
2. Have Zoom installed and tested before Sunday morning.
3. New to conscious connected breathwork? Watch this 4-minute primer: https://youtu.be/7UjoGbeRZII
4. Headphones beat speakers if you have them.
5. Avoid heavy meals an hour before each session.
6. Journal or sketchbook nearby. Insights often arrive sideways.
7. Come with a curious mind, not a fixed goal.

See you on Sunday.

With love,
The Alchemy of Breath team

P.S. If something comes up and you can't make it live, the recording is $49.99 and yours for life. Both sessions, full audio. Grab it here: {{custom_values.qs_event_recording}}
```

### HTML version

```html
<table cellpadding="0" cellspacing="0" width="100%" style="background:#f9f8f5;padding:32px 16px;">
  <tr><td align="center">
    <table cellpadding="0" cellspacing="0" width="600" style="max-width:600px;background:#ffffff;">
      <tr><td style="padding:32px 32px 16px;text-align:center;background:#1a1a18;">
        <img src="{{custom_values.logo}}" alt="Alchemy of Breath" width="160" style="display:block;margin:0 auto;height:auto;opacity:0.95;" />
        <p style="font-family:Roboto,Arial,sans-serif;font-weight:500;font-size:10px;letter-spacing:0.22em;text-transform:uppercase;color:#cc9924;margin:18px 0 0;">Two days &middot; Sunday 17 May</p>
      </td></tr>

      <tr><td style="padding:40px 32px 8px;text-align:center;">
        <h1 style="font-family:'Marcellus',Georgia,serif;font-size:32px;line-height:1.2;letter-spacing:-0.02em;color:#1a1a18;margin:0;">Two days.</h1>
        <p style="font-family:'Marcellus',Georgia,serif;font-size:20px;line-height:1.4;color:#cc9924;font-style:italic;margin:14px 0 0;">Are you ready?</p>
        <div style="width:40px;height:2px;background:#cc9924;margin:28px auto;"></div>
      </td></tr>

      <tr><td style="padding:0 32px 16px;font-family:Roboto,Arial,sans-serif;font-size:16px;line-height:1.7;color:#1a1a18;">
        <p style="margin:0 0 18px;">Hi {{first_name}},</p>
        <p style="margin:0 0 18px;">We want you showing up with space cleared. Not just in your diary, in your head. The work Anthony and Amy guide people through on days like this asks for your full presence. The more you can prepare for that, the more you'll get out of it.</p>
      </td></tr>

      <tr><td style="padding:8px 32px 24px;text-align:center;">
        <a href="{{custom_values.btw_am_session_link}}" style="display:inline-block;background:#cc9924;color:#ffffff;font-family:Roboto,Arial,sans-serif;font-weight:500;font-size:13px;letter-spacing:0.12em;text-transform:uppercase;padding:16px 36px;text-decoration:none;">Open Zoom &rarr;</a>
        <p style="font-family:Roboto,Arial,sans-serif;font-size:12px;color:#c5c3c2;margin:14px 0 0;line-height:1.6;">Same link for both Part 1 (9:30 to 11:30am UK) and Part 2 (5 to 7pm UK)<br/>Meeting ID 885 1581 3912 &middot; Passcode Breathe</p>
      </td></tr>

      <tr><td style="padding:8px 32px 24px;font-family:Roboto,Arial,sans-serif;font-size:15px;line-height:1.75;color:#4a4a46;">
        <p style="margin:0 0 14px;color:#1a1a18;font-weight:500;font-size:11px;letter-spacing:0.22em;text-transform:uppercase;">7 small things that will make Sunday land properly</p>
        <p style="margin:0 0 14px;"><strong style="color:#1a1a18;font-weight:500;">1.</strong> Find a quiet space where you won't be disturbed. Blanket, cushions, gentle lighting.</p>
        <p style="margin:0 0 14px;"><strong style="color:#1a1a18;font-weight:500;">2.</strong> Have Zoom installed and tested before Sunday morning.</p>
        <p style="margin:0 0 14px;"><strong style="color:#1a1a18;font-weight:500;">3.</strong> New to conscious connected breathwork? <a href="https://youtu.be/7UjoGbeRZII" style="color:#cc9924;text-decoration:underline;">Watch this 4-minute primer</a>.</p>
        <p style="margin:0 0 14px;"><strong style="color:#1a1a18;font-weight:500;">4.</strong> Headphones beat speakers if you have them.</p>
        <p style="margin:0 0 14px;"><strong style="color:#1a1a18;font-weight:500;">5.</strong> Avoid heavy meals an hour before each session.</p>
        <p style="margin:0 0 14px;"><strong style="color:#1a1a18;font-weight:500;">6.</strong> Journal or sketchbook nearby. Insights often arrive sideways.</p>
        <p style="margin:0 0 18px;"><strong style="color:#1a1a18;font-weight:500;">7.</strong> Come with a curious mind, not a fixed goal.</p>
      </td></tr>

      <tr><td style="padding:0 32px 28px;font-family:Roboto,Arial,sans-serif;font-size:16px;line-height:1.7;color:#4a4a46;">
        <p style="margin:0 0 18px;">See you on Sunday.</p>
        <p style="margin:0 0 4px;color:#1a1a18;">With love,</p>
        <p style="margin:0;font-size:14px;color:#c5c3c2;">The Alchemy of Breath team</p>
      </td></tr>

      <tr><td style="padding:0 32px 32px;">
        <table cellpadding="0" cellspacing="0" width="100%" style="background:rgba(204,153,36,0.06);border:1px solid rgba(204,153,36,0.3);">
          <tr><td style="padding:20px 24px;font-family:Roboto,Arial,sans-serif;font-size:14px;line-height:1.6;color:#4a4a46;">
            <p style="margin:0 0 12px;"><strong style="color:#cc9924;font-weight:500;">P.S.</strong> If something comes up and you can't make it live, the recording is <strong style="color:#1a1a18;">$49.99</strong> and yours for life. Both sessions, full audio.</p>
            <a href="{{custom_values.qs_event_recording}}" style="display:inline-block;background:transparent;color:#cc9924;font-family:Roboto,Arial,sans-serif;font-weight:500;font-size:11px;letter-spacing:0.12em;text-transform:uppercase;padding:10px 22px;text-decoration:none;border:1px solid #cc9924;">Get the recording &middot; $49.99</a>
          </td></tr>
        </table>
      </td></tr>

      <tr><td style="padding:24px 32px;background:#1a1a18;text-align:center;">
        <p style="font-family:Roboto,Arial,sans-serif;font-size:11px;color:rgba(255,255,255,0.5);margin:0;letter-spacing:0.06em;">Alchemy of Breath &middot; <a href="https://alchemyofbreath.com" style="color:rgba(255,255,255,0.5);text-decoration:none;">alchemyofbreath.com</a></p>
      </td></tr>
    </table>
  </td></tr>
</table>
```

---

## EMAIL 4 of 6 · 24-Hour Reminder (Saturday 16 May)

**From:** Anthony Abbagnano `<info@alchemyofbreath.com>`
**Subject:** 24 hours.
**Preview text:** What to do tonight, what to do tomorrow morning.

### Plain-text version

```
{{first_name}}, we're 24 hours out.

Quantum Shift starts live on Zoom tomorrow at 9:30 AM UK. Are you the slightest bit excited? Good.

Your link (same for both sessions): {{custom_values.btw_am_session_link}}
Meeting ID: 885 1581 3912
Passcode: Breathe

Tonight or tomorrow morning, four things:

1. Block the full day. Even if you only join one session, the day matters.
2. Protect the afternoon between 12:30 and 5 PM UK if you can. The space between sessions is part of the work.
3. Find your space. Quiet. Somewhere you can lie down safely.
4. Set one intention, not a goal. What are you willing to be honest about tomorrow?

Big breath in. Big breath out. You're ready.

Anthony

P.S. Last day to lock in the recording before the live. $49.99, yours for life. {{custom_values.qs_event_recording}}
```

### HTML version

```html
<table cellpadding="0" cellspacing="0" width="100%" style="background:#f9f8f5;padding:32px 16px;">
  <tr><td align="center">
    <table cellpadding="0" cellspacing="0" width="600" style="max-width:600px;background:#ffffff;">
      <tr><td style="padding:32px 32px 16px;text-align:center;background:#1a1a18;">
        <img src="{{custom_values.logo}}" alt="Alchemy of Breath" width="160" style="display:block;margin:0 auto;height:auto;opacity:0.95;" />
        <p style="font-family:Roboto,Arial,sans-serif;font-weight:500;font-size:10px;letter-spacing:0.22em;text-transform:uppercase;color:#cc9924;margin:18px 0 0;">24 hours &middot; Tomorrow</p>
      </td></tr>

      <tr><td style="padding:40px 32px 8px;text-align:center;">
        <h1 style="font-family:'Marcellus',Georgia,serif;font-size:34px;line-height:1.2;letter-spacing:-0.02em;color:#1a1a18;margin:0;">24 hours.</h1>
        <p style="font-family:'Marcellus',Georgia,serif;font-size:20px;line-height:1.4;color:#cc9924;font-style:italic;margin:14px 0 0;">Tomorrow at 9:30 AM UK.</p>
        <div style="width:40px;height:2px;background:#cc9924;margin:28px auto;"></div>
      </td></tr>

      <tr><td style="padding:0 32px 16px;font-family:Roboto,Arial,sans-serif;font-size:16px;line-height:1.7;color:#1a1a18;">
        <p style="margin:0 0 18px;">{{first_name}}, we're 24 hours out.</p>
        <p style="margin:0 0 18px;">Quantum Shift starts live on Zoom tomorrow at 9:30 AM UK. Are you the slightest bit excited? Good.</p>
      </td></tr>

      <tr><td style="padding:8px 32px 24px;text-align:center;">
        <a href="{{custom_values.btw_am_session_link}}" style="display:inline-block;background:#cc9924;color:#ffffff;font-family:Roboto,Arial,sans-serif;font-weight:500;font-size:13px;letter-spacing:0.12em;text-transform:uppercase;padding:16px 36px;text-decoration:none;">Open Zoom &rarr;</a>
        <p style="font-family:Roboto,Arial,sans-serif;font-size:12px;color:#c5c3c2;margin:14px 0 0;line-height:1.6;">Same link for both sessions<br/>Meeting ID 885 1581 3912 &middot; Passcode Breathe</p>
      </td></tr>

      <tr><td style="padding:8px 32px 24px;font-family:Roboto,Arial,sans-serif;font-size:16px;line-height:1.75;color:#4a4a46;">
        <p style="margin:0 0 14px;color:#1a1a18;font-weight:500;font-size:11px;letter-spacing:0.22em;text-transform:uppercase;">Tonight or tomorrow morning</p>
        <p style="margin:0 0 14px;"><strong style="color:#1a1a18;font-weight:500;">1. Block the full day.</strong> Even if you only join one session, the day matters.</p>
        <p style="margin:0 0 14px;"><strong style="color:#1a1a18;font-weight:500;">2. Protect the afternoon</strong> between 12:30 and 5 PM UK if you can. The space between sessions is part of the work.</p>
        <p style="margin:0 0 14px;"><strong style="color:#1a1a18;font-weight:500;">3. Find your space.</strong> Quiet. Somewhere you can lie down safely.</p>
        <p style="margin:0 0 18px;"><strong style="color:#1a1a18;font-weight:500;">4. Set one intention, not a goal.</strong> What are you willing to be honest about tomorrow?</p>
      </td></tr>

      <tr><td style="padding:0 32px 28px;font-family:Roboto,Arial,sans-serif;font-size:16px;line-height:1.7;color:#4a4a46;">
        <p style="margin:0 0 18px;font-style:italic;">Big breath in. Big breath out. You're ready.</p>
        <p style="margin:0;color:#1a1a18;">Anthony</p>
      </td></tr>

      <tr><td style="padding:0 32px 32px;">
        <table cellpadding="0" cellspacing="0" width="100%" style="background:rgba(204,153,36,0.06);border:1px solid rgba(204,153,36,0.3);">
          <tr><td style="padding:20px 24px;font-family:Roboto,Arial,sans-serif;font-size:14px;line-height:1.6;color:#4a4a46;">
            <p style="margin:0 0 12px;"><strong style="color:#cc9924;font-weight:500;">P.S.</strong> Last day to lock in the recording before the live. <strong style="color:#1a1a18;">$49.99</strong>, yours for life.</p>
            <a href="{{custom_values.qs_event_recording}}" style="display:inline-block;background:transparent;color:#cc9924;font-family:Roboto,Arial,sans-serif;font-weight:500;font-size:11px;letter-spacing:0.12em;text-transform:uppercase;padding:10px 22px;text-decoration:none;border:1px solid #cc9924;">Get the recording &middot; $49.99</a>
          </td></tr>
        </table>
      </td></tr>

      <tr><td style="padding:24px 32px;background:#1a1a18;text-align:center;">
        <p style="font-family:Roboto,Arial,sans-serif;font-size:11px;color:rgba(255,255,255,0.5);margin:0;letter-spacing:0.06em;">Alchemy of Breath &middot; <a href="https://alchemyofbreath.com" style="color:rgba(255,255,255,0.5);text-decoration:none;">alchemyofbreath.com</a></p>
      </td></tr>
    </table>
  </td></tr>
</table>
```

---

## EMAIL 5 of 6 · Morning Day-Of (Sunday 17 May, 8:30am UK)

**From:** Alchemy of Breath `<info@alchemyofbreath.com>`
**Subject:** We start in one hour.
**Preview text:** Glass of water, blanket, headphones. We'll see you at 9:30.

### Plain-text version

```
Hi {{first_name}},

This is it. One hour and Quantum Shift starts live on Zoom with Anthony and Amy.

Take a few minutes to settle in before we open the room.

Your Zoom link: {{custom_values.btw_am_session_link}}
Meeting ID: 885 1581 3912
Passcode: Breathe

In the next 50 minutes:

- Glass of water.
- Yoga mat or blanket out, ready to lie on.
- Journal nearby.
- Phone on do-not-disturb.
- Headphones if you have them.

That's it. We'll see you inside at 9:30 AM UK.

With love,
Alchemy of Breath

P.S. The recording is $49.99 if you'd like both sessions for life: {{custom_values.qs_event_recording}}
```

### HTML version

```html
<table cellpadding="0" cellspacing="0" width="100%" style="background:#f9f8f5;padding:32px 16px;">
  <tr><td align="center">
    <table cellpadding="0" cellspacing="0" width="600" style="max-width:600px;background:#ffffff;">
      <tr><td style="padding:32px 32px 16px;text-align:center;background:#1a1a18;">
        <img src="{{custom_values.logo}}" alt="Alchemy of Breath" width="160" style="display:block;margin:0 auto;height:auto;opacity:0.95;" />
        <p style="font-family:Roboto,Arial,sans-serif;font-weight:500;font-size:10px;letter-spacing:0.22em;text-transform:uppercase;color:#cc9924;margin:18px 0 0;">Today &middot; Quantum Shift</p>
      </td></tr>

      <tr><td style="padding:40px 32px 8px;text-align:center;">
        <h1 style="font-family:'Marcellus',Georgia,serif;font-size:34px;line-height:1.2;letter-spacing:-0.02em;color:#1a1a18;margin:0;">We start in one hour.</h1>
        <p style="font-family:'Marcellus',Georgia,serif;font-size:20px;line-height:1.4;color:#cc9924;font-style:italic;margin:14px 0 0;">9:30 AM UK</p>
        <div style="width:40px;height:2px;background:#cc9924;margin:28px auto;"></div>
      </td></tr>

      <tr><td style="padding:0 32px 28px;text-align:center;">
        <a href="{{custom_values.btw_am_session_link}}" style="display:inline-block;background:#cc9924;color:#ffffff;font-family:Roboto,Arial,sans-serif;font-weight:500;font-size:14px;letter-spacing:0.12em;text-transform:uppercase;padding:18px 44px;text-decoration:none;">Open Zoom &rarr;</a>
        <p style="font-family:Roboto,Arial,sans-serif;font-size:12px;color:#c5c3c2;margin:14px 0 0;line-height:1.6;">Same link for Part 2 at 5pm UK<br/>Meeting ID 885 1581 3912 &middot; Passcode Breathe</p>
      </td></tr>

      <tr><td style="padding:8px 32px 32px;font-family:Roboto,Arial,sans-serif;font-size:16px;line-height:1.8;color:#4a4a46;">
        <p style="margin:0 0 14px;color:#1a1a18;font-weight:500;font-size:11px;letter-spacing:0.22em;text-transform:uppercase;">In the next 50 minutes</p>
        <p style="margin:0 0 8px;">Glass of water.</p>
        <p style="margin:0 0 8px;">Yoga mat or blanket out, ready to lie on.</p>
        <p style="margin:0 0 8px;">Journal nearby.</p>
        <p style="margin:0 0 8px;">Phone on do-not-disturb.</p>
        <p style="margin:0 0 18px;">Headphones if you have them.</p>
        <p style="margin:0 0 18px;">That's it. We'll see you inside at 9:30 AM UK.</p>
        <p style="margin:0 0 4px;color:#1a1a18;">With love,</p>
        <p style="margin:0;font-size:14px;color:#c5c3c2;">Alchemy of Breath</p>
      </td></tr>

      <tr><td style="padding:0 32px 32px;">
        <table cellpadding="0" cellspacing="0" width="100%" style="background:rgba(204,153,36,0.06);border:1px solid rgba(204,153,36,0.3);">
          <tr><td style="padding:18px 22px;font-family:Roboto,Arial,sans-serif;font-size:13px;line-height:1.6;color:#4a4a46;">
            <p style="margin:0;"><strong style="color:#cc9924;font-weight:500;">P.S.</strong> Want the recording? <a href="{{custom_values.qs_event_recording}}" style="color:#cc9924;text-decoration:underline;">$49.99 for both sessions, yours for life</a>.</p>
          </td></tr>
        </table>
      </td></tr>

      <tr><td style="padding:24px 32px;background:#1a1a18;text-align:center;">
        <p style="font-family:Roboto,Arial,sans-serif;font-size:11px;color:rgba(255,255,255,0.5);margin:0;letter-spacing:0.06em;">Alchemy of Breath &middot; <a href="https://alchemyofbreath.com" style="color:rgba(255,255,255,0.5);text-decoration:none;">alchemyofbreath.com</a></p>
      </td></tr>
    </table>
  </td></tr>
</table>
```

---

## EMAIL 6 of 6 · Evening Day-Of (Sunday 17 May, 4pm UK)

**From:** Anthony & Amy `<info@alchemyofbreath.com>`
**Subject:** How was the morning?
**Preview text:** Part 2 opens in one hour. This is where it deepens.

### Plain-text version

```
Hi {{first_name}},

How was the morning?

We hope you've had time to rest, move, journal, and let some of what came up in Part 1 settle.

The afternoon is part of the work too. We can't wait to see you again in the same room we spent the morning in together.

Part 2 opens in one hour. This is where things deepen. A closing breathwork journey, an integration circle, a fully regulated nervous system to end the day with.

This is the part people remember most.

Your Zoom link (same as the morning): {{custom_values.btw_am_session_link}}
Meeting ID: 885 1581 3912
Passcode: Breathe

See you in an hour.

With love,
Anthony & Amy

P.S. Missed the morning? The recording captures both sessions. $49.99, yours for life: {{custom_values.qs_event_recording}}
```

### HTML version

```html
<table cellpadding="0" cellspacing="0" width="100%" style="background:#f9f8f5;padding:32px 16px;">
  <tr><td align="center">
    <table cellpadding="0" cellspacing="0" width="600" style="max-width:600px;background:#ffffff;">
      <tr><td style="padding:32px 32px 16px;text-align:center;background:#1a1a18;">
        <img src="{{custom_values.logo}}" alt="Alchemy of Breath" width="160" style="display:block;margin:0 auto;height:auto;opacity:0.95;" />
        <p style="font-family:Roboto,Arial,sans-serif;font-weight:500;font-size:10px;letter-spacing:0.22em;text-transform:uppercase;color:#cc9924;margin:18px 0 0;">Part 2 &middot; In one hour</p>
      </td></tr>

      <tr><td style="padding:40px 32px 8px;text-align:center;">
        <h1 style="font-family:'Marcellus',Georgia,serif;font-size:32px;line-height:1.2;letter-spacing:-0.02em;color:#1a1a18;margin:0;">How was the morning?</h1>
        <p style="font-family:'Marcellus',Georgia,serif;font-size:20px;line-height:1.4;color:#cc9924;font-style:italic;margin:14px 0 0;">Part 2 starts at 5 PM UK.</p>
        <div style="width:40px;height:2px;background:#cc9924;margin:28px auto;"></div>
      </td></tr>

      <tr><td style="padding:0 32px 16px;font-family:Roboto,Arial,sans-serif;font-size:16px;line-height:1.75;color:#1a1a18;">
        <p style="margin:0 0 18px;">Hi {{first_name}},</p>
        <p style="margin:0 0 18px;color:#4a4a46;">We hope you've had time to rest, move, journal, and let some of what came up in Part 1 settle.</p>
        <p style="margin:0 0 18px;color:#4a4a46;">The afternoon is part of the work too. We can't wait to see you again in the same room we spent the morning in together.</p>
        <p style="margin:0 0 18px;">Part 2 opens in one hour. This is where things deepen. A closing breathwork journey, an integration circle, a fully regulated nervous system to end the day with.</p>
        <p style="margin:0 0 24px;color:#cc9924;font-family:'Marcellus',Georgia,serif;font-size:18px;font-style:italic;">This is the part people remember most.</p>
      </td></tr>

      <tr><td style="padding:0 32px 28px;text-align:center;">
        <a href="{{custom_values.btw_am_session_link}}" style="display:inline-block;background:#cc9924;color:#ffffff;font-family:Roboto,Arial,sans-serif;font-weight:500;font-size:14px;letter-spacing:0.12em;text-transform:uppercase;padding:18px 44px;text-decoration:none;">Open Zoom &rarr;</a>
        <p style="font-family:Roboto,Arial,sans-serif;font-size:12px;color:#c5c3c2;margin:14px 0 0;line-height:1.6;">Same link as the morning<br/>Meeting ID 885 1581 3912 &middot; Passcode Breathe</p>
      </td></tr>

      <tr><td style="padding:8px 32px 32px;font-family:Roboto,Arial,sans-serif;font-size:16px;line-height:1.7;color:#4a4a46;">
        <p style="margin:0 0 18px;">See you in an hour.</p>
        <p style="margin:0 0 4px;color:#1a1a18;">With love,</p>
        <p style="margin:0;font-size:14px;color:#c5c3c2;">Anthony &amp; Amy</p>
      </td></tr>

      <tr><td style="padding:0 32px 32px;">
        <table cellpadding="0" cellspacing="0" width="100%" style="background:rgba(204,153,36,0.06);border:1px solid rgba(204,153,36,0.3);">
          <tr><td style="padding:20px 24px;font-family:Roboto,Arial,sans-serif;font-size:14px;line-height:1.6;color:#4a4a46;">
            <p style="margin:0 0 12px;"><strong style="color:#cc9924;font-weight:500;">P.S.</strong> Missed the morning? The recording captures both sessions. <strong style="color:#1a1a18;">$49.99</strong>, yours for life.</p>
            <a href="{{custom_values.qs_event_recording}}" style="display:inline-block;background:transparent;color:#cc9924;font-family:Roboto,Arial,sans-serif;font-weight:500;font-size:11px;letter-spacing:0.12em;text-transform:uppercase;padding:10px 22px;text-decoration:none;border:1px solid #cc9924;">Get the recording &middot; $49.99</a>
          </td></tr>
        </table>
      </td></tr>

      <tr><td style="padding:24px 32px;background:#1a1a18;text-align:center;">
        <p style="font-family:Roboto,Arial,sans-serif;font-size:11px;color:rgba(255,255,255,0.5);margin:0;letter-spacing:0.06em;">Alchemy of Breath &middot; <a href="https://alchemyofbreath.com" style="color:rgba(255,255,255,0.5);text-decoration:none;">alchemyofbreath.com</a></p>
      </td></tr>
    </table>
  </td></tr>
</table>
```

---

## Setup checklist in GHL

- [ ] Trigger: form submission on `JXFlOEgAhMoElAqLBG1L`
- [ ] Step 1: Send Email 1 (Confirmation) immediately
- [ ] Step 2: Wait 2 days, send Email 2 (Educational primer from Amy)
- [ ] Step 3: Wait until Friday 15 May 9am UK, send Email 3 (48-hour reminder)
- [ ] Step 4: Wait until Saturday 16 May 9:30am UK, send Email 4 (24-hour reminder)
- [ ] Step 5: Wait until Sunday 17 May 8:30am UK, send Email 5 (Part 1 morning reminder)
- [ ] Step 6: Wait until Sunday 17 May 4pm UK, send Email 6 (Part 2 evening reminder)
- [ ] Configure these custom values in GHL:
  - `{{custom_values.logo}}` = AoB logo URL
  - `{{custom_values.btw_am_session_link}}` = Zoom link `https://us06web.zoom.us/j/88515813912?pwd=d2JjSjhsOWhneVZWQWVkc0h0aTh2QT09`
  - `{{custom_values.qs_event_recording}}` = Stripe / GHL payment link for $49.99 recording
- [ ] Exit conditions: contact buys recording (tag `quantum-shift-recording-purchased`), unsubscribes, or has tag `quantum-shift-attended-live`

## Post-event follow-ups (separate sequence, draft separately)

- T+12h after evening session: "Did you feel that?" with what's-next pitch
- T+2 days: Recording delivery email for everyone who could not attend, with $49.99 purchase link
- T+5 days: Final what's-next push for non-converters

## Optional show-rate boosters (not in current sequence)

- **SMS at 30 minutes before each session** if GHL has phone numbers. Single line: "Quantum Shift starts in 30 mins. Tap here: [link]". 5 to 10 percent show rate lift on its own.
- **Segmented evening reminder** for people who said in the form they could only attend the evening session, sent earlier in the day.
- **Personalize subject lines using their "What brought you here?" answer.** People who said "I am exhausted" get "You said you wanted to feel different. Today is the day."
