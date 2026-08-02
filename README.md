# NEON POP

Official site for the mobile game **NEON POP** (`com.neonpop.game`) — landing page plus
the legal pages linked from inside the game and from the Google Play listing.

**Live:** https://wish-go.github.io/neonpop-legal/

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

## ⚠️ Do not rename this repository

The URL above is already registered in Play Console under **App content → Privacy policy**,
and that field is effectively frozen once the listing is filed. The repo name is therefore
part of a published contract, not a cosmetic choice.

GitHub Pages does **not** redirect after a rename — the old URL returns 404 immediately and
the in-game links break silently: the player taps Privacy Policy in Settings and lands on a
404, which is exactly what Google checks during review.

This already happened once (`neonpop-legal` → `Neonpop`, Aug 2026) and had to be undone by
renaming back, because the Play Console entry could not be edited.

If a rename ever becomes unavoidable, **confirm the Play Console field can be changed first**,
then update, in this order:

1. Play Console → App content → Privacy policy
2. Play Console → Store listing → Website
3. `Assets/Scripts/GamePlay/Common/PloxLinks.cs` → `LEGAL_BASE`, in the game repo
4. The **Live** link at the top of this file

Finally open `<new-url>/privacy.html` and confirm 200 — not just the landing page. The
landing page and the legal pages are separate checks.

## Contact

Support: <aslm2l1k123@gmail.com>
