JCL Cricket Scorer — Separated Histories Update

Files:
- index.html: based on the user's uploaded current index.html. Multiple Matches now opens a separate new-session setup screen with session name, total team count, team-name inputs, and Start First Match. Multiple Match History is available only through its separate History option. Existing Tournament History and regular Match History sections remain separate.
- overlay.html: included from the user's uploaded current overlay.html, preserving the batting/bowling labels and match-result scorecard overlay already present in that file.

Install:
1. Extract this ZIP.
2. Replace index.html and overlay.html in the root of the existing GitHub repository with the files from this ZIP. Keep exact filenames.
3. Commit both files.
4. Wait for GitHub Pages to deploy, then open the site in Chrome Incognito or refresh without cache.
5. Test with a new test match before using live.

Notes:
- JavaScript syntax was checked with Node.js.
- Firebase/PRISM behavior was not end-to-end tested in this environment.
- Existing historical records lacking AppMode may not be classifiable into the right history section automatically.
