# glowscan-legal

The privacy policy and terms for the GlowScan iOS app. Static, self-contained,
English then Turkish on each page — KVKK requires a Turkish notice and an English
policy does not discharge it.

Both are written from the engineering account of what the app actually does
(`PRIVACY.md` in the app repo). Every factual claim is one the code currently
keeps. They have not been reviewed by a lawyer.

## The URLs the app links to

Settings opens these exact addresses, and App Review opens them too:

    https://glowscan.app/privacy
    https://glowscan.app/terms

Vercel resolves extensionless paths to the matching `.html`, so deploying this
repo at that domain serves both without configuration. If it is deployed
somewhere else, the two URLs in `SettingsView.swift` have to change to match — a
link the app makes and the host does not serve is a rejection.
