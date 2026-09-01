# Just \[Code]

*Just* a general purpose programming language.

Key highlights:

- statically typed, with support of type inference and type union.
- strongly typed, with support of implicit and explicit type narrowing.
- structurally typed, while nominal type is also supported.
- built for class-less object oriented programming
- built for functional programming
- secure by default
- compile to native assembly, no VM or garbage collection.
- complete type-level programming.
- tool first, with battery included.

## Milestones

- 🚧 High level language design
- 🚧 Define language syntax
- ⌛️ `just_std_io` in *rust*
- ⌛️ `just_std_fs` in *rust*
- ⌛️ `stage-0` compiler in *rust*
- ⌛️ `stage-1` compiler in *just*
- ⌛️ `just_std_*` libraries
- ⌛️ `just_compiler`
- ⌛️ `just_test`
- ⌛️ `just_package_manager`
- ⌛️ `just` all-in-one cli tool
- ⌛️ `just_language_service`
- ⌛️ `just_language_server`
- ⌛️ `just_vscode_plugin`
- ⌛️ `just_lint`
- ⌛️ `just_doc`
- ⌛️ `just_interpreter`

*Just* is influenced by multiple programming languages,
most notably `Rust`, `TypeScript`, and `AssemblyScript`.

- statically type with strong type inference
  - type inference is the solution to the "static vs dynamic" debate.
  - Uni aims to only require type declaration at function parameters.\\
    Everything else can be type inferred.
  - Haskell, TypeScript, Rust, and Go have type inference in various degrees.
- structural type
  - nominal type has a few significant drawbacks:
    - create an inverted coupling between the producer and consumer.
      - this is the biggest problem of all.\\
        Marking the application architecture rigit or very tedious to develop and maintain.
    - make the program unnecessary verbose and fill with needless type casts.
  - It is much easier to create a nominal type language vs a structural type language.
  -
- compile to native code
- explicit ownership, no garbage collection
- extensible through macro
- build-in linting and formatting
- workspace support
- filename conventions
- generics

Traits it gets from TypeScript:

- structural type
- type inference
- type composition
- syntax in TypeScript and JavaScript
  - generics

Traits unique to *Just*:

- set theory type composition
- explicit syntax enables strong IDE support
- compiler engine is available during test
  - allow test to create isolated execution scope for dependency injection

## Module Organization

The `std` library is modeled after NodeJS instead of Rust.
One of the main differences is that they are different modules.
This way, it is more flexible and `unic0` only needs to build some of the key modules required to build `unic`.
Meaning other modules can be written with better syntax.

- <https://nodejs.org/api/http.html>
- <https://github.com/denoland/deno/tree/master/std>
- <https://github.com/rust-lang/rust/tree/master/src/libstd>

## Testing

```sh
# watch test a specific package
cargo watch -x "test -p libunic_compiler -- --nocapture"
```

## Recommended setup

- <https://github.com/rust-lang/rust-clippy>
- <https://github.com/xd009642/tarpaulin>
