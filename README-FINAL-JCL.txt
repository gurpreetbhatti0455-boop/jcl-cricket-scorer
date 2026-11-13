Cricket Scorer by JCL — Same App Icon Logo Everywhere
Build date: 13 November 2026

FILES TO UPLOAD TO THE SAME GITHUB REPOSITORY ROOT
- index.html
- overlay.html
- jcl-logo.png
- jcl-logo-icon.png

LOGO
Both logo image files now use the exact cricket ball-and-bat app icon shown in the user's Play Store screenshot. The same image is used on the app home screen, scorer header and PRISM overlay top brand area.

OTHER INCLUDED CHANGES
1. Match Setup has one large, full-width START NEW MATCH button; Update names/details and Overlay-only preview are removed from that setup screen.
2. Match History cards show date/time, both team names and scores, then toss details for an in-progress match or the saved result for a completed match.
3. Each history card has Resume, Copy Overlay, Scoreboard and Delete actions.
4. Delete asks for confirmation and checks that the signed-in Google account owns the match before deleting its private match record and public overlay record.

DEPLOYMENT
1. Back up the current repository files.
2. Upload/replace all four files above in the repository root. Keep both PNG files beside index.html and overlay.html; do not put them in a subfolder.
3. Commit and wait for GitHub Pages to deploy.
4. Hard-refresh the scorer page. Refresh or re-add the PRISM website source.

VALIDATION
- JavaScript syntax checks and ZIP integrity check passed.
- Firebase deletion permissions, legacy saved-match rendering, actual device display and PRISM broadcast still need live testing.
