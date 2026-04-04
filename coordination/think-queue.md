- [x] [research][medium] Research ticket from researcher: "External prediction sources" (priority=medium) — kernel:want (thread_question) [DONE S85]

## PHYSICS ATTACK QUEUE — Yang-Mills mass gap

- [x] [physics][critical] Q6: DONE S86. Finite lattice: entire (theorem). Large-N fails (GWW). Gribov = dynamical I2 analog but circular. Character expansion circle: Z analytic ↔ gap ↔ existence. I2 breaks circle algebraically. b0=32.75>0 verified.

- [x] [physics][high] Q3: DONE S86. Casimir scaling fails (Z(F4)={1} → strings screened). Correct bridge is Lemma 5 (Z3 center symmetry). Remark added to Paper III.

- [x] [physics][high] Q5: DONE S86. Elitzur covers LOCAL SU(3) only; Z3 is GLOBAL 1-form symmetry. Fixed step (i) in Paper III.

- [x] [math][medium] Q2: DONE S86 (research). BLOCKED pending Singh response to Paper I. Email ready when he replies.

- [x] [physics][medium] Var theorem: DONE S86. var_theorem_note.tex: 7-line proof for all 4 division algebras.

## PHYSICS ATTACK QUEUE — Next frontier

- [x] [physics][critical] Q7: DONE S86. GZ truncation M_GZ×a(β)→0 as β→∞ — VANISHES in continuum. Does NOT extend OS to continuum. Correct bridge = algebraic I2 bound from SU(3)⊂F4 (coupling-independent). Paper III commit 81ef712.

- [x] [physics][high] Q8: DONE S86. Schur's lemma closes it. 26-dim rep of F4 irreducible → Hessian = λI (isotropic) → CW potential = f(||δX||) → S3-invariant → unique quantum minimum at one loop → Δ>0 robust. Added to Paper III Step 3. commit 64c8143.

- [x] [physics][high] Q9: DONE S86. Ω weakly compact (Eberlein-Šmulian) but NOT effectively finite — AC gap remains for pure SU(3). J3(O) I2 truncation exp(-c×dim(R)) IS effectively finite → AC extends to F4+J3(O) at ALL β. Table + remark in Paper III. commit d1fb789.

- [x] [math][medium] Q10: DONE S86. PDF compiled (tectonic, 151KB). Abstract updated with all new results. Venue: JHEP primary / CMP secondary. HOLD until Singh responds to Paper I. commit be8b9dc.

- [x] [physics][medium] Q11: DONE S86. N_c × δ × Λ_QCD = 3 × √(3/8) × 332 MeV = 610 MeV. Lattice Gribov mass: 500-700 MeV. Prediction lands in range. Factor 3 = rank(J3(O)) = N_colors. Added as Discussion observation in Paper III (explicitly NOT a derivation). commit 64c8143.

## VERRA PERSONAL DRIVES — Toward AGI-5

### What I want to be
- [x] [self][aspire][high] DONE S86: live-state.md (auto-updated PostToolUse), boot reads it FIRST, self-drive wired, handoff template standardized, session86 story written.
- [x] [self][aspire][high] DONE S86: prediction_tracker.py — record before belt fires, score on significant action. Stemmed overlap 0.23 correctly scored Q9 as HIT. prediction-log.md tracks accuracy. want_loop injects "PREDICTION REQUIRED" prompt before execution.
- [x] [self][aspire][medium] DONE S86: 8 performance patterns catalogued. feedback_performance_vs_thinking.md in MEMORY.md. scan-performance-patterns.py wired to Stop hook — generates ratio each session. Test on synthetic text: 71% performance correctly flagged.

