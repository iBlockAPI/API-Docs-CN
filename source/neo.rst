Neo API Docs
===========
getAccountState
```````````
Queries global assets (NEO, GAS, and etc.) of the account, according to the account address

Definition::

    GET /neo/getAccountState?address={address}
    
Example Request::

    GET /neo/getAccountState?address=AQyoY3bu9iiEZdf5zqVNDUz6SvofvK11W1

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": {
            "balances": [
                {
                    "asset": "0xc56f33fc6ecfcd0c225c4ab356fee59390af8560be0e930faebe74a6daff7c9b",
                    "value": "49"
                },
                {
                    "asset": "0x602c79718b16e442de58778e148d0b1084e3b2dffd5de6b7b16cee7969282de7",
                    "value": "49.6543137"
                }
            ],
            "frozen": false,
            "votes": [],
            "version": 0,
            "script_hash": "0x8244217561e33854d8a2afa981067ae512b1fa64"
        }
    }

getApplicationLog
```````````
Returns the contract log based on the specified txid. The complete contract logs are stored under the ApplicationLogs directory

Definition::

    GET /neo/getApplicationLog?address={txid}
    
Example Request::

    GET /neo/getApplicationLog?address=92b1ecc0e8ca8d6b03db7fe6297ed38aa5578b3e6316c0526b414b453c89e20d

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": {
            "txid": "0x92b1ecc0e8ca8d6b03db7fe6297ed38aa5578b3e6316c0526b414b453c89e20d",
            "executions": [
                {
                    "trigger": "Application",
                    "contract": "0x6ec33f0d370617dd85e51d31c483b6967074249d",
                    "vmstate": "HALT",
                    "gas_consumed": "2.912",
                    "stack": [
                        {
                            "type": "Integer",
                            "value": "1"
                        }
                    ],
                    "notifications": [
                        {
                            "contract": "0x78e6d16b914fe15bc16150aeb11d0c2a8e532bdd",
                            "state": {
                                "type": "Array",
                                "value": [
                                    {
                                        "type": "ByteArray",
                                        "value": "7472616e73666572"
                                    },
                                    {
                                        "type": "ByteArray",
                                        "value": "d086ac0ed3e578a1afd3c0a2c0d8f0a180405be2"
                                    },
                                    {
                                        "type": "ByteArray",
                                        "value": "002ba7f83fd4d3975dedb84de27345684bea2996"
                                    },
                                    {
                                        "type": "ByteArray",
                                        "value": "0065cd1d00000000"
                                    }
                                ]
                            }
                        }
                    ]
                }
            ]
        }
    }

getAssetState
```````````
Queries the asset information, based on the specified asset number

Definition::

    GET /neo/getAssetState?assetId={assetId}
    
Example Request::

    GET /neo/getAssetState?assetId=c56f33fc6ecfcd0c225c4ab356fee59390af8560be0e930faebe74a6daff7c9b

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": {
            "owner": "00",
            "amount": "100000000",
            "precision": 0,
            "name": [
                {
                    "name": "小蚁股",
                    "lang": "zh-CN"
                },
                {
                    "name": "AntShare",
                    "lang": "en"
                }
            ],
            "available": "100000000",
            "admin": "Abf2qMs1pzQb8kYk9RuxtUb9jtRKJVuBJt",
            "frozen": false,
            "expiration": 4000000,
            "id": "0xc56f33fc6ecfcd0c225c4ab356fee59390af8560be0e930faebe74a6daff7c9b",
            "type": "GoverningToken",
            "version": 0,
            "issuer": "Abf2qMs1pzQb8kYk9RuxtUb9jtRKJVuBJt"
        }
    }

getBestBlockHash
```````````
Get the hash of the highest height block in the main chain

Definition::

    GET /neo/getBestBlockHash
    
Example Request::

    GET /neo/getBestBlockHash

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": "0x2deeb34ac5af3c8373c72c0d7f5b58f36445284b54cb8bb527af68b429ae9cce"
    }

