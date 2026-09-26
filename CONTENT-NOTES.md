# Content notes

The rules the copy follows, and the calls that were made deliberately.
The full brief and the fact source live outside this repo. If a fact is not in the fact
source, it does not go on the site; leave `<!-- TODO: confirm -->` in the HTML instead.

## Positioning

Data platform architect: data engineering, lakehouse, streaming, and ML. The site tells the
same story as the résumé, with the same titles and dates. Product sense and building things
of my own are supporting evidence and live on the Ventures page.

## Deliberately left off

**Internal metrics from the current employer.** No pipeline counts, subject-area counts, cost
figures, or performance percentages. Those belong on the résumé and in conversation. Scope is
described qualitatively. Kaiser's membership is public information and may stay. Numbers from
past employers (Kaiser, Belk) are fine.

**Anything I cannot talk about for two minutes.** Every technology on the Work page is one I
have used. Unconfirmed skills stay out of the visible text, with a TODO comment, until confirmed.

**Anything that reads as a reason for leaving or a job search.** The contact section says how
to reach me, nothing more.

**Names, links, dates, and numbers for ventures.** The Ventures page describes the kind of work,
never the business: no names, URLs, screenshots, revenue, traction, or launch claims. Work that
is in development says so.

**Chess ratings.** The site says I play chess. No rating, no profile link.

**Titles other than the titles of record.** The Work page uses the titles and dates of record,
exactly. Management scope at eHealth is stated as scope in the role description, never as a title.

## Judgment calls

**1. The management sentence on Work.** Five direct reports from April 2024 to January 2026 is
stated as scope. The reorganization that followed is not mentioned.

**2. Cognizant clients.** Named, because they are twenty years old and public engagements.

**3. The food business.** Past tense, unnamed, no dates. Framed as what it taught.

**4. The URL `/building/`.** The nav says Ventures; the folder name stays so older links work.

## Tone

Written to sound like me thinking out loud, not like a brochure. Short declarative sentences,
first person, no superlatives, no "passionate about." The one rhetorical move used repeatedly is
stating the constraint before the solution, which is how I actually talk about this work.
Prose over bullet lists on the home page. No em dashes; use a colon, comma, period, or
parentheses.

If a line does not sound like something I would say to a colleague, change it.

## Before every push

Run the never-publish grep from the private brief over `*.html` and `*.md`, check every link,
and look at each page at desktop and phone width in light and dark mode.
