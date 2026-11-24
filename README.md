# l0ffhax.github.io

Public web pages, served by GitHub Pages at https://l0ffhax.github.io/ (Settings → Pages: deploy
from branch `main`, folder `/`).

## Znixx

| File                       | Published at                             | Used for                                   |
|----------------------------|------------------------------------------|--------------------------------------------|
| `znixx/index.html`         | https://l0ffhax.github.io/znixx/         | Store listing "website" field              |
| `znixx/privacy/index.html` | https://l0ffhax.github.io/znixx/privacy/ | Play Console privacy policy URL (required) |
| `znixx/icon.png`           | https://l0ffhax.github.io/znixx/icon.png | Icon on both pages                         |

The pages are written in the Znixx app repository (private), in its `site/znixx/` folder, so they
change together with the game. To publish a change, copy that folder over this repo's `znixx/`
folder, check the diff, commit and push. Pages updates a minute or two later.

The privacy policy's contact address is the one players see; Play Console's store listing uses
the same one.

## Later

Because this is a user site served from the domain root, it can also host:

- `/.well-known/assetlinks.json`, so `https://l0ffhax.github.io/znixx/s/<code>` shape links open
  straight in the app (Android App Links; needs the Play app signing key's SHA-256 fingerprint);
- `/app-ads.txt`, which AdMob asks for once ads are live (AdMob shows the line to put in it).

The repository was once named `znixx.github.io`; GitHub redirects that name here.
