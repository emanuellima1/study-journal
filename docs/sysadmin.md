# Notes on System Administration

## Table of Contents

- [Notes on System Administration](#notes-on-system-administration)
  - [Table of Contents](#table-of-contents)
  - [Compilation](#compilation)
    - [Using distutils with cythonize](#using-distutils-with-cythonize)

## Compilation

### Using distutils with cythonize

Consider a `fib.pyx` Cython so uxrce code. Our goal is to use distutils to create a compiled extension module (`fib.so` on Mac OS X or Linux and `fib.pyd` on Windows). For that, we use a `setup.py` file like so: