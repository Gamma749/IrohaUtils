# Iroha Utilities
## Hayden McAlister
---

This repository holds utilities developed for working with the [Iroha blockchain](https://www.hyperledger.org/use/iroha). The utilities offer a slightly easier pathway into interacting with the Iroha blockchain by offering utility methods that encapsulate often repeated code.

`IrohaUtils.py` is the backbone/setup for these utilities, setting variables for the other utilities to use. In particular, ensure that your local copy sets the correct IP addresses and ports for you Iroha nodes. The admin private key is also set from the default/example gensis block in the Iroha docs, but this can also be changed quite easily. Otherwise, this file offers easier ways to send transactions, get and log blocks, and create new users.

`IrohaHashCustodian.py` is a more specalised utility that was designed to log hashes on the Iroha blockchain (something that Iroha is not specalised in). The hash custodian offers the ability to hash any serializable object, then log that hash on-chain in a domain managed by the custodian. The hash custodian also employes a blockstore that caches the blocks seen to avoid extra calls to the chain.

For examples of these utilities in use see [this project](https://github.com/Gamma749/Hypderledger-Iroha-Multinode-Demo) for the `IrohaUtils.py` utilities, and [this project](https://github.com/Gamma749/IrohaFileHashing) for the `IrohaHashCustodian.py` in action.

Also, see the `pydocs` directory in this repo for more information on these utilities.
