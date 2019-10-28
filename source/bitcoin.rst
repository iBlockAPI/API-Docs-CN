Bitcoin API Docs
===========
getbestblockhash
```````````
Returns the hash of the best (tip) block in the longest block chain.

Definition::

    GET /btc/getBestBlockHash/

Example Request::

    GET /btc/getBestBlockHash/

Response:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
    "data": "0000000000000000000f7cf7d8b4aaf52c5bc7980170fd95bde609b424b19946"
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

Definition::

    GET /btc/getBlockByHash?hash={hash}    //hash (string) 

Example Request::

    GET /btc/getBlockByHash?hash=00000000000000000009ebd5b872ca8f18255889ee5629a0b764a25e3659b326

Response:

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

Definition::

    GET /btc/getBlockByHeight?height={height}   //height (Integer)
Example Request::

    GET /btc/getBlockByHeight?height=600618

Response:

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
    "pruneheight": xxxxxx,        (numeric) lowest-height complete block stored (only present if pruning is enabled)
    "automatic_pruning": xx,      (boolean) whether automatic pruning is enabled (only present if pruning is enabled)
    "prune_target_size": xxxxxx,  (numeric) the target size used by pruning (only present if automatic pruning is enabled)
    "softforks": [                (array) status of softforks in progress
        {
            "id": "xxxx",           (string) name of softfork
            "version": xx,          (numeric) block version
            "reject": {             (object) progress toward rejecting pre-softfork blocks
            "status": xx,        (boolean) true if threshold reached
            },
        }, ...
    ],
    "bip9_softforks": {           (object) status of BIP9 softforks in progress
        "xxxx" : {                 (string) name of the softfork
            "status": "xxxx",       (string) one of "defined", "started", "locked_in", "active", "failed"
            "bit": xx,              (numeric) the bit (0-28) in the block version field used to signal this softfork (only for "started" status)
            "startTime": xx,        (numeric) the minimum median time past of a block at which the bit gains its meaning
            "timeout": xx,          (numeric) the median time past of a block at which the deployment is considered failed if not yet locked in
            "since": xx,            (numeric) height of the first block to which the status applies
            "statistics": {         (object) numeric statistics about BIP9 signalling for a softfork (only for "started" status)
            "period": xx,        (numeric) the length in blocks of the BIP9 signalling period
            "threshold": xx,     (numeric) the number of blocks with the version bit set required to activate the feature
            "elapsed": xx,       (numeric) the number of blocks elapsed since the beginning of the current period
            "count": xx,         (numeric) the number of blocks with the version bit set in the current period
            "possible": xx       (boolean) returns false if there are not enough blocks left in this period to pass activation threshold
            }
        }
    }
    "warnings" : "...",           (string) any network and blockchain warnings.
 }

Definition::

    GET /btc/getBlockChainInfo
Example Request::

    GET /btc/getBlockChainInfo

Response:

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



getBlockCount
```````````
Returns the number of blocks in the longest blockchain

Definition::

    GET /btc/getBlockCount
Example Request::

    GET /btc/getBlockCount

Response:

.. code-block:: json

   {
    "status": 0,
    "message": "success",
    "data": 600626
 }

getBlockHash
```````````
Returns hash of block in best-block-chain at height provided

Definition::

    GET /btc/getBlockHash?heighth={height}
Example Request::

    GET /btc/getBlockHash?heighth=600626

Response:

.. code-block:: json

   {
    "status": 0,
    "message": "success",
    "data": "00000000000000000000c6e0c8a6587835746ae98018b6740bc8c15751ee3900"
 }

getDifficulty
```````````
Returns the proof-of-work difficulty as a multiple of the minimum difficulty

Definition::

    GET /btc/getDifficulty
Example Request::

    GET /btc/getDifficulty

Response:

.. code-block:: json

   {
    "status": 0,
    "message": "success",
    "data": 13008091666971.9
 }


getRawMemPool
```````````
Returns all transaction ids in memory pool as a json array of string transaction ids

Hint: use getmempoolentry to fetch a specific transaction from the mempool

Definition::

    GET /btc/getRawMemPool
Example Request::

    GET /btc/getRawMemPool

Response:

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

Definition::

    GET /btc/gettxout?hash={hash}&vouth={vouth}&unconfirmed={unconfirmed}
Example Request::

    GET /btc/gettxout?hash=xxx&vouth=1&unconfirmed=false

Response:

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

Definition::

    GET /btc/getTxOutSetInfo
Example Request::

    GET /btc/getTxOutSetInfo

Response:

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


verifyChain
```````````
Verifies blockchain database

Definition::

    GET /btc/verifyChain
Example Request::

    GET /btc/verifyChain

Response:

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

Definition::

    GET /btc/verifyChainByParam?checkLevel={checkLevel}&numOfBlocks={numOfBlocks}
Example Request::

    GET /btc/verifyChainByParam?checkLevel=3&numOfBlocks=6

Response:

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

Definition::

    GET /btc/createMultiSig?nRequired={nRequired}&keys={nRequired}
Example Request:

    GET /btc/createMultiSig?nRequired=6&keys=xxxxxxxxxxxxxxxxx

Response:

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
    "feerate" : x.x,     (numeric, optional) estimate fee rate in BTC/kB
    "errors": [ str... ] (json array of strings, optional) Errors encountered during processing
    "blocks" : n         (numeric) block number where estimate was found
  }

Definition::

    GET /btc/estimateSmartFee?blocks={blocks}
Example Request:

    GET /btc/estimateSmartFee?blocks=1

Response:

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



validateAddress
```````````
Return information about the given bitcoin address

Definition::

    GET /btc/validateAddress?address={address}
Example Request:

    GET /btc/validateAddress?address=3LwxH2frucsDJfFainnKKGonJduHXesXAD

Response:

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


Definition::

    GET /btc/verifyMessage?bitcoinAddress={address}&signature={signature}&message={message}
Example Request:

    GET /btc/verifyMessage?bitcoinAddress=xxxxxxxx&signature=xxxxxxxx&message=xxxxxxxx

Response:

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

Definition::

    GET /btc/queryTransactionInfo?txId={txId}
Example Request:

    GET /btc/queryTransactionInfo?txId=xxxxxxxxxxxx
Response:

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
 

decodeRawTransaction
```````````
Return a JSON object representing the serialized, hex-encoded transaction.

Also see createrawtransaction and signrawtransaction calls

Definition::

    GET /btc/decodeRawTransaction?hex={hex}
Example Request:

    GET /btc/decodeRawTransaction?hex=xxxxxxxxxx

Response:

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

