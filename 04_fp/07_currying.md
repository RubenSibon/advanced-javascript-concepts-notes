# Currying

Example of currying:

```
// Not curried:
const multiply = (a, b) => a * b;

// Curried
const curriedMultiply = a => b => a * b;


multiply(5, 3); // 15;
curriedMultiply(5)(3); // 15;
```

With currying functions have only one parameter can be be combined (**composed**) into new functions. You are basically creating functions on the fly.
