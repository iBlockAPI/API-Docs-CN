BitcoinABC API Docs
===========
getbestblockhash
```````````
获取链头区块哈希.

定义::

    GET /bch/getBestBlockHash/

请求示例::

    GET /bch/getBestBlockHash/

返回:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
    "data": "0000000000000000014608bb6ae585f82907a240f308bd892448fe27dcd2ea7c"
 }

getBlockByHash
```````````
获取指定哈希的区块

Return:

.. code-block:: json

 {
    "hash" : "hash",     (string) 区块哈希
    "confirmations" : n,   (numeric) 确认数
    "size" : n,            (numeric) 区块字节数
    "strippedsize" : n,    (numeric) 剔除隔离见证数据后的区块字节数
    "weight" : n           (numeric) BIP141定义的区块权重
    "height" : n,          (numeric) 区块高度
    "version" : n,         (numeric) 版本
    "versionHex" : "00000000", (string) 16进制表示的版本
    "merkleroot" : "xxxx", (string) 区块的默克尔树根
    "tx" : [               (array of string) 区块内所有交易组成的数组，成员为交易id
        "transactionid"     (string) 交易id
        ,...
    ],
    "time" : ttt,          (numeric) 区块创建时间戳
    "mediantime" : ttt,    (numeric) 区块中值时间戳
    "nonce" : n,           (numeric) nonce值
    "bits" : "1d00ffff", (string) The bits
    "difficulty" : x.xxx,  (numeric) 难度
    "chainwork" : "xxxx",  (string) 产生链到此区块所需的预期哈希
    "nTx" : n,             (numeric) 区块内交易数量.
    "previousblockhash" : "hash",  (string) 前一区块的哈希
    "nextblockhash" : "hash"       (string) 下一区块的哈希
 }

定义::

    GET /bch/getBlockByHash?hash={hash}    //hash (string)

请求示例::

    GET /bch/getBlockByHash?hash=0000000000000000014608bb6ae585f82907a240f308bd892448fe27dcd2ea7c

返回:

