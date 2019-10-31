Litecoin API Docs
===========
getBestBlockHash
```````````
返回本地最优链上最后一个区块的哈希

定义::

    GET /ltc/getBestBlockHash/

请求示例::

    GET /ltc/getBestBlockHash/

返回:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
    "data": "069234e09f3d2cebcea66397c607279223047f4a05c8825564346fa728c73a68"
 }

getBlockByHash
```````````
根据区块hash返回指定区块

定义::

    GET /ltc/getBlockByHash?hash={hash}    //hash (string) 

请求示例::

    GET /ltc/getBlockByHash?hash=069234e09f3d2cebcea66397c607279223047f4a05c8825564346fa728c73a68

返回:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
    "data": {
        "m": {
        "hash": "069234e09f3d2cebcea66397c607279223047f4a05c8825564346fa728c73a68",
        "confirmations": 1,
        "strippedsize": 3798,
        "size": 5255,
        "weight": 16649,
        "height": 1724047,
        "version": 536870912,
        "versionHex": "20000000",
        "merkleroot": "7f5f08c2ba228a556fb7d568379cb2f48f0c925ff003affbb2edfd9eb6d5d7c7",
        "tx": [
            "30c2edb122394cd2799349caf18230da67eab65ec9c4dfd765119c3077e32b1a",
            "06b86624397264bd895687b3a61574440c8f46449a5aec3212252dc8bde23901",
            "0a095e7a24356221c8f9dab9632acd0056934be9cf0d775461df5966cce41ed9",
            "49102e78d8170121f18683748e912b8270e160bfc9eca9c5bcff6de6b7db88f9",
            "c8ca06445c7df9f3e25c7147c0a8c9f2e9f4d880b88659fb4d285a87b411a3e5",
            "933d334a9381986ce68c70af551ceeef0c18815a2a35eebadab8ec8894d8ac48",
            "ea5c18cd4cfc33ef20e604f4a2c927b128e59cc59e071d25bc3cd26b4c942756",
            "ed4cef7b66835dbbaf01e5a2e9b20d1317bc75e38d2e1d49304c98d4a5af78f2",
            "169ffd8bd1fe76265414966243ab3c00bcbf9864176ee608db78c3507a3c4e08",
            "862326d75e3ddcff6d88296d27abf3a690c4e9ddab303a011d85276765e037c7",
            "b4eb29c080ac11a2e4c9dc5b0f309b24107f71b17d63fb045a7d37cc0f3ed3db",
            "33eb43e7f44ca8877f9ad86036f7adb2f4fd2b31a13c27cb88d91af04782a092",
            "c551a3e30f02ab234d56c5a8220b0cc7bbef50582ad1fa70703807c3312d2fb4",
            "8a978fee22c835a7763831f9d6b3c92dc48a201b265845adde8a72e36f28c107",
            "6024ca9c902318500d5dd3674e9f8646894fa50a99a956d62ec7764c70ef9308",
            "31aacb22b0ea43878ac03b4f55c509ea87138bbde6579c0876d89e29129f7a42"
        ],
        "time": 1571817501,
        "mediantime": 1571817169,
        "nonce": 2836448068,
        "bits": "1a020b7e",
        "difficulty": 8204328.283313683,
        "chainwork": "000000000000000000000000000000000000000000000354ea1c9478b1e7f060",
        "nTx": 16,
        "previousblockhash": "3e0576f0471c05cfba213e16d705c09a202212226fc683057ddd551519ce0fdb"
        }
    }
 }

返回:

.. code-block:: json

 {
    "hash" : "hash",     (string) 块哈希（与提供的相同）
    "confirmations" : n,   (numeric) 确认数，如果该块不在主链上，则为-1
    "size" : n,            (numeric) 块大小
    "strippedsize" : n,    (numeric) 区块大小，不包括见证数据
    "weight" : n           (numeric) BIP 141中定义的块重量
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
根据区块高度返回指定哈希的区块

定义::

    GET /ltc/getBlockByHeight?height={height}   //height (Integer)
请求示例::

    GET /ltc/getBlockByHeight?height=1724047

返回:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
    "data": {
        "m": {
        "hash": "00000000000000000009ebd5b872ca8f18255889ee5629a0b764a25e3659b326",
        "confirmations": 1,
        "strippedsize": 925588,
        "size": 1216432,
        "weight": 3993196,
        "height": 600618,
        "version": 536870912,
        "versionHex": "20000000",
        "merkleroot": "4b4ed5dfe5c8f72fdbced9e9820ab733c703f5aac0cf9c8a18b2c02ef4c3b5bc",
        "tx": [
            "1725e9081e028d1285c5415d9530c23dafdca4ba0e6496ca5059a7113aa97486",
            "b47794c66971a770749e90d49f543f840e9c6cf54b2f75707aee3ff0725cdc34",
            "d9880f19a4a53509de2bda8e87183f0d937af9faf932f84432ce35fbd68122ac",
            "8540e966fae4e793bd7a6ff4fd41f6be280a04625e4539dfcc728c4b370ae111",

                ],
        "time": 1571793551,
    "mediantime": 1571787998,
    "nonce": 3590812334,
    "bits": "1715a35c",
    "difficulty": 13008091666971.9,
    "chainwork": "0000000000000000000000000000000000000000097eb7a6a9b150bb52f83e19",
    "nTx": 3257,
    "previousblockhash": "00000000000000000010ff158c5126b37bfa453f04077750b527448416d39436",
    "nextblockhash": "00000000000000000007315593295701d0892e5bad63936b72aed708ff366f84"
      }
    }
 }


