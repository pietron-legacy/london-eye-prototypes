London Eye — Ticketing Prototype
================================

Landing page: index.html  (open this to start)

HOW TO RUN
----------
Option A — double-click index.html
  Opens in your browser via file://. Everything works offline except the
  web-font (falls back to a system font) and the small map on the plan view.

Option B — run a local web server (recommended, closest to production)
  From this folder, run:
      python3 -m http.server 8000
  then open  http://localhost:8000  in your browser.

TWO FLOWS (both start on index.html and end on checkout.html)
-------------------------------------------------------------
Standard plan:  index → schedule (date + tickets) → addons → upsell
                (fever-bundle) → checkout
Cluster plan:   index → attraction-picker → schedule (plan view) → addons
                → checkout

FILES
-----
index.html ...................... landing page
attraction-picker.html .......... cluster: "Build your perfect visit"
schedule.html ................... date + tickets (and cluster plan view)
addons.html ..................... "Add more to your visit"
fever-bundle-prototype_1.html ... standard upsell "Add now and save"
checkout.html ................... confirm & pay
*.png / *.jpg ................... image assets used by the pages

NOTES
-----
- State is passed between pages via the browser's localStorage. To reset to a
  clean session, open index.html (it clears prior selections) or clear the
  site's localStorage in DevTools.
- No build step, no dependencies to install — plain HTML/CSS/JS.
