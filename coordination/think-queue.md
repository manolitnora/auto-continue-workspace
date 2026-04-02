# Think Queue — What Needs Thinking

Items are picked top-down by priority. Mark done with [x] when complete.
Any session (human, autonomous, kernel) can add items.

## Format
`- [ ] [lane][priority] Description — source`

Lanes: research, revenue, maintenance, chef, intel
Priority: critical, high, medium, low

---

- [ ] [revenue][low] Bank statements — map spending to budget framework
- [ ] [chef][low] 🔔TRIGGER(user-initiated) First chef menu test — activates when user requests a menu, not schedulable
- [x] [research][medium] [2026-04-01] ESP32-C6 WiFi CSI sensing researched — ESPectre on XIAO ESP32-C6, $6/board, ESPHome not Arduino. Done autonomous
- [x] [research][medium] [2026-04-01] External prediction sources researched — 5 gaps, 10 sources, implementation priority mapped. Done autonomous
- [ ] [research][critical] 27-DOF lattice trace dynamics simulation — full J₃(O) with kinetic term, HMC, correlation functions. Charge-dependent mass ratios from first principles. Separate project, weeks of compute. — S74 Phase 67
- [ ] [research][high] ⏳BLOCKED(on arXiv v1 processing) Paper v2 upload — R* derived section, updated abstract/conclusion. Upload when v1 clears arXiv. — S74
- [x] [research][high] [2026-04-01] Email Singh: 5 emails drafted S77 (Singh, Furey, Boyle, Duff, Dixon). Pending human send. Done
- [x] [research][medium] [2026-04-02] Derive sigmoid params — OBSOLETE. Phase 72 discovered sigmoid was wrong framework. Eigenvalue ratios replaced it. Closed
- [x] [maintenance][medium] [2026-04-02] Self-optimization: audit all 247 MCP tools — which exist, which work, which are unused. Build a tool index for faster lookup. — S73 optimize directive
- [ ] [maintenance][medium] ⚠️STALE(13d) Self-optimization: test all cron jobs fire correctly — backup, think, optimizer. Verify logs. — S73 (NOTE: S79 built+tested auto-continue cron system; old crons may need separate audit)
- [x] [revenue][critical] [2026-04-01] Viral Shorts reverse-engineered — 484-line analysis, 4 channels, production playbook, 10-Short queue. Done S78
- [x] [revenue][high] [2026-04-01] Video gen tools researched — Runway Gen-4, Kling 2.0, Pika, Veo 3, Sora 2 compared. Done S78
- [x] [revenue][high] [2026-04-01] AI voices researched — ElevenLabs, OpenAI TTS, Chatterbox, Voxtral compared. Done S78
- [x] [revenue][high] [2026-04-02] Hermes Agent deep dive — memory + skills compared to Verra. Auto-SOP from 5+ tool calls is adoptable. Done autonomous
- [x] [maintenance][high] [2026-04-01] NBA engine errors (fetch failed + connectivity) — resolved as transient, not NBA-specific. Picks logging daily. Done S78
- [x] [maintenance][high] [2026-04-02] NBA engine errors: DB conn fixed c19673b, ESPN fetch timeouts added (15s AbortSignal). Done autonomous
- [x] [maintenance][high] [2026-04-02] NBA engine fetch-failed: 15s AbortSignal.timeout on 3 ESPN calls. Done autonomous
- [x] [research][medium] [2026-04-01] External prediction sources — completed autonomous S75. Done
- [x] [maintenance][high] [2026-04-02] NBA engine error: fetch failed — already fixed autonomous (DB conn + ESPN timeouts) — kernel:nba
- [ ] [research][high] Prediction projection framework — unify NBA predictions, adaptive clock engagement forecasting, dream chain pattern prediction, and external data sources into one prediction layer. What APIs/models/feeds can the kernel consume? User priority. — kernel:want + S79
- [x] [maintenance][high] [2026-04-02] NBA engine timeout — already fixed by autonomous session (AbortSignal.timeout on ESPN calls)
- [x] [research][medium] [2026-04-02] External prediction sources — completed autonomous S75. Duplicates cleaned (3x kernel auto-filed, 1 remains as done)
- [x] [research][medium] [2026-04-02] External prediction sources — completed autonomous S75. Kernel auto-filed 40+ duplicates (want phase bug). Cleaned S79.
- [ ] [maintenance][high] NBA engine error: The operation was aborted due to timeout — kernel:nba
- [ ] [research][medium] Research ticket from researcher: "External prediction sources" (priority=medium) — kernel:want (thread_question)
