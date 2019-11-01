DASH API Docs
===========
getBestBlockHash
```````````
返回最新区块的哈希。

定义::

    GET /dash/getBestBlockHash/

请求示例::

    GET /dash/getBestBlockHash/

返回:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
    "data": "000000000000002056c37f7d57864341be0cc01b79c7dfb68350abd831bb50d7"
 }

getBlockByHash
```````````
根据区块hash返回指定区块。


定义::

    GET /dash/getBlockByHash?hash={hash}    //hash (string) 

请求示例::

    GET /dash/getBlockByHash?hash=000000000000002056c37f7d57864341be0cc01b79c7dfb68350abd831bb50d7

返回:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
    "data": {
        "m": {
        "hash": "000000000000002056c37f7d57864341be0cc01b79c7dfb68350abd831bb50d7",
        "confirmations": 2,
        "size": 10940,
        "height": 1158713,
        "version": 536870912,
        "versionHex": "20000000",
        "merkleroot": "a9ea98c84ce1d538c332e65d1db9de65f7cdb80783a0e0121097993073e60bac",
        "tx": [
            "11f15873f50e55de555729d76dd3d9189cfda6042a3807bb3a0529f80722dac2",
            "4bf438829fe339265f704f3eb62f32ca6db78faa6663a58736a9fa750dc4c022",
            "02a053ca2fcc6c5be98b5701608c6d3ce1f3363ae24cadde189c49293285045d",
            "14e2099bc5e173aee2e18cfdbc228edb850e1181aec7260668b8416815367835",
            "ff624e5970c4716d6d1b78b39ae50edc46fe0c66bb6038a6fe5a05dd4791ebdc",
            "db3c3406a8ec947e21bb56f243e5eb4ffa28adf9be8a6adff06a8cb044d6dca6",
            "e7b6c39a1a178eb8889cbfab8001dbc167e03b49be2e7fbd8a5320b2d3a61de2",
            "64aeaacbcbb9fb6842bc80144e19ccbfaa49b7ca1e438c4c35023376a4768a1b",
            "add2bff452a81710b46cd269d49a21506437c8959409b0f6861664263b19baf8"
        ],
        "cbTx": {
            "version": 2,
            "height": 1158713,
            "merkleRootMNList": "2ef31ada7aa72d5f5215fbd978c47f4ee7b68d293ce68d3b1b2a84fcbc777bc9",
            "merkleRootQuorums": "812ff025ba417a6deb37fc1e0e5f35678665202e09db7e2a31d0b67ce181d187"
        },
        "time": 1571814866,
        "mediantime": 1571814640,
        "nonce": 3600838889,
        "bits": "19240c41",
        "difficulty": 119144408.2195601,
        "chainwork": "000000000000000000000000000000000000000000001f71b3ca52972d74626f",
        "previousblockhash": "00000000000000175d2d0a1c8c4b081b745e066d235af284eea184285cc68297",
        "nextblockhash": "00000000000000074ce217b129e141632aaa9d2b93a400d3137243d361bf4139",
        "chainlock": true
        }
    }
 }

返回:

.. code-block:: json

 {
    "hash" : "hash",     (string) 块哈希（与提供的相同）
    "confirmations" : n,   (numeric) 确认数，如果该块不在主链上，则为-1
    "size" : n,            (numeric) 块大小
    "height" : n,          (numeric) 块高或索引
    "version" : n,         (numeric) 块版本
    "versionHex" : "00000000", (string) 十六进制格式的块版本
    "merkleroot" : "xxxx", (string) 
    "tx" : [               (array of string) 交易信息
        "transactionid"     (string) 交易id
        ,...
    ],
    "time" : ttt,          (numeric) 自时间段以来的阻止时间（以秒为单位）（格林尼治标准时间1970年1月1日）
    "mediantime" : ttt,    (numeric) 自历元（1970年1月1日格林威治标准时间）以来的平均阻止时间，以秒为单位
    "nonce" : n,           (numeric) 随机数
    "bits" : "1d00ffff", (string) 比特
    "difficulty" : x.xxx,  (numeric) 困难度
    "chainwork" : "xxxx",  (string) 生成此区块之前的链所需的哈希数（以十六进制表示）
    "nTx" : n,             (numeric) 区块中的交易数量
    "previousblockhash" : "hash",  (string) 上一个区块的哈希
    "nextblockhash" : "hash"       (string) 下一块的哈希
 }

