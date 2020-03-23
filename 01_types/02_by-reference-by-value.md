# Pass by reference vs pass by value

## Passed by value

Primitives are **passed by value**.

There is no link back to memory, but bascially you are dealing with a copy of the original. Changing these values does not affect the original, but the copy.

## Passed by reference

Objects are **passed by reference**.

When objects are passed into a function they still point to the original place in memory. Making changes to the object that are passed into functions changes the original.

## Cloning objects

How can we create copies of objects and not references?

### Shallow cloning

Clone one object, but not child objects.

```
const obj = {
	a: 1,
	b: 2,
	c: {
		deep: "Try and copy me"
	}
};

let clone1 = Object.assign({}, obj);
let clone2 = { ...obj };
```

### Deep cloning

Clone an object and all objects within it.

Below is not a good idea generally, because with massive objects it can take a long time and increased memory consumption. There are better ways of solve problems around objects passed by reference.

```
const obj = {
	a: 1,
	b: 2,
	c: {
		deep: "Try and copy me"
	}
};

let deepClone = JSON.parse(JSON.stringify(obj)); 
```
