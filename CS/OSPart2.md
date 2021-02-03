## Memory management
- Paging 
- Segmentation
- Paging in Segmentation

---
### Note
- Paging and Virtual memory (extended paging)
- Without virtual memory, all pages in main memory and so no page faults

---
### Page replacement policy
- FIFO - random 
- Optimal
- LRU 
- Belady's anamaly: Random algorithms like FIFO (not LRU and OPTIMAL)
    - ***When no of allotted frames increase, general assumption is that the page fault rate reduces. But it increases ironically (that's why anamaly)***
---
#### Thrashing
- *High degree of multiprogramming* - CPU utilisation is low compared to high paging activity
- ***Reasons***
    1. High degree of MP
    1. Less main memory space
    1. Page replacement policy may be bad (like FIFO)
- ***Solution*** - Reduce degree of multiprogramming or Increase memory 
---
### Segmentation
- Variable partition
- Preserves user view(programmer's view)
    - *Paging doesn't preserve user view (split without asking user)*
- 8086 architecture `(CS, DS, ES, SS)`
- Nowadays, compilers and assemblers take care of segmentation completely.
- `<s,d> - s is segment number and d is offset.`
- If d is above the segment size, the request is denied. Trap to OS
- ***Segment table:*** consists of BASE address and Size (limit) for each segment
- Then *a comparator* compares, the offset and limit and only if valid generates the *PHYSICAL address*
---
### Paging on Segment
- 2 kinds 
    - Paging on segment table
    - Paging on segment 
- CPU -> Segment table -> Page Table -> Word
- In segment table, we can apply paging to each segment
    - ***No external fragmentation*** 
    - Overcomes external fragmentation in the segementation concept
- `|s|p|d1|` where 
    - `s is segment number(indexed from segment table)`
    - `p is page number for that particular segment`
    - `d1 is the offset(word) within the page.`
-  Most Complicated architecture:
    - `|s|d|`
    - `s is divided as |m|d2|`
    - `d is divided as |p|d1|`
- m is page table for the segment table and p is page table for the segment
    - ![image](https://user-images.githubusercontent.com/43994542/106783583-74180180-6671-11eb-8207-445b1fd7b3ac.png)

---
## File system
- DBA - Database admin
- DEntry - Directory Entry
### File allocation
1. Contiguous
    - Advantage: Fast random access from base address
    - Disadvantage: 
        1. Internal and External fragmentation
        1. Cannot increase file size (flexiblity) ie. *it depends on the other consecutive locations*
1. Linked
    1. Disadv: 
        - when link breaks due to malware or something, the next part is completely unaccessible
        - Address is stored in each block which wastes time.
        - ![image](https://user-images.githubusercontent.com/43994542/106784247-22bc4200-6672-11eb-8a20-b8dde0ca25ca.png)

1. Indexed -> INODE structure  
    - One block just to store the DBA(s) of the file
    - Every file has index block
    - If file is large then, one block is not sufficient to store the DBAs for the file
    - If file is too small, waste of using one disk block for just storing DBAs



