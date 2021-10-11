- Refer GATE VIDYALAY [LINK](https://www.gatevidyalay.com/acid-properties/)
## Transaction
- Transaction is a set of operations which are all logically related
### Main operations:
- Read 
- Write
- READ - read from DB into buffer in main memory
- WRITE - write from buffer to DB

---
### States of transaction
- **Active state**
  - As long as instructions in transactions are executed.
  - Now changes are in buffer in main memory
- **Partially committed state**
  - After last instruction of the transaction
  - Still stored in buffer of main memory
- **Committed state**
  - Successfully stored in DB
  - NOT possible to rollback now
  - Only possible : Another transaction to undo the effects of transaction
  - New consistent state
- **Failed state**
  - Impossible to continue execution
  - Inconsistent state (half of transaction changes in main memory)
- **Aborted state**
  - Changes made by a failed transaction are undone
  - Now the state is as if the transaction never took place
- **Terminated state**
  - Last state in lifecycle of transaction

![image](https://www.gatevidyalay.com/wp-content/uploads/2018/05/Transaction-States-in-DBMS.png)

### ACID PROPERTIES
- **ACID**
- A - _Atomicity_
- C - _Consistency_
- I - _Isolation_
- D - _Durability_

---
**Explanation of ACID**
1. Atomicity
  - **Transaction Control Manager** takes care of it
  - All or Nothing rule
  - No transaction occurs partially
2. Consistency
  - DBMS and App programmer takes care of it
  - Database remains consistent before and after the transaction.
  - The integrity constraints are maintained.
3. Isolation
  - **Concurrency control manager** takes care of it
  - During execution, each transaction feels as if it is getting executed alone in the system.
  - System state after all the transactions is same as the state if the transactions were executed serially one after the other.
4. Durability
  - Recovery manager takes care of it
  - Ensures successful write to disk after transaction
  - Ensures changes are permanent even if there is failure

---
### Concurrency problems in transactions



---

## **Schedules**

