AGENTOPS STATE

CONFIRMED DIRECTION
- Agent is execution layer in the architecture.
- Agent should interact with LM runtime memory and validator, not replace them.
- AGENTOPS must be tracked as separate agent lines, not as one mixed runtime.
- Runtime truth should come from evidence / validator, not from model text.

ACTIVE AGENTS
1. GH_BATCH
- Type: mini-agent / batch runner.
- Verified artifact baseline: runtime pack contains RUN_BATCH.ps1, agent.config.json, and .state/processed_sha256.txt.
- Verified operational role from uploaded pack: GitHub batch apply / repair-pack execution.
- Verified controls from uploaded pack:
  - allowed_scope = src/
  - safe auto-fix layer exists
  - plaintext guard exists
  - post-commit verify exists
  - preview mode (WhatIfOnly) exists

2. SITE_AUDITOR_AGENT
- Type: audit-agent / report generator.
- Verified artifact baseline: runtime pack contains run.ps1, agent.ps1, advice_engine.ps1, inventory.ps1, links_audit.ps1, semantic_audit.ps1, render_audit.ps1, screenshot.ps1, and target_stage.ps1.
- Verified passport baseline from uploaded pack:
  - AgentName = SITE_AUDITOR_AGENT
  - Version = v3.6
  - EntryPoint = run.ps1
  - OutputContract includes audit_result.json, HOW_TO_FIX.json, 00_PRIORITY_ACTIONS.txt, 01_TOP_ISSUES.txt, 11A_EXECUTIVE_SUMMARY.txt, REPORT.txt, DONE.ok / DONE.fail
- Verified operational role from uploaded pack: repo fetch -> audit -> report pack.

SEPARATE / NON-ACTIVE-FOCUS CONTOURS
- LM-agent / watcher / Vault loop remains a separate contour.
- It must not be merged into the active-state description of GH_BATCH or SITE_AUDITOR_AGENT.
- If resumed later, it should be tracked as its own agent line/status block.

BOUNDARY
- e-factory-memory stores AGENTOPS continuity and status, not runtime logs.
- e-factory-agent stores agent code / structure.
- Runtime folders, token stores, inbox/done/outbox, screenshots, and reports are operational layers, not memory-core.
