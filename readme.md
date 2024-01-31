# nvim clangd cmake setup

Prerequisites:
- [CMake](https://cmake.org)
- [Clangd](https://clangd.llvm.org/)

## Setup

Install `clangd` lsp for neovim, e.g. with Mason. Make sure it's automatically running on cpp files (default). 


### Generate cmake with `compile_commands.json`
```sh
cmake -S . -B build -DCMAKE_EXPORT_COMPILE_COMMANDS=1
```

Build the project

```sh
cmake --build build/
```

### .clangd

```yaml
CompileFlags:
  CompilationDatabase: "build"
```
