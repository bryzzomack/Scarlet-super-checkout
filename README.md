# Scarlet's Super Checkout — Kid Fun Edition

This version is designed for a 5-year-old and includes:
- iPad + Android camera barcode scanning
- environment/back camera selection
- barcode detection using the browser's BarcodeDetector API when available
- a manual barcode fallback when automatic detection is unavailable
- talking checkout: item name, price, and running total
- produce PLU lookup
- price check
- automatic "NEW ITEM!" setup for unknown barcodes
- fun sounds, celebration confetti, emojis, bagging station
- pretend cash, pretend card, and pretend gift-card payments
- pretend receipt
- parent station with PIN
- export/import store data so products can be moved between devices
- installable PWA

## iPad barcode scanning
Open the HTTPS GitHub Pages URL in Safari and allow Camera access.
For best results, use Safari on the iPad, hold the barcode steady, and keep it well lit.
Some iPad/browser combinations may not expose BarcodeDetector. The app detects that and leaves the manual Enter Code option available.

## Important
This is a pretend checkout for play. Gift cards and payments are local pretend balances only.
No real payment or gift-card system is connected.

## GitHub Pages update
Replace the files in your existing repository with the new index.html, manifest.webmanifest, sw.js, and icons. Commit to main. The service-worker cache is versioned v8 to force a fresh app shell.

## Moving the pretend store
Parent Station -> Export Store on the old device.
On the new device, Parent Station -> Import Store and select the JSON file.


## New in v8
- Scanner appears near the top when activated.
- One camera session can scan multiple products without reopening the scanner.
- Voice uses the best available natural English system voice and a slower, friendlier delivery.
- Price Check announces itself and generates a random pretend price.


## New in v8 — Faster, More Lifelike Scanning
- Continuous scan mode: one camera session can scan item after item.
- Faster barcode polling with duplicate protection.
- ZXing browser fallback is included for iPad/browser combinations without BarcodeDetector.
- Known store items are added instantly.
- Unknown food barcodes can be looked up through Open Food Facts. The documented API provides product-by-barcode lookup; the app uses the product name when available. citeturn0search0turn0search1
- If a barcode isn't found or the internet is unavailable, the checkout automatically creates a pretend Mystery Grocery instead of asking Scarlet to type anything.
- Scanner has a READY / BEEP / NEXT ITEM flow.
- Scanner uses a higher-resolution rear camera request when available.


## v8 repair
Fixed the broken JavaScript that prevented buttons from working. Cache version bumped to v8.


## v8 — One-Tap Kid Scanning
The iPad no longer depends on barcode detection. Scarlet can open Scan mode and simply tap the large green **SCAN ITEM!** button. Every tap instantly creates a fun pretend grocery item and a randomly generated pretend price, announces it, adds it to the cart, and keeps the scanner ready for the next tap. No typing is required.
