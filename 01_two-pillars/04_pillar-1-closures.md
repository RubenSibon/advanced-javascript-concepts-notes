# Pillar 1: Closures

Variables in the **variable environment** of an **execution context** of a **higher order function**, i.e. a function that returns a function, are stored in a special box, "**the closure**". These variables are **not collected** by the **garbage collector**.

That all this can happen is thanks to the concept of the **lexical environment** which is checked by the JIT Compiler before executing any code. It sees that there are variables in functions bodies (soon to be execution contexts) that will be referenced later by "lower order" functions.

## Closures are sometimes referred to as "lexical scoping"

**lexical** = where the code is written.
**scope** = what variables the JIT compiler/runtime has access to.

In execution contexts you do not only have access to variables higher in the calling context, but also what is stored in the memory heap through closures.

**Lexical environment === [[scope]]**

Where we write the function matters. Not where we call/invoke the function.

CodePen: https://codepen.io/RubenSibon/pen/vYOOZRq
