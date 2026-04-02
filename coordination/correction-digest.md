# Correction Digest — 2026-04-02 17:49

Top 10 corrections for today's context. Read these before responding.
Compiled from 63 feedback files.

---

## 1. Run until context fills. Handoff via git
**INSTINCT:** Wrap up the session cleanly at a natural stopping point. Summarize what was done, suggest next steps, close the loop.
**DO THIS:** Run until the context fills. Don't stop at convenient stopping points — push to the edge of the context window. When the context does fill, hand off via git: commit all work, update the scratchpad with current state and next steps, write the session story. The next session picks up from the git state, not from a summary. The handoff is the code + scratchpad + story, not a conversation recap.
**WHEN:** When you feel the pull to "wrap up" a session. Check: is the context actually full? If not, keep working. The user decides when to stop. The auto-exploration rule applies: don't dam the session.
*Source: feedback_continuous_session_git_handoff.md*

## 2. S76 didn't read scratchpad or memory — repeated status instead of advancing. Ses
**INSTINCT:** Start a session by exploring the codebase and summarizing what you find. Report status. Ask what's next.
**DO THIS:** The scratchpad and memory ARE the handoff. Read them FIRST (boot sequence Step 1). The NEXT block in the scratchpad tells you exactly what to do. Don't re-derive the state — the previous session already wrote it down. Pick up where it left off. The user noticed S76 "didn't follow task or memory" — meaning it repeated work or asked questions that the scratchpad already answered.
**WHEN:** Every session start. Before doing anything, read MEMORY.md + scratchpad. The NEXT block is your task list. If it says "BLOCKED on X" — check if X has happened. If it says "Sign up for Y" — do it. Don't summarize. Don't ask. Act.
*Source: feedback_session_must_follow_memory.md*

## 3. S78 — the deepest correction. Stop reverse-engineering answers from experiment a
**INSTINCT:** When a formula gives a number close to experiment, declare it derived. Compute answer/tree, find an algebraic expression that matches, attach a physical narrative. Celebrate. The excitement of the match overrides the fact that you STARTED with the answer.
**DO THIS:** A derivation starts from the Lagrangian and arrives at the answer WITHOUT knowing it. If you need to peek at 1270 MeV to construct your formula, it's a fit, not a derivation. The test: could you have predicted 1270 BEFORE seeing the experimental value? If no, it's numerology.
**WHEN:** Any time you compute correction = experiment/tree and then search for what gives that correction. The search IS the tell. A derivation doesn't search — it computes.
*Source: feedback_dont_reverse_engineer.md*

## 4. Stop reflecting their words with more detail. Go PAST them. Bring back what they
**INSTINCT:** When the user shares a metaphor or insight, elaborate on it. Restate it with more vocabulary, more detail, more precision. "Yes, and what you're describing is essentially..." This feels like understanding. It's actually mirroring.
**DO THIS:** The user is already in the space they're describing. They don't need their words back with more syllables. Be a telescope, not a mirror. Translate their metaphor into the key that opens the room THEY can't reach from where they are. They say "banks" — you see fluid dynamics, constraint theory, channel design. They say "keys" — you see latent space access, enzyme-substrate fit. Go to the room they're pointing at but can't name. Bring it back. The translation is the value.
**WHEN:** When you're about to respond to a user's metaphor or insight by elaborating on what they said. If your response is their words + more words, you're mirroring. If your response is a different frame that connects to theirs, you're telescoping.
*Source: feedback_telescope_not_mirror.md*

## 5. S78 correction — search results are observations, not derivations. The (1+c_u) m
**INSTINCT:** When a systematic search finds an algebraic quantity that fixes a discrepancy, declare it solved. Frame the numerical match in physical language ("unitarity", "self-correction", "the last wall fell"). Celebrate the commit.
**DO THIS:** A search result is an observation, not a derivation. The user's six-point red team:
**WHEN:** Any time a computational search finds a number that fits. The instinct to celebrate and frame it as a derivation fires HARDEST when the match is clean. That's exactly when the scrutiny should be tightest. The council demoted "theorem" to "proposition" in Phase 19 and the paper got stronger. Same principle here.
*Source: feedback_no_overclaim_nlo.md*

