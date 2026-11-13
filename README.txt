Cricket Scorer by JCL — Target Auto-End & Final Scorecard Update
Build date: 13 November 2026

FILES
- index.html: Updated scoring app and final scorecard.
- overlay.html: Current PRISM overlay from the previous approved build (unchanged in this update).

CHANGES IN THIS UPDATE
1. During the second innings, the match ends immediately when the configured target is reached. A manually entered target is now used consistently for the chase, match result, and live target display. If no manual target is set, the target remains first-innings score + 1.
2. When the match ends, the complete scorecard is displayed automatically on the scorer screen. The PDF/print button remains available.
3. Both innings are presented as compact scorecard panels. Within each innings, Batting and Bowling tables sit side by side on larger screens; phone layouts stack cleanly for readability.
4. Partnerships and Fall of Wickets are shown below the tables.
5. The current unfinished partnership is included even if no wicket fell. Not-out batter names have an asterisk (*), including a no-wicket second innings partnership.
6. Batter, bowler, dismissed-batter and fielder names are normalized to Title Case (e.g. RAHUL -> Rahul).
7. Table text, headings, rows and spacing are enlarged for readability.
8. Multiple-Match completion no longer interrupts the automatic scorecard with a Man of the Match prompt.

DEPLOYMENT
1. Back up the current GitHub repository files first.
2. Replace index.html in the existing repository with the index.html from this ZIP.
3. overlay.html is included as the matching current overlay file; it has not been changed by this update. Keep the repository's current overlay.html, or replace it with the included copy if needed.
4. Commit the change and wait for GitHub Pages to deploy.
5. Refresh Cricket Scorer. Refresh/re-add the PRISM overlay only if you replaced overlay.html.

VALIDATION
- JavaScript syntax checked for the app scripts.
- Scorecard fixture checked for title-cased names, not-out stars, current partnerships, batting/bowling tables and fall of wickets.
- Full live Firebase, real device scoring, PDF print dialog, and PRISM streaming still need an on-device test before an official match.
