# Promises

Promises are handy for asynchronous (non-blocking) code like

- making API calls,
- grabbing data from a database, or
- optimizing an image.

## Definition

A Promise is an **object** that may return a single value in the future that is either **resolved** or **rejected** (and a reason why it was rejected).

A promise may be in one of three possible states: **fulfilled**, **rejected** or **pending**.

## Combine multiple Promises

```
const promise = new Promise((resolve, reject) => {
	setTimeout(resolve, 0, 'Resolved after 0 seconds.');
});

const promise = new Promise((resolve, reject) => {
	setTimeout(resolve, 2000, 'Resolved after 2 seconds.');
});

const promise = new Promise((resolve, reject) => {
	setTimeout(resolve, 5000, 'Resolved after 5 seconds.');
});

Promise.all([promise, promise2, promise3]).then(values => console.log(values));

// Result: Array with the return values from all promises after 5 seconds.
// Due to `.all()` we have to wait for the last promise to resolve.
```

## Fetch data from JSON's (API calls)

```
const urls = [
	"https://jsonplaceholder.typicode.com/users",
	"https://jsonplaceholder.typicode.com/posts",
	"https://jsonplaceholder.typicode.com/albums",
];

Promise.all(urls.map(url => {
	return fetch(url).then(resp => resp.json())
})).then(results => {
	console.log(results[0]);
	console.log(results[1]);
	console.log(results[2]);
}).catch(() => console.error(error));
```
