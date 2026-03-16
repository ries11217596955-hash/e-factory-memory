ACTIVE STATE

Project memory pack is used as Project Sources SSOT.

CURRENT FOCUS
- Memory discipline and architecture stability.
- LMOPS stabilization: Open WebUI + LM Studio + qwen/qwen3-8b.
- Goal: prepare reliable LM runtime before agent integration.
- Maintain clean separation between GitHub repos and runtime folders.

LINE MATURITY MAP
- MEMORY = stable base.
- LMOPS = usable / partially stable.
- AGENTOPS = partially verified / not production-ready.
- WEBOPS = baseline present / not current active focus.

CONFIRMED GITHUB REPO TOPOLOGY
- automation-kb = SITE repo
- e-factory-memory = MEMORY repo
- e-factory-agent = AGENT repo

AGENT LINE SPLIT
- mini-agent = RUN_BATCH.ps1 / GH_BATCH line
- LM-agent / watcher / loop = separate line
- Do not mix mini-agent and LM-agent as one runtime or one canonical file.

RUNTIME BOUNDARY
- Repo != runtime.
- e-factory-memory stores continuity / architecture / decisions / incidents.
- e-factory-agent stores code / structure of the agent line.
- GH_BATCH and LN_GDRIVE_AGENT_AUTO are operational runtime folders, not memory-core and not repo-memory.

NEXT
- Use clean memory-delta updates.
- Stabilize LM runtime before building direct LM-agent automation loop.
- Keep mini-agent and LM-agent separated at repo/runtime level.
- Do not promote AGENTOPS or LMOPS to stable system status without evidence / validator closure.
