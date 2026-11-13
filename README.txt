Cricket Scorer by JCL — Full package with Bowler / This Over layout update

Files:
- index.html: current scorer application file included for a complete backup/package.
- overlay.html: updated PRISM overlay.

Overlay changes:
1. Bowler heading is shown at the top with OVER number at the right.
2. Bowler name appears on the next line.
3. Bowler figures (wickets, runs, overs) appear on the next line.
4. THIS OVER: appears immediately before the ball-by-ball row; the separate top "Bowler · This over" heading has been removed.

Deployment:
- Back up your current GitHub files first.
- Replace index.html and overlay.html from this ZIP if you want the complete package deployed together.
- If index.html has newer changes than the included copy, keep your newer index.html and replace only overlay.html.
- After GitHub Pages deploys, hard-refresh the scorer and refresh/re-add the overlay URL in PRISM.

Validation:
- JavaScript syntax and ZIP integrity should be checked locally; full Firebase/scoring/PRISM live testing is still required.
