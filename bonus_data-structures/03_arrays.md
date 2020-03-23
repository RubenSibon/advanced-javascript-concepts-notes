# Arrays

## Static and dynamic arrays

**Static arrays** has memory allocated "statically", meaning that its lifetime is the entire run of the program. It cannot be allocated more or less memory and therefor static arrays may not get more data in them.

**Dynamic arrays** which are usually local variables in many programming languages can be allocated more memory as is needed on the memory heap.

JavaScript only knows dynamic variables and dynamic arrays.

## Pros and cons of array data structures:

+ Fast lookups (O(1))
+ Fash push/pop (O(1))
+ Ordered
+ Small memory footprint compared to many other data structures like hash tables

- Slow inserts*
- Slow deletes*
- Fixed size (if using **static array**)

(*) Due to shifting the items in the array.
