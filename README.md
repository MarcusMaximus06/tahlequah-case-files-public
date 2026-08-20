# Tahlequah Case Files — public site

**This repository is safe to be public.** It may be shared with anyone.

It contains only pre-approved public case material: pages that a human
deliberately walked through fact-check and legal/sensitivity review and then
explicitly approved for publication. It holds no database, no evidence files, no
research notes, no leads, no private editorial drafts, and nothing about any case
that has not been approved.

## Do not hand-edit these files

Everything here is **generated** from the private Tahlequah Case Files research
vault. Any edit made directly in this repository will be silently overwritten the
next time the site is published.

To change what appears here:

1. Make the change in the private system (the desktop app or its CLI).
2. Approve it for publication there, if it is new material.
3. Run `PUBLISH_PUBLIC_SITE.bat` in the private project.
4. Commit and push from this repository.

## How this repository is produced

`tools/publish_public_site.py` in the private project regenerates the public
export from the database, runs a leak scan against it derived from the database
itself, and only then mirrors the result into this repository. If the scan finds
any trace of unapproved material, the publish fails and nothing is copied.

Nothing is ever published automatically. A person has to decide, every time.

## Hosting

Deployed via Cloudflare Pages from the connected branch of this repository.
`_headers`, `robots.txt`, `sitemap.xml` and `404.html` are Cloudflare Pages
configuration and live only here.

See `DEPLOY_INSTRUCTIONS.md` in the private project's `deploy/` folder for setup.
