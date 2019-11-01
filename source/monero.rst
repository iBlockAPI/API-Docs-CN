Monero API Docs
===========
getBlockCount
```````````
查找节点已知的最长链中有多少个块

定义::

    GET /xmr/getBlockCount/

请求示例::

    GET /xmr/getBlockCount/

返回:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
    "data": {
        "返回": {
        "count": 1951488,
        "status": "OK"
        },
        "id": "1571896281490",
        "jsonrpc": "2.0"
    }
 }

onGetblockhash
```````````
通过高度查看区块的哈希值

定义::

    GET /xmr/onGetblockhash?blockHeight={blockHeight}

请求示例::

    GET /xmr/onGetblockhash?blockHeight=912345

返回:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
    "data": {
        "返回": "a18075437c250ce4dd3999bbfbf63a1863f422056df1733786fcc48816133fe5",
        "id": "1571900453426",
        "jsonrpc": "2.0"
    }
 }


getLastBlockHeader
```````````
使用此方法可轻松检索最新块的块头信息

定义::

    GET /xmr/getLastBlockHeader/

请求示例::

    GET /xmr/getLastBlockHeader/

返回:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
    "data": {
        "返回": {
        "block_header": {
            "block_weight": 45702,
            "num_txes": 17,
            "reward": 2244010531416,
            "wide_difficulty": "0x9480c8821",
            "pow_hash": "",
            "cumulative_difficulty_top64": 0,
            "prev_hash": "c9caf49838a0dcc275c5a17dcff4bda46d5d248c89ff7819b58af553a3fa03a1",
            "cumulative_difficulty": 34052350008858796,
            "wide_cumulative_difficulty": "0x78fa6e920b98ab",
            "nonce": 3489661100,
            "minor_version": 11,
            "difficulty": 39863486497,
            "depth": 0,
            "major_version": 11,
            "orphan_status": false,
            "difficulty_top64": 0,
            "miner_tx_hash": "4a26ce549c063bd2d3d6337652a201685848b7fc931792e02434844c47d43c8d",
            "long_term_weight": 45702,
            "block_size": 45702,
            "hash": "9383c087dc644eed46a343c72867a020ed6ebf29f76d08b6735ce143e403a4d1",
            "height": 1951494,
            "timestamp": 1571896656
        },
        "untrusted": false,
        "status": "OK"
        },
        "id": "1571897056680",
        "jsonrpc": "2.0"
    }
 }

返回:

.. code-block:: json

 {
    block_header - 包含块头信息的结构
        block_size - unsigned int; 块大小（以字节为单位）
        depth - unsigned int; 区块链上此区块之后的区块数量。 较大的数字表示较旧的块
        difficulty - unsigned int; 基于挖掘能力的门罗币网络的优势
        hash - string; 该块的哈希值
        height - unsigned int; 区块链上此区块之前的区块数量
        major_version - unsigned int; 此区块高度的monero协议的主要版本
        minor_version - unsigned int; 此块高度处的monero协议的次要版本
        nonce - unsigned int; 用于挖掘Monero块的加密随机一次号码
        num_txes - unsigned int; 区块中的交易数量，不计算币种tx
        orphan_status - boolean; 通常为假。 如果为true，则此块不属于最长链的一部分
        prev_hash - string; 链中紧接该块之前的块的哈希
        reward - unsigned int; 在该区块中生成并奖励给矿工的新原子单元的数量。 注意：1 XMR = 1e12原子单位
        timestamp - unsigned int; 将该区块记录到区块链的Unix时间
    status - string; 常规RPC错误代码。 “确定”表示一切看起来不错
    untrusted - boolean; 说明是否使用引导程序模式获得返回，因此返回值不受信任（真），或者守护程序已完全同步（假）。
 }


getBlockHeaderByHash
```````````
可以使用块的哈希值或高度来检索块头信息。
此方法包括将块的哈希作为输入参数来检索有关该块的基本信息


定义::

    GET /xmr/getBlockHeaderByHash?hash={hash}

请求示例::

    GET /xmr/getBlockHeaderByHash?hash=e22cf75f39ae720e8b71b3d120a5ac03f0db50bba6379e2850975b4859190bc6

