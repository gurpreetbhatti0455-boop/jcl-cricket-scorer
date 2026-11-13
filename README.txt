JCL Cricket Scorer - Match History Update

Included files:
- index.html: updated Match History layout and actions
- overlay.html: existing JCL overlay version retained from the previous logo/setup update

Match History now shows:
- Match date and time
- Each team's name with its own score and overs
- Toss information
- Resume
- Copy Overlay
- Scoreboard
- Delete

Delete asks for confirmation, verifies that the signed-in Google account owns the match, and removes the private match record plus its public overlay record when possible.

Deployment:
1. Back up your current GitHub index.html and overlay.html.
2. Replace both files with the files in this ZIP (overlay.html is included unchanged from the previous update).
3. Commit the changes and wait for GitHub Pages to deploy.
4. Refresh the app. Sign in with the same Google account used to create the matches.

Validation:
- Inline JavaScript syntax checked with Node.js.
- ZIP integrity checked.
- Live Firebase deletion, score rendering across legacy records, and browser/PRISM behavior still need testing in your account.
