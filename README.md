# Write

**Write** is a lightweight, distraction-free text editor in the browser — Markdown + LaTeX, instant preview, and one-click PDF export. No login, no server, no tracking.

**Live at [write.chinmay.fyi](https://write.chinmay.fyi/)**

<img src="http://i.imgur.com/c56hDwi.gif" />

## Features

* **Instant preview** — no delay between typing and rendering, no flicker on math equations
* **LaTeX / MathJax** — inline (`$x^2+1$`) and display (`$$...$$`) formulas
* **PDF export** — click the **PDF** button (bottom-right) or press `CTRL + P`; the exported filename is taken from your first `# heading`, and `\pagebreak` forces a page break in the output
* **Dark mode**, LaTeX-style Computer Modern or sans-serif font
* **Autosave** — your text is stored in your browser's local storage
* **Open / save `.md` files** — or just drag & drop one onto the page
* **Zero backend** — pure static files; runs offline if you open `index.html` directly

## Keyboard shortcuts

| Shortcut | Action |
|---|---|
| `CTRL + P` | Export as PDF / print (or click the **PDF** button) |
| `CTRL + D` | Toggle display mode (editor only / preview only / split) |
| `CTRL + S` | Save source as `.md` file |
| `CTRL + SHIFT + O` | Open a `.md` file |
| `CTRL + SHIFT + D` | Toggle dark mode |
| `CTRL + SHIFT + L` | Enable / disable LaTeX (math) |
| `CTRL + SHIFT + R` | Toggle Computer Modern / sans-serif font |
| `CTRL + SHIFT + H` | Help dialog |
| `F11` | Full screen |

## Run locally

Open `index.html` in a browser. That's it — there is no build step and no server code.

## Deploy

Hosted on Cloudflare Workers (static assets) at `write.chinmay.fyi`. The worker name and custom domain are declared in `wrangler.toml`:

```
npx wrangler deploy
```

## Credits & license

MIT license.

Based on [**Writing**](https://github.com/josephernest/writing) by Joseph Ernest (MIT), which uses [Pagedown](https://code.google.com/archive/p/pagedown/), [Pagedown Extra](https://github.com/jmcmanus/pagedown-extra), [MathJax](https://www.mathjax.org/), StackOverflow's [editor code](https://gist.github.com/gdalgas/a652bce3a173ddc59f66), and the [Computer Modern](http://cm-unicode.sourceforge.net/) font. Some of these libraries were slightly modified upstream to work together, which is why they are included in this package.

This fork adds the PDF export button, a Cloudflare deployment setup, and removes upstream analytics.
