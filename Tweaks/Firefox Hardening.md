1. Use the recommended privacy settings (about:preferences)
- Use "Strict" content blocking (Settings → Privacy & Security)
- Disable search suggestions; set a privacy search engine (DuckDuckGo/Startpage)
- Turn off "Allow sites to save and re-fill form data"

2. Harden about:config — paste about:config in the URL bar, search and set:
privacy.trackingprotection.enabled = true
privacy.trackingprotection.socialtracking.enabled = true
privacy.firstparty.isolate = true          # isolate site data
privacy.resistFingerprinting = true        # spoofs fingerprint (can break sites)
privacy.donottrackheader.enabled = false   # DNT is a track signal; leave off
network.cookie.lifetimePolicy = 2          # cookies to session only
browser.send_pings = false                 # blocks link pingbacks
media.peerconnection.enabled = false       # disables WebRTC IP leak
webgl.disabled = true                      # reduces fingerprinting surface
geo.enabled = false                        # disables geolocation
beacon.enabled = false                     # no background telemetry
browser.urlbar.suggest.searches = false

3. Add defensive add-ons
- uBlock Origin — the single best hardening tool (also add the "uBlock filters – Privacy" and "Fanboy Annoyances" lists)
- Privacy Badger — learned tracker blocking
- ClearURLs / Neat URL — strips tracking parameters from links
- Add-ons should only have the permissions they need; disable about:addons extra permissions

4. Behavior habits (matter more than config)
- Use Firefox Containers (Multi-Account Containers) to isolate logins/sites: google in one container, banking in another, shopping in another
- Log out of sites you aren't actively using
- Clear history/cookies on exit (Settings → clear on close)
- Keep Firefox updated; add-ons updated; only install add-ons from addons.mozilla.org

5. For strict hardening — use the arkenfox user.js project; it's a well-vetted, community-maintained hardening profile that overrides all of the above (and much more) correctly and keeps itself updated against regressions.
Caveat: heavy hardening (resistFingerprinting, WebRTC off, cookies to session) will break some sites — payments, some logins, video calls. If something breaks, temporarily toggle the specific flag, not everything.


