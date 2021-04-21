# KuCoin Community Chain

## Introduction
KuCoin Community Chain (KCC) is a high-performance and decentralized public chain built by KuCoin for all community users.  

Developed based on the go-ethereum, the purpose is to provide the community users with a higher-speed,
convenient and low-cost blockchain user experience.

KuCoin Community Chain (KCC) will have the following characteristics:
- Fully compatible with Ethereum and ERC-20 smart contracts, with extremely low migration costs
- KuCoin Token (KCS) will serve as the only core fuel and native token for KCC and can be used in scenarios such as gas fee payment
- A block every 3 seconds results in faster transaction confirmation and higher chain performance
- Proof of Staked Authority(PoSA) consensus algorithm, high efficiency, security and stability

## Mission and Vision

Mission: Promoting Financial Democratization

Vision：Blockchain will greatly accelerate the global free flow of value, allowing everyone to embrace crypto assets

# Network Params
Community users can use any Ethereum compatible wallet to configure with KCC network params, like `metamask`,`myetherwallet`,`imtoken` etc.

## Mainnet
```
Chain Name: KCC
Chain ID: 321
Symbol: KCS
RPC URL: https://rpc.kucoin.org
Explorer URL: https://scan.kucoin.org
```

## Testnet
```
Chain Name: KCC-testnet
Chain ID: 322
Symbol: KCS
RPC URL: https://rpc-testnet.kucoin.one
Explorer URL: https://scan-testnet.kucoin.one

Faucet URL: https://faucet-testnet.kucoin.one
```

# Developer documentation

## Compilation
### Requirements
- Linux or Mac
- golang >= 1.13
- git

### Steps
```
git clone -b kcc --single-branch git@github.com:kucoin-community-chain/kcc.git
cd kcc
make geth
```
### Running
The command line flags are similar to the go-ethereum, you can use `./build/bin/geth --help` for all command line options,
like `geth --testnet` to join the Testnet.

## Deploy

### Requirements
```
4 core cpu
8g memory
scalable SSD disk
public ip with TCP/UDP:30303 open
```

### Start command
```
./geth #Mainnet
./geth --testnet #Testnet

useful options:
/data/kcc/geth \
--datadir /data/.kcc/testnet \ #your data dir
--testnet \ #Testnet
--http \ #http rpc
--ws \ #ws rpc
--http.vhosts * \ #vhosts
--rpccorsdomain * \ #http corsdomain
--http.addr 0.0.0.0 \ #http rpc bind address
--ws.addr 0.0.0.0 \ #ws rpc bind address
--syncmode full \ #syncmode
--gcmode archive #gcmode
```

## SDKs
You can use the following SDKs to interacting with KCC node rpc.

- [Js: web3.js](https://github.com/kucoin-community-chain/web3.js) Ethereum JavaScript API
- [Java: web3j](https://github.com/web3j/web3j) Web3 Java Ethereum Ðapp API
- [PHP: web3.php](https://github.com/sc0Vu/web3.php) A php interface for interacting with the Ethereum blockchain and ecosystem.
- [Python: Web3.py](https://github.com/ethereum/web3.py) A Python library for interacting with Ethereum, inspired by web3.js.
- [Golang: go-ethereum](https://github.com/ethereum/go-ethereum)

## Consensus
KCC introduces a PoSA consensus mechanism, which has the features of low transaction cost, low transaction delay,
and high transaction concurrency, and supports up to 29 validators.

PoSA is a combination of PoA and Pos. To become a validator, you need to submit a proposal first and wait for other active validators to vote on it, after more than half of them pass, you will be eligible to become a validator. Any address can stake to an address that qualifies to become a validator, and after the validator's staking volume ranks in the top 29, it will become an active validator in the next epoch.

All active validators are ordered according to predefined rules and take turns to mine blocks. If a validator fails to mine a block in time in its own round, the active validators who have not involved in the past n/2 (n is the number of active validators) blocks will randomly perform the block-out. At least n/2+1 active validators work properly to ensure the proper operation of the blockchain.

The difficulty value of a block is 2 when the block is generated normally and 1 when the block is not generated in a predefined order. when a fork of the block chain occurs, the block chain selects the corresponding fork according to the cumulative maximum difficulty.

### System Contracts
KCC made 3 built-in contracts for PoSA in genesis file.

The source code of those contracts are forked from Heco, you can locate [https://github.com/kucoin-community-chain/kcc-genesis-contracts](https://github.com/kucoin-community-chain/kcc-genesis-contracts)。

The management of the current validators are all done by the system contracts.

- Proposal Responsible for managing access to validators and managing validator proposals and votes.
- Validators Responsible for ranking management of validators, staking and unstaking operations, distribution of block rewards, etc..
- Punish Responsible for punishing operations against active validators who are not working properly.

Blockchain call system contracts：

- At the end of each block, the Validators contract is called and the fees for all transactions in the block are distributed to active validators.
- The Punish contract is called to punish the validator when the validator is not working properly.
- At the end of each epoch, the Validators contract is called to update active validators, based on the ranking.

### stake
You can call `stake` method in the `validator` contract to stake for any validator, and the minimum staking amount for each validator is 32KCS.

### unstake
If you want to `unstake` your KCS, you need to call `unstake` method in the `validator` contract,
and waiting for 86400 blocks(3 days), then call `withdrawStaking` method in the `validator` contract to make the amount available.

### punish
Whenever a validator is found not to mine block as predefined, the Punish contract is automatically called at the end of this block and the validator is counted. When the count reaches 24, all income of the validator is punished. When the count reaches 48, the validator is removed from the list of active validators, and the validator is disqualified.

# Governance

## KIPs
KCC Improvement Proposals

KCC Improvement Proposals (KIPs) describe standards for the KCC platform, including Chain, Dex, and Dapps.

The purpose of this process is to ensure changes to KCC are transparent and well governed.

URL：[https://github.com/kucoin-community-chain/KIPs](https://github.com/kucoin-community-chain/KIPs)
