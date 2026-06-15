# go-diskimages.github.io

Source for the [go-diskimages](https://github.com/go-diskimages) organization
landing page, served at <https://go-diskimages.github.io/>.

A single-page [Hugo](https://gohugo.io) site: one inline-CSS `layouts/index.html`
template fed by the repo cards in `hugo.toml`, with a light/dark theme that follows
`prefers-color-scheme`. It matches the shared family grammar used across the
sibling Go organizations (centered hero logo, tagline, pills, Documentation +
GitHub CTAs, and an honest "Repositories" grid).

## Build locally

```sh
GOWORK=off hugo --minify     # output in ./public
hugo server                  # live preview at http://localhost:1313
```

## Deploy

Pushes to `main` are built and published to GitHub Pages by
`.github/workflows/hugo.yml` (the official Hugo Pages workflow). Pages must be set
to "GitHub Actions" as its build source.

BSD-3-Clause.
