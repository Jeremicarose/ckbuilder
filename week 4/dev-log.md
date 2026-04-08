# Builder Track Weekly Report — Week 4  
**Name:** Jeremic  
**Week Ending:** 30 March - 5 April  

---

## Courses Completed

### Intermediate Practical Exercises
- Sending CKBytes using `ckb-cli`  
- Verifying accounts and addresses on Devnet  
- Retrieving transaction details using RPC  
- Inspecting transaction inputs and outputs  
- Understanding transaction fees and change handling  

---

## Key Learnings

### Transaction as State Transition
- Transactions on CKB do not update balances directly  
- Instead:
  - Existing Cells are consumed (inputs)  
  - New Cells are created (outputs)  

**Insight:**  
State is not modified — it is reconstructed through new Cell creation  

---

### Inputs Originate from Previous Outputs
- Each input references:
  - A previous transaction output  
- Identified using:
  - `tx_hash + index` (Out Point)  

**Insight:**  
All CKBytes are traceable, ensuring transparency and accountability  

---

### UTXO Model (Cell Model on CKB)
- CKB uses a model similar to Bitcoin:
  - Unspent Transaction Outputs (UTXOs)  
- A Cell can only be used once:
  - After consumption → it becomes spent  

**Insight:**  
Prevents double-spending through one-time use of Cells  

---

### Transaction Structure

A valid transaction includes:
- Inputs: Cells being consumed  
- Outputs: Newly created Cells  
- Outputs Data: Capacity or stored data  
- Witnesses: Signatures for authorization  

**Insight:**  
Developers must explicitly define complete state transitions  

---

### Change Handling
- Input capacity may exceed transfer amount  
- Remaining capacity must be:
  - Returned as a new output Cell to the sender  

**Insight:**  
CKB requires explicit change outputs, similar to physical cash transactions  

---

### Transaction Fees
- Fee is calculated as:
  - `Total Inputs - Total Outputs`  

**Insight:**  
Fees are implicitly defined and serve as incentives for miners  

---

## Practical Progress

### Devnet Account Verification
- Used `ckb-cli account list` to:
  - View available accounts  
  - Identify devnet/testnet addresses  

**Outcome:**  
- Confirmed access to pre-funded accounts for testing  

---

### CKByte Transfer Execution

Performed transfer using:

- `wallet transfer` command with:
  - Source account  
  - Destination address  
  - Specified capacity  

**Outcome:**  
- Successfully executed transaction  
- Received transaction hash for reference  

---

### Transaction Retrieval & Analysis

Used:

- `rpc get_transaction --hash <TRANSACTION_ID>`  

Analyzed:
- Inputs (source of funds)  
- Outputs (receiver and change)  

**Outcome:**  
- Verified correct transfer and structure of transaction  

---

### Input–Output Relationship Exploration

- Traced how outputs from previous transactions become inputs  
- Observed chaining of transactions across the network  

**Outcome:**  
- Developed clear understanding of transaction flow and lineage  

---

### Fee and Capacity Validation

- Compared total input capacity with outputs  

**Outcome:**  
- Identified transaction fee as the difference  
- Confirmed correct accounting of CKBytes  

---

## Challenges & Observations

### Understanding the UTXO Model
- Initially difficult to shift from:
  - Account-based balance thinking  
- Required adapting to:
  - Cell-based tracking  

**Observation:**  
Thinking in terms of discrete value units (Cells) improves clarity  

---

### CLI Command Precision
- Commands required exact syntax  
- Minor errors caused failed executions  

**Observation:**  
CLI tools enforce discipline and deeper system understanding  

---

### Interpreting RPC Output
- Transaction data is detailed and complex  

**Observation:**  
Focusing on key fields (inputs and outputs) simplifies analysis  

---

### Manual Transaction Logic
- Developer must handle:
  - Inputs  
  - Outputs  
  - Change  
  - Fees  

**Observation:**  
CKB provides flexibility but shifts responsibility to the developer  

---