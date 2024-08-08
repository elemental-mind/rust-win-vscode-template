# Rust Windows VSCode Template

This repository provides a template for setting up a Rust development environment on Windows using Visual Studio Code where you then can simply hit `F5` and debugging just works.

## Prerequisites

You should have Rust and VSCode installed:
- [Rust](https://www.rust-lang.org/tools/install)
- [Visual Studio Code](https://code.visualstudio.com/)

You should then install the `cargo watch` cargo extension by running `cargo install cargo-watch`:
- [Cargo Watch](https://crates.io/crates/cargo-watch)

Also add the `C/C++ extension` to VSCode in order for debugging to work:
- [Microsoft C/C++](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools)


## Getting Started

1. **Clone the repository:**

    ```sh
    git clone https://github.com/elemental-mind/rust-win-vscode-template.git <your-dir-name>
    ```

    Then `cd` into your chosen directory and run the following command to unlink the template from this remote repository:

    ```sh
    git remote remove origin
    ```

2. **Rename your program and project**

    Go into `cargo.toml` and rename your `package -> name` to your project name. 

    To rename your binary output, change the `bin -> name` property.
    Then also change the `configurations -> program` property in the `launch.json` to reflect the changed executable name.

3. **Code and debug**

    The project is configured to use the `cppvsdbg` debugger for Rust on Windows. Have this installed as a VSCode extension (as mentioned in the prerequisites).

    You should then be able to set a breakpoint and just hit `F5` for your program to run. This will launch the debug build task (if not already running) and launch your program.
    The debug output should be visible in the Debug Console, the build output shut be visible in a new tab of the Terminal in VSCode.

All the normal cargo commands should work like `cargo run` and `cargo build`.