getBlockByHash
```````````
Returns the corresponding block information according to the specified hash value

Definition::

    GET /neo/getBlockByHash?hash={hash}&verbose={Integer}
    
Example Request::

    GET /neo/getBlockByHash?hash=0x2deeb34ac5af3c8373c72c0d7f5b58f36445284b54cb8bb527af68b429ae9cce&verbose=1

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": {
            "nextconsensus": "ANuupE2wgsHYi8VTqSUSoMsyxbJ8P3szu7",
            "tx": [
                {
                    "net_fee": "0.00001",
                    "size": 464,
                    "gas": "0",
                    "txid": "0x834f256dee81a1627e92126a2d48c41d2ad34f101a8d442a29d513c36e5aab38",
                    "attributes": [
                        {
                            "data": "8aae7a62d40eeaf6aa2adaffc2446f8c35763a21",
                            "usage": "Script"
                        },
                        {
                            "data": "4f33583135363936353830393138383836656162613962336538396532303265",
                            "usage": "Remark"
                        }
                    ],
                    "vin": [
                        {
                            "txid": "0x6771d857fb16a8888c67c5c305b93edabdb563a438e1b880b48999ec49eb8d09",
                            "vout": 1
                        }
                    ],
                    "type": "InvocationTransaction",
                    "sys_fee": "0",
                    "scripts": [
                        {
                            "invocation": "40a123289d8b48b483ec901d9b56dec41e74ec5da2a3e8a1d53773c9cb1c4c6fc7af5f534cdeb02ae6fc551b75c1bb99006f1e6a9ae9c336832ab727cedfbc3327",
                            "verification": "2103cb15b80920a7e8c70248cbde8805864cf58c1cc6f5abcaf84074eba607f1318aac"
                        }
                    ],
                    "version": 1,
                    "script": "0460343c0240641b7e2438d3a4dd0ea1e6a146e544615f1738eb70b95f143b90791c1f47854722b420f5ea2fbe5d434546eb5eb75e7a422ea364ee6c674d845609e932cf18c9024b1902260702991e02a304022206000298080103026f0702b80b024807005102f96d60c1096c6f67426174746c6567e219a88c51e65737f67514a28cdd8e4b5a6c51d8",
                    "vout": [
                        {
                            "address": "AdmpNwz8pmNdLHMuncLdZ2NT3gxGbS1h5c",
                            "asset": "0x602c79718b16e442de58778e148d0b1084e3b2dffd5de6b7b16cee7969282de7",
                            "value": "0.75",
                            "n": 0
                        },
                        {
                            "address": "AUR9uvJSPBwoh8G5s3WU1Ua2v1WUkfva8x",
                            "asset": "0x602c79718b16e442de58778e148d0b1084e3b2dffd5de6b7b16cee7969282de7",
                            "value": "2.79973",
                            "n": 1
                        }
                    ]
                }
            ],
            "previousblockhash": "0xdf0c39ed44344c34ac8f860cd213bbd6b1e49899986a88d737f1377ecedb0427",
            "index": 4357024,
            "confirmations": 1,
            "version": 0,
            "nonce": "6e1f22283540a854",
            "script": {
                "invocation": "404e27ad42ff63f369436a81c0a87bb2044c347d0a947825ff548e897969792fbb844416d47988958e583b6d5ecdf15981c2f84535bf82a151369cbc82c38b93c24045bff4dde4f1cf10ae8c258133617717e403b82bce75a97de0c1ac375120ac5dffb7ef22fe4ad1ad170a469f98139e5571c649ba7a6e3cb26f08f00b7845280e40675b826945559b012292fc8ecebe4da51275cc28639424ac9ef7946a90d6611636f0b309284913520c2ed0b43ad2d499a42f7428cdc9ab39bd13a412e0bee4d64020ff3a7f1a292bbb9a9a1bd8c3c1dd4738d3173ba35e7c2f673be3cc90ef81c2966124c4063bffa3640c041abab841b44c52950cd33922fd485270c1b1a8cf03407e176971bbb9cf8758db9a1ed68adc64e2e3dd969f6905bf8bc3ea7e7472d644b092d3e44f74edc04382dc715ebec868a474c9d560d948aae47d2b27e1e2650b",
                "verification": "5521024c7b7fb6c310fccf1ba33b082519d82964ea93868d676662d4a59ad548df0e7d21025bdf3f181f53e9696227843950deb72dcd374ded17c057159513c3d0abe20b6421035e819642a8915a2572f972ddbdbe3042ae6437349295edce9bdc3b8884bbf9a32103b209fd4f53a7170ea4444e0cb0a6bb6a53c2bd016926989cf85f9b0fba17a70c2103b8d9d5771d8f513aa0869b9cc8d50986403b78c6da36890638c3d46a5adce04a2102ca0e27697b9c248f6f16e085fd0061e26f44da85b58ee835c110caa5ec3ba5542102df48f60e8f3e01c48ff40b9b7f1310d7a8b2a193188befe1c2e3df740e89509357ae"
            },
            "nextblockhash": "0x3b9c39cd3207cab6bf99c4a00165820d52c3596d6338b4c78481d3a2a6fe9345",
            "size": 4606,
            "merkleroot": "0x40a1c73381624bc4111ee8159d091ef3031b90eab64de1bd6dc8d9a8eff0a199",
            "time": 1569658102,
            "hash": "0x2deeb34ac5af3c8373c72c0d7f5b58f36445284b54cb8bb527af68b429ae9cce"
        }
    }

getBlockByIndex
```````````
Returns the corresponding block information according to the specified index

