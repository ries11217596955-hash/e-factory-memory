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
- Local AI environment deployed: Open WebUI + LM Studio + qwen/qwen3-8b.
- Memory Center connected; project memory retrieval works partially.
- Profile baseline is usable, but reasoning tag output (<think>) is not fully eliminated.
- New LM agent runtime root is C:\Users\Azerbaijan\Desktop\LN_GDRIVE_AGENT_AUTO.
- Scheduled task LN_GDRIVE_AGENT_AUTO points to agent_loop_vault.ps1.
- Google Drive Vault _INBOX is the intake surface; addressing contract is AGENT__*.
- Popup/start signal is verified on manual loop start.
- Direct job handler contains move logic for _DONE / _FAILED / _DONE\_PENDING_ROUTE.
- Current runtime status is PARTIAL: queue/scheduler/addressing path verified; normal-loop text route not yet PASS-closed.

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

NEXT_STEP
- Close the text-route failure in normal LM-agent loop execution and normalize outputs/state for remote-visible operation through Google Drive Vault paths.
- Keep repo-memory and runtime layers separated while updating AGENTOPS documentation.
