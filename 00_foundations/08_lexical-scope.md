# Lexical scope

Lexical scope is the **available data** (execution context and memory heap?) + **variables where the function was defined** (lexical environment).

This determines our available variables and _not_ where the function is called (dynamic scope).

If a function is written inside another function you have a function lexical environment. The outer function is the **function lexical environment** for the inner function.
