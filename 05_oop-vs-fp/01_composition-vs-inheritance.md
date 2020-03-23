# Composition vs Inhertance

Nuances:

- With **FP** you can use **(prototypal) inheritance**, but the focus tends to be more on **composition**.
- In **OOP** you can use **composition**, but the focus is more on **(classical) inheritance**.

## Problems with OOP

### Tight coupling

OOP has the **tight coupling** problem: making a small change in a class has a rippling effect to all subclasses and objects. You can easily break things "downstream".

Tight coupling can also be seen as a benefit: somtimes you want everything to be affected because your code stays DRY and you only have to work in one "class" object. The direction and flow of data and methods is immediatly clear.

### Fragile Base Class Problem

The base class should be well tought out and well structured from the beginning. If it is not, many subsequent changes will certainly break things (breaking API, legacy code breaking).

### Hierarchy

- Extending classes gives you a hierarchy that may not make semantic sense.
- Lower level classes inherit all the garbage of higher level classes: this is called the Gorilla/Banana-problem: "You only wanted the banana, but you end up getting a gorilla holding a banana en the entire jungle".
- Tight coupling creates a lot of problems with deep hierarchies.

## Mixture between OOP and FP

Create objects with only properties, but not methods. The methods are composed into the constructed objects from the base classes.
