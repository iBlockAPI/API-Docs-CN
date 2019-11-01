Bitcoin API Docs
===========
getBestBlockHash
```````````
返回本地最优链上最后一个区块的哈希。

定义::

    GET /btc/getBestBlockHash/

请求示例::

    GET /btc/getBestBlockHash/

返回:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
    "data": "0000000000000000000f7cf7d8b4aaf52c5bc7980170fd95bde609b424b19946"
 }

getBlockByHash
```````````
根据区块hash返回指定区块。


定义::

    GET /btc/getBlockByHash?hash={hash}    //hash (string) 

请求示例::

    GET /btc/getBlockByHash?hash=00000000000000000009ebd5b872ca8f18255889ee5629a0b764a25e3659b326

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
            "8540e966fae4e793bd7a6ff4fd41f6be280a04625e4539dfcc728c4b370ae111"
                ],
        "time": 1571793551,
        "mediantime": 1571787998,
        "nonce": 3590812334,
        "bits": "1715a35c",
        "difficulty": 13008091666971.9,
        "chainwork": "0000000000000000000000000000000000000000097eb7a6a9b150bb52f83e19",
        "nTx": 3257,
        "previousblockhash": "00000000000000000010ff158c5126b37bfa453f04077750b527448416d39436"
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
根据区块高度返回指定区块。

定义::

    GET /btc/getBlockByHeight?height={height}   //height (Integer)
请求示例::

    GET /btc/getBlockByHeight?height=600618

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
返回区块链的当前状态 。


定义::

    GET /btc/getBlockChainInfo
请求示例::

    GET /btc/getBlockChainInfo

返回:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
    "data": {
        "m": {
        "chain": "main",
        "blocks": 600625,
        "headers": 600625,
        "bestblockhash": "00000000000000000009828f2f721497dff73c4e6b77e555b9b5c13463e8bb7e",
        "difficulty": 13008091666971.9,
        "mediantime": 1571793802,
        "verificationprogress": 0.9999961968294349,
        "initialblockdownload": false,
        "chainwork": "0000000000000000000000000000000000000000097f0a77c34a6117ac351ba6",
        "size_on_disk": 278903834699,
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
            "startTime": 1462060800,
            "timeout": 1493596800,
            "since": 419328
            },
            "segwit": {
            "status": "active",
            "startTime": 1479168000,
            "timeout": 1510704000,
            "since": 481824
            }
        },
        "warnings": "Warning: Unknown block versions being mined! It's possible unknown rules are in effect"
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
返回最长链中的区块数量。

定义::

    GET /btc/getBlockCount
请求示例::

    GET /btc/getBlockCount

返回:

.. code-block:: json

   {
    "status": 0,
    "message": "success",
    "data": 600626
 }

getBlockHash
```````````
根据指定高度查询区块数量。

定义::

    GET /btc/getBlockHash?heighth={height}
请求示例::

    GET /btc/getBlockHash?heighth=600626

返回:

.. code-block:: json

   {
    "status": 0,
    "message": "success",
    "data": "00000000000000000000c6e0c8a6587835746ae98018b6740bc8c15751ee3900"
 }

getDifficulty
```````````
返回当前的出块难度。

定义::

    GET /btc/getDifficulty
请求示例::

    GET /btc/getDifficulty

返回:

.. code-block:: json

   {
    "status": 0,
    "message": "success",
    "data": 13008091666971.9
 }


