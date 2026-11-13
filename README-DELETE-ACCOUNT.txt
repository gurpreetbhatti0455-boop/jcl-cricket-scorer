CRICKET SCORER BY JCL — DELETE ACCOUNT UPDATE
Build date: 13 November 2026

FILES IN THIS ZIP
1. index.html — adds a Delete My Account link on the signed-in home screen.
2. delete-account.html — public account-deletion page for Google Play Data safety.
3. overlay.html — included unchanged; keep it with the same app deployment.

GITHUB PAGES DEPLOYMENT
1. Back up the current repository files.
2. Upload/replace index.html and overlay.html in the repository root.
3. Add delete-account.html in the SAME repository root (beside index.html).
4. Keep existing jcl-logo.png, jcl-logo-icon.png, manifest.json and other app assets in place.
5. Commit and wait for GitHub Pages to deploy.
6. Open and test:
   https://gurpreetbhatti0455-boop.github.io/jcl-cricket-scorer/delete-account.html
7. In Google Play Console > Data safety, use that exact URL as the account deletion URL.

WHAT THE PAGE DOES
- Signs the user in with Google and asks for a fresh Google verification.
- Finds documents in Firestore Matches where OwnerUid equals the signed-in user's UID.
- Deletes each corresponding PublicMatches document and private Matches document.
- Deletes the Firebase Authentication account last.
- Clears JCL-prefixed localStorage keys on the device used for deletion.

IMPORTANT LIMITATIONS / LIVE TEST REQUIRED
- This update is based on the supplied index.html and current Firebase collection names (Matches, PublicMatches; OwnerUid).
- No firestore.rules file was supplied. Firestore security rules must permit an authenticated owner to delete their own Matches document and its matching PublicMatches document. If rules deny either deletion, the page will show an error and will not claim the account was deleted.
- This page does not delete data in any other Firebase collection or external service not present in the supplied source files.
- Test with a separate test Google account and test matches before submitting the Play Console form. Verify that both private and public match records disappear and that the Authentication user is removed.
- JavaScript syntax checks passed. Firebase permissions, Google popup/re-authentication, real deletion, and Play Console acceptance have not been live-tested.