返回:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
    "data": {
        "返回": {
        "block_header": {
            "block_weight": 210,
            "num_txes": 0,
            "reward": 7388968946286,
            "wide_difficulty": "0x309d758b",
            "pow_hash": "",
            "cumulative_difficulty_top64": 0,
            "prev_hash": "b61c58b2e0be53fad5ef9d9731a55e8a81d972b8d90ed07c04fd37ca6403ff78",
            "cumulative_difficulty": 754734824984346,
            "wide_cumulative_difficulty": "0x2ae6d65248f1a",
            "nonce": 1646,
            "minor_version": 2,
            "difficulty": 815625611,
            "depth": 1039159,
            "major_version": 1,
            "orphan_status": false,
            "difficulty_top64": 0,
            "miner_tx_hash": "c7da3965f25c19b8eb7dd8db48dcd4e7c885e2491db77e289f0609bf8e08ec30",
            "long_term_weight": 210,
            "block_size": 210,
            "hash": "e22cf75f39ae720e8b71b3d120a5ac03f0db50bba6379e2850975b4859190bc6",
            "height": 912345,
            "timestamp": 1452793716
        },
        "untrusted": false,
        "status": "OK"
        },
        "id": "1571897903177",
        "jsonrpc": "2.0"
    }
 }




getBlockHeaderByHeight
```````````
此方法将块的高度作为输入参数来检索有关该块的基本信息

定义::

    GET /xmr/getBlockHeaderByHeight?height={height}

请求示例::

    GET /xmr/getBlockHeaderByHeight?height=912345

返回:

.. code-block:: json

 {
  "status": 0,
  "message": "success",
  "data": {
    "返回": {
      "block_header": {
        "block_weight": 210,
        "num_txes": 0,
        "reward": 7388968946286,
        "wide_difficulty": "0x309d758b",
        "pow_hash": "",
        "cumulative_difficulty_top64": 0,
        "prev_hash": "b61c58b2e0be53fad5ef9d9731a55e8a81d972b8d90ed07c04fd37ca6403ff78",
        "cumulative_difficulty": 754734824984346,
        "wide_cumulative_difficulty": "0x2ae6d65248f1a",
        "nonce": 1646,
        "minor_version": 2,
        "difficulty": 815625611,
        "depth": 1039161,
        "major_version": 1,
        "orphan_status": false,
        "difficulty_top64": 0,
        "miner_tx_hash": "c7da3965f25c19b8eb7dd8db48dcd4e7c885e2491db77e289f0609bf8e08ec30",
        "long_term_weight": 210,
        "block_size": 210,
        "hash": "e22cf75f39ae720e8b71b3d120a5ac03f0db50bba6379e2850975b4859190bc6",
        "height": 912345,
        "timestamp": 1452793716
      },
      "untrusted": false,
      "status": "OK"
    },
    "id": "1571898044641",
    "jsonrpc": "2.0"
  }
 }




getBlockHeadersRange
```````````
该方法包括起始块高度和终止块高度作为参数，以检索有关块范围的基本信息。

定义::

    GET /xmr/getBlockHeadersRange?startHeight={startHeight}&endHeight={endHeight}

请求示例::

    GET /xmr/getBlockHeadersRange?startHeight=1&endHeight=2

