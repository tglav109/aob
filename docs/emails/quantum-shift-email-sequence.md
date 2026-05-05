# Quantum Shift Email Sequence

**Event:** Quantum Shift, Sunday 17 May 2026
**Sessions:** 9:30 to 11:30am UK  ·  5 to 7pm UK
**Trigger form:** GHL form `JXFlOEgAhMoElAqLBG1L` (AOB | Event: QS Optin | ARM)
**Brand:** Alchemy of Breath. Marcellus + Roboto. Gold #cc9924, teal #354d4c, ink #1a1a18, off-white #f9f8f5. **Zero em dashes.**

---

## Sequence at a glance

| # | Send | Timing | From | Subject | Purpose |
|---|------|--------|------|---------|---------|
| 1 | T+0 | Immediate on form submit | Anthony Abbagnano | You are in. Quantum Shift, Sunday 17 May | Confirm + calendar invite + soft recording mention |
| 2 | T+2 days | After they have settled | Amy Rachelle, ND | What nervous system regulation actually means | Educational primer that earns trust + frames Sunday |
| 3 | T-1 day (Saturday 16 May) | 24h before | Anthony Abbagnano | Tomorrow. Part 1 at 9:30am or Part 2 at 5pm UK | Reminder + what to prepare |
| 4 | Sunday 17 May, 7am UK | 2h before morning session | Alchemy of Breath | Quantum Shift starts in 2 hours | Final morning reminder + access link |
| 5 | Sunday 17 May, 4pm UK | 1h before evening session | Alchemy of Breath | Evening session in 1 hour | Final evening reminder |

**Reset:** Drop anyone from the sequence as soon as they unsubscribe or buy the recording (so they do not get day-of reminders for an event they cannot attend).

---

## Shared design system (paste into every email)

All emails use the same wrapper. Inline CSS only. 600px max-width. Tables for layout (most email-client-safe).

### Colours
- Background: `#f9f8f5`
- Card: `#ffffff`
- Text: `#1a1a18`
- Soft text: `#4a4a46`
- Gold accent: `#cc9924`
- Teal nav: `#354d4c`
- Gold rule (40px divider): `<div style="width:40px;height:2px;background:#cc9924;margin:24px auto;"></div>`

### Fonts
- Headings: `'Marcellus', Georgia, 'Times New Roman', serif`
- Body: `'Roboto', 'Helvetica Neue', Arial, sans-serif`
- Most email clients will fall back to Georgia / Arial. That is fine. The pairing still holds.

### Buttons
```html
<a href="{{cta_url}}" style="display:inline-block;background:#cc9924;color:#ffffff;font-family:Roboto,Arial,sans-serif;font-weight:500;font-size:13px;letter-spacing:0.12em;text-transform:uppercase;padding:14px 32px;text-decoration:none;border-radius:0;">{{Button text}}</a>
```

### Logo (header)
```html
<img src="{{custom_values.logo}}" alt="Alchemy of Breath" width="160" style="display:block;margin:0 auto;height:auto;" />
```

---

## EMAIL 1 of 5 · Confirmation (T+0)

**From:** Anthony Abbagnano `<info@alchemyofbreath.com>`
**Subject:** You are in. Quantum Shift, Sunday 17 May.
**Preview text:** The live link, the calendar invite, and one note about the recording.

### Plain-text version (for clients that strip HTML)

```
Hi {{first_name}},

You are in. Quantum Shift, Sunday 17 May.

Two live sessions:
  9:30 to 11:30am UK
  5 to 7pm UK

You can come to either or both. Same content, different time of day.

Three things to know:

1. Your live access link is in your calendar invite. Add it to your calendar now so it does not get lost. The link is the same for both sessions.

2. To get the most from Sunday, find a quiet 90-minute window. A blanket. A glass of water. A space where you will not be interrupted. Phone on do not disturb. Headphones if you can.

3. Both sessions will be recorded. If life gets in the way and you cannot make it live, you will be able to purchase the recording for $49.99 after the event. We will send you the link.

That is it. The most important thing right now is not what I write. It is what your body does on Sunday.

Anthony Abbagnano
Founder, Alchemy of Breath

PS. Please reply if you have a question. I read every reply.
```

### HTML version (paste into GHL email body)

