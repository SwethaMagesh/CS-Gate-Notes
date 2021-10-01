## Points
### Kernel
- A program which is a part of OS **running at all times**
- Apart from kernel, some system process or daemons and application programs run
### Device controller
- Memory is connected to CPU and other device controllers, these are in turn connected to devices (I/O devices)
### Firmware 
- Program burnt into **ROM or EEPROM** (Eg. Bootstrap or program in Embedded system)
- Bootstrap does:
    - load initial register and memory values
    - loads OS into main memory
    - loads and starts the kernel and other processes
### Multiprogramming and Timesharing
- Single process runs at a time
#### Multiprogramming 
- Many programs reside in memory so that **CPU is never idle**
#### Timesharing 
- A concept based on Multiprogramming
- Many programs are **context switched so fast that user gets illusion** that processes run concurrently
----------
### System Call
- Acts as interface to services provided by OS
- Used to **access hardware**
- Usually API or Runtime support library is used to implement system call
- *EG: device management, file handling, process management*
- Goes through user space to kernel space
---
## Process Management
### Program and Process
- Program is a file - passive entity residing on disk etc
- Process is a program in execution.
    - It has **text(code), data(variables), stack and heap** associated. 
    - It has **program counter PC, and register contents**
    - It has program plus a state defined by the above
- A single program may have many instance of processes running at a time each having different variable values.
### Process States
- *New* - when created
- *Terminate* - when finished
- *Ready* - Waiting for scheduler to dispatch
- *Waiting* - Waiting for some I/O job; After job finishes, goes to ready state
- *Running* - CPU is assigned
### Process Control Block - PCB
- Details about processes
- Like *program counter, register, scheduling info, I/O, files open, address space*
- When context switched, process PCB state is stored, and on resuming, the state is retreived.
### Process Creation
- `init` is parent of all process
- Child process can either 
    - use parent's resource
    - get resource allocated from OS
- Child process can  
    - execute same code as parent (address space)
    - execute loaded code => `exec() system call`
- A parent process can execute
    - concurrently with child
    - Wait till one or all children terminate => `wait()` provides status of child to parent 
- *Note: fork() returns 0 for a child process, so that it doesn't create a new process agaian while executing the same code*
- Child process can share code and data after `fork()` and then split using the `exec()` call when needed. 
- `exit()` is system call to terminate. Called either directly or indirectly ( *return statement in main() function*)
- Child process terminates if 
    - *task is no longer needed*
    - *excess resource usage*
    - *if parent terminates* => In some OS, whenever parent terminates, child cannet exist. This is called ***cascading termination.***
#### Zombie and orphan processes
- Even if a process is completed, its parent process might not issue `wait()` immediately. 
Such process - `Zombie process`
    - Till parent calls `wait()`, the entry remains in process table 
- If parent terminates without `wait()` statement, child has no parent. It is called `orphan process`
    - By default, they become the child of the `init process`. `init` periodically issues `wait()` to release these processes
---
### IPC - Interprocess Communication
- Cooperating process - need data from other process 
- Independent process - no need to share data from other process
- Types : ***Shared Memory, Message Passing*** 
- ***Shared Memory:*** 
    - Fast 
    - No kernel intervention except to establish
    - Cache coherence problem
- ***Message Passing:*** 
    - Slow
    - Kernel intervention needed for each message
    - Especially Distributed systems
    - Higher performance especially multiprocessor

### Thread
- Basic unit of CPU utilisation
- **Different subtasks** of a single process is assigned to a separate thread.
- Useful in multicore processors where each thread is assigned to a core
- PCB is expanded to accomodate the thread info
- ***Note: Threads share code, data and files along with heap. But, each thread has its own copy of stack and register values like program counter***
- ***Advantagae compared to process creation:*** Process creation is slow; data has to communicated. *Eg: Web server creates new thread to service client and continues to listen*
#### Benefits
- Responsiveness
- Economy
- Resource Sharing
- Scalability
#### Parallelism vs Concurrency
- Even in single processor systems, processes run concurrently, but not at same time
- But in parallelism, processes run simultaneously, like on multiple cores of processor.
#### Kernel Threads and User Threads
##### Models
- ***Many-One:***  
    - Many user threads and a single kernel thread
    - Blocking system call blocks the process
    - No concurrency - cannot utilise multicore 
- ***One-One:*** 
    - Each user thread creates kernel thread 
    - Overhead is more for creating kernel threads
    - True concurrency is achieved; even if blocked, process continues
- ***Many-Many:*** 
    - User threads>= Kernel threads
    - Concurrency is achieved
- **Two level:**
    - Hybrid of Many-Many and One-One

---
### Scheduling
#### Long Term Scheduler
- Also called Job scheduler
- Used to change degree of Multiprogramming
- From disk to main memory
#### Short Term Scheduler
- Used very frequently. Must be fast
- Also called CPU scheduling
- In some systems, Short term scheduler does the job of the long term scheduler also.
#### Middle Term Scheduler
- Semi executed process are swapped to disk
- This swapping in and out done by middle term scheduler
- This may or may not be present

