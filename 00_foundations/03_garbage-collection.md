# Garbage Collection

Only the data that is still useful to us remains in the Memory Heap to make sure to not use up all the memory available.

## False sense of security

Automatic garbage collection creates a false sense of safety. Programmers should think about how their programs affect the memory usage.

Memory leaks might still happen with automatic garbage collection. No system is perfect and garbage collectors can only do so much.

It's easy to create a memory leak:

```
let array = [];

for (let i = 0; i > 1; i++) {
	array.push(i-1);
}
```

Risky patterns that may create memory leaks:

- Global variables (keep sitting in memory and might get bigger and bigger)
- Event listeners (should be removed)
- setInterval (objects references inside intervals will never be cleared in memory because the interval runs forever)
