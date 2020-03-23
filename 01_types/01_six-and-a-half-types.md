# Six and a half types ...and "function"

There are 6 data types in JavaScript... or actually 7... wait, no! There are six! Huh!? Whaaa!

## Primitive types

Represent single values. Easy and simply.

1. `number` like 5

2. `string` like "Hello world!"

3. `undefined` when something lacks a definition. Variables that are hoisted or defined without assignment are assigned "undefined".

4. `null` doesn't actually exist as a type, but is an "object". This is one of the quirks of JS.

5. `symbol` for unique object properties


##  Non-primitive types

Can combine multiple types. Do not actually contain the value directly, but is a reference (pointer) to some place in memory.

6. `object` for objects, arrays, functions and... null

7. `function` is not actually a real type because it is actually an object.

- Arrays are `object`s

So up to number five it all makes sense, but then it gets weird. `null` is an object while it shouldn't be. Functions have the type of `function` while they should be `object`s.
