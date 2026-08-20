# glowscan-legal

The privacy policy and terms for the GlowScan iOS app. Static, self-contained,
English then Turkish on each page — KVKK requires a Turkish notice and an English
policy does not discharge it.

Both are written from the engineering account of what the app actually does
(`PRIVACY.md` in the app repo). Every factual claim is one the code currently
keeps. They have not been reviewed by a lawyer.

## The URLs the app links to

Settings opens these exact addresses, and App Review opens them too:

    https://legal.glowscan.app/privacy
    https://legal.glowscan.app/terms

A subdomain rather than the app's own root, because `glowscan.app` serves a
different product — and separate from it on purpose: a policy page must not be
able to go down because a marketing site was redeployed.

Vercel resolves extensionless paths to the matching `.html`, so deploying this
repo at that subdomain serves both with no configuration. If it ever moves, the
two URLs in `SettingsView.swift` have to move with it — `LegalLinkTests` asserts
they are the ones that are live, because a link the app makes and the host does
not serve is a rejection on its own.