getRawMemPool
```````````
返回节点交易池中的所有交易。

定义::

    GET /btc/getRawMemPool
请求示例::

    GET /btc/getRawMemPool

返回:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
    "data": [
        "314204c7d5871f6f6a99cb375d77164ccbe13652e8520464ec6609dcc8a3ce76",
        "173acde0510d140090f84a433c127f795184de81d89787fe354b7258637e86e4",
        "a326b1999b2044feb53ab7849e474488b9951f18eec691b496dea037ac611755",
        "6ff9946dd8a74256784beb0ba33cd5c9f8f684b8494bd7aee6cdcbd0e6004411",
        "713d7e9cc29239418c19097a58d38edffb4b86a2cb75efe95e9735c6c887d107",
        "b9b2b1b3a7571336216980de21112750a96860483cb189d053b5152c62efc872"
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

    GET /btc/gettxout?hash={hash}&vouth={vouth}&unconfirmed={unconfirmed}
请求示例::

    GET /btc/gettxout?hash=xxx&vouth=1&unconfirmed=false

返回:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
    "data": {
        "m": {
        "bestblock": "0000000000000000000c1e06ea912c30274fe01a9878f8686f35b59b798a9e5e",
        "confirmations": 1754,
        "value": 0.0002,
        "scriptPubKey": {
            "asm": "OP_HASH160 d33d95cae178329ec460de9652a70e045a7e3638 OP_EQUAL",
            "hex": "a914d33d95cae178329ec460de9652a70e045a7e363887",
            "reqSigs": 1,
            "type": "scripthash",
            "addresses": [
            "3LwxH2frucsDJfFainnKKGonJduHXesXAD"
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
  "value" : x.xxx,           (numeric) BTC中的交易价值
  "scriptPubKey" : {         (json object)
     "asm" : "code",       (string)
     "hex" : "hex",        (string)
     "reqSigs" : n,          (numeric) 所需签名数
     "type" : "pubkeyhash", (string) 类型，例如pubkeyhash
     "addresses" : [          (array of string) 比特币地址数组
        "address"     (string) btc 地址
        ,...
     ]
  },
  "coinbase" : true|false   (boolean) 是否有Coinbase
 }


getTxOutSetInfo
```````````
返回确认的UTXO集合的统计信息。注意该调用的执行可能需要一定时间，而且该调用只会计算来自确认交易的输出， 它不会考虑来自交易池的输出。

定义::

    GET /btc/getTxOutSetInfo
请求示例::

    GET /btc/getTxOutSetInfo

返回:

