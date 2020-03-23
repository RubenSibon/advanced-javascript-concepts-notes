# Scope chain

From an **execution context** you have access to contexts higher in the **scope chain** up to the **global scope**.

**Undefined** is a type in JavaScript. It means a variable has been declared and exists in the scope (can be found up the scope chain), but there is no value assigned (or the value assigned is *undefined*).

`[[scope]]` is an built-in object sitting on function calls as part of the prototype.
