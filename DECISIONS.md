DECISIONS LOG

Use this file for confirmed architectural and operational decisions only.

BASELINE DECISIONS
- Repo memory is treated as SSOT continuity layer.
- Layered architecture:
  ChatGPT = strategy
  Local LLM = memory / analysis
  Agent = execution
  Project Brain = FUTURE / PLANNED
- Line-based memory pack with shared core + bootstrap layer is the chosen project memory model.
- Prioritize LM runtime stabilization before building the direct agent automation loop.
  Reason: agent loop reliability depends on stable LM API responses and predictable runtime behaviour.

NEW CONFIRMED DECISIONS (2026-03-11)
- New LM agent is developed as a separate runtime from the legacy agent; legacy agent remains untouched during LM-agent bring-up.
- Google Drive Vault is the target intake surface for the new LM agent; the Desktop runtime folder is for code/state/logs, not as the target inbox.
- Shared _INBOX ownership is determined by explicit AGENT__ addressing, not by file type alone.
- On the current agent PC, downloaded ChatGPT artifacts can act as LM-agent intake because they land in Google Drive Vault _INBOX.
- Startup visibility for the new LM agent is required; popup/start signal is accepted as a human-visible indicator while AUTOPILOT_STATUS.json + HEARTBEAT remain the truth sources.
- Remote-work operating model for the LM agent should be Google-Drive-centric: intake through Vault _INBOX and operational outputs targeted to Vault _OUTBOX / _DONE / _FAILED rather than relying on Desktop-only visibility.

NEW CONFIRMED DECISIONS (2026-03-12)
- For WEBOPS/site work, the default delivery mode is a ready patch-archive (ZIP) with correct repo-relative paths plus short APPLY / DELETE / VERIFY instructions.
- File-by-file manual replacement is not the default WEBOPS/site mode unless explicitly requested as an exception.
- Reaffirmation of an existing line practice must not be recorded as a new kernel rule when the behavior is already covered by active memory or line workflow.
