## FiM++
FiM++ is an esolang modeled after the friendship reports found in the first few
seasons of _My Litte Pony: Friendship is Magic_. Each class is a letter
addressed to its superclass, and signed by its author. Paragraphs form methods,
and the language tries to structure its syntax such that a program can be
presented like natural language.

The syntax of FiM++ is largely modeled after Java, and inspired by the likes of
the Shakespeare Programming Language and Inform 7.

See [the FiM++ wiki](https://fimpp.fandom.com/) for additional details.

## FiM++ Typescript Compiler
This repository represents a compiler that will take a FiM++ source file
(`*.fimpp` rather than `*.fpp` as suggested in the FiM++ specification document,
because `*.fpp` is already used by Fortran) and translate it into a Typescript
file (`*.ts`). Optionally, the compiler can automatically run the Typescript
compiler to produce a JavaScript file (`*.js`).

### Running the compiler
Use `fimpp-ts [options] files...` to compile any number of `*.fimpp` files.
While FiM++ files are expected to use the extension `FIMPP`, the compiler will
accept any files you give it; be aware of this if you pass wildcards to the
compiler parameter. Unless you specify a different output location, the compiler
will generate the output files in the same location as the input files, with the
same name. The output files will overwrite the input files if they happen to
have the same file extension (eg, if you write a FiM++ file in a `*.ts` file and
run the compiler with no options to prevent overwriting).

#### Compiler options
* `-o dirname` or `--out dirname`: place output files in `dirname` (relative to
  current working directory). If the input files have directory structure, that
  structure will be preserved.
* `-js` or `--javascript`: compile the Typescript files into JavaScript.
* `--no-typescript`: do not leave any Typescript files behind (not recommended
  without `--javascript`). Typescript files will still be generated, they will
  simply be deleted after the compiler has finished its job.
* `-v` or `--verbose`: produce additional output when running the compiler.
* `-h` or `--help`: display command-line instructions for compiler.

## Language specification
Some parts of the FiM++ language are not fully specified. In order for this
compiler to work properly, those missing pieces need filling in. To that end,
the `docs` directory contains the full specification used by this compiler.

See the language specification [README](docs/README.md) for additional
information.
