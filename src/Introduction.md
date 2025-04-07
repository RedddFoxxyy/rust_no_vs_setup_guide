# Introduction

This guide will help you to setup rust on windows without the use of Visual Studio IDE. This guide will cover through the alternative rust toolchains available to use on windows rather than using stable-x86_64-pc-windows-msvc that rustup defaults too during installation.

> Note: This guide assumes that you are using windows on Intel/AMD x86_64 cpus, and thus uses
> the toolchains for the given architecture. However this guide also applies to i686 and aarch64
> architectures. For these architectures, just replace x86_64 with i686/aarch64 in the
> toolchain name. (i.e. i686-pc-windows-gnu/aarch64-pc-windows-gnu instead of
> x86_64-pc-windows-gnu).

There are 2 alternative toolchains you that can use on windows instead of using the default x86_64-pc-windows-msvc toolchain: -

1. x86_64-pc-windows-gnu [(Tier 1 Target)](https://rust-lang.github.io/rustup-components-history/x86_64-pc-windows-gnu.html)
2. x86_64-pc-windows-gnullvm [(Tier 2.5 Target)](https://rust-lang.github.io/rustup-components-history/x86_64-pc-windows-gnullvm.html)

This guide will cover the setup of rust for developing on windows using each of the above toolchain.

> Note: This guide is still under developement, and might contain some mistakes. Contributers are welcomed to fix them and open a pull request for the fixes. New additions to the guide are also welcomed.
