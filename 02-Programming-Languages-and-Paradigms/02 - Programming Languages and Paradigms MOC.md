# 02 — Programming Languages & Paradigms MOC

> ← Back to [[Software Engineering - Map of Content]]

How we express computation. The choice of language and paradigm shapes how you think about problems.

---

## [[Programming Paradigms]]

### Imperative Programming
- **Core Idea** — Sequences of statements that change program state
- **Procedural** — Functions/procedures as the organizing unit (C, Pascal)
- **Structured Programming** — Loops, conditionals, subroutines instead of goto
- **Key Concepts** — Variables, assignment, control flow, mutation

### Object-Oriented Programming (OOP)
- **Core Pillars** — Encapsulation, Inheritance, Polymorphism, Abstraction
- **Classes & Objects** — Blueprints and instances, constructors, methods
- **Inheritance** — Single vs multiple, interface inheritance, abstract classes
- **Polymorphism** — Subtype (runtime), parametric (generics), ad-hoc (overloading)
- **Composition over Inheritance** — Favoring has-a over is-a relationships
- **SOLID Principles** — See [[OOP and SOLID Principles]]
- **Languages** — Java, C#, Python, Ruby, C++, Kotlin, Swift

### Functional Programming
- **Core Principles** — Pure functions, immutability, declarative style
- **First-Class Functions** — Functions as values, higher-order functions
- **Key Operations** — Map, filter, reduce/fold, flatMap
- **Closures & Currying** — Partial application, function factories
- **Algebraic Data Types** — Sum types (enums/unions), product types (tuples/records)
- **Pattern Matching** — Destructuring, exhaustiveness checking
- **Monads & Functors** — Option/Maybe, Result/Either, IO monad, do-notation
- **Lazy Evaluation** — Thunks, infinite sequences, call-by-need
- **Referential Transparency** — Same input → same output, no side effects
- **Languages** — Haskell, Elixir, Clojure, OCaml, F#, Scala, Erlang

### Concurrent & Parallel Programming
- **Concurrency vs Parallelism** — Dealing with many things vs doing many things at once
- **Threads** — POSIX threads, thread pools, thread safety
- **Synchronization** — Mutexes, semaphores, monitors, condition variables
- **Deadlock & Livelock** — Prevention, avoidance, detection
- **Lock-Free Programming** — Compare-and-swap (CAS), atomic operations
- **Actor Model** — Isolated actors, message passing (Erlang, Akka)
- **CSP (Communicating Sequential Processes)** — Channels, goroutines (Go)
- **Async/Await** — Event loops, coroutines, futures/promises
- **Data Parallelism** — SIMD, GPU computing, MapReduce
- **Reactive Programming** — Streams, observables, backpressure (RxJS, Project Reactor)

### Logic Programming
- **Declarative Rules** — Facts and rules, inference engines
- **Unification** — Pattern matching on logic variables
- **Backtracking Search** — Prolog-style resolution
- **Applications** — Expert systems, constraint solving, Datalog

### Metaprogramming
- **Reflection** — Inspecting types/objects at runtime
- **Macros** — Compile-time code generation (Lisp, Rust, Elixir)
- **Code Generation** — Templates, source generators, AST manipulation
- **DSLs (Domain-Specific Languages)** — Internal vs external DSLs, fluent interfaces

---

## [[Type Systems]]

### Static vs Dynamic Typing
- **Static** — Types checked at compile time (Java, C++, Rust, Haskell, Go)
- **Dynamic** — Types checked at runtime (Python, JavaScript, Ruby, Clojure)
- **Gradual Typing** — Optional type annotations (TypeScript, Python with mypy)

### Strong vs Weak Typing
- **Strong** — No implicit type coercion (Python, Haskell)
- **Weak** — Implicit conversions allowed (JavaScript, C)

### Type Inference
- **Hindley-Milner** — Fully inferred types (Haskell, OCaml, Rust partially)
- **Local Inference** — `var`/`auto` keywords (Java, C++, Kotlin)
- **Bidirectional Type Checking** — Combining inference and checking

