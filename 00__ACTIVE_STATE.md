ACTIVE STATE

Project memory pack is used as Project Sources SSOT.

CURRENT FOCUS
- Repo-memory alignment to the current operational contour.
- Two agent lines are currently active: GH_BATCH and SITE_AUDITOR_AGENT.
- MEMORY remains the continuity layer; LMOPS remains a support line, not the current primary focus.
- Maintain clean separation between GitHub repos and runtime folders.

LINE MATURITY MAP
- MEMORY = stable base.
- AGENTOPS = active operational line with two active agents; overall line is not treated as globally stable without evidence per agent.
- LMOPS = usable / support line / partially stable.
- WEBOPS = active through supporting agent workflows, but not the main memory-update focus in this patch.

CONFIRMED GITHUB REPO TOPOLOGY
- automation-kb = SITE repo
- e-factory-memory = MEMORY repo
- e-factory-agent = AGENT repo

ACTIVE AGENT MAP
- GH_BATCH = active mini-agent for GitHub batch apply / repair packs.
- SITE_AUDITOR_AGENT = active site-audit agent for repo fetch -> audit -> report pack.
- LM-agent / watcher / Vault loop = separate contour and not the current active focus in repo-memory.

RUNTIME BOUNDARY
- Repo != runtime.
- e-factory-memory stores continuity / architecture / decisions / incidents.
- e-factory-agent stores code / structure of the agent line.
- GH_BATCH and SITE_AUDITOR_AGENT uploaded runtime packs are operational agent artifacts, not memory-core.
- Frozen or paused agent contours must not overwrite the active agent map.

NEXT
- Keep repo-memory aligned with the two active agent lines.
- Track agent status by agent line, not as one mixed AGENTOPS runtime.
- Keep mini-agent, audit-agent, and LM-agent separated at repo/runtime level.
- Do not promote any agent line to stable system status without evidence / validator closure.
