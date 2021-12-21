# Call stack & Memory Heap

## Memory heap

Value storage (functions, variables) in a prepared space in the computers [working memory (RAM)](https://en.wikipedia.org/wiki/Random-access_memory).

## Call stack

In an execution context, called functions get added on top of the [call stack](https://developer.mozilla.org/en-US/docs/Glossary/Call_Stack). Once the interpreter leaves the function, through a return or otherwise, the function reference gets popped of the call stack.

The values and functions that are in the memory heap are referenced in the call stack.

There is only one call stack, i.e. JavaScript is "single threaded" and "synchronous".

A new thread creates a new call stack.

## Stack Overflow

If the stack takes up more space than it had assigned to it, it results in a "stack overflow" error.

Functions calling themselves or functions being called in a never ending loop can cause a stack overflow.

The error message "maximum stack size reached" indicates that a stack overflow has occurred.
