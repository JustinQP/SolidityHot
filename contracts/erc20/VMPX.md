

### 来源

网络：以太坊



https://etherscan.io/address/0xb48eb8368c9c6e9b0734de1ef4ceb9f484b80b9c#code

功能：
消耗gas生成代币。
每消耗6个存储费用产生一个份COIN。

时间：
2023-7-5 占用全网gas使用 52%


### 原理

利用循环写状态到达消耗gas的目的
```solidity
    function _doWork(uint256 power) internal {
        for(uint i = 0; i < cycles * power; i++) {
            _work[++counter] = true;
        }
    }
```



