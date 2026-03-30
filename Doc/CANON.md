Digsay Core — Executable Canon
CANON.md v1.0-core
---

## Preamble — Why Digsay Exists

As AI systems increasingly interact with each other and with humans, the absence of a neutral point of verification creates a structural risk.

Internal logs, internal policies, and internal explanations remain bound to the system that produced them.


When disputes, conflicting interpretations, legal, social, or economic consequences arise, no party can be considered a neutral source of truth.

Digsay is not created to control systems.

It exists to resolve a structural problem that no single participant can solve from within its own boundary.

The moment responsibility crosses systems, internal truth is no longer sufficient.

Digsay exists to introduce a neutral fixation layer at responsibility boundaries.

It does not belong to any side of the interaction, conflict, or consequence chain.

Its purpose is to create an independently verifiable fact at the exact moment when responsibility may arise.

---

##  Scope
This canon defines ONLY the executable invariants of Digsay-Core.
Anything not defined here is out of scope for the Core and MUST NOT
influence Core APIs or data models.

Canonical statement:
> Digsay fixes verifiable boundary facts and nothing beyond them.

---

Digsay is not a participant of processes.
Digsay is a neutral infrastructure for fixation and verifiability of facts.

- Digsay does not make decisions.
- Digsay does not interpret meaning.
- Digsay does not manage consequences.
- Digsay records externally verifiable facts only.

---

## 1A. Human Non-Surveillance & AI Accountability Principle

Digsay is NOT about monitoring or controlling people.

Digsay is about:
- verifiability of interactions in automated environments,
- accountability of AI systems and algorithms,
- proving that systems acted within allowed boundaries.

Digsay MUST NOT:
- track individuals,
- build behavioral profiles,
- enable surveillance of humans.

Digsay is designed to provide:
- proof that an AI/system acted within permitted constraints,
- a verifiable boundary of interaction without storing meaning.

Digsay focuses on:
- AI–AI interactions,
- AI–Human responsibility boundaries,
- autonomous systems operating within defined constraints.

---

## 1B. Evidence Positioning Principle

Digsay does NOT prove, evaluate, or judge actions.

Digsay fixes a deterministic trace that MAY be used as independently verifiable evidence outside the system.

- Digsay does not create a verdict.
- Digsay does not determine permissibility.
- Digsay does not assign legal meaning.

Digsay enables:
- verifiable traceability of boundary events,
- independent verification of fixed facts,
- use of those facts as evidence by external parties and frameworks.

Canonical statement:
> Digsay creates a verifiable trace — not a verdict.
---

## 2. External Boundary Principle
Internal ecosystems rely on internal logs and policies.
At the moment an interaction crosses into an external responsibility domain,
an external, neutral and verifiable fact is required.

Digsay exists exclusively to fix this external responsibility boundary.

The boundary is considered crossed only upon finalized Context Binding and creation of a deterministic Event.

---

## 3. Trust Modes
Digsay separates two non-overlapping modes:

### 3.1 Trust Observation
- Records confirmed facts of existence or interaction.
- Does not express consent or intent.
- Creates no responsibility.
- Never becomes Action automatically.

### 3.2 Trust Action
- Records explicit, confirmed human will.
- Requires a physical confirmation by the human.
- Creates responsibility outside Digsay only.
- Happens once per responsibility boundary.

---

## 4. Machine Event (SYSTEM ↔ SYSTEM)
Machine Event records the fact that a SYSTEM performed an action
at a specific moment when crossing the External Boundary.

Properties:
- SYSTEM ↔ SYSTEM only.
- Observation mode only.
- No physical confirmation.
- Does not by itself create or assign legal responsibility.
- No content, logs or data stored.

Machine Event records the boundary of fact, not the meaning of the action.

---

## 5. Assertion Event (SYSTEM → HUMAN)
Assertion Event records the moment a human accepts an assertion
produced outside Digsay as a basis for their own decision.

Rules:
- Initiated and confirmed by a human only.
- SYSTEM cannot perform Action.
- Requires physical confirmation.
- Records the moment after which responsibility may attach to the human
  according to the applicable legal or operational framework.
- Stores no assertion content.