返回:

.. code-block:: json

 {
    "hash" : "hash",     (string) 块哈希（与提供的相同）
    "confirmations" : n,   (numeric) 确认数，如果该块不在主链上，则为-1
    "size" : n,            (numeric) 块大小
    "strippedsize" : n,    (numeric) 区块大小，不包括见证数据
    "weight" : n           (numeric) BIP 141中定义的块重量
    "height" : n,          (numeric) 块高或索引
    "version" : n,         (numeric) 块版本
    "versionHex" : "00000000", (string) 十六进制格式的块版本
    "merkleroot" : "xxxx", (string) 鱼尾根
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
返回区块链的当前状态

定义::

    GET /ltc/getBlockChainInfo
请求示例::

    GET /ltc/getBlockChainInfo

返回:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
    "data": {
        "m": {
        "chain": "main",
        "blocks": 1724047,
        "headers": 1724047,
        "bestblockhash": "069234e09f3d2cebcea66397c607279223047f4a05c8825564346fa728c73a68",
        "difficulty": 8204328.283313683,
        "mediantime": 1571817169,
        "verificationprogress": 0.9999964193199571,
        "initialblockdownload": false,
        "chainwork": "000000000000000000000000000000000000000000000354ea1c9478b1e7f060",
        "size_on_disk": 25648074736,
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
            "startTime": 1485561600,
            "timeout": 1517356801,
            "since": 1201536
            },
            "segwit": {
            "status": "active",
            "startTime": 1485561600,
            "timeout": 1517356801,
            "since": 1201536
            }
        },
        "warnings": ""
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
    "initialblockdownload": xxxx, (bool) （调试信息）此节点是否处于初始块下载模式的估计
    "chainwork": "xxxx"           (string) 活动链中的工作总数，以十六进制表示
    "size_on_disk": xxxxxx,       (numeric) 磁盘上块和撤消文件的估计大小
    "pruned": xx,                 (boolean) 如果块需要修剪
    "pruneheight": xxxxxx,        (numeric) 已存储最低高度的完整块（仅在启用修剪后才存在）
    "automatic_pruning": xx,      (boolean) 是否启用自动修剪（仅在启用修剪时存在）
    "prune_target_size": xxxxxx,  (numeric) 修剪使用的目标大小（仅在启用自动修剪后才存在）
    "softforks": [                (array) 正在进行的软叉状态
        {
            "id": "xxxx",           (string) 软叉的名称
            "version": xx,          (numeric) 块版本
            "reject": {             (object) 拒绝软叉前的进展
            "status": xx,        (boolean) 如果达到阈值，则为true
            },
        }, ...
    ],
    "bip9_softforks": {           (object) BIP9软叉的状态
        "xxxx" : {                 (string) 软叉的名称
            "status": "xxxx",       (string)  "defined", "started", "locked_in", "active", "failed" 其中之一
            "bit": xx,              (numeric) 块版本字段中的位（0-28），用于向该软叉发送信号（仅用于“已启动”状态）
            "startTime": xx,        (numeric) 该位获得其含义的最小经过块的中值时间
            "timeout": xx,          (numeric) 如果尚未锁定，则认为已部署失败的块经过的中值时间
            "since": xx,            (numeric) 该状态适用的第一个块的高度
            "statistics": {         (object) 有关软叉的BIP9信令的数字统计信息（仅适用于“已启动”状态）
            "period": xx,        (numeric) BIP9信令周期的块长度
            "threshold": xx,     (numeric) 激活功能所需的版本位已设置的块数
            "elapsed": xx,       (numeric) 自当前周期开始以来经过的块数
            "count": xx,         (numeric) 当前时段中设置了版本位的块数
            "possible": xx       (boolean) 如果在这段时间内没有足够的块通过激活阈值，则返回false
            }
        }
    }
    "warnings" : "...",           (string) 任何网络和区块链警告
 }