.. code-block:: json

 {
  "status": 0,
  "message": "success",
  "data": {
    "m": {
      "height": 600650,
      "bestblock": "0000000000000000000c1e06ea912c30274fe01a9878f8686f35b59b798a9e5e",
      "transactions": 37166109,
      "txouts": 63667152,
      "bogosize": 4788031555,
      "hash_serialized_2": "51a84883e8024a567c03abf23333183149db0838d2e6cc16dcaca0961f765b36",
      "disk_size": 3813438942,
      "total_amount": 18007954.82188878
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

    GET /btc/verifyChain
请求示例::

    GET /btc/verifyChain

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

    GET /btc/verifyChainByParam?checkLevel={checkLevel}&numOfBlocks={numOfBlocks}
请求示例::

    GET /btc/verifyChainByParam?checkLevel=3&numOfBlocks=6

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

    GET /btc/createMultiSig?nRequired={nRequired}&keys={nRequired}
Example Request:

    GET /btc/createMultiSig?nRequired=6&keys=xxxxxxxxxxxxxxxxx

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

    GET /btc/estimateSmartFee?blocks={blocks}
Example Request:

    GET /btc/estimateSmartFee?blocks=1

返回:

.. code-block:: json

 {
  "status": 0,
  "message": "success",
  "data": {
    "m": {
      "feerate": 0.00006264,
      "blocks": 2
    }
  }
 }

返回:

.. code-block:: json

 {
    "feerate" : x.x,     (numeric, optional) BTC / kB中的估算费用率
    "errors": [ str... ] (json array of strings, optional) 处理期间遇到的错误
    "blocks" : n         (numeric) 找到估计的块号
  }


validateAddress
```````````
验证地址是否有效。

定义::

    GET /btc/validateAddress?address={address}
Example Request:

    GET /btc/validateAddress?address=3LwxH2frucsDJfFainnKKGonJduHXesXAD

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

    GET /btc/verifyMessage?bitcoinAddress={address}&signature={signature}&message={message}
Example Request:

    GET /btc/verifyMessage?bitcoinAddress=xxxxxxxx&signature=xxxxxxxx&message=xxxxxxxx

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

    GET /btc/queryTransactionInfo?txId={txId}
Example Request:

    GET /btc/queryTransactionInfo?txId=xxxxxxxxxxxx
返回:

.. code-block:: json

 {
  "status": 0,
  "message": "success",
  "data": {
    "m": {
      "txid": "xxxxxxxxxxxxxxxxxxxxxx",
      "hash": "23efefe700fdc913625ded236d5059f72bcd9e7ce06aa4e004c1a728490f1547",
      "version": 1,
      "size": 223,
      "vsize": 142,
      "weight": 565,
      "locktime": 0,
      "vin": [
        {
          "txid": "506e7728e251d9fbc332af643b6769eab1591287d7fa823b0c22019e1723b219",
          "vout": 0,
          "scriptSig": {
            "asm": "",
            "hex": ""
          },
          "txinwitness": [
            "30440220644e7e0ce0e04aab8084a4afce0bcb3a2b3073507b89e783a68839ec994fdd1b02207ed8b7cf82aab855bd52814ed49f7cb58608bc3d221179709d8bee6961a7421501",
            "02a2f7e4a1faf55187aecd8431525002caf9d506be9543cf56affc63a9228b255a"
          ],
          "sequence": 4294967293
        }
      ],
      "vout": [
        {
          "value": 0.0005,
          "n": 0,
          "scriptPubKey": {
            "asm": "OP_HASH160 914337bd14547f2fdf4f978ebd9af042265a5f7f OP_EQUAL",
            "hex": "a914914337bd14547f2fdf4f978ebd9af042265a5f7f87",
            "reqSigs": 1,
            "type": "scripthash",
            "addresses": [
              "3Ew6RjE5qLTcE4FjVrJ2P19Xpo95NFPBPF"
            ]
          }
        },
        {
          "value": 0.00073009,
          "n": 1,
          "scriptPubKey": {
            "asm": "0 6b2fe54aaf926535e6a56a286c3a59f35a02073d",
            "hex": "00146b2fe54aaf926535e6a56a286c3a59f35a02073d",
            "reqSigs": 1,
            "type": "witness_v0_keyhash",
            "addresses": [
              "bc1qdvh72j40jfjnte49dg5xcwje7ddqypeaz56dmv"
            ]
          }
        }
      ],
      "hex": "0100000000010119b223179e01220c3b82fad7871259b1ea69673b64af32c3fbd951e228776e500000000000fdffffff0250c300000000000017a914914337bd14547f2fdf4f978ebd9af042265a5f7f87311d0100000000001600146b2fe54aaf926535e6a56a286c3a59f35a02073d024730440220644e7e0ce0e04aab8084a4afce0bcb3a2b3073507b89e783a68839ec994fdd1b02207ed8b7cf82aab855bd52814ed49f7cb58608bc3d221179709d8bee6961a74215012102a2f7e4a1faf55187aecd8431525002caf9d506be9543cf56affc63a9228b255a00000000",
      "blockhash": "00000000000000000011fc42de5b474990b92067013d69b7170557194b60eb49",
      "confirmations": 1078,
      "time": 1571212116,
      "blocktime": 1571212116
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
        "value" : x.xxx,            (numeric) The value in BTC
        "n" : n,                    (numeric) index
        "scriptPubKey" : {          (json object)
            "asm" : "asm",          (string) the asm
            "hex" : "hex",          (string) the hex
            "reqSigs" : n,            (numeric) 所需信号
            "type" : "pubkeyhash",  (string) The type, eg 'pubkeyhash'
            "addresses" : [           (json array of string)
            "address"        (string) btc 地址
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
解码裸交易。

定义::

    GET /btc/decodeRawTransaction?hex={hex}
Example Request:

    GET /btc/decodeRawTransaction?hex=xxxxxxxxxx

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
        "value" : x.xxx,            (numeric) BTC中的价值
        "n" : n,                    (numeric) index
        "scriptPubKey" : {          (json object)
            "asm" : "asm",          (string) the asm
            "hex" : "hex",          (string) the hex
            "reqSigs" : n,            (numeric) 所需信号
            "type" : "pubkeyhash",  (string) 类型，例如'pubkeyhash'
            "addresses" : [           (json array of string)
            "12tvKAXCxZjSmdNbao16dKXC8tRWfcF5oc"   (string) BTC 地址
            ]
        }
        }
        ,...
    ],
        }
  }
 }

