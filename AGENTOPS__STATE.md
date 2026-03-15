AGENTOPS STATE

CONFIRMED DIRECTION
- Agent is execution layer in the architecture.
- Agent should interact with LM runtime memory and validator, not replace them.
- Shared Google Drive Vault _INBOX is the intake surface for the new LM agent; ownership is determined by explicit AGENT__ addressing, not by file type alone.
- Downloaded ChatGPT artifacts on the current agent PC can land directly into Google Drive Vault _INBOX and therefore can act as agent job intake items when they match the addressing contract.

CURRENT STATUS
- AGENTOPS is less fully represented in repo-memory than WEBOPS.
- Runtime truth should come from evidence / validator, not from model text.
- New LM agent runtime root is C:\Users\Azerbaijan\Desktop\LN_GDRIVE_AGENT_AUTO.
- Scheduled task LN_GDRIVE_AGENT_AUTO points to agent_loop_vault.ps1.
- Startup popup for the new agent loop is verified on manual loop start.
- agent_loop_vault.ps1 scans Google Drive Vault _INBOX for AGENT__ addressed jobs.
- run_agent_job.ps1 already contains move logic for _DONE / _FAILED / _DONE\_PENDING_ROUTE.
- Current runtime is PARTIALLY VERIFIED: queue/scheduler/popup/addressing path are live, but text route is not yet PASS-closed in normal loop execution.
