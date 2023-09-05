# Quick Start

### Install Rust

See the Rust ["Getting Started"] page to install the Rust development tools.

["Getting Started"]: https://www.rust-lang.org/learn/get-started

### Using BDK in a Rust project

Follow these steps to use BDK in your own rust project with the async `esplora` blockchain client.

> ⚠ For now use the latest `master` branch versions of BDK crates.

1. Create a new Rust project:
   ```shell
   cargo init my_bdk_app
   cd my_bdk_app
   ```
2. Add `bdk` to your `Cargo.toml` file. Find the latest `bdk@1` release on [`crates.io`](https://crates.io/crates/bdk/versions), for example:
   ```shell
    cargo add bdk@1.0.0-alpha.1
   ```
3. Add other required dependencies:
   ```shell
   cargo add bdk_esplora@0.3.0
   cargo add bdk_file_store@0.2.0
   cargo add tokio@1 --features "rt,rt-multi-thread,macros"
   ```

See the [Wallet with Async Esplora](tutorials/wallet_async_esplora.md) tutorial for how to create and sync a wallet.

### Contributing to BDK

To contribute to BDK first install the stable version of `rust`, clone the repository `master` branch and verify you can run the tests for all features.

1. Clone the repo:
   ```shell
   git clone https://github.com/bitcoindevkit/bdk.git
   cd bdk
   ```
2. Build and run the tests:
   ```shell
   cargo test --all-features
   ```

 
