JCL Cricket Scorer — Secure Spark Build

Files
- index.html: scorer app; private match state is owner-only and public scoreboard data is published separately.
- overlay.html: reads only PublicMatches, which contains scoreboard fields only.
- firestore.rules: owner-only private match rules and public read-only scoreboard rules.

Important behavior change
- Five-digit Umpire Code resume is removed. To resume a match on another device, sign in with the SAME Google account that created the match.
- Anyone with the overlay link can view the public score, but cannot read FullState through the public scoreboard document.
- This build is prepared for Firebase Spark; no Cloud Functions are required.

Before publishing
1. Keep a backup of the current GitHub index.html, overlay.html, and current Firestore Rules.
2. In the GitHub repository, replace index.html and overlay.html with the two files from this package. Commit the changes.
3. In Firebase Console > Firestore Database > Rules, replace the rules with firestore.rules and click Publish.
4. Reload the app. Sign in with Google, create a test match, enter the opening players, and confirm the match starts.
5. Open the copied overlay link in a private/incognito tab. Confirm the score appears and updates when you add runs.
6. Test Match History and resume on a second device/browser signed into the SAME Google account.
7. Test All Live Matches: it should show public score and open the overlay, not allow resuming another person's match.

Migration note
Existing private Matches documents remain private after the new rules are published. Existing old matches may not appear in PublicMatches until opened by their owner in the updated scorer and synced. Never loosen the private Matches read rule to fix an overlay error; check that the updated overlay reads PublicMatches instead.

Validation performed
- JavaScript syntax checks passed for the script blocks in index.html and overlay.html.
- Firebase Rules were prepared but not deployed or emulator-tested. Test on a temporary/test match before relying on this during a live game.