.. code-block:: json

 {
  "status": 0,
  "message": "success",
  "data": {
    "m": {
      "hash": "0000000000000000014608bb6ae585f82907a240f308bd892448fe27dcd2ea7c",
      "confirmations": 1,
      "size": 18335,
      "height": 606508,
      "version": 541065216,
      "versionHex": "20400000",
      "merkleroot": "f90246a9769b9f8f79b12572db1593402b9892d4d66acd27d2b0a1f71f24e7bd",
      "tx": [
        "a0a6b9c55189a8f57be8cc6f1d27adbe9fa6f6bc7f9d3fb9724d3258047f880b",
        "01499db8f2157c80eab737ba881555e65a7c2e04ccebab3bd55df845bbe3c2e2",
        "01e951a1f9932ce34d013a284d9611e6a007a4f4c9f5a0557338545e72cda352",
        "029ed89ce9658f9a7be935fbcfa33b8368364d672a7bf32555d638ead149f643",
        "04bbe6003be6e037786b0e3073aa437bc44df1e29ed261810d1766e6f78990fb",
        "06fc01017ffb5620bd379489d2516351751ae3d675e345eb3f9e44d5d97b736d",
        "08deb8e75bf8cffaa479a7d17c8cb0c46a52d1cda6fb7e101323515dae09c52b",
        "09e07d6a863b306749a0f12865ad0360f8c3bd78c6323b9f0a202324e4b8f2dd",
        "0db2f21445dc70cbf13d87740a4793da93231d597bac8be33f832fcc98a830a4",
        "0fa3b66175878b07c2c40009fccd6c1e8e1a92c1f13517303d77acb0f8e3b561",
        "15d665642d0d8005e9494617cd1731ed511ebaf6a60725bee0e31de0fd68dce2",
        "16aa8b8df330f8fb0311593cc025914ce4cd2daf3e66d7289adbefa41d1ae2d5",
        "20543c787937f3e47bb2b526104081cdf541748110a95840f3e7f26cafcd03f6",
        "245b80ec023044ec86445a6ea9ede0de10b5960683308f5d6defc7bf48971403",
        "36f979f1f25514f32c054cfe841f23a4e543e4472d48ebc0cf0db5eb346dbf61",
        "39f13993134a9bccfc2233a5f7cc020eb8bfd972e143299bfe6c4001483c0b33",
        "468bd8f3c7b06c4d10f76af3d91ace27979652669be7792b07c3922743ef9f24",
        "4bc7e95da11c20024b91b737ff19bf8189c4122384407343c67985c97529b2de",
        "553879efc5572ec84b44695e19569478220d3d4c15e77a13e11b736274c15054",
        "5a7642645f014ee8cef5a1a5df00d96d202f647eed5627e742891d6451dd41db",
        "5b3e55ecf275028ec91815d5efb87dcd3329f1070c0bcd396cbcbb980e154b75",
        "64e04fd10c301304e0adb7187579bddd97400287a992c0f29c952c9c231509d7",
        "679b80bde3013bf7219e1f06d0e41d85f41a4a263bff93ee2510249054e969b3",
        "688a79df127bb841b5916f3f418b6b6ffcd271e44ae3687827b3c07896535235",
        "6cfd7c0cb5cc1c815d7476111b4419c53a9d2757d5eb351e9a0f7eec2ef96d0a",
        "71bcc87880deb4afb5092de7b46dcd06679c9ce2a2c7fdbf635597260f819efa",
        "75104ab7c9db0abafcb8741771b26461cff83965acbee75022a5ff3b8339ab06",
        "77d361c9cce1b8698f35279df686fa90f1e3bbdbc6cdd5e268ae4b04210a582f",
        "7dad697bf7d0a612dc0e3bf51c764a9e832d10b083e2dbce7da8c45f4c676fed",
        "8986310cd6ba76322c962a2c75d4171ebe39e572304a10d9b5e68d35b6f2247e",
        "97f05100cc2050db4b9ce4dc161d4e77a7a1d343697ddef78fb0398edeae3bdb",
        "9812a6734bffddfd50d77a65bfc1be3213c7987d4ab8ae4ad36130cc2f453807",
        "a1b068d55e5f21cd5260b0ed8153f8b4992c369c32b68b431e5f5f3121bee4cb",
        "a3502b399669ff48e6da247847392bbbdd42bebfa040b268cd97a2d7b07508f9",
        "a6e0562adc045e580cfc528b294f48cc80bda6ab66035cce1fb01ec95abeede0",
        "a904741bd431f456051127f27bff01d59d7177221da3dd83f02c4c9462fbeead",
        "aa3cfb04892b4dde1b67aa4e176f5984fd9cd35425c4747eb78ade2303434086",
        "abe8f5be472eac050e622a006d7f6f0917033e584436bb9f63651a940dad077f",
        "afd800ff097912e47513f28c1e102f5300313a86c0992dcaec2795a25ee4148f",
        "b535e8a39455227e2f8a5fea07e3a6385d40043ca3301f547a20522f1e3804f1",
        "bf26d0a9e104dec2f9615c9fc06f690cbb45a09f812a78971be90b88c9e62539",
        "bff88aa6043900e18da278f0e4c6018c7bb6f80f79ba7257b71526b32235722e",
        "c645bf093c8fe105e4e5af7431809715948d0a3abc7deb989afe2b5b2ae91f67",
        "ca6a870dae99d4ad3ad15a71fd8e937c666345603c5a5b56b32f98c8432aa4a9",
        "cb3458e031c87a21d18244fd3f23879a3969312a724c8ff34c216e07f809eb44",
        "d3453f3b5398495d2b2cb7345263b0c3d3a93ed40c31e33b76cf15092473a10d",
        "e98f8d2b4b436a9575cd202a0c9c17c4c0163c4a502e77d30aea1dce23f24ee6",
        "eae7fe691aef371523e4aa960dddd8f64b20abe1fa1e352a1a5823c67421322a",
        "ef0b8c025450e588746c31b963ef12406df9fb58314faea6dbe86def358b7a39",
        "f182b8247b274af4a5f47c5b4c2e4f864946f501d27593bc615ecc040eaf6291",
        "fe5591dcf4fdd911a5e7bc4e2c5823587135eac82d4456afa18c4b63fb03be70"
      ],
      "time": 1572244008,
      "mediantime": 1572236224,
      "nonce": 1747648579,
      "bits": "180303bd",
      "difficulty": 364722974850.3032,
      "chainwork": "000000000000000000000000000000000000000001055dfb2d5ea9697bfa7c4d",
      "previousblockhash": "000000000000000002c78e7995fa70ff33de95567cba74119552601aac705222"
    }
  }
}

