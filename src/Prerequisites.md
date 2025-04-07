# Prerequisites

You will need the following softwares before we begin:

- The Rustup Installer, to install rust and toolchain on your windows machine.

- MSYS2 to install GNU GCC/CLANG on your windows machine.

## Rust Setup:

- Download Rustup from the [Official Website](https://www.rust-lang.org/tools/install).

- Execute the rustup installer.

- Once the rustup installer opens up in the terminal, type 3 and click on enter( Cause we are targetting the GNU ABI instead of using VISUAL STUDIO ).

- Next type 2 in the terminal and click on enter to customise the installation options so that we can select a different toolchain instead of the default MSVC toolchain for windows.

- When it asks you for the default host tripple, type in this as the input: `x86_64-pc-windows-gnu` and then press enter to change the toolchain and compile target from MSVC to GNU GCC.

- Next, when asked for which tools to install, type in `complete` or `default` depending upon your needs.

- Finally, when asked to modify the path Variable, type `Y` and pressing Enter will give you the new installation options that we set up for rust, just press enter and wait for rust to install on the machine.

#### The whole rust installation process should look something like this:

```

    Rust Visual C++ prerequisites

    Rust requires a linker and Windows API libraries but they don't seem to be
    available.

    These components can be acquired through a Visual Studio installer.

    1) Quick install via the Visual Studio Community installer
    (free for individuals, academic uses, and open source).

    2) Manually install the prerequisites
    (for enterprise and advanced users).

    3) Don't install the prerequisites
    (if you're targeting the GNU ABI).

    >3


    Welcome to Rust!

    This will download and install the official compiler for the Rust
    programming language, and its package manager, Cargo.

    Rustup metadata and toolchains will be installed into the Rustup
    home directory, located at:

    C:\Users\suyog\.rustup

    This can be modified with the RUSTUP_HOME environment variable.

    The Cargo home directory is located at:

    C:\Users\suyog\.cargo

    This can be modified with the CARGO_HOME environment variable.

    The cargo, rustc, rustup and other commands will be added to
    Cargo's bin directory, located at:

    C:\Users\suyog\.cargo\bin

    This path will then be added to your PATH environment variable by
    modifying the HKEY_CURRENT_USER/Environment/PATH registry key.

    You can uninstall at any time with rustup self uninstall and
    these changes will be reverted.

    Current installation options:


    default host triple: x86_64-pc-windows-msvc
        default toolchain: stable (default)
                profile: default
    modify PATH variable: yes

    1) Proceed with standard installation (default - just press enter)
    2) Customize installation
    3) Cancel installation
    >2

    I'm going to ask you the value of each of these installation options.
    You may simply press the Enter key to leave unchanged.

    Default host triple? [x86_64-pc-windows-msvc]
    x86_64-pc-windows-gnu

    Default toolchain? (stable/beta/nightly/none) [stable]
    stable

    Profile (which tools and data to install)? (minimal/default/complete) [default]
    complete

    Modify PATH variable? (Y/n)
    Y


    Current installation options:


    default host triple: x86_64-pc-windows-gnu
        default toolchain: stable
                profile: complete
    modify PATH variable: yes

    1) Proceed with selected options (default - just press enter)
    2) Customize installation
    3) Cancel installation
>
```

#### Next we setup MSYS2 for the GCC/CLang compilers and tools that we will be needing.

## What is MSYS2?

**MSYS2** is a collection of tools and libraries providing you with an easy-to-use environment for building, installing and running native Windows software.

You will need MSYS2 to install and setup C compiler, C developement libraries and linker. To install MSYS2 follow these steps:

## MSYS2 Setup:

- Download MSYS2 installer from the official website of [MSYS2](https://www.msys2.org/) or [download here](https://github.com/msys2/msys2-installer/releases/download/2025-02-21/msys2-x86_64-20250221.exe).

- Install MSYS2 with default settings or change the install path if required.

Now you will have MSYS2available on your pc. We will next install C compiler ( GCC/ CLANG ) using MSYS2 terminals.

You can check if MSYS2 is installed or not by searching MINGW64 in windows search bar and opening MSYS2 MINGW64 terminal. This will be used later to install GCC.
