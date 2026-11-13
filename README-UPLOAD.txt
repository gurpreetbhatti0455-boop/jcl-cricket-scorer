CRICKET SCORER BY JCL — FINAL READY UPDATE
Build: 13 November 2026 (r5)

UPLOAD THESE FILES TO THE ROOT OF THE EXISTING GITHUB REPOSITORY
- index.html (replace)
- overlay.html (replace)
- delete-account.html (add or replace)
- manifest.json (replace)
- jcl-logo-icon-new.png (add)
- jcl-app-icon-192.png (add)
- jcl-app-icon-512.png (add)

KEEP THESE EXISTING REPOSITORY FILES — DO NOT DELETE
- firestore.rules
- privacy-policy.html
- googled...html (Google Search Console verification file; keep exact existing filename)
- Any other existing Firebase / app files not listed above.

WHAT THIS UPDATE INCLUDES
1. Official cricket-ball-and-bat JCL logo on the home screen, app header, PRISM overlay, and app icons/manifest.
2. Small Delete My Account link at the bottom of the signed-in home content, below Instructions.
3. Account-deletion page for the Google Play Data safety account-deletion URL.
4. Scoring-button click handler hardened with delegated click handling, explicit button type, and visible error reporting.
5. Existing match history, multiple-match, Firebase, scorecard, partnerships, fall-of-wickets, and overlay functionality retained from the supplied build.

DEPLOY
1. Back up the current repository first.
2. Upload/replace the seven files above in the repository ROOT (same level as index.html).
3. Commit changes and wait for the green github-pages deployment.
4. Open https://gurpreetbhatti0455-boop.github.io/jcl-cricket-scorer/ and refresh.
5. Test a new match: score 1, 4, and 6 and confirm the score changes immediately.
6. Refresh/re-add the overlay URL in PRISM if it is still showing an old cached version.

GOOGLE PLAY DATA SAFETY
Account deletion URL:
https://gurpreetbhatti0455-boop.github.io/jcl-cricket-scorer/delete-account.html

IMPORTANT TESTING NOTE
HTML/JavaScript syntax and ZIP integrity are checked. A live GitHub Pages + Firebase + PRISM test cannot be completed from this offline file workspace. Test with a separate test Google account before using the account-deletion page on a real account. Do not test deletion using your main account.
