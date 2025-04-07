# Setting up alternative Toolchain.

Rust by default forces you to use msvc as the default compiler and linker on windows because it provides the C runtime libraries (UCRT) required by rustc while compilation to link the required C code and it also needs the linker provided by MSVC however there are few alternatives to this.

Using the GNU GCC compiler or the CLANG compiler instead of msvc, these compilers also provide a linker and a C compiler similar to MSVC but the licenses of these are more open comapred to MSVC.

We will be installing and setting up either of these using MSYS2. Which compiler to use (GCC or CLANG) depends upon what alternative toolchain you are going to use, there are two alternative toolchains available as referred to in the introduction of this guide.

- x86_64-pc-windows-gnu [(Tier 1 Target)](https://rust-lang.github.io/rustup-components-history/x86_64-pc-windows-gnu.html)
- x86_64-pc-windows-gnullvm [(Tier 2.5 Target)](https://rust-lang.github.io/rustup-components-history/x86_64-pc-windows-gnullvm.html)

The difference between the two is the compiler tools that they use and the Windows C libraries that they link too.

### 1. x86_64-pc-windows-gnu

The `x86_64-pc-windows-gnu` target similar to MSVC, also helps in linking and compiling of C code for the rust compiler however unlike `x86_64-pc-windows-gnu` which links to the modern UCRT libraries, x86_64-pc-windows-gnu links to the old MSVCRT C libraries which are old and are not compatible with code compiled using UCRT. This is the only drawback of this toolchain.

The rust code compiled using this toolchain is similar in operation to that compiled by the msvc toolchain however the binary produced is not the same.

This is a ['Tier 1](https://doc.rust-lang.org/nightly/rustc/platform-support.html)' target and thus can be set as the default toolchain using rustup.

### 2. x86_64-pc-windows-gnullvm

Similar to `x86_64-pc-windows-gnu`, the `x86_64-pc-windows-gnullvm` toolchain also is an alternative to `x86_64-pc-windows-msvc` but overcomes the drawback of `x86_64-pc-windows-gnu`.

This toolchain uses the LLVM linker and compiler(CLANG) instead of `GNU GCC` and links to the newer
UCRT C libraries instead of the old MSVCRT which is also compatible and produces code similar to that produced by MSVC.

However, the drawback of using this target is that this is a ['Tier 2.5'](https://rust-lang.github.io/rustup-components-history/x86_64-pc-windows-gnullvm.html) target and cannot be set as the default toolchain using rustup. Instead you have to pass this as the target while compiling your code. (i.e. `cargo build --target x86_64-pc-windows-gnullvm`).

Tier 2 or 3 targets are also not tested a lot, unlike the Tier 1 targets. So expect unexpected bugs / errors during compiling your app. Though rare, but can happen.

The next chapters will guide you through the setup of either of these toolchains and the required compilers.
