AGENTOPS ISSUES

OPEN ISSUES
- AGENTOPS is not yet as fully documented as WEBOPS in the current memory-core.
- Full retry-to-GOLD loop with LM diagnosis and validator truth is still a target state.
- Direct write-back path from agent runtime into clean project memory is not yet confirmed as active.
- New LM agent intake/runtime is only partially closed: scheduler, popup, Google Drive Vault detection, and AGENT__ addressing are verified, but normal-loop text route is not yet PASS-closed.
- One addressed text test ended in _FAILED, so the LM text route still needs root-cause closure before declaring production readiness.
- Reboot behaviour is not yet verified: popup was observed on manual loop start, but not yet after a full Windows reboot.
- Job-container contract (AGENT__job_* with order.json + attachments) is designed but not yet activated as the standard production runtime contract.
- Desktop-local outputs and state remain a visibility risk for remote work; operational outputs should be normalized toward Google Drive Vault paths where practical.