getBlockCount
```````````
返回本地最优链中的区块数量

定义::

    GET /ltc/getBlockCount
请求示例::

    GET /ltc/getBlockCount

返回:

.. code-block:: json

   {
    "status": 0,
    "message": "success",
    "data": 1724047
 }

getBlockHash
```````````
返回在本地最优链中指定高度区块的哈希

定义::

    GET /ltc/getBlockHash?heighth={height}
请求示例::

    GET /ltc/getBlockHash?heighth=1724047

返回:

.. code-block:: json

   {
    "status": 0,
    "message": "success",
    "data": "069234e09f3d2cebcea66397c607279223047f4a05c8825564346fa728c73a68"
 }

getDifficulty
```````````
返回当前的出块难度

定义::

    GET /ltc/getDifficulty
请求示例::

    GET /ltc/getDifficulty

返回:

.. code-block:: json

   {
    "status": 0,
    "message": "success",
    "data": 13008091666971.9
 }


getRawMemPool
```````````
返回节点交易池中的所有交易

定义::

    GET /ltc/getRawMemPool
请求示例::

    GET /ltc/getRawMemPool

返回:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
    "data": [
        "ec588146077b4846497e7b2a000ef8a45076beebc931b18393af4044a506b654",
        "0c0364e892b8b03ef6739fe1ef29f5fa584ed7a5533ae9fbfa381a87804cee14",
        "2d460905cb0fadb06970cf86f7e04ba7d249bcfb6bb31b5e49a8d7d55ad79f6e",
        "5f301cef57449a566a8860aa2fa3143975edd69bfd7616ada2c4f8fdec6ce062"
    ]
 }


gettxout
```````````
返回一个UTXO的详细信息

Params:

1."hash"             (string, required) UTXO‘s 交易id

2."vouth"                (numeric, required) 交易输出中的UTXO序列号

3."unconfirmed"  (boolean, optional) 是否包括内存池。 默认值：false。 请注意，不会显示在内存池中花费的未用输出。

定义::

    GET /ltc/gettxout?hash={hash}&vouth={vouth}&unconfirmed={unconfirmed}
请求示例::

    GET /ltc/gettxout?hash=xxx&vouth=1&unconfirmed=false

返回:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
    "data": {
        "m": {
        "bestblock": "069234e09f3d2cebcea66397c607279223047f4a05c8825564346fa728c73a68",
        "confirmations": 3752,
        "value": 0.04,
        "scriptPubKey": {
            "asm": "0 c7b377fb142734e3a69f76a7e02d6634c7510b8f",
            "hex": "0014c7b377fb142734e3a69f76a7e02d6634c7510b8f",
            "reqSigs": 1,
            "type": "witness_v0_keyhash",
            "addresses": [
            "ltc1qc7eh07c5yu6w8f5lw6n7qttxxnr4zzu03rp5s7"
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
  "value" : x.xxx,           (numeric) LTC中的交易价值
  "scriptPubKey" : {         (json object)
     "asm" : "code",       (string)
     "hex" : "hex",        (string)
     "reqSigs" : n,          (numeric) 所需签名数
     "type" : "pubkeyhash", (string) 类型，例如pubkeyhash
     "addresses" : [          (array of string) 比特币地址数组
        "address"     (string) ltc 地址
        ,...
     ]
  },
  "coinbase" : true|false   (boolean) 是否有Coinbase
 }
            

getTxOutSetInfo
```````````
返回确认的UTXO集合的统计信息。注意该调用 的执行可能需要一定时间，而且该调用只会计算来自确认交易的输出， 它不会考虑来自交易池的输出


定义::

    GET /ltc/getTxOutSetInfo
请求示例::

    GET /ltc/getTxOutSetInfo

返回:

