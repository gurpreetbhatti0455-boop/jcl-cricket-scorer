JCL Cricket Scorer + Firebase Overlay prototype

Files:
- index_firebase.html: scorer app; after toss it generates a Match Code and Overlay Link, then allows player selection.
- overlay_firebase.html: read-only live scoreboard for PRISM/browser overlay.
- firestore.rules: rules for public read-only overlay and owner-only writes.

Before testing:
1. In Firebase Console > Authentication > Sign-in method, enable Anonymous.
2. In Firestore Database > Rules, publish firestore.rules.
3. Host both HTML files on the same HTTPS Firebase Hosting site. Rename index_firebase.html to index.html and overlay_firebase.html to overlay.html when uploading/deploying.
4. Open the hosted index.html, start a match, confirm toss. Copy the generated link, then continue to select the opening batsmen and bowler.
5. Add the link as a browser/web overlay in PRISM Live Studio. Score updates should appear in realtime.

Important:
- The Firestore collection name is case-sensitive. This version writes to `Matches` (capital M), matching the user's existing database.
- The match code is a secret-style link identifier. Anyone with the overlay link can view that match's public score. Do not put private information in these fields.
- Firebase client config is intended for browser apps; never place service-account private keys in HTML.
- This is a prototype. Test with a dummy match before using it for a real broadcast.