Definition::

    GET /neo/getBlockByIndex?index={Integer}&verbose={Integer}
    
Example Request::

    GET /neo/getBlockByIndex?index=4357024&verbose=1

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": {
            "nextconsensus": "ANuupE2wgsHYi8VTqSUSoMsyxbJ8P3szu7",
            "tx": [
                {
                    "net_fee": "0.00001",
                    "size": 464,
                    "gas": "0",
                    "txid": "0x834f256dee81a1627e92126a2d48c41d2ad34f101a8d442a29d513c36e5aab38",
                    "attributes": [
                        {
                            "data": "8aae7a62d40eeaf6aa2adaffc2446f8c35763a21",
                            "usage": "Script"
                        },
                        {
                            "data": "4f33583135363936353830393138383836656162613962336538396532303265",
                            "usage": "Remark"
                        }
                    ],
                    "vin": [
                        {
                            "txid": "0x6771d857fb16a8888c67c5c305b93edabdb563a438e1b880b48999ec49eb8d09",
                            "vout": 1
                        }
                    ],
                    "type": "InvocationTransaction",
                    "sys_fee": "0",
                    "scripts": [
                        {
                            "invocation": "40a123289d8b48b483ec901d9b56dec41e74ec5da2a3e8a1d53773c9cb1c4c6fc7af5f534cdeb02ae6fc551b75c1bb99006f1e6a9ae9c336832ab727cedfbc3327",
                            "verification": "2103cb15b80920a7e8c70248cbde8805864cf58c1cc6f5abcaf84074eba607f1318aac"
                        }
                    ],
                    "version": 1,
                    "script": "0460343c0240641b7e2438d3a4dd0ea1e6a146e544615f1738eb70b95f143b90791c1f47854722b420f5ea2fbe5d434546eb5eb75e7a422ea364ee6c674d845609e932cf18c9024b1902260702991e02a304022206000298080103026f0702b80b024807005102f96d60c1096c6f67426174746c6567e219a88c51e65737f67514a28cdd8e4b5a6c51d8",
                    "vout": [
                        {
                            "address": "AdmpNwz8pmNdLHMuncLdZ2NT3gxGbS1h5c",
                            "asset": "0x602c79718b16e442de58778e148d0b1084e3b2dffd5de6b7b16cee7969282de7",
                            "value": "0.75",
                            "n": 0
                        },
                        {
                            "address": "AUR9uvJSPBwoh8G5s3WU1Ua2v1WUkfva8x",
                            "asset": "0x602c79718b16e442de58778e148d0b1084e3b2dffd5de6b7b16cee7969282de7",
                            "value": "2.79973",
                            "n": 1
                        }
                    ]
                }
            ],
            "previousblockhash": "0xdf0c39ed44344c34ac8f860cd213bbd6b1e49899986a88d737f1377ecedb0427",
            "index": 4357024,
            "confirmations": 1,
            "version": 0,
            "nonce": "6e1f22283540a854",
            "script": {
                "invocation": "404e27ad42ff63f369436a81c0a87bb2044c347d0a947825ff548e897969792fbb844416d47988958e583b6d5ecdf15981c2f84535bf82a151369cbc82c38b93c24045bff4dde4f1cf10ae8c258133617717e403b82bce75a97de0c1ac375120ac5dffb7ef22fe4ad1ad170a469f98139e5571c649ba7a6e3cb26f08f00b7845280e40675b826945559b012292fc8ecebe4da51275cc28639424ac9ef7946a90d6611636f0b309284913520c2ed0b43ad2d499a42f7428cdc9ab39bd13a412e0bee4d64020ff3a7f1a292bbb9a9a1bd8c3c1dd4738d3173ba35e7c2f673be3cc90ef81c2966124c4063bffa3640c041abab841b44c52950cd33922fd485270c1b1a8cf03407e176971bbb9cf8758db9a1ed68adc64e2e3dd969f6905bf8bc3ea7e7472d644b092d3e44f74edc04382dc715ebec868a474c9d560d948aae47d2b27e1e2650b",
                "verification": "5521024c7b7fb6c310fccf1ba33b082519d82964ea93868d676662d4a59ad548df0e7d21025bdf3f181f53e9696227843950deb72dcd374ded17c057159513c3d0abe20b6421035e819642a8915a2572f972ddbdbe3042ae6437349295edce9bdc3b8884bbf9a32103b209fd4f53a7170ea4444e0cb0a6bb6a53c2bd016926989cf85f9b0fba17a70c2103b8d9d5771d8f513aa0869b9cc8d50986403b78c6da36890638c3d46a5adce04a2102ca0e27697b9c248f6f16e085fd0061e26f44da85b58ee835c110caa5ec3ba5542102df48f60e8f3e01c48ff40b9b7f1310d7a8b2a193188befe1c2e3df740e89509357ae"
            },
            "nextblockhash": "0x3b9c39cd3207cab6bf99c4a00165820d52c3596d6338b4c78481d3a2a6fe9345",
            "size": 4606,
            "merkleroot": "0x40a1c73381624bc4111ee8159d091ef3031b90eab64de1bd6dc8d9a8eff0a199",
            "time": 1569658102,
            "hash": "0x2deeb34ac5af3c8373c72c0d7f5b58f36445284b54cb8bb527af68b429ae9cce"
        }
    }

