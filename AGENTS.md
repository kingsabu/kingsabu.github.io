# 한눈 사이트 (developer website for the 한눈 app series)

- Purpose: the public developer website of the 한눈 series of Google Play apps (operator, 2026-11-01). Google Play needs a privacy policy address for each app, and
  AdMob needs app-ads.txt at the root of the developer website listed in the store, so this static site holds both. It is plain HTML with no build step, no
  scripts and no outside fonts; every page keeps the light and dark colours of index.html and reads well on a phone.
- Layout: index.html lists the apps; each app has its own folder named after its store name in romanization (hannun-gauge for 한눈계기판) with privacy.html and
  any other page that app needs; app-ads.txt stays at the root, one line per AdMob publisher ID in the form `google.com, pub-<id>, DIRECT, f08c47fec0942fa0`
  (added once the operator's AdMob account exists); .nojekyll keeps GitHub Pages from rewriting files.
- Hosting: GitHub Pages user site of the operator's GitHub account kingsabu, repository kingsabu.github.io, so the site lives at https://kingsabu.github.io and
  app-ads.txt at https://kingsabu.github.io/app-ads.txt (github.io is a public suffix, so that host is its own root domain). Publishing makes every file public:
  push only after the operator agreed to publish that change. A custom domain can point at the same site later without moving it.
- The privacy policy of each app lives only here; the app repositories link to its address (play_gauge docs/store-listing.md). When an app starts to collect
  something new or its ads SDK changes what it gathers, change its privacy.html with a new 시행일 in the same task.
- Hard wrap 170 columns, no comments, UTF-8 without BOM, LF line endings.
