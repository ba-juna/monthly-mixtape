# Monthly Mixtape

Static site on GitHub Pages. No build step: edit these files and push to `main`.

- `index.html`: layout, styles, all page code
- `data/tapes.json`: months and tracks, `[{id:"YYYY-MM", y, m, t:[[title, artist, genre, seconds], ...]}]`, oldest first
- `data/notes.json`: writing and links. `m["YYYY-MM"] = {text, at, am, yt}`; `at` is when the writing was first posted
- `data/photos.json`: `{"YYYY-MM": {src, date}}`; `date` is the capture date shown as the orange stamp
- `photos/YYYY-MM.jpg`: month covers, long edge about 1200px

## Rules

- The home feature, the ticker and the On air chip follow the post with the newest `at`, not the calendar.
- A month with no photo shows the film-grain black box with Coming soon.
- The month page shows the YouTube player only after the black bar is pressed, and only for months with a `yt` link.
- The avatar circle stays still; the character bobs on page load, on hover and while the YouTube player is open.
- The back-to-top button appears only at phone width after scrolling.
- Footer totals (tapes, tracks, artists) are computed from `tapes.json`.

## Visit counts

GoatCounter: https://monthly-mixtape.goatcounter.com. Month pages count as `/YYYY-MM`; YouTube and Apple Music clicks count as events. Browsers holding the edit key are not counted.

## Editing on the page

Open the site with `#owner` once per device and paste the edit key. The key is a GitHub fine-grained token limited to this repository (Contents: read and write). It stays in that browser only and must never be committed. Saves commit to `main` and go live in 1 to 2 minutes.

## Monthly routine

1. Export the finished month from the Music app and update `data/tapes.json`.
2. Write the post and set the photo on the page in edit mode.
3. Add the Apple Music and YouTube links to that month.
4. Export the Instagram slides from the month page and post.

Before pushing changes made elsewhere, run `git pull`: the owner may have saved from the page.
