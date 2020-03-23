# bind() and currying

WIth `.bind()` you can extend any function through currying (passing function into functions).

```
function multiply(a, b) {
	return a * b;
}

let multiplyByTwo = multiply.bind(this, 2);
let multiplyByTen = multiply.bind(this, 10);

console.log(multiplyByTwo(4)); // 8
console.log(multiplyByTen(4)); // 40
```
