# OOP and Inheritance

With the `extend` and `super` keywords you can extend classes created with the `class` keyword.

It's the core of the Classical Object Oriented paradigm. It adds inheritance. In the case of JavaScript it creates a Prototypal Inhertiance.

```
// Base Character class
class Character {
  constructor (name, allegiance, weapon) {
    this.name = name;
    this.allegiance = allegiance;
    this.weapon = weapon;
  }
  
  attack () {
    return `${this.name} attacks with ${this.weapon ? this.weapon : "fists"}.`;
  }
  
  battleCry () {
    return `${this.name}: "For ${this.allegiance}! Charge!!"`;
  }
}

// Elf class that exends the Character class
class Elf extends Character {
  constructor (name, allegiance, weapon, type) {
    super (name, allegiance, weapon);
    
    this.type = type;
  }
}

const doby = new Elf("Doby", "House of Fallstar", "Aspen Bow", "elf");

console.log(doby.battleCry());
console.log(doby.attack());
```

CodePen: https://codepen.io/RubenSibon/pen/KKpzyjV