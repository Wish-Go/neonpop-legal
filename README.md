# NEON POP

Official site for the mobile game **NEON POP** (`com.neonpop.game`) — landing page plus
the legal pages linked from inside the game and from the Google Play listing.

**Live:** https://wish-go.github.io/Neonpop/

| Page | Where it is used |
| --- | --- |
| [`index.html`](index.html) | Landing page. Goes in the Play listing's **Website** field. |
| [`privacy.html`](privacy.html) | Privacy Policy. Play Console → App content → **Privacy policy**, and the in-game Settings page. |
| [`terms.html`](terms.html) | Terms of Service. Opened from the in-game Settings page. |

## Editing

Edit the files **here** — this repo is what actually ships. Pushing to `main` redeploys
GitHub Pages within a minute or two.

The game repo keeps a mirror under `Docs/Legal/` so the pages travel with the source,
but that is a copy: after changing anything here, copy the three files over and commit
them there too.

## ⚠️ If you rename this repository

GitHub Pages does **not** redirect the old URL — it starts returning 404 immediately, and
the in-game links break silently: the player taps Privacy Policy in Settings and lands on
a 404. That is exactly what Google checks during review.

A rename means updating all of these:

1. `Assets/Scripts/GamePlay/Common/PloxLinks.cs` → `LEGAL_BASE`, in the game repo
2. Play Console → App content → Privacy policy
3. Play Console → Store listing → Website
4. The **Live** link at the top of this file

Then open `<new-url>/privacy.html` and confirm it returns 200 — not just the landing page.
The landing page and the legal pages are separate checks, and this repo has already been
renamed once (`neonpop-legal` → `Neonpop`) with the in-game links left pointing at the
dead address.

## Contact

Support: <aslm2l1k123@gmail.com>
