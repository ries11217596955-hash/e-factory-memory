AGENTOPS ISSUES

OPEN ISSUES
- AGENTOPS memory picture previously over-focused on the LM-agent / Vault-loop contour and under-described the two currently active agents.
- GH_BATCH is active operationally, but its status/boundary had not been fully reflected in the main AGENTOPS state files.
- SITE_AUDITOR_AGENT has dedicated memory fragments, but was not fully integrated into the shared active-state picture.
- Per-agent evidence maturity is still uneven: uploaded runtime packs confirm structure and contracts, but not full runtime closure for every workflow in this repo-memory patch.
- Active, paused, and frozen agent contours must remain explicitly separated to avoid future state drift.

PATCH INTENT
- Keep AGENTOPS state organized by agent line.
- Preserve the boundary between active agents and non-active-focus contours.
- Avoid treating one historical contour as the whole AGENTOPS picture.
