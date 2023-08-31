# BDK Wallet

The BDK [`Wallet`] struct provides as high level interface to perform common bitcoin wallet operations. In BDK a wallet encapsulates:

1. the "external" keychain output descriptor 
2. an optional "internal" keychain output descriptor
3. optional signing keys
2. storage for wallet state data
3. a view of the current blockchain
4. an indexed graph of wallet transactions

The common operations that can be performed with a BDK wallet are:

1. get a new address
2. list unspent transaction outputs
3. list transactions
4. get the wallet balance
5. build a new unsigned transaction
6. build a transaction to bump the fee of an unconfirmed transaction
7. sign an unsigned or partially signed transaction
8. finalize a partially signed transaction
9. cancel an unconfirmed transaction

[`Wallet`]: https://docs.rs/bdk/1.0.0-alpha.1/bdk/wallet/struct.Wallet.html