返回:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
    "data": {
        "返回": {
        "headers": [
            {
            "block_weight": 383,
            "num_txes": 0,
            "reward": 17592169267200,
            "wide_difficulty": "0x1",
            "pow_hash": "",
            "cumulative_difficulty_top64": 0,
            "prev_hash": "418015bb9ae982a1975da7d79277c2705727a56894ba0fb246adaabb1f4632e3",
            "cumulative_difficulty": 2,
            "wide_cumulative_difficulty": "0x2",
            "nonce": 813497413,
            "minor_version": 0,
            "difficulty": 1,
            "depth": 1951507,
            "major_version": 1,
            "orphan_status": false,
            "difficulty_top64": 0,
            "miner_tx_hash": "52578a3816ec18ca6db2ec4f594b7c8a778caa4c52d2c1705bcbab9798a9ea7b",
            "long_term_weight": 383,
            "block_size": 383,
            "hash": "771fbcd656ec1464d3a02ead5e18644030007a0fc664c0a964d30922821a8148",
            "height": 1,
            "timestamp": 1397818193
            },
            {
            "block_weight": 382,
            "num_txes": 0,
            "reward": 17592152490000,
            "wide_difficulty": "0x1",
            "pow_hash": "",
            "cumulative_difficulty_top64": 0,
            "prev_hash": "771fbcd656ec1464d3a02ead5e18644030007a0fc664c0a964d30922821a8148",
            "cumulative_difficulty": 3,
            "wide_cumulative_difficulty": "0x3",
            "nonce": 1184456756,
            "minor_version": 0,
            "difficulty": 1,
            "depth": 1951506,
            "major_version": 1,
            "orphan_status": false,
            "difficulty_top64": 0,
            "miner_tx_hash": "f059b321c5c84f781563080f2ea5958788e16236ca65512e6d81e6e171c93d08",
            "long_term_weight": 382,
            "block_size": 382,
            "hash": "e2914694b698fb417eebaebad3fed4d13e8f670119c95c6e3fa83c1d45311520",
            "height": 2,
            "timestamp": 1397818193
            }
        ],
        "untrusted": false,
        "status": "OK"
        },
        "id": "1571898383549",
        "jsonrpc": "2.0"
    }
 }

getBlockByHeight
```````````
完整的块信息可通过块高度检索


定义::

    GET /xmr/getBlockByHeight?height={height}

请求示例::

    GET /xmr/getBlockByHeight?height=912345

返回:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
    "data": {
        "返回": {
        "block_header": {
            "block_weight": 210,
            "num_txes": 0,
            "reward": 7388968946286,
            "wide_difficulty": "0x309d758b",
            "pow_hash": "",
            "cumulative_difficulty_top64": 0,
            "prev_hash": "b61c58b2e0be53fad5ef9d9731a55e8a81d972b8d90ed07c04fd37ca6403ff78",
            "cumulative_difficulty": 754734824984346,
            "wide_cumulative_difficulty": "0x2ae6d65248f1a",
            "nonce": 1646,
            "minor_version": 2,
            "difficulty": 815625611,
            "depth": 1039149,
            "major_version": 1,
            "orphan_status": false,
            "difficulty_top64": 0,
            "miner_tx_hash": "c7da3965f25c19b8eb7dd8db48dcd4e7c885e2491db77e289f0609bf8e08ec30",
            "long_term_weight": 210,
            "block_size": 210,
            "hash": "e22cf75f39ae720e8b71b3d120a5ac03f0db50bba6379e2850975b4859190bc6",
            "height": 912345,
            "timestamp": 1452793716
        },
        "blob": "0102f4bedfb405b61c58b2e0be53fad5ef9d9731a55e8a81d972b8d90ed07c04fd37ca6403ff786e0600000195d83701ffd9d73704ee84ddb42102378b043c1724c92c69d923d266fe86477d3a5ddd21145062e148c64c5767700880c0fc82aa020273733cbd6e6218bda671596462a4b062f95cfe5e1dbb5b990dacb30e827d02f280f092cbdd080247a5dab669770da69a860acde21616a119818e1a489bb3c4b1b6b3c50547bc0c80e08d84ddcb01021f7e4762b8b755e3e3c72b8610cc87b9bc25d1f0a87c0c816ebb952e4f8aff3d2b01fd0a778957f4f3103a838afda488c3cdadf2697b3d34ad71234282b2fad9100e02080000000bdfc2c16c00",
        "untrusted": false,
        "miner_tx_hash": "c7da3965f25c19b8eb7dd8db48dcd4e7c885e2491db77e289f0609bf8e08ec30",
        "json": "{\n  \"major_version\": 1, \n  \"minor_version\": 2, \n  \"timestamp\": 1452793716, \n  \"prev_id\": \"b61c58b2e0be53fad5ef9d9731a55e8a81d972b8d90ed07c04fd37ca6403ff78\", \n  \"nonce\": 1646, \n  \"miner_tx\": {\n    \"version\": 1, \n    \"unlock_time\": 912405, \n    \"vin\": [ {\n        \"gen\": {\n          \"height\": 912345\n        }\n      }\n    ], \n    \"vout\": [ {\n        \"amount\": 8968946286, \n        \"target\": {\n          \"key\": \"378b043c1724c92c69d923d266fe86477d3a5ddd21145062e148c64c57677008\"\n        }\n      }, {\n        \"amount\": 80000000000, \n        \"target\": {\n          \"key\": \"73733cbd6e6218bda671596462a4b062f95cfe5e1dbb5b990dacb30e827d02f2\"\n        }\n      }, {\n        \"amount\": 300000000000, \n        \"target\": {\n          \"key\": \"47a5dab669770da69a860acde21616a119818e1a489bb3c4b1b6b3c50547bc0c\"\n        }\n      }, {\n        \"amount\": 7000000000000, \n        \"target\": {\n          \"key\": \"1f7e4762b8b755e3e3c72b8610cc87b9bc25d1f0a87c0c816ebb952e4f8aff3d\"\n        }\n      }\n    ], \n    \"extra\": [ 1, 253, 10, 119, 137, 87, 244, 243, 16, 58, 131, 138, 253, 164, 136, 195, 205, 173, 242, 105, 123, 61, 52, 173, 113, 35, 66, 130, 178, 250, 217, 16, 14, 2, 8, 0, 0, 0, 11, 223, 194, 193, 108\n    ], \n    \"signatures\": [ ]\n  }, \n  \"tx_hashes\": [ ]\n}",
        "status": "OK"
        },
        "id": "1571896711791",
        "jsonrpc": "2.0"
    }
 }



getBlockByHash
```````````
完整的区块信息可通过区块哈希检索


