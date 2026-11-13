Cricket Scorer by JCL — Target Auto-End, Final Scorecard & Wicket Dialog Readability Update
Build date: 13 November 2026

FILES
- index.html: scorer application and PDF scorecard.
- overlay.html: PRISM overlay and final match result scorecard.

CHANGES
1. Kept the previous target auto-end and final scorecard functionality.
2. Increased the final overlay scorecard font sizes for innings headings, scores, batting, bowling, partnerships, fall of wickets and result text. The innings panels can scroll if a long scorecard needs more room; phone layout stacks the innings panels vertically.
3. Overlay batter and bowler names use Title Case. Not-out batters retain the * marker.
4. Wicket dialog now pre-fills the next batter field with a suggested name such as “Batter 3”. Focusing the field selects the suggestion so the scorer can type the actual name immediately.
5. Confirm Wicket is blocked when the next batter is required but the field is blank or still contains the generic “Batter N” suggestion. A clear alert explains that the actual batter name is required. On the final wicket, no replacement name is required.
6. Enlarged wicket dialog labels, inputs and confirmation button for easier use.

DEPLOYMENT
1. Back up both current repository files.
2. Replace index.html and overlay.html with the files in this ZIP.
3. Commit and wait for GitHub Pages to deploy.
4. Refresh the scorer page. Refresh/re-add the PRISM overlay URL to load the updated overlay.

VALIDATION
- JavaScript syntax checks are included in the build validation.
- Wicket dialog validation and final scorecard layout were reviewed in source.
- Live Firebase, actual phone/browser interaction, print/PDF and PRISM broadcast still require a real-device test before an official match.
