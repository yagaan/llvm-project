# Language Server protocol AST extensions

This project if a fork of [LLVM compiler infrastructure](https://github.com/llvm/llvm-project). LLVM has been forked in order to add AST export and background parsing ,without diagnostic, to Clangd.

## LSP extensions

Some extensions to the LSP protocol have been added

- `textDocument/ast/native` : save the clang AST of the parsed text document into a JSON file.
- `textDocument/background/parse`: background parsing of a file without any produced diagnostic.

Those `clangd`extensions have been updated:

- `textDocument/ast` : clangd AST JSON output of the parsed text document for a given start/end range. If the start range line is `-1` then the whole AST is returned instead of searching the ASTNode that contains the range.