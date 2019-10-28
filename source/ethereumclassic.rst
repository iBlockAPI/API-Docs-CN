EthereumClassic API Docs
===========

ethGetTransactionReceipt
`````````````````
Returns the receipt of a transaction by transaction hash.

Definition::

    GET /eth/ethGetTransactionReceipt?txHash=0x2fd36a4d0ac98e2c01ed3669835927cb1a18375d8bf97e09ac2f4cc287687743
    
Example Request::

    curl -X GET --header 'Accept: application/json' 'http://localhost:8080/eth/ethGetTransactionReceipt?txHash=0x2fd36a4d0ac98e2c01ed3669835927cb1a18375d8bf97e09ac2f4cc287687743'

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": {
            "transactionHash": "0x2fd36a4d0ac98e2c01ed3669835927cb1a18375d8bf97e09ac2f4cc287687743",
            "transactionIndex": 186,
            "blockHash": "0x2d68b3f6414ed8426a55aba998f08bc0f4ae9f3c7b6e827236063a5f526ca10f",
            "blockNumber": 8795598,
            "cumulativeGasUsed": 9980375,
            "gasUsed": 21000,
            "contractAddress": null,
            "root": null,
            "status": "0x1",
            "from": "0x7e4c2d4a37e7b7d1ddeba94bfaa59ac50edf4fad",
            "to": "0x9254d7b911e0f2b02932766a2fe6b21fb8924a97",
            "logs": [],
            "logsBloom": "0x00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000",
            "cumulativeGasUsedRaw": "0x9849d7",
            "transactionIndexRaw": "0xba",
            "blockNumberRaw": "0x8635ce",
            "gasUsedRaw": "0x5208",
            "statusOK": true
        }
    }


ethGetTransactionByHash
`````````````````
Returns the information about a transaction requested by transaction hash.

Definition::

    GET /eth/ethGetTransactionByHash?txHash=0x2fd36a4d0ac98e2c01ed3669835927cb1a18375d8bf97e09ac2f4cc287687743
    
Example Request::

    curl -X GET --header 'Accept: application/json' 'http://localhost:8080/eth/ethGetTransactionByHash?txHash=0x2fd36a4d0ac98e2c01ed3669835927cb1a18375d8bf97e09ac2f4cc287687743'

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": {
            "id": 6,
            "jsonrpc": "2.0",
            "result": {
                "hash": "0x2fd36a4d0ac98e2c01ed3669835927cb1a18375d8bf97e09ac2f4cc287687743",
                "nonce": 11,
                "blockHash": "0x2d68b3f6414ed8426a55aba998f08bc0f4ae9f3c7b6e827236063a5f526ca10f",
                "blockNumber": 8795598,
                "transactionIndex": 186,
                "from": "0x7e4c2d4a37e7b7d1ddeba94bfaa59ac50edf4fad",
                "to": "0x9254d7b911e0f2b02932766a2fe6b21fb8924a97",
                "value": 376160000000000,
                "gasPrice": 6000000000,
                "gas": 21000,
                "input": "0x",
                "creates": null,
                "publicKey": null,
                "raw": null,
                "r": "0x4892a5321ef66a66e7b299d1d5fe42eb62b3431d9d65e6255f08d18283bfad68",
                "s": "0x27d736bb643c4a90d4d978b5fc934e6ed488fc19103b79c4435fd5188fa130d8",
                "v": 37,
                "transactionIndexRaw": "0xba",
                "blockNumberRaw": "0x8635ce",
                "chainId": 1,
                "nonceRaw": "0xb",
                "gasRaw": "0x5208",
                "gasPriceRaw": "0x165a0bc00",
                "valueRaw": "0x1561d932dc000"
            },
            "error": null,
            "rawResponse": null,
            "transaction": {
                "hash": "0x2fd36a4d0ac98e2c01ed3669835927cb1a18375d8bf97e09ac2f4cc287687743",
                "nonce": 11,
                "blockHash": "0x2d68b3f6414ed8426a55aba998f08bc0f4ae9f3c7b6e827236063a5f526ca10f",
                "blockNumber": 8795598,
                "transactionIndex": 186,
                "from": "0x7e4c2d4a37e7b7d1ddeba94bfaa59ac50edf4fad",
                "to": "0x9254d7b911e0f2b02932766a2fe6b21fb8924a97",
                "value": 376160000000000,
                "gasPrice": 6000000000,
                "gas": 21000,
                "input": "0x",
                "creates": null,
                "publicKey": null,
                "raw": null,
                "r": "0x4892a5321ef66a66e7b299d1d5fe42eb62b3431d9d65e6255f08d18283bfad68",
                "s": "0x27d736bb643c4a90d4d978b5fc934e6ed488fc19103b79c4435fd5188fa130d8",
                "v": 37,
                "transactionIndexRaw": "0xba",
                "blockNumberRaw": "0x8635ce",
                "chainId": 1,
                "nonceRaw": "0xb",
                "gasRaw": "0x5208",
                "gasPriceRaw": "0x165a0bc00",
                "valueRaw": "0x1561d932dc000"
            }
        }
    }

