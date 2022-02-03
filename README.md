# Visual Studio Code Protobuf Stack

## Pre-requirements

### Protocol Buffer Compiler

> [https://grpc.io/docs/protoc-installation/](https://grpc.io/docs/protoc-installation/)

- Linux:

```bash
sudo apt-get install -y protobuf-compiler
```

- MacOS:

```bash
brew install protobuf
```

### ClangFormat

> [https://clang.llvm.org/docs/ClangFormat.html](<https://clang.llvm.org/docs/ClangFormat.html>)

- Linux:

```bash
sudo apt-get install -y clang-format
```

- MacOS:

```bash
brew install clang-format
```

### protolint

> [https://github.com/yoheimuta/protolint](https://github.com/yoheimuta/protolint)

Requires [Go](https://go.dev/) to be installed.

```bash
go install github.com/yoheimuta/protolint/cmd/protolint@latest
```

## Visual Studio Code

### Extensions

- [vscode-proto3](https://marketplace.visualstudio.com/items?itemName=zxh404.vscode-proto3)

```bash
code --install-extension zxh404.vscode-proto3
```

- [Proto Lint](https://marketplace.visualstudio.com/items?itemName=Plex.vscode-protolint)

```bash
code --install-extension plex.vscode-protolint
```

### Config

```json
{
    // Format on save.
    "editor.formatOnSave": true,

    // Clang parameters.
    "clang-format.style": "{ IndentWidth: 4, BasedOnStyle: google, AlignConsecutiveAssignments: true }",

    // Protobuf formatter.
    "[proto3]": {
        "editor.defaultFormatter": "xaver.clang-format"
    }
}
```