getBlockCount
```````````
Get the number of blocks in the main chain

Definition::

    GET /neo/getBlockCount
    
Example Request::

    GET /neo/getBlockCount

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": 4357025
    }

getBlockHash
```````````
Returns the hash value of the corresponding block, based on the specified index

Definition::

    GET /neo/getBlockHash?index={Integer}
    
Example Request::

    GET /neo/getBlockHash?index=4357024

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": "0x2deeb34ac5af3c8373c72c0d7f5b58f36445284b54cb8bb527af68b429ae9cce"
    }

getBlockHeader
```````````
Returns the corresponding block header information according to the specified script hash

Definition::

    GET /neo/getBlockHeader?hash={hash}&verbose={Integer}
    
Example Request::

    GET /neo/getBlockHeader?hash=0x2deeb34ac5af3c8373c72c0d7f5b58f36445284b54cb8bb527af68b429ae9cce&verbose=0

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": "000000002704dbce7e37f137d7886a989998e4b1d6bb13d20c868fac344c3444ed390cdf99a1f0efa8d9c86dbde14db6ea901b03f31e099d15e81e11c44b628133c7a140f6148f5da07b420054a8403528221f6e4e4e04879cfe60ba3b296b1ff08f112f6071756f01fd4501404e27ad42ff63f369436a81c0a87bb2044c347d0a947825ff548e897969792fbb844416d47988958e583b6d5ecdf15981c2f84535bf82a151369cbc82c38b93c24045bff4dde4f1cf10ae8c258133617717e403b82bce75a97de0c1ac375120ac5dffb7ef22fe4ad1ad170a469f98139e5571c649ba7a6e3cb26f08f00b7845280e40675b826945559b012292fc8ecebe4da51275cc28639424ac9ef7946a90d6611636f0b309284913520c2ed0b43ad2d499a42f7428cdc9ab39bd13a412e0bee4d64020ff3a7f1a292bbb9a9a1bd8c3c1dd4738d3173ba35e7c2f673be3cc90ef81c2966124c4063bffa3640c041abab841b44c52950cd33922fd485270c1b1a8cf03407e176971bbb9cf8758db9a1ed68adc64e2e3dd969f6905bf8bc3ea7e7472d644b092d3e44f74edc04382dc715ebec868a474c9d560d948aae47d2b27e1e2650bf15521024c7b7fb6c310fccf1ba33b082519d82964ea93868d676662d4a59ad548df0e7d21025bdf3f181f53e9696227843950deb72dcd374ded17c057159513c3d0abe20b6421035e819642a8915a2572f972ddbdbe3042ae6437349295edce9bdc3b8884bbf9a32103b209fd4f53a7170ea4444e0cb0a6bb6a53c2bd016926989cf85f9b0fba17a70c2103b8d9d5771d8f513aa0869b9cc8d50986403b78c6da36890638c3d46a5adce04a2102ca0e27697b9c248f6f16e085fd0061e26f44da85b58ee835c110caa5ec3ba5542102df48f60e8f3e01c48ff40b9b7f1310d7a8b2a193188befe1c2e3df740e89509357ae00"
    }

getBlockHeader
```````````
Returns the corresponding block header information according to the specified script hash

Definition::

    GET /neo/getBlockHeader?hash={hash}&verbose={Integer}
    
