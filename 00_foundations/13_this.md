# `this`

Do you know what *this* is?

**this** is the object that the function is a property of.

`this` basically answers the question: **"what called me?"**

Global functions are a property of the global object. On the web that is `window`.

For methods, functions sitting on objects, *this* refers to those objects that they are a method of.

`this` then refers to what is left of the "." in method calls.

When calling `Person.sayName()` `this` refers to "Person".

When calling `helloWorld()` in the global lexical scope, `this` refers to the global scope such as the Window object in browsers. You could also have written `window.helloWorld()`.

## `this` and dynamic scope vs lexical scope

It's about the calling context (**dynamic scope**) and _NOT_ the lexical scope.

"In JavaScript our lexical scope (available data + variables where the function was defined) determines our available variables. Not where the function is called (dynamic scope)."

```
// Helper function
const isSingular = (number) => {
		return number === 0 || number === 1;
};

const Person = {
		name: null,
		age: null,
		sayName() {
			return this.name;
		},
		sayAge() {
			return this.age;
		},
		sayNameAndAge() {
				return `My name is ${this.sayName} and I am ${this.sayAge} year${isSingular(this.sayAge) ? "" : "s"} old.`;
		},
};

const ruben = { ...Person, name: "Ruben", age: 33 };
```
