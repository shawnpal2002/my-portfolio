# Assignment Submission — Build and Deploy a Professional Portfolio with Claude

## 1. Live URL

**https://shawnpal2002.github.io/my-portfolio/**

Repository: https://github.com/shawnpal2002/my-portfolio

The site is a single `index.html` file (HTML + inline CSS + inline JavaScript) deployed via GitHub Pages from the `main` branch (root).

---

## 2. Prompt History

Three prompts were used with Claude. The first generated the base structure; the next two refined the design (per the assignment's iteration requirement).

### Prompt 1 — Initial generation

> Build me a responsive, single-page personal portfolio website for **Shawn Pal**, a Computer Science student and aspiring full-stack developer. Output everything in **one `index.html` file** with the CSS and JavaScript inlined.
>
> Required sections:
> - A sticky top navigation
> - A hero header with my name and a short tagline
> - An "About Me" section with a 2–3 paragraph bio and a small stats block
> - A "Skills" section listing my main tools and technologies
> - A "Projects" gallery with 3 project cards (title, description, tech tags, links)
> - A "Contact" section with an email link and a GitHub link (`shawnpal2002`)
> - A footer with the current year auto-filled by JavaScript
>
> Keep the layout responsive on mobile, use semantic HTML, and favour clean modern typography.

### Prompt 2 — Dark mode iteration

> Change the colour scheme to a professional **Dark Mode** with accent colours. Use a deep near-black background (around `#0d1117`), slightly lighter card surfaces, and two accent colours: a violet (`#7c5cff`) and a teal (`#29d4c4`). Apply a subtle gradient glow behind the hero. The accent colours should be used for headings, the call-to-action button, and small highlights — not overused.

### Prompt 3 — Hover lift on project cards

> Add a hover effect to my project cards so they **lift up** when I move my mouse over them. The lift should be smooth (around 250ms), include a soft shadow underneath, and the card border should change to the violet accent on hover. Make sure it doesn't make the layout jump on touch devices.

---

## 3. Self-Correction

**What I asked Claude to fix:** the smooth-scroll behaviour for the in-page navigation links.

**The issue:** the first version relied solely on the CSS `scroll-behavior: smooth` rule. While this works in modern browsers, it doesn't always feel consistent — and clicking a `#section` link still updates the URL hash, which can cause a sudden jump on some browsers before the smooth scroll kicks in. It also did nothing to gracefully handle a bare `#` href (which would scroll to the top abruptly).

**The fix:** I asked Claude to add a small JavaScript handler that intercepts clicks on any `a[href^="#"]`, calls `preventDefault()`, and triggers `scrollIntoView({ behavior: 'smooth', block: 'start' })` on the target element. The handler also short-circuits when the href is just `#`, so it can't accidentally jump.

**Why this matters:** it makes the in-page navigation feel intentional and identical across browsers, and prevents a subtle UX bug where clicking a nav link would briefly flash to the top of the page before scrolling. Small thing, but it's the kind of polish that separates a hobby site from a professional one.

---

## 4. File Structure

```
my-portfolio/
├── index.html      # complete portfolio (HTML + CSS + JS in one file)
└── SUBMISSION.md   # this file
```
