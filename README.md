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
work/index.html       Experience and technical depth.
building/index.html   Homemade, RE Analyzer, and the thesis behind them.
writing/index.html    Blog index. Currently an empty state with the queued topics.
writing/_template/    Copy this to start a post.
404.html              Not-found page. GitHub Pages uses this automatically.
style.css             Everything visual. Design tokens at the top.
```

## Adding a post

```
cp -r writing/_template writing/your-post-slug
```

Edit `writing/your-post-slug/index.html`, then add a row to the list in `writing/index.html`:

```html
<div class="row">
  <div class="when">Oct 2026</div>
  <div class="body">
    <h3><a href="/writing/your-post-slug/">Post title</a></h3>
    <p>One sentence on what it argues.</p>
  </div>
</div>
```

Delete the `<div class="empty">` block once you have two or three posts up.

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

See `CONTENT-NOTES.md`. Two judgment calls in there are worth thirty seconds of your time.
