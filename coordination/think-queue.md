- [x] [research][medium] Research ticket from researcher: "External prediction sources" (priority=medium) — kernel:want (thread_question) [DONE S85]

## PHYSICS ATTACK QUEUE — Yang-Mills mass gap

- [x] [physics][critical] Q6: DONE S86. Finite lattice: entire (theorem). Large-N fails (GWW). Gribov = dynamical I2 analog but circular. Character expansion circle: Z analytic ↔ gap ↔ existence. I2 breaks circle algebraically. b0=32.75>0 verified. Paper III commits a7ccbe4, 6d12afe, 05d26de.

- [x] [physics][high] Q3: DONE S86. Casimir scaling fails because Z(F4)={1} → all F4 strings screened → σ_F4_∞ may vanish → bound trivial. Correct bridge is Lemma 5 (Z3 center symmetry, not Casimir). Added Remark on Casimir insufficiency to Paper III. N-ality protection makes σ_SU3_fund non-zero independently of σ_F4.

- [x] [physics][high] Q5: DONE S86. Elitzur covers LOCAL SU(3), not GLOBAL Z3 (1-form symmetry). Fixed step (i) in Paper III chain — now clearly states Z3 is a global symmetry that CAN order, broken at high T, unbroken at T=0 by anomaly matching + lattice evidence. This is the honest remaining gap.

- [ ] [math][medium] Q2: Does Singh's trace dynamics FORCE M = M_P/δ or is it a choice? Send email to Singh (draft at research/alpha-137/paper/email_singh_paper2.txt). Also: check Singh's original papers for whether he derives M from equations of motion or assumes it.

- [x] [physics][medium] Var(Re(âĉb̂)) = 1/dim(K) theorem: DONE S86. var_theorem_note.tex written. 7-line proof: left-mult isometry + spherical symmetry. Parenthesization-independence via alternative law + Re(associator)=0. Springer-Veldkamp §1.7.1 cited. 4 algebras MC-verified. commit 4244f7c.

## NBA ENGINE QUEUE

- [x] [code][medium] stats.nba.com direct (TypeScript) — DONE S86. statsNba.ts: Advanced stats, diacritic normalization, 4-tier impact, 24h cache, hardcoded fallback. Wired into enricher.ts. commit d86e5a5.