### Advanced Type Features
- **Generics / Parametric Polymorphism** — Type parameters, bounded types, variance (covariance, contravariance)
- **Algebraic Data Types** — Sum types (tagged unions), product types (structs/tuples)
- **Dependent Types** — Types that depend on values (Idris, Agda)
- **Phantom Types** — Unused type parameters for compile-time safety
- **Type Classes / Traits** — Ad-hoc polymorphism (Haskell type classes, Rust traits, Swift protocols)
- **Higher-Kinded Types** — Types that take type constructors as parameters
- **Refinement Types** — Types with predicates (e.g., positive integers)
- **Structural vs Nominal Typing** — Shape-based (TypeScript, Go interfaces) vs name-based (Java, C#)

---

## [[Language Implementation]]

### Compilation Pipeline
- **Lexing / Tokenization** — Source code → tokens
- **Parsing** — Tokens → Abstract Syntax Tree (AST)
- **Semantic Analysis** — Type checking, name resolution, scope analysis
- **Intermediate Representation (IR)** — SSA form, three-address code
- **Optimization** — Constant folding, dead code elimination, loop unrolling, inlining
- **Code Generation** — IR → machine code or bytecode

### Compilation Strategies
- **Ahead-of-Time (AOT)** — Compile before execution (C, C++, Rust, Go)
- **Just-in-Time (JIT)** — Compile at runtime based on hot paths (JVM HotSpot, V8, PyPy)
- **Interpretation** — Execute AST or bytecode directly (CPython, Ruby MRI)
- **Transpilation** — Source-to-source compilation (TypeScript → JavaScript, Babel)

### Runtime Systems
- **Virtual Machines** — JVM, CLR, BEAM (Erlang), WASM
- **Bytecode** — Platform-independent intermediate format
- **Foreign Function Interface (FFI)** — Calling C from other languages, interop
- **Runtime Linking** — Dynamic libraries, shared objects, DLL loading

### Parsing Techniques
- **Recursive Descent** — Hand-written, top-down
- **Parser Combinators** — Composable parsing functions
- **Parser Generators** — YACC, Bison, ANTLR, PEG grammars
- **Operator Precedence Parsing** — Pratt parsing

---

## [[Memory Models]]

### Stack vs Heap
- **Stack** — Fast, LIFO, automatic allocation, function call frames, limited size
- **Heap** — Dynamic allocation, manual or GC-managed, fragmentation concerns

### Garbage Collection (GC)
- **Mark-and-Sweep** — Trace reachable objects, free unreachable
- **Generational GC** — Young/old generations, minor/major collections (JVM, .NET)
- **Concurrent GC** — G1, ZGC, Shenandoah — minimize pause times
- **Reference Counting** — Increment/decrement counts (Python, Swift, Objective-C)
- **Cycle Detection** — Handling circular references in ref-counted systems
- **GC Tuning** — Heap sizing, pause time goals, throughput tuning

### Manual Memory Management
- **malloc/free** — C-style explicit allocation and deallocation
- **RAII (Resource Acquisition Is Initialization)** — C++ destructors, deterministic cleanup
- **Smart Pointers** — unique_ptr, shared_ptr, weak_ptr (C++)
- **Common Bugs** — Use-after-free, double-free, memory leaks, buffer overflows, dangling pointers

### Ownership & Borrowing (Rust Model)
- **Ownership Rules** — Each value has one owner, ownership can be moved
- **Borrowing** — Immutable (&T) and mutable (&mut T) references
- **Lifetimes** — Compile-time tracking of reference validity
- **Zero-Cost Abstractions** — Safety without runtime overhead

### Memory Layout
- **Alignment & Padding** — Struct layout, cache line alignment
- **Endianness** — Big-endian vs little-endian byte ordering
- **Virtual Memory** — Pages, page tables, TLB, memory-mapped files
- **Cache Hierarchy** — L1/L2/L3, cache lines, spatial/temporal locality (impacts [[Performance Engineering]])

---

#programming-languages #paradigms #type-systems