```html
<table cellpadding="0" cellspacing="0" width="100%" style="background:#f9f8f5;padding:32px 16px;">
  <tr><td align="center">
    <table cellpadding="0" cellspacing="0" width="600" style="max-width:600px;background:#ffffff;">
      <!-- Header -->
      <tr><td style="padding:32px 32px 16px;text-align:center;background:#1a1a18;">
        <img src="{{custom_values.logo}}" alt="Alchemy of Breath" width="160" style="display:block;margin:0 auto;height:auto;opacity:0.95;" />
        <p style="font-family:Roboto,Arial,sans-serif;font-weight:500;font-size:10px;letter-spacing:0.22em;text-transform:uppercase;color:#cc9924;margin:18px 0 0;">Quantum Shift &middot; Sunday 17 May 2026</p>
      </td></tr>

      <!-- Headline -->
      <tr><td style="padding:40px 32px 8px;text-align:center;">
        <h1 style="font-family:'Marcellus',Georgia,serif;font-size:32px;line-height:1.2;letter-spacing:-0.02em;color:#1a1a18;margin:0;">You are in.</h1>
        <p style="font-family:'Marcellus',Georgia,serif;font-size:20px;line-height:1.4;color:#cc9924;font-style:italic;margin:14px 0 0;">Two live sessions. Sunday 17 May.</p>
        <div style="width:40px;height:2px;background:#cc9924;margin:28px auto;"></div>
      </td></tr>

      <!-- Greeting + body -->
      <tr><td style="padding:0 32px 16px;font-family:Roboto,Arial,sans-serif;font-size:16px;line-height:1.7;color:#1a1a18;">
        <p style="margin:0 0 18px;">Hi {{first_name}},</p>
        <p style="margin:0 0 18px;">You are in. Two live breathwork sessions, both led by me and Amy Rachelle, ND. Same content, different time of day. You can come to either or both.</p>
      </td></tr>

      <!-- Session times card -->
      <tr><td style="padding:8px 32px 24px;">
        <table cellpadding="0" cellspacing="0" width="100%" style="background:#f9f8f5;border:1px solid #d3cdb3;">
          <tr><td style="padding:22px 24px;">
            <p style="font-family:Roboto,Arial,sans-serif;font-weight:500;font-size:10px;letter-spacing:0.22em;text-transform:uppercase;color:#cc9924;margin:0 0 12px;">Your sessions</p>
            <p style="font-family:'Marcellus',Georgia,serif;font-size:18px;color:#1a1a18;margin:0 0 6px;letter-spacing:-0.01em;">Morning &middot; 9:30 to 11:30am UK</p>
            <p style="font-family:'Marcellus',Georgia,serif;font-size:18px;color:#1a1a18;margin:0;letter-spacing:-0.01em;">Evening &middot; 5 to 7pm UK</p>
          </td></tr>
        </table>
      </td></tr>

      <!-- Three things to know -->
      <tr><td style="padding:8px 32px 24px;font-family:Roboto,Arial,sans-serif;font-size:16px;line-height:1.7;color:#4a4a46;">
        <p style="margin:0 0 18px;color:#1a1a18;font-weight:500;">Three things to know:</p>
        <p style="margin:0 0 18px;"><strong style="color:#1a1a18;font-weight:500;">1. Your live access link is in your calendar invite.</strong> Add it to your calendar now so it does not get lost. The link is the same for both sessions.</p>
        <p style="margin:0 0 18px;"><strong style="color:#1a1a18;font-weight:500;">2. To get the most from Sunday, find a quiet 90-minute window.</strong> A blanket. A glass of water. A space where you will not be interrupted. Phone on do not disturb. Headphones if you can.</p>
        <p style="margin:0 0 18px;"><strong style="color:#1a1a18;font-weight:500;">3. Both sessions will be recorded.</strong> If life gets in the way and you cannot make it live, you will be able to purchase the recording for $49.99 after the event. We will send you the link.</p>
      </td></tr>

      <!-- CTA -->
      <tr><td style="padding:8px 32px 32px;text-align:center;">
        <a href="{{calendar_invite_url}}" style="display:inline-block;background:#cc9924;color:#ffffff;font-family:Roboto,Arial,sans-serif;font-weight:500;font-size:13px;letter-spacing:0.12em;text-transform:uppercase;padding:14px 32px;text-decoration:none;">Add to calendar</a>
      </td></tr>

      <!-- Closing -->
      <tr><td style="padding:8px 32px 32px;font-family:Roboto,Arial,sans-serif;font-size:16px;line-height:1.7;color:#4a4a46;">
        <p style="margin:0 0 18px;">That is it. The most important thing right now is not what I write. It is what your body does on Sunday.</p>
        <p style="margin:0 0 8px;color:#1a1a18;">Anthony Abbagnano</p>
        <p style="margin:0;font-size:14px;color:#c5c3c2;">Founder, Alchemy of Breath</p>
        <p style="margin:24px 0 0;font-size:14px;color:#4a4a46;font-style:italic;">PS. Please reply if you have a question. I read every reply.</p>
      </td></tr>

      <!-- Footer -->
      <tr><td style="padding:24px 32px;background:#1a1a18;text-align:center;">
        <p style="font-family:Roboto,Arial,sans-serif;font-size:11px;color:rgba(255,255,255,0.5);margin:0 0 6px;letter-spacing:0.06em;">Alchemy of Breath &middot; <a href="https://alchemyofbreath.com" style="color:rgba(255,255,255,0.5);text-decoration:none;">alchemyofbreath.com</a></p>
        <p style="font-family:Roboto,Arial,sans-serif;font-size:11px;color:rgba(255,255,255,0.3);margin:0;">You are receiving this because you registered for Quantum Shift.</p>
      </td></tr>
    </table>
  </td></tr>
</table>
```

