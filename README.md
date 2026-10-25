☕ jlox: A Tree-Walk Interpreter in Java

<p align="center">
  <img src="https://img.shields.io/badge/Language-Java-orange?style=for-the-badge&logo=openjdk" alt="Java"/>
  <img src="https://img.shields.io/badge/Project-Interpreter-blue?style=for-the-badge" alt="Interpreter"/>
  <img src="https://img.shields.io/badge/Focus-Programming%20Languages-purple?style=for-the-badge" alt="Programming Languages"/>
</p>jlox is a Java implementation of the Lox programming language, built by following "Crafting Interpreters" (https://craftinginterpreters.com/) by Robert Nystrom.

This project explores how programming languages work internally, from scanning and parsing source code to evaluating expressions, managing variables, and executing programs.

«💡 A hands-on journey into programming language implementation, interpreters, and the fundamentals of language design.»

---

📌 Table of Contents

- "Overview" (#-overview)
- "Features" (#-features)
- "Technologies" (#-technologies)
- "Project Structure" (#-project-structure)
- "Getting Started" (#-getting-started)
- "Usage" (#-usage)
- "Example Programs" (#-example-programs)
- "Key Concepts" (#-key-concepts)
- "Learning Reference" (#-learning-reference)
- "Author" (#-author)

---

🚀 Overview

jlox is a tree-walk interpreter for Lox. It processes source code through several stages before executing it:

1. 🔎 Scanning: Converts source code into tokens.
2. 🌳 Parsing: Converts tokens into an abstract syntax tree (AST).
3. 🧠 Resolution: Resolves variable references and lexical scope.
4. ⚙️ Interpretation: Evaluates expressions and executes statements.

The implementation brings together fundamental programming language concepts, including recursive-descent parsing, environments, closures, functions, classes, and inheritance.

✨ Features

- 🔎 Lexical Analysis: Tokenizes source code using a scanner.
- 🌳 Recursive-Descent Parsing: Parses expressions and statements according to the language grammar.
- 🧩 Abstract Syntax Trees: Represents expressions and statements using structured AST nodes.
- ➕ Expressions and Operators: Supports arithmetic, comparison, equality, and logical operations.
- 📦 Variables and Scope: Implements declarations, assignments, blocks, and lexical scoping.
- 🔀 Control Flow: Supports "if", "else", "while", and "for" statements.
- ⚙️ Functions: Supports function declarations, calls, arguments, and return values.
- 🔗 Closures: Allows functions to retain access to their surrounding lexical environment.
- 🏛️ Classes and Objects: Implements classes, instances, and methods.
- 🧬 Inheritance: Supports subclasses and superclass method access through "super".
- 👤 Method Binding: Supports the "this" keyword.
- 🧠 Static Resolution: Uses a resolver to determine variable bindings.
- ⚠️ Error Handling: Handles scanning, parsing, and runtime errors.

🛠️ Technologies

Technology| Purpose
☕ Java| Implementation language
🌳 Recursive-descent parsing| Syntax analysis
🧩 Abstract Syntax Tree (AST)| Program representation
⚙️ Tree-walk interpretation| Program execution
🐙 Git and GitHub| Version control and project hosting

📂 Project Structure

The core interpreter implementation is organized under "com/craftinginterpreters/lox/".

com/craftinginterpreters/lox/
├── Lox.java           # Entry point and error reporting
├── Scanner.java       # Lexical analysis
├── Token.java         # Token representation
├── TokenType.java     # Token types
├── Parser.java        # Recursive-descent parser
├── Expr.java          # Expression AST nodes
├── Stmt.java          # Statement AST nodes
├── Interpreter.java   # Tree-walk interpreter
├── Environment.java   # Variable environments and scope
├── Resolver.java      # Static variable resolution
├── LoxCallable.java   # Callable object interface
├── LoxFunction.java   # User-defined functions
├── LoxClass.java      # Class representation
├── LoxInstance.java   # Class instances
├── RuntimeError.java  # Runtime error handling
└── Return.java        # Return statement control flow

💻 Getting Started

📋 Prerequisites

Make sure you have the following installed:

- Java Development Kit (JDK)
- Java compiler ("javac")
- Java runtime ("java")
- A terminal or command prompt

1️⃣ Clone the Repository

git clone https://github.com/danielking-debug/craftinginterpreters.git
cd craftinginterpreters

2️⃣ Compile the Interpreter

From the directory containing the "com/" folder, run:

javac com/craftinginterpreters/lox/*.java

3️⃣ Start the Interactive Interpreter

java com.craftinginterpreters.lox.Lox

You can now enter Lox statements directly into the interactive interpreter.

🎮 Usage

👋 Hello, Lox!

print "Hello, Lox!";
print 10 + 20;

Output:

Hello, Lox!
30

📄 Run a Lox Script

Create a file named "hello.lox":

var language = "Lox";
print "Hello from " + language + "!";

Execute the script from the project root:

java com.craftinginterpreters.lox.Lox hello.lox

Output:

Hello from Lox!

🧪 Example Programs

1. 📦 Variables and Control Flow

var language = "Lox";
var version = 1;

if (version == 1) {
  print "Learning " + language;
}

Output:

Learning Lox

2. 🔗 Functions and Closures

fun makeCounter() {
  var count = 0;

  fun increment() {
    count = count + 1;
    print count;
  }

  return increment;
}

var counter = makeCounter();

counter();
counter();
counter();

Output:

1
2
3

What this demonstrates: The "increment" function retains access to the "count" variable from its enclosing function, even after "makeCounter()" has returned.

3. 🧬 Classes and Inheritance

class Doughnut {
  cook() {
    print "Fry until golden brown.";
  }
}

class BostonCream < Doughnut {
  cook() {
    super.cook();
    print "Add custard and chocolate.";
  }
}

BostonCream().cook();

Output:

Fry until golden brown.
Add custard and chocolate.

What this demonstrates: A subclass inherits behavior from its superclass and can invoke the superclass implementation using "super".

🧠 Key Concepts Explored

Building jlox provides practical experience with:

- Language Implementation: Understanding how source code becomes executable behavior.
- Lexical Analysis: Identifying keywords, operators, literals, and identifiers.
- Parsing: Translating tokens into a structured representation of a program.
- Interpreter Design: Evaluating expressions and executing statements.
- Environments and Scope: Managing variables, assignments, and lexical scope.
- Closures: Preserving access to variables across function calls.
- Object-Oriented Language Features: Implementing classes, methods, instances, and inheritance.
- Static Resolution: Resolving variable references before interpretation.
- Error Handling: Identifying and reporting errors during different stages of execution.

📚 Learning Reference

This project follows the Java interpreter implementation in:

"Crafting Interpreters" (https://craftinginterpreters.com/)

Author: Robert Nystrom

The book serves as the primary learning reference for the interpreter's design and implementation.

👨‍💻 Author

Daniel Oche

- 🐙 GitHub: "@danielking-debug" (https://github.com/danielking-debug)
- 📂 Repository: "craftinginterpreters" (https://github.com/danielking-debug/craftinginterpreters)

---

<p align="center">
  <b>☕ Built with Java, curiosity, and a deeper interest in how programming languages work.</b>
</p>