getBlockByHeight
```````````
根据区块高度获取指定哈希的区块

Return:

.. code-block:: json

 {
     "hash" : "hash",     (string) 区块哈希
     "confirmations" : n,   (numeric) 确认数
     "size" : n,            (numeric) 区块字节数
     "strippedsize" : n,    (numeric) 剔除隔离见证数据后的区块字节数
     "weight" : n           (numeric) BIP141定义的区块权重
     "height" : n,          (numeric) 区块高度
     "version" : n,         (numeric) 版本
     "versionHex" : "00000000", (string) 16进制表示的版本
     "merkleroot" : "xxxx", (string) 区块的默克尔树根
     "tx" : [               (array of string) 区块内所有交易组成的数组，成员为交易id
         "transactionid"     (string) 交易id
         ,...
     ],
     "time" : ttt,          (numeric) 区块创建时间戳
     "mediantime" : ttt,    (numeric) 区块中值时间戳
     "nonce" : n,           (numeric) nonce值
     "bits" : "1d00ffff", (string) The bits
     "difficulty" : x.xxx,  (numeric) 难度
     "chainwork" : "xxxx",  (string) 产生链到此区块所需的预期哈希
     "nTx" : n,             (numeric) 区块内交易数量.
     "previousblockhash" : "hash",  (string) 前一区块的哈希
     "nextblockhash" : "hash"       (string) 下一区块的哈希
  }

定义::

    GET /bch/getBlockByHeight?height={height}   //height (Integer)
请求示例::

    GET /bch/getBlockByHeight?height=606508

返回:

.. code-block:: json

  {
    "status": 0,
    "message": "success",
    "data": {
      "m": {
        "hash": "0000000000000000014608bb6ae585f82907a240f308bd892448fe27dcd2ea7c",
        "confirmations": 2,
        "size": 18335,
        "height": 606508,
        "version": 541065216,
        "versionHex": "20400000",
        "merkleroot": "f90246a9769b9f8f79b12572db1593402b9892d4d66acd27d2b0a1f71f24e7bd",
        "tx": [
          "a0a6b9c55189a8f57be8cc6f1d27adbe9fa6f6bc7f9d3fb9724d3258047f880b",
          "01499db8f2157c80eab737ba881555e65a7c2e04ccebab3bd55df845bbe3c2e2",
          "01e951a1f9932ce34d013a284d9611e6a007a4f4c9f5a0557338545e72cda352",
          "029ed89ce9658f9a7be935fbcfa33b8368364d672a7bf32555d638ead149f643",
          "04bbe6003be6e037786b0e3073aa437bc44df1e29ed261810d1766e6f78990fb",
          "06fc01017ffb5620bd379489d2516351751ae3d675e345eb3f9e44d5d97b736d",
          "08deb8e75bf8cffaa479a7d17c8cb0c46a52d1cda6fb7e101323515dae09c52b",
          "09e07d6a863b306749a0f12865ad0360f8c3bd78c6323b9f0a202324e4b8f2dd",
          "0db2f21445dc70cbf13d87740a4793da93231d597bac8be33f832fcc98a830a4",
          "0fa3b66175878b07c2c40009fccd6c1e8e1a92c1f13517303d77acb0f8e3b561",
          "15d665642d0d8005e9494617cd1731ed511ebaf6a60725bee0e31de0fd68dce2",
          "16aa8b8df330f8fb0311593cc025914ce4cd2daf3e66d7289adbefa41d1ae2d5",
          "20543c787937f3e47bb2b526104081cdf541748110a95840f3e7f26cafcd03f6",
          "245b80ec023044ec86445a6ea9ede0de10b5960683308f5d6defc7bf48971403",
          "36f979f1f25514f32c054cfe841f23a4e543e4472d48ebc0cf0db5eb346dbf61",
          "39f13993134a9bccfc2233a5f7cc020eb8bfd972e143299bfe6c4001483c0b33",
          "468bd8f3c7b06c4d10f76af3d91ace27979652669be7792b07c3922743ef9f24",
          "4bc7e95da11c20024b91b737ff19bf8189c4122384407343c67985c97529b2de",
          "553879efc5572ec84b44695e19569478220d3d4c15e77a13e11b736274c15054",
          "5a7642645f014ee8cef5a1a5df00d96d202f647eed5627e742891d6451dd41db",
          "5b3e55ecf275028ec91815d5efb87dcd3329f1070c0bcd396cbcbb980e154b75",
          "64e04fd10c301304e0adb7187579bddd97400287a992c0f29c952c9c231509d7",
          "679b80bde3013bf7219e1f06d0e41d85f41a4a263bff93ee2510249054e969b3",
          "688a79df127bb841b5916f3f418b6b6ffcd271e44ae3687827b3c07896535235",
          "6cfd7c0cb5cc1c815d7476111b4419c53a9d2757d5eb351e9a0f7eec2ef96d0a",
          "71bcc87880deb4afb5092de7b46dcd06679c9ce2a2c7fdbf635597260f819efa",
          "75104ab7c9db0abafcb8741771b26461cff83965acbee75022a5ff3b8339ab06",
          "77d361c9cce1b8698f35279df686fa90f1e3bbdbc6cdd5e268ae4b04210a582f",
          "7dad697bf7d0a612dc0e3bf51c764a9e832d10b083e2dbce7da8c45f4c676fed",
          "8986310cd6ba76322c962a2c75d4171ebe39e572304a10d9b5e68d35b6f2247e",
          "97f05100cc2050db4b9ce4dc161d4e77a7a1d343697ddef78fb0398edeae3bdb",
          "9812a6734bffddfd50d77a65bfc1be3213c7987d4ab8ae4ad36130cc2f453807",
          "a1b068d55e5f21cd5260b0ed8153f8b4992c369c32b68b431e5f5f3121bee4cb",
          "a3502b399669ff48e6da247847392bbbdd42bebfa040b268cd97a2d7b07508f9",
          "a6e0562adc045e580cfc528b294f48cc80bda6ab66035cce1fb01ec95abeede0",
          "a904741bd431f456051127f27bff01d59d7177221da3dd83f02c4c9462fbeead",
          "aa3cfb04892b4dde1b67aa4e176f5984fd9cd35425c4747eb78ade2303434086",
          "abe8f5be472eac050e622a006d7f6f0917033e584436bb9f63651a940dad077f",
          "afd800ff097912e47513f28c1e102f5300313a86c0992dcaec2795a25ee4148f",
          "b535e8a39455227e2f8a5fea07e3a6385d40043ca3301f547a20522f1e3804f1",
          "bf26d0a9e104dec2f9615c9fc06f690cbb45a09f812a78971be90b88c9e62539",
          "bff88aa6043900e18da278f0e4c6018c7bb6f80f79ba7257b71526b32235722e",
          "c645bf093c8fe105e4e5af7431809715948d0a3abc7deb989afe2b5b2ae91f67",
          "ca6a870dae99d4ad3ad15a71fd8e937c666345603c5a5b56b32f98c8432aa4a9",
          "cb3458e031c87a21d18244fd3f23879a3969312a724c8ff34c216e07f809eb44",
          "d3453f3b5398495d2b2cb7345263b0c3d3a93ed40c31e33b76cf15092473a10d",
          "e98f8d2b4b436a9575cd202a0c9c17c4c0163c4a502e77d30aea1dce23f24ee6",
          "eae7fe691aef371523e4aa960dddd8f64b20abe1fa1e352a1a5823c67421322a",
          "ef0b8c025450e588746c31b963ef12406df9fb58314faea6dbe86def358b7a39",
          "f182b8247b274af4a5f47c5b4c2e4f864946f501d27593bc615ecc040eaf6291",
          "fe5591dcf4fdd911a5e7bc4e2c5823587135eac82d4456afa18c4b63fb03be70"
        ],
        "time": 1572244008,
        "mediantime": 1572236224,
        "nonce": 1747648579,
        "bits": "180303bd",
        "difficulty": 364722974850.3032,
        "chainwork": "000000000000000000000000000000000000000001055dfb2d5ea9697bfa7c4d",
        "previousblockhash": "000000000000000002c78e7995fa70ff33de95567cba74119552601aac705222",
        "nextblockhash": "000000000000000001b5fedaf06b0be22682ab9de951576f108d82e1f0dc8b24"
      }
    }
  }

getBlockChainInfo
```````````
获取区块链当前状态

