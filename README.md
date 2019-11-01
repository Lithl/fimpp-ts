## FiM++
FiM++ is an esolang modeled after the friendship reports found in the first few
seasons of _My Litte Pony: Friendship is Magic_. Each class is a letter
addressed to its superclass, and signed by its author. Paragraphs form methods,
and the language tries to structure its syntax such that a program can be
presented like natural language.

See [the FiM++ wiki](https://fimpp.fandom.com/) for additional details.

## FiM++ Typescript Compiler
This repository represents a compiler that will take a FiM++ source file
(`*.fimpp` rather than `*.fpp` as suggested in the FiM++ specification document,
because `*.fpp` is already used by Fortran) and translate it into a Typescript
file (`*.ts`). Optionally, the compiler can automatically run the Typescript
compiler to produce a JavaScript file (`*.js`).

## Language specification
Some parts of the FiM++ language are not fully specified. In order for this
compiler to work properly, those missing pieces need filling in. To that end,
the `docs` directory contains the full specification used by this compiler.
