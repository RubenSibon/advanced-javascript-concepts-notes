# Callstack & Memory Heap

## Memory heap

Opslag voor waardes (functions, variables) in een voorbereide ruimte in het werkgeheugen (RAM).

## Callstack

In an execution context called functions get added on top of the callstack. Once the interpreter leaves the function through a return or otherwise the function reference gets popped of the callstack.

The values and functions that are in the memory heap are referenced in the callstack.

There is only one callstack, i.e. "single threaded" and "synchronous" JS 

A new thread creates a new callstack

## Stack Overflow

Functions calling themselves or functions being called in a never ending loop.

These days the error "maximum stack size reached"
