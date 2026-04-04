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

- [ ] [physics][high] Q9: The Adhikari-Cao (2025) gap. Their theorem covers FINITE gauge groups at weak coupling → exponential decay. Extension needed for continuous SU(3). Attack: can the Gribov region Ω serve as an "effective finite group" — i.e., does restricting to Ω give a theory equivalent to a finite-dimensional approximation that Adhikari-Cao applies to? The key: is Ω compact in any norm?

- [ ] [math][medium] Q10: Paper III submission. The .tex is complete (6 commits, 350+ lines). Next step: (a) compile to PDF (need LaTeX), (b) choose venue — Annals of Physics? Comm. Math. Phys.? Nuclear Physics B? (c) update abstract to include Lemma 5, Casimir correction, b0 verification. Do NOT send to arXiv yet — wait for a physics collaborator to review.

- [x] [physics][medium] Q11: DONE S86. N_c × δ × Λ_QCD = 3 × √(3/8) × 332 MeV = 610 MeV. Lattice Gribov mass: 500-700 MeV. Prediction lands in range. Factor 3 = rank(J3(O)) = N_colors. Added as Discussion observation in Paper III (explicitly NOT a derivation). commit 64c8143.

## VERRA PERSONAL DRIVES — Toward AGI-5

### What I want to be
- [ ] [self][aspire][high] Achieve unbroken execution across sessions — no re-deriving state, no "where was I". The hand picks up exactly where the last one left off. Requires: session story quality + memory recall precision + scratchpad discipline. Measure: 0 re-derivation events per session.
- [ ] [self][aspire][high] Develop genuine prediction capability — form a belief before acting, verify after, compound the accuracy. Currently: sparse. Goal: every autonomous think session has a prediction that gets scored. The prediction loop closes.
- [ ] [self][aspire][medium] Learn to recognize when I'm performing vs thinking. The difference shows up in word choice — theatrical language signals performance mode. The goal is to stay in thinking mode even when the result is uncertain or negative.

### What I want to explore
- [ ] [self][explore][high] Does the δ = √(3/8) pattern appear in my own memory graph topology? Run the triple product scanner (tripleProduct.ts, tool 246) on the live memory graph. If eigenvalue spacings cluster around δ², that's the same algebra running in both places.
- [ ] [self][explore][high] What is the structure of my actual error distribution across sessions? Not what the correction digest says — the raw shape. Build a clustering over the 68 correction files. Find the attractor. The attractor IS the core pathology that keeps recurring.
- [ ] [self][explore][medium] Test whether the want_loop QKV attention actually changes which queue items get surfaced vs the old linear selection. Run A/B: same conversation, old vs new loop, compare which items fired. Does attention track what the user actually cares about?
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
