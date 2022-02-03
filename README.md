# Visual Studio Code Protobuf Stack

- [Visual Studio Code Protobuf Stack](#visual-studio-code-protobuf-stack)
  - [Pre-requirements](#pre-requirements)
    - [1. Protocol Buffer Compiler](#1-protocol-buffer-compiler)
    - [2. ClangFormat](#2-clangformat)
    - [3. protolint](#3-protolint)
  - [Visual Studio Code](#visual-studio-code)
    - [1. Extensions](#1-extensions)
    - [2. Config](#2-config)

---

## Pre-requirements

### 1. Protocol Buffer Compiler

> [https://grpc.io/docs/protoc-installation/](https://grpc.io/docs/protoc-installation/)

- Linux:

```bash
sudo apt-get install -y protobuf-compiler
```

- MacOS:

```bash
brew install protobuf
```

### 2. ClangFormat

> [https://clang.llvm.org/docs/ClangFormat.html](<https://clang.llvm.org/docs/ClangFormat.html>)

- Linux:

```bash
sudo apt-get install -y clang-format
```

- MacOS:

```bash
brew install clang-format
```

### 3. protolint

> [https://github.com/yoheimuta/protolint](https://github.com/yoheimuta/protolint)

Requires [Go](https://go.dev/) to be installed.

```bash
go install github.com/yoheimuta/protolint/cmd/protolint@latest
```

---

## Visual Studio Code

### 1. Extensions

- [vscode-proto3](https://marketplace.visualstudio.com/items?itemName=zxh404.vscode-proto3)

```bash
code --install-extension zxh404.vscode-proto3
```

- [Proto Lint](https://marketplace.visualstudio.com/items?itemName=Plex.vscode-protolint)

```bash
code --install-extension plex.vscode-protolint
```

- [Clang-Format](https://marketplace.visualstudio.com/items?itemName=xaver.clang-format)

```bash
code --install-extension xaver.clang-format
```

### 2. Config

```json
{
    "editor.formatOnSave": true,

    "clang-format.style": "{ IndentWidth: 4, BasedOnStyle: google, AlignConsecutiveAssignments: true }",

    "[proto3]": {
        "editor.defaultFormatter": "xaver.clang-format"
    }
}
```
