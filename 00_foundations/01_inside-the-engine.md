# Inside the Engine

## Concepten

**parser**,
**interpreter**,
**compiler**,
**abstract syntax tree (AST)**,
**call stack**,
**memory heap**

## First engine

Eerste engine, genaamd SpiderMonkey, werd gebouwd door de bedenker van JavaScript, Brandon Eick. SpiderMonkey wordt tot op de dag van vandaag gebruikt door Mozilla Firefox.

## Flow van de JS-engine:

Parser => AST => Interpreter
	(1) => Bytecode (01010110011)
	(2) => Profiler ==> Compiler ==> Optimized code (100110011010)

**Interpreter**: regel voor regel; van links naar rechts en van boven naar beneden

**Compiler**: code optimizations: kijkt eerst naar de code voor optimalisaties

**JIT (Just In Time) Compiler**: combinatie van interpreter en een compiler.