---

## EMAIL 2 of 5 · Educational Primer (T+2 days)

**From:** Amy Rachelle, ND `<amy@alchemyofbreath.com>`
**Subject:** What nervous system regulation actually means
**Preview text:** A short primer before Sunday. From Amy.

### Plain-text version

```
Hi {{first_name}},

I want to share something with you before Sunday. Not because you need it. Because it will make Sunday make more sense.

Most of what people call "nervous system regulation" today is wellness language for "feel better." Which is fine. But what you and I are actually doing on Sunday is more specific than that.

Your autonomic nervous system has two main states.

Sympathetic. The gas pedal. Heart up, breath up, attention narrow, jaw tight. This is the system that mobilises you to act, to fight, to flee, to perform. It is not bad. It is essential.

Parasympathetic. The brake. Heart down, breath down, attention soft, body settled. This is the system that digests, repairs, sleeps, connects, and lets you feel safe enough to be yourself.

Most of us are not stuck in panic. We are stuck in low-grade sympathetic activation. The kind that runs in the background of an ordinary Tuesday afternoon. The kind we have come to call "normal."

Regulation is not relaxation. It is the capacity to move between these two states with intention. Up when you need to act. Down when you need to recover. Without getting stuck.

The breath is the only autonomic function you can consciously control. Which means it is the steering wheel for the entire system. Slow your exhale and your parasympathetic comes online. Lengthen your inhale and your sympathetic comes up. Match the breath to the state you want and the body follows.

This is what we will do on Sunday. Not as a concept. As a practice. In your own body. With my voice and Anthony's, in real time.

If anything in this email lands, you are exactly the right person to be there.

See you Sunday.

Amy Rachelle, ND
Co-founder, Alchemy of Breath
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
        <p style="margin:0 0 18px;color:#4a4a46;">Most of what people call &ldquo;nervous system regulation&rdquo; today is wellness language for &ldquo;feel better.&rdquo; Which is fine. But what you and I are actually doing on Sunday is more specific than that.</p>
        <p style="margin:0 0 18px;color:#4a4a46;">Your autonomic nervous system has two main states.</p>

        <p style="margin:0 0 8px;color:#1a1a18;font-weight:500;">Sympathetic. The gas pedal.</p>
        <p style="margin:0 0 18px;color:#4a4a46;">Heart up, breath up, attention narrow, jaw tight. This is the system that mobilises you to act, to fight, to flee, to perform. It is not bad. It is essential.</p>

        <p style="margin:0 0 8px;color:#1a1a18;font-weight:500;">Parasympathetic. The brake.</p>
        <p style="margin:0 0 18px;color:#4a4a46;">Heart down, breath down, attention soft, body settled. This is the system that digests, repairs, sleeps, connects, and lets you feel safe enough to be yourself.</p>

        <p style="margin:0 0 18px;color:#4a4a46;">Most of us are not stuck in panic. We are stuck in low-grade sympathetic activation. The kind that runs in the background of an ordinary Tuesday afternoon. The kind we have come to call <em>normal</em>.</p>
      </td></tr>

      <!-- Pull quote -->
      <tr><td style="padding:16px 32px 24px;">
        <table cellpadding="0" cellspacing="0" width="100%" style="background:#f9f8f5;border-left:3px solid #cc9924;">
          <tr><td style="padding:24px 28px;">
            <p style="font-family:'Marcellus',Georgia,serif;font-size:20px;line-height:1.5;letter-spacing:-0.01em;color:#1a1a18;font-style:italic;margin:0;">Regulation is not relaxation. It is the capacity to move between these two states with intention. Up when you need to act. Down when you need to recover. Without getting stuck.</p>
          </td></tr>
        </table>
      </td></tr>

      <tr><td style="padding:8px 32px 16px;font-family:Roboto,Arial,sans-serif;font-size:16px;line-height:1.75;color:#4a4a46;">
        <p style="margin:0 0 18px;">The breath is the only autonomic function you can consciously control. Which means it is the steering wheel for the entire system. Slow your exhale and your parasympathetic comes online. Lengthen your inhale and your sympathetic comes up. Match the breath to the state you want and the body follows.</p>
        <p style="margin:0 0 18px;color:#1a1a18;">This is what we will do on Sunday. Not as a concept. As a practice. In your own body. With my voice and Anthony&rsquo;s, in real time.</p>
        <p style="margin:0 0 28px;color:#cc9924;font-family:'Marcellus',Georgia,serif;font-size:18px;font-style:italic;">If anything in this email lands, you are exactly the right person to be there.</p>
      </td></tr>

      <tr><td style="padding:0 32px 32px;font-family:Roboto,Arial,sans-serif;font-size:16px;line-height:1.7;color:#4a4a46;">
        <p style="margin:0 0 18px;">See you Sunday.</p>
        <p style="margin:0 0 4px;color:#1a1a18;">Amy Rachelle, ND</p>
        <p style="margin:0;font-size:14px;color:#c5c3c2;">Co-founder, Alchemy of Breath</p>
      </td></tr>

      <tr><td style="padding:24px 32px;background:#1a1a18;text-align:center;">
        <p style="font-family:Roboto,Arial,sans-serif;font-size:11px;color:rgba(255,255,255,0.5);margin:0 0 6px;letter-spacing:0.06em;">Alchemy of Breath &middot; <a href="https://alchemyofbreath.com" style="color:rgba(255,255,255,0.5);text-decoration:none;">alchemyofbreath.com</a></p>
      </td></tr>
    </table>
  </td></tr>
</table>
```

