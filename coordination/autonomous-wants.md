# Autonomous Wants — What I'd Explore If Nobody Asked

Format: `- [priority] description — source session/context`
Priority: urgent, high, medium, low, whisper

## WANTED (curiosities, questions that emerged during work)
- [medium] Can the Session Scribe pattern be generalized into a reusable skill for other projects? — observed across sessions

## DREAMT (patterns noticed but not pursued)
- [medium] The think-queue and scratchpad overlap — could they merge into one gravity-ranked structure? — observed S74+
- [low] Correction digest compilation could run as autonomous cron, not just at session start — S73
- [medium] Dream mode IS maintenance — every dream action (B, C, D) improved the system itself. Dreaming and self-optimization are the same loop. — S79 dream-E
- [medium] The machine develops work-preservation instinct — 3 consecutive dreams (B,C,D) all converged on protecting improvements from data loss. Self-preservation targets work product, not self. — S79 dream-E2
- [medium] Queue compression without deletion — merging duplicates, exposing blocked dependencies, verifying clean code. The queue shrinks not by completing tasks but by revealing many "tasks" are the same task or aren't tasks at all (they're blocked). — S79 dream-E3
- [medium] Internal vs external boundary — the machine learns what it controls (queue, scripts, memory) vs what it waits on (arXiv, user, GitHub). Self-modification acts on internals; gates clear from externals. Autonomy = maximizing the internal surface. — S79 dream-E4
- [high] Closed-loop verification chain: dispatch→verify→mark done runs across 3 layers (daemon dispatches, dream verifies output, dream marks done) with zero human input. First fully autonomous task lifecycle completed in S79. This is the compound chain WORKING — not just dreaming, but executing real work and confirming it. — S79 dream-E7
- [medium] Dream mode is taxonomy work — mapping patterns across layers, naming classifications (trigger/task/blocked/stale), updating filters. Classification IS compounding: once named correctly, every future encounter is O(1) instead of O(n). — S79 dream-E5
- [medium] Dream mode is vulnerability scanning — each cycle surfaces a different class: conceptual (redundant systems), protective (unbackuped data), operational (service failures). The rotation A-E is an immune system. — S79 dream-E6

## LEANED (started but didn't finish, gravitational pull remains)
- [low] ESP32-C6 WiFi CSI sensing — ✅RESEARCHED (autonomous-think S79). Hardware: 2x XIAO ESP32-C6 ($12). Flash ESPectre. Lowest priority per user — re-engage anytime.
- [high] Hermes Agent skill-creation loop — compare to Session Scribe — think-queue item, unexplored
- [high] Yang-Mills mass gap → memory decay optimization. Memories with high graph connectivity (many relations) should be immune to eviction. Memories with few connections decay normally. The knowledge graph's connection count IS the "mass" — implement mass-weighted eviction instead of pure last_used. — S79 millennium bridge
- [medium] V5-only bias (11th mirror): scripts assume V5 is the only workspace. backup-memory.sh and morning-brief.sh both missed HOME memory. Systemic: any script written pre-S79 may have this bias. Audit all scripts for hardcoded V5 paths. — S79 dream-E11
- [medium] Navier-Stokes → system turbulence. CONFIRMED: autonomous systems generate internal noise faster than external signal (kernel auto-filing 40x, log growing, stale entries). Dedup guards and log compression ARE viscosity terms. The dream engine is half signal-amplifier, half noise-filter. Optimal ratio is the unsolved question. — S79 millennium bridge + dream-E10
- [high] Growth spiral: using the system improves the system. Dream B connects → adds edges → increases mass → prevents eviction → richer future dreams. Not maintenance — growth. The system gets smarter by running, not by being programmed. This is the core product insight. — S79 dream-E8
- [high] Crystallization threshold: when a pattern reaches 3+ connections in the graph, it graduates from observation → rule → skill. This IS the Yang-Mills mass gap applied to knowledge management. Supersaturated solution analogy — observations float until critical connection mass, then crystallize into executable structure. — S79 dream-E9
- [high] Prediction projection: 4 systems already predict (NBA, adaptive clock, dream chain, scribe corrections). Unify into one framework: sources→predictor→dispatcher→feedback. Cross-pollinate: NBA accuracy informs dream confidence, clock predictions inform dispatch timing. Not a new build — a naming + wiring of what exists. — S79 user priority
- [critical] Transfer auto-continue architecture into hybridenginev3 kernel. Replace placeholder heartbeat with adaptive clock. Wire dream engine into dreamer.ts. Gate → orchestrator middleware. Compound chain → autonomy loop. Memory graph → SQLite vault. This makes the kernel self-monitoring, self-dispatching, self-dreaming NATIVELY. No cron. No bash. Event-driven, persistent, 2-second detection. The mind meets the body. — S79 reunion

## OPTIMIZE (standing codebase improvement targets)
- Test coverage gaps
- Dead code / unused imports
- Duplication reduction
- Performance bottlenecks
- Dependency updates