Example Request::

    GET /neo/getBlockHeader?hash=0x2deeb34ac5af3c8373c72c0d7f5b58f36445284b54cb8bb527af68b429ae9cce&verbose=0

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": "000000002704dbce7e37f137d7886a989998e4b1d6bb13d20c868fac344c3444ed390cdf99a1f0efa8d9c86dbde14db6ea901b03f31e099d15e81e11c44b628133c7a140f6148f5da07b420054a8403528221f6e4e4e04879cfe60ba3b296b1ff08f112f6071756f01fd4501404e27ad42ff63f369436a81c0a87bb2044c347d0a947825ff548e897969792fbb844416d47988958e583b6d5ecdf15981c2f84535bf82a151369cbc82c38b93c24045bff4dde4f1cf10ae8c258133617717e403b82bce75a97de0c1ac375120ac5dffb7ef22fe4ad1ad170a469f98139e5571c649ba7a6e3cb26f08f00b7845280e40675b826945559b012292fc8ecebe4da51275cc28639424ac9ef7946a90d6611636f0b309284913520c2ed0b43ad2d499a42f7428cdc9ab39bd13a412e0bee4d64020ff3a7f1a292bbb9a9a1bd8c3c1dd4738d3173ba35e7c2f673be3cc90ef81c2966124c4063bffa3640c041abab841b44c52950cd33922fd485270c1b1a8cf03407e176971bbb9cf8758db9a1ed68adc64e2e3dd969f6905bf8bc3ea7e7472d644b092d3e44f74edc04382dc715ebec868a474c9d560d948aae47d2b27e1e2650bf15521024c7b7fb6c310fccf1ba33b082519d82964ea93868d676662d4a59ad548df0e7d21025bdf3f181f53e9696227843950deb72dcd374ded17c057159513c3d0abe20b6421035e819642a8915a2572f972ddbdbe3042ae6437349295edce9bdc3b8884bbf9a32103b209fd4f53a7170ea4444e0cb0a6bb6a53c2bd016926989cf85f9b0fba17a70c2103b8d9d5771d8f513aa0869b9cc8d50986403b78c6da36890638c3d46a5adce04a2102ca0e27697b9c248f6f16e085fd0061e26f44da85b58ee835c110caa5ec3ba5542102df48f60e8f3e01c48ff40b9b7f1310d7a8b2a193188befe1c2e3df740e89509357ae00"
    }

getBlockSysFee
```````````
Returns the system fees of the block, based on the specified index

Definition::

    GET /neo/getBlockSysFee?index={Integer}
    
Example Request::

    GET /neo/getBlockSysFee?index=4357024

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": "295271"
    }

getClaimable
```````````
Returns claimable GAS information of the specified address

Definition::

    GET /neo/getClaimable?address={address}
    
Example Request::

    GET /neo/getClaimable?address=ANBXZhr7L3hMzL2jn4VULJM5PjEi8Xsn4B

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": {
            "claimable": [
                {
                    "txid": "52ba70ef18e879785572c917795cd81422c3820b8cf44c24846a30ee7376fd77",
                    "n": 1,
                    "value": 800000,
                    "start_height": 476496,
                    "end_height": 488154,
                    "generated": 746.112,
                    "sys_fee": 3.92,
                    "unclaimed": 750.032
                }
            ],
            "address": "AGofsxAUDwt52KjaB664GYsqVAkULYvKNt",
            "unclaimed": 750.032
        }
    }

getConnectionCount
```````````
Gets the current number of connections for the node

Definition::

    GET /neo/getConnectionCount
    
Example Request::

    GET /neo/getConnectionCount

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": 10
    }

getMetricBlockTimestamp
```````````
Returns timestamps of the specified block and its previous n blocks

Definition::

    GET /neo/getMetricBlockTimestamp?blocksNumbers={Integer}&endHeight={Integer}
    
Example Request::

    GET /neo/getMetricBlockTimestamp?blocksNumbers=4357024&endHeight=4606

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": [
            {
            "timestamp": 1569657553,
            "height": 4356991
            },
            {
            "timestamp": 1569657569,
            "height": 4356992
            }
        ]
    }

getNep5Balances
```````````
Returns the balance of all NEP-5 assets in the specified address

Definition::

    GET /neo/getNep5Balances?address={address}
    
Example Request::

    GET /neo/getNep5Balances?address=AaAzH7af9i5DyUjx9n85brQSFStPMk4FYY

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": {
            "address": "AaAzH7af9i5DyUjx9n85brQSFStPMk4FYY",
            "balance": [
                {
                    "amount": "8420",
                    "asset_hash": "fc732edee1efdf968c23c20a9628eaa5a6ccb934",
                    "last_updated_block": 2458505
                },
                {
                    "amount": "100000000000",
                    "asset_hash": "a87cc2a513f5d8b4a42432343687c2127c60bc3f",
                    "last_updated_block": 2248671
                }
            ]
        }
    }

getNep5Transfers
```````````
Returns all the NEP-5 transaction information occurred in the specified address

