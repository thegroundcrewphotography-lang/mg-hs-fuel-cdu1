MG HS FUEL CDU v6 — HOSTED HTML / PWA
========================================

WHY THE SCREENSHOT SHOWED GPS MANUAL + DATA FAIL
The browser URL was:
content://media/external/file/...

That is Android's local document/content provider. It is NOT the same as loading this project from an HTTPS website.
v6 now detects this correctly and displays:
CONTENT:// — GPS/API LIMITED

LIVE MODE REQUIREMENTS
Use one of:
- https://your-site/.../index.html
- http://localhost/.../index.html on the same device for GPS testing

For the installable PWA/service worker, HTTPS is the normal deployment method.

FILES TO HOST TOGETHER
- index.html
- manifest.webmanifest
- sw.js
- icon-192.png
- icon-512.png

EXPECTED DATA PAGE WHEN HOSTED CORRECTLY
URL SCHEME      HTTPS
HOST MODE       VALID
LIVE CAPABLE    YES
PWA             YES
GPS             LIVE (after permission)
PERMISSION      GRANTED
PWA CACHE       READY

FUEL API
The CDU supports:
1. API.NSW demo mode
2. your API.NSW credentials
3. an HTTPS proxy endpoint (recommended for reliable browser operation)

If API.NSW rejects direct browser requests because of browser/CORS/network policy, configure the proxy endpoint.
Do not put private long-lived API secrets into public client-side HTML.

SAFETY
Planning aid only. Verify against the vehicle fuel gauge and navigation.
Do not interact with it while driving.
