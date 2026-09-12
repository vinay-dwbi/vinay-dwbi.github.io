# vinay-dwbi.github.io

Personal site. Plain HTML and one stylesheet. No framework, no build step, no dependencies.
Edit a file, commit, done.

## Deploying

1. On GitHub, create a repository named exactly **`vinay-dwbi.github.io`** (must match your
   username or it will not publish at the root domain).
2. Upload the contents of this folder to the repository root. Not the folder itself, the
   contents. `index.html` must sit at the top level.
3. Settings → Pages → Source: **Deploy from a branch**, branch `main`, folder `/ (root)`.
4. Wait a minute or two. The site is live at `https://vinay-dwbi.github.io`.

`.nojekyll` is included so GitHub serves the files as-is instead of running them through Jekyll.
Do not delete it.

## Structure

```
index.html            About. The front page.
work/index.html       Enterprise initiatives, experience, and technical depth.
building/index.html   Enterprise & Ventures — hospitality, SaaS, and AI experiments.
404.html              Not-found page. GitHub Pages uses this automatically.
style.css             Everything visual. Design tokens at the top.
```

## Changing the look

Everything visual is in the `:root` block at the top of `style.css`. Changing `--blue`
changes every link and accent on the site. `--measure` controls column width; 640px keeps
lines under about 75 characters, which is where prose is comfortable to read.

Dark mode is automatic via `prefers-color-scheme` and has its own token block. No toggle,
because a toggle is a control nobody asked for.

## Custom domain, if you ever want one

Add a file named `CNAME` at the root containing just your domain, e.g. `vinayambalihalli.com`.
Then point a CNAME record at `vinay-dwbi.github.io` in your DNS. Settings → Pages will confirm.

## Before you publish

See `CONTENT-NOTES.md`. A few judgment calls in there are worth thirty seconds of your time.
