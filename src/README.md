# Introduction

The Bitcoin Dev Kit (BDK) project was created to provide well engineered and reviewed components for building bitcoin based applications. The core components of BDK are written in the [`Rust`] language and live in the [`bitcoindevkit/bdk`] repository. The core BDK components are built upon the excellent [`rust-bitcoin`] and [`rust-miniscript`] crates.

The BDK team also maintains the [`bitcoindevkit/bdk-ffi`] repository which provide cross platform versions of the high level BDK APIs. Current supported platforms are: [`Kotlin`] (android, linux, MacOS), [`Swift`] (iOS, MacOS), and [`Python`] (linux, MacOS, Windows).

> ⚠ The BDK developers are in the process of rewriting major components of the software to be release in an upcoming `1.0` version. `BDK 1.0` is a still under active development and should be considered "alpha" quality. This means APIs may change and full testing and documentation has not been completed. For current status and release timeline please see the [`BDK 1.0`] project page.
>
> The [`bitcoindevkit/bdk-ffi`] project has not yet been updated to use the new `BDK 1.0` crates. For current status and timeline for `BDK-FFI 1.0` see the [`BDK-FFI`] project page.

### 🔨 Project Organization

Within the [`bitcoindevkit/bdk`] repository the BDK team maintains a suite of rust crates which provide both an easy to use high level API as well as powerful lower level components to used when building more advanced bitcoin software.

The project is split up into several crates in the `/crates` directory:

- [`bdk`](./crates/bdk): Contains the central high level `Wallet` type that is built from the low-level mechanisms provided by the other components
- [`chain`](./crates/chain): Tools for storing and indexing chain data
- [`file_store`](./crates/file_store): A (experimental) persistence backend for storing chain data in a single file.
- [`esplora`](./crates/esplora): Extends the [`esplora-client`] crate with methods to fetch chain data from an esplora HTTP server in the form that [`bdk_chain`] and `Wallet` can consume.
- [`electrum`](./crates/electrum): Extends the [`electrum-client`] crate with methods to fetch chain data from an electrum server in the form that [`bdk_chain`] and `Wallet` can consume.

Fully working examples of how to use these components are in `/example-crates`:
- [`example_cli`](./example-crates/example_cli): Library used by the `example_*` crates. Provides utilities for syncing, showing the balance, generating addresses and creating transactions without using the bdk `Wallet`.
- [`example_electrum`](./example-crates/example_electrum): A command line Bitcoin wallet application built on top of `example_cli` and the `electrum` crate. It shows the power of the bdk tools (`chain` + `file_store` + `electrum`), without depending on the main `bdk` library.
- [`wallet_esplora_blocking`](./example-crates/wallet_esplora_blocking): Uses the `Wallet` to sync and spend using the Esplora blocking interface.
- [`wallet_esplora_async`](./example-crates/wallet_esplora_async): Uses the `Wallet` to sync and spend using the Esplora asynchronous interface.
- [`wallet_electrum`](./example-crates/wallet_electrum): Uses the `Wallet` to sync and spend using Electrum.

[`rust-miniscript`]: https://github.com/rust-bitcoin/rust-miniscript
[`rust-bitcoin`]: https://github.com/rust-bitcoin/rust-bitcoin
[`esplora-client`]: https://docs.rs/esplora-client/
[`electrum-client`]: https://docs.rs/electrum-client/
[`bdk_chain`]: https://docs.rs/bdk-chain/

### 😃 Join our community

Open source is fundamental to this project and we would love to connect with you. 

Please feel free to open or comment on PRs and issues in any of the [`bitcoindevkit`] repos or join us on the BDK [discord server](https://discord.gg/UbTmGbNF3M), come say hi!

[`Rust`]: https://www.rust-lang.org/
[`Kotlin`]: https://kotlinlang.org/
[`Swift`]: https://www.swift.org/
[`Python`]: https://www.python.org/

[`BDK 1.0`]: https://github.com/orgs/bitcoindevkit/projects/14/views/2
[`BDK-FFI`]: https://github.com/orgs/bitcoindevkit/projects/8
[`bitcoindevkit`]: https://github.com/bitcoindevkit
[`bitcoindevkit/bdk`]: https://github.com/bitcoindevkit/bdk
[`bitcoindevkit/bdk-ffi`]: https://github.com/bitcoindevkit/bdk-ffi
[`rust-bitcoin`]: https://github.com/rust-bitcoin/rust-bitcoin
[`rust-miniscript`]: https://github.com/rust-bitcoin/rust-miniscript