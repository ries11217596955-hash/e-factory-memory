MEMORY OPERATIONS

CHANGELOG PURPOSE
Track structural memory changes.

UPDATE PRIORITY
1. ACTIVE_STATE
2. CONTROL_LOOP
3. DECISIONS
4. INCIDENTS
5. LINE FILES

SIZE RULES
- STATE files: keep small and readable
- ISSUES: keep short and current
- LESSONS: only mature repeated patterns
- INCIDENTS: archive old entries when needed

BOUNDARIES
Do not mix:
- project memory
- runtime logs
- chat transcripts
- temporary experiments

CANONICAL FILE DISCIPLINE
- For each memory role, keep one canonical active file.
- If parallel or older copies exist, mark them as archive/legacy and do not use them as active truth.
- When current state and historical notes conflict, ACTIVE_STATE + CONTROL_LOOP + validator/evidence take precedence over older summaries.
- Do not promote runtime observations into core architectural truth without distilled confirmation.

MATURITY DISCIPLINE
- Stable = architecture/base truth with repeated confirmation.
- Partial = usable but not release- or production-ready.
- Volatile = runtime or remote fact that may drift and must be rechecked.
- Never label the whole system stable if a critical line remains only Partial.

RULE NOVELTY GUARD
Before promoting a new rule to core or bio-memory:
1. Check whether the behavior is already covered by:
   - frozen/core architecture files
   - active line practice
   - established delivery mode
   - existing live memory/committed project memory
2. If already covered, do not create a new rule.
3. Respond/state outcome as:
   NO NEW RULE — already covered / existing practice.
4. Promote only when scope, novelty, and impact are genuinely new.

CLASSIFICATION CHECK
When evaluating a proposed memory update or commit:
- Rule = architecture / invariant / cross-line guard.
- Practice = established working method inside one line.
- Delivery mode = default artifact handoff format for a lane/task.
- Do not promote practice or delivery mode to core unless it changes cross-line behavior or architecture.

LINE PRACTICE PRECEDENCE
- If an active line already has an established default delivery mode, follow that mode unless an explicit exception is requested.
- Do not silently downgrade from archive/batch delivery to file-by-file manual replacement.
- If a delivery mode is reaffirmed rather than invented, record it as existing practice, not as a new core rule.

AUDIT CYCLE
Every major phase should include:
1. Review ACTIVE_STATE
2. Review ISSUES files
3. Promote lessons
4. Remove obsolete facts
5. Check canonical-file precedence and archive stale duplicates when found
6. Run rule-novelty check before any core/bio-memory commit


PROMOTION CONTROLLER

Purpose
Control how knowledge moves through project memory without creating new files or breaking the layered architecture.

PROMOTION PIPELINE
Chat → Incident → Lesson → Rule → Architecture

PROMOTION RULES

1. INCIDENT
Create or update an entry in INCIDENTS.md when:
- a failure or confusion occurred
- anti-regression needs to be recorded
- the event may repeat in future work

2. LESSON
Promote to *_LESSONS.md when:
- the same incident pattern appears more than once
- the fix becomes stable knowledge
- the pattern is useful for future work in the same lane

3. RULE
Promote to a rule only when:
- the lesson becomes a cross-line invariant
- the behavior must be enforced system-wide
- it affects architecture, governance, or core safety

4. ARCHITECTURE
Promote to architecture only when:
- the rule changes the system structure
- the change affects memory layout, project layers, or core boundaries

ANTI-REPEAT SYSTEM

To reduce repeated mistakes and drift across chats, the system maintains:

MistakeBank-Lite
A registry of recurring reasoning or process mistakes stored inside INCIDENTS.md.

Claim Discipline
Clearly distinguish:
- hypothesis
- probable analysis
- verified fact
- reproducible confirmation

Operational Clarity
When performing memory updates:
- confirm baseline first
- verify canonical file
- apply delta instead of rewriting unrelated sections

ANTI-REPEAT RULE
When a mistake pattern appears twice:
1. record it in the MistakeBank-Lite section of INCIDENTS.md
2. include early detection and correct move
3. use it as anti-regression guidance for future updates

FILE ROLE REMINDER

INCIDENTS.md
Holds incidents, anti-regression patterns, and MistakeBank entries.

DECISIONS.md
Contains architectural or operational decisions only.

*_LESSONS.md
Contains stable lessons derived from repeated incidents.

KERNEL / RULE FILES
Contain only cross-line invariants and architectural guards.
