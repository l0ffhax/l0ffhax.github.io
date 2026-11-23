# Public pages for l0ffhax.github.io

This folder holds Znixx's public web pages. They live here so they're versioned with the
game, but they're **published from a separate public repository**: `l0ffhax/l0ffhax.github.io`
(this app repo is private, and GitHub Pages needs a public repo on the free plan).

| File                       | Published at                                   | Used for                                   |
|----------------------------|------------------------------------------------|--------------------------------------------|
| `znixx/index.html`         | https://l0ffhax.github.io/znixx/               | Store listing "website" field              |
| `znixx/privacy/index.html` | https://l0ffhax.github.io/znixx/privacy/       | Play Console privacy policy URL (required) |

## Publish (one time)

1. On GitHub, create a **public** repository named exactly `l0ffhax.github.io`.
2. Copy the contents of this folder into it (keep the `znixx/` folder) and push:
   ```bash
   git clone https://github.com/l0ffhax/l0ffhax.github.io.git
   cp -r site/znixx l0ffhax.github.io/
   cd l0ffhax.github.io && git add . && git commit -m "Add Znixx pages" && git push
   ```
3. In that repo: Settings → Pages → Source: *Deploy from a branch*, branch `main`, folder `/ (root)`.
4. After a minute, open https://l0ffhax.github.io/znixx/privacy/ and check it loads.

The contact address in `znixx/privacy/index.html` is the one players see; use the same one in
Play Console's store listing contact details.

## Later: tappable https shape links

Because a user site serves from the domain root, it can also host
`/.well-known/assetlinks.json`, which Android needs to open `https://l0ffhax.github.io/znixx/s/<code>`
links straight in the app (App Links). That needs the SHA-256 fingerprint of the Play app signing
key, so it's a post-launch step: see "Shape links over https" in `docs/release.md`.
