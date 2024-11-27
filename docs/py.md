# Notes on Python

Python is a high-level, dynamically and strongly typed, garbage-collected, general-purpose programming language. It supports multiple programming paradigms, including structured (particularly procedural), object-oriented programming, functional programming and aspect-oriented programming (including metaprogramming and metaobjects). It is often described as a "batteries included" language due to its comprehensive standard library.

Python uses dynamic typing and a combination of reference counting and a cycle-detecting garbage collector for memory management. It uses dynamic name resolution (late binding), which binds method and variable names during program execution.

Its design offers some support for functional programming in the Lisp tradition. It has `filter`, `map` and `reduce` functions; list comprehensions, dictionaries, sets, and generator expressions. The standard library has two modules (`itertools` and `functools`) that implement functional tools borrowed from Haskell and Standard ML.

Its core philosophy is summarized in the Zen of Python (PEP 20), which includes aphorisms such as:

- Beautiful is better than ugly.
- Explicit is better than implicit.
- Simple is better than complex.
- Complex is better than complicated.
- Readability counts.

## Implementations

CPython is the reference implementation of Python. It is written in C, meeting the C11 standard (beginning with Python 3.11). It compiles Python programs into an intermediate bytecode which is then executed by its virtual machine. CPython is distributed with a large standard library written in a mixture of C and native Python, and is available for many platforms.

Other implementations are:

- PyPy, a fast, compliant interpreter of Python 2.7 and 3.8. Its just-in-time compiler often brings a significant speed improvement over CPython but some libraries written in C cannot be used with it.
- Stackless Python, a significant fork of CPython that implements microthreads; it does not use the call stack in the same way, thus allowing massively concurrent programs. PyPy also has a stackless version.
- Pyston, a variant of the Python runtime that uses just-in-time compilation to speed up the execution of Python programs.
- Cinder, a performance-oriented fork of CPython 3.8 that contains a number of optimizations, including bytecode inline caching, eager evaluation of coroutines, a method-at-a-time JIT, and an experimental bytecode compiler.
- Codon, that compiles a subset of statically typed Python to machine code (via LLVM) and supports native multithreading.
- Cython, that compiles (a superset of) Python to C. The resulting code is also usable with Python via direct C-level API calls into the Python interpreter.
- PyJL, that compiles/transpiles a subset of Python to "human-readable, maintainable, and high-performance Julia source code".
- Nuitka, that compiles Python into C.
- Numba, that uses LLVM to compile a subset of Python to machine code.
- Pythran, that compiles a subset of Python 3 to C++ 11.