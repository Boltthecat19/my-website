# BOLTT — Sovereign Cloud (CIS155 Web Development)

A static landing site for **BOLTT**, a concept for a locally deployed sovereign cloud
you run on hardware you own, administered in plain English by an AI assistant named **Ebi**.

Built for CIS155 Web Development at Olympic College. Plain HTML5 + CSS, no JavaScript,
no frameworks, no build tools.

## Pages

| Page | File | Purpose |
| --- | --- | --- |
| Home | `index.html` | Hook, the problem, the BOLTT solution, and Ebi |
| How It Works | `how-it-works.html` | Three-step flow plus a deeper technical explanation and a comparison table |
| About | `about.html` | Mission, beliefs, and long-term vision |
| Request Access | `contact.html` | Early-access contact form |

---

## Peer Feedback / Self-Assessment

I did not receive peer feedback for the previous discussion board assignment, so per the
assignment instructions I performed my own assessment of the site against what we covered
in Chapter 16 (web typography, icons, and final polish). The two most significant issues
I identified, written as if they were peer suggestions:

> **Suggestion 1:** "The site uses the browser's default sans-serif font everywhere and has
> no icons, so it reads as unfinished and generic. For a security/infrastructure brand it
> should have a distinct typeface and visual cues."

> **Suggestion 2:** "Everything is written as paragraphs. There's no quick way to compare
> BOLTT against a traditional cloud at a glance, and the site is only three pages with no
> way for a visitor to actually reach out."

---

## Improvements Made

Based on the assessment above, I made the following specific changes:

### Typography — Google Font (required)
- Added the **Space Grotesk** typeface (a geometric, technical-feeling font that suits the
  brand) via Google Fonts, loaded in the `<head>` of every page with `preconnect` hints for
  faster loading.
- Set it as the site-wide `font-family` in `style.css`, falling back to `sans-serif`.
- **Privacy note:** because Google Fonts is a Google service, the font URL can be switched
  from `fonts.googleapis.com` to `fonts.bunny.net` (Bunny Fonts), a drop-in,
  privacy-respecting proxy with an identical API, with no other changes.

### Icons — FontAwesome (required)
- Loaded the free **FontAwesome 6** icon library via CDN in the `<head>` of every page.
- Added relevant icons throughout the site (for example a shield, a lock, and a server) to
  reinforce the security and infrastructure theme. These are real icon-font glyphs, not emoji.

### Comparison table (extra credit)
- Added a **BOLTT vs. Traditional Cloud** table to the How It Works page, comparing who owns
  the data, where it physically lives, who has access, and how compliance is handled.

### Fourth page + contact form
- Added `contact.html`, a "Request Early Access" page with a real HTML form
  (`<form>`, `<label>`, `<input>`, `<textarea>`, `<button>`), bringing the site to four
  content pages, each filling at least a full viewport height.

### Favicon (extra credit)
- Added the BOLTT logo (`images/boltt-logo-dark2.svg`) as an SVG favicon so the brand mark
  shows in the browser tab. SVG keeps it crisp at any size.

### Polish
- Made the nav logo link back to the home page (standard convention).
- Added a styled call-to-action button in the hero instead of a plain text link.
- Proofread and corrected spelling and punctuation across the pages.

---

## Running Locally

Open `index.html` directly in a browser, or serve the folder:

```bash
python3 -m http.server
```

Then visit `http://localhost:8000`.