.. code-block:: json

 {
  "status": 0,
  "message": "success",
  "data": {
    "m": {
      "height": 1724049,
      "bestblock": "5a99a99656c8f7715fbed8e7c1ea2fe26894fc6106922848949a986cf42f250e",
      "transactions": 4121604,
      "txouts": 22522673,
      "bogosize": 1686662133,
      "hash_serialized_2": "088f326cfd517ea6421e3a882cd02e54588900554dbe4df667b15b3751629b6e",
      "disk_size": 1087908427,
      "total_amount": 63548620.68070497
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
验证本地区块链数据库中的每个成员

定义::

    GET /ltc/verifyChain
请求示例::

    GET /ltc/verifyChain

返回:

.. code-block:: json

 {
  "status": 0,
  "message": "success",
  "data": true
 }


verifyChainByParam
```````````
通过参数验证本地区块链数据库中的每个成员

Params:
1. checklevel   （数字，可选，0-4，默认值= 3）块验证的彻底程度

2. nblocks      （数字，可选的，缺省值=6，0 =全部）的块，以检查所述的数

定义::

    GET /ltc/verifyChainByParam?checkLevel={checkLevel}&numOfBlocks={numOfBlocks}
请求示例::

    GET /ltc/verifyChainByParam?checkLevel=3&numOfBlocks=6

返回:

.. code-block:: json

 {
  "status": 0,
  "message": "success",
  "data": true
 }




createMultiSig
```````````
创建一个P2SH多重签名地址

Params

1. nrequired                    (numeric, required) n个键中所需签名的数量

2. "keys"                       (string, required) 十六进制编码的公钥的json数组

定义::

    GET /ltc/createMultiSig?nRequired={nRequired}&keys={nRequired}
Example Request:

    GET /ltc/createMultiSig?nRequired=6&keys=xxxxxxxxxxxxxxxxx

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
估算交易经几个区块确认所需的每千字节的交易费，并获取估算时找到的区块数


定义::

    GET /ltc/estimateSmartFee?blocks={blocks}
Example Request:

    GET /ltc/estimateSmartFee?blocks=1

返回:

.. code-block:: json

 {
  "status": 0,
  "message": "success",
  "data": {
    "m": {
      "feerate":  0.00001039,
      "blocks": 6
    }
  }
 }

返回:

.. code-block:: json

 {
    "feerate" : x.x,     (numeric, optional) LTC / kB中的估算费用率
    "errors": [ str... ] (json array of strings, optional) 处理期间遇到的错误
    "blocks" : n         (numeric) 找到估计的块号
  }



validateAddress
```````````
验证地址是否有效

定义::

    GET /ltc/validateAddress?address={address}
Example Request:

    GET /ltc/validateAddress?address=ltc1qc7eh07c5yu6w8f5lw6n7qttxxnr4zzu03rp5s7

返回:

.. code-block:: json

 {
  "status": 0,
  "message": "success",
  "data": true
 }



verifyMessage
```````````
验证消息签名

Params

1. "address"         (string, required) 用于签名的比特币地址

2. "signature"       (string, required) 签名人以base 64编码提供的签名（请参阅signmessage）

3. "message"         (string, required) 已签名的消息



定义::

    GET /ltc/verifyMessage?address={address}&signature={signature}&message={message}
Example Request:

    GET /ltc/verifyMessage?address=xxxxxxxx&signature=xxxxxxxx&message=xxxxxxxx

返回:

.. code-block:: json

 {
  "status": 0,
  "message": "success",
   "data": true
 }



queryTransactionInfo
```````````
根据交易id查询交易详情

定义::

    GET /ltc/queryTransactionInfo?txId={txId}
Example Request:

    GET /ltc/queryTransactionInfo?txId=xxxxxxxxxxxx
返回:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
    "data": {
        "m": {
        "txid": "xxxxxxxxxxxxxxxxxx",
        "hash": "ec588146077b4846497e7b2a000ef8a45076beebc931b18393af4044a506b654",
        "version": 1,
        "size": 225,
        "vsize": 225,
        "weight": 900,
        "locktime": 1724047,
        "vin": [
            {
            "txid": "351592c3ea91221a9f8b6ec313a0112b28ee45da52156e5e0c84a72212b2dc8b",
            "vout": 0,
            "scriptSig": {
                "asm": "30440220503932491c47d12d243cda2a6f66dd9e2c45ccf925379b31e2898840c4db786e022058de6efb800239964952594344fddf4d9c1403bd04fa98458f3bd6bf1736cd32[ALL] 026ff95a6d5ac014658c6d28860a9a7694ce11e5aeed94f3192b76d9b8df79be0c",
                "hex": "4730440220503932491c47d12d243cda2a6f66dd9e2c45ccf925379b31e2898840c4db786e022058de6efb800239964952594344fddf4d9c1403bd04fa98458f3bd6bf1736cd320121026ff95a6d5ac014658c6d28860a9a7694ce11e5aeed94f3192b76d9b8df79be0c"
            },
            "sequence": 4294967294
            }
        ],
        "vout": [
            {
            "value": 1.3514,
            "n": 0,
            "scriptPubKey": {
                "asm": "OP_DUP OP_HASH160 e15c14bddeb1c61f84a89679326d582e4364c8e4 OP_EQUALVERIFY OP_CHECKSIG",
                "hex": "76a914e15c14bddeb1c61f84a89679326d582e4364c8e488ac",
                "reqSigs": 1,
                "type": "pubkeyhash",
                "addresses": [
                "LfmYcGzCkkWTaSJ5CQrCH2QzaoVukf2eLW"
                ]
            }
            },
            {
            "value": 406.41203457,
            "n": 1,
            "scriptPubKey": {
                "asm": "OP_DUP OP_HASH160 4d5fddacbc2c1106d50a3a2718f335b09e710d89 OP_EQUALVERIFY OP_CHECKSIG",
                "hex": "76a9144d5fddacbc2c1106d50a3a2718f335b09e710d8988ac",
                "reqSigs": 1,
                "type": "pubkeyhash",
                "addresses": [
                "LSH58s6uL22Zu6M2sMo9P8iWBYvRf4Knb5"
                ]
            }
            }
        ],
        "hex": "01000000018bdcb21222a7840c5e6e1552da45ee282b11a013c36e8b9f1a2291eac3921535000000006a4730440220503932491c47d12d243cda2a6f66dd9e2c45ccf925379b31e2898840c4db786e022058de6efb800239964952594344fddf4d9c1403bd04fa98458f3bd6bf1736cd320121026ff95a6d5ac014658c6d28860a9a7694ce11e5aeed94f3192b76d9b8df79be0cfeffffff02a0120e08000000001976a914e15c14bddeb1c61f84a89679326d582e4364c8e488ac018d6776090000001976a9144d5fddacbc2c1106d50a3a2718f335b09e710d8988ac8f4e1a00",
        "blockhash": "339f4a27357d67646d0bca016185cdf91d3fa7951ebe791d518b6449259664f4",
        "confirmations": 2,
        "time": 1571818161,
        "blocktime": 1571818161
        }
    }
 }

返回:

.. code-block:: json

 {
    "in_active_chain": b, (bool) 指定的块是否在活动链中（仅与显式的“ blockhash”参数一起出现）
    "hex" : "data",       (string) 'txid'的序列化，十六进制编码的数据
    "txid" : "id",        (string) 交易ID（与提供的ID相同）
    "hash" : "id",        (string) 交易哈希（与见证交易的txid不同）
    "size" : n,             (numeric) 序列化的交易规模
    "vsize" : n,            (numeric) 虚拟交易规模（与见证交易规模不同）
    "weight" : n,           (numeric) 事务的权重（介于vsize * 4-3和vsize * 4之间）
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
        "txinwitness": ["hex", ...] (array of string) hex-encoded witness data (if any)
        }
        ,...
    ],
    "vout" : [              (array of json objects)
        {
        "value" : x.xxx,            (numeric) The value in LTC
        "n" : n,                    (numeric) index
        "scriptPubKey" : {          (json object)
            "asm" : "asm",          (string) the asm
            "hex" : "hex",          (string) the hex
            "reqSigs" : n,            (numeric) 所需信号
            "type" : "pubkeyhash",  (string) The type, eg 'pubkeyhash'
            "addresses" : [           (json array of string)
            "address"        (string) ltc 地址
            ,...
            ]
        }
        }
        ,...
    ],
    "blockhash" : "hash",   (string) 区块哈希
    "confirmations" : n,      (numeric) 确认数
    "time" : ttt,             (numeric) 自时间段以来的阻止时间（以秒为单位）（格林尼治标准时间1970年1月1日）
    "blocktime" : ttt         (numeric) 区块时间
 }

decodeRawTransaction
```````````
解码裸交易

定义::

    GET /ltc/decodeRawTransaction?hex={hex}
Example Request:

    GET /ltc/decodeRawTransaction?hex=xxxxxxxxxx

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
        "value" : x.xxx,            (numeric) LTC中的价值
        "n" : n,                    (numeric) index
        "scriptPubKey" : {          (json object)
            "asm" : "asm",          (string) the asm
            "hex" : "hex",          (string) the hex
            "reqSigs" : n,            (numeric) 所需信号
            "type" : "pubkeyhash",  (string) 类型，例如'pubkeyhash'
            "addresses" : [           (json array of string)
            "12tvKAXCxZjSmdNbao16dKXC8tRWfcF5oc"   (string) LTC 地址
            ]
        }
        }
        ,...
    ],
        }
  }
 }
