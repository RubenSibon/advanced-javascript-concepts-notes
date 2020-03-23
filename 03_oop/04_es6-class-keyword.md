# ES6 `class` keyword

```
// "Class" for Pseudo-Classical Inheritance
class Elf {
  constructor(name, kingdom, weapon) {
    this.name = name;
    this.kingdom = kingdom;
    this.weapon = weapon; 
  }

  // Do not add methods inside the constructor because that
  // gets run everytime a new object is instantiated.
  attack() {
      return `${this.name} attacks with ${this.weapon}.`;
  };

  battleCry() {
    return `${this.name}: "For ${this.kingdom}!"`;
  }
}

// Instantiate new objects.
const legolas = new Elf("Legolas", "Dark Woods", "silver bow");
const arwen = new Elf("Arwen", "Ravendale", "moon lance");

// Is legolas an istance of Elf?
console.log(`Is legolas an istance of Elf? ${legolas instanceof Elf}`);

console.log(legolas.battleCry());
console.log(legolas.attack());

console.log(arwen.battleCry());
console.log(arwen.attack());
```

CodePen: https://codepen.io/RubenSibon/pen/WNvwXom