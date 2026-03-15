
INCIDENTS LOG

Use this file for:
- symptom
- root cause
- fix
- anti-regression
- status

This file also hosts the project MistakeBank-Lite section used to track recurring reasoning and process mistakes across chats and project lanes.

---

BASELINE INCIDENT THEMES

- memory drift when continuity layer is not updated
- confusion when architecture/state/lessons/chat-delta are mixed
- volatile LM runtime facts becoming stale

---

ACTIVE INCIDENT

ID
MEMORY.CANONICAL_DRIFT.001

SYMPTOM
Parallel or stale state copies can create more than one apparent version of truth for the same project line or status snapshot.

ROOT CAUSE
Canonical precedence is not explicit enough during memory-pack refreshes, especially when operational summaries evolve faster than architecture files.

FIX
Use one canonical active file per memory role and apply precedence: ACTIVE_STATE + CONTROL_LOOP + validator/evidence over older summaries.

ANTI-REGRESSION
- Add canonical-file discipline to MEMORY_OPERATIONS.
- Mark older or parallel copies as archive/legacy when discovered.
- Do not declare system stability from stale summaries.

STATUS
OPEN

---

ACTIVE INCIDENT

ID
MEMORY.RULE_DUPLICATE_PROMOTION.001

SYMPTOM
A behavior already covered by active line practice or live project memory was reintroduced as if it were a new kernel rule.

ROOT CAUSE
Rule novelty was not checked explicitly before promotion. Classification between rule, line practice, and delivery mode was blurred.

FIX
Add a mandatory novelty guard before core/bio-memory promotion. If the behavior is already covered, record: NO NEW RULE — already covered / existing practice.

ANTI-REGRESSION
- Run Rule Novelty Guard before any new core commit.
- Classify each proposal as Rule / Practice / Delivery mode before promotion.
- Reaffirm existing line practice in line/state or decisions files instead of duplicating it as a new kernel rule.

STATUS
OPEN

---

MISTAKEBANK_LITE

Purpose
Track recurring reasoning and operational mistakes so they do not repeat across sessions, lanes, or memory cycles.

Maintained by
Assistant (owner does not maintain this manually).

Usage
Entries are added only when a pattern appears or repeats. This is not a log of random mistakes but a registry of recurring failure patterns.

Format

MB-ID
Symptom
False Move
Correct Move
Early Detector
Scope
Status

---

MB-01

Symptom
Kernel rule is created even though the behavior already exists as line practice.

False Move
Operational practice is promoted to architecture rule.

Correct Move
Apply CORE.RULE_NOVELTY_GUARD before rule promotion.

Early Detector
Question: “Does this affect the whole architecture or only the current workflow?”

Scope
CORE

Status
ACTIVE

---

MB-02

Symptom
Strong claims (“fixed”, “resolved”, “ready”) are made without artifact verification.

False Move
Claim strength exceeds available evidence.

Correct Move
Use evidence discipline and claim ladder:
hypothesis → probable → verified → reproducible.

Early Detector
No artifact, log, file diff, or runtime confirmation exists.

Scope
ALL LANES

Status
ACTIVE

---

MB-03

Symptom
Patch or fix begins before baseline/source of truth is confirmed.

False Move
System is modified before confirming the active baseline.

Correct Move
Confirm baseline → verify source artifact → then patch.

Early Detector
No confirmed SSOT file, artifact hash, repo state, or runtime log.

Scope
DOCS / WEBOPS / AGENT

Status
ACTIVE

---

MB-04

Symptom
Architecture, execution, and analysis are mixed in the same step, causing scope drift.

False Move
Answer attempts to redesign architecture while executing a patch or analysis task.

Correct Move
Separate phases clearly:
analysis → decision → patch → verification.

Early Detector
Change depth increases without explicit command.

Scope
ALL LANES

Status
ACTIVE
