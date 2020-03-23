# Compose & Pipe

## Compose

**Composition** is the idea that any kind of data transformation should be obvious.

Or: composability is a system design principle that deals with the relationship between components.

```
const compose = (f, g) => (data) => f(g(data));
const multiplyBy3 = (num) => num * 3;
const multiplyBy3AndAbsolute = compose(multiplyBy3, Math.abs());

console.log(multiplyBy3AndAbsolute(-50));
```

## Pipe

"Performs left-to-right function composition. The leftmost function may have any arity*; the remaining functions must be unary."

It is very similar to compose, but the direction is left-to-right.

```
const pipe = (f, g) => (data) => g(f(data));
const multiplyBy3 = (num) => num * 3;
const multiplyBy3AndAbsolute = pipe(multiplyBy3, Math.abs());

console.log(multiplyBy3AndAbsolute(-50));
```

## *: Arity

The number of functions that are conposed or piped together.

CodePen: https://codepen.io/RubenSibon/pen/WNvGLVr
