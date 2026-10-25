jlox: A Tree-Walk Interpreter in Java

A Java implementation of Lox, a dynamically typed programming language, built by following "Crafting Interpreters" (https://craftinginterpreters.com/) by Robert Nystrom.

This project explores how programming languages work internally, from lexical analysis and parsing to expression evaluation, environments, and control flow.

Overview

jlox is a tree-walk interpreter written in Java. It reads Lox source code, parses it into an abstract syntax tree (AST), and evaluates the resulting expressions and statements.

The project was built as a hands-on exercise in programming language implementation, compiler fundamentals, and interpreter design.

Features

The implementation follows the jlox interpreter developed in Crafting Interpreters.

- Lexical analysis: Converts source code into tokens.
- Parsing: Builds an abstract syntax tree using recursive descent.
- Expression evaluation: Evaluates arithmetic, comparison, logical, and other supported expressions.
- Variables and environments: Handles variable declarations, assignment, and scope.
- Control flow: Supports conditional statements and loops.
- Functions: Supports user-defined functions, arguments, return values, and closures.
- Classes and objects: Implements the class and object features supported by jlox.
- Runtime error handling: Reports errors encountered during scanning, parsing, and execution.

The exact feature list should reflect the implementation currently present in your repository.

How It Works

The interpreter processes source code through several stages:

1. Source code: Receives Lox code from a file or interactive prompt.
2. Scanner: Converts characters into tokens.
3. Parser: Transforms tokens into an abstract syntax tree.
4. Interpreter: Evaluates expressions and executes statements.
5. Environment: Maintains variables, scope, and runtime bindings.

Example

fun fibonacci(n) {
  if (n <= 1) return n;
  return fibonacci(n - 2) + fibonacci(n - 1);
}

print fibonacci(10);

Expected output:

55

Technologies

- Java
- Object-oriented programming
- Recursive descent parsing
- Abstract syntax trees (ASTs)
- Tree-walk interpretation
- Runtime environments and lexical scoping

Getting Started

Prerequisites

- A compatible Java Development Kit (JDK).
- The source code and build instructions for this repository.

Installation

Clone the repository:

git clone https://github.com/YOUR_USERNAME/jlox.git
cd jlox

Compile and run the interpreter using the build process configured in the project.

For example, if your project uses plain Java source files, the compilation and execution commands will depend on its package structure and entry point.

What I Learned

Building jlox helped me explore:

- How source code becomes executable behavior.
- How scanners and parsers recognize programming language syntax.
- How abstract syntax trees represent expressions and statements.
- How interpreters evaluate expressions and manage runtime state.
- How lexical scope, closures, functions, and object-oriented features work internally.
- How to translate language specifications into working software.

Reference

Robert Nystrom, "Crafting Interpreters" (https://craftinginterpreters.com/).

This project is an educational implementation inspired by the book.

License

See the repository's license file for the applicable terms.