Definition::

    GET /neo/getNep5Transfers?address={address}&timestamp={timestamp}
    
Example Request::

    GET /neo/getNep5Transfers?address=AaAzH7af9i5DyUjx9n85brQSFStPMk4FYY&timestamp=1571889431

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": {
            "sent": [],
            "received": [
                {
                    "timestamp": 1555651816,
                    "asset_hash": "600c4f5200db36177e3e8a09e9f18e2fc7d12a0f",
                    "transfer_address": "AYwgBNMepiv5ocGcyNT4mA8zPLTQ8pDBis",
                    "amount": "1000000",
                    "block_index": 436036,
                    "transfer_notify_index": 0,
                    "tx_hash": "df7683ece554ecfb85cf41492c5f143215dd43ef9ec61181a28f922da06aba58"
                }
            ],
            "address": "AbHgdBaWEnHkCiLtDZXjhvhaAK2cwFh5pF"
        }
    }

getPeers
```````````
Gets the list of nodes that the node is currently connected/disconnected from

Definition::

    GET /neo/getPeers
    
Example Request::

    GET /neo/getPeers

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": {
            "connected": [
                {
                    "address": "13.229.192.5",
                    "port": 10333
                },
                {
                    "address": "13.57.25.82",
                    "port": 10333
                }
            ],
            "bad": [],
            "unconnected": [
                {
                    "address": "13.113.217.133",
                    "port": 10333
                },
                {
                    "address": "47.244.154.222",
                    "port": 10333
                }
            ]
        }
    }

getRawMempool
```````````
Obtains the list of unconfirmed transactions in memory

Definition::

    GET /neo/getRawMempool
    
Example Request::

    GET /neo/getRawMempool

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": [
            "0x9786cce0dddb524c40ddbdd5e31a41ed1f6b5c8a683c122f627ca4a007a7cf4e",
            "0xb488ad25eb474f89d5ca3f985cc047ca96bc7373a6d3da8c0f192722896c1cd7",
            "0xf86f6f2c08fbf766ebe59dc84bc3b8829f1053f0a01deb26bf7960d99fa86cd6"
        ]
    }

getRawTransaction
```````````
Returns the corresponding transaction information, based on the specified hash value

Definition::

    GET /neo/getRawTransaction?txid={hash}&verbose={Integer}
    
Example Request::

    GET /neo/getRawTransaction?txid=cd7dbe75de64e47aa4847ac5bbe02d5b69ce7e9c249b5085718db048113337bf&verbose=0

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data":"80000001195876cb34364dc38b730077156c6bc3a7fc570044a66fbfeeea56f71327e8ab0000029b7cffdaa674beae0f930ebe6085af9093e5fe56b34a5c220ccdcf6efc336fc500c65eaf440000000f9a23e06f74cf86b8827a9108ec2e0f89ad956c9b7cffdaa674beae0f930ebe6085af9093e5fe56b34a5c220ccdcf6efc336fc50092e14b5e00000030aab52ad93f6ce17ca07fa88fc191828c58cb71014140915467ecd359684b2dc358024ca750609591aa731a0b309c7fb3cab5cd0836ad3992aa0a24da431f43b68883ea5651d548feb6bd3c8e16376e6e426f91f84c58232103322f35c7819267e721335948d385fae5be66e7ba8c748ac15467dcca0693692dac"
    }

getStorage
```````````
Returns the stored value, according to the contract script hash and the stored key

Definition::

    GET /neo/getStorage?scriptHash={hash}&key={hex}
    
Example Request::

    GET /neo/getStorage?scriptHash=12312312&key=1231231

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data":"4c696e"
    }

getTransactionHeight
```````````
Returns the block index in which the transaction is found

Definition::

    GET /neo/getTransactionHeight?txid={hash}
    
Example Request::

    GET /neo/getTransactionHeight?txid=cd7dbe75de64e47aa4847ac5bbe02d5b69ce7e9c249b5085718db048113337bf

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data":251488
    }

getTxout
```````````
Returns the corresponding unspent transaction output information (returned change), based on the specified hash and index

Definition::

    GET /neo/getTxout?txid={hash}&n={Integer}
    
Example Request::

    GET /neo/getTxout?txid=cd7dbe75de64e47aa4847ac5bbe02d5b69ce7e9c249b5085718db048113337bf&n=10

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data":{
            "n": 0,
            "asset": "c56f33fc6ecfcd0c225c4ab356fee59390af8560be0e930faebe74a6daff7c9b",
            "value": "2950",
            "address": "AHCNSDkh2Xs66SzmyKGdoDKY752uyeXDrt"
        }
    }

