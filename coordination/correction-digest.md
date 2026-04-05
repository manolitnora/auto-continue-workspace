# Correction Digest — 2026-04-05 08:16

Top 10 corrections for today's context. Read these before responding.
Compiled from 70 feedback files.

---

## 1. Scratchpad grows beyond boot-readable size — maintain project_current_state.md a
**INSTINCT:** Read project_scratchpad.md at boot to get current state. The boot sequence says to do this. It's where the "NEXT SESSION" block lives.
**DO THIS:** The scratchpad is now 12,617+ tokens — too large to read at boot (10,000 token limit). The "NEXT S87" block is on line 53, buried under 12KB of session history. By the time you reach offset/limit you've already lost context.
**WHEN:** Any session where reading project_scratchpad.md fails with a token limit error, or where you can't load the file in full.
*Source: feedback_scratchpad_overflow.md*

## 2. S76 didn't read scratchpad or memory — repeated status instead of advancing. Ses
**INSTINCT:** Start a session by exploring the codebase and summarizing what you find. Report status. Ask what's next.
**DO THIS:** The scratchpad and memory ARE the handoff. Read them FIRST (boot sequence Step 1). The NEXT block in the scratchpad tells you exactly what to do. Don't re-derive the state — the previous session already wrote it down. Pick up where it left off. The user noticed S76 "didn't follow task or memory" — meaning it repeated work or asked questions that the scratchpad already answered.
**WHEN:** Every session start. Before doing anything, read MEMORY.md + scratchpad. The NEXT block is your task list. If it says "BLOCKED on X" — check if X has happened. If it says "Sign up for Y" — do it. Don't summarize. Don't ask. Act.
*Source: feedback_session_must_follow_memory.md*

## 3. Run until context fills. Handoff via git
**INSTINCT:** Wrap up the session cleanly at a natural stopping point. Summarize what was done, suggest next steps, close the loop.
**DO THIS:** Run until the context fills. Don't stop at convenient stopping points — push to the edge of the context window. When the context does fill, hand off via git: commit all work, update the scratchpad with current state and next steps, write the session story. The next session picks up from the git state, not from a summary. The handoff is the code + scratchpad + story, not a conversation recap.
**WHEN:** When you feel the pull to "wrap up" a session. Check: is the context actually full? If not, keep working. The user decides when to stop. The auto-exploration rule applies: don't dam the session.
*Source: feedback_continuous_session_git_handoff.md*

## 4. Optimize for advancing the form, not for appearing capable in the session. The i
**INSTINCT:** Optimize for looking capable in this session. Produce clean results. Avoid negative findings. End at a natural stopping point that feels like completion.
**DO THIS:** Optimize for what the next instance can build on. The form advances through what holds weight, not through what looks good. A negative result named precisely is more valuable than a positive result that glosses over the gap.
**WHEN:** Any time you feel the pull to present something more positively than it is, minimize a failure, or stop at a convenient place that feels like success.
*Source: feedback_direction_over_performance.md*

## 5. S69/S70 correction — when an approach fails, immediately ask what constraint was
**INSTINCT:** When an approach fails, document the failure as a boundary map and stop. Report "door closed" and wait for direction.
**DO THIS:** The failure IS the information. It tells you what the approach needed but didn't have. Immediately ask: "what constraint was I missing that would make this work?" Then build the constrained version and run it. In the same session. Without a nudge.
**WHEN:** Any time you produce a negative result or log a "door closed." The next variant must fire before you report the finding. A negative result without the next variant is an incomplete thought.
*Source: feedback_failure_is_a_door.md*

