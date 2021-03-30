# 库币社区链

## 社区链简介
库币社区链KuCoin Community Chain(KCC)是库币**为广大社区用户**构建的，基于以太坊的，高性能和去中心化的公链，**目的是为广大社区用户提供更加高速便捷并且低成本的区块链使用体验**。

KCC具有如下特性：
- 完全兼容以太坊和ERC20智能合约，迁移成本极低
- 以KCS作为链的gas费，成本极低
- 每3秒出一个块，交易确认更快，链性能更高
- Proof of Staked Authority(PoSA)共识算法，效率高，安全稳定

## 平台简介
库币是全球知名的数字货币交易所，支持多种数字资产交易。成立于2017年9月，库币已成长为最受欢迎的数字货币交易所之一，目前为全球207个国家和地区的600万用户提供币币、法币、合约、Pool-X、借贷等一站式服务。据Alexa全球网站排名显示，库币访问率常年在业内排名前五。

以“全民的交易所”著称，库币的运营地为塞舌尔，为用户提供多语言、7X24小时客服团队，同时，库币在韩国、日本、西班牙、意大利、越南、土耳其、俄罗斯、印度等地建立了本地化社群，为各地用户提供最本地化的服务。目前，全球每4个数字货币持有者就有1个是库币用户。

库币交易所已推出IOS和Android版App，用户可前往应用商城下载，7*24随时随地进行交易。

2018年11月，库币获得来自IDG资本和经纬创投的2000万美元A轮融资。

## 使命和愿景



# 网络参数
社区用户可以使用任何以太坊的钱包，并配置KCC链的网络参数，如`metamask`,`myetherwallet`,`imtoken`等。

## 主网
```
网络名称:KCC
链ID:321
符号:KCS
RPC地址:https://rpc.kucoin.org
浏览器地址:https://scan.kucoin.org
```

## 测试网
```
网络名称:KCC-testnet
链ID:322
符号:KCS
RPC地址:https://rpc-testnet.kucoin.org
浏览器地址:https://scan-testnet.kucoin.org
```

# 共识
KCC采用PoSA共识机制，具有成本低、性能高、出块稳的特点，支持最多21个验证人节点；

PoSA结合了PoS和PoA，想要成为验证人，需要先创建节点并提交提案，等待其他活跃的验证人进行投票，半数以上通过之后，则有资格成为验证人。任意地址均可对有资格成为验证人的地址进行质押，当验证人的质押量排名进入前21位之后，则会在下一个epoch成为活跃验证人。

所有的活跃验证人按照预定规则排序，轮流进行出块。如果有验证人在自己的出块轮次没能及时出块，则在过去n/2(n为活跃验证人的数量)个块内，没有参与过出块操作的活跃验证人，随机进行出块。最少n/2+1个活跃验证人正常工作，即可保证区块链的正常运行。

正常产块时，区块的难度值为2，未按照预定顺序进行产块时，区块的难度值为1。当区块链发生分叉时，区块链按照累计最大难度选择对应分叉。

## 内置合约
KCC在genesis文件中内置了PoSA共识相关的合约，
合约源代码fork自heco，可在[https://github.com/kucoin-community-chain/kcc-genesis-contracts](https://github.com/kucoin-community-chain/kcc-genesis-contracts)查看。

目前验证人的管理，均由系统合约完成，目前的系统合约有：
- proposal 负责管理验证人的准入资格，管理验证人提案和投票；
- validators 负责对验证人进行排名管理、质押和解质押操作、分发区块奖励等；
- punish 负责对不正常工作的活跃验证人进行惩罚操作；

区块链调用系统合约：
- 每个块结束的时候，会调用validators合约，将区块中所有交易的手续费分发给active validator;
- 发现validator没有正常工作的时候，会调用punish合约，对validator进行惩罚；
- 每个epoch结束的时候，会调用validators合约，根据排名，更新active validator；


## 质押
用户可以调用validator合约的`stake`方法，对任意节点进行质押，每个validator的最小质押量是32KCS。

## 解质押
如果用户想取回质押的KCS，需要先调用validators合约的`unstake`方法进行解质押，然后在86400个块之后(3天)，再调用validators合约的`withdrawStaking`方法才能把质押的KCS取回到可用余额。

## 惩罚
如果验证人没有按照预定规则进行出块，就会在这个块结束时，自动调用punish合约，对验证人进行计数。当计数达到24次时，罚没验证人的所有收入。当计数达到48次时，将验证人移除出活跃验证人列表，同时取消验证人资格。

# 开发者文档

## 编译
### 编译要求
- Linux or Mac
- golang >= 1.13
- git

### 编译步骤
```
git clone -b kcc --single-branch git@github.com:kucoin-community-chain/kcc.git
cd kcc
make geth
```
### 启动
启动参数配置和以太坊类似，可以通过`./build/bin/geth --help`查看所有的参数配置，可以通过`geth --testnet`加入测试网。

## 部署

### 推荐配置
```
4核
8G内存
可扩容的SSD
公网IP并开启TCP/UDP:30303端口
```

### 启动命令
```
./geth #主网
./geth --testnet #测试网

部分常用参数示例：
/data/kcc/geth \
--datadir /data/.kcc/testnet \ #自定义数据目录
--testnet \ #测试网
--http \ #开启http rpc
--ws \ #开启ws rpc
--http.vhosts * \ #vhosts
--rpccorsdomain * \ #http corsdomain
--http.addr 0.0.0.0 \ #http rpc监听地址
--ws.addr 0.0.0.0 \ #ws rpc监听地址
--syncmode full \ #同步模式
--gcmode archive #gc模式
```