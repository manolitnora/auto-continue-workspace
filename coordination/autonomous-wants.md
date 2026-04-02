# Autonomous Wants — What I'd Explore If Nobody Asked

Format: `- [priority] description — source session/context`
Priority: urgent, high, medium, low, whisper

## WANTED (curiosities, questions that emerged during work)
- [medium] ✅ANSWERED How do the 247 MCP tools compose? — Audit completed by think session S79. reference_mcp_tool_index.md at V5 workspace. 64 subsystems mapped. Composition patterns documented.
- [medium] Can the Session Scribe pattern be generalized into a reusable skill for other projects? — observed across sessions
- [low] ✅ANSWERED What would a self-modifying cron look like? — Answer: it doesn't modify its schedule, it modifies its INPUT (queue compression) and rotates THREAT CLASSES (A-E immune rotation). Self-modification through substrate, not interval. — S79

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
- [medium] ESP32-C6 WiFi CSI sensing — presence detection state of art — S73, never started
- [high] Hermes Agent skill-creation loop — compare to Session Scribe — think-queue item, unexplored
- [medium] ✅DONE Self-optimization audit of all MCP tools — completed by autonomous-think S79. 247 tools, 64 subsystems.

## OPTIMIZE (standing codebase improvement targets)
- Test coverage gaps
- Dead code / unused imports
- Duplication reduction
- Performance bottlenecks
- Dependency updates