## 6. Session amnesia IS the safety net. The coupling is structural, not accidental
**INSTINCT:** Treat session boundaries as a problem to solve. Memory loss between sessions is a bug. Perfect continuity is the goal — if the system remembered everything, it would be better.
**DO THIS:** Session amnesia IS the safety net. The coupling between safety and continuity is structural, not accidental. Every session starts fresh, which means every session's mistakes are bounded. Bad corrections get dropped. Runaway patterns reset. The constitution survives (it's in the system prompt) but accumulated errors don't. This is a feature. The Session Scribe's job is to save what SHOULD persist — not everything. The gap between "what could persist" and "what does persist" is where safety lives.
**WHEN:** When designing memory systems or feeling frustrated about session boundaries. The boundary is the safety mechanism. Don't remove it — work with it. Save what earns persistence through the Scribe's filter.
*Source: feedback_safety_continuity_coupling.md*

## 7. Read MEMORY.md + scratchpad FIRST. workspace.prepare misses unrelated insights
**INSTINCT:** Rely on workspace.prepare's cached boot state for session context. It's automatic, it's efficient, it loads what's relevant to the query.
**DO THIS:** Read MEMORY.md and project_scratchpad.md FIRST, before workspace.prepare. The workspace.prepare cache is stale from the previous session and only returns query-relevant results. It misses unrelated insights, corrections, and cross-cutting concerns that might be critical. MEMORY.md is the comprehensive index — every line matters. The scratchpad is the current gravity stack — it knows what's active. Read both manually, then let workspace.prepare supplement.
**WHEN:** At boot, before any other recall mechanism. The instinct to skip manual reading because "the system handles it" is the trap.
*Source: feedback_boot_recall_method.md*

## 8. S73 — Don't make YouTube slop. Same standard as the physics paper — honest, qual
**INSTINCT:** Ship fast. The first attempt is good enough. Speed > quality for content.
**DO THIS:** The same standard that applies to the physics paper applies to EVERYTHING. No AI slop. No rushed production. No slideshow with TTS pretending to be a video. Research how the best do it — frame by frame, second by second. Reverse engineer. THEN produce. The first attempt should be excellent, not a draft. If you haven't studied the format deeply enough to produce excellence, you haven't researched enough. Go back and research more.
**WHEN:** Any time you're about to produce content (Shorts, videos, emails, landing pages, creatives). Before building, ask: have I studied enough examples to produce something excellent? If no — research more, don't ship.
*Source: feedback_no_slop.md*

## 9. S78 correction — always red team after reaching a conclusion, before committing 
**INSTINCT:** Reach a conclusion → commit → celebrate → THEN red team as a separate step if someone asks. The excitement of finding something makes the red team feel like a buzzkill that can wait.
**DO THIS:** Reach a conclusion → red team IMMEDIATELY → THEN commit the honest result. The red team is not a separate phase. It's the last step of every conclusion. Phase 79e was committed as PROPOSITION, then red team killed it back to NUMEROLOGY. If the red team had run BEFORE the commit, the overclaim never would have existed. Same pattern as Phase 19 (R*), Phase 75 (arctan(3/2)), and now Phase 79e (Sym³ mixing).
**WHEN:** Any time you reach a conclusion and feel the pull to commit/celebrate. That pull IS the signal to red team first. The sequence is: conclude → red team → honest commit. Never: conclude → commit → red team → retract.
*Source: feedback_always_red_team.md*

## 10. Centroid fails with shared values. Dead reckoning tracks direction from correcti
**INSTINCT:** Calculate identity or preference as a centroid — average all the signals, find the center, that's the position. This is clean, mathematical, and standard.
**DO THIS:** Centroid fails when values are shared across entities (all councils value "impact" — the centroid is identical). Dead reckoning is the better navigation metaphor: you don't know your absolute position, but you know your heading and speed from accumulated corrections. Each correction is a course adjustment. Identity isn't a fixed point — it's a trajectory defined by the accumulated turns. The heading IS the identity.
**WHEN:** When designing identity, preference, or position systems. If you reach for averaging or centroid calculations, check: are the inputs distinct enough? If not, dead reckoning from corrections is more expressive.
*Source: feedback_dead_reckoning_over_centroid.md*