getBlockByHeight
```````````
根据区块高度返回指定区块。


定义::

    GET /dash/getBlockByHeight?height={height}   //height (Integer)
请求示例::

    GET /dash/getBlockByHeight?height=1158713

返回:

.. code-block:: json

 {
  "status": 0,
  "message": "success",
  "data": {
        "m": {
        "hash": "000000000000002056c37f7d57864341be0cc01b79c7dfb68350abd831bb50d7",
        "confirmations": 2,
        "size": 10940,
        "height": 1158713,
        "version": 536870912,
        "versionHex": "20000000",
        "merkleroot": "a9ea98c84ce1d538c332e65d1db9de65f7cdb80783a0e0121097993073e60bac",
        "tx": [
            "11f15873f50e55de555729d76dd3d9189cfda6042a3807bb3a0529f80722dac2",
            "4bf438829fe339265f704f3eb62f32ca6db78faa6663a58736a9fa750dc4c022",
            "02a053ca2fcc6c5be98b5701608c6d3ce1f3363ae24cadde189c49293285045d",
            "14e2099bc5e173aee2e18cfdbc228edb850e1181aec7260668b8416815367835",
            "ff624e5970c4716d6d1b78b39ae50edc46fe0c66bb6038a6fe5a05dd4791ebdc",
            "db3c3406a8ec947e21bb56f243e5eb4ffa28adf9be8a6adff06a8cb044d6dca6",
            "e7b6c39a1a178eb8889cbfab8001dbc167e03b49be2e7fbd8a5320b2d3a61de2",
            "64aeaacbcbb9fb6842bc80144e19ccbfaa49b7ca1e438c4c35023376a4768a1b",
            "add2bff452a81710b46cd269d49a21506437c8959409b0f6861664263b19baf8"
        ],
        "cbTx": {
            "version": 2,
            "height": 1158713,
            "merkleRootMNList": "2ef31ada7aa72d5f5215fbd978c47f4ee7b68d293ce68d3b1b2a84fcbc777bc9",
            "merkleRootQuorums": "812ff025ba417a6deb37fc1e0e5f35678665202e09db7e2a31d0b67ce181d187"
        },
        "time": 1571814866,
        "mediantime": 1571814640,
        "nonce": 3600838889,
        "bits": "19240c41",
        "difficulty": 119144408.2195601,
        "chainwork": "000000000000000000000000000000000000000000001f71b3ca52972d74626f",
        "previousblockhash": "00000000000000175d2d0a1c8c4b081b745e066d235af284eea184285cc68297",
        "nextblockhash": "00000000000000074ce217b129e141632aaa9d2b93a400d3137243d361bf4139",
        "chainlock": true
        }
  }
 }

返回:

.. code-block:: json

 {
        "hash" : "hash",     (string) 块哈希（与提供的相同）
        "confirmations" : n,   (numeric) 确认数，如果该块不在主链上，则为-1
        "size" : n,            (numeric) 块大小
        "height" : n,          (numeric) 块高或索引
        "version" : n,         (numeric) 块版本
        "versionHex" : "00000000", (string) 十六进制格式的块版本
        "merkleroot" : "xxxx", (string) 
        "tx" : [               (array of string) 交易信息
            "transactionid"     (string) 交易id
            ,...
        ],
        "time" : ttt,          (numeric) 自时间段以来的阻止时间（以秒为单位）（格林尼治标准时间1970年1月1日）
        "mediantime" : ttt,    (numeric) 自历元（1970年1月1日格林威治标准时间）以来的平均阻止时间，以秒为单位
        "nonce" : n,           (numeric) 随机数
        "bits" : "1d00ffff", (string) 比特
        "difficulty" : x.xxx,  (numeric) 困难度
        "chainwork" : "xxxx",  (string) 生成此区块之前的链所需的哈希数（以十六进制表示）
        "nTx" : n,             (numeric) 区块中的交易数量
        "previousblockhash" : "hash",  (string) 上一个区块的哈希
        "nextblockhash" : "hash"       (string) 下一块的哈希
    }

getBlockChainInfo
```````````
返回区块链的当前状态。