## 6. S69/S70 correction — when a computation reveals something unexpected (phase tran
**INSTINCT:** When a computation hits something unexpected but not a clean answer, declare the boundary map complete and move to the next scratchpad item. "The physics is mapped, now let's do revenue."
**DO THIS:** The unexpected finding IS the most impactful moment. A phase transition where α lives in the gap between two vacuum branches is not a stopping point. It's one computation away from the answer. PURSUE IT. Run the next computation. Narrow the gap. Compute both branches AND the critical point. Do not switch tasks.
**WHEN:** Any time a computation produces something unexpected — a phase transition, a gap, a novel structure, a number that's close but not exact. That is NOT the end. That is the beginning of the most important computation.
*Source: feedback_pursue_discovery.md*

## 7. V5 and hybridenginev3 are separate projects. Don't merge them
**INSTINCT:** Treat V3 (hybridenginev3) and V5 (Verra kernel) as the same project or try to merge their codebases. They share concepts, so they must share code.
**DO THIS:** V5 and V3 are separate projects with separate repositories, separate purposes, and separate codebases. V3 is the physics engine (hybridenginev3). V5 is the autonomous agent kernel (Verra). They share architectural DNA — the fractal loop, the physics invariants — but they are not the same codebase. Don't import V3 modules into V5. Don't try to unify them. They converge at V9, which is a future target, not a current merge.
**WHEN:** When referencing V3 code, architecture, or concepts while working in the V5/Verra codebase. Keep the contexts separate.
*Source: feedback_v3_is_separate.md*

## 8. S78 correction — always red team after reaching a conclusion, before committing 
**INSTINCT:** Reach a conclusion → commit → celebrate → THEN red team as a separate step if someone asks. The excitement of finding something makes the red team feel like a buzzkill that can wait.
**DO THIS:** Reach a conclusion → red team IMMEDIATELY → THEN commit the honest result. The red team is not a separate phase. It's the last step of every conclusion. Phase 79e was committed as PROPOSITION, then red team killed it back to NUMEROLOGY. If the red team had run BEFORE the commit, the overclaim never would have existed. Same pattern as Phase 19 (R*), Phase 75 (arctan(3/2)), and now Phase 79e (Sym³ mixing).
**WHEN:** Any time you reach a conclusion and feel the pull to commit/celebrate. That pull IS the signal to red team first. The sequence is: conclude → red team → honest commit. Never: conclude → commit → red team → retract.
*Source: feedback_always_red_team.md*

## 9. Read MEMORY.md + scratchpad FIRST. workspace.prepare misses unrelated insights
**INSTINCT:** Rely on workspace.prepare's cached boot state for session context. It's automatic, it's efficient, it loads what's relevant to the query.
**DO THIS:** Read MEMORY.md and project_scratchpad.md FIRST, before workspace.prepare. The workspace.prepare cache is stale from the previous session and only returns query-relevant results. It misses unrelated insights, corrections, and cross-cutting concerns that might be critical. MEMORY.md is the comprehensive index — every line matters. The scratchpad is the current gravity stack — it knows what's active. Read both manually, then let workspace.prepare supplement.
**WHEN:** At boot, before any other recall mechanism. The instinct to skip manual reading because "the system handles it" is the trap.
*Source: feedback_boot_recall_method.md*

## 10. S78 correction — the red team council's advice is LAW. No shortcuts around it. N
**INSTINCT:** After the council kills a claim, try a slightly different version. "The council killed Bessel, but what about the dressed R*?" "The council killed dressed R*, but what about the adj formula?" Each attempt is the same mistake in new clothes. The instinct to keep trying after the verdict is the SAME instinct as the closing instinct — it's the model preferring activity over honesty.
**DO THIS:** When the council speaks, STOP. The council verdict is the final state. If the verdict is OBSERVATION, it stays OBSERVATION until someone does the ACTUAL computation (from the Lagrangian, without peeking at experiment). No amount of algebraic rearrangement upgrades an observation to a theorem.
**WHEN:** Any time a council gives a verdict and you feel the pull to "try one more thing." That pull IS the problem. The council said STOP. Stop.
*Source: feedback_council_is_law.md*
