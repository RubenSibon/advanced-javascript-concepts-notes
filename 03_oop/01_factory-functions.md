# Factory functions

Factory functions are functions that create objects with arguments passed into them. Each new object created this way can share properties and methods, but can also have it's own unique properties and methods.

```
function createElf(name, weapon) {
	return {
		name,
		weapon,
		attack() {
			return `${this.name} attacks with ${this.weapon}`;
		}
	};
}

const legolas = createElf("Legolas", "silver bow");
const marwin = createElf("Marwin", "dual swords");

console.log(legolas.attack());
console.log(marwin.attack());
```

Although above code is DRY there is a downside: for each new elf a new object is created and stored at a new address in memory. Each object has it's own properties and methods.

CodePen: https://codepen.io/RubenSibon/pen/QWbNqVB
