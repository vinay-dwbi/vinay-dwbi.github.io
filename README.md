# vinay-ambal.github.io

Personal site. Plain HTML and one stylesheet on GitHub Pages. No framework, no build step.
Edit a file, commit, push, done.

## Structure

```
index.html                        Home: the essay, then latest writing. Filled from Medium.
about/index.html                  About: resume-style. Prints cleanly.
building/index.html               Ventures. The URL stays /building/ so older links keep working.
work/index.html                   Redirects to /about/ (old link).
404.html                          Not-found page.
style.css                         Everything visual. Tokens at the top.
favicon.svg                       Orange "VA" mark.
scripts/sync-medium.mjs           (planned) Copies the Medium essay and posts into index.html.
.github/workflows/sync-medium.yml (planned) Runs the sync every 6 hours, or on demand.
```

Every page carries the same header and footer. If you change one, change all.

## Medium sync

**Status: not set up yet.** The script, its `package.json`, and the workflow are not in the repo.
Until they are, the essay in `index.html` is static: edit it by hand, and keep it in step with
the Medium version. The rest of this section describes the planned setup.

The essay is written and edited on Medium (@anp.vinay). The workflow reads the Medium feed
and rewrites two blocks in `index.html`:

- between `<!-- MEDIUM-ESSAY:START -->` and `<!-- MEDIUM-ESSAY:END -->`: the full essay
- between `<!-- MEDIUM-POSTS:START -->` and `<!-- MEDIUM-POSTS:END -->`: the six newest other posts

Never hand-edit anything between those markers; the next sync overwrites it.

Setup, once: publish the essay on Medium, then add repository variables `MEDIUM_USER`
(`anp.vinay`) and `ESSAY_ID`
(Settings > Secrets and variables > Actions > Variables) set to the 12-character code at the end
of the essay's URL. Then run the workflow from the Actions tab.

To push an edit live right away: Actions > Sync Medium > Run workflow.

Limits: Medium's feed holds only the 10 newest posts. If the essay falls out of the feed, the
site keeps the last copy it synced. Keep the essay free to read (not member-only), or the feed may
carry only a preview.

## Changing the look

Everything visual is in the `:root` block at the top of `style.css`: `--orange` is the header and
footer, `--beige` is the page. Dark mode is automatic via `prefers-color-scheme`.

## Before you publish

See `CONTENT-NOTES.md`.
