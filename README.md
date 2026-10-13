# Shervin's Food Lab 🍽️

**Food & gastro marketing portfolio site · Berlin · English / Deutsch**

🔗 **Live site:** [shervinkhm1-hue.github.io/foodlab](https://shervinkhm1-hue.github.io/foodlab/?utm_source=github&utm_medium=referral&utm_campaign=readme)

Shervin's Food Lab is where I combine my backgrounds: a degree in **Food Science**, years of **hospitality** work, and my current B.A. studies in **Business Administration (Digital Marketing)** at BSBI Berlin. I share marketing ideas for cafés, restaurants and food brands, from Berlin döner shops to fine dining.

---

## What the site covers

- **Social media for gastro:** content ideas and posting strategies for restaurants and cafés
- **Food content that sells:** how to present food so people want to order it
- **Local visibility:** helping food businesses get found in their neighbourhood

---

## Marketing & analytics setup

I built the tracking myself, using Google Analytics 4 and the same tools I'd use for a client.

| Area | What I did |
|---|---|
| **GA4** | Website tracking, loaded **only after cookie consent** (GDPR / DSGVO compliant) |
| **Custom events** | `social_click`, `contact_click` and `certificate_click`, each with `platform` and `location` parameters, so I can see *which* button on *which* section gets clicked |
| **Campaign tracking** | UTM-tagged links per channel and placement (e.g. LinkedIn Featured vs. Contact info vs. posts) |
| **Social previews** | Open Graph tags and a custom 1200×627 preview image for LinkedIn, Instagram and WhatsApp |
| **Debugging** | Tested with Google Tag Assistant and GA4 DebugView (`?debug=1`) |
| **Legal** | Impressum and Datenschutzerklärung pages |

---

## Case study: auditing my own GA4 data

After the first weeks, GA4 reported **19 users**. Before trusting that number, I investigated it.

**What I found**
- About **8 users were bots**, coming from data-center cities such as Ashburn, Santa Clara, Moses Lake, and Meta's data centers in Prineville, Forest City and Luleå.
- All 3 "Instagram users" were most likely **Meta's link-preview crawler**, not real people.
- Several sessions were **my own testing** (Tag Assistant, GitHub referrals, my own Wi-Fi).
- **LinkedIn traffic was invisible**, because the in-app browser strips the referrer and nobody had clicked the profile link yet.
- Real audience: **around 5–7 genuine visitors**, all arriving as "Direct".

**What I fixed**
1. Activated an **internal traffic filter** (IP-based) to exclude my own visits
2. Activated a **developer traffic filter** to remove debug and Tag Assistant hits
3. Added `tagassistant.google.com` and `github.com` to the **unwanted referrals** list
4. Added **UTM tags** to every LinkedIn link, with a different campaign name per placement
5. Added **Open Graph tags** so shared links show a proper preview card

**Takeaway:** raw analytics numbers can be misleading. Checking *where* traffic really comes from, and cleaning it, matters more than the headline figure.

---

## Tech

Plain HTML, CSS and JavaScript, with no framework. Hosted for free on **GitHub Pages**. Bilingual EN/DE with a language switch (tracked as a `language_switch` event).

---

## About me

**Shervin Khamseh:** Digital Marketing student at BSBI Berlin, looking for a **Werkstudent role in digital or content marketing** in Berlin.

- Certifications: HubSpot Social Media Marketing (2026) · Google Analytics Certification (2026)
- Languages: Persian (native) · English (C1) · German (B2)
- LinkedIn: [linkedin.com/in/shervin-khamseh-3ab2a341b](https://www.linkedin.com/in/shervin-khamseh-3ab2a341b/)
