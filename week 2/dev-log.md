# Builder Track Weekly Report — Week 2  
**Name:** Jeremic  
**Week Ending:** 16 - 22 March

---

## Courses Completed

### CKB Academy (Lessons 1 & 2)
- Reinforced understanding of:
  - Cell lifecycle
  - Script execution model
  - Transaction validation flow  

### Practical Script Concepts
- Explored:
  - Lock vs Type script execution
  - Code storage via CellDeps
  - Script reuse through `code_hash`

---

## Key Learnings

### Script Execution Model
- Lock scripts:
  - Validate ownership (executed on inputs)
- Type scripts:
  - Validate state transitions (executed on inputs and outputs)

### Transaction Lifecycle in CKB
- Transactions:
  - Consume existing cells (inputs)
  - Create new cells (outputs)
  - Include witnesses (signatures)
- Every state change is explicit and traceable  

### Cell Model in Practice
- Cells store:
  - Capacity (CKB value)
  - Arbitrary data (`outputs_data`)
- Enables combining **value + application state** in a single structure  

### CKB vs Solidity (Practical View)
- Solidity:
  - Contract holds state + logic
- CKB:
  - Cells hold state
  - Scripts validate transitions  
- More flexible, but requires explicit transaction design  

---

## Practical Progress

### FiberAgentPay — On-Chain Execution

Built and executed real transactions on CKB testnet as part of the **FiberAgentPay** system.

---

### 🔗 Verified Transactions

- Transaction 1 (CKB transfer):  
  https://pudge.explorer.nervos.org/transaction/0xf16e3b6737c4bc30e8a15db6cd9239875827141e95e00ab0c29d0882c64abda1  

- Transaction 2 (On-chain payment record):  
  https://pudge.explorer.nervos.org/transaction/0xee511bba5f9ea131a94e63edd33764cf8e48297ed006219e7193a004bb9550b6  

---

### Transaction Breakdown

#### Transaction 1 — CKB Transfer
- Consumed 1 input cell and created 2 output cells:
  - Payment (62 CKB)
  - Change
- Signed using `secp256k1`
- Verified via default lock script  
- Successfully committed on-chain  

#### Transaction 2 — Payment Data Storage
- Consumed outputs from Transaction 1 (Cell model in action)
- Created a new cell containing structured JSON data:

```json
{
  "type": "fiber-agent-payment",
  "agentId": "441507a4-aa0b-4c26-aab8-34ed14c8fbc7",
  "amount": "6200000000",
  "timestamp": 1774258989322,
  "description": "DCA purchase #1"
}