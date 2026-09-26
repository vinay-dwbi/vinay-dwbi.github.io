# Content notes

The rules the copy follows. The full brief and the fact source live outside this repo. If a fact
is not in the fact source, it does not go on the site; leave `<!-- TODO: confirm -->` instead.

## What each page does

**Home** leads with ideas, not a biography: the essay "The Age of Enough," then recent writing,
then one short line about the author. The name appears in the header and footer, not the headline.

**About** reads like a resume: no adjectives about the person, no "I am" statements. Experience,
skills, and education, and the work speaks for itself.

**Ventures** describes the kind of work, never the business.

## Deliberately left off

- **Detail on earlier roles.** The About page gives eHealth, Kaiser Permanente, and Belk in full.
  Trane, TIAA, and Cognizant appear as one "Earlier" line with titles and dates, so the page
  matches the resume and LinkedIn without the detail.
- **Internal metrics from the current employer.** No pipeline counts, cost figures, or
  performance percentages from eHealth. Numbers from past employers (Kaiser, Belk) are fine.
- **Venture names, URLs, screenshots, revenue, or traction.** Work in development says so.
- **Phone number and street address.** Email, LinkedIn, GitHub, and Medium only. The resume PDF
  is not linked because it carries the phone number.
- **Job-search signals.** Nothing that reads as "open to opportunities."
- **Chess ratings.** "Chess and puzzles," nothing more.

## Tone

Humble and neutral. Short declarative sentences, no superlatives, no "passionate about."
Let experience and ideas carry the weight. No em dashes; use a colon, comma, period, or
parentheses.

## Before every push

Run the never-publish grep from the private brief over `*.html` and `*.md`, check every link, and
look at each page at desktop and phone width in light and dark mode.
