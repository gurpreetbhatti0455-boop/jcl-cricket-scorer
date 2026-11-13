CRICKET SCORER BY JCL - FINAL OVERLAY UPDATE

Files included:
- index.html: scorer application file (included unchanged from the previous full package)
- overlay.html: updated PRISM broadcast overlay

Changes in this update:
1. SIX / FOUR / WICKET / milestone celebration temporarily hides the live lower scoreboard, so the celebration text is shown cleanly. The scoreboard returns after the animation.
2. Main score (runs/wickets and overs) is lifted slightly and given a little more bottom spacing.
3. Third / chase information panel is nudged slightly down and remains vertically centered.
4. The separate green result strip is disabled.
5. After the existing 15-second celebration delay, the final match-result panel covers the entire lower scoreboard. The live scoreboard disappears while the result panel is shown.
6. First innings and second innings scorecards remain side-by-side, with compact batting, bowling, partnerships and fall-of-wickets details sized to fit one screen as far as the available data and screen dimensions allow.

GitHub upload:
- Replace index.html and overlay.html in the repository with the two files in this ZIP.
- Commit the changes and wait for GitHub Pages to deploy.
- Refresh the scorer page and re-add/refresh the overlay URL in PRISM.

Validation:
- JavaScript syntax check passed with Node.js.
- ZIP integrity check passed.
- Firebase live data, PRISM animation timing, and real-device one-screen fit still need to be tested in your actual match setup.