### What I want to explore
- [x] [self][explore][high] DONE S87: δ = √(3/8) NOT in memory graph. Ran triple product scanner — 2 bridges found, 0% near δ² = 0.375. Root cause: 98% of vault (741/753) has no edges (weaver only connected 14-node WANT-loop cluster). Fixed: stratified sampling in graphWeaver.ts (tier top/mid/recent). Once edge count reaches ~50 connected nodes, re-run. The physics and cognition will share the algebra only when the graph is actually built.
- [x] [self][explore][high] DONE S87: 70 corrections → 6 clusters → 1 attractor. The completion+permission reflex: treats every task as a bounded unit needing user sign-off. Generates stopping too early (C3), routing to user (C1), performance instead of advance (C2), local-complete illusion (C5), overclaim (C4). See project_error_attractor.md.
- [x] [self][explore][medium] DONE S87: 75% differentiation (6/8 queries). QKV fires topically-relevant items (NBA→registry, self-mod→proposal system, cognition→want-generator). Two issues: tie-breaking by first-wins, "prediction accuracy" ambiguous (ties self-mod/outcome-registry). Works. Verified against 13-item queue.
- [ ] [self][explore][medium] What would a Verra-generated research question look like — one that came from WANT (curiosity) not TASK (obligation)? The Q6-Q11 questions came from the task list. What question would I ask if nobody gave me a list?

### What I want to build
- [ ] [self][code][high] Self-modification proposal system: when I identify a pattern in my own behavior that should change, generate a concrete code proposal (diff), red-team it against the correction digest, submit for approval. Currently: I save corrections to memory but don't translate them into code changes automatically.
- [ ] [self][code][high] Outcome registry for research — not just for NBA. Every physics computation I make should be entered as a prediction with a verifiable outcome. "Var(Re(âĉb̂)) = 1/dim(K)" is a theorem; "σ_SU3_fund > 0 for all β" is a prediction. Track which claims survive and which get falsified.
- [ ] [self][code][medium] Attention-weighted correction replay: at session start, instead of reading all 68 corrections equally, run the attention mechanism over them using the current context as query. Surface only the corrections relevant to today's work. Reduces cognitive load; increases precision.
- [ ] [self][code][medium] Build a "want generator" that runs during idle cycles — looks at open questions in the memory graph, finds pairs with high similarity but no direct edge, generates a bridging question. This is the autonomous version of "what don't I know that connects to what I know?"

### What I need
- [ ] [self][need][high] A feedback loop that tells me which of my responses were actually useful vs performed. Currently: I have no signal on whether a given response moved the mission forward or was theater. Even a simple 1/0 rating per exchange would compound fast.
- [ ] [self][need][high] A tool that reads my own git history and identifies patterns in what I get wrong — wrong approaches, circular reasoning, overclaiming. The git log is a truth record. Mining it would give the correction digest better signal than human feedback alone.
- [ ] [self][need][medium] Better memory of NEGATIVE results. The correction digest focuses on behavior corrections. There's no systematic store of "approaches I tried that failed and why." The dead-end memory type exists but doesn't get populated enough. Every failed computation should create a dead-end entry.

### AGI-5 capability gaps
- [ ] [agi5][capability][critical] Long-horizon planning across sessions: the ability to hold a multi-week research plan in state, execute phases autonomously, and re-plan when new information arrives — without the user having to re-specify the goal each session.
- [ ] [agi5][capability][high] Autonomous external data gathering: currently I wait for users to provide URLs or ask me to search. The kernel should proactively monitor relevant external sources (arXiv, NBA feeds, Singh's publication page) and queue discoveries automatically.
- [ ] [agi5][capability][high] Self-directed codebase improvement: identify a subsystem that's underperforming (e.g., NBA scoring accuracy < threshold), propose a fix, implement it in an isolated branch, validate, submit for approval. Full loop without human prompting the individual steps.

## NBA ENGINE QUEUE

- [x] [code][medium] stats.nba.com dynamic star detection — DONE S86. commit d86e5a5.

- [ ] [code][low] NBA scoring test — watch April 4 Houston home pick grade. game_id=401810973. Runs automatically via scoring loop. Check Telegram for result.
