# KuCoin Community Chain

## Introduction
KuCoin Community Chain (KCC) is a high-performance and decentralized public chain built by KuCoin for all community users.  

Developed based on go-ethereum with the purpose of providing community users with a higher-speed,
convenient and low-cost blockchain user experience.

KuCoin Community Chain (KCC) will have the following characteristics:
- Fully compatible with Ethereum and ERC-20 smart contracts, with extremely low migration costs
- KuCoin Token (KCS) will serve as the only core fuel and native token for KCC and can be used in scenarios such as gas fee payment
- A block every 3 seconds results in faster transaction confirmation and higher chain performance
- Proof of Staked Authority (PoSA) consensus algorithm, high efficiency, security and stability

## Mission

Mission: To accelerate the flow of value around the world without boundaries.

# Network Params
Community users can use any Ethereum compatible wallet to configure with KCC network params, like `metamask`,`myetherwallet`,`imtoken` etc.

## Mainnet (NOT STARTED)

## Testnet
```
Chain Name: KCC-testnet
Chain ID: 322
Symbol: KCS
RPC URL: https://rpc-testnet.kucoin.one
Explorer URL: https://scan-testnet.kucoin.one

Faucet URL: https://faucet-testnet.kucoin.one (for test only, no value)
```

# Developer documentation

## Compilation
### Requirements
- Linux or Mac
- golang >= 1.13
- git

[how to download and install golang](https://golang.org/doc/install)

### Steps
```
git clone -b kcc --single-branch https://github.com/kucoin-community-chain/kcc.git
cd kcc
make geth
```
### Running
The command line flags are similar to go-ethereum, you can use `./build/bin/geth --help` for all command line options,
like `geth --testnet` to join the Testnet.

## Docker

You can use [https://hub.docker.com/r/kucoincommunitychain/kcc](https://hub.docker.com/r/kucoincommunitychain/kcc) to fast deploy and test.

[How to use Docker?](https://docs.docker.com/get-started/)

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

You can use `nohup`,`supervisor`,`systemd` to run and manage `geth` in the background.

- [supervisor](http://supervisord.org/)
- [systemd](https://wiki.debian.org/systemd)

## SDKs
You can use the following SDKs to interact with KCC node rpc.

- [Js: web3.js](https://github.com/kucoin-community-chain/web3.js) Ethereum JavaScript API
- [Java: web3j](https://github.com/web3j/web3j) Web3 Java Ethereum Ðapp API
- [PHP: web3.php](https://github.com/sc0Vu/web3.php) A php interface for interacting with the Ethereum blockchain and ecosystem.
- [Python: Web3.py](https://github.com/ethereum/web3.py) A Python library for interacting with Ethereum, inspired by web3.js.
- [Golang: go-ethereum](https://github.com/ethereum/go-ethereum)

## Consensus
KCC introduces a PoSA consensus mechanism, which features low transaction costs, low transaction delay,
high transaction concurrency, and supports up to 29 validators.

PoSA is a combination of PoA and PoS. To become a validator, you need to submit a proposal first and wait for other active validators to vote on it. After more than half of them voted, you will be eligible to become a validator. Any address can stake to an address that qualifies to become a validator, and after the validator's staking volume ranks in the top 29, it will become an active validator in the next epoch.

All active validators are ordered according to predefined rules and take turns to mine blocks. If a validator fails to mine a block on time during their own round, the active validators who have not been involved in the past n/2 (n is the number of active validators) blocks will randomly perform the block-out. At least n/2+1 active validators work properly to ensure the proper operation of the blockchain.

The difficulty value of a block is 2 when the block is generated normally and 1 when the block is not generated in a predefined order. When a fork of the blockchain occurs, the blockchain selects the corresponding fork according to the cumulative maximum difficulty.

### System Contracts
KCC has made 3 built-in contracts for PoSA in the genesis file.

The source code of those contracts are forked from Heco, you can locate them here: [https://github.com/kucoin-community-chain/kcc-genesis-contracts](https://github.com/kucoin-community-chain/kcc-genesis-contracts)。

The management of the current validators are all done by the system contracts.

- Proposal Responsible for managing access to validators and managing validator proposals and votes.
- Validators Responsible for ranking management of validators, staking and unstaking operations, distribution of block rewards, etc.
- Punish Responsible for punishing operations against active validators who are not working properly.

Blockchain call system contracts：

- At the end of each block, the Validators contract is called and the fees for all transactions in the block are distributed to active validators.
- The Punish contract is called to punish the validator when the validator is not working properly.
- At the end of each epoch, the Validators contract is called to update active validators, based on the ranking.

### stake
You can call the `stake` method in the `validator` contract to stake for any validator, the minimum staking amount for each validator is 32KCS.

### unstake
If you want to `unstake` your KCS, you need to call the `unstake` method in the `validator` contract,
and wait for 86400 blocks(3 days), then call the `withdrawStaking` method in the `validator` contract to make the amount available.

### punish
Whenever a validator is found not to mine a block as predefined, the Punish contract is automatically called at the end of this block and the validator is counted. When the count reaches 24, all income of the validator is punished. When the count reaches 48, the validator is removed from the list of active validators, and the validator is disqualified.

# Governance

## Advice, Issue & Discussion

Any advice, issues and discussion are welcome.

[Leave advice or an issue](https://github.com/kucoin-community-chain/any-advice-issue/issues)

[Start a discussion](https://github.com/kucoin-community-chain/any-advice-issue/discussions)

If you have an issue on a special project, please move to the `issue` page in the special project.


## KIPs
KCC Improvement Proposals

KCC Improvement Proposals (KIPs) describe the standards for the KCC platform, including Chain, DEX, and dApps.

The purpose of this process is to ensure changes to KCC are transparent and well governed.

URL：[https://github.com/kucoin-community-chain/KIPs](https://github.com/kucoin-community-chain/KIPs)


## FAQ
### 如何配置 MetaMask 钱包

Use Chrome browser open MetaMask [extension site](https://chrome.google.com/webstore/detail/metamask/nkbihfbeogaeaoehlefnkodbefgpgknn?hl=zh-CN)

Follow the intro, create your ETH wallet，**backup your private key or mnemonic**；

Config KCC testnet

(1) Open MetaMask，you can see the default config of【Ethereum mainnet】。

![](https://trello-attachments.s3.amazonaws.com/608a2ec80599322eb36f3444/371x614/fe15faa8566a72481c7ee86a320c4531/image.png)


click【Ethereum mainnet】，click【custom RPC】on the drop menu

![](https://trello-attachments.s3.amazonaws.com/608a2ec80599322eb36f3444/371x614/f8a4b49c1a47513d01c38260cbeb6f5a/image.png)

(2) Fill that config value in order change to the KCC testnet：
    Network Name：KCC-Test 
    New RPC URL：https://rpc-testnet.kucoin.one/
    Chain ID: 322
    Currency Symbol (optional)：KCS
    Block Explorer URL (optional):https://scan-testnet.kucoin.one/

![](https://trello-attachments.s3.amazonaws.com/608a2ec80599322eb36f3444/371x614/f86ac1082e601980de9659f9dcb4537a/image.png)

Done

![](https://trello-attachments.s3.amazonaws.com/608a2ec80599322eb36f3444/371x614/c0dc2af90e2f473cba0b9d16c7c8122d/image.png)