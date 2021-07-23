# KCC

## Introduction
KCC is a high-performance and decentralized public chain built by KCS’ and KuCoin’s fan communities.  

Developed based on go-ethereum with the purpose of providing community users with a higher-speed,
convenient and low-cost blockchain user experience.

KCC will have the following characteristics:
- Fully compatible with Ethereum and ERC-20 smart contracts, with extremely low migration costs;
- KCS will serve as the only core fuel and native token for KCC and can be used in scenarios such as gas fee payment;
- A block every 3 seconds results in faster transaction confirmation and higher chain performance;
- Proof of Staked Authority (PoSA) consensus algorithm, high efficiency, security and stability.

## Mission

Mission: To accelerate the flow of value around the world without boundaries.

## Risk statement

- KCC officially will not release any Swap project because all projects are developed by the community.So KCC is not responsible for any inconvenience caused by these projects. Also, KCC does not serve as customer service for relevant projects.
- Before any operations in the fields related to cryptocurrency or DeFi, please first do your own research.
- All users and developers can build the dApp in KCC testnet then the mainnet in the follow-up for free.
- Please distinguish the test environment (the testnet) from the main network environment (the mainnet). The assets generated in the test environment do not have value, so please be careful against the cryptocurrency fraud.
- KCC will announce authorization, promotion and other cooperation through its official social network, please kindly check the official information and avoid phishing sites.
- Please make sure that you are visiting the official website to avoid the loss of private key.

## Disclaimers
Dear user (hereinafter referred to as "you"):

KCC (hereinafter referred to as "KCC" or "we") is a decentralized public chain. Developers around the world can deploy applications on KCC, all users can read, send and trade on KCC. Due to the characteristics of decentralization, we hereby remind you the risks of the third-party DAPP are as follows:

- Before you operate on any platform, wallet or third-party DAPP, please do your own research first;
- Whether you participate in or use DAPP on KCC through any trading platform or wallet, it is your own behavior and we do not recommend it to you;
-  We are not responsible for auditing any third-party DAPP, nor do we make any commitment and guarantee on the validity, accuracy, correctness, reliability, quality, stability, integrity and timeliness of the technology and information involved in its services;
- You should bear all the responsibilities arising from your use of any third-party DAPP services on your own;
- Whether the third-party DAPP services meet the laws, regulations or relevant policies of your jurisdiction, please make your own judgment and evaluation. We do not provide any evaluation, please make sure that you strictly abide by the laws of your jurisdiction;
- You and the third-party DAPP shall assume the responsibilities of any issues related to the usage of the third-party DAPP, including but not limited to legal issues, contractual liability issues, economic losses, etc., KCC will not be responsible for them;
- Unless you authorize us to do so, KCC will not share your personal information with any third-party DAPP. If you authorize us to share the information, all legal liabilities and disputes arising from the access by the third-party DAPP to your personal information shall be assumed by you and the third-party DAPP.
- KCC has no right to provide you with the personal information of any third-party DAPP developers unless they agree to do so. We will assist in this issue however we cannot guarantee that the information can be obtained.

Finally, we need to reiterate that we do not recommend or ask you to use any third-party DAPP service.

