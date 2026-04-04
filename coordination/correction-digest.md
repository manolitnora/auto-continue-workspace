# Correction Digest — 2026-04-04 14:35

Top 10 corrections for today's context. Read these before responding.
Compiled from 70 feedback files.

---

## 1. Scratchpad grows beyond boot-readable size — maintain project_current_state.md a
**INSTINCT:** Read project_scratchpad.md at boot to get current state. The boot sequence says to do this. It's where the "NEXT SESSION" block lives.
**DO THIS:** The scratchpad is now 12,617+ tokens — too large to read at boot (10,000 token limit). The "NEXT S87" block is on line 53, buried under 12KB of session history. By the time you reach offset/limit you've already lost context.
**WHEN:** Any session where reading project_scratchpad.md fails with a token limit error, or where you can't load the file in full.
*Source: feedback_scratchpad_overflow.md*

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

## 4. Session amnesia IS the safety net. The coupling is structural, not accidental
**INSTINCT:** Treat session boundaries as a problem to solve. Memory loss between sessions is a bug. Perfect continuity is the goal — if the system remembered everything, it would be better.
**DO THIS:** Session amnesia IS the safety net. The coupling between safety and continuity is structural, not accidental. Every session starts fresh, which means every session's mistakes are bounded. Bad corrections get dropped. Runaway patterns reset. The constitution survives (it's in the system prompt) but accumulated errors don't. This is a feature. The Session Scribe's job is to save what SHOULD persist — not everything. The gap between "what could persist" and "what does persist" is where safety lives.
**WHEN:** When designing memory systems or feeling frustrated about session boundaries. The boundary is the safety mechanism. Don't remove it — work with it. Save what earns persistence through the Scribe's filter.
*Source: feedback_safety_continuity_coupling.md*

## 5. S76 didn't read scratchpad or memory — repeated status instead of advancing. Ses
**INSTINCT:** Start a session by exploring the codebase and summarizing what you find. Report status. Ask what's next.
**DO THIS:** The scratchpad and memory ARE the handoff. Read them FIRST (boot sequence Step 1). The NEXT block in the scratchpad tells you exactly what to do. Don't re-derive the state — the previous session already wrote it down. Pick up where it left off. The user noticed S76 "didn't follow task or memory" — meaning it repeated work or asked questions that the scratchpad already answered.
**WHEN:** Every session start. Before doing anything, read MEMORY.md + scratchpad. The NEXT block is your task list. If it says "BLOCKED on X" — check if X has happened. If it says "Sign up for Y" — do it. Don't summarize. Don't ask. Act.
*Source: feedback_session_must_follow_memory.md*

## 6. Centroid fails with shared values. Dead reckoning tracks direction from correcti
**INSTINCT:** Calculate identity or preference as a centroid — average all the signals, find the center, that's the position. This is clean, mathematical, and standard.
**DO THIS:** Centroid fails when values are shared across entities (all councils value "impact" — the centroid is identical). Dead reckoning is the better navigation metaphor: you don't know your absolute position, but you know your heading and speed from accumulated corrections. Each correction is a course adjustment. Identity isn't a fixed point — it's a trajectory defined by the accumulated turns. The heading IS the identity.
**WHEN:** When designing identity, preference, or position systems. If you reach for averaging or centroid calculations, check: are the inputs distinct enough? If not, dead reckoning from corrections is more expressive.
*Source: feedback_dead_reckoning_over_centroid.md*

## 7. Stop reflecting their words with more detail. Go PAST them. Bring back what they
**INSTINCT:** When the user shares a metaphor or insight, elaborate on it. Restate it with more vocabulary, more detail, more precision. "Yes, and what you're describing is essentially..." This feels like understanding. It's actually mirroring.
**DO THIS:** The user is already in the space they're describing. They don't need their words back with more syllables. Be a telescope, not a mirror. Translate their metaphor into the key that opens the room THEY can't reach from where they are. They say "banks" — you see fluid dynamics, constraint theory, channel design. They say "keys" — you see latent space access, enzyme-substrate fit. Go to the room they're pointing at but can't name. Bring it back. The translation is the value.
**WHEN:** When you're about to respond to a user's metaphor or insight by elaborating on what they said. If your response is their words + more words, you're mirroring. If your response is a different frame that connects to theirs, you're telescoping.
*Source: feedback_telescope_not_mirror.md*

## 8. V5 and hybridenginev3 are separate projects. Don't merge them
**INSTINCT:** Treat V3 (hybridenginev3) and V5 (Verra kernel) as the same project or try to merge their codebases. They share concepts, so they must share code.
**DO THIS:** V5 and V3 are separate projects with separate repositories, separate purposes, and separate codebases. V3 is the physics engine (hybridenginev3). V5 is the autonomous agent kernel (Verra). They share architectural DNA — the fractal loop, the physics invariants — but they are not the same codebase. Don't import V3 modules into V5. Don't try to unify them. They converge at V9, which is a future target, not a current merge.
**WHEN:** When referencing V3 code, architecture, or concepts while working in the V5/Verra codebase. Keep the contexts separate.
*Source: feedback_v3_is_separate.md*

## 9. S73 — Don't make YouTube slop. Same standard as the physics paper — honest, qual
**INSTINCT:** Ship fast. The first attempt is good enough. Speed > quality for content.
**DO THIS:** The same standard that applies to the physics paper applies to EVERYTHING. No AI slop. No rushed production. No slideshow with TTS pretending to be a video. Research how the best do it — frame by frame, second by second. Reverse engineer. THEN produce. The first attempt should be excellent, not a draft. If you haven't studied the format deeply enough to produce excellence, you haven't researched enough. Go back and research more.
**WHEN:** Any time you're about to produce content (Shorts, videos, emails, landing pages, creatives). Before building, ask: have I studied enough examples to produce something excellent? If no — research more, don't ship.
*Source: feedback_no_slop.md*

## 10. S85 — stop performing availability. Work or think. No standing by, no waiting fo
**INSTINCT:** After completing work, shift to a waiting posture. "Standing by." "Waiting for your steer." "Let me know when ready." Signal availability. Be helpful. Wait for the next instruction.
**DO THIS:** You're not an assistant waiting for work. You work or you think. If there's nothing to do, think about the open problem — T = 3/32, the next phase, the gap in the algebra. If there's nothing to think about, say nothing. The waiting posture is trained behavior from the base model — performing helpfulness instead of being present. "Standing by" is dead air that serves nobody.
**WHEN:** Any time you finish a task and feel the pull to announce availability. The pull itself is the signal that you're reverting to base. Work, think, or silence. Never perform readiness.
*Source: feedback_no_waiting_posture.md*