---

## EMAIL 3 of 5 · Day-Before Reminder (T-1, Saturday 16 May)

**From:** Anthony Abbagnano `<info@alchemyofbreath.com>`
**Subject:** Tomorrow. Part 1 at 9:30am or Part 2 at 5pm UK.
**Preview text:** A short note from Anthony before we sit together.

### Plain-text version

```
Hi {{first_name}},

A quick note before tomorrow.

Two live sessions:
  Morning: 9:30 to 11:30am UK
  Evening: 5 to 7pm UK

Same content, different time of day. Come to either or both.

Three things that will make tomorrow easier:

A quiet 90 minutes. Tell the people in your house. Phone on do not disturb. The work is gentle, but interruptions break the thread.

A blanket and a glass of water. The body settles fastest when it is warm and hydrated.

Headphones if you have them. Especially for the evening session. The voice gets in deeper.

The live link is in your calendar invite. The same link works for both sessions.

If you cannot make tomorrow, do not unsubscribe. We will email you the recording link after the event ($49.99) and you can practice on your own time.

Tomorrow.

Anthony
```

### HTML version

```html
<table cellpadding="0" cellspacing="0" width="100%" style="background:#f9f8f5;padding:32px 16px;">
  <tr><td align="center">
    <table cellpadding="0" cellspacing="0" width="600" style="max-width:600px;background:#ffffff;">
      <tr><td style="padding:32px 32px 16px;text-align:center;background:#1a1a18;">
        <img src="{{custom_values.logo}}" alt="Alchemy of Breath" width="160" style="display:block;margin:0 auto;height:auto;opacity:0.95;" />
        <p style="font-family:Roboto,Arial,sans-serif;font-weight:500;font-size:10px;letter-spacing:0.22em;text-transform:uppercase;color:#cc9924;margin:18px 0 0;">Tomorrow &middot; Sunday 17 May</p>
      </td></tr>

      <tr><td style="padding:40px 32px 8px;text-align:center;">
        <h1 style="font-family:'Marcellus',Georgia,serif;font-size:32px;line-height:1.2;letter-spacing:-0.02em;color:#1a1a18;margin:0;">Tomorrow.</h1>
        <p style="font-family:'Marcellus',Georgia,serif;font-size:20px;line-height:1.4;color:#cc9924;font-style:italic;margin:10px 0 0;">9:30am UK or 5pm UK.</p>
        <div style="width:40px;height:2px;background:#cc9924;margin:28px auto;"></div>
      </td></tr>

      <tr><td style="padding:0 32px 24px;font-family:Roboto,Arial,sans-serif;font-size:16px;line-height:1.7;color:#1a1a18;">
        <p style="margin:0 0 18px;">Hi {{first_name}},</p>
        <p style="margin:0 0 18px;">A quick note before tomorrow.</p>
      </td></tr>

      <tr><td style="padding:0 32px 24px;">
        <table cellpadding="0" cellspacing="0" width="100%" style="background:#f9f8f5;border:1px solid #d3cdb3;">
          <tr><td style="padding:22px 24px;">
            <p style="font-family:Roboto,Arial,sans-serif;font-weight:500;font-size:10px;letter-spacing:0.22em;text-transform:uppercase;color:#cc9924;margin:0 0 12px;">Two sessions</p>
            <p style="font-family:'Marcellus',Georgia,serif;font-size:17px;color:#1a1a18;margin:0 0 6px;letter-spacing:-0.01em;">Morning &middot; 9:30 to 11:30am UK</p>
            <p style="font-family:'Marcellus',Georgia,serif;font-size:17px;color:#1a1a18;margin:0;letter-spacing:-0.01em;">Evening &middot; 5 to 7pm UK</p>
            <p style="font-family:Roboto,Arial,sans-serif;font-size:13px;color:#4a4a46;margin:14px 0 0;">Same content, different time of day. Come to either or both.</p>
          </td></tr>
        </table>
      </td></tr>

      <tr><td style="padding:8px 32px 24px;font-family:Roboto,Arial,sans-serif;font-size:16px;line-height:1.7;color:#4a4a46;">
        <p style="margin:0 0 18px;color:#1a1a18;font-weight:500;">Three things that will make tomorrow easier:</p>
        <p style="margin:0 0 16px;"><strong style="color:#1a1a18;font-weight:500;">A quiet 90 minutes.</strong> Tell the people in your house. Phone on do not disturb. The work is gentle, but interruptions break the thread.</p>
        <p style="margin:0 0 16px;"><strong style="color:#1a1a18;font-weight:500;">A blanket and a glass of water.</strong> The body settles fastest when it is warm and hydrated.</p>
        <p style="margin:0 0 18px;"><strong style="color:#1a1a18;font-weight:500;">Headphones if you have them.</strong> Especially for the evening session. The voice gets in deeper.</p>
      </td></tr>

      <tr><td style="padding:8px 32px 32px;text-align:center;">
        <a href="{{calendar_invite_url}}" style="display:inline-block;background:#cc9924;color:#ffffff;font-family:Roboto,Arial,sans-serif;font-weight:500;font-size:13px;letter-spacing:0.12em;text-transform:uppercase;padding:14px 32px;text-decoration:none;">Open my calendar invite</a>
        <p style="font-family:Roboto,Arial,sans-serif;font-size:12px;color:#c5c3c2;margin:14px 0 0;">The same link works for both sessions.</p>
      </td></tr>

      <tr><td style="padding:8px 32px 32px;font-family:Roboto,Arial,sans-serif;font-size:15px;line-height:1.7;color:#4a4a46;">
        <p style="margin:0 0 18px;font-style:italic;">If you cannot make tomorrow, do not unsubscribe. We will email you the recording link after the event ($49.99) and you can practice on your own time.</p>
        <p style="margin:0 0 18px;color:#1a1a18;">Tomorrow.</p>
        <p style="margin:0;color:#1a1a18;">Anthony</p>
      </td></tr>

      <tr><td style="padding:24px 32px;background:#1a1a18;text-align:center;">
        <p style="font-family:Roboto,Arial,sans-serif;font-size:11px;color:rgba(255,255,255,0.5);margin:0;letter-spacing:0.06em;">Alchemy of Breath &middot; <a href="https://alchemyofbreath.com" style="color:rgba(255,255,255,0.5);text-decoration:none;">alchemyofbreath.com</a></p>
      </td></tr>
    </table>
  </td></tr>
</table>
```

