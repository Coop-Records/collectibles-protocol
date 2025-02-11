# Collectibles Protocol

**A smart contract protocol for managing collectibles on Abstract's testnet, built with Foundry.**

Foundry consists of:

- **Forge**: Ethereum testing framework (like Truffle, Hardhat and DappTools).
- **Cast**: Swiss army knife for interacting with EVM smart contracts, sending transactions and getting chain data.
- **Anvil**: Local Ethereum node, akin to Ganache, Hardhat Network.
- **Chisel**: Fast, utilitarian, and verbose solidity REPL.

## Documentation

https://book.getfoundry.sh/

## Setup

### Environment Variables

1. Copy the example environment file:

```shell
cp .env.example .env
```

2. Update the `.env` file with your configuration:

```shell
# RPC URLs
ABSTRACT_TESTNET_RPC_URL=https://api.testnet.abs.xyz
ABSTRACT_VERIFIER_URL=https://api-sepolia.abscan.org/api

# Deployment
PRIVATE_KEY=0xyour_private_key_here
```

## Usage

### Build

```shell
$ forge build
```

### Test

```shell
$ forge test
```

### Format

```shell
$ forge fmt
```

### Gas Snapshots

```shell
$ forge snapshot
```

### Deploy

First, make sure your environment variables are loaded:

```shell
source .env
```

Then run the deployment script:

```shell
forge script script/Counter.s.sol:CounterScript --rpc-url $ABSTRACT_TESTNET_RPC_URL --private-key $PRIVATE_KEY --broadcast --verify --verifier blockscout --verifier-url $ABSTRACT_VERIFIER_URL -vvvv --zksync
```

### Cast

```shell
$ cast <subcommand>
```

### Help

```shell
$ forge --help
$ anvil --help
$ cast --help
```
