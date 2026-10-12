JCL CRICKET SCORER — FINAL TOURNAMENT / MULTIPLE MATCH FIX

Files in this package:
- index.html — tournament setup, multiple-match history/results, scoring app, and Firebase publishing.
- overlay.html — live overlay and completed-match result display.
- firestore.rules — owner-only private match writes and public read-only overlay rules.

IMPORTANT FIX
The Multiple Match results renderer is now defined at top-level and exposed as window.__JCL_multiResultsHtml. Both Multiple Match History and the completed-match panel call the global function, so they do not depend on render()'s local scope. This addresses the “multiResultsHtml is not defined” error.

INSTALL
1. Back up your current GitHub index.html, overlay.html, and Firebase Firestore rules.
2. Replace the repository's index.html with this package's index.html (keep the filename index.html).
3. Replace the repository's overlay.html with this package's overlay.html (keep the filename overlay.html).
4. Commit the changes and wait for GitHub Pages to deploy.
5. On your phone, open the scorer in Chrome and reload the page. If the old error remains, open the site in an Incognito tab to bypass cached files.

FIREBASE PERMISSIONS
If the app still shows “Missing or insufficient permissions”, the rules file must be published separately:
1. Firebase Console > Firestore Database > Rules.
2. Back up the existing rules, then paste the contents of firestore.rules and click Publish.
3. Firebase Console > Authentication > Sign-in method: ensure Google sign-in is enabled.

TEST BEFORE A LIVE MATCH
- Open Multiple Match mode and open Multiple Match History.
- Set up a tournament, save team names, and verify it opens toss setup for the first match.
- Start a dummy match and check that the overlay updates.
- Complete a dummy match and confirm the result appears.

LIMITATIONS
Tournament team names are stored locally in this browser. Automatic tournament fixtures/brackets are not implemented. Firebase behavior must be verified against the user's live project after publishing; these files cannot deploy changes to GitHub or Firebase automatically.
