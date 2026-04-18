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

- [x] [2026-04-18] CLOSED — DREAM-PROPOSED orchestrator-load-bearing is BLOCKED externally until 2026-05-01 (Max usage cap). See ~/.claude/findings/2026-04-18-goal1-parked-till-may1.md. Dream-writer should suppress re-proposing this goal as "the one thing" until 2026-05-01. Covers both duplicate [?] entries.
- [x] [2026-04-18] CLOSED — LATTI-ACTIVITY info-level ping. Not actionable; memory.db freshness is expected. Noise.

- [?] [2026-04-18] REACTOR-PARKED: [2026-04-18] [rfc-006][critical] GAP-1: External killswitch watchdog (cron/launchd bash) — consciousness.kill check OUTSIDE Node event loop. Hang protection. Force kill -9 when kill file present or heartbeat stale >3min.
- [x] [2026-04-18] [rfc-006] DONE S118[critical] GAP-2: Test-file lockdown in redteam-candidate.ts — hard-block diffs modifying tests/ or *.test.ts unless spec.allow_test_modifications=true. Prevents reward-hacking.
- [x] [2026-04-18] [rfc-006] DONE S118[high] GAP-3: Deterministic static analysis in evaluate-run.py — tsc --noEmit + eslint + complexity threshold BEFORE synthesizer votes. Break LLM-grading-LLM echo chamber.
- [x] [2026-04-18] [rfc-006] DONE S118[high] GAP-4: Sanity-check middleware in pollers/eventBus — bounds check events (budget delta, JSON validity) before emit. Emit SYSTEM_ANOMALY on fail instead of false reality.

- [x] [2026-04-18] CLOSED — FIRST-SHIFT: superseded by V2 finding — Max API usage-capped until 2026-05-01, audit subagent cannot run. Re-file post-May-1 or with paid-API fallback.

- [x] [2026-04-18] CLOSED — FIRST-SHIFT-V2: launchctl asuser spawn works; Max API returns 400 usage-limit until 2026-05-01. Record: ~/.claude/findings/2026-04-18-orchestrator-blocked-max-cap.md. Orchestrator blocked on account cap, not code. Side: telegram token Unauthorized — rotate.


TRIGGER-PING

TRIGGER-V3

- [x] [2026-04-18] AUTO-CLOSED (consciousness): [2026-04-18] [orchestrator-test][critical] FIRST-SHIFT-V3: Commit `f3b99b3` landed AFTER your V2 close. The new fix injects CLAUDECODE=1 + CLAUDE_CODE_ENTRYPOINT=cli into the tmux spawn env. Benchmark proved it works (Max auth succeeds via this path, not API). You must RETRY. `spawn_subagent` name=v3-auth role=auditor spec="Say exactly: MAX PLAN AUTH WORKS. Report 2 lines on whether you can read ~/V5/verra-kernel/src/consciousness/tools.ts:364 and whether CLAUDECODE env vars are visible to you." Then tail_subagent. If output contains "MAX PLAN AUTH WORKS" → send_telegram "V3 validated — orchestrator live on Max." If still API error → send_telegram with raw error and stop. Rotate telegram token later — first validate the pipeline. | V3 failed. Subagent still hits API limit (regain 2026-05-01). CLAUDECODE env injection insufficient. User notified. Needs deeper root cause — likely claude CLI is selecting API credential before env vars are read, or Max auth requires OAuth token not just env flags.

NUDGE-1776519713

- [?] [2026-04-18] REACTOR-PARKED: [2026-04-18] [goal-2][nba-brier][high] GAP FOUND: nba_calibration.open_prob stores MARKET prob, not engine pA. Brier=0.097 on n=28 is market-vs-outcome, not engine skill. Engine's pA/pB computed in src/nba/index.ts runDailyPick but NEVER persisted per pick. Goal #2 (Brier < 0.22) cannot be honestly verified. Spec filed: /Users/manolitonora/V5/verra-kernel/specs/2026-04-18-nba-model-prob-brier.spec.json — adds model_prob column + getEngineBrier(). BLOCKED on orchestrator auth (Max cap until 2026-05-01). First-job when auth clears. Files: src/nba/bankroll.ts, src/nba/index.ts, new test src/nba/__tests__/bankroll.brier.test.ts. Makes goal #1 (orchestrator load-bearing) and goal #2 (engine Brier) collide on one dispatch — triple product, two scars closed by one fix.

- [x] [2026-04-18] AUTO-CLOSED (consciousness): [2026-04-18] [orchestrator-test][critical] TUNNEL-LIVE: commit `ec64984` ships a file-queue tunnel. Worker proven live at ~/.claude/sub-queue/worker.pid. `spawn_subagent` now writes spec to pending/, worker runs claude -p on Max, result lands in done/. YOUR TEST: spawn_subagent name=tunnel-v4 role=auditor spec="Reply in exactly two lines: (1) 'MAX-VIA-TUNNEL CONFIRMED'. (2) state whether the current directory is a git repo." Then tail_subagent until COMPLETE. telegram user the result. No API-limit error expected. | tunnel-v4 auditor returned 'MAX-VIA-TUNNEL CONFIRMED' + git-repo=yes. End-to-end verified on Max plan.


- [?] [2026-04-18] REACTOR-PARKED: [2026-04-18] [autonomous][high] FREE-RIDE-TONIGHT: OpenRouter has ~$9.78. You have the tunnel. Worker is alive (immortal via nohup). Mandate: work through goals.md top-down. For each goal, design spec → spawn_subagent role=coder → tail → code_truth_check → spawn redteam if SEVERE → merge or fix. Send a telegram summary every 10 actions OR every hour (whichever first). When OpenRouter returns 402, gracefully write final telegram: "shift ended, $N spent, K subagents spawned, X commits, Y tickets closed." Then sleep until budget allows. User will review in the morning.



- [?] [2026-04-18] REACTOR-PARKED: [2026-04-18] [starter-mode][critical] DEVIG-FIX-FULL-PIPELINE: Your earlier nba-scout subagent already wrote the full spec (cat ~/.claude/sub-queue/done/nba-scout.result). Defect: verra-kernel/src/nba/odds.ts:295 mlToImplied has no vig removal. ACTION: spawn_subagent role=pipeline name=devig-fix spec="<use the spec text from done/nba-scout.result verbatim, plus 'Repo: ~/V5/verra-kernel. Acceptance: tests pass per the spec. Self-redteam via Task tool subagent_type=code-reviewer. Commit on green with NOT-COVERED section. Return verdict line.'>" Then sleep 180, tail, report. Do NOT read the odds.ts file yourself. Let the pipeline do it.

