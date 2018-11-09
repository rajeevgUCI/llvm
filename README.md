# LLVM #

Fork of LLVM. Build instructions below show how to build with WebAssembly support.

For original README, see README\_original.txt .

## Build Instructions ##

To clone and check out correct releases of LLVM and clang:
```bash
git clone -b "release_60" https://github.com/rajeevgUCI/llvm.git
git clone -b "release_60" https://github.com/rajeevgUCI/clang.git llvm/tools/clang
```
This clones and checks out release 6.0.0 of both.

To build:
```bash
mkdir build
cd build
cmake -DLLVM_ENABLE_TERMINFO=OFF -DLLVM_TARGETS_TO_BUILD= -DLLVM_EXPERIMENTAL_TARGETS_TO_BUILD=WebAssembly -DLLVM_ENABLE_ASSERTIONS=ON -DCMAKE_BUILD_TYPE=Release ..
make
```

