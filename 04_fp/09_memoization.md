# Memoization

A form of caching data: the returned values of functions are cached.

Example:
```
function memoizedAddTo80() {
	let cache = {};

	return function (n) {
		if (n in cache) {
			return cache[n];
		} else {
			cache[n] = n + 80;

			return cache[n];
		}
	}
}

const memoized = memoizedAddTo80();

// First call is calculated and the return is cached.
console.log("1", memoized(5));

// Second call retrieved from cache.
console.log("2", memoized(5));
```
