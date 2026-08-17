# Builder Track Weekly Report — Week 23
**Name:** Jeremic  
**Week Ending:** 10 - 16 August

---

# Overview

This week focused on strengthening the Registry V2 infrastructure, improving reproducibility, and preparing a focused Spark grant proposal for the CKB Receiver Registry SDK.

---

# Completed Work

## Registry V2

- Completed Registry V2 implementation and testnet lifecycle validation.
- Verified receiver creation, update, ownership transfer, and permanent revocation.
- Added immutable receiver identities using CKB Type ID.
- Added sequence-controlled lifecycle transitions and security checks.
- Tested adversarial cases including forged identities, duplicate outputs, resurrection, and identity burn.

## Reproducibility & Evidence

- Completed deterministic benchmark and evidence tooling.
- Added pinned Python dependencies and reproducible CI workflows.
- Verified generated artifacts using SHA-256 hashes.
- Published reproducibility evidence and CI results.
- Verified the deployed Registry V2 binary against the reproducible build artifact.

## Repository & Security Review

- Continued reviewing the repository structure and technical debt.
- Identified remaining gaps between the Registry V2 contract and off-chain discovery implementation.
- Defined the required architectural fixes to ensure the same receiver identity is preserved across Rust, Python, and future TypeScript implementations.
- External security review remains pending.

## Spark Grant Proposal

Drafted a Spark proposal for the **CKB Receiver Registry SDK**.

The proposed SDK will:
- provide a TypeScript interface for Registry V2
- integrate with CKB-CCC signers
- support create, update, transfer, and revoke operations
- provide CKB indexer discovery
- maintain consistent lifecycle rules across Rust, Python, and TypeScript
- include cross-language conformance tests
- produce a fresh testnet lifecycle and reproducible evidence package

The proposal intentionally keeps the scope focused on developer infrastructure rather than the broader MLAT dashboard or physical receiver deployment.

---

# Current Status

The project now has:

- Registry V2 smart contract
- CKB testnet deployment and lifecycle evidence
- Reproducible build and CI infrastructure
- Python discovery and validation tooling
- MLAT reference application
- Public technical documentation
- Draft Spark proposal for the Registry V2 SDK

---

# Next Steps

- Finalize and submit the Spark proposal.
- Complete the Registry V2 external security review.
- Reconcile the Rust, Python, and TypeScript identity models.
- Begin implementation of the Registry V2 TypeScript SDK if funded.
- Continue preparing the MLAT platform for future live receiver validation.

---

# Summary

Week 23 focused on moving the project from a working Registry V2 implementation toward a reusable CKB developer infrastructure component. The main focus was reproducibility, security review preparation, and defining a clear SDK scope for the next stage of the project.