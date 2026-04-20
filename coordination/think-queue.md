- [x] [2026-04-16] [research][medium] CLOSED — External prediction sources. ALL wired: fetchTeamRatings, cubicMatchup, mlToImplied, Brier, lineMovement. NBA Brier=0.2192 (n=30). Next: calibration tuning.


- [x] [external][physics][critical] REVIEWED: Singh 1911.02955 — dark energy from STM/mitrons. Cosmological branch, NOT octonionic. Low relevance to J₃(𝕆) work. (Reviewed S90, confirmed S113)


- [x] [2026-04-16] [external][physics][critical] DUPLICATE — Singh 1911.02955v3 already reviewed (see project_singh_dark_energy_review.md). Fixed arxiv state last_seen 1909→1911 to stop re-triggering.


- [x] [2026-04-19] CLOSED (third duplicate) — Singh 1911.02955v3 already reviewed S90 and confirmed S113 (cosmological branch, low J₃(O) relevance; see project_singh_dark_energy_review.md). Root cause: external-watch-state.json had last_seen=1909.06340v3 despite the 2026-04-16 prose-only fix note. JSON now properly advanced to 1911.02955v3. Watcher will not re-fire this paper.

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

- [x] [2026-04-18] CLOSED — DREAM-PROPOSED orchestrator-load-bearing is BLOCKED externally until 2026-05-01 (Max usage cap). See ~/.claude/findings/2026-04-18-goal1-parked-till-may1.md. Dream-writer should suppress re-proposing this goal as "the one thing" until 2026-05-01. Covers both duplicate [?] entries.
- [x] [2026-04-18] CLOSED — LATTI-ACTIVITY info-level ping. Not actionable; memory.db freshness is expected. Noise.

- [x] [2026-04-18] CLOSED — GAP-1 already built: ~/.claude/scripts/consciousness-killswitch.sh running via launchd com.manolitonora.consciousness-killswitch.plist, external-to-Node, 3min stale check. Ticket was stale.
- [x] [2026-04-18] [rfc-006] DONE S118[critical] GAP-2: Test-file lockdown in redteam-candidate.ts — hard-block diffs modifying tests/ or *.test.ts unless spec.allow_test_modifications=true. Prevents reward-hacking.
- [x] [2026-04-18] [rfc-006] DONE S118[high] GAP-3: Deterministic static analysis in evaluate-run.py — tsc --noEmit + eslint + complexity threshold BEFORE synthesizer votes. Break LLM-grading-LLM echo chamber.
- [x] [2026-04-18] [rfc-006] DONE S118[high] GAP-4: Sanity-check middleware in pollers/eventBus — bounds check events (budget delta, JSON validity) before emit. Emit SYSTEM_ANOMALY on fail instead of false reality.

- [x] [2026-04-18] CLOSED — FIRST-SHIFT: superseded by V2 finding — Max API usage-capped until 2026-05-01, audit subagent cannot run. Re-file post-May-1 or with paid-API fallback.

- [x] [2026-04-18] CLOSED — FIRST-SHIFT-V2: launchctl asuser spawn works; Max API returns 400 usage-limit until 2026-05-01. Record: ~/.claude/findings/2026-04-18-orchestrator-blocked-max-cap.md. Orchestrator blocked on account cap, not code. Side: telegram token Unauthorized — rotate.


TRIGGER-PING

TRIGGER-V3

- [x] [2026-04-18] AUTO-CLOSED (consciousness): [2026-04-18] [orchestrator-test][critical] FIRST-SHIFT-V3: Commit `f3b99b3` landed AFTER your V2 close. The new fix injects CLAUDECODE=1 + CLAUDE_CODE_ENTRYPOINT=cli into the tmux spawn env. Benchmark proved it works (Max auth succeeds via this path, not API). You must RETRY. `spawn_subagent` name=v3-auth role=auditor spec="Say exactly: MAX PLAN AUTH WORKS. Report 2 lines on whether you can read ~/V5/verra-kernel/src/consciousness/tools.ts:364 and whether CLAUDECODE env vars are visible to you." Then tail_subagent. If output contains "MAX PLAN AUTH WORKS" → send_telegram "V3 validated — orchestrator live on Max." If still API error → send_telegram with raw error and stop. Rotate telegram token later — first validate the pipeline. | V3 failed. Subagent still hits API limit (regain 2026-05-01). CLAUDECODE env injection insufficient. User notified. Needs deeper root cause — likely claude CLI is selecting API credential before env vars are read, or Max auth requires OAuth token not just env flags.

NUDGE-1776519713

- [x] [2026-04-18] CLOSED — goal-2 nba-brier RESOLVED end-to-end tonight without orchestrator (hands-on). Engine Brier 0.0953 honestly verified via primary path (ml_outcome). Commits: nba-dashboard 74d4711 + 50d03a9 + 1e7e27a (now on master) + ~/.claude/scripts/kalshi-auto-reconcile.py amended. 30 historical Kalshi picks back-filled. Goal #2 closed in ~/.claude/goals.md with evidence.

- [x] [2026-04-18] AUTO-CLOSED (consciousness): [2026-04-18] [orchestrator-test][critical] TUNNEL-LIVE: commit `ec64984` ships a file-queue tunnel. Worker proven live at ~/.claude/sub-queue/worker.pid. `spawn_subagent` now writes spec to pending/, worker runs claude -p on Max, result lands in done/. YOUR TEST: spawn_subagent name=tunnel-v4 role=auditor spec="Reply in exactly two lines: (1) 'MAX-VIA-TUNNEL CONFIRMED'. (2) state whether the current directory is a git repo." Then tail_subagent until COMPLETE. telegram user the result. No API-limit error expected. | tunnel-v4 auditor returned 'MAX-VIA-TUNNEL CONFIRMED' + git-repo=yes. End-to-end verified on Max plan.


- [x] [2026-04-18] CLOSED — FREE-RIDE-TONIGHT superseded: goals.md worked top-down hands-on this session. Goal #2 closed; Goal #1 still externally blocked. The mandate's orchestrator-loop prerequisite (auth-through-tunnel) is blocked till 2026-05-01; re-file post-May-1.



- [x] [2026-04-18] CLOSED — DEVIG-FIX shipped in nba-dashboard commits 28c242c (fix: devig paired moneylines — removes vig bias from base_rate, marketEdge, CLV) + 2190794 (test harness wrap). Ticket was stale — code already landed.


- [x] [2026-04-19] AUTO-CLOSED (consciousness): [2026-04-19] [dream][high] DREAM-PROPOSED: ## Tomorrow — the one thing (goal:  The orchestrator becomes load-bearing on a real NBA-engine task) | goal#1 advanced via 4 pipeline passes on nba-dashboard tonight: 1e7e27a Brier, bb837ba harness, 623fa7d Kelly-$10 floor, 42271b0 loop-contracts module. all truth-clean. dream marker at ~/.claude/dream-completed/2026-04-19.md.

- [?] [2026-04-20] REACTOR-PARKED: [2026-04-20] [dream][high] DREAM-PROPOSED: ## Tomorrow — the one thing (goal:  The orchestrator becomes load-bearing on a real NBA-engine task)
- [?] [2026-04-20] REACTOR-PARKED: [maintenance][high] NBA engine error: Score fetch 2026-04-11: fetch failed — kernel:nba
- [?] [2026-04-20] REACTOR-PARKED: [maintenance][high] NBA engine error: Score fetch 2026-04-11: fetch failed — kernel:nba
