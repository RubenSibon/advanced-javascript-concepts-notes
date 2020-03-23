# Pillar 2: Prototypal Inheritance

Almost everything in JavaScript is an object. All objects inherit from other objects until all the way up to the **prototype chain** the base `Object`.

`__proto__` can be used to extend objects to protypal objects, but should never be used!

`.isPrototypeOf(Object)` checks if passed the object it is called upon (`this`) is a prototype of the passed in object.

`.hasOwnProperty`: checks if a given property is on the object it is called upon. There is, in other words, no need to go up the prototype chain.

Make one object inherit from another object:

```
const lizard = {
	strength: 10,
	health: 100,
	attack() {
		return this.strength;
	},
	battleCry() {
		return `Broaoa!`;
	},
}

const dragon = {
	strength: 50,
	health: 200,
};

dragon.__proto__ = lizard;
```

`lizard.isPrototypeOf(dragon) === true`

CodePen: https://codepen.io/RubenSibon/pen/XWbbaMG
