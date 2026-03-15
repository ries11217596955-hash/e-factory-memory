AGENTOPS RUNTIME LESSONS

MATURE LESSONS
1. Runtime logs must be written by the agent, not by the LLM.
2. Validator output is SSOT for PASS / FAIL.
3. Project memory should receive distilled lessons, not raw execution traces.
4. Retry-to-GOLD loop is target architecture and should not be written as active until confirmed.
5. Splitting the new LM agent from the legacy agent and narrowing scope to Google Drive Vault -> PowerShell loop -> LM Studio makes the runtime testable and drastically reduces setup complexity.
6. For shared inbox operation, addressing must be explicit (AGENT__) and must not be inferred from file type alone.
7. Direct manual execution of run_agent_job.ps1 is an effective diagnostic step to separate loop/scheduler issues from job-handler issues.
8. Popup on loop start is useful as a human-visible startup signal, but AUTOPILOT_STATUS.json and HEARTBEAT remain the truth sources.
9. Download path matters operationally: on the current agent PC, ChatGPT downloads landing directly in Google Drive Vault _INBOX create a practical remote-intake path without requiring direct ChatGPT-to-Google-Drive integration.
