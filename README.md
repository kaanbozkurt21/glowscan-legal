# glowscan-legal

The privacy policy and terms for the GlowScan iOS app. Static, self-contained,
English then Turkish on each page — KVKK requires a Turkish notice and an English
policy does not discharge it.

Both are written from the engineering account of what the app actually does
(`PRIVACY.md` in the app repo). Every factual claim is one the code currently
keeps. They have not been reviewed by a lawyer.

## The URLs the app links to

Settings opens these exact addresses, and App Review opens them too:

    https://kaanbozkurt21.github.io/glowscan-legal/privacy.html
    https://kaanbozkurt21.github.io/glowscan-legal/terms.html

GitHub Pages, which is where `scrollmind-legal` and `scrollgames-legal` already
live — the same pattern, and it serves HTML as HTML. Two other hosts were tried
first and neither did: `glowscan.app` serves a different product, and Supabase
Storage records a content type when an object is created and hands these back as
`text/plain`, so a reviewer would have read the markup rather than the page.

Links between the pages are relative, not root-relative. The site sits under
`/glowscan-legal/`, so `href="/privacy"` leaves it entirely.

If these ever move, the two URLs in `SettingsView.swift` have to move with them —
`LegalLinkTests` asserts they are the ones that are live, because a link the app
makes and the host does not serve is a rejection on its own.
