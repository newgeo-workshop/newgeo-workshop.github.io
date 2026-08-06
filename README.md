# newgeows.github.io

Website for **NewGeo 2026 — New Directions in IP Geolocation Workshop**, co-located with
[ACM IMC 2026](https://conferences.sigcomm.org/imc/2026/) in Karlsruhe, Germany, on
Monday, October 12, 2026.

Published at <https://newgeows.github.io/>.

## How it works

The page content is **Markdown**. GitHub Pages runs Jekyll automatically, converts
`index.md` to HTML using `_layouts/default.html`, and publishes it. Push to `main` and the
change is usually live within a minute — there is nothing to build or commit by hand.

| File | Purpose |
| --- | --- |
| `index.md` | **All page content, as Markdown.** This is the file you normally edit. |
| `_config.yml` | Title, subtitle, and the event details shown in the page header |
| `_layouts/default.html` | Page shell: `<head>`, header, navigation, footer |
| `style.css` | Styling on top of Bootstrap 5.3 (loaded from a CDN) |
| `favicon.svg` | Browser tab icon |

There is no JavaScript on the site.

> Do not add a `.nojekyll` file — it disables Jekyll, and the Markdown would be served as
> raw source instead of a rendered page.

## Editing content

Almost everything lives in `index.md` as ordinary Markdown. Three conventions to know:

- **Heading anchors.** The `{#id}` after each `##` heading is what the nav links point at,
  e.g. `## Call for Papers {#cfp}`. Rename the heading text freely, but keep the `{#id}` or
  the corresponding nav link in `_layouts/default.html` will break.
- **Notices.** A blockquote (`> ...`) renders as a small grey italic note.
- **Editor notes.** `{% comment %} ... {% endcomment %}` blocks are stripped at build time
  and never appear in the published page.

Common updates:

- **Change any date** — all four live in `_config.yml` (`submission_date`,
  `notification_date`, `camera_ready_date`, `workshop_date`). The Important Dates table in
  `index.md` reads them, so edit them there and not in the table.
- **Add a news item** — add a bullet at the top of the News list.
- **Add the HotCRP link** — replace the placeholder paragraph under *Submission Site*.
- **Announce the program committee** — replace `TBD — to be announced.` with a Markdown
  table. Please list name and affiliation only; do not publish PC members' email addresses.
  `workshop_date` in particular also feeds the page header and the Venue section, so all
  three places update at once.

  Note: Jekyll does not pick up `_config.yml` changes while `jekyll serve` is running —
  restart it to see them.
- **Publish the program** — the Program section currently says `TBD`. Replace that line with
  a Markdown table; a commented-out skeleton sits just above it in `index.md`. Keep the
  `{: .program}` line directly beneath the table — that is what stops the time ranges from
  wrapping mid-range.

## Local preview

Local preview needs Ruby and Jekyll, which is why it is easiest to just push and check the
live site. If you do want to build locally:

```sh
gem install bundler jekyll
jekyll serve
```

Or, without installing Ruby, using a container:

```sh
podman run --rm -it -v "$PWD":/srv/jekyll:Z -p 4000:4000 \
  docker.io/jekyll/jekyll:4 jekyll serve --host 0.0.0.0
```

Then open <http://localhost:4000/>.
