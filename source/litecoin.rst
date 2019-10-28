Litecoin API Docs
===========
getbestblockhash
```````````
Returns the hash of the best (tip) block in the longest block chain.

Definition::

    GET /ltc/getBestBlockHash/

Example Request::

    GET /ltc/getBestBlockHash/

Response:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
    "data": "069234e09f3d2cebcea66397c607279223047f4a05c8825564346fa728c73a68"
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

    GET /ltc/getBlockByHash?hash={hash}    //hash (string) 

Example Request::

    GET /ltc/getBlockByHash?hash=069234e09f3d2cebcea66397c607279223047f4a05c8825564346fa728c73a68

Response:

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

    GET /ltc/getBlockByHeight?height={height}   //height (Integer)
Example Request::

    GET /ltc/getBlockByHeight?height=1724047

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

    GET /ltc/getBlockChainInfo
Example Request::

    GET /ltc/getBlockChainInfo

Response:

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



getBlockCount
```````````
Returns the number of blocks in the longest blockchain

Definition::

    GET /ltc/getBlockCount
Example Request::

    GET /ltc/getBlockCount

Response:

.. code-block:: json

   {
    "status": 0,
    "message": "success",
    "data": 1724047
 }

getBlockHash
```````````
Returns hash of block in best-block-chain at height provided

Definition::

    GET /ltc/getBlockHash?heighth={height}
Example Request::

    GET /ltc/getBlockHash?heighth=1724047

Response:

.. code-block:: json

   {
    "status": 0,
    "message": "success",
    "data": "069234e09f3d2cebcea66397c607279223047f4a05c8825564346fa728c73a68"
 }

getDifficulty
```````````
Returns the proof-of-work difficulty as a multiple of the minimum difficulty

Definition::

    GET /ltc/getDifficulty
Example Request::

    GET /ltc/getDifficulty

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

    GET /ltc/getRawMemPool
Example Request::

    GET /ltc/getRawMemPool

Response:

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
  "value" : x.xxx,           (numeric) The transaction value in LTC
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

    GET /ltc/gettxout?hash={hash}&vouth={vouth}&unconfirmed={unconfirmed}
Example Request::

    GET /ltc/gettxout?hash=xxx&vouth=1&unconfirmed=false

Response:

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

    GET /ltc/getTxOutSetInfo
Example Request::

    GET /ltc/getTxOutSetInfo

Response:

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


verifyChain
```````````
Verifies blockchain database

Definition::

    GET /ltc/verifyChain
Example Request::

    GET /ltc/verifyChain

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

    GET /ltc/verifyChainByParam?checkLevel={checkLevel}&numOfBlocks={numOfBlocks}
Example Request::

    GET /ltc/verifyChainByParam?checkLevel=3&numOfBlocks=6

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

    GET /ltc/createMultiSig?nRequired={nRequired}&keys={nRequired}
Example Request:

    GET /ltc/createMultiSig?nRequired=6&keys=xxxxxxxxxxxxxxxxx

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
    "feerate" : x.x,     (numeric, optional) estimate fee rate in LTC/kB
    "errors": [ str... ] (json array of strings, optional) Errors encountered during processing
    "blocks" : n         (numeric) block number where estimate was found
  }

Definition::

    GET /ltc/estimateSmartFee?blocks={blocks}
Example Request:

    GET /ltc/estimateSmartFee?blocks=1

Response:

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



validateAddress
```````````
Return information about the given bitcoin address

Definition::

    GET /ltc/validateAddress?address={address}
Example Request:

    GET /ltc/validateAddress?address=ltc1qc7eh07c5yu6w8f5lw6n7qttxxnr4zzu03rp5s7

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

    GET /ltc/verifyMessage?address={address}&signature={signature}&message={message}
Example Request:

    GET /ltc/verifyMessage?address=xxxxxxxx&signature=xxxxxxxx&message=xxxxxxxx

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
        "value" : x.xxx,            (numeric) The value in LTC
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

    GET /ltc/queryTransactionInfo?txId={txId}
Example Request:

    GET /ltc/queryTransactionInfo?txId=xxxxxxxxxxxx
Response:

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

decodeRawTransaction
```````````
Return a JSON object representing the serialized, hex-encoded transaction.

Also see createrawtransaction and signrawtransaction calls

Definition::

    GET /ltc/decodeRawTransaction?hex={hex}
Example Request:

    GET /ltc/decodeRawTransaction?hex=xxxxxxxxxx

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
       "value" : x.xxx,            (numeric) The value in LTC
       "n" : n,                    (numeric) index
       "scriptPubKey" : {          (json object)
         "asm" : "asm",          (string) the asm
         "hex" : "hex",          (string) the hex
         "reqSigs" : n,            (numeric) The required sigs
         "type" : "pubkeyhash",  (string) The type, eg 'pubkeyhash'
         "addresses" : [           (json array of string)
           "12tvKAXCxZjSmdNbao16dKXC8tRWfcF5oc"   (string) LTC address
         ]
       }
     }
     ,...
  ],
    }
  }
 }