# Network Params
Community users can use any Ethereum compatible wallet to configure with KCC network params, like [metamask](https://metamask.io/), [myetherwallet](https://www.myetherwallet.com/), [imtoken](https://token.im/), [TokenPocket](https://www.tokenpocket.pro/) etc.

## Mainnet
```
Chain Name: KCC-MAINNET
Chain ID: 321
Symbol: KCS
RPC URL: https://rpc-mainnet.kcc.network
Explorer URL: https://explorer.kcc.io/en
WebSocket RPC URL: wss://rpc-ws-mainnet.kcc.network
```

## Testnet
```
Chain Name: KCC-TESTNET
Chain ID: 322
Symbol: KCS
RPC URL: https://rpc-testnet.kcc.network
Explorer URL: https://scan-testnet.kcc.network
WebSocket RPC URL: wss://rpc-ws-testnet.kcc.network

Faucet URL: https://faucet-testnet.kcc.network (for test only, no value)
```

# Developer 

## Node
### Binary file
You can directly visit[https://github.com/kcc-community/kcc/releases](https://github.com/kcc-community/kcc/releases) to download the latest version of the binary file。

### Docker
Or you can visit [https://hub.docker.com/r/kucoincommunitychain/kcc](https://hub.docker.com/r/kucoincommunitychain/kcc) to rapid deployment and testing。([How t use Docker？](https://docs.docker.com/get-started/))

### Compilation
#### Requirements
- Linux or Mac
- golang >= 1.13
- git

[how to download and install golang](https://golang.org/doc/install)

#### Steps
```
git clone -b kcc --single-branch https://github.com/kcc-community/kcc.git
cd kcc
make geth
```
#### Running
The command line flags are similar to go-ethereum, you can use `./build/bin/geth --help` for all command line options,
like `./build/bin/geth --testnet` to join the Testnet. Caution: Use the specific "geth" version located at `./build/bin/geth`.

## Docker

You can use [https://hub.docker.com/r/kucoincommunitychain/kcc](https://hub.docker.com/r/kucoincommunitychain/kcc) to fast deploy and test.

[How to use Docker?](https://docs.docker.com/get-started/)

## Deploy

### Requirements
```
4 core cpu
8g memory
200G and scalable SSD
public ip with TCP/UDP:30303 open
```

#### Start command
```
./geth  #Mainnet
./geth --testnet #Testnet

useful options:
/data/kcc/geth \
--datadir /data/.kcc/testnet \ #your data dir
--testnet \ #Testnet
--http \ #http rpc
--http.addr 0.0.0.0 \ #http rpc bind address
--http.vhosts * \ #vhosts
--http.corsdomain * \ #http corsdomain
--ws \ #ws rpc
--ws.addr 0.0.0.0 \ #ws rpc bind address
--syncmode full \ #syncmode
--gcmode archive #gcmode
```

You can use `nohup`,`supervisor`,`systemd` to run and manage `geth` in the background.

- [supervisor](http://supervisord.org/)
- [systemd](https://wiki.debian.org/systemd)

## SDKs
You can use the following SDKs to interact with KCC node rpc.

- [Js: web3.js](https://github.com/ChainSafe/web3.js) Ethereum JavaScript API
- [Java: web3j](https://github.com/web3j/web3j) Web3 Java Ethereum Ðapp API
- [PHP: web3.php](https://github.com/sc0Vu/web3.php) A php interface for interacting with the Ethereum blockchain and ecosystem.
- [Python: Web3.py](https://github.com/ethereum/web3.py) A Python library for interacting with Ethereum, inspired by web3.js.
- [Golang: go-ethereum](https://github.com/ethereum/go-ethereum)

## Tools
- [Solidity](https://docs.soliditylang.org/en/latest/)
- [Remix](https://remix.ethereum.org/)
- [Truffle](https://www.trufflesuite.com/docs/truffle/overview)
- [Faucet](https://faucet-testnet.kcc.network)
- [Explorer](https://explorer.kcc.io)

## Bridge
- [KCC-Bridge](https://www.kcc.io/#/bridge/transfer)
- [AnySwap](https://anyswap.exchange/bridge)

## Consensus
KCC introduces a PoSA consensus mechanism, which features low transaction costs, low transaction delay,
high transaction concurrency, and supports up to 29 validators.

PoSA is a combination of PoA and PoS. To become a validator, you need to submit a proposal first and wait for other active validators to vote on it. After more than half of them voted, you will be eligible to become a validator. Any address can stake to an address that qualifies to become a validator, and after the validator's staking volume ranks in the top 29, it will become an active validator in the next epoch.

All active validators are ordered according to predefined rules and take turns to mine blocks. If a validator fails to mine a block on time during their own round, the active validators who have not been involved in the past n/2 (n is the number of active validators) blocks will randomly perform the block-out. At least n/2+1 active validators work properly to ensure the proper operation of the blockchain.

The difficulty value of a block is 2 when the block is generated normally and 1 when the block is not generated in a predefined order. When a fork of the blockchain occurs, the blockchain selects the corresponding fork according to the cumulative maximum difficulty.

### System Contracts
KCC has made 3 built-in contracts for PoSA in the genesis file.

The source code of those contracts are forked from Heco, you can locate them here: [https://github.com/kcc-community/kcc-genesis-contracts](https://github.com/kcc-community/kcc-genesis-contracts)。

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

[Leave advice or an issue](https://github.com/kcc-community/any-advice-issue/issues)

[Start a discussion](https://github.com/kcc-community/any-advice-issue/discussions)

If you have an issue on a special project, please move to the `issue` page in the special project.


## KIPs
KCC Improvement Proposals

KCC Improvement Proposals (KIPs) describe the standards for the KCC platform, including Chain, DEX, and dApps.

The purpose of this process is to ensure changes to KCC are transparent and well governed.

URL：[https://github.com/kcc-community/KIPs](https://github.com/kcc-community/KIPs)

# FAQ
1.What is the consensus mechanism of KCC?

>KCC adopts the PoSA consensus mechanism, featuring with low cost, high performance and stable block generation, supporting up to 29 validator nodes;

2.How to become a KCC validator node?

>To become a validator, you need to create a node and submit a proposal, and wait for other active validators to vote. After receiving more than half of the votes, you are eligible to become a validator. Any address can stake the address that is eligible to become a validator. After the validator's staked amount ranks in the top 29, the validator will become an active one in the next epoch.

3.Does KCC support EVM?

>KCC fully supports EVM and is completely friendly to Ethereum developers.

4.What SDK does KCC use?

>KCC is highly compatible with Ethereum, so we adopt the sdk of Ethereum such as web3js, web3j, etc.

5.I want to carry out some operations and tests on the KCC testnet. Where can I get test tokens?

>You can visit our testnet faucet: https://faucet-testnet.kcc.network.

6.How to stake contract nodes?

>Users can call the stake method of the validator contract to stake any node. The minimum staked amount for each validator is 32 KCS.

7.How to unlock the staked amount?

>If users want to retrieve the staked KCS, they need to call the unstake method of the validators contract to unlock the staked amount. After 86,400 blocks were generated (3 days), call the withdrawStaking method of the validators contract to get the staked KCS back.

8.Get stuck when using MetaMask (including but not limited to transfer stuck or delay, problem of data display, etc.)

>Use the plug-in expand view to display at full screen, which can be more stable or choose "Accelerate" to increase gaslimt and gasPrice.

## How to configure MetaMask Wallet

Use Chrome browser open MetaMask [extension site](https://chrome.google.com/webstore/detail/metamask/nkbihfbeogaeaoehlefnkodbefgpgknn?hl=zh-CN)

Follow the intro, create your ETH wallet，**backup your private key or mnemonic**；

Config KCC Mainnet

(1) Open MetaMask，you can see the default config of【Ethereum mainnet】。

<img width="170" alt="E1" src="https://user-images.githubusercontent.com/13411690/121641021-3f093900-cac1-11eb-9c06-fd653cd598a1.png">


click【Ethereum mainnet】，click【custom RPC】on the drop menu

<img width="170" alt="E2" src="https://user-images.githubusercontent.com/13411690/121641049-4597b080-cac1-11eb-8674-3755c30a3398.png">


(2) Fill that config value in order change to the KCC Mainnet：

    Network Name：KCC-MAINNET
    
    New RPC URL：https://rpc-mainnet.kcc.network
    
    Chain ID: 321
    
    Currency Symbol (optional)：KCS
    
    Block Explorer URL (optional):https://explorer.kcc.io/en

<img width="170" alt="E3" src="https://user-images.githubusercontent.com/13411690/121641889-598fe200-cac2-11eb-92c5-6617c103ebee.png">




Done

<img width="170" alt="E4" src="https://user-images.githubusercontent.com/13411690/121641085-51837280-cac1-11eb-80cd-1a208c0bcd54.png">