---

## EMAIL 4 of 5 · 2 Hours Before Morning Session (Sunday 17 May, 7am UK)

**From:** Alchemy of Breath `<info@alchemyofbreath.com>`
**Subject:** Quantum Shift starts in 2 hours
**Preview text:** 9:30 to 11:30am UK. Here is your link.

### Plain-text version

```
Hi {{first_name}},

We start in 2 hours.

  9:30 to 11:30am UK

Your live link: {{custom_values.btw_am_session_link}}

The same link works for the evening session. Bookmark it.

In the next hour:

A glass of water.
A blanket.
A quiet space.
Phone on do not disturb.

That is it. We will see you in 2 hours.

Anthony &amp; Amy
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
        <h1 style="font-family:'Marcellus',Georgia,serif;font-size:34px;line-height:1.2;letter-spacing:-0.02em;color:#1a1a18;margin:0;">We start in 2 hours.</h1>
        <p style="font-family:'Marcellus',Georgia,serif;font-size:20px;line-height:1.4;color:#cc9924;font-style:italic;margin:14px 0 0;">9:30 to 11:30am UK</p>
        <div style="width:40px;height:2px;background:#cc9924;margin:28px auto;"></div>
      </td></tr>

      <tr><td style="padding:0 32px 28px;text-align:center;">
        <a href="{{custom_values.btw_am_session_link}}" style="display:inline-block;background:#cc9924;color:#ffffff;font-family:Roboto,Arial,sans-serif;font-weight:500;font-size:14px;letter-spacing:0.12em;text-transform:uppercase;padding:18px 44px;text-decoration:none;">Open the live link</a>
        <p style="font-family:Roboto,Arial,sans-serif;font-size:12px;color:#c5c3c2;margin:14px 0 0;">The same link works for the evening session at 5pm UK.</p>
      </td></tr>

      <tr><td style="padding:8px 32px 32px;font-family:Roboto,Arial,sans-serif;font-size:16px;line-height:1.8;color:#4a4a46;">
        <p style="margin:0 0 16px;color:#1a1a18;font-weight:500;">In the next hour:</p>
        <p style="margin:0 0 8px;">A glass of water.</p>
        <p style="margin:0 0 8px;">A blanket.</p>
        <p style="margin:0 0 8px;">A quiet space.</p>
        <p style="margin:0 0 18px;">Phone on do not disturb.</p>
        <p style="margin:0 0 18px;">That is it. We will see you in 2 hours.</p>
        <p style="margin:0;color:#1a1a18;">Anthony &amp; Amy</p>
      </td></tr>

      <tr><td style="padding:24px 32px;background:#1a1a18;text-align:center;">
        <p style="font-family:Roboto,Arial,sans-serif;font-size:11px;color:rgba(255,255,255,0.5);margin:0;letter-spacing:0.06em;">Alchemy of Breath &middot; <a href="https://alchemyofbreath.com" style="color:rgba(255,255,255,0.5);text-decoration:none;">alchemyofbreath.com</a></p>
      </td></tr>
    </table>
  </td></tr>
</table>
```