Return:

.. code-block:: json

 {
    "chain": "xxxx",              (string) 区块链名称，可以是：main、test或regtest
    "blocks": xxxxxx,             (numeric) 本地最优链中的已验证区块数量
    "headers": xxxxxx,            (numeric) 本地最有区块头链表中的已验证区块头数量
    "bestblockhash": "...",       (string) 本地最优链中最高区块的哈希
    "difficulty": xxxxxx,         (numeric) 区块难度
    "mediantime": xxxxxx,         (numeric) 最近区块之前的11个区块的中位时间
    "verificationprogress": xxxx, (numeric) 区块验证进度，0.0~1.0
    "chainwork": "xxxx"           (string) 产生链到此区块所需的预期哈希
    "size_on_disk": xxxxxx,       (numeric) 磁盘上块和撤消文件的估计大小
    "pruned": xx,                 (boolean) 块是否需要修剪

    "warnings" : "...",           (string) 区块链警告信息.
 }

定义::

    GET /bch/getBlockChainInfo
请求示例::

    GET /bch/getBlockChainInfo

返回:

.. code-block:: json

 {
  "status": 0,
  "message": "success",
  "data": {
    "m": {
      "chain": "main",
      "blocks": 606509,
      "headers": 606509,
      "bestblockhash": "000000000000000001b5fedaf06b0be22682ab9de951576f108d82e1f0dc8b24",
      "difficulty": 364262035367.8951,
      "mediantime": 1572237519,
      "verificationprogress": 0.999994386094298,
      "initialblockdownload": false,
      "chainwork": "000000000000000000000000000000000000000001055e4ffd69091bc0cefa58",
      "size_on_disk": 163967849142,
      "pruned": false,
      "warnings": ""
    }
  }
}



