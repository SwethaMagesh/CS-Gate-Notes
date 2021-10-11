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
#### Explanation of ACID
1. **Atomicity**
  - **Transaction Control Manager** takes care of it
  - All or Nothing rule
  - No transaction occurs partially
2. **Consistency**
  - DBMS and App programmer takes care of it
  - Database remains consistent before and after the transaction.
  - The integrity constraints are maintained.
3. **Isolation**
  - **Concurrency control manager** takes care of it
  - During execution, each transaction feels as if it is getting executed alone in the system.
  - System state after all the transactions is same as the state if the transactions were executed serially one after the other.
4. **Durability**
  - Recovery manager takes care of it
  - Ensures successful write to disk after transaction
  - Ensures changes are permanent even if there is failure

---
### Concurrency problems in transactions

#### Dirty Read
- Reading the data written by an uncommitted transaction is called as dirty read.
- Possiblity of rollback and inconsistency of database
- Not inconsistent always; problematic only when the uncommitted transaction fails and roll backs later due to some reason.

![image](https://user-images.githubusercontent.com/43994542/136761142-2920cd7d-dc12-43fd-83f6-56b5f5a7b289.png)

#### Unrepeatable Read
- Transaction gets to read unrepeated i.e. different values of the same variable in its different read operations even when it has not updated its value

![image](https://user-images.githubusercontent.com/43994542/136761620-58a51026-d3d0-4067-889a-d049886e16d6.png)
- _T2 wonders how the value of X got changed because according to it, it is running in isolation._


#### Lost Update 
- Multiple transactions occur concurrently; updates from one or more transactions get overwritten or lost
- This problem occurs whenever there is a write-write conflict.
- In write-write conflict, **there are two writes one by each transaction on the same data item without any read in the middle.**
![image](https://user-images.githubusercontent.com/43994542/136761966-08573de7-32e2-4601-b52a-d4d72de57198.png)
- _T1 writes the over written value of X in the database. Thus, update from T1 gets lost._
#### Phantom Read
- When a transaction reads from a variable once, and during the next read, the variable doesn't exist. 
![image](https://user-images.githubusercontent.com/43994542/136762726-b7058c80-6881-4726-9bc9-a019acea10d7.png)
- _T2 wonders who deleted the variable X because according to it, it is running in isolation._

- Concurrency Control Protocols help to prevent the occurrence of above problems and maintain the consistency of the database.
 
---

## **Schedules**