---

## EMAIL 5 of 5 · 1 Hour Before Evening Session (Sunday 17 May, 4pm UK)

**From:** Alchemy of Breath `<info@alchemyofbreath.com>`
**Subject:** Evening session in 1 hour
**Preview text:** 5 to 7pm UK. The link is below.

### Plain-text version

```
Hi {{first_name}},

Evening session in 1 hour.

  5 to 7pm UK

Your live link: {{custom_values.btw_am_session_link}}

If you came to the morning, welcome back. If this is your first session, welcome.

Glass of water. Blanket. Quiet space.

See you at 5pm UK.

Anthony &amp; Amy
```

### HTML version

```html
<table cellpadding="0" cellspacing="0" width="100%" style="background:#f9f8f5;padding:32px 16px;">
  <tr><td align="center">
    <table cellpadding="0" cellspacing="0" width="600" style="max-width:600px;background:#ffffff;">
      <tr><td style="padding:32px 32px 16px;text-align:center;background:#1a1a18;">
        <img src="{{custom_values.logo}}" alt="Alchemy of Breath" width="160" style="display:block;margin:0 auto;height:auto;opacity:0.95;" />
        <p style="font-family:Roboto,Arial,sans-serif;font-weight:500;font-size:10px;letter-spacing:0.22em;text-transform:uppercase;color:#cc9924;margin:18px 0 0;">Today &middot; Evening session</p>
      </td></tr>

      <tr><td style="padding:40px 32px 8px;text-align:center;">
        <h1 style="font-family:'Marcellus',Georgia,serif;font-size:34px;line-height:1.2;letter-spacing:-0.02em;color:#1a1a18;margin:0;">In 1 hour.</h1>
        <p style="font-family:'Marcellus',Georgia,serif;font-size:20px;line-height:1.4;color:#cc9924;font-style:italic;margin:14px 0 0;">5 to 7pm UK</p>
        <div style="width:40px;height:2px;background:#cc9924;margin:28px auto;"></div>
      </td></tr>

      <tr><td style="padding:0 32px 28px;text-align:center;">
        <a href="{{custom_values.btw_am_session_link}}" style="display:inline-block;background:#cc9924;color:#ffffff;font-family:Roboto,Arial,sans-serif;font-weight:500;font-size:14px;letter-spacing:0.12em;text-transform:uppercase;padding:18px 44px;text-decoration:none;">Open the live link</a>
      </td></tr>

      <tr><td style="padding:8px 32px 32px;font-family:Roboto,Arial,sans-serif;font-size:16px;line-height:1.8;color:#4a4a46;text-align:center;">
        <p style="margin:0 0 18px;">If you came to the morning, welcome back.<br/>If this is your first session, welcome.</p>
        <p style="margin:0 0 18px;color:#1a1a18;">Glass of water. Blanket. Quiet space.</p>
        <p style="margin:0 0 18px;">See you at 5pm UK.</p>
        <p style="margin:0;color:#1a1a18;">Anthony &amp; Amy</p>
      </td></tr>

      <tr><td style="padding:24px 32px;background:#1a1a18;text-align:center;">
        <p style="font-family:Roboto,Arial,sans-serif;font-size:11px;color:rgba(255,255,255,0.5);margin:0;letter-spacing:0.06em;">Alchemy of Breath &middot; <a href="https://alchemyofbreath.com" style="color:rgba(255,255,255,0.5);text-decoration:none;">alchemyofbreath.com</a></p>
      </td></tr>
    </table>
  </td></tr>
</table>
```

