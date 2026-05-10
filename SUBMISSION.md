# Assignment Submission — Build and Deploy a Professional Portfolio with Claude

## 1. Live URL

**https://shawnpal2002.github.io/my-portfolio/**

Repository: https://github.com/shawnpal2002/my-portfolio

The site is a single `index.html` file (HTML + inline CSS + inline JavaScript) deployed via GitHub Pages from the `main` branch (root).

---

## 2. Prompt History

Three prompts were used with Claude. The first generated the base structure; the next two refined the design (per the assignment's iteration requirement).

### Prompt 1 — Initial generation

> Build me a responsive, single-page personal portfolio website for **Shawn Pal**, a Computer Science student and aspiring software developer. Output everything in **one `index.html` file** with the CSS and JavaScript inlined.
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

### Prompt 2 — Add hover lift on project cards

> Add a hover effect to my project cards so they **lift up** when I move my mouse over them. The lift should be smooth (around 250–300 ms), include a soft shadow underneath the card, and the card border should change to the accent colour on hover. Make sure it doesn't make the layout jump on touch devices.

### Prompt 3 — Premium light redesign

> I don't like the current colour scheme. Redesign the site for a **premium light theme** — no purple, no dark mode. Use a warm ivory background (around `#f6f3ec`), white card surfaces, and a single sophisticated accent (a deep sienna, around `#8a3a1f`) used sparingly for italics and hover states.
>
> For typography, switch to an **editorial serif/sans pairing**: use **Fraunces** for all headings (with italic variants for emphasis) and **Inter** for body text. Both via Google Fonts.
>
> Restructure the sections so each one has a small numbered label (`01 — About`, `02 — Skills`, etc.) on the left and the section title on the right. Replace the boxy stats block with a thin border-divided strip. Make the skills list a 3-column underlined list with skill levels (e.g. *advanced*, *comfortable*) shown in italic. Use generous whitespace throughout — think editorial magazine, not tech dashboard.

---

## 3. Self-Correction

**What I asked Claude to fix:** the entire visual direction — specifically the colour scheme and typography of the first version.

**The issue:** Claude's first version defaulted to a dark theme with a violet/teal accent palette and a system sans-serif font stack. While technically correct and visually clean, the result felt generic — closer to a developer-tool landing page than a personal portfolio. The violet accent in particular was overused for headings, buttons, and highlights, which made the page feel busy rather than considered.

**The fix:** I asked Claude to redesign with a **premium light theme**: warm ivory background, a single restrained sienna accent used only for italic emphasis and hover states, and an editorial typographic pairing of Fraunces (serif, with italics for the accent words) and Inter (sans for body). I also restructured each section to use a numbered label + title layout so the page reads more like a printed editorial spread.

**Why this matters:** the original brief asked for a *professional* portfolio. Professional doesn't automatically mean dark mode with neon accents — that aesthetic has become associated with dev tools and SaaS landing pages, not with personal portfolios that need to convey craft and care. Switching to a light editorial aesthetic with disciplined typography and a single accent colour produced something that feels considered and individual, not templated. It also taught me a useful prompting lesson: it's much more effective to give Claude a specific aesthetic reference (palette values, named fonts, layout structure) than to ask vaguely for "premium" or "professional" — those words mean very different things to different designers.

---

## 4. File Structure

```
my-portfolio/
├── index.html      # complete portfolio (HTML + CSS + JS in one file)
└── SUBMISSION.md   # this file
```
