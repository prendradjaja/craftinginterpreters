A fork of https://github.com/munificent/craftinginterpreters

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