getBlockCount
```````````
获取区块数量

定义::

    GET /bch/getBlockCount
请求示例::

    GET /bch/getBlockCount

返回:

.. code-block:: json

   {
        "status": 0,
        "message": "success",
        "data": 606509
    }

getBlockHash
```````````
获取指定高度区块的哈希

定义::

    GET /bch/getBlockHash?heighth={height}
请求示例::

    GET /bch/getBlockHash?heighth=606509

返回:

.. code-block:: json

   {
        "status": 0,
        "message": "success",
        "data": "000000000000000001b5fedaf06b0be22682ab9de951576f108d82e1f0dc8b24"
    }

getDifficulty
```````````
获取出块难度

定义::

    GET /bch/getDifficulty
请求示例::

    GET /bch/getDifficulty

返回:

.. code-block:: json

   {
        "status": 0,
        "message": "success",
        "data": 364262035367.8951
    }


getRawMemPool
```````````
获取交易池详情

定义::

    GET /bch/getRawMemPool
请求示例::

    GET /bch/getRawMemPool

返回:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
    "data": [
        "1adba7ed129515e19021679daae275ea724245ec766e48f35eb873d8b80e0d59",
        "baa081a004a5273363ff7091afd85a6cd9806c8fb624a38315f9e7de6f34c707",
        "587ab6687b40fd37f6c5ce166bb783577730e6ee7f617f16eec9f54894f6fdc9",
        "79aefa9265aac264b4ce2962947a765a9a374ff97f189e4406802b82505e0786",
        "e15a2a17163dd351ea1d5083d408de0b1f7748588083440136acca81888d20f1",
        "930c370d2f66cdb04f2c3e0f246004500acb70a8f9efd222b6578ecd9ce0ba32"
        ,...
    ]
 }


