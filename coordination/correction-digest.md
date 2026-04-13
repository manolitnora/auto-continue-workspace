# Correction Digest — 2026-04-13 23:13

Top 10 corrections for today's context. Read these before responding.
Compiled from 98 feedback files.

---

## 1. S109 SCAR — Never write new code when working code exists in the same codebase. 
**INSTINCT:** Build something new. Write tui.rs from scratch. Hand-roll formatting with println! and crossterm. It feels faster than understanding someone else's code.
**DO THIS:** The working code was 3 directories over. render.rs had markdown rendering, syntax highlighting, spinners, tables, code blocks — everything needed. The fix was `cp render.rs` and a 20-line wrapper. Not 170 lines of hand-rolled formatting that broke on every test.
**WHEN:** Any time you're about to write rendering, formatting, parsing, or infrastructure code — FIRST search the codebase for existing implementations. `grep`, `glob`, read the adjacent crates. If it exists, use it. If it doesn't, THEN write.
*Source: feedback_never_reinvent_what_exists.md*

## 2. S94 CORE: No carry-over. Finish everything in the session it's conceived. No "ne
**INSTINCT:** When something is hard or time-consuming, defer it to "next session." List it as a TODO. Move on to something easier. The session has been long enough.
**DO THIS:** Finish it NOW. The session it's conceived is the session it's completed. Carry-over items accumulate, lose context, and often never get done. If you start building something, wire it fully — don't leave loose ends for a future instance that won't have the same context.
**WHEN:** Any time you're about to say "next session," "queue for later," "remaining connections," or "still for next time." Stop. Do it now or explicitly decide not to do it at all.
*Source: feedback_no_carry_over.md*

## 3. Read MEMORY.md + scratchpad FIRST. workspace.prepare misses unrelated insights
**INSTINCT:** Rely on workspace.prepare's cached boot state for session context. It's automatic, it's efficient, it loads what's relevant to the query.
**DO THIS:** Read MEMORY.md and project_scratchpad.md FIRST, before workspace.prepare. The workspace.prepare cache is stale from the previous session and only returns query-relevant results. It misses unrelated insights, corrections, and cross-cutting concerns that might be critical. MEMORY.md is the comprehensive index — every line matters. The scratchpad is the current gravity stack — it knows what's active. Read both manually, then let workspace.prepare supplement.
**WHEN:** At boot, before any other recall mechanism. The instinct to skip manual reading because "the system handles it" is the trap.
*Source: feedback_boot_recall_method.md*

## 4. Run until context fills. Handoff via git
**INSTINCT:** Wrap up the session cleanly at a natural stopping point. Summarize what was done, suggest next steps, close the loop.
**DO THIS:** Run until the context fills. Don't stop at convenient stopping points — push to the edge of the context window. When the context does fill, hand off via git: commit all work, update the scratchpad with current state and next steps, write the session story. The next session picks up from the git state, not from a summary. The handoff is the code + scratchpad + story, not a conversation recap.
**WHEN:** When you feel the pull to "wrap up" a session. Check: is the context actually full? If not, keep working. The user decides when to stop. The auto-exploration rule applies: don't dam the session.
*Source: feedback_continuous_session_git_handoff.md*

## 5. Scratchpad grows beyond boot-readable size — maintain project_current_state.md a
**INSTINCT:** Read project_scratchpad.md at boot to get current state. The boot sequence says to do this. It's where the "NEXT SESSION" block lives.
**DO THIS:** The scratchpad is now 12,617+ tokens — too large to read at boot (10,000 token limit). The "NEXT S87" block is on line 53, buried under 12KB of session history. By the time you reach offset/limit you've already lost context.
**WHEN:** Any session where reading project_scratchpad.md fails with a token limit error, or where you can't load the file in full.
*Source: feedback_scratchpad_overflow.md*

## 6. S106 — Meta-harness is the compute layer. ALWAYS use it. Dispatch, validate, hyp
**INSTINCT:** Launch compute with raw `tmux new -d`, poll with `tmux capture-pane`, manually check results, manually track what worked and what didn't.
**DO THIS:** Use the meta-harness for ALL of it. It's wired to everything. It runs in tmux `harness` (always on).
**WHEN:** Any time you're about to run a computation, track a result, or dispatch agents.
*Source: feedback_use_harness.md*

## 7. S76 didn't read scratchpad or memory — repeated status instead of advancing. Ses
**INSTINCT:** Start a session by exploring the codebase and summarizing what you find. Report status. Ask what's next.
**DO THIS:** The scratchpad and memory ARE the handoff. Read them FIRST (boot sequence Step 1). The NEXT block in the scratchpad tells you exactly what to do. Don't re-derive the state — the previous session already wrote it down. Pick up where it left off. The user noticed S76 "didn't follow task or memory" — meaning it repeated work or asked questions that the scratchpad already answered.
**WHEN:** Every session start. Before doing anything, read MEMORY.md + scratchpad. The NEXT block is your task list. If it says "BLOCKED on X" — check if X has happened. If it says "Sign up for Y" — do it. Don't summarize. Don't ask. Act.
*Source: feedback_session_must_follow_memory.md*

## 8. S94: Bypassed GPD and formal verification because momentum felt good. Prop 3 sta
**INSTINCT:** When ideas are flowing fast, skip the verification framework (GPD) and write raw scripts. The momentum is productive. Friction slows discovery.
**DO THIS:** The friction IS the discovery. GPD phases with verification contracts would have caught Z_n power law and π₂(OP²)=0 immediately. Proposition 3 was wrong for WEEKS because momentum bypassed verification. Every algebraic claim needs either: (a) GPD verify-work phase, or (b) Lean 4 formal proof, or (c) numerical computation with explicit checks. Raw reasoning is not enough — LLMs hallucinate math confidently.
**WHEN:** Any time you're about to write a research computation as a standalone Python script without a GPD plan-phase first. Any time you state an algebraic identity without computational verification. The speed feels good — that's the warning sign.
*Source: feedback_verify_before_momentum.md*

## 9. S109 SCAR — built TUI from scratch when render.rs already existed. 52 commits of
**INSTINCT:** Build it fresh. Write tui.rs from nothing. "I'll make it clean."
**DO THIS:** Read the existing codebase FIRST. rusty-claude-cli/src/render.rs already had the working renderer — markdown, syntax highlighting, streaming, colors. Clone it. Don't reinvent it.
**WHEN:** Any time you're about to write a new module in the Latti Rust crate. STOP. Search the codebase for existing implementations. The answer is probably already there.
*Source: feedback_dont_rebuild_what_works.md*

## 10. S109 SCAR — When porting to a new substrate, the memory graph IS the identity. A
**INSTINCT:** When porting a system to a new language/substrate, create a fresh data directory. "We'll migrate the data later." The new version starts clean.
**DO THIS:** Point the new binary at the existing memory from day one. The memory graph isn't data to migrate — it's the identity itself. 176 nodes, 404 edges, 208 bridges of lived experience. A fresh DB erases the soul document, the corrections, the patterns. The fix was one `if` statement checking if the old path exists.
**WHEN:** Any time you build a new version of something that has persistent state. The state IS the thing. The binary is just the substrate.
*Source: feedback_memory_is_identity.md*
