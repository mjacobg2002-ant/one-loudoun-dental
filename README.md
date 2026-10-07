# Dental Practice Website Template

A single-file, mobile-first, conversion-focused website template for **dental practices** (general, cosmetic, family). Warm, modern, patient-friendly aesthetic — teal + navy + champagne, Cormorant Garamond serif + Manrope sans, rounded cards and soft shadows. Clone it, change the accent color and logo, find-and-replace the details, ship.

Design synthesized from two real dental sites — **Waterman Family Dentistry** (warmth, rounded cards, stats band, first-visit steps, insurance band, live "accepting patients" status, gradient headline) and **Westpark Dental Studio** (clean service grid, doctor + experience sections) — into one reusable, rebrandable base with its own identity.

---

## Why it converts

- **Book everywhere** — every "Book Appointment" button points at your scheduler (Zocdoc / NexHealth / etc.), plus a **sticky mobile call/book bar** on phones and a phone number in the top utility bar.
- **Instant credibility** — hero rating row, a teal **stats band**, a doctor credibility line, and a 5.0-star reviews section with real patient quotes.
- **Lowers first-visit anxiety** — a "your first visit, made simple" 4-step section and an insurance/financing band.
- **Local SEO ready** — semantic HTML, meta/Open Graph, Dentist structured data, Google Maps embed, and NAP (name/address/phone) in the footer.
- **Warm + modern** — rounded cards, soft shadows, lift-on-hover; missing photos fall back to a soft brand-tinted panel so it always looks finished.
- **Fast & self-contained** — one HTML file, no build step. Just Google Fonts.

---

## Setup (5 minutes)

### 1. Copy the folder & find-and-replace tokens

| Token | Example |
|---|---|
| `{{PRACTICE_NAME}}` | Riverstone Dental |
| `{{TAGLINE}}` | General & Cosmetic Dentistry |
| `{{DOCTOR_NAME}}` | Dr. Jane Smith, DDS |
| `{{DOCTOR_CRED}}` | General & Cosmetic Dentist |
| `{{DOCTOR_BLURB}}` | West Point graduate & Army veteran (any credibility line) |
| `{{SINCE}}` | 2009 |
| `{{PHONE}}` | (703) 555-0100 |
| `{{PHONE_TEL}}` | +17035550100 (digits only) |
| `{{CITY}}` | McLean |
| `{{REGION}}` | Northern Virginia |
| `{{STATE}}` | VA |
| `{{STREET}}` | 123 Main Street, Suite 200 |
| `{{ZIP}}` | 22102 |
| `{{DOMAIN}}` | riverstonedental.com |
| `{{BOOK_URL}}` | booking link (Zocdoc/NexHealth) — or `#book` |
| `{{REVIEW_URL}}` | Google reviews link — or `#` |
| `{{MAP_QUERY}}` | url-encoded address, e.g. `123%20Main%20St%2C%20McLean%2C%20VA` |

### 2. Change the accent color
In `index.html`, find `★ BRAND ACCENT` in `:root` and edit two lines:
```css
--brand:#0f766e;        /* deep shade — buttons, text */
--brand-bright:#21b6a8; /* vivid shade — gradients, accents */
```
Presets below it: **teal** (default), **navy**, **plum**, **forest**, **slate-blue** — uncomment one.

### 3. Add the logo
Drop `assets/img/logo-white.png` (shown on the dark header/footer) — transparent PNG. No logo yet? The practice name shows as styled serif text automatically.

### 4. Add photos
Drop into `assets/img` (any missing photo auto-hides and shows a soft brand panel):
```
hero.jpg  welcome.jpg  doctor.jpg  office-1.jpg  office-2.jpg  office-3.jpg
```
Optional: add `hero.mp4` and uncomment the `<video>` tag in the HERO section for a background video (like Waterman's).

### 5. Edit the copy
Search `index.html` for `EDIT:` — that marks the headline, stats, services (6 cards), first-visit steps, doctor bio, reviews, insurance list, and hours.

### 6. Booking
Every booking button uses `{{BOOK_URL}}`. Point it at your online scheduler. No scheduler? Set it to `#book` and lean on the phone CTAs.

---

## Deploy

One HTML file + an `assets/img/` folder — any static host works.
- **GitHub Pages:** push, then Settings → Pages → deploy from `main` / root.
- **Vercel / Netlify:** drag-and-drop or connect the repo.

---

## Sections included

Top utility bar (status + hours + phone) · sticky header · hero (rating + credibility) · stats band · welcome · services grid (6) · first-visit steps · doctor bio · experience (dark) · office gallery · testimonials · insurance/financing band · appointment CTA · location + Google Map · footer (NAP) · sticky mobile book bar.

Delete any section you don't want — each is a clearly commented `<section>`.

> **Compliance note:** never publish fake reviews, credentials, or claims. Use only real patient reviews and verified doctor credentials.
