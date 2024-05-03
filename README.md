# Whirlpool

## Chaumian CoinJoin implementation by the developers of [Samourai Wallet](https://samouraiwallet.com)

Whirlpool is a framework backed up by a collection of software tools that mathematically disassociates the ownership of inputs to outputs in a given bitcoin transaction. This is to increase the privacy of the users involved, protect against financial surveillance, and to increase the fungibility of the Bitcoin network as a whole.

Whirlpool is a fully modular CoinJoin implementation based on a heavily modified fork of the ZeroLink theory. You can [review the theory](THEORY.md) or [review the architecture](ARCHITECTURE.md) in further detail.

**Current Status - PUBLIC BETA**

### What makes Whirlpool different

- **Fast**
  - Focusing on many smaller CoinJoin cycles instead of a single large cycle allows for a theoretical anonymity set that grows exponentially in minutes instead of hours.
  
- **Portable**
  - Modular architecture allows Whirlpool to be embedded anywhere. Our focus on creating a system that can handle the limitations of a mobile environment has created a robust protocol usable under most conditions.
  
- **Usable**
  - Focusing on the spending by enforcing best practices to prevent privacy damaging pitfalls automatically without the user needing to intervene. A simple UX that feels familiar to most users.
  
- **Strong**
  - Structurally built on a strong mathematical foundation. Each Whirlpool cycle:
    - **100%** maximum entropy (10.54 bits)
    - **1496** possible interpretations
    - **Never** any deterministic links between inputs and outputs
    - **Never** cycle with yourself
    - **Never** cycle with UTXOs seen in a previous cycle.


## Using Whirlpool
Whirlpool requires the use of a blinded coordinator server to pass messages between clients. This server doesn't and crucially **cannot** know the contents of the messages it is passing. The following clients have been created and open sourced by the developers of Samourai Wallet and offer unrestricted access to the Samourai operated coordinator server.

**NOTE** - Whirlpool is currently in a **public beta** state. While we are confident in the architecture and the core functionality, it is essential to keep Whirlpool up to date throughout the development cycle.

### Windows, OSX, Linux

- An electron/react GUI desktop client is available on Windows, OSX, and most flavors of Linux. See [`whirlpool-gui`](https://github.com/noosphere888/whirlpool-gui) repository.

### Mobile

- [Samourai Wallet](https://samouraiwallet.com)

### Developers

- A [REST API](https://github.com/noosphere888/whirlpool-client-cli/blob/develop/README-API.md) is made available to quickly bootstrap your own applications on top of Whirlpool.
- Java and Android libraries can be found within the [`whirlpool-client`](https://github.com/noosphere888/whirlpool-client) repository.
- A command line client is also available. You can find more information within the [`whirlpool-client-cli`](https://github.com/noosphere888/whirlpool/whirlpool-client-cli) repository.