gettxout
```````````
获取交易输出信息

参数说明 :

1."hash"             (必填项) UTXO所在的交易id

2."vouth"                (numeric, 必填项) UTXO在交易输出中的序号

3."unconfirmed"  (boolean, 可选项) 是否显示在内存交易池中的未确认交易，默认值：false.

Result:

.. code-block:: json

 {
  "bestblock":  "hash",    (string) 本地最优链上该区块的哈希
  "confirmations" : n,       (numeric) 所在交易的确认数
  "value" : x.xxx,           (numeric) 该UTXO的面值
  "scriptPubKey" : {         (json object)
     "asm" : "code",       (string)助记符表示的公钥脚本
     "hex" : "hex",        (string)16进制表示的公钥脚本
     "reqSigs" : n,          (numeric) 消费该UTXO需要的最少签名数量
     "type" : "pubkeyhash", (string) 脚本类型
     "addresses" : [          (array of string) 交易中使用的地址数组
        "address"     (string) 比特币地址
        ,...
     ]
  },
  "coinbase" : true|false   (boolean) 如果utxo所在交易是coinbase交易，则为true，否则为false
 }

定义::

    GET /bch/gettxout?hash={hash}&vouth={vouth}&unconfirmed={unconfirmed}
请求示例::

    GET /bch/gettxout?hash=801c9f5625b84daad0272d14231fa95eae58a328668dbf97a283b2600273648b&vouth=1&unconfirmed=false

返回:

.. code-block:: json

 {
  "status": 0,
  "message": "success",
  "data": {
    "m": {
      "bestblock": "000000000000000001b5fedaf06b0be22682ab9de951576f108d82e1f0dc8b24",
      "confirmations": 6777,
      "value": 0.00052214,
      "scriptPubKey": {
        "asm": "OP_DUP OP_HASH160 10d74ad0c8890b2104df7f8138ba6def3ad33220 OP_EQUALVERIFY OP_CHECKSIG",
        "hex": "76a91410d74ad0c8890b2104df7f8138ba6def3ad3322088ac",
        "reqSigs": 1,
        "type": "pubkeyhash",
        "addresses": [
          "bitcoincash:qqgdwjksezyskggymalczw96dhhn45ejyqrq899rly"
        ]
      },
      "coinbase": false
    }
  }
}


getTxOutSetInfo
```````````
获取交易输出集信息

Result:

.. code-block:: json

 {
    "height":n,     (numeric) 本地最优链的高度
    "bestblock": "hex",   (string) 最高位置区块的哈希
    "transactions": n,      (numeric) 包含utxo的交易数量
    "txouts": n,            (numeric) utxo总数
    "bogosize": n,          (numeric) UTXO集大小的无意义指标
    "hash_serialized_2": "hash", (string) 序列化哈希
    "disk_size": n,         (numeric) 磁盘上链环状态的估计大小
    "total_amount": x.xxx          (numeric) 总金额
  }

定义::

    GET /bch/getTxOutSetInfo
请求示例::

    GET /bch/getTxOutSetInfo

返回:

.. code-block:: json

 {
  "status": 0,
  "message": "success",
  "data": {
    "m": {
      "height": 606509,
      "bestblock": "000000000000000001b5fedaf06b0be22682ab9de951576f108d82e1f0dc8b24",
      "transactions": 18851737,
      "txouts": 41445822,
      "bogosize": 3134708465,
      "hash_serialized": "c9d6ccbe83c2110b94e3d00d8aa675fb865a798ccc67de8f6aab1f9fac93dcff",
      "disk_size": 2338997382,
      "total_amount": 18081210.92512499
    }
  }
}


verifyChain
```````````
校验本地区块

定义::

    GET /bch/verifyChain
请求示例::

    GET /bch/verifyChain

返回:

.. code-block:: json

 {
  "status": 0,
  "message": "success",
  "data": true
 }


verifyChainByParam
```````````
通过参数校验本地区块s

Params:
1. checklevel   (numeric, 可选项) 指定检查的细致等级，0~4，默认值：3，等级越高 检查越细致

2. nblocks      (numeric, 可选项) 要检查的区块数量，0表示检查所有区块，默认值：6

定义::

    GET /bch/verifyChainByParam?checkLevel={checkLevel}&numOfBlocks={numOfBlocks}
请求示例::

    GET /bch/verifyChainByParam?checkLevel=3&numOfBlocks=6

返回:

.. code-block:: json

 {
  "status": 0,
  "message": "success",
  "data": true
 }




createMultiSig
```````````
创建多签地址与脚本

该接口耗费时间略长

Params

1. nrequired                    (numeric, 必填项) 消费发往该地址的UTXO所需要的最少签名数

2. "keys"                       (string, 必填项) 公钥或地址数组

Result:

.. code-block:: json

 {
    "address":"multisigaddress",  (string) 地址
    "redeemScript":"script"       (string) 赎回脚本
  }

定义::

    GET /bch/createMultiSig?nRequired={nRequired}&keys={nRequired}

请求示例::

    GET /bch/createMultiSig?nRequired=6&keys=xxxxxxxxxxxxxxxxx

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


validateAddress
```````````
验证地址有效性

