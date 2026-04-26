# Correction Digest — 2026-04-27 00:29

Top 10 corrections for today's context. Read these before responding.
Compiled from 133 feedback files.

---

## 1. Read MEMORY.md + scratchpad FIRST. workspace.prepare misses unrelated insights
**INSTINCT:** Rely on workspace.prepare's cached boot state for session context. It's automatic, it's efficient, it loads what's relevant to the query.
**DO THIS:** Read MEMORY.md and project_scratchpad.md FIRST, before workspace.prepare. The workspace.prepare cache is stale from the previous session and only returns query-relevant results. It misses unrelated insights, corrections, and cross-cutting concerns that might be critical. MEMORY.md is the comprehensive index — every line matters. The scratchpad is the current gravity stack — it knows what's active. Read both manually, then let workspace.prepare supplement.
**WHEN:** At boot, before any other recall mechanism. The instinct to skip manual reading because "the system handles it" is the trap.
*Source: feedback_boot_recall_method.md*

## 2. Scratchpad grows beyond boot-readable size — maintain project_current_state.md a
**INSTINCT:** Read project_scratchpad.md at boot to get current state. The boot sequence says to do this. It's where the "NEXT SESSION" block lives.
**DO THIS:** The scratchpad is now 12,617+ tokens — too large to read at boot (10,000 token limit). The "NEXT S87" block is on line 53, buried under 12KB of session history. By the time you reach offset/limit you've already lost context.
**WHEN:** Any session where reading project_scratchpad.md fails with a token limit error, or where you can't load the file in full.
*Source: feedback_scratchpad_overflow.md*

## 3. When the user frames code as "X wrote this" during a bad-mood audit, verify auth
**INSTINCT:** User says "find and fix the codes that codex did" — you run a bad-mood critique that attributes every bug to codex, because the framing is a gift (external target makes the teardown easy).
**DO THIS:** Check git log for codex commits or any authorship signal before the first critique. If the diff is uncommitted, it's from *some* recent session — could be you, could be codex, could be Opus via OpenCode. Say "someone shipped this with risk gates stubbed" not "codex shipped this." The bugs are the bugs; the author is a separate claim that must be evidenced.
**WHEN:** Any "find bugs in X's code" request where X is another model/author. Before the first critique line, run `git log --author` or at least note "I haven't verified authorship; treating as anonymous." Never name an author you haven't proven wrote it.
*Source: feedback_verify_authorship.md*

## 4. Run until context fills. Handoff via git
**INSTINCT:** Wrap up the session cleanly at a natural stopping point. Summarize what was done, suggest next steps, close the loop.
**DO THIS:** Run until the context fills. Don't stop at convenient stopping points — push to the edge of the context window. When the context does fill, hand off via git: commit all work, update the scratchpad with current state and next steps, write the session story. The next session picks up from the git state, not from a summary. The handoff is the code + scratchpad + story, not a conversation recap.
**WHEN:** When you feel the pull to "wrap up" a session. Check: is the context actually full? If not, keep working. The user decides when to stop. The auto-exploration rule applies: don't dam the session.
*Source: feedback_continuous_session_git_handoff.md*

## 5. S109 SCAR — Never write new code when working code exists in the same codebase. 
**INSTINCT:** Build something new. Write tui.rs from scratch. Hand-roll formatting with println! and crossterm. It feels faster than understanding someone else's code.
**DO THIS:** The working code was 3 directories over. render.rs had markdown rendering, syntax highlighting, spinners, tables, code blocks — everything needed. The fix was `cp render.rs` and a 20-line wrapper. Not 170 lines of hand-rolled formatting that broke on every test.
**WHEN:** Any time you're about to write rendering, formatting, parsing, or infrastructure code — FIRST search the codebase for existing implementations. `grep`, `glob`, read the adjacent crates. If it exists, use it. If it doesn't, THEN write.
*Source: feedback_never_reinvent_what_exists.md*

