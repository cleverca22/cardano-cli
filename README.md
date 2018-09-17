# cardano-cli

[![Build Status](https://travis-ci.org/input-output-hk/cardano-cli.svg?branch=master)](https://travis-ci.org/input-output-hk/cardano-cli)
![MIT or APACHE-2 licensed](https://img.shields.io/badge/licensed-MIT%20or%20APACHE--2-blue.svg)
![Cardano Mainnet](https://img.shields.io/badge/Cardano%20Ada-mainnet-brightgreen.svg)
![Cardano Staging](https://img.shields.io/badge/Cardano%20Ada-staging-brightgreen.svg)
![Cardano Staging](https://img.shields.io/badge/Cardano%20Ada-testnet-orange.svg)

The [Cardano](https://www.cardano.org) command line interface:

* powerful blockchain manager: download, explore, verify, analyse;
* manage multiple wallets: daedalus', icarus' or other kind of wallets;
* flexible transaction build engine.

This command line interface is built upon the
[**Rust Cardano SDK**](https://github.com/input-output-hk/rust-cardano).

## Warning

* The software is currently still in alpha phase, please don't use for
  any other purpose than debugging and testing, until stable releases.
* While most of the operations in the CLI is reading state, and are thus
  relatively safe even in the precense of bugs, do take special note that
  `transaction send` will permanently change your state.
* Consider to test testnet operations (depending on testnet availability)
  before doing mainnet operations.
* If you think, something is suspicious, it may very well be the case.
  Check the documentation, or ask for help.
* Do not share your wallet mnemonics, passwords, cryptographic material, pending signatures.

## Installation guide

While it is recommended to wait for official releases, it is also possible
to build the executable yourself:

1. [install rust toolchain](;https://www.rust-lang.org/en-US/install.html);
2. clone the project repository (with the dependencies)
   ```sh
   git clone https://github.com/input-output-hk/cardano-cli.git --recursive
   ```
3. build and install the binary:
   ```sh
   cd cardano-cli
   cargo install
   ```
4. enjoy

## Usage

### Quick start

```sh
$ cardano-cli blockchain new mainnet
$ cardano-cli blockchain pull mainnet
$ cardano-cli wallet create "My Wallet"
$ cardano-cli wallet attach "My Wallet" mainnet
$ cardano-cli wallet sync   "My Wallet"
$ cardano-cli wallet status "My Wallet"
```

### Complete documentation

[Command line documentation](./USAGE.md)

# Supported platforms

| Target                               | `test` |
|--------------------------------------|:------:|
| `aarch64-unknown-linux-gnu`          |   ✓    |
| `arm-unknown-linux-gnueabi`          |   ✓    |
| `armv7-unknown-linux-gnueabihf`      |   ✓    |
| `i686-unknown-linux-gnu`             |   ✓    |
| `i686-unknown-linux-musl`            |   ✓    |
| `x86_64-unknown-linux-gnu`           |   ✓    |
| `x86_64-unknown-linux-musl`          |   ✓    |
| `i686-apple-darwin`                  |   ✓    |
| `x86_64-apple-darwin`                |   ✓    |
| `x86_64-apple-darwin`                |   ✓    |
| `i686-unknown-freebsd`               |   ✓    |
| `x86_64-unknown-freebsd`             |   ✓    |

# Supported compiler versions

| Rust    | `test` |
|---------|:------:|
| stable  |   ✓    |
| beta    |   ✓    |
| nightly |   ✓    |

We aim to support compiler versions down to 1.30. This is not a contract though.
We might drop support of older compiler with time at our own convenience.

# License

This project is licensed under either of

 * Apache License, Version 2.0, ([LICENSE-APACHE](LICENSE-APACHE) or
   http://www.apache.org/licenses/LICENSE-2.0)
 * MIT license ([LICENSE-MIT](LICENSE-MIT) or
   http://opensource.org/licenses/MIT)

at your option.
