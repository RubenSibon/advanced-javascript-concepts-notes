# Inside the Engine

## Concepts

- [**Parser**](https://www.techopedia.com/definition/3854/parser)
- [**Interpreter**](https://www.techopedia.com/definition/7793/interpreter)
- [**Compiler**](https://www.techopedia.com/definition/3912/compiler)
- [**Abstract Syntax Tree (AST)**](https://en.wikipedia.org/wiki/Abstract_syntax_tree)
- [**Call stack**](https://developer.mozilla.org/en-US/docs/Glossary/Call_Stack)
- [**Memory heap**](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Memory_Management)

## First engine

The first engine, named [SpiderMonkey](https://spidermonkey.dev/), was built by the creator of JavaScript, [Brandon Eick](https://en.wikipedia.org/wiki/Brendan_Eich). SpiderMonkey is used by [Mozilla Firefox](https://www.mozilla.org/) to this day.

## Flow van de JS-engine

```
Parser => AST => Interpreter (1) => Bytecode (01010110011) (2) => Profiler ==> Compiler ==> Optimized code (100110011010)
```

**Interpreter**: line by line; from left to right; from top to bottom.

**Compiler**: code optimizations: first look at the code for optimizations.

[**JIT (Just In Time) Compiler**](https://en.wikipedia.org/wiki/Just-in-time_compilation): combination of an interpreter and a compiler.
