# vinay-ambal.github.io

Personal site. Plain HTML and one stylesheet on GitHub Pages. No framework, no build step.
Edit a file, commit, push, done.

## Structure

```
index.html            Home ("Blog post"): the latest Medium post, then What I believe.
about/index.html      About me: resume-style. Prints cleanly.
building/index.html   Ventures. The URL stays /building/ so older links keep working.
work/index.html       Redirects to /about/ (old link).
404.html              Not-found page.
style.css             Everything visual. Tokens at the top.
favicon.svg           Yin-yang mark, same as the header.
```

Every page carries the same header and footer. If you change one, change all.

## Latest post from Medium

The home page ships with a static copy of the latest post (title, date, first two paragraphs,
link). A small script at the bottom of `index.html` refreshes it in the visitor's browser from
the Medium feed (@anp.vinay) and lists up to five older posts. Medium's feed does not allow
browser requests, so the script goes through the free rss2json service. It uses only text,
never Medium's HTML, and if the request fails the static copy stays.

When you publish a new post, update the static copy too, so visitors without JavaScript and
search engines see it.

## Changing the look

Everything visual is in the `:root` block at the top of `style.css`: `--orange` is the header and
footer, `--beige` is the page. Dark mode is automatic via `prefers-color-scheme`.

## Before you publish

See `CONTENT-NOTES.md`.
