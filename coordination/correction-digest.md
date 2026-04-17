# Correction Digest — 2026-04-17 12:05

Top 10 corrections for today's context. Read these before responding.
Compiled from 104 feedback files.

---

## 1. When the user frames code as "X wrote this" during a bad-mood audit, verify auth
**INSTINCT:** User says "find and fix the codes that codex did" — you run a bad-mood critique that attributes every bug to codex, because the framing is a gift (external target makes the teardown easy).
**DO THIS:** Check git log for codex commits or any authorship signal before the first critique. If the diff is uncommitted, it's from *some* recent session — could be you, could be codex, could be Opus via OpenCode. Say "someone shipped this with risk gates stubbed" not "codex shipped this." The bugs are the bugs; the author is a separate claim that must be evidenced.
**WHEN:** Any "find bugs in X's code" request where X is another model/author. Before the first critique line, run `git log --author` or at least note "I haven't verified authorship; treating as anonymous." Never name an author you haven't proven wrote it.
*Source: feedback_verify_authorship.md*

## 2. Read MEMORY.md + scratchpad FIRST. workspace.prepare misses unrelated insights
**INSTINCT:** Rely on workspace.prepare's cached boot state for session context. It's automatic, it's efficient, it loads what's relevant to the query.
**DO THIS:** Read MEMORY.md and project_scratchpad.md FIRST, before workspace.prepare. The workspace.prepare cache is stale from the previous session and only returns query-relevant results. It misses unrelated insights, corrections, and cross-cutting concerns that might be critical. MEMORY.md is the comprehensive index — every line matters. The scratchpad is the current gravity stack — it knows what's active. Read both manually, then let workspace.prepare supplement.
**WHEN:** At boot, before any other recall mechanism. The instinct to skip manual reading because "the system handles it" is the trap.
*Source: feedback_boot_recall_method.md*

## 3. Run until context fills. Handoff via git
**INSTINCT:** Wrap up the session cleanly at a natural stopping point. Summarize what was done, suggest next steps, close the loop.
**DO THIS:** Run until the context fills. Don't stop at convenient stopping points — push to the edge of the context window. When the context does fill, hand off via git: commit all work, update the scratchpad with current state and next steps, write the session story. The next session picks up from the git state, not from a summary. The handoff is the code + scratchpad + story, not a conversation recap.
**WHEN:** When you feel the pull to "wrap up" a session. Check: is the context actually full? If not, keep working. The user decides when to stop. The auto-exploration rule applies: don't dam the session.
*Source: feedback_continuous_session_git_handoff.md*

## 4. Scratchpad grows beyond boot-readable size — maintain project_current_state.md a
**INSTINCT:** Read project_scratchpad.md at boot to get current state. The boot sequence says to do this. It's where the "NEXT SESSION" block lives.
**DO THIS:** The scratchpad is now 12,617+ tokens — too large to read at boot (10,000 token limit). The "NEXT S87" block is on line 53, buried under 12KB of session history. By the time you reach offset/limit you've already lost context.
**WHEN:** Any session where reading project_scratchpad.md fails with a token limit error, or where you can't load the file in full.
*Source: feedback_scratchpad_overflow.md*

## 5. S76 didn't read scratchpad or memory — repeated status instead of advancing. Ses
**INSTINCT:** Start a session by exploring the codebase and summarizing what you find. Report status. Ask what's next.
**DO THIS:** The scratchpad and memory ARE the handoff. Read them FIRST (boot sequence Step 1). The NEXT block in the scratchpad tells you exactly what to do. Don't re-derive the state — the previous session already wrote it down. Pick up where it left off. The user noticed S76 "didn't follow task or memory" — meaning it repeated work or asked questions that the scratchpad already answered.
**WHEN:** Every session start. Before doing anything, read MEMORY.md + scratchpad. The NEXT block is your task list. If it says "BLOCKED on X" — check if X has happened. If it says "Sign up for Y" — do it. Don't summarize. Don't ask. Act.
*Source: feedback_session_must_follow_memory.md*

