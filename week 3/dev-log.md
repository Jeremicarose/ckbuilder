# Builder Track Weekly Report — Week 3  
**Name:** Jeremic  
**Week Ending:** 23 - 29 March  

---

## Courses Completed

### Beginner Practical Exercises
- Transfer CKB using Devnet environment  
- Store structured data in Cells  
- Issue custom tokens using xUDT  
- Query and inspect token Cells  
- Transfer tokens between accounts  

---

## Key Learnings

### Tokens as Type Script Cells
- Custom tokens on CKB are implemented using **Type Scripts (xUDT)**  
- Each token is uniquely identified by:
  - `args = issuer_lock_script_hash + optional data`

- Token amount is stored in:
  - `outputs_data` (not in the script itself)

**Insight:**  
Tokens are not balances stored in contracts, but **data inside Cells governed by scripts**

---

### Ownership = Lock Script
- Token ownership is determined by the **Lock Script of the Cell**
- Transferring tokens involves:
  - Consuming input Cells  
  - Recreating output Cells with a new Lock Script  

**Insight:**  
Ownership is not “updated” — it is **reassigned via new Cells**

---

### Cell-Based Accounting Model
- Balance is not stored as a single number  
- Instead, it is derived from:
  - The sum of all live Cells matching a Type Script + Lock Script  

**Insight:**  
CKB requires reconstructing state from distributed Cells rather than querying a central balance

---

### Transaction Construction Flow

A valid transaction includes:
- Inputs: Cells being consumed  
- Outputs: Newly created Cells  
- Outputs Data: Token amount or custom data  
- Witnesses: Signatures  
- CellDeps: Script references  

**Insight:**  
Developers must explicitly construct full state transitions, unlike account-based models

---

### Change Handling (Critical Concept)
- When transferring tokens:
  - Input Cells may contain more tokens than required  
- The remaining amount must be:
  - Returned to the sender as a new Cell  

**Insight:**  
CKB requires explicit “change outputs,” similar to UTXO in Bitcoin

---

## Practical Progress

### Devnet Setup & Interaction
- Started local blockchain using OffCKB  
- Retrieved pre-funded accounts and private keys  
- Executed transactions in isolated development environment  

---

### Token Issuance (xUDT)

Implemented token creation logic:

- Constructed Type Script using:
  - Issuer Lock Script Hash  
- Created output Cell with:
  - Type Script (xUDT)  
  - Token amount in `outputs_data`  

Successfully broadcast transaction and received transaction hash  

---

### Token Querying

Implemented token discovery:

- Queried live Cells using:
  - `findCellsByType(typeScript)`  
- Collected all Cells associated with token  

**Outcome:**  
- Identified token holders via Lock Scripts  
- Verified token distribution on-chain  

---

### Token Transfer

Executed token transfer logic:

- Collected sender’s token Cells  
- Constructed transaction:
  - Output to receiver (new Lock Script)  
  - Change output (if necessary)  

- Included:
  - Script dependencies (xUDT)  
  - Capacity completion  
  - Transaction fee handling  

**Outcome:**  
- Successfully transferred tokens between accounts  
- Verified ownership change via updated Lock Scripts  

---

### Application Execution

- Ran local dApp using:
  - `npm install && NETWORK=devnet npm start`  
- Interacted with frontend at `http://localhost:1234`  
- Tested token issuance and transfers through UI  

---

## Challenges & Observations

### Mental Model Shift (Reinforced)
- No global token balance  
- No contract storage  
- Everything is:
  - Cell creation  
  - Cell consumption  

---

### Explicit Transaction Complexity
- Required to manually handle:
  - Inputs  
  - Change  
  - Fees  
  - Script dependencies  

**Observation:**  
CKB provides flexibility at the cost of developer responsibility  

---

### Script Argument Design
- xUDT uniqueness depends on:
  - Lock Script hash  
- Placeholder (`00000000`) introduces extensibility  

**Observation:**  
Future token standards (xUDT extensions) can introduce advanced logic through args  

---