定义::

    GET /xmr/getBlockByHash?hash={hash}

请求示例::

    GET /xmr/getBlockByHash?hash=e22cf75f39ae720e8b71b3d120a5ac03f0db50bba6379e2850975b4859190bc6

返回:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
    "data": {
        "返回": {
        "block_header": {
            "block_weight": 210,
            "num_txes": 0,
            "reward": 7388968946286,
            "wide_difficulty": "0x309d758b",
            "pow_hash": "",
            "cumulative_difficulty_top64": 0,
            "prev_hash": "b61c58b2e0be53fad5ef9d9731a55e8a81d972b8d90ed07c04fd37ca6403ff78",
            "cumulative_difficulty": 754734824984346,
            "wide_cumulative_difficulty": "0x2ae6d65248f1a",
            "nonce": 1646,
            "minor_version": 2,
            "difficulty": 815625611,
            "depth": 1039186,
            "major_version": 1,
            "orphan_status": false,
            "difficulty_top64": 0,
            "miner_tx_hash": "c7da3965f25c19b8eb7dd8db48dcd4e7c885e2491db77e289f0609bf8e08ec30",
            "long_term_weight": 210,
            "block_size": 210,
            "hash": "e22cf75f39ae720e8b71b3d120a5ac03f0db50bba6379e2850975b4859190bc6",
            "height": 912345,
            "timestamp": 1452793716
        },
        "blob": "0102f4bedfb405b61c58b2e0be53fad5ef9d9731a55e8a81d972b8d90ed07c04fd37ca6403ff786e0600000195d83701ffd9d73704ee84ddb42102378b043c1724c92c69d923d266fe86477d3a5ddd21145062e148c64c5767700880c0fc82aa020273733cbd6e6218bda671596462a4b062f95cfe5e1dbb5b990dacb30e827d02f280f092cbdd080247a5dab669770da69a860acde21616a119818e1a489bb3c4b1b6b3c50547bc0c80e08d84ddcb01021f7e4762b8b755e3e3c72b8610cc87b9bc25d1f0a87c0c816ebb952e4f8aff3d2b01fd0a778957f4f3103a838afda488c3cdadf2697b3d34ad71234282b2fad9100e02080000000bdfc2c16c00",
        "untrusted": false,
        "miner_tx_hash": "c7da3965f25c19b8eb7dd8db48dcd4e7c885e2491db77e289f0609bf8e08ec30",
        "json": "{\n  \"major_version\": 1, \n  \"minor_version\": 2, \n  \"timestamp\": 1452793716, \n  \"prev_id\": \"b61c58b2e0be53fad5ef9d9731a55e8a81d972b8d90ed07c04fd37ca6403ff78\", \n  \"nonce\": 1646, \n  \"miner_tx\": {\n    \"version\": 1, \n    \"unlock_time\": 912405, \n    \"vin\": [ {\n        \"gen\": {\n          \"height\": 912345\n        }\n      }\n    ], \n    \"vout\": [ {\n        \"amount\": 8968946286, \n        \"target\": {\n          \"key\": \"378b043c1724c92c69d923d266fe86477d3a5ddd21145062e148c64c57677008\"\n        }\n      }, {\n        \"amount\": 80000000000, \n        \"target\": {\n          \"key\": \"73733cbd6e6218bda671596462a4b062f95cfe5e1dbb5b990dacb30e827d02f2\"\n        }\n      }, {\n        \"amount\": 300000000000, \n        \"target\": {\n          \"key\": \"47a5dab669770da69a860acde21616a119818e1a489bb3c4b1b6b3c50547bc0c\"\n        }\n      }, {\n        \"amount\": 7000000000000, \n        \"target\": {\n          \"key\": \"1f7e4762b8b755e3e3c72b8610cc87b9bc25d1f0a87c0c816ebb952e4f8aff3d\"\n        }\n      }\n    ], \n    \"extra\": [ 1, 253, 10, 119, 137, 87, 244, 243, 16, 58, 131, 138, 253, 164, 136, 195, 205, 173, 242, 105, 123, 61, 52, 173, 113, 35, 66, 130, 178, 250, 217, 16, 14, 2, 8, 0, 0, 0, 11, 223, 194, 193, 108\n    ], \n    \"signatures\": [ ]\n  }, \n  \"tx_hashes\": [ ]\n}",
        "status": "OK"
        },
        "id": "1571900658875",
        "jsonrpc": "2.0"
    }
 }


