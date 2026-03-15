LMOPS STATE

CONFIRMED BASELINE
- Local LLM is part of the project architecture.
- LM Studio is the intended local runtime platform.
- LM responsibilities include log analysis, summarization and context reconstruction.

CURRENT STATUS
- Open WebUI + LM Studio + qwen/qwen3-8b were brought to a working baseline.
- A dedicated profile "ISO Template Factory AI — Qwen3" was created in Open WebUI.
- Memory Center was connected to the profile and project memory files are retrievable.
- The profile can answer from KERNEL_INDEX and other memory files.

KNOWN ISSUE
- <think> output remains present in the current contour.
- Root cause is not confirmed at prompt/UI level; likely backend/runtime or model-template related.
- CONTROL_LOOP retrieval/formatting is not yet stable enough to treat as verified operational command.

RUNTIME NOTE
Highly volatile remote-access facts should be refreshed when needed and not treated as stable architecture truth.
