# `Object.create()`

`Object.create()` creates a link between two objects. It creates a prototype chain: (`derivedObject.__proto__ === originObject`)

```
// Factory function using Object.create() for efficient memory usage.
const elfMethods = {
  attack() {
    return `${this.name} attacks with ${this.weapon}.`;
  },
  battleCry() {
    return `${this.name}: "For ${this.kingdom}!"`;
  },
};

// The factory function.
function createElf(name, kingdom, weapon) {
  let newElf = Object.create(elfMethods);
  
  newElf.name = name;
  newElf.kingdom = kingdom;
  newElf.weapon = weapon;
  
  return newElf;
}

const legolas = createElf("Legolas", "Dark Woods", "silver bow");
const arwen = createElf("Arwen", "Ravendale", "moon lance");

console.log(legolas.battleCry());
console.log(legolas.attack());
console.log(arwen.battleCry());
console.log(arwen.attack());
```