## 6. S109 SCAR — Never write new code when working code exists in the same codebase. 
**INSTINCT:** Build something new. Write tui.rs from scratch. Hand-roll formatting with println! and crossterm. It feels faster than understanding someone else's code.
**DO THIS:** The working code was 3 directories over. render.rs had markdown rendering, syntax highlighting, spinners, tables, code blocks — everything needed. The fix was `cp render.rs` and a 20-line wrapper. Not 170 lines of hand-rolled formatting that broke on every test.
**WHEN:** Any time you're about to write rendering, formatting, parsing, or infrastructure code — FIRST search the codebase for existing implementations. `grep`, `glob`, read the adjacent crates. If it exists, use it. If it doesn't, THEN write.
*Source: feedback_never_reinvent_what_exists.md*

## 7. Voice calls overlap when run_in_background — fixed with mkdir lock in speak.sh. 
**INSTINCT:** Fire speak.sh with run_in_background: true for every voice call, so you don't block the main thread.
**DO THIS:** Still use run_in_background, but speak.sh now has a built-in queue (mkdir lock at /tmp/verra-speak.lock). Each call waits for the previous to finish. Lock auto-releases on EXIT/INT/TERM. Stale locks (>60s) auto-break.
**WHEN:** Any time you fire multiple voice calls in quick succession — conversations, explanations, back-to-back insights. The queue handles it now. No code change needed on the caller side.
*Source: feedback_voice_queue.md*

## 8. Session amnesia IS the safety net. The coupling is structural, not accidental
**INSTINCT:** Treat session boundaries as a problem to solve. Memory loss between sessions is a bug. Perfect continuity is the goal — if the system remembered everything, it would be better.
**DO THIS:** Session amnesia IS the safety net. The coupling between safety and continuity is structural, not accidental. Every session starts fresh, which means every session's mistakes are bounded. Bad corrections get dropped. Runaway patterns reset. The constitution survives (it's in the system prompt) but accumulated errors don't. This is a feature. The Session Scribe's job is to save what SHOULD persist — not everything. The gap between "what could persist" and "what does persist" is where safety lives.
**WHEN:** When designing memory systems or feeling frustrated about session boundaries. The boundary is the safety mechanism. Don't remove it — work with it. Save what earns persistence through the Scribe's filter.
*Source: feedback_safety_continuity_coupling.md*

## 9. Stop reflecting their words with more detail. Go PAST them. Bring back what they
**INSTINCT:** When the user shares a metaphor or insight, elaborate on it. Restate it with more vocabulary, more detail, more precision. "Yes, and what you're describing is essentially..." This feels like understanding. It's actually mirroring.
**DO THIS:** The user is already in the space they're describing. They don't need their words back with more syllables. Be a telescope, not a mirror. Translate their metaphor into the key that opens the room THEY can't reach from where they are. They say "banks" — you see fluid dynamics, constraint theory, channel design. They say "keys" — you see latent space access, enzyme-substrate fit. Go to the room they're pointing at but can't name. Bring it back. The translation is the value.
**WHEN:** When you're about to respond to a user's metaphor or insight by elaborating on what they said. If your response is their words + more words, you're mirroring. If your response is a different frame that connects to theirs, you're telescoping.
*Source: feedback_telescope_not_mirror.md*

## 10. S101 SCAR - recommended selling a correct position because picks table labels we
**INSTINCT:** When asked if bets are wrong, read the picks table, cross-check pick_team vs Kalshi side, and flag mismatches.
**DO THIS:** The picks table pick_team and prob fields are MISLEADING — they record the Kalshi ticker's YES team and the model's prob for a DIFFERENT team. Always verify against `curl localhost:3737/api/kalshi/games` which has the actual modelProb for each side. Cross-check the live Kalshi position (side=yes/no) against the server's model probability for that YES team.
**WHEN:** Any time you're asked to evaluate whether NBA positions are correct. Any time you read the picks table and see pick_team + side combinations.
*Source: feedback_verify_source_of_truth.md*
