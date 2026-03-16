# KERNEL RULE PACK — SITE_AUDITOR_AGENT BASELINE

CommitId: COMMIT-2026-03-16-SITE-AUDITOR-BASELINE-PACK
CoreRev: KERNEL.AGENTOPS.v1.0.1

## NEW ACTIVE RULES

### AGENT.DELIVERY.PACKAGE_STANDARD v1.0
Agents must be delivered as ZIP packages. Standard install flow:
extract -> token/config -> `CREATE_SHORTCUT.ps1` -> launch by shortcut.

### AGENT.RUNTIME.ROOT_RESOLVER.PSSCRIPTROOT_FIRST v1.0
For agent launcher/runtime scripts use `$PSScriptRoot` as primary root resolver.
Do not rely on `MyInvocation.MyCommand.Path` as primary entrypoint root detection.

### AGENT.OUTPUT.LOCAL_OUTBOX_RELATIVE_TO_AGENT_ROOT v1.0
Default output location for agent results is `outbox` under agent root.
Do not hardcode drive-specific delivery paths for baseline local delivery.

### AGENT.DEBUG.NO_DOUBLECLICK_DIAG v1.0
Launcher/runtime diagnostics must be done from visible console, not by double-click execution.

## Reality / Evidence
Practical evidence observed in working session:
- ZIP delivery/install model used successfully
- shortcut creation validated
- initial launcher defect identified
- launcher fixed by switching to `$PSScriptRoot`
- audit pack generated successfully