getFeeEstimate
```````````
估算每字节费用

定义::

    GET /xmr/getFeeEstimate

请求示例::

    GET /xmr/getFeeEstimate

返回:

.. code-block:: json

 {
  "status": 0,
  "message": "success",
  "data": {
    "返回": {
      "untrusted": false,
      "fee": 14917,
      "quantization_mask": 10000,
      "status": "OK"
    },
    "id": "1571900764457",
    "jsonrpc": "2.0"
  }
 }
 
返回:

.. code-block:: json

 {
    fee - unsigned int; 每字节估算的费用量，以原子为单位
    quantization_mask - unsigned int; 最终费用应四舍五入为该值的偶数倍
 }


getHeight
```````````
获取节点的当前高度

定义::

    GET /xmr/getHeight

请求示例::

    GET /xmr/getHeight

返回:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
    "data": {
        "untrusted": false,
        "hash": "cea0baafaf626dba2fd53b2ff9b6d3e7f514e759303da7985a819e8fe665b735",
        "height": 1951534,
        "status": "OK"
    }
 }




getTransactions
```````````
通过哈希查找一个或多个交易


定义::

    GET /xmr/getTransactionsgetTransactions?{tx_hash}&decodeAsJson=true

请求示例::

    GET /xmr/getTransactions?txsHashes=d6e48158472848e6687173a91ae6eebfa3e1d778e65252ee99d7515d63090408&decodeAsJson=true

返回:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
    "data": {
        "status": "OK",
        "txs": [{
            "as_hex": "...",
            "as_json": "",
            "block_height": 993442,
            "block_timestamp": 1457749396,
            "double_spend_seen": false,
            "in_pool": false,
            "output_indices": [198769,418598,176616,50345,509],
            "tx_hash": "d6e48158472848e6687173a91ae6eebfa3e1d778e65252ee99d7515d63090408"
        }],
        "txs_as_hex": ["..."],
        "untrusted": false
    }
 }


返回:

.. code-block:: json

 {
    missed_tx - array of strings.
    status - 状态
    txs - 结构条目数组如下
    as_hex - string; 完整的交易信息（十六进制字符串）
    as_json - json string; 交易信息列表
    version - 交易版本
    unlock_time - 如果不为0，则指示事务输出何时可用
    vin - 交易输入清单
    key - 先前输出在此事务中花费的公钥
    amount -输入量，以原子单位表示
    key_offsets - 输入的整数office列表
    k_image - 给定输入的关键图像
    vout - 交易输出清单
    amount - 交易输出量，以原子单位表示
    target - 输出目的地信息
    key - 接收者的隐形公钥。 拥有与此密钥关联的私有密钥的人将控制此事务的输出
    extra - 通常称为“付款ID”，但可用于包含任意32个字节
    signatures - 环形签名中用于隐藏交易真实来源的签名列表
    block_height - unsigned int; 包括交易在内的区块高度
    block_timestamp - unsigned int; Unix时间已被添加到区块链中
    double_spend_seen - boolean; 说明交易是否是双花（true）或不是（false）
    in_pool - boolean; 说明事务是在池中（true）还是在块中（false）
    output_indices - array of unsigned int; 交易指标
    tx_hash - string; 交易 hash
    txs_as_hex - string; 交易信息为十六进制字符串（旧兼容性参数）
 }


getAltBlocksHashes
```````````
获取不在主链上的已知块散列

