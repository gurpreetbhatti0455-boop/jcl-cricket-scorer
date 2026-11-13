Cricket Scorer by JCL — overlay layout refinement

Replace both files in your existing GitHub repository:
- index.html (included unchanged from the uploaded source)
- overlay.html (updated layout)

Overlay changes:
- Scoreboard now spans the full screen width, flush to both edges.
- Vertical height reduced to about 75% of the earlier lower-third height.
- Batter name, runs (balls), and 4s/6s now appear on one line.
- Centre batting/score panel widened; target panel narrowed.
- First innings without a target shows toss winner, overs limit and projected score.
- Innings indicator explicitly shows INNINGS 1 or INNINGS 2.
- When target is set, chase target and runs/balls remaining cycle as before.

Note: projected value is a projected total score based on the current run rate, not a projected run-rate figure.
The app's Firebase public payload already includes Toss and MaxOvers, used by the overlay.
After GitHub Pages deploys, refresh/re-add the overlay URL in PRISM.

Validation: source updated; run the live match and PRISM checks after deployment.
