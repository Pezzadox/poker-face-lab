# Poker Face Lab

Watch a face react, moment by moment: a live wireframe, a reaction gauge and a science check on the old body-language tales. For fun and curiosity, not lie detection.

- `www/` is the whole app: one page, the [Human](https://github.com/vladmandic/human) face library and its models (blazeface, facemesh, iris, emotion). Everything runs on the device; nothing is sent anywhere.
- `android/` wraps it with Capacitor for Google Play (`com.pezzadox.pokerfacelab`).
- `docs/privacy.html` is the privacy policy, served by GitHub Pages.
- `store/listing.md` holds the Play listing text and data-safety answers.

## Build

The Release workflow (Actions → Release → Run workflow, version e.g. `1.0.0`) builds a signed `.aab` and puts it on the `play-bundles` branch. It needs the `ANDROID_KEYSTORE_BASE64`, `ANDROID_KEYSTORE_PASSWORD`, `ANDROID_KEY_ALIAS` and `ANDROID_KEY_PASSWORD` secrets, which `make-more-android-keys.ps1` sets.

Locally: `npm ci && npx cap sync android && npx cap open android`.

The face library and models are © Vladimir Mandic and Google, under their own licences (MIT and Apache 2.0).
