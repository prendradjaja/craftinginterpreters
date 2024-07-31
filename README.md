A fork of https://github.com/munificent/craftinginterpreters with the code as
it looks like at the end of each chapter.

## Table of contents

Each directory contains the code as it looks at the _end_ of each chapter.

See also https://craftinginterpreters.com/contents.html

Java chapters:

- [4. Scanning              ](./gen/chap04_scanning)
- [5. Representing Code     ](./gen/chap05_representing)
- [6. Parsing Expressions   ](./gen/chap06_parsing)
- [7. Evaluating Expressions](./gen/chap07_evaluating)
- [8. Statements and State  ](./gen/chap08_statements)
- [9. Control Flow          ](./gen/chap09_control)
- [10. Functions            ](./gen/chap10_functions)
- [11. Resolving and Binding](./gen/chap11_resolving)
- [12. Classes              ](./gen/chap12_classes)
- [13. Inheritance          ](./gen/chap13_inheritance)

C chapters:

- [14. Chunks of Bytecode      ](./gen/chap14_chunks)
- [15. A Virtual Machine       ](./gen/chap15_virtual)
- [16. Scanning on Demand      ](./gen/chap16_scanning)
- [17. Compiling Expressions   ](./gen/chap17_compiling)
- [18. Types of Values         ](./gen/chap18_types)
- [19. Strings                 ](./gen/chap19_strings)
- [20. Hash Tables             ](./gen/chap20_hash)
- [21. Global Variables        ](./gen/chap21_global)
- [22. Local Variables         ](./gen/chap22_local)
- [23. Jumping Back and Forth  ](./gen/chap23_jumping)
- [24. Calls and Functions     ](./gen/chap24_calls)
- [25. Closures                ](./gen/chap25_closures)
- [26. Garbage Collection      ](./gen/chap26_garbage)
- [27. Classes and Instances   ](./gen/chap27_classes)
- [28. Methods and Initializers](./gen/chap28_methods)
- [29. Superclasses            ](./gen/chap29_superclasses)
- [30. Optimization            ](./gen/chap30_optimization)

## How it works

I ran `make split_chapters` (described in the original repo's README,
excerpted below) and added the result (the `gen/` directory) to git.

> You can also see what the interpreters look like at the end of each chapter. (I
> use this to make sure they are working even in the middle of the book.) This is
> driven by a script, `tool/bin/split_chapters.dart` that uses the same comment
> markers for the code snippets to determine which chunks of code are present in
> each chapter. It takes only the snippets that have been seen by the end of each
> chapter and produces a new copy of the source in `gen/`, one directory for each
> chapter's code. (These are also an easier way to view the source code since they
> have all of the distracting marker comments stripped out.)

I also had to run `make java_chapters` to run GenerateAst.java for each chapter
(GenerateAst creates the Expr.java and Stmt.java files).

I don't think there's a corresponding AST generator for the C chapters(?)

It looks like Expr.java and Stmt.java don't have marker comments stripped out,
unfortunately!

If you're interested in Expr.java or Stmt.java, see also: https://craftinginterpreters.com/appendix-ii.html