ethGetBlockByHash
`````````````````
Returns information about a block by hash.

Definition::

    GET /eth/ethGetBlockByHash?txHash=0x9de9fa4172199ad230af553ac26ffa6b10f2d896d61a5e71f3f30dea5da62d65
    
Example Request::

    curl -X GET --header 'Accept: application/json' 'http://localhost:8080/eth/ethGetBlockByHash?txHash=0x9de9fa4172199ad230af553ac26ffa6b10f2d896d61a5e71f3f30dea5da62d65'

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": {
            "number": 8795764,
            "hash": "0x9de9fa4172199ad230af553ac26ffa6b10f2d896d61a5e71f3f30dea5da62d65",
            "parentHash": "0xbc2aa0bb1ec55c316bf6cc3e587b1080df9045e55fd50e14065e9c59b92cf958",
            "nonce": 10180611859362855000,
            "sha3Uncles": "0x1dcc4de8dec75d7aab85b567b6ccd41ad312451b948a7413f0a142fd40d49347",
            "logsBloom": "0x5a50a0002a020a0802011264830116004421916620190b0c9022000d18228cc00400480800421502aca00102240001095b04758538412b179c005102017460125d3a8990a04284220402168e81c600801f96212843c000c40102c0481590b4e41824d00606084102680030bc0140280a400538802a2706088400859250c051a94208007c80170a000008ca11a0900a8c0805c4953704064548194200601c20014a0a800200018813651200808d008f90030a4064800c0a0800001001181b02801950402bc0802071a10223001044942720a10c8a00300449080a589a0a09641120d32dc4168062082001034fb43081905913c00a95000102090088440d815711",
            "transactionsRoot": "0xc38555b67ec17c849c2aa0ff427fac5758880d3af8e326498451cbfaae656c66",
            "stateRoot": "0xae079e6819475221f79ffcf3dce5520d6749dd5a689640c6fe44dbc6235e575c",
            "receiptsRoot": "0x62061bab522039802c1a43bff6da0168891f3ced13dc932433b61b1c7b458d1e",
            "author": null,
            "miner": "0xea674fdde714fd979de3edf0f56aa9716b898ec8",
            "mixHash": "0xb5038cb1793dec31e9e409cd85ab1e02800d52caa729c455e9f2416255de19c4",
            "difficulty": 2504433270499895,
            "totalDifficulty": 1.2511530675610835e+22,
            "extraData": "0x505059452d65746865726d696e652d6575312d31",
            "size": 26265,
            "gasLimit": 9982482,
            "gasUsed": 9978169,
            "timestamp": 1571821118,
            "transactions": [{
                    "hash": "0xb2fccf160f2f7bd40c75373920d5612429fbab09730c2d2a16160b6b7d67f517",
                    "nonce": 23268118,
                    "blockHash": "0x9de9fa4172199ad230af553ac26ffa6b10f2d896d61a5e71f3f30dea5da62d65",
                    "blockNumber": 8795764,
                    "transactionIndex": 0,
                    "from": "0xea674fdde714fd979de3edf0f56aa9716b898ec8",
                    "to": "0x32d779ac804337e89a5c4a83716b8858530ff9c5",
                    "value": 50078403318330940,
                    "gasPrice": 1000000000,
                    "gas": 50000,
                    "input": "0x",
                    "creates": null,
                    "publicKey": null,
                    "raw": null,
                    "r": "0xb9bc43ea7a0e8cc456e61516186aca0fbd55fbbb40b5c60ed74b39c61289d973",
                    "s": "0x71edfdabdeed09013747e5ae759df139ecb9707d4332d8f3a518b7dc12358f28",
                    "v": 37,
                    "transactionIndexRaw": "0x0",
                    "blockNumberRaw": "0x863674",
                    "nonceRaw": "0x1630b16",
                    "valueRaw": "0xb1ea0ae0b53640",
                    "gasPriceRaw": "0x3b9aca00",
                    "chainId": 1,
                    "gasRaw": "0xc350"
                }, {
                    "hash": "0x2ae6d4b0fa1ed50f5669ac0d54929136c63ba8d08dec0881a20f7d35cf66cebb",
                    "nonce": 23268119,
                    "blockHash": "0x9de9fa4172199ad230af553ac26ffa6b10f2d896d61a5e71f3f30dea5da62d65",
                    "blockNumber": 8795764,
                    "transactionIndex": 1,
                    "from": "0xea674fdde714fd979de3edf0f56aa9716b898ec8",
                    "to": "0x41994bbfb6c210901e4cd39d87c2f0ae47cfe8d3",
                    "value": 72635648797365580,
                    "gasPrice": 1000000000,
                    "gas": 50000,
                    "input": "0x",
                    "creates": null,
                    "publicKey": null,
                    "raw": null,
                    "r": "0x8b40d75947cccbf24215bd449280943c40d215b81903a4e9c528706919a1b82c",
                    "s": "0x36b8562bb2533fe3370382bba3f961b0fef97f12fd7dcbc467bdb6f67b07c32a",
                    "v": 37,
                    "transactionIndexRaw": "0x1",
                    "blockNumberRaw": "0x863674",
                    "nonceRaw": "0x1630b17",
                    "valueRaw": "0x1020dbcdc98d54c",
                    "gasPriceRaw": "0x3b9aca00",
                    "chainId": 1,
                    "gasRaw": "0xc350"
                }
            ],
            "uncles": [],
            "sealFields": null,
            "totalDifficultyRaw": "0x2a6405e2c899ad5c94a",
            "numberRaw": "0x863674",
            "nonceRaw": "0x8d48cc8c0173b8a5",
            "timestampRaw": "0x5db0163e",
            "sizeRaw": "0x6699",
            "gasLimitRaw": "0x985212",
            "gasUsedRaw": "0x984139",
            "difficultyRaw": "0x8e5c4cf73aa37"
        }
    }


ethGetBlockByNumber
`````````````````
Returns information about a block by block number.

