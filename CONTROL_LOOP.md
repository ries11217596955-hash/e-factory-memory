CONTROL LOOP

FORMAT
DATE
EVENT
CAUSE
ACTION
RESULT

CURRENT BASELINE
- Repo memory-core confirmed as enforced layer.
- New line-based memory pack introduced for project continuity.
- Bootstrap layer added for fast entry into new chats.

CURRENT_STATE
- Repo-memory is aligned around continuity, not runtime storage.
- Two uploaded agent packs are the current active operational focus:
  - GH_BATCH
  - SITE_AUDITOR_AGENT
- LMOPS remains part of the architecture, but is not the primary focus of this memory patch.
- Agent lines must be tracked separately to avoid mixed-state drift.

EVENT LOG
2026-03-16
EVENT
GitHub architecture split confirmed as three repos.
CAUSE
Project continuity, site delivery, and agent code needed separate canonical layers.
ACTION
Confirmed and fixed repo map:
- automation-kb = SITE
- e-factory-memory = MEMORY
- e-factory-agent = AGENT
RESULT
Repo roles became explicit; project memory, site code, and agent code are no longer treated as one mixed repo.

2026-03-16
EVENT
Agent line split clarified.
CAUSE
Mini-agent Git batch runner and LM-agent loop had started to drift conceptually into one “agent”.
ACTION
Confirmed:
- mini-agent = RUN_BATCH.ps1 / GH_BATCH line
- LM-agent = separate watcher/loop line
- runtime folders are not repo-memory
RESULT
Boundary between code repo and runtime folders became explicit; future memory updates can describe both lines without mixing them.

2026-04-01
EVENT
Repo-memory active agent map was realigned to current operational use.
CAUSE
Current work is centered on two active uploaded agent packs, while repo-memory was still centered on LMOPS stabilization and the older LM-agent contour.
ACTION
Updated active-state files to reflect:
- active agents = GH_BATCH + SITE_AUDITOR_AGENT
- LM-agent / Vault-loop = separate non-active-focus contour
- README consistency fix for repo structure contract
RESULT
Repo-memory active picture now matches the current operational contour without changing the core architecture.

NEXT_STEP
- Keep per-agent status current inside AGENTOPS state files.
- Update decisions only for confirmed operational facts, not for temporary runtime observations.
- Preserve the separation between active agents, frozen contours, and runtime evidence.
