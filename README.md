## Overview
The LLVM compiler runtime (compiler-rt) is essential in clang-based builds.
However, it should be noted that the compiler-rt is exclusively accessible in
the form of source code for RISC-V targets. Consequently, within this project,
we possess the capability to construct it entirely from scratch.

## Build
To build it, run `make`, the static library will be generated at `build/libcompiler-rt.a`.
Then use following Makefile configuration:
```
LDFLAGS += -L./build -lcompiler-rt
```

## Source
This project is **completely** from the llvm project:

- Repo: `https://github.com/llvm/llvm-project`
- Branch: `master`
- Commit: `a3fb2348b19167dfb027e20f8e1306ebbf31cfbf`

See more: https://github.com/llvm/llvm-project/blob/release/16.x/compiler-rt/lib/builtins/README.txt
