MEMORY UPDATE CONTRACT

Every memory update should follow:
CHAT_SCOPE
VERIFIED_FACTS
FILE_DELTAS
OPEN_ISSUES
ONE_LINE_STATE

AUTO MEMORY TRIGGERS
- Architecture decisions
- Incidents
- Operational lessons
- System state changes
- Confirmed runtime facts

PROMOTION PIPELINE
Chat → Incident → Lesson → Rule → Architecture

SYSTEM CONTRACTS
- Agent writes runtime facts.
- LM analyzes and summarizes.
- Validator determines PASS / FAIL.
- Project memory receives only distilled knowledge.