定义::

    GET /dash/getBlockChainInfo
请求示例::

    GET /dash/getBlockChainInfo

返回:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
    "data": {
        "m": {
        "chain": "main",
        "blocks": 1158718,
        "headers": 1158718,
        "bestblockhash": "00000000000000075c5ea13ea35f6eaec10fe04090caba3517f7b67a1e2f0c39",
        "difficulty": 152787443.6043571,
        "mediantime": 1571814857,
        "verificationprogress": 0.9999998938525501,
        "chainwork": "000000000000000000000000000000000000000000001f71dd358976a87cabde",
        "pruned": false,
        "softforks": [
            {
            "id": "bip34",
            "version": 2,
            "reject": {
                "status": true
            }
            },
            {
            "id": "bip66",
            "version": 3,
            "reject": {
                "status": true
            }
            },
            {
            "id": "bip65",
            "version": 4,
            "reject": {
                "status": true
            }
            }
        ],
        "bip9_softforks": {
            "csv": {
            "status": "active",
            "startTime": 1486252800,
            "timeout": 1517788800,
            "since": 622944
            },
            "dip0001": {
            "status": "active",
            "startTime": 1508025600,
            "timeout": 1539561600,
            "since": 782208
            },
            "dip0003": {
            "status": "active",
            "startTime": 1546300800,
            "timeout": 1577836800,
            "since": 1028160
            },
            "dip0008": {
            "status": "active",
            "startTime": 1557878400,
            "timeout": 1589500800,
            "since": 1088640
            },
            "bip147": {
            "status": "active",
            "startTime": 1524477600,
            "timeout": 1556013600,
            "since": 939456
            }
        }
        }
    }
 }

返回:

.. code-block:: json

 {
    "chain": "xxxx",              (string) BIP70中定义的当前网络名称（主要，测试，regtest）
    "blocks": xxxxxx,             (numeric) 服务器中当前处理的块数
    "headers": xxxxxx,            (numeric) 我们已验证的标头的当前数量
    "bestblockhash": "...",       (string) 当前最佳块的哈希
    "difficulty": xxxxxx,         (numeric) 目前的困难
    "mediantime": xxxxxx,         (numeric) 当前最佳区块的中位时间
    "verificationprogress": xxxx, (numeric) 验证进度估算[0..1]
    "chainwork": "xxxx"     (string) 活动链中的工作总数，以十六进制表示
    "pruned": xx,                 (boolean) 如果块需要修剪
    "pruneheight": xxxxxx,        (numeric) 已存储最低高度的完整块（仅在启用修剪后才存在）
    "softforks": [                (array) 正在进行的软叉状态
        {
            "id": "xxxx",           (string) 软叉的名称
            "version": xx,          (numeric) 块版本
            "reject": {             (object) 拒绝软叉前的进展
            "status": xx,        (boolean) 如果达到阈值，则为true
            },
        }, ...
    ],
    "bip9_softforks": {          (object) BIP9软叉的状态
        "xxxx" : {                (string) 软叉的名称
            "status": "xxxx",    (string) "defined", "started", "locked_in", "active", "failed" 其中之一
            "bit": xx,             (numeric) 块版本字段中的位（0-28），用于向该软叉发送信号（仅用于“已启动”状态）
            "period": xx,        (numeric) BIP9信令周期的块长度
            "threshold": xx,     (numeric) 激活功能所需的版本位已设置的块数
            "windowStart": xx,     (numeric) 当前窗口的起始块高度（仅适用于“已启动”状态）
            "windowBlocks": xx,    (numeric) 当前窗口中已为此软叉设置版本位的块数（仅适用于“已启动”状态）
            "windowProgress": xx,  (numeric) 激活此软叉的进度（0到1之间）（仅适用于“已启动”状态）
            "startTime": xx,        (numeric) 该位获得其含义的最小经过块的中值时间
            "timeout": xx,          (numeric) 如果尚未锁定，则认为已部署失败的块经过的中值时间
            "since": xx,            (numeric) 该状态适用的第一个块的高度
        }
    }
 }



