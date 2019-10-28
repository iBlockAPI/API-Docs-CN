DASH API Docs
===========
getbestblockhash
```````````
Returns the hash of the best (tip) block in the longest block chain.

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
Get the block of the specified hash according to the block hash

返回:

.. code-block:: json

 {
    "hash" : "hash",     (string) the block hash (same as provided)
    "confirmations" : n,   (numeric) The number of confirmations, or -1 if the block is not on the main chain
    "size" : n,            (numeric) The block size
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

getBlockByHeight
```````````
Get the block of the specified hash according to the block height

返回:

.. code-block:: json

 {
    "hash" : "hash",     (string) the block hash (same as provided)
    "confirmations" : n,   (numeric) The number of confirmations, or -1 if the block is not on the main chain
    "size" : n,            (numeric) The block size
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

getBlockChainInfo
```````````
Returns an object containing various state info regarding blockchain processing

返回:

.. code-block:: json

 {
    "chain": "xxxx",        (string) current network name as defined in BIP70 (main, test, regtest)
    "blocks": xxxxxx,         (numeric) the current number of blocks processed in the server
    "headers": xxxxxx,        (numeric) the current number of headers we have validated
    "bestblockhash": "...", (string) the hash of the currently best block
    "difficulty": xxxxxx,     (numeric) the current difficulty
    "mediantime": xxxxxx,     (numeric) median time for the current best block
    "verificationprogress": xxxx, (numeric) estimate of verification progress [0..1]
    "chainwork": "xxxx"     (string) total amount of work in active chain, in hexadecimal
    "pruned": xx,             (boolean) if the blocks are subject to pruning
    "pruneheight": xxxxxx,    (numeric) lowest-height complete block stored
    "softforks": [            (array) status of softforks in progress
        {
            "id": "xxxx",        (string) name of softfork
            "version": xx,         (numeric) block version
            "reject": {            (object) progress toward rejecting pre-softfork blocks
            "status": xx,       (boolean) true if threshold reached
            },
        }, ...
    ],
    "bip9_softforks": {          (object) status of BIP9 softforks in progress
        "xxxx" : {                (string) name of the softfork
            "status": "xxxx",    (string) one of "defined", "started", "locked_in", "active", "failed"
            "bit": xx,             (numeric) the bit (0-28) in the block version field used to signal this softfork (only for "started" status)
            "period": xx,          (numeric) the window size/period for this softfork (only for "started" status)
            "threshold": xx,       (numeric) the threshold for this softfork (only for "started" status)
            "windowStart": xx,     (numeric) the starting block height of the current window (only for "started" status)
            "windowBlocks": xx,    (numeric) the number of blocks in the current window that had the version bit set for this softfork (only for "started" status)
            "windowProgress": xx,  (numeric) the progress (between 0 and 1) for activation of this softfork (only for "started" status)
            "startTime": xx,       (numeric) the minimum median time past of a block at which the bit gains its meaning
            "timeout": xx,         (numeric) the median time past of a block at which the deployment is considered failed if not yet locked in
            "since": xx            (numeric) height of the first block to which the status applies
        }
    }
 }

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



getBlockCount
```````````
Returns the number of blocks in the longest blockchain

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
Returns hash of block in best-block-chain at height provided

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
Returns the proof-of-work difficulty as a multiple of the minimum difficulty

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
Returns all transaction ids in memory pool as a json array of string transaction ids

Hint: use getmempoolentry to fetch a specific transaction from the mempool

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
  "value" : x.xxx,           (numeric) The transaction value in DASH
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
  "version" : n,            (numeric) The version
  "coinbase" : true|false   (boolean) Coinbase or not
 }

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


verifyChain
```````````
Verifies blockchain database

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
Verifies blockchain database

Params:
1. checklevel   (numeric, optional, 0-4, default=3) How thorough the block verification is

2. nblocks      (numeric, optional, default=6, 0=all) The number of blocks to check

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

 


estimateSmartFee
```````````
Estimates the approximate fee per kilobyte needed for a transaction to begin
confirmation within conf_target blocks if possible and return the number of blocks
for which the estimate is valid. Uses virtual transaction size as defined
in BIP 141 (witness data is discounted)

Result:

.. code-block:: json

 {
    "feerate" : x.x,     (numeric, optional) estimate fee rate in 
    "errors": [ str... ] (json array of strings, optional) Errors encountered during processing
    "blocks" : n         (numeric) block number where estimate was found
  }

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



validateAddress
```````````
Return information about the given bitcoin address

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
Verify a signed message

Params

1. "address"         (string, required) The bitcoin address to use for the signature

2. "signature"       (string, required) The signature provided by the signer in base 64 encoding (see signmessage)

3. "message"         (string, required) The message that was signed


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
Query transaction information according to txid

返回:

.. code-block:: json

 {
    "hex" : "data",       (string) The serialized, hex-encoded data for 'txid'
    "txid" : "id",        (string) The transaction id (same as provided)
    "size" : n,             (numeric) The transaction size
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
        }
        ,...
    ],
    "vout" : [              (array of json objects)
        {
        "value" : x.xxx,            (numeric) The value in DASH
        "n" : n,                    (numeric) index
        "scriptPubKey" : {          (json object)
            "asm" : "asm",          (string) the asm
            "hex" : "hex",          (string) the hex
            "reqSigs" : n,            (numeric) The required sigs
            "type" : "pubkeyhash",  (string) The type, eg 'pubkeyhash'
            "addresses" : [           (json array of string)
            "address"        (string) dash address
            ,...
            ]
        }
        }
        ,...
    ],
    "extraPayloadSize" : n    (numeric) Size of DIP2 extra payload. Only present if it's a special TX
    "extraPayload" : "hex"    (string) Hex encoded DIP2 extra payload data. Only present if it's a special TX
    "blockhash" : "hash",   (string) the block hash
    "confirmations" : n,      (numeric) The confirmations
    "time" : ttt,             (numeric) The transaction time in seconds since epoch (Jan 1 1970 GMT)
    "blocktime" : ttt         (numeric) The block time in seconds since epoch (Jan 1 1970 GMT)
    "instantlock" : true|false, (bool) Current transaction lock state
    "instantlock_internal" : true|false, (bool) Current internal transaction lock state
    "chainlock" : true|false, (bool) The state of the corresponding block chainlock
 }

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

getBlockByHeight
```````````
Get the block of the specified hash according to the block height