Formal Mode Mapping:
- Machine Event always operates in Observation mode.
- Assertion Event necessarily involves Action mode.

---

## 6. Context Binding v3.1
Context Binding is the minimal, deterministic structure
that defines participants, policies and responsibility boundaries.

### Canonical Structure
```json
{
  "version": "3.1",
  "event_id": "deterministic_hash",
  "initiator": {
    "type": "human | system",
    "id": "string",
    "policy": "observation | action | assertion",
    "represents": "optional_legal_entity"
  },
  "participants": [
    {
      "type": "human | system",
      "id": "string",
      "policy": "observation | action | assertion",
      "represents": "optional_legal_entity"
    }
  ],
  "finalized": true,
  "timestamp": "unix"
}
```

### Canonical Rules
- Only HUMAN may have policy = action.
- SYSTEM may have observation or assertion only.
- The role of Initiator does not by itself create or transfer responsibility.
- Digsay does not generate legal responsibility.
- Digsay records boundary events after which responsibility may arise
  according to the applicable legal or operational framework.
- Finalization is mandatory.
- Event creation MUST occur only after successful finalization of Context Binding.
- A non-finalized Context Binding MUST NOT produce a valid Event.

---

## 7. Fixation Acknowledgement (FA)
Fixation Acknowledgement is a mirrored marker stored outside Digsay
by the operator of the interacting system.

FA:
- Is not an action or consent.
- Does not store content.
- Cannot exist without a prior Digsay fixation.
- Prevents denial of fixation by the operator.

Minimal format:
```json
{
  "digsay_fixation": {
    "event_id": "deterministic_hash",
    "timestamp": "unix",
    "context_binding_hash": "hash"
  }
}
```

FA references the canonical Event identifier and does not introduce an alternative identity.

---

## 8. Black Box Principle (Aviation Sense)
Digsay is a black box of interaction in the aviation sense.

- Digsay does not explain decisions.
- Digsay does not control behavior.
- Digsay records facts, moments, and boundary transitions.

Digsay increases accountability without altering decision authority.

## 9. Verification as a Canonical Primitive

Verification in Digsay-Core is a canonical, authority-free primitive.

- Digsay does not introduce new cryptographic algorithms.
- Digsay relies on existing, well-known cryptographic primitives.
- Verification is deterministic, stateless, and reproducible.
- Verification does not interpret meaning or consequences.

Verification answers only one canonical question:
> "Does this proof correspond to the same fixed fact?"

In this sense:
- cryptographic algorithms (e.g. SHA-256) provide mathematics,
- verification primitives (e.g. `sha256sum`) provide standards of use,
- Digsay Verify provides a canonical standard of fact verification.

Verification never initiates fixation
and never creates responsibility.

Canonical Note (Future Compatibility):

Digsay-Core intentionally does not bind verification
to a single cryptographic era or algorithm family.

All cryptographic primitives used by Digsay Verify
are treated as replaceable, provided they satisfy
the required security and determinism properties.

This allows Digsay-Core to remain valid across
future computational shifts without changing
its canonical meaning or responsibility model.

Any cryptographic replacement MUST preserve deterministic identity of already fixed Events.

---

## 10. Storage and Privacy

Digsay stores only fixation artifacts and cryptographic metadata strictly required for deterministic verification of boundary events.

Digsay:
- Stores no business content.
- Stores no personal data.
- Stores no behavioral graphs.
- If storage is used for proof anchoring, it is append-only and immutable.

Privacy is achieved by architectural minimization and absence of business-level data.

---

## 11. Multilingual Canon Synchronization Rule

Digsay Core Canon may exist in multiple language versions.

Rule:
- Any change to the Canon MUST be applied to ALL language versions.
- Changes MUST be structurally and semantically mirrored.
- No language version may introduce unique rules, entities, or scope.

If a change cannot be mirrored, it MUST NOT be introduced.

---

## 12. Canonical Formulae

Internal domain — rules and logs.  
External boundary — verifiable fact.

SYSTEM produces assertions.  
Responsibility may attach outside Digsay according to the applicable framework.  
Digsay fixes the moment.

Observation never becomes Action automatically.
