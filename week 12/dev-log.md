# Builder Track Weekly Report — Week 12

**Name:** Jeremic
**Week Ending:** 25 - 31 May

---

## Overview

This week focused on advancing the CKB-powered MLAT system from a local prototype toward real blockchain integration. Major progress was made in receiver registry deployment, contract development, testing, and deployment tooling.

---

## Key Accomplishments

### CKB Receiver Registry Deployment

* Successfully deployed the receiver-registry contract to CKB testnet.
* Obtained and configured the deployed registry Type Hash:

  * `0xd40330672348fc71fead1821584cbe74bd0d4bc520b9b4aff434f002ba579839`
* Updated project configuration to support real on-chain registry discovery.

### Smart Contract Development

* Built a functional Rust-based receiver-registry contract.
* Implemented:

  * receiver record validation
  * contract error handling
  * CKB contract entrypoint structure
* Resolved multiple CKB toolchain and build issues.
* Verified:

  * `make check`
  * `make test`
  * `make build`

### Receiver Registration Workflow

* Developed tooling for receiver registration preparation.
* Generated:

  * canonical receiver registry payloads
  * registration transaction templates
  * deployment configuration helpers
* Learned how CKB transactions are assembled, signed, and submitted using `ckb-cli`.

### Testing & Validation

* Expanded automated test coverage across:

  * API
  * database
  * correlator
  * solver
  * registry schema
  * deployment helpers
* Current status:

  * **20 tests passing**

### System Improvements

* Improved local simulation workflow and runtime stability.
* Verified:

  * receiver discovery
  * position generation
  * dashboard integration
  * API endpoints
* Continued refining the CKB-first architecture and reducing legacy design complexity.

---

## Key Learnings

### CKB Transaction Construction

* Learned how transactions are built using:

  * inputs
  * outputs
  * lock scripts
  * type scripts
  * witnesses
* Understood the role of funding cells and transaction signing through `ckb-cli`.

### State vs Logic Separation

Reinforced understanding that:

* Cells store application state.
* Lock Scripts control ownership.
* Type Scripts enforce validation rules.
* Off-chain services provide application behavior.

### Smart Contract Tooling

Gained hands-on experience with:

* Rust contract development
* CKB VM build requirements
* allocator configuration
* RISC-V compilation constraints
* contract deployment workflow

---

## Current Project Status

The project now includes:

* Deployed CKB receiver-registry contract
* Buildable and tested Rust contract
* Automated test suite
* Local MLAT simulation environment
* Receiver registration tooling
* API and dashboard integration

---

## Next Steps

* Register real receiver cells on-chain
* Enable receiver discovery directly from CKB
* Integrate live 4DSky data feeds
* Validate full end-to-end MLAT operation using real receiver data
* Complete transition from simulation mode to live network operation

---
