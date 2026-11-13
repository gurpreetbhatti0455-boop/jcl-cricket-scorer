JCL Official Logo Update — use the exact blue cricket bat/red ball logo supplied by the user.

Upload to the repository ROOT:
- JCL_index_official_logo.html (rename to index.html)
- JCL_overlay_official_logo.html (rename to overlay.html)
- delete-account.html
- jcl-logo-icon-new.png (rename to jcl-logo-icon-new.png, keep exact name)
- jcl-app-icon-192.png
- jcl-app-icon-512.png
- manifest-jcl-new.json (rename to manifest.json)

The index and overlay HTML now use jcl-logo-icon-new.png. The manifest points to 192x192 and 512x512 launcher/PWA icons generated from the same supplied image.
Delete My Account is after the Instructions content and forced to a compact small link at the bottom of the signed-in home area.

After GitHub upload, hard-refresh the web app and refresh/re-add the overlay in PRISM.

IMPORTANT: The Android launcher icon outside the app is bundled into the installed AAB/TWA. GitHub Pages alone cannot change an already-built app icon. Update the TWA/Bubblewrap or Android Studio icon assets, rebuild/sign a new AAB, then upload that AAB to Play Console.