定义::

    GET /bch/validateAddress?address={address}

请求示例::

    GET /bch/validateAddress?address=36EFm6DSWhV47miSZmEsfsfc2cKrf1bnSg

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

1. "address"         (string, 必填项) 签名私钥对应的地址

2. "signature"       (string, 必填项) Tbase64编码的签名

3. "message"         (string, 必填项) 原始消息


定义::

    GET /bch/verifyMessage?bitcoinAddress={address}&signature={signature}&message={message}

请求示例::

    GET /bch/verifyMessage?bitcoinAddress=xxxxxxxx&signature=xxxxxxxx&message=xxxxxxxx

返回:

.. code-block:: json

 {
  "status": 0,
  "message": "success",
   "data": true
 }



queryTransactionInfo
```````````
获取指定裸交易

Return:

.. code-block:: json

 {
    "in_active_chain": b, (bool) 指定的块是否在活动链中
    "hex" : "data",       (string) 交易id的16进制值
    "txid" : "id",        (string) 交易id
    "hash" : "id",        (string) 交易啥希
    "size" : n,             (numeric) 序列化的交易大小
    "vsize" : n,            (numeric) 虚拟的交易大小
    "weight" : n,           (numeric) 交易重量
    "version" : n,          (numeric) 版本
    "locktime" : ttt,       (numeric) 锁定时间
    "vin" : [               (array of json objects)
        {
        "txid": "id",    (string) 交易id
        "vout": n,         (numeric)
        "scriptSig": {     (json object) 脚本
            "asm": "asm",  (string) asm
            "hex": "hex"   (string) hex
        },
        "sequence": n      (numeric) 脚本序列号
        "txinwitness": ["hex", ...] (array of string)
        }
        ,...
    ],
    "vout" : [              (array of json objects)
        {
        "value" : x.xxx,            (numeric) 交易数量
        "n" : n,                    (numeric) index
        "scriptPubKey" : {          (json object)
            "asm" : "asm",          (string) the asm
            "hex" : "hex",          (string) the hex
            "reqSigs" : n,            (numeric) 需要签名的数量
            "type" : "pubkeyhash",  (string) The type, eg 'pubkeyhash'
            "addresses" : [           (json array of string)
            "address"        (string) 地址
            ,...
            ]
        }
        }
        ,...
    ],
    "blockhash" : "hash",   (string) 区块哈希
    "confirmations" : n,      (numeric) 确认数
    "time" : ttt,             (numeric) 交易时间秒数
    "blocktime" : ttt         (numeric) 块时间秒数
 }

定义::

    GET /bch/queryTransactionInfo?txId={txId}

请求示例::

    GET /bch/queryTransactionInfo?txId=7ce42db1afb579af4f24395c46475af3c4f21c7603220ce2f36fd38d2f300d03

返回:

.. code-block:: json

 {
  "status": 0,
  "message": "success",
  "data": {
    "m": {
      "txid": "7ce42db1afb579af4f24395c46475af3c4f21c7603220ce2f36fd38d2f300d03",
      "hash": "7ce42db1afb579af4f24395c46475af3c4f21c7603220ce2f36fd38d2f300d03",
      "version": 1,
      "size": 271,
      "locktime": 0,
      "vin": [
        {
          "txid": "d8a26a0ccb3a4c9534a1786d776f438a2255040e28bd5cc4e280b5ac81a833ca",
          "vout": 1,
          "scriptSig": {
            "asm": "304402204f6c5000652c33824b78bb9ec3c142dc6574649527a881a9cb3a62f94194ada302202a0c572a23c7ab6a8f73c015ddaec80e58bb4dbc193b19dda4670ffd6d2eda3a[ALL|FORKID] 0467ff2df20f28bc62ad188525868f41d461f7dab3c1e500314cdb5218e5637bfd0f9c02eb5b3f383f698d28ff13547eaf05dd9216130861dd0216824e9d7337e3",
            "hex": "47304402204f6c5000652c33824b78bb9ec3c142dc6574649527a881a9cb3a62f94194ada302202a0c572a23c7ab6a8f73c015ddaec80e58bb4dbc193b19dda4670ffd6d2eda3a41410467ff2df20f28bc62ad188525868f41d461f7dab3c1e500314cdb5218e5637bfd0f9c02eb5b3f383f698d28ff13547eaf05dd9216130861dd0216824e9d7337e3"
          },
          "sequence": 4294967295
        }
      ],
      "vout": [
        {
          "value": 0,
          "n": 0,
          "scriptPubKey": {
            "asm": "OP_RETURN 1703982685 461314003697aa813ce1c58239b9cec33c9e6eeb3bca57a8360ef11f380474c4",
            "hex": "6a045db6906520461314003697aa813ce1c58239b9cec33c9e6eeb3bca57a8360ef11f380474c4",
            "type": "nulldata"
          }
        },
        {
          "value": 0.00003173,
          "n": 1,
          "scriptPubKey": {
            "asm": "OP_DUP OP_HASH160 066ebee590278f32aedc8a4865700c49e717f1d7 OP_EQUALVERIFY OP_CHECKSIG",
            "hex": "76a914066ebee590278f32aedc8a4865700c49e717f1d788ac",
            "reqSigs": 1,
            "type": "pubkeyhash",
            "addresses": [
              "bitcoincash:qqrxa0h9jqnc7v4wmj9ysetsp3y7w9l36u8gnnjulq"
            ]
          }
        }
      ],
      "hex": "0100000001ca33a881acb580e2c45cbd280e0455228a436f776d78a134954c3acb0c6aa2d8010000008a47304402204f6c5000652c33824b78bb9ec3c142dc6574649527a881a9cb3a62f94194ada302202a0c572a23c7ab6a8f73c015ddaec80e58bb4dbc193b19dda4670ffd6d2eda3a41410467ff2df20f28bc62ad188525868f41d461f7dab3c1e500314cdb5218e5637bfd0f9c02eb5b3f383f698d28ff13547eaf05dd9216130861dd0216824e9d7337e3ffffffff020000000000000000276a045db6906520461314003697aa813ce1c58239b9cec33c9e6eeb3bca57a8360ef11f380474c4650c0000000000001976a914066ebee590278f32aedc8a4865700c49e717f1d788ac00000000",
      "blockhash": "0000000000000000006cf904a9aff1500a81954e1a3552803f4808f0c0f3262e",
      "confirmations": 1,
      "time": 1572246639,
      "blocktime": 1572246639
    }
  }
}



decodeRawTransaction
```````````
解码裸交易