Definition::

    GET /eth/ethGetBlockByNumber?number=8795764
    
Example Request::

    curl -X GET --header 'Accept: application/json' 'http://localhost:8080/eth/ethGetBlockByNumber?number=8795764'

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": {
            "number": 8795764,
            "hash": "0x9de9fa4172199ad230af553ac26ffa6b10f2d896d61a5e71f3f30dea5da62d65",
            "parentHash": "0xbc2aa0bb1ec55c316bf6cc3e587b1080df9045e55fd50e14065e9c59b92cf958",
            "nonce": 10180611859362855000,
            "sha3Uncles": "0x1dcc4de8dec75d7aab85b567b6ccd41ad312451b948a7413f0a142fd40d49347",
            "logsBloom": "0x5a50a0002a020a0802011264830116004421916620190b0c9022000d18228cc00400480800421502aca00102240001095b04758538412b179c005102017460125d3a8990a04284220402168e81c600801f96212843c000c40102c0481590b4e41824d00606084102680030bc0140280a400538802a2706088400859250c051a94208007c80170a000008ca11a0900a8c0805c4953704064548194200601c20014a0a800200018813651200808d008f90030a4064800c0a0800001001181b02801950402bc0802071a10223001044942720a10c8a00300449080a589a0a09641120d32dc4168062082001034fb43081905913c00a95000102090088440d815711",
            "transactionsRoot": "0xc38555b67ec17c849c2aa0ff427fac5758880d3af8e326498451cbfaae656c66",
            "stateRoot": "0xae079e6819475221f79ffcf3dce5520d6749dd5a689640c6fe44dbc6235e575c",
            "receiptsRoot": "0x62061bab522039802c1a43bff6da0168891f3ced13dc932433b61b1c7b458d1e",
            "author": null,
            "miner": "0xea674fdde714fd979de3edf0f56aa9716b898ec8",
            "mixHash": "0xb5038cb1793dec31e9e409cd85ab1e02800d52caa729c455e9f2416255de19c4",
            "difficulty": 2504433270499895,
            "totalDifficulty": 1.2511530675610835e+22,
            "extraData": "0x505059452d65746865726d696e652d6575312d31",
            "size": 26265,
            "gasLimit": 9982482,
            "gasUsed": 9978169,
            "timestamp": 1571821118,
            "transactions": [{
                    "hash": "0xb2fccf160f2f7bd40c75373920d5612429fbab09730c2d2a16160b6b7d67f517",
                    "nonce": 23268118,
                    "blockHash": "0x9de9fa4172199ad230af553ac26ffa6b10f2d896d61a5e71f3f30dea5da62d65",
                    "blockNumber": 8795764,
                    "transactionIndex": 0,
                    "from": "0xea674fdde714fd979de3edf0f56aa9716b898ec8",
                    "to": "0x32d779ac804337e89a5c4a83716b8858530ff9c5",
                    "value": 50078403318330940,
                    "gasPrice": 1000000000,
                    "gas": 50000,
                    "input": "0x",
                    "creates": null,
                    "publicKey": null,
                    "raw": null,
                    "r": "0xb9bc43ea7a0e8cc456e61516186aca0fbd55fbbb40b5c60ed74b39c61289d973",
                    "s": "0x71edfdabdeed09013747e5ae759df139ecb9707d4332d8f3a518b7dc12358f28",
                    "v": 37,
                    "chainId": 1,
                    "valueRaw": "0xb1ea0ae0b53640",
                    "gasPriceRaw": "0x3b9aca00",
                    "gasRaw": "0xc350",
                    "nonceRaw": "0x1630b16",
                    "blockNumberRaw": "0x863674",
                    "transactionIndexRaw": "0x0"
                }, {
                    "hash": "0x2ae6d4b0fa1ed50f5669ac0d54929136c63ba8d08dec0881a20f7d35cf66cebb",
                    "nonce": 23268119,
                    "blockHash": "0x9de9fa4172199ad230af553ac26ffa6b10f2d896d61a5e71f3f30dea5da62d65",
                    "blockNumber": 8795764,
                    "transactionIndex": 1,
                    "from": "0xea674fdde714fd979de3edf0f56aa9716b898ec8",
                    "to": "0x41994bbfb6c210901e4cd39d87c2f0ae47cfe8d3",
                    "value": 72635648797365580,
                    "gasPrice": 1000000000,
                    "gas": 50000,
                    "input": "0x",
                    "creates": null,
                    "publicKey": null,
                    "raw": null,
                    "r": "0x8b40d75947cccbf24215bd449280943c40d215b81903a4e9c528706919a1b82c",
                    "s": "0x36b8562bb2533fe3370382bba3f961b0fef97f12fd7dcbc467bdb6f67b07c32a",
                    "v": 37,
                    "chainId": 1,
                    "valueRaw": "0x1020dbcdc98d54c",
                    "gasPriceRaw": "0x3b9aca00",
                    "gasRaw": "0xc350",
                    "nonceRaw": "0x1630b17",
                    "blockNumberRaw": "0x863674",
                    "transactionIndexRaw": "0x1"
                }
            ],
            "uncles": [],
            "sealFields": null,
            "numberRaw": "0x863674",
            "gasUsedRaw": "0x984139",
            "gasLimitRaw": "0x985212",
            "nonceRaw": "0x8d48cc8c0173b8a5",
            "difficultyRaw": "0x8e5c4cf73aa37",
            "sizeRaw": "0x6699",
            "timestampRaw": "0x5db0163e",
            "totalDifficultyRaw": "0x2a6405e2c899ad5c94a"
        }
    }


ethGetBalance
`````````````````
Returns the balance(integer of the current balance in wei.) of the account of given address.

Definition::

    GET /eth/ethGetBalance?address=0xea674fdde714fd979de3edf0f56aa9716b898ec8
    
Example Request::

    curl -X GET --header 'Accept: application/json' 'http://localhost:8080/eth/ethGetBalance?address=0xea674fdde714fd979de3edf0f56aa9716b898ec8'

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": 521236181469710200000
    }


ethBlockNumber
`````````````````
Returns the number of most recent block.

Definition::

    GET /eth/ethBlockNumber
    
Example Request::

    curl -X GET --header 'Accept: application/json' 'http://localhost:8080/eth/ethBlockNumber'

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": 8795861
    }
