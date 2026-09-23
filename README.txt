SCARLET'S SUPER CHECKOUT — FULL PWA

NEW:
- Unknown barcodes can be auto-added to the store.
- When a new barcode is scanned, the app asks for the product name and price,
  saves the barcode, and immediately adds it to the local store.
- The new item can be edited later in Parent Mode.
- Gift-card barcode scanning is supported for pretend payments.
- Scanner success sounds are included.

ANDROID:
Works as an installable PWA in a modern Android browser. Camera access requires
HTTPS and browser camera permission.

IPAD / IPHONE:
The PWA layout is designed to work on iPad and iPhone as well. Install it from
Safari using Share -> Add to Home Screen. Camera permission is required.
Because barcode-detection APIs vary by browser, the app keeps manual barcode
entry as a fallback. For maximum cross-browser barcode compatibility, a future
build can use a dedicated JavaScript barcode library instead of relying only on
the browser BarcodeDetector API.

IMPORTANT:
Gift cards are pretend/local only. The app does not access, validate, or charge
real gift cards.

PICTURE MODE:
TensorFlow.js + MobileNet load from jsDelivr the first time picture recognition
is used, so picture recognition needs internet initially.

PARENT PIN:
Default PIN is 1234. Change it under Parent Mode.


KID-FRIENDLY AUDIO:
- Product scan announces product name and price.
- New cart total is announced after each item.
- Successful scans use a two-tone chime.
- Checkout announces payment/change and thanks the shopper.
- Picture/voice features remain optional and can be used with device volume on.

PUSHING UPDATES TO GITHUB PAGES:
If the repository is already set up:
1. Extract the newest ZIP.
2. In GitHub open your scarlet-super-checkout repository.
3. Tap Add file -> Upload files.
4. Upload the NEW index.html and any changed files.
5. Commit changes to the main branch.
6. Wait for GitHub Pages to redeploy.
7. On the phone/iPad, close the installed app and reopen it.
8. If the old version is still cached, open the site in Chrome/Safari first,
   refresh it, then relaunch the installed PWA. If necessary, remove/reinstall
   the home-screen app to force a fresh service-worker cache.

IMPORTANT:
Because the service worker caches the app, incrementing its CACHE name in sw.js
is the most reliable way to force an update. In this package it is already
versioned; when you make future code updates, change e.g.
scarlet-checkout-full-v1 -> scarlet-checkout-full-v2 in sw.js, upload sw.js,
and reload the site.
