## Quick start

```bash
digsay fix input.json > proof.json
digsay verify proof.json
```
---


# AI Decision Trace — Digsay Example

---

## Problem

AI systems increasingly act autonomously, but there is no neutral way to fix the moment when a decision crosses a responsibility boundary.

Each system relies on its own internal logs, leading to incompatible versions of reality.

Digsay introduces a minimal, neutral fixation at that boundary.

This example demonstrates how to fix a decision boundary
and verify it independently.

---

## What is happening

An AI system produces a recommendation.

A human reviewer accepts it.

The moment of acceptance is fixed as a verifiable event.

This is not about logging the process — it is about fixing the boundary.

---

## Why this matters (Dispute scenario)

Later, a dispute occurs.

A client, regulator, or partner asks:


> "Why was this decision made?"

Or more precisely:

> "What exactly happened, and can you prove it?"

Without a verifiable trace:
- only internal logs exist,
- explanations are subjective,
- trust is limited.

With Digsay:
- the moment of decision is fixed,
- the boundary is verifiable,
- no reliance on internal logs is required.

## Step 1 — Fix the event

```bash
digsay fix input.json > proof.json
```

---

## Step 2 — Verify the event

```bash
digsay verify proof.json
```

Expected output:

```bash
VALID
event_id=...
```

---

## What this proves

- A decision boundary existed.
- It was finalized.
- It can be verified independently.
- The event can be used as an independent reference in a dispute.

---

## What this does NOT do

- Does not explain the AI decision.
- Does not store user data.
- Does not interpret meaning.

---

## Scope (What Digsay does and does NOT touch)

Digsay does NOT observe or verify your entire system.

It does NOT:
- inspect your application,
- monitor your services,
- analyze your logs,
- access user data.

Digsay only fixes boundary events at the moment when your AI agents interact with:
- other agents,
- external systems,
- or humans.

All internal behavior of your AI agents remains your own process.

You decide:
- whether to use Digsay,
- where to place fixation points,
- and what interactions matter.

Digsay does not enter your system.

It only fixes the boundary where your system meets the outside world.

## Key idea

Digsay does not record system activity.

It fixes the moment — so it cannot be rewritten.