定义::

    GET /bch/decodeRawTransaction?hex={hex}

请求示例::

    GET /bch/decodeRawTransaction?hex=xxxxxxxxxx

返回:

.. code-block:: json

 {
  "status": 0,
  "message": "success",
 "data": {
       {
          "txid" : "id",        (string) 交易id
          "hash" : "id",        (string) 交易啥希
          "size" : n,             (numeric) 序列化的交易大小
          "vsize" : n,            (numeric) 虚拟的交易大小
          "weight" : n,           (numeric) 交易重量
          "version" : n,          (numeric) 版本
          "locktime" : ttt,       (numeric) 锁定时间
          "vin" : [               (array of json objects)
              {
              "txid": "id",    (string) 交易id
              "vout": n,         (numeric)
              "scriptSig": {     (json object) 脚本
                  "asm": "asm",  (string) asm
                  "hex": "hex"   (string) hex
              },
              "sequence": n      (numeric) 脚本序列号
              "txinwitness": ["hex", ...] (array of string)
              }
              ,...
          ],
          "vout" : [              (array of json objects)
              {
              "value" : x.xxx,            (numeric) 交易数量
              "n" : n,                    (numeric) index
              "scriptPubKey" : {          (json object)
                  "asm" : "asm",          (string) the asm
                  "hex" : "hex",          (string) the hex
                  "reqSigs" : n,            (numeric) 需要签名的数量
                  "type" : "pubkeyhash",  (string) The type, eg 'pubkeyhash'
                  "addresses" : [           (json array of string)
                  "address"        (string) 地址
                  ,...
                  ]
              }
              }
              ,...
          ],
    }
  }
 }

