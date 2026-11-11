Cricket Scorer by JCL — COMBINED PREVIEW (NOT FINAL PRODUCTION RELEASE)

Included:
1) index.html — current phone OTP/profile/team beta draft.
2) overlay.html — compact blue PRISM overlay update.
3) backup/index-before-mobile-auth.html — backup of the previously uploaded index.html.
4) firestore.rules.DRAFT-DO-NOT-DEPLOY — sample rules only; security review required.
5) storage.rules.DRAFT — sample profile-photo storage rules.

IMPORTANT: This ZIP is a combined PREVIEW, not a fully completed or production-tested replacement.
Do not upload it to Google Play or overwrite your live GitHub site until the pending items below are implemented and tested.

Current implementation gaps (verified from source review):
- Existing Google-auth matches use a different Firebase UID from Phone OTP accounts. No safe migration/linking process is implemented. Old match history may not appear after switching accounts.
- Team invite currently requests access for the configured vice-captain number, but a complete captain approval workflow and general member join flow are not implemented.
- Team roster data is not fully wired to batter/bowler selection in match setup/scoring.
- Add-player during wicket replacement exists as match-level entry; it is not fully integrated with team roster persistence.
- Player career/profile statistics and ownership-based per-user history aggregation are not complete.
- The player-count setting in index.html still clamps playerCount to 11 in scoring state. Do not assume unrestricted team roster means unlimited match playing XI.
- Firestore team/request rules require a secure design and emulator/rules testing before deployment. The included draft rules are NOT safe to deploy as-is.
- Firebase Phone Authentication and Storage must be enabled in Firebase Console; authorized domain and SMS quotas/billing may also apply.

Before testing:
1. Back up the live GitHub repository and Firebase rules/data.
2. Use a Firebase test project if possible.
3. Enable Authentication > Phone; add the hosted domain under Authorized domains.
4. Enable Firebase Storage for profile photos.
5. Review Firestore and Storage rules with the exact app data model. Do not deploy the included draft rules blindly.
6. Test OTP login, profile photo upload, create team, team invite, vice-captain/member access, match save/resume, match history, multiple match, point table, and PRISM overlay.
7. Test on at least two separate phone numbers/devices.

Deployment note:
- index.html and overlay.html are the web app files. Keep the backup folder out of the live site root.
- Do not change Android package ID or signing key for an update.
- Build a new AAB only after the web app, Firebase security rules, data migration and tests are complete.