返回:

.. code-block:: json

 {
    "hash" : "hash",     (string) the block hash (same as provided)
    "confirmations" : n,   (numeric) The number of confirmations, or -1 if the block is not on the main chain
    "size" : n,            (numeric) The block size
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
                "hex": "01000000011db3632af8f48b2ca6dfd21b410ad05129cf32762d586abd6dfef656727536ba010000006b483045022100a86acc0ca389f849ad52f3154dc5d43333ebe2f4163c71b4ac2de30b4dc49b1d022017b0ba9af85150ceedb109e0c0b78d49b843aa6bbfd41cf75626dd94a401bab301210389c9b2ba32f648e3756b3f58a64c462fbccd56d4e48ada71a7224eedeae0e43cfeffffff02408af701000000001976a914916853b469ae7ad8e9d66bb892c336899b615d5788ac70cf0b00000000001976a914c6e8b9d49ff49c751dab2689cfdf0dfb8c9537e488ac00000000",
            rnal": false,
            "chainlock": true
                }"txid": "0e6d444bf4de1773cf4f27834f362bec825af55dea7de267e13484f4e023462c",
            "size": 226,
            "version": 1,
            "type": 0,
            "locktime": 0,
            "vin": [
                {
                "txid": "ba36757256f6fe6dbd6a582d7632cf2951d00a411bd2dfa62c8bf4f82a63b31d",
                "vout": 1,
                "scriptSig": {
                    "asm": "3045022100a86acc0ca389f849ad52f3154dc5d43333ebe2f4163c71b4ac2de30b4dc49b1d022017b0ba9af85150ceedb109e0c0b78d49b843aa6bbfd41cf75626dd94a401bab3[ALL] 0389c9b2ba32f648e3756b3f58a64c462fbccd56d4e48ada71a7224eedeae0e43c",
                    "hex": "483045022100a86acc0ca389f849ad52f3154dc5d43333ebe2f4163c71b4ac2de30b4dc49b1d022017b0ba9af85150ceedb109e0c0b78d49b843aa6bbfd41cf75626dd94a401bab301210389c9b2ba32f648e3756b3f58a64c462fbccd56d4e48ada71a7224eedeae0e43c"
                },
                "sequence": 4294967294
                }
            ],
            "vout": [
                {
                "value": 0.33000000,
                "valueSat": 33000000,
                "n": 0,
                "scriptPubKey": {
                    "asm": "OP_DUP OP_HASH160 916853b469ae7ad8e9d66bb892c336899b615d57 OP_EQUALVERIFY OP_CHECKSIG",
                    "hex": "76a914916853b469ae7ad8e9d66bb892c336899b615d5788ac",
                    "reqSigs": 1,
                    "type": "pubkeyhash",
                    "addresses": [
                    "XowgnqKdQtCvZdztRXp7kFFmMxaGRh4thK"
                    ]
                }
                },
                {
                "value": 0.00774000,
                "valueSat": 774000,
                "n": 1,
                "scriptPubKey": {
                    "asm": "OP_DUP OP_HASH160 c6e8b9d49ff49c751dab2689cfdf0dfb8c9537e4 OP_EQUALVERIFY OP_CHECKSIG",
                    "hex": "76a914c6e8b9d49ff49c751dab2689cfdf0dfb8c9537e488ac",
                    "reqSigs": 1,
                    "type": "pubkeyhash",
                    "addresses": [
                    "XtpaRKDiZdJBw5xaZGLYSTMXxNXcfieMRx"
                    ]
                }
                }
            ],
            "blockhash": "000000000000001a703370075ee3b97fd7fec42adda86b159d60d30ba1ebe645",
            "height": 1142826,
            "confirmations": 15898,
            "time": 1569310357,
            "blocktime": 1569310357,
            "instantlock": true,
            "instantlock_inte
  }
 }
 

decodeRawTransaction
```````````
Return a JSON object representing the serialized, hex-encoded transaction.

Also see createrawtransaction and signrawtransaction calls

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
       "value" : x.xxx,            (numeric) The value in Dash
       "n" : n,                    (numeric) index
       "scriptPubKey" : {          (json object)
         "asm" : "asm",          (string) the asm
         "hex" : "hex",          (string) the hex
         "reqSigs" : n,            (numeric) The required sigs
         "type" : "pubkeyhash",  (string) The type, eg 'pubkeyhash'
         "addresses" : [           (json array of string)
           "12tvKAXCxZjSmdNbao16dKXC8tRWfcF5oc"   (string) Dash address
         ]
       }
     }
     ,...
  ],
   }
  }
 }

