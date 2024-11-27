# Notes on Julia Performance

Statically typing the program, or facilitating the type inference of the JIT compiler makes the code run faster. Some notes:

- Avoid global variables and run your performance-critical code within functions rather than in the global scope;
- Annotate the inner type of a container, so it can be stored in memory contiguously;
- Annotate the fields of composite types (use eventually parametric types);
- Loop matrices first by column and then by row.

Notes on profiling :

- To time a part of the code type `@time myFunc(args)` (be sure you ran that function at least once, or you will measure compile time rather than run-time).
- `@benchmark myFunc(args)` (from package BenchmarkTools) also works.
- Profile a function: `Profile.@profile myfunct()` (best after the function has been already ran once for JIT-compilation).
- Print the profiling results: `Profile.print()` (number of samples in corresponding line and all downstream code; file name:line number; function name;)
- Explore a chart of the call graph with profiled data: `ProfileView.view()` (from package ProfileView).
- Clear profile data: `Profile.clear()`.