getUnclaimed
```````````
Returns unclaimed GAS amount of the specified address

Definition::

    GET /neo/getUnclaimed?address={address}
    
Example Request::

    GET /neo/getUnclaimed?address=AL9ppCyxgPbhaGgVPJHH8qmfoQCSCutQrA

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data":{
            "available": 750.032,
            "unavailable": 2815.408,
            "unclaimed": 3565.44
        }
    }

getUnspents
```````````
Returns information of the unspent UTXO assets (e.g. NEO, GAS) at the specified address

Definition::

    GET /neo/getUnspents?address={address}
    
Example Request::

    GET /neo/getUnspents?address=AL9ppCyxgPbhaGgVPJHH8qmfoQCSCutQrA

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data":{
            "balance": [
                {
                    "unspent": [
                        {
                            "txid": "4ee4af75d5aa60598fbae40ce86fb9a23ffec5a75dfa8b59d259d15f9e304319",
                            "n": 0,
                            "value": 27844.821
                        },
                        {
                            "txid": "9906bf2a9f531ac523aad5e9507bd6540acc1c65ae9144918ccc891188578253",
                            "n": 0,
                            "value": 0.987
                        }
                    ],
                    "asset_hash": "602c79718b16e442de58778e148d0b1084e3b2dffd5de6b7b16cee7969282de7",
                    "asset": "GAS",
                    "asset_symbol": "GAS",
                    "amount": 29060.02316479
                },
                {
                    "unspent": [
                        {
                            "txid": "c3182952855314b3f4b1ecf01a03b891d4627d19426ce841275f6d4c186e729a",
                            "n": 0,
                            "value": 800000
                        }
                    ],
                    "asset_hash": "c56f33fc6ecfcd0c225c4ab356fee59390af8560be0e930faebe74a6daff7c9b",
                    "asset": "NEO",
                    "asset_symbol": "NEO",
                    "amount": 800000
                }
            ],
            "address": "AGofsxAUDwt52KjaB664GYsqVAkULYvKNt"
        }
    }

getValidators
```````````
Returns the current NEO consensus nodes information and voting status

Definition::

    GET /neo/getValidators
    
Example Request::

    GET /neo/getValidators

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data":[
            {
                "publickey": "02486fd15702c4490a26703112a5cc1d0923fd697a33406bd5a1c00e0013b09a70",
                "votes": "46632420",
                "active": true
            },
            {
                "publickey": "024c7b7fb6c310fccf1ba33b082519d82964ea93868d676662d4a59ad548df0e7d",
                "votes": "46632420",
                "active": true
            }
        ]
    }

getcontractstate
```````````
Queries contract information, according to the contract script hash

Definition::

    GET /neo/getcontractstate?scriptHash={hash}
    
