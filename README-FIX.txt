Cricket Scorer by JCL — dismissal fielder and partnership update

Files in this ZIP:
- index.html
- overlay.html

Changes:
1. Caught, Run out and Stumped require a fielder name in the wicket dialog.
2. Dismissal type and fielder name are stored separately in the fall-of-wickets record.
3. PDF scorecard shows dismissal type and fielder, plus partnership batter names, runs and balls.
4. Firebase public match scorecards now include fall-of-wickets and partnership details.
5. The final PRISM overlay scorecards show partnerships (batters, runs, balls) and fall of wickets (dismissed batter, dismissal type, fielder and over).
6. Partnership entries capture the two batters at the time of the wicket and the partnership balls.

Deploy:
1. Back up the current GitHub files.
2. Replace BOTH index.html and overlay.html in the existing repository.
3. Commit and wait for GitHub Pages to deploy.
4. Refresh the scorer and refresh/re-add the overlay URL in PRISM.

Validation:
- JavaScript syntax check only. Full live Firebase, PDF print and PRISM match testing is still required.
- Old saved matches may not contain fielder or partnership-ball data; the new fields are recorded for matches scored with this update.
