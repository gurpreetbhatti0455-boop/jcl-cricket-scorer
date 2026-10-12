JCL Cricket Scorer — Firebase Sync + Tournament Start + History Fix

Included files:
- index.html: fixes the Multiple Match History error (multiResultsHtml is now available to the history screen) and starts the first tournament match immediately after saving the team list, opening the normal toss setup for the first two teams.
- overlay.html: the current overlay file from the latest provided package, preserving the existing batting/bowling and match-result presentation.
- firestore.rules: proposed secure Firestore rules for private owner-only Matches and publicly readable scoreboard-only PublicMatches. PublicMatches writes are limited to the signed-in owner of the corresponding private match.

IMPORTANT — Firebase rules must be published in Firebase Console:
1. Open Firebase Console > project jcl-cricket-scorer > Firestore Database > Rules.
2. Save a backup of your current rules first.
3. Open the included firestore.rules file and copy its full contents into the Rules editor.
4. Click Publish.
5. Do not expect uploading firestore.rules to GitHub alone to change Firebase security rules.

GitHub update:
1. Replace index.html and overlay.html in the root of the existing repository.
2. Commit both files and wait for the newest GitHub Pages deployment to show Success.
3. Open the site in Chrome Incognito and test a short match.

Safety/validation notes:
- JavaScript syntax checked with Node.js.
- Firebase/PRISM were not end-to-end tested here.
- These rules assume the app uses only the Matches and PublicMatches collections described in the app. Review any additional collections/rules in your existing project before replacing your full ruleset. Keep a backup and never use open write permissions for all users.
- Tournament setup now launches Match 1 after saving team names; full automated league fixtures/quarter-final/semi-final/final bracket logic is not implemented by this patch.