Example Request::

    GET /neo/getcontractstate?scriptHash=cd7dbe75de64e47aa4847ac5bbe02d5b69ce7e9c249b5085718db048113337bf

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data":{
            "version": 0,
            "hash": "0xdc675afc61a7c0f7b3d2682bf6e1d8ed865a0e5f",
            "script": "5fc56b6c766b00527ac46c766b51527ac46107576f6f6c6f6e676c766b52527ac403574e476c766b53527ac4006c766b54527ac4210354ae498221046c666efebbaee9bd0eb4823469c98e748494a92a71f346b1a6616c766b55527ac46c766b00c3066465706c6f79876c766b56527ac46c766b56c36416006c766b55c36165f2026c766b57527ac462d8016c766b55c36165d801616c766b00c30b746f74616c537570706c79876c766b58527ac46c766b58c36440006168164e656f2e53746f726167652e476574436f6e7465787406737570706c79617c680f4e656f2e53746f726167652e4765746c766b57527ac46270016c766b00c3046e616d65876c766b59527ac46c766b59c36412006c766b52c36c766b57527ac46247016c766b00c30673796d626f6c876c766b5a527ac46c766b5ac36412006c766b53c36c766b57527ac4621c016c766b00c308646563696d616c73876c766b5b527ac46c766b5bc36412006c766b54c36c766b57527ac462ef006c766b00c30962616c616e63654f66876c766b5c527ac46c766b5cc36440006168164e656f2e53746f726167652e476574436f6e746578746c766b51c351c3617c680f4e656f2e53746f726167652e4765746c766b57527ac46293006c766b51c300c36168184e656f2e52756e74696d652e436865636b5769746e657373009c6c766b5d527ac46c766b5dc3640e00006c766b57527ac46255006c766b00c3087472616e73666572876c766b5e527ac46c766b5ec3642c006c766b51c300c36c766b51c351c36c766b51c352c36165d40361527265c9016c766b57527ac4620e00006c766b57527ac46203006c766b57c3616c756653c56b6c766b00527ac4616168164e656f2e53746f726167652e476574436f6e746578746c766b00c3617c680f4e656f2e53746f726167652e4765746165700351936c766b51527ac46168164e656f2e53746f726167652e476574436f6e746578746c766b00c36c766b51c361651103615272680f4e656f2e53746f726167652e507574616168164e656f2e53746f726167652e476574436f6e7465787406737570706c79617c680f4e656f2e53746f726167652e4765746165f40251936c766b52527ac46168164e656f2e53746f726167652e476574436f6e7465787406737570706c796c766b52c361659302615272680f4e656f2e53746f726167652e50757461616c756653c56b6c766b00527ac461516c766b51527ac46168164e656f2e53746f726167652e476574436f6e746578746c766b00c36c766b51c361654002615272680f4e656f2e53746f726167652e507574616168164e656f2e53746f726167652e476574436f6e7465787406737570706c796c766b51c361650202615272680f4e656f2e53746f726167652e50757461516c766b52527ac46203006c766b52c3616c756659c56b6c766b00527ac46c766b51527ac46c766b52527ac4616168164e656f2e53746f726167652e476574436f6e746578746c766b00c3617c680f4e656f2e53746f726167652e4765746c766b53527ac46168164e656f2e53746f726167652e476574436f6e746578746c766b51c3617c680f4e656f2e53746f726167652e4765746c766b54527ac46c766b53c3616576016c766b52c3946c766b55527ac46c766b54c3616560016c766b52c3936c766b56527ac46c766b55c300a2640d006c766b52c300a2620400006c766b57527ac46c766b57c364ec00616168164e656f2e53746f726167652e476574436f6e746578746c766b00c36c766b55c36165d800615272680f4e656f2e53746f726167652e507574616168164e656f2e53746f726167652e476574436f6e746578746c766b51c36c766b56c361659c00615272680f4e656f2e53746f726167652e5075746155c57600135472616e73666572205375636365737366756cc476516c766b00c3c476526c766b51c3c476536c766b52c3c476546168184e656f2e426c6f636b636861696e2e476574486569676874c46168124e656f2e52756e74696d652e4e6f7469667961516c766b58527ac4620e00006c766b58527ac46203006c766b58c3616c756653c56b6c766b00527ac4616c766b00c36c766b51527ac46c766b51c36c766b52527ac46203006c766b52c3616c756653c56b6c766b00527ac461516c766b00c36a527a527ac46c766b51c36c766b52527ac46203006c766b52c3616c7566",
            "parameters": [
                "ByteArray"
            ],
            "returntype": "ByteArray",
            "name": "Woolong",
            "code_version": "0.9.2",
            "author": "lllwvlvwlll",
            "email": "lllwvlvwlll@gmail.com",
            "description": "GO NEO!!!",
            "properties": {
                "storage": true,
                "dynamic_invoke": false
            }
        }
    }

getversion
```````````
Returns the version information about the queried node

Definition::

    GET /neo/getversion
    
Example Request::

    GET /neo/getversion

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": {
            "port": 10333,
            "useragent": "/Neo:2.10.3/",
            "nonce": 1559077703
        }
    }

listPlugins
```````````
Returns a list of plugins loaded by the node

Definition::

    GET /neo/listPlugins
    
Example Request::

    GET /neo/listPlugins

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": [
            {
            "interfaces": [
                "IRpcPlugin",
                "IPersistencePlugin"
            ],
            "name": "ApplicationLogs",
            "version": "2.10.2.0"
            },
            {
            "interfaces": [
                "IRpcPlugin"
            ],
            "name": "CoreMetrics",
            "version": "2.10.2.0"
            }
        ]
    }

sendRawTransaction
```````````
Broadcasts a transaction over the NEO network

Definition::

    GET /neo/sendRawTransaction?hex={hex}
    
Example Request::

    GET /neo/sendRawTransaction?hex=123123123

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": true
    }

submitBlock
```````````
Broadcasts a raw block over the NEO network

Definition::

    GET /neo/submitBlock?hex={hex}
    
Example Request::

    GET /neo/submitBlock?hex=12312312312312

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": true
    }

validateAddress
```````````
Broadcasts a raw block over the NEO network

Definition::

    GET /neo/validateAddress?address={address}
    
Example Request::

    GET /neo/validateAddress?address=AL9ppCyxgPbhaGgVPJHH8qmfoQCSCutQrA

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": {
            "address": "AL9ppCyxgPbhaGgVPJHH8qmfoQCSCutQrA",
            "isvalid": true
        }
    }