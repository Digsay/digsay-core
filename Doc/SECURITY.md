# Digsay Core — Security Policy
Version: 1.0

This document defines the security model of Digsay Core.

Digsay Core is designed as a deterministic, stateless
boundary verification protocol.

Security is achieved through architectural minimization.

---

## 1. Security Philosophy

Digsay Core follows the principle:

Security by absence.

Digsay Core:
- Stores no content
- Stores no personal data
- Maintains no behavioral logs
- Maintains no identity registry
- Performs no access control
- Performs no authentication

It verifies cryptographic consistency only.

---

## 2. Attack Surface

The attack surface of Digsay Core is intentionally minimal.

Primary exposure areas:
- Canonical JSON serialization
- Cryptographic fingerprint generation
- Token derivation logic
- Envelope validation logic

There is:
- No database
- No network layer (Core level)
- No session management
- No key storage

---

## 3. Cryptographic Integrity

Digsay Core relies on deterministic hashing.

Default:
- SHA-256

Future:
- SHA-512 or alternative cryptographic primitives
- Must follow VERSIONING policy

Silent cryptographic migration is forbidden.

---

## 4. Trust Boundaries

Digsay Core:
- Does not trust external inputs
- Does not validate business logic
- Does not enforce execution

It validates only:
- Structural integrity
- Canonical fingerprint reproducibility

Responsibility lies outside Digsay.

---

## 5. Threat Model Overview

Digsay Core protects against:
- Envelope tampering
- Token manipulation
- Event mutation
- Canonicalization ambiguity

Digsay Core does NOT protect against:
- Malicious AI behavior
- False external assertions
- Business logic errors
- Human misinterpretation

It protects the boundary fact only.

---

## 6. Responsible Disclosure

Security vulnerabilities should be reported privately.

Until a public security contact channel is defined,
issues must not be publicly exploited.

---

## 7. Stability Requirement

Security-related changes that affect:
- Canon
- Fingerprint algorithm
- Envelope structure

Require MAJOR version increment.

Security stability is part of institutional credibility.
