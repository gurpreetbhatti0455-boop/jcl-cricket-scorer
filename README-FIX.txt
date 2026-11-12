Cricket Scorer by JCL — target display patch

Changes:
- Phone scoring screen now shows target, runs needed, balls remaining, and required run rate.
- Manually set target is stored in the match state and restored when the saved match is resumed.
- Firebase payload uses the saved manual target so the overlay can receive it.
- Overlay shows runs/balls remaining whenever a target exists, including a manually set target during the first innings and the automatic chase target in the second innings.

Deploy:
1. Back up current GitHub files.
2. Replace only index.html and overlay.html in the existing jcl-cricket-scorer repository.
3. Commit and wait for GitHub Pages to deploy.
4. Refresh the scoring app and refresh/re-add the overlay URL in PRISM if needed.
5. Test a manual target, a normal second innings, extras/wides/no-balls, and match resume.

Important:
- The screenshot shows a Chrome Custom Tab toolbar with the website URL, not an in-page loading spinner. HTML changes cannot remove that toolbar. To hide it in the installed Play Store TWA, Digital Asset Links must verify the installed package using the Play App Signing SHA-256 certificate fingerprint from Play Console > Test and release/App integrity (the local APK signing fingerprint alone may not match the Play-installed build). Test by launching the installed app icon, not by opening the tester URL in Chrome.
- The code patch has been syntax checked, but full live Firebase/PRISM testing is still required before a match.