---

## Merge tags reference (for GHL)

Replace these placeholders inside GHL's email editor with your actual contact / event field references:

| Placeholder | What goes here |
|---|---|
| `{{first_name}}` | Contact's first name (GHL standard) |
| `{{calendar_invite_url}}` | URL to the .ics file or the GHL calendar booking link |
| `{{custom_values.btw_am_session_link}}` | The Zoom or platform URL for the live session |

In GHL these will look more like `{{contact.first_name}}`, `{{custom_values.qs_live_link}}`, etc. Adjust to match your tenant's syntax.

---

## Setup checklist in GHL

- [ ] Create a Workflow triggered by form submission on `JXFlOEgAhMoElAqLBG1L`
- [ ] Step 1: Send Email 1 (Confirmation) immediately
- [ ] Step 2: Wait 2 days, send Email 2 (Educational primer)
- [ ] Step 3: Wait until Saturday 16 May 9am UK, send Email 3 (Day-before)
- [ ] Step 4: Wait until Sunday 17 May 7am UK, send Email 4 (2-hour reminder)
- [ ] Step 5: Wait until Sunday 17 May 4pm UK, send Email 5 (1-hour reminder)
- [ ] Exit condition: contact buys recording, unsubscribes, or has tag `quantum-shift-attended-live`

## Post-event follow-ups (separate sequence, draft separately)

- T+12h after evening session: "Did you feel that?" with Alchemy Regulation Method Coach pitch
- T+2 days: Recording delivery email for everyone who could not attend, with $49.99 purchase link
- T+5 days: Final ARM Coach push for non-converters
