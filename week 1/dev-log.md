# Builder Track Weekly Report — Week 1  
**Name:** Jeremic  
**Week Ending:** 9 - 15 March

---

## Courses Completed

### Introduction to Nervos CKB
- Studied the core architecture of the Nervos CKB blockchain  
- Covered:
  - Cell Model (UTXO-based design)
  - Capacity model (1 CKB = 1 byte of storage)
  - Transaction structure (inputs → outputs)
  - Lock vs Type scripts

### Getting Started on CKB
- Explored development environment setup and tooling direction  
- Reviewed ecosystem tools such as OffCKB and CCC  
- Gained familiarity with testnet usage and RPC interaction  

### Introduction to Scripts
- Learned script structure:
  - `code_hash`
  - `args`
  - `hash_type`
- Understood that scripts define validation logic rather than storing executable contracts directly  

---

## Key Learnings

### Cell Model
- CKB state is composed of **cells that are created and consumed over time**  
- State is represented as a set of live cells  
- No traditional account-based balance model  

### Ownership via Lock Scripts
- Lock scripts define ownership using cryptographic verification  
- Unlocking requires a valid signature  
- A return value of `0` indicates successful validation  

### Type Scripts (Validation Rules)
- Optional scripts used to enforce rules on how cells can change  
- Applied across both inputs and outputs  
- Useful for implementing tokens, NFTs, and other programmable assets  

### Code as Data
- Scripts reference code via `code_hash`  
- Actual code is stored in separate cells (CellDeps)  
- Enables modularity and reuse of on-chain logic  

### Execution Model
- Scripts are executed in the CKB-VM  
- Lock scripts validate inputs  
- Type scripts validate full state transitions  

---

## Practical Progress

- Connected wallet to the CKB testnet  
- Retrieved and inspected live cells  
- Explored cell structure in JSON format:
  - capacity  
  - lock script  
  - optional type script  
- Understood that wallet balance equals the sum of all live cell capacities  

---

## Challenges & Observations

- Adjusting from account-based (Ethereum) to UTXO-based thinking  
- Separating:
  - state (cells)  
  - logic (scripts)  
- Understanding script referencing via hashes required deeper conceptual clarity  

---