getBlockCount
```````````
返回本地最长链中的区块数量。

定义::

    GET /dash/getBlockCount
请求示例::

    GET /dash/getBlockCount

返回:

.. code-block:: json

   {
    "status": 0,
    "message": "success",
    "data": 1158719
 }

getBlockHash
```````````
返回在本地最长链中指定高度区块的哈希。

定义::

    GET /dash/getBlockHash?heighth={height}
请求示例::

    GET /dash/getBlockHash?heighth=6666

返回:

.. code-block:: json

   {
    "status": 0,
    "message": "success",
    "data": "000000009c0010bf59231db4a6ae07df4b68fb1b49b7fbf6081a143d71ae8159"
 }

getDifficulty
```````````
返回当前的出块难度。

定义::

    GET /dash/getDifficulty
请求示例::

    GET /dash/getDifficulty

返回:

.. code-block:: json

   {
    "status": 0,
    "message": "success",
    "data": 164078454.4259512
 }


getRawMemPool
```````````
返回节点交易池中的所有交易。

定义::

    GET /dash/getRawMemPool
请求示例::

    GET /dash/getRawMemPool

返回:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
    "data": [
        "b4e43f83e24e91be928b53b086c49a9f76c97528b70938f53182dac0ea96df23",
        "1bdfa3873fafb881ab17fdad8f906fe24c301d80aff978d6ec27a8f6e7f2437c",
        "2c24bb228f28fbf61e4a8e934fc5d1e49feaf7c3640b2ff604ca1511e60d0708",
        "73018a6f83e577eda827f19d0570b9edd690bcc656a57c382d095472006f89f3"
    ]
 }


gettxout
```````````
返回一个UTXO的详细信息。

Params:

1."hash"             (string, required) UTXO‘s 交易id

2."vouth"                (numeric, required) 交易输出中的UTXO序列号

3."unconfirmed"  (boolean, optional) 是否包括内存池。 默认值：false。 请注意，不会显示在内存池中花费的未用输出。

定义::

    GET /dash/gettxout?hash={hash}&vouth={vouth}&unconfirmed={unconfirmed}
请求示例::

    GET /dash/gettxout?hash=xxx&vouth=1&unconfirmed=false

返回:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
    "data": {
        "m": {
        "bestblock": "00000000000000046b7545928489f397bace1a91c5562940a6a565a75639595d",
        "confirmations": 8343,
        "value": 0.25182372,
        "scriptPubKey": {
            "asm": "OP_DUP OP_HASH160 5b2e99dce6f51c6e748dd7e35105ac72ad1274b4 OP_EQUALVERIFY OP_CHECKSIG",
            "hex": "76a9145b2e99dce6f51c6e748dd7e35105ac72ad1274b488ac",
            "reqSigs": 1,
            "type": "pubkeyhash",
            "addresses": [
            "Xizy9c7KzgbZA6ZjNaZRU4B9b6sT1BVzCt"
            ]
        },
        "coinbase": false
        }
    }
 }

返回:

.. code-block:: json

 {
  "bestblock":  "hash",    (string) 链末端的区块哈希
  "confirmations" : n,       (numeric) 确认数
  "value" : x.xxx,           (numeric) dash中的交易价值
  "scriptPubKey" : {         (json object)
     "asm" : "code",       (string)
     "hex" : "hex",        (string)
     "reqSigs" : n,          (numeric) 所需签名数
     "type" : "pubkeyhash", (string) 类型，例如pubkeyhash
     "addresses" : [          (array of string) 比特币地址数组
        "address"     (string) dash 地址
        ,...
     ]
  },
  "version" : n,            (numeric) 版本
  "coinbase" : true|false   (boolean) 是否有Coinbase
 }
            

getTxOutSetInfo
```````````
返回确认的UTXO集合的统计信息。注意该调用 的执行可能需要一定时间，而且该调用只会计算来自确认交易的输出， 它不会考虑来自交易池的输出。


