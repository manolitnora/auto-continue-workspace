- [x] [2026-04-16] [research][medium] CLOSED — External prediction sources. ALL wired: fetchTeamRatings, cubicMatchup, mlToImplied, Brier, lineMovement. NBA Brier=0.2192 (n=30). Next: calibration tuning.


- [x] [external][physics][critical] REVIEWED: Singh 1911.02955 — dark energy from STM/mitrons. Cosmological branch, NOT octonionic. Low relevance to J₃(𝕆) work. (Reviewed S90, confirmed S113)


- [x] [2026-04-16] [external][physics][critical] DUPLICATE — Singh 1911.02955v3 already reviewed (see project_singh_dark_energy_review.md). Fixed arxiv state last_seen 1909→1911 to stop re-triggering.

## WANT GENERATOR — Curiosity-driven questions

- [x] [self][want][high] WANT-GEN: correction/identity tension — deprioritized, not actionable this session
- [x] [maintenance][high] NBA engine score fetch Apr 13 — resolved, all picks scored
- [x] [maintenance][high] NBA engine score fetch Apr 11 — stale, all picks scored, engine healthy
- [x] [2026-04-16] [maintenance][high] STALE — Score fetch 2026-04-11 error. Engine has 42 picks, 34 scored since. Resolved.

- [x] [2026-04-16] [research][medium] CLOSED — Loop IS closing. Degenerate minimum found: sigma/form/injuries pinned at 0.1 lower bound. Engine learning to predict ~0.5. See project_brier_degenerate_minimum.md. Fix: raise sigma floor to 0.3 OR penalize-near-0.5 in cost OR wait for n>=100.
- [x] [2026-04-17] [research][medium] DEDUP — Same as 04-16 CLOSED "External prediction sources". Re-fire from thread_question writer (separate from nba.error writer fixed 04-17). project_queue_dedup_gap.md still open: want/thread_question writer does not check prior resolved [x] before append.
- [x] [2026-04-17] [maintenance][high] STALE — Filed 2026-04-02 (dream: db-not-open + fetch-failed merge). 0 occurrences in current cron.log. Engine healthy: 23W/12L, 4 pending picks, $1196 balance, actively placing/scoring bets. 15 days no recurrence. Resolved downstream.
- [x] [2026-04-17] [maintenance][high] DEDUP — Same as 04-16 STALE. Fixed writer: thinkQueue.ts nba.error now blocks on resolved [x] within 7 days. Source of the leak found and sealed.
- [ ] [research][medium] Research ticket from researcher: "External prediction sources" (priority=medium) — kernel:want (thread_question)
