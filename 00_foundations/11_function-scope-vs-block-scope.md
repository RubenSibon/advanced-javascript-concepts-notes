# Function scope vs Block scope

Originally JavaScript is only functionally scoped and not block scoped. This means that variables inside functions are private, but variables inside code blocks `{}` such as with if/else-statements are not scoped. Values in such blocks can be accessed.

Most languages do have block scoping.

Because JS was weird in that sense they introduced the `let` and `const` keywords in ECMAScript 6. Variables declared with these keywords are block scoped.
