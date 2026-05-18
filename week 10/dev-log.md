# Builder Track Weekly Report — Week 10  
**Name:** Jeremic  
**Week Ending:** 11 - 17 May

---

## Overview

This week focused on decentralized identity systems on CKB and how identity can persist independently from wallet addresses using Cells, Lock Scripts, and Type Scripts.

I explored the `did:ckb` ecosystem through the Vellum dashboard project and studied how DID operations are implemented directly on-chain without centralized APIs.

---

## Key Learnings

### DID Architecture on CKB
Learned how `did:ckb` uses:
- Cells for DID state
- Lock Scripts for ownership
- Type Scripts for validation
- transaction lineage for operation history

### DID Lifecycle
Studied:
- DID creation
- DID resolution
- profile updates
- key rotation
- DID deactivation
- migration from `did:plc`

### Identity Persistence
Understood how identity remains stable even when wallet addresses change:
- DID stays constant
- ownership can rotate to a new Lock Script
- reputation can persist across wallets

### History Resolution
Learned how DID history can be reconstructed client-side by:
- traversing previous transaction inputs
- following Cell lineage
- classifying operations:
  - CREATE
  - UPDATE
  - MIGRATE

---

## SDK & Development Concepts

Studied the proposed `@ckb-ccc/identity` package:
- `resolveDid`
- `buildCreateTx`
- `buildUpdateTx`
- `buildDeactivateTx`
- `buildMigrationTx`
- `listDidsByLock`

Also explored:
- DAG-CBOR encoding
- DID document structure
- base32 identifiers
- profile metadata conventions

---

## Design Insights

### Profile Metadata
Explored portable DID profile data:
- display names
- avatars
- bios
- service entries

### Capacity Economics
Learned how DID documents consume CKB capacity:
- more data locks more CKB
- storage must remain compact
- reserve capacity helps future updates

### Future Directions Studied
- DID-linked Spores/NFTs
- DID-based reputation systems
- Verifiable Credentials
- Nostr integration
- wallet rotation UX

---

## Current Understanding

This week improved my understanding of:
- decentralized identity on CKB
- practical use of Cells beyond payments
- ownership vs state separation
- on-chain vs off-chain responsibilities
- persistent digital identity systems on CKB

---