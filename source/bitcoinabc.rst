BitcoinABC API Docs
===========
getbestblockhash
```````````
Returns the hash of the best (tip) block in the longest block chain.

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
Get the block of the specified hash according to the block hash

Return:

.. code-block:: json

 {
    "hash" : "hash",     (string) the block hash (same as provided)
    "confirmations" : n,   (numeric) The number of confirmations, or -1 if the block is not on the main chain
    "size" : n,            (numeric) The block size
    "strippedsize" : n,    (numeric) The block size excluding witness data
    "weight" : n           (numeric) The block weight as defined in BIP 141
    "height" : n,          (numeric) The block height or index
    "version" : n,         (numeric) The block version
    "versionHex" : "00000000", (string) The block version formatted in hexadecimal
    "merkleroot" : "xxxx", (string) The merkle root
    "tx" : [               (array of string) The transaction ids
        "transactionid"     (string) The transaction id
        ,...
    ],
    "time" : ttt,          (numeric) The block time in seconds since epoch (Jan 1 1970 GMT)
    "mediantime" : ttt,    (numeric) The median block time in seconds since epoch (Jan 1 1970 GMT)
    "nonce" : n,           (numeric) The nonce
    "bits" : "1d00ffff", (string) The bits
    "difficulty" : x.xxx,  (numeric) The difficulty
    "chainwork" : "xxxx",  (string) Expected number of hashes required to produce the chain up to this block (in hex)
    "nTx" : n,             (numeric) The number of transactions in the block.
    "previousblockhash" : "hash",  (string) The hash of the previous block
    "nextblockhash" : "hash"       (string) The hash of the next block
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
Get the block of the specified hash according to the block height

Return:

.. code-block:: json

 {
    "hash" : "hash",     (string) the block hash (same as provided)
    "confirmations" : n,   (numeric) The number of confirmations, or -1 if the block is not on the main chain
    "size" : n,            (numeric) The block size
    "strippedsize" : n,    (numeric) The block size excluding witness data
    "weight" : n           (numeric) The block weight as defined in BIP 141
    "height" : n,          (numeric) The block height or index
    "version" : n,         (numeric) The block version
    "versionHex" : "00000000", (string) The block version formatted in hexadecimal
    "merkleroot" : "xxxx", (string) The merkle root
    "tx" : [               (array of string) The transaction ids
        "transactionid"     (string) The transaction id
        ,...
    ],
    "time" : ttt,          (numeric) The block time in seconds since epoch (Jan 1 1970 GMT)
    "mediantime" : ttt,    (numeric) The median block time in seconds since epoch (Jan 1 1970 GMT)
    "nonce" : n,           (numeric) The nonce
    "bits" : "1d00ffff", (string) The bits
    "difficulty" : x.xxx,  (numeric) The difficulty
    "chainwork" : "xxxx",  (string) Expected number of hashes required to produce the chain up to this block (in hex)
    "nTx" : n,             (numeric) The number of transactions in the block.
    "previousblockhash" : "hash",  (string) The hash of the previous block
    "nextblockhash" : "hash"       (string) The hash of the next block
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
Returns an object containing various state info regarding blockchain processing

Return:

.. code-block:: json

 {
    "chain": "xxxx",              (string) current network name as defined in BIP70 (main, test, regtest)
    "blocks": xxxxxx,             (numeric) the current number of blocks processed in the server
    "headers": xxxxxx,            (numeric) the current number of headers we have validated
    "bestblockhash": "...",       (string) the hash of the currently best block
    "difficulty": xxxxxx,         (numeric) the current difficulty
    "mediantime": xxxxxx,         (numeric) median time for the current best block
    "verificationprogress": xxxx, (numeric) estimate of verification progress [0..1]
    "initialblockdownload": xxxx, (bool) (debug information) estimate of whether this node is in Initial Block Download mode.
    "chainwork": "xxxx"           (string) total amount of work in active chain, in hexadecimal
    "size_on_disk": xxxxxx,       (numeric) the estimated size of the block and undo files on disk
    "pruned": xx,                 (boolean) if the blocks are subject to pruning

    "warnings" : "...",           (string) any network and blockchain warnings.
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
Returns the number of blocks in the longest blockchain

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
Returns hash of block in best-block-chain at height provided

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
Returns the proof-of-work difficulty as a multiple of the minimum difficulty

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
Returns all transaction ids in memory pool as a json array of string transaction ids

Hint: use getmempoolentry to fetch a specific transaction from the mempool

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
Returns details about an unspent transaction output

Params:

1."hash"             (string, required) UTXO‘s transaction id

2."vouth"                (numeric, required) UTXO serial number in the transaction output //long

3."unconfirmed"  (boolean, optional) Whether to include the mempool. Default: false.     Note that an unspent output that is spent in the mempool won't appear.

Result:

.. code-block:: json

 {
  "bestblock":  "hash",    (string) The hash of the block at the tip of the chain
  "confirmations" : n,       (numeric) The number of confirmations
  "value" : x.xxx,           (numeric) The transaction value in BTC
  "scriptPubKey" : {         (json object)
     "asm" : "code",       (string)
     "hex" : "hex",        (string)
     "reqSigs" : n,          (numeric) Number of required signatures
     "type" : "pubkeyhash", (string) The type, eg pubkeyhash
     "addresses" : [          (array of string) array of bitcoin addresses
        "address"     (string) bitcoin address
        ,...
     ]
  },
  "coinbase" : true|false   (boolean) Coinbase or not
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
Returns statistics about the unspent transaction output set,Note this call may take some time

Result:

.. code-block:: json

 {
    "height":n,     (numeric) The current block height (index)
    "bestblock": "hex",   (string) The hash of the block at the tip of the chain
    "transactions": n,      (numeric) The number of transactions with unspent outputs
    "txouts": n,            (numeric) The number of unspent transaction outputs
    "bogosize": n,          (numeric) A meaningless metric for UTXO set size
    "hash_serialized_2": "hash", (string) The serialized hash
    "disk_size": n,         (numeric) The estimated size of the chainstate on disk
    "total_amount": x.xxx          (numeric) The total amount
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
Verifies blockchain database

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
Verifies blockchain database

Params:
1. checklevel   (numeric, optional, 0-4, default=3) How thorough the block verification is

2. nblocks      (numeric, optional, default=6, 0=all) The number of blocks to check

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
Creates a multi-signature address with n signature of m keys required,
It returns a json object with the address and redeemScript

Note this call may take some time

Params

1. nrequired                    (numeric, required) The number of required signatures out of the n keys

2. "keys"                       (string, required) A json array of hex-encoded public keys

Result:

.. code-block:: json

 {
    "address":"multisigaddress",  (string) The value of the new multisig address
    "redeemScript":"script"       (string) The string value of the hex-encoded redemption script
  }

定义::

    GET /bch/createMultiSig?nRequired={nRequired}&keys={nRequired}
请求示例:

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
Return information about the given bitcoin address

定义::

    GET /bch/validateAddress?address={address}
请求示例:

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
Verify a signed message

Params

1. "address"         (string, required) The bitcoin address to use for the signature

2. "signature"       (string, required) The signature provided by the signer in base 64 encoding (see signmessage)

3. "message"         (string, required) The message that was signed


定义::

    GET /bch/verifyMessage?bitcoinAddress={address}&signature={signature}&message={message}
请求示例:

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
Query transaction information according to txid

Return:

.. code-block:: json

 {
    "in_active_chain": b, (bool) Whether specified block is in the active chain or not (only present with explicit "blockhash" argument)
    "hex" : "data",       (string) The serialized, hex-encoded data for 'txid'
    "txid" : "id",        (string) The transaction id (same as provided)
    "hash" : "id",        (string) The transaction hash (differs from txid for witness transactions)
    "size" : n,             (numeric) The serialized transaction size
    "vsize" : n,            (numeric) The virtual transaction size (differs from size for witness transactions)
    "weight" : n,           (numeric) The transaction's weight (between vsize*4-3 and vsize*4)
    "version" : n,          (numeric) The version
    "locktime" : ttt,       (numeric) The lock time
    "vin" : [               (array of json objects)
        {
        "txid": "id",    (string) The transaction id
        "vout": n,         (numeric)
        "scriptSig": {     (json object) The script
            "asm": "asm",  (string) asm
            "hex": "hex"   (string) hex
        },
        "sequence": n      (numeric) The script sequence number
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
            "reqSigs" : n,            (numeric) The required sigs
            "type" : "pubkeyhash",  (string) The type, eg 'pubkeyhash'
            "addresses" : [           (json array of string)
            "address"        (string) bitcoin address
            ,...
            ]
        }
        }
        ,...
    ],
    "blockhash" : "hash",   (string) the block hash
    "confirmations" : n,      (numeric) The confirmations
    "time" : ttt,             (numeric) The transaction time in seconds since epoch (Jan 1 1970 GMT)
    "blocktime" : ttt         (numeric) The block time in seconds since epoch (Jan 1 1970 GMT)
 }

定义::

    GET /bch/queryTransactionInfo?txId={txId}
请求示例:

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
Return a JSON object representing the serialized, hex-encoded transaction.

Also see createrawtransaction and signrawtransaction calls

定义::

    GET /bch/decodeRawTransaction?hex={hex}
请求示例:

    GET /bch/decodeRawTransaction?hex=xxxxxxxxxx

返回:

.. code-block:: json

 {
  "status": 0,
  "message": "success",
 "data": {
       {
  "txid" : "id",        (string) The transaction id
  "hash" : "id",        (string) The transaction hash (differs from txid for witness transactions)
  "size" : n,             (numeric) The transaction size
  "vsize" : n,            (numeric) The virtual transaction size (differs from size for witness transactions)
  "weight" : n,           (numeric) The transaction's weight (between vsize*4 - 3 and vsize*4)
  "version" : n,          (numeric) The version
  "locktime" : ttt,       (numeric) The lock time
  "vin" : [               (array of json objects)
     {
       "txid": "id",    (string) The transaction id
       "vout": n,         (numeric) The output number
       "scriptSig": {     (json object) The script
         "asm": "asm",  (string) asm
         "hex": "hex"   (string) hex
       },
       "txinwitness": ["hex", ...] (array of string) hex-encoded witness data (if any)
       "sequence": n     (numeric) The script sequence number
     }
     ,...
  ],
  "vout" : [             (array of json objects)
     {
       "value" : x.xxx,            (numeric) The value in BTC
       "n" : n,                    (numeric) index
       "scriptPubKey" : {          (json object)
         "asm" : "asm",          (string) the asm
         "hex" : "hex",          (string) the hex
         "reqSigs" : n,            (numeric) The required sigs
         "type" : "pubkeyhash",  (string) The type, eg 'pubkeyhash'
         "addresses" : [           (json array of string)
           "12tvKAXCxZjSmdNbao16dKXC8tRWfcF5oc"   (string) BTC address
         ]
       }
     }
     ,...
  ],
    }
  }
 }

