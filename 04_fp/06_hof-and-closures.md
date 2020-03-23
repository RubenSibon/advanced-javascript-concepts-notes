# HOF & Closures

Example of higher order function:

```
const hof = (fn) => fn(5);
hof(function a(x) { return x });
```

Functions as first class citizens can be passed around and returned by functions.

```
const closureFunction = function() {
	let count = 0;

	return function increment() {
		count++;

		return count;
	}
}

const incrementFn = closureFunction();

incrementFn();
```
