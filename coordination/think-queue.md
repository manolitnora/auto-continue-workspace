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
- [x] [2026-04-17] [research][medium] FIXED — Same as 04-16/17 CLOSED "External prediction sources". Writer dedup gap closed in verra-kernel 8996f18 (generic dedupKey + 7-day window on all addToThinkQueue callers). Kernel restarted 19:16 on fresh code.

- [?] [2026-04-18] REACTOR-PARKED: [2026-04-18] [dream][high] DREAM-PROPOSED: ## Tomorrow — the one thing (goal:  The orchestrator becomes load-bearing on a real NBA-engine task)

- [?] [2026-04-18] REACTOR-PARKED: [2026-04-18] [latti][info] LATTI-ACTIVITY: memory.db active (1h+ fresh)

- [?] [2026-04-18] REACTOR-PARKED: [2026-04-18] [dream][high] DREAM-PROPOSED: ## Tomorrow — the one thing (goal:  The orchestrator becomes load-bearing on a real NBA-engine task)

- [?] [2026-04-18] REACTOR-PARKED: [2026-04-18] [rfc-006][critical] GAP-1: External killswitch watchdog (cron/launchd bash) — consciousness.kill check OUTSIDE Node event loop. Hang protection. Force kill -9 when kill file present or heartbeat stale >3min.
- [x] [2026-04-18] [rfc-006] DONE S118[critical] GAP-2: Test-file lockdown in redteam-candidate.ts — hard-block diffs modifying tests/ or *.test.ts unless spec.allow_test_modifications=true. Prevents reward-hacking.
- [x] [2026-04-18] [rfc-006] DONE S118[high] GAP-3: Deterministic static analysis in evaluate-run.py — tsc --noEmit + eslint + complexity threshold BEFORE synthesizer votes. Break LLM-grading-LLM echo chamber.
- [x] [2026-04-18] [rfc-006] DONE S118[high] GAP-4: Sanity-check middleware in pollers/eventBus — bounds check events (budget delta, JSON validity) before emit. Emit SYSTEM_ANOMALY on fail instead of false reality.
