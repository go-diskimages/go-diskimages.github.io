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

## The design is not here

It comes from the shared Hugo module
[`go-fleettools/landingkit`](https://github.com/go-fleettools/landingkit),
pinned in `go.mod` (Renovate bumps it); `kit.go` keeps `go mod tidy` from
deleting that requirement. `[params.brand]` in `hugo.toml` is read from the logo by
`landingkit brand`. A file under `layouts/partials/` with the name of one of the
kit's would silently override it.
