Cricket Scorer by JCL — Account deletion button + logo fix
Build: 13 November 2026

UPLOAD THESE FILES TO THE ROOT OF THE SAME GITHUB REPOSITORY:
- JCL_index_fixed.html (rename to index.html before uploading)
- JCL_overlay_fixed.html (rename to overlay.html before uploading)
- delete-account.html
- jcl-logo-icon.png
- jcl-logo.png (legacy wide logo; not used by the updated screens)

CHANGES
1. Delete My Account moved to the very bottom of the signed-in home screen, after Instructions.
2. Delete button is compact rather than a large full-width red button.
3. Home screen, scorer header, and PRISM overlay use the same square cricket icon.
4. Logo image paths use ./jcl-logo-icon.png. The PNG must be in the repository root beside the HTML files.

DEPLOY
1. Back up current repository files.
2. Rename JCL_index_fixed.html to index.html and JCL_overlay_fixed.html to overlay.html.
3. Replace index.html and overlay.html; add/replace delete-account.html and jcl-logo-icon.png.
4. Commit changes and wait for GitHub Pages deployment.
5. Hard-refresh the app and refresh/re-add the PRISM overlay source.

If the PNG is not uploaded to GitHub root, the browser will continue to show a broken-image icon.
Firebase account deletion and actual PRISM rendering still require live testing.
