SCARLET'S SUPER CHECKOUT — FULL PWA

NEW IN THIS BUILD:
- Scanner success beep and checkout sounds.
- Gift Card payment mode.
- Gift-card barcode scanning during checkout.
- Pretend gift-card balances are stored locally by card number.
- Gift cards can be scanned or entered manually.
- If a stored gift-card balance exists, it is reused.
- Gift cards are pretend/local only; this app does NOT access or charge real gift cards.

HOSTING:
Upload this entire folder to an HTTPS static host such as GitHub Pages.
Open the HTTPS URL in Chrome on Android and choose Install app / Add to Home screen.

CAMERA:
Camera access requires HTTPS (or localhost) and permission from Chrome.
BarcodeDetector support varies by browser. Manual code entry remains available.

PICTURE MODE:
TensorFlow.js + MobileNet are loaded from jsDelivr when picture recognition
is first used, so picture recognition needs internet initially.

PARENT PIN:
Default PIN is 1234. Change it under Parent Mode.
