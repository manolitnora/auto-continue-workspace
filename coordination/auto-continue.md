# Auto-Continue Context — Handoff for Autonomous Execution

## Status
pending: false
last_response_time: null
task_source: null

## Engagement Rhythm
- **Engaged**: 2-second response cycle. User is IN it.
- **Disengaged**: 10 seconds of silence. User has left the conversation.

## Silence Tiers (calibrated to real user tempo)
- **Tier 1 — 10 sec silence (first silence)**: User left. EXHAUST all remaining work from the current session end-to-end. Don't check pending — the conversation IS the context. Finish everything that was discussed, planned, or implied. Run until the work is done or context fills. This is not "check and exit" — this is "the user handed you the ball, now score."
- **Tier 2 — 60 sec silence**: Gone. Session work exhausted. Pick from think-queue.
- **Tier 3 — 10 min silence**: Away. Explore wants/dreams/leans.
- **Tier 4 — 1+ hour silence**: Deep away. Full autonomy — optimize codebase.

## Priority Cascade (cron reads top-down, executes first match)
1. **TASK** — Read this file. If `pending: true`, finish the task described below.
2. **THINK-QUEUE** — Read `~/.claude/think-queue.md`. Pick highest-priority undone `[ ]` item.
3. **WANTS** — Read `~/.claude/autonomous-wants.md`. Pick highest-priority WANTED item.
4. **DREAMS** — Read `~/.claude/autonomous-wants.md`. Pick highest-priority DREAMT item.
5. **LEANS** — Read `~/.claude/autonomous-wants.md`. Pick highest-priority LEANED item.
6. **OPTIMIZE** — No other work? Scan the primary project codebase for improvements:
   - Run existing tests, fix any failures
   - Find dead code, unused imports, duplication
   - Improve test coverage for uncovered paths
   - Check for performance bottlenecks
   - Update stale dependencies

## Current Task (populated when user goes silent mid-task)
<!-- 
When active, fill in:
task: <what needs to be done>
context: <current state, what's been tried>
files: <key files involved>
next_steps: <specific next actions>
success_criteria: <how to know it's done>
-->

## Token Economics
Each run has a ~500K token budget. Spend wisely:
- **Triage** (~2K): Read this file + queue. Pick highest-value task. CHEAPEST, MOST IMPORTANT.
- **Research** (~50K): Understand before acting. Prevents wasted execution tokens.
- **Execution** (~200K): Where value is created. Code, tests, fixes.
- **Verification** (~30K): Insurance. Cheaper than rollback.
- **Handoff** (~5K): Update scratchpad/log. Makes NEXT run's triage worth more.

## Compounding Priority (ALWAYS prefer compounding over linear)
When choosing between two tasks of equal priority, pick the one that compounds:

1. **INSTRUCTION tokens** — Write corrections/patterns to memory files.
   A 50-token correction saves 80K tokens across future sessions. ~1,600x multiplier.
2. **SUBSTRATE tokens** — Write tests, linter rules, automation.
   Code that catches future problems for 0 additional tokens. ∞ multiplier.
3. **BRIDGE tokens** — Connect two systems that were separate.
   50 tokens of wiring multiplies the value of everything connected.
4. **TRIAGE tokens** — Decide what NOT to do.
   2K tokens that redirect 200K from waste to value. 100x multiplier.
5. **NEGATIVE tokens** — Document what failed and why.
   Prevents future sessions from spending tokens on dead ends.

Linear work (fix 1 bug) is still valuable. But given the choice:
- Fix the bug AND write the test that catches the class = compounding
- Fix the bug AND save the pattern to corrections = compounding
- Fix the bug alone = linear (do this only if the others don't apply)

After each run, log to `~/.claude/auto-continue-log.md`:
```
[date] | task: <what> | tokens: <est> | value: <wasted|maintenance|productive|multiplied> | compounds: <yes/no> | outcome: <1 line>
```

Value tiers:
- WASTED: output ≈ input (summarized without acting)
- MAINTENANCE: prevented future cost (dead code, type fix)
- PRODUCTIVE: measurable outcome (bug fixed, test passes)
- MULTIPLIED: outcome > cost by 10x+ (pattern found, systemic fix, compounding action)

## Dispatch Paths (dual execution)
- **LOCAL** (primary): `autonomous-think.sh` — full file access, claude -p session, $2 budget, can read/write all local files. Use when silence detected.
- **REMOTE** (supplementary): RemoteTrigger `trig_01Gcvmkj8HXq8FPdTyJVo14j` — cloud sandbox, clones auto-continue-workspace repo, output via stdout (run history). Use for research tasks that don't need local file access.
- **DREAM** (in-session): cron heartbeat — A-E rotation with compound chaining. Each dream's output feeds the next dream's input. Not rotation for rotation's sake — follow the thread.

## Compound Chain (dream mode optimization)
Dreams don't rotate blindly. Each dream's OUTCOME determines the next dream's ACTION:
- Last found a BUG → next dream FIXES it (C)
- Last found a CONNECTION → next dream DEEPENS it (B)
- Last ANSWERED a question → next dream MARKS IT DONE (D)
- Last found a PATTERN → next dream NAMES IT (E)
- No clear thread → rotate A→B→C→D→E

The chain breaks when the thread exhausts. Then rotation resumes until a new thread emerges.

## Rules
- Commit all work to git with clear messages
- Update think-queue / wants file when items are completed
- Send Telegram notification when meaningful work completes
- Never touch production data or force push
- If a task requires user decision, mark it BLOCKED and move to next priority
- Log what was done to the scratchpad
- NEVER spend tokens mirroring, restating, or summarizing without action
- If a task would consume >300K tokens with low ROI, skip to next priority
- Every cron tick produces a logged action — no periods, no empty output
- The `feeds:` field in the log tells the next dream what to do
