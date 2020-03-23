# Four ways to bind `this`

```
// (1) With the `new` keyword
function Person(name, age) {
  this.name = name;
  this.age = age;
  this.sayHi = function () {
    return `Hi, I'm ${this.name}.`;
  };
}

const dave = new Person("Dave", 24);

console.log(dave.sayHi());

// (2) Implicit binding
const charlotte = {
  name: "Charlotte",
  age: 35,
  sayHi() {
    return `Hi, I'm ${this.name}.`;
  },
};

console.log(charlotte.sayHi());

// (3) Explicit binding
const karin = {
  name: "Karin",
  age: 48,
  
  // Below function with timeout returns "2"... lol?
  sayHi: function () {
    return `Hi, I'm ${this.setTimeout(() => this.name, 500)}.`;
  }.bind(window),
};

console.log(karin.sayHi());

// (4) Arrow function
const aris = {
  name: "Aris",
  age: 59,
  sayHi: function () {
    var inner = () => {
      return `Hi, I'm ${this.name}.`;
    };
    
    return inner();
  },
};

console.log(aris.sayHi());
```
