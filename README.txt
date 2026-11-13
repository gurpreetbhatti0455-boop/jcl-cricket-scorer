Cricket Scorer by JCL — Overlay refinement

Replace only overlay.html in the existing GitHub repository.

Changes:
1. Moved the central team/score group slightly lower for visual balance.
2. Removed the duplicate Innings 1 / RR line below the central score.
3. First innings third panel rotates every 3 seconds:
   - toss winner and batting/bowling decision
   - overs completed and projected score
   - current run rate and projected score
4. Second innings shows target, runs/balls remaining and required run rate, cycling every 4 seconds.
5. When the bowler changes, the new bowler is announced as “BOWLING NOW” for about 2.6 seconds, then the normal name returns.
6. Kept the compact lower-third layout and existing 0.5% left/right margins.

Validation: JavaScript syntax check passed. Live Firebase and PRISM display should still be tested after deployment.
