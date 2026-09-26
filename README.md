# vinay-ambal.github.io

Personal site. Plain HTML and one stylesheet. No framework, no build step, no dependencies.
Edit a file, commit, push, done.

## Deploying

GitHub Pages serves the `main` branch from the repository root
(Settings → Pages → Source: **Deploy from a branch**, branch `main`, folder `/ (root)`).
A push to `main` is live at `https://vinay-ambal.github.io` within a minute or two.

The empty `.nojekyll` file tells GitHub to serve the files as they are instead of running
them through Jekyll. Do not delete it.

## Structure

```
index.html            About. The front page.
work/index.html       Selected work, experience, technical depth, education.
building/index.html   Ventures. The URL stays /building/ so older links keep working.
404.html              Not-found page. GitHub Pages uses this automatically.
style.css             Everything visual. Design tokens at the top.
```

Every page carries the same header, nav, and footer. If you change one, change all four.

## Changing the look

Everything visual is in the `:root` block at the top of `style.css`. Changing `--blue`
changes every link and accent on the site. `--measure` controls column width; 640px keeps
lines under about 75 characters, which is where prose is comfortable to read.

Dark mode is automatic via `prefers-color-scheme` and has its own token block. No toggle,
because a toggle is a control nobody asked for.

## Custom domain, if you ever want one

Add a file named `CNAME` at the root containing just your domain, e.g. `vinayambalihalli.com`.
Then point a CNAME record at `vinay-ambal.github.io` in your DNS. Settings → Pages will confirm.

## Before you publish

See `CONTENT-NOTES.md` for the content rules and the check to run before every push.
