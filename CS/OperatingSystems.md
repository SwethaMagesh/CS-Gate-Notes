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

### Thread
- **Different subtasks** of a single process is assigned to a separate thread.
- Useful in multicore processors where each thread is assigned to a core
- PCB is expanded to accomodate the thread info
- ***Note: Threads share code, data and files along with heap. But stack and register values like program counter vary between threads***
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