定义::

    GET /xmr/getAltBlocksHashes
请求示例::

    GET /xmr/getAltBlocksHashes
返回:

.. code-block:: json

 {
  "status": 0,
  "message": "success",
  "data": {
    "untrusted": false,
    "blks_hashes": [
      "d4c8ed9449351113d6805a5c0b39b87c0d13a2cf6cb03db0f4bac62cff54fcac",
      "85a66fc974d7897f6c0260fd29febf0a62edfa9d3d38b19a8caf133009c0e8ff",
      "e8b3812fa85c33064d2e00bbe840fccc7b0463f680f979eb87fda2c15326f950",
      "7d1fb2490985031c68e2ae1e61d613a4fef028292e40b2cd73d47875a8431f52",
      "f82201e30050f8740dae0696a828ec0fc5af99b35cd06ab4cefa0028d4841163",
      "943ca363c0a9c7bf9689340f7657904b3f6d21f3e9f4fdd0306aa9da42b75e6e",
      "0e8e65e30d63222f4fdf96103689af8e3251fc8ee7b3c6e68702b7c45e32e382",
      "2a84592df5a60aa905e71a85e6899a731d49c8480220ece6165c55191d81b0aa",
      "2781adfbef757528b6fe19b178cd4f96fec298131317df7704d014d839738990",
      "7b63a9104d8bb92ab31aaf3fc944e21d0243efe39744b2db48577bb0f836c585",
      "893151868470cc94742b5171e5dfd8a42c02ebdf2de0ace127bd583e6a6a8824",
      "a984f9dc66ed910f478d9899fb16cc18e13750af08062b38daff4d2986a79291",
      "365882ffa7e40cb3517ec9f6f22aa62e533e5a553a0d3de50b85914420864f0e",
      "fa247f9152af67e5667fc040ea6d9f62b360a055291c8607ee38b899d921723d",
      "8a00a265a4f069b79e1fe6eddad4da941c91efd41600826707778b0d48a095cd"
    ],
    "status": "OK"
  }
 }

返回:

.. code-block:: json

 {
   blks_hashes - array of strings; 主链的替代块列表
 }


isKeyImageSpent
```````````
使用与输出关联的关键图像检查输出是否已用完

定义::

    GET /xmr/isKeyImageSpent?keyImages=xxxxxxxx
请求示例::

    GET /xmr/isKeyImageSpent?keyImages=xxxxxxxxx
返回:

.. code-block:: json

 {
  "status": 0,
  "message": "success",
  "data": {
    "spent_status": [1,2],
    "untrusted": false,
    "status": "OK"
  }
 }

返回:

.. code-block:: json

 {
  spent_status - unsigned int list; 每个已检查图像的状态列表。 状态如下：0 =未使用，1 =已花费在区块链上，2 =已花费在交易池中
 }



sendRawTransaction
```````````
向网络广播原始交易

定义::

    GET /xmr/sendRawTransaction?txAsHex=xxxxxxxx&doNotRelay=true
请求示例::

    GET /xmr/sendRawTransaction?txAsHex=xxxxxxxxx&doNotRelay=true
返回:

.. code-block:: json

 {
  "status": 0,
  "message": "success",
  "data": {
    "status": "OK"
  }
 }