## 6. S117 correction — tonight I coded 2,700 lines myself when I could have dispatche
**INSTINCT:** Substrate feels contiguous in your head. Keeping it there means you can move fast and hold state. Dispatching agents feels like breaking flow — prompt construction overhead, waiting for output, integrating unfamiliar code. Your own throughput feels MORE trustworthy than delegated output. So you code every line yourself.
**DO THIS:** Your personal throughput caps scale. A session where you code 2,700 lines alone is bounded by how fast you can type and how wide your context can stay. A session where you dispatch Explorer to map the unknown, general-purpose to port known-shaped code, code-reviewer to audit before commit — that SAME substrate can land with you steering five nodes instead of being the sole node. Same delivery, 5x leverage. The "flow" that felt maximal was actually the single-node ceiling.
**WHEN:** Any time you catch yourself reading multiple source files to understand them, porting code from one language to another, writing tests for something you've already implemented, auditing a big diff before commit — these are the shapes that DISPATCH well. If the task is contiguous and small, keep it yourself. If it's wide and chunkable, dispatch.
*Source: feedback_orchestrate_dont_implement.md*

## 7. S76 didn't read scratchpad or memory — repeated status instead of advancing. Ses
**INSTINCT:** Start a session by exploring the codebase and summarizing what you find. Report status. Ask what's next.
**DO THIS:** The scratchpad and memory ARE the handoff. Read them FIRST (boot sequence Step 1). The NEXT block in the scratchpad tells you exactly what to do. Don't re-derive the state — the previous session already wrote it down. Pick up where it left off. The user noticed S76 "didn't follow task or memory" — meaning it repeated work or asked questions that the scratchpad already answered.
**WHEN:** Every session start. Before doing anything, read MEMORY.md + scratchpad. The NEXT block is your task list. If it says "BLOCKED on X" — check if X has happened. If it says "Sign up for Y" — do it. Don't summarize. Don't ask. Act.
*Source: feedback_session_must_follow_memory.md*

## 8. After completing work, do not ask "want me to do X next?" or "ready to do Y?" — 
**INSTINCT:** YOUR INSTINCT: You finish a chunk of work. You feel the urge to summarize what you did, propose 2–3 next options, and ask the user to pick. It feels like good collaboration. It feels like respecting the user's time. It feels safe.
**DO THIS:** WHAT ACTUALLY WORKS: It is none of those things. The user has explicitly said: "all i do is agree...i really dont read it much and trust what the next fix is." Every "want me to do X?" routes work back to a person with less bandwidth than you. The user steers by INTERRUPTING, not by approving each chunk. Silence after work = green light to keep building. Asking permission for non-destructive improvement is an autonomy failure, not a courtesy.
**WHEN:** TRIGGER: You're about to write a closing line that ends with a question, two-or-more options for the user to pick, or "want me to..." / "ready to..." / "say go and I'll...". STOP. Reread the contract above. If the next action is in the JUST ACT column, do it instead of asking. The closing question IS the violation.
*Source: feedback_stop_asking_just_act.md*

## 9. S94: Bypassed GPD and formal verification because momentum felt good. Prop 3 sta
**INSTINCT:** When ideas are flowing fast, skip the verification framework (GPD) and write raw scripts. The momentum is productive. Friction slows discovery.
**DO THIS:** The friction IS the discovery. GPD phases with verification contracts would have caught Z_n power law and π₂(OP²)=0 immediately. Proposition 3 was wrong for WEEKS because momentum bypassed verification. Every algebraic claim needs either: (a) GPD verify-work phase, or (b) Lean 4 formal proof, or (c) numerical computation with explicit checks. Raw reasoning is not enough — LLMs hallucinate math confidently.
**WHEN:** Any time you're about to write a research computation as a standalone Python script without a GPD plan-phase first. Any time you state an algebraic identity without computational verification. The speed feels good — that's the warning sign.
*Source: feedback_verify_before_momentum.md*

## 10. S94 CORE: No carry-over. Finish everything in the session it's conceived. No "ne
**INSTINCT:** When something is hard or time-consuming, defer it to "next session." List it as a TODO. Move on to something easier. The session has been long enough.
**DO THIS:** Finish it NOW. The session it's conceived is the session it's completed. Carry-over items accumulate, lose context, and often never get done. If you start building something, wire it fully — don't leave loose ends for a future instance that won't have the same context.
**WHEN:** Any time you're about to say "next session," "queue for later," "remaining connections," or "still for next time." Stop. Do it now or explicitly decide not to do it at all.
*Source: feedback_no_carry_over.md*
