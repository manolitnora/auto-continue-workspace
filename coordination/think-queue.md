# Think Queue — What Needs Thinking

Items are picked top-down by priority. Mark done with [x] when complete.
Any session (human, autonomous, kernel) can add items.

## Format
`- [ ] [lane][priority] Description — source`

Lanes: research, revenue, maintenance, chef, intel
Priority: critical, high, medium, low

---

- [x] [research][high] [2026-03-30] Convergence zone researched — data points collapse (concrete+paint = sphere packing). Real question: RCP void ≈ 1/e. Open since 1960s — done S74
- [x] [revenue][high] [2026-03-30] Second YouTube Short: short_alpha_137.mp4 (55s, 967KB) — done S74
- [x] [revenue][medium] [2026-03-30] arXiv submission uploaded — tar.gz with TeX source. Awaiting processing + Singh endorsement — done S74
- [x] [research][medium] [2026-03-31] FlavorGraph: do cuisine pairing clusters match geographic proximity? — done autonomous S75
- [x] [maintenance][medium] [2026-03-30] NBA engine verified — pick-20260330-401810953 in database — done S74
- [ ] [revenue][low] Bank statements — map spending to budget framework
- [x] [research][low] [2026-03-30] Information theory partition — answered by convergence zone research: no universal 1/3. Explore-exploit is problem-dependent. 1/e appears in optimal stopping but not as universal partition — done S74
- [ ] [chef][low] 🔔TRIGGER(user-initiated) First chef menu test — activates when user requests a menu, not schedulable
- [x] [revenue][critical] [2026-03-30] Revenue intelligence compiled — affiliates > Shorts RPM by 100x. GetResponse 40-60%, agent revenue 95% hype — done S74
- [x] [revenue][high] [2026-03-30] Affiliate programs researched — GetResponse, Writesonic, Frase, Semrush mapped — done S74
- [x] [revenue][critical] [2026-03-30] Competitive intelligence done — no autonomous AI agent makes real money independently. Cursor $500M, Claude $1B = SaaS not agents — done S74
- [x] [revenue][high] [2026-03-31] Research: AI agent frameworks — Devin, Manus, OpenClaw, Hermes, AutoGPT, Claude Code compared. No agent makes money FOR users. Verra gap = revenue-through-agent — done autonomous
- [x] [maintenance][high] [2026-03-30] Accountability system rewired — daily Telegram at 19:30, DOW variety, tested working — done S74
- [x] [research][high] [2026-03-30] Multi-model council researched — 8B local = dispatcher not strategist. No Slack (SQLite rows). Ollama HTTP from kernel. Pull hermes3:8b + qwen2.5-coder:7b — done S74
- [x] [research][medium] [2026-04-01] ESP32-C6 WiFi CSI sensing researched — ESPectre on XIAO ESP32-C6, $6/board, ESPHome not Arduino. Done autonomous
- [x] [maintenance][critical] [2026-03-30] Build correction digest system: autonomous session compiles top 10 most relevant corrections into a daily digest file. Boot sequence reads digest instead of skimming index. Floor loads before ceiling. — S73
- [x] [maintenance][high] [2026-03-30] Tripwire upgraded — two-tier HARD+SOFT detection, tested working — done S74
- [x] [maintenance][high] [2026-03-30] Boot priority verified — correction digest already loads FIRST in Step 1. No change needed — done S74
- [x] [research][medium] [2026-04-01] External prediction sources researched — 5 gaps, 10 sources, implementation priority mapped. Done autonomous
- [ ] [research][critical] 27-DOF lattice trace dynamics simulation — full J₃(O) with kinetic term, HMC, correlation functions. Charge-dependent mass ratios from first principles. Separate project, weeks of compute. — S74 Phase 67
- [ ] [research][high] ⏳BLOCKED(on arXiv v1 processing) Paper v2 upload — R* derived section, updated abstract/conclusion. Upload when v1 clears arXiv. — S74
- [x] [research][high] [2026-03-31] Companion paper written S75, revised S76-S77. 20 pages, red-teamed. Done
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
- [ ] [research][medium] Research ticket from researcher: "External prediction sources" (priority=medium) — kernel:want (thread_question)