定义::

    GET /dash/getTxOutSetInfo
请求示例::

    GET /dash/getTxOutSetInfo

返回:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
    "data": {
        "m": {
        "height": 1158721,
        "bestblock": "00000000000000046b7545928489f397bace1a91c5562940a6a565a75639595d",
        "transactions": 1094306,
        "txouts": 4224612,
        "hash_serialized_2": "9cd91533290b9fd2bbaf3b0b4a8d419bd6e8f0b484d78950a083f661909cdd42",
        "disk_size": 218388088,
        "total_amount": 9109644.01166697
        }
    }
 }

返回:

.. code-block:: json

 {
    "height":n,     (numeric) 当前块高（索引）
    "bestblock": "hex",   (string) 链末端的区块哈希
    "transactions": n,      (numeric) 未使用输出的事务数
    "txouts": n,            (numeric) 未使用的交易输出数
    "bogosize": n,          (numeric) UTXO集大小的无意义指标
    "hash_serialized_2": "hash", (string) 序列化的哈希
    "disk_size": n,         (numeric) 磁盘上链环状态的估计大小
    "total_amount": x.xxx          (numeric) 总量
  }


verifyChain
```````````
验证本地区块链数据库中的数据。

定义::

    GET /dash/verifyChain
请求示例::

    GET /dash/verifyChain

返回:

.. code-block:: json

 {
  "status": 0,
  "message": "success",
  "data": true
 }


verifyChainByParam
```````````
通过参数验证本地区块链数据库中的数据。

Params:
1. checklevel   （数字，可选，0-4，默认值= 3）块验证的彻底程度

2. nblocks      （数字，可选的，缺省值=6，0 =全部）的块，以检查所述的数

定义::

    GET /dash/verifyChainByParam?checkLevel={checkLevel}&numOfBlocks={numOfBlocks}
请求示例::

    GET /dash/verifyChainByParam?checkLevel=3&numOfBlocks=6

返回:

.. code-block:: json

 {
  "status": 0,
  "message": "success",
  "data": true
 }




createMultiSig
```````````
创建一个P2SH多重签名地址。

Params

1. nrequired                    (numeric, required) n个键中所需签名的数量

2. "keys"                       (string, required) 十六进制编码的公钥的json数组

定义::

    GET /dash/createMultiSig?nRequired={nRequired}&keys={nRequired}
Example Request:

    GET /dash/createMultiSig?nRequired=6&keys=xxxxxxxxxxxxxxxxx

返回:

.. code-block:: json

 {
  "status": 0,
  "message": "success",
  "data": {
    "m": {
      "address":"xxxxxxxxxxxxxxxxxx"
      "redeemScript":"xxxxxxxxxxxxxxxxxxxxxxxx"
    }
  }
 }

返回:

.. code-block:: json

 {
    "address":"multisigaddress",  (string) The value of the new multisig address
    "redeemScript":"script"       (string) The string value of the hex-encoded redemption script
  }



estimateSmartFee
```````````
估算交易经几个区块确认所需的每千字节的交易费，并获取估算时找到的区块数。


定义::

    GET /dash/estimateSmartFee?blocks={blocks}
Example Request:

    GET /dash/estimateSmartFee?blocks=1

返回:

