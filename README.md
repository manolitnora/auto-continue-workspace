# Auto-Continue Workspace

Public workspace for the autonomous continuation system. The remote agent clones this repo to:
- Read coordination files (think-queue, wants, cascade)
- Read context handoff (what the user was working on)
- Write output (research, analysis, drafts)
- Commit results (persisted across sessions)

## Structure

```
coordination/          Shared state files (synced from ~/.claude/)
  auto-continue.md     Priority cascade + token economics
  autonomous-wants.md  Dreams, leans, curiosities
  think-queue.md       Task queue with priorities
  context-handoff.md   What the last session was working on
  auto-continue-log.md Run log with value tracking

output/                Remote agent work output
  (research, analysis, drafts — committed by remote agent)

worktrees/             Worktree metadata
  (branch tracking for parallel work)
```

## How It Works

1. Local session detects silence (user stops responding)
2. Writes context-handoff.md + pushes coordination files
3. Dispatches remote trigger
4. Remote agent clones this repo
5. Reads coordination files → knows what to do
6. Executes work → commits output
7. Next local session pulls → sees what was done
