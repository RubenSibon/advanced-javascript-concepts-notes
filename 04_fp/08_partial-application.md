# Partial application

Like currying the aim is to have less parameters: some parameters are passed in initially, but are stored with closures for later use.

```
const multiply = (a, b, c) => a * b * c;
const partialMultiplyBy5 = multiply.bind(null, 5);

partialMultiplyBy5(4, 10); // 200
```