.. code-block:: json

 {
  "status": 0,
  "message": "success",
  "data": {
    "m": {
      "feerate": 0.00004463,
      "blocks": 4
    }
  }
 }

返回:

.. code-block:: json

 {
    "feerate" : x.x,     (numeric, optional) dash / kB中的估算费用率
    "errors": [ str... ] (json array of strings, optional) 处理期间遇到的错误
    "blocks" : n         (numeric) 找到估计的块号
  }

validateAddress
```````````
验证地址是否有效。

定义::

    GET /dash/validateAddress?address={address}
Example Request:

    GET /dash/validateAddress?address=3LwxH2frucsDJfFainnKKGonJduHXesXAD

返回:

.. code-block:: json

 {
  "status": 0,
  "message": "success",
  "data": true
 }



verifyMessage
```````````
验证消息签名。

Params

1. "address"         (string, required) 用于签名的比特币地址

2. "signature"       (string, required) 签名人以base 64编码提供的签名（请参阅signmessage）

3. "message"         (string, required) 已签名的消息


定义::

    GET /dash/verifyMessage?address={address}&signature={signature}&message={message}
Example Request:

    GET /dash/verifyMessage?address=xxxxxxxx&signature=xxxxxxxx&message=xxxxxxxx

返回:

.. code-block:: json

 {
  "status": 0,
  "message": "success",
   "data": true
 }



queryTransactionInfo
```````````
根据交易id查询交易详情。

定义::

    GET /dash/queryTransactionInfo?txId={txId}
Example Request:

    GET /dash/queryTransactionInfo?txId=xxxxxxxxxxxx
返回:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
    "data": {
        "m": {
        "hash": "000000000000002056c37f7d57864341be0cc01b79c7dfb68350abd831bb50d7",
        "confirmations": 2,
        "size": 10940,
        "height": 1158713,
        "version": 536870912,
        "versionHex": "20000000",
        "merkleroot": "a9ea98c84ce1d538c332e65d1db9de65f7cdb80783a0e0121097993073e60bac",
        "tx": [
            "11f15873f50e55de555729d76dd3d9189cfda6042a3807bb3a0529f80722dac2",
            "4bf438829fe339265f704f3eb62f32ca6db78faa6663a58736a9fa750dc4c022",
            "02a053ca2fcc6c5be98b5701608c6d3ce1f3363ae24cadde189c49293285045d",
            "14e2099bc5e173aee2e18cfdbc228edb850e1181aec7260668b8416815367835",
            "ff624e5970c4716d6d1b78b39ae50edc46fe0c66bb6038a6fe5a05dd4791ebdc",
            "db3c3406a8ec947e21bb56f243e5eb4ffa28adf9be8a6adff06a8cb044d6dca6",
            "e7b6c39a1a178eb8889cbfab8001dbc167e03b49be2e7fbd8a5320b2d3a61de2",
            "64aeaacbcbb9fb6842bc80144e19ccbfaa49b7ca1e438c4c35023376a4768a1b",
            "add2bff452a81710b46cd269d49a21506437c8959409b0f6861664263b19baf8"
        ],
        "cbTx": {
            "version": 2,
            "height": 1158713,
            "merkleRootMNList": "2ef31ada7aa72d5f5215fbd978c47f4ee7b68d293ce68d3b1b2a84fcbc777bc9",
            "merkleRootQuorums": "812ff025ba417a6deb37fc1e0e5f35678665202e09db7e2a31d0b67ce181d187"
        },
        "time": 1571814866,
        "mediantime": 1571814640,
        "nonce": 3600838889,
        "bits": "19240c41",
        "difficulty": 119144408.2195601,
        "chainwork": "000000000000000000000000000000000000000000001f71b3ca52972d74626f",
        "previousblockhash": "00000000000000175d2d0a1c8c4b081b745e066d235af284eea184285cc68297",
        "nextblockhash": "00000000000000074ce217b129e141632aaa9d2b93a400d3137243d361bf4139",
        "chainlock": true
        }
    }
 }


返回:

.. code-block:: json

 {
    "hex" : "data",       (string) 'txid'的序列化，十六进制编码的数据
    "txid" : "id",        (string) 交易ID（与提供的ID相同）
    "size" : n,             (numeric) 序列化的交易规模
    "version" : n,          (numeric) 版本
    "locktime" : ttt,       (numeric) 锁定时间
    "vin" : [               (array of json objects)
        {
        "txid": "id",    (string) 交易id
        "vout": n,         (numeric)
        "scriptSig": {     (json object) The script
            "asm": "asm",  (string) asm
            "hex": "hex"   (string) hex
        },
        "sequence": n      (numeric) 脚本序列号
        }
        ,...
    ],
    "vout" : [              (array of json objects)
        {
        "value" : x.xxx,            (numeric) The value in dash
        "n" : n,                    (numeric) index
        "scriptPubKey" : {          (json object)
            "asm" : "asm",          (string) the asm
            "hex" : "hex",          (string) the hex
            "reqSigs" : n,            (numeric) 所需信号
            "type" : "pubkeyhash",  (string) The type, eg 'pubkeyhash'
            "addresses" : [           (json array of string)
            "address"        (string) dash 地址
            ,...
            ]
        }
        }
        ,...
    ],
    "extraPayloadSize" : n    (numeric) DIP2额外有效负载的大小。 仅在特殊发送时才显示
    "extraPayload" : "hex"    (string) 十六进制编码的DIP2额外有效载荷数据。 仅在特殊发送时才显示
    "blockhash" : "hash",   (string) 区块哈希
    "confirmations" : n,      (numeric) 确认数
    "time" : ttt,             (numeric) 自时间段以来的阻止时间（以秒为单位）（格林尼治标准时间1970年1月1日）
    "blocktime" : ttt         (numeric) 区块时间
    "instantlock" : true|false, (bool) 当前事务锁定状态
    "instantlock_internal" : true|false, (bool) 当前内部事务锁定状态
    "chainlock" : true|false, (bool) 相应区块链锁的状态
 }

decodeRawTransaction
```````````
解码裸交易。

定义::

    GET /dash/decodeRawTransaction?hex={hex}
Example Request:

    GET /dash/decodeRawTransaction?hex=xxxxxxxxxx

返回:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
        "data": {
            {
        "txid" : "id",        (string) 交易id
        "hash" : "id",        (string) 交易哈希（与见证交易的txid不同）
        "size" : n,             (numeric) 交易规模
        "vsize" : n,            (numeric) 虚拟交易规模（与见证交易规模不同）
        "weight" : n,           (numeric) 事务的权重（介于vsize * 4-3和vsize * 4之间）
        "version" : n,          (numeric) 版本
        "locktime" : ttt,       (numeric) 锁定时间
        "vin" : [               (array of json objects)
            {
            "txid": "id",    (string) 交易id
            "vout": n,         (numeric) 输出编号
            "scriptSig": {     (json object) The script
                "asm": "asm",  (string) asm
                "hex": "hex"   (string) hex
            },
            "txinwitness": ["hex", ...] (array of string) 十六进制编码的见证数据（如果有）
            "sequence": n     (numeric) 脚本序列号
            }
            ,...
        ],
        "vout" : [             (array of json objects)
            {
            "value" : x.xxx,            (numeric) DASH中的价值
            "n" : n,                    (numeric) index
            "scriptPubKey" : {          (json object)
                "asm" : "asm",          (string) the asm
                "hex" : "hex",          (string) the hex
                "reqSigs" : n,            (numeric) 所需信号
                "type" : "pubkeyhash",  (string) 类型，例如'pubkeyhash'
                "addresses" : [           (json array of string)
                "12tvKAXCxZjSmdNbao16dKXC8tRWfcF5oc"   (string) DASH 地址
                ]
            }
            }
            ,...
        ],
            }
    }
 }

