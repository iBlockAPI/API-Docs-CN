Tron API Docs
===========
getNowBlock
```````````
查询最新块。

定义::

    GET /trx/getNowBlock/
    
请求示例::

    GET /trx/getNowBlock/

返回:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": {
            "blockID": "0000000000d354bbd46b43ba64897698e9d727fd16e7730ecf2612bca32195f3",
            "block_header": {
            "raw_data": {
                "number": 13849787,
                "txTrieRoot": "630b68ed807d398e3c79d88466376b7f04b7b0ae74526fd3590c0251607463d0",
                "witness_address": "41d25855804e4e65de904faf3ac74b0bdfc53fac76",
                "parentHash": "0000000000d354ba4e12c69b9e76022dfbe2b170ec33499905615145a6772431",
                "version": 9,
                "timestamp": 1571795934000
            }
            },
            "transactions": [
            {
                "ret": [
                {
                    "contractRet": "SUCCESS"
                }
                ],
                "signature": [
                "096c70f3b73fce5d8bcac0a8e886e729d70f3e659040448da73980da5a0bdd4b25092f9348caac4dcb246a434e69a4bc263135b10328f2b1defe365486dcd4a500"
                ],
                "txID": "ebd1ce89f031964e1a0620e3d2d38cf76eb0949615643eac8ec3bb0e1bfdde22",
                "raw_data": {
                "contract": [
                    {
                    "parameter": {
                        "value": {
                        "data": "a3082be900000000000000000000000000000000000000000000000000000000000000310000000000000000000000000000000000000000000000000000000000000000",
                        "owner_address": "41e78f6df1d536b0bfb2c4a8d71dd7a892b65179f5",
                        "contract_address": "41e42d76d15b7ecd27a92cc9551738c2635c63b71c",
                        "call_value": 10000000
                        },
                        "type_url": "type.googleapis.com/protocol.TriggerSmartContract"
                    },
                    "type": "TriggerSmartContract"
                    }
                ],
                "ref_block_bytes": "54a7",
                "ref_block_hash": "d4037270a1694d6d",
                "expiration": 1571795988000,
                "fee_limit": 6000000,
                "timestamp": 1571795931057
                },
                "raw_data_hex": "0a0254a72208d4037270a1694d6d40a0dcddb2df2d5ab301081f12ae010a31747970652e676f6f676c65617069732e636f6d2f70726f746f636f6c2e54726967676572536d617274436f6e747261637412790a1541e78f6df1d536b0bfb2c4a8d71dd7a892b65179f5121541e42d76d15b7ecd27a92cc9551738c2635c63b71c1880ade2042244a3082be90000000000000000000000000000000000000000000000000000000000000031000000000000000000000000000000000000000000000000000000000000000070b19fdab2df2d9001809bee02"
            },
            {
                "ret": [
                {
                    "contractRet": "SUCCESS"
                }
                ],
                "signature": [
                "d96553310e242db28f0288223e29148a2260d19683325905a35cabc97ad5edfe3e4e57c8a4d3eaac4756f324b7d70be91166acf00751605d81e962294c82b2d600"
                ],
                "txID": "9e55e7d6e25da0458b9928ccff8ff3c988e1f8dd5a65e02c1da86d635af8632b",
                "raw_data": {
                "contract": [
                    {
                    "parameter": {
                        "value": {
                        "data": "cad9acb50000000000000000000000000000000000000000000000000000000000000060000000000000000000000000bd3ae7330b91e8fe0c2702db7fe38535c01edb09000000000000000000000000000000000000000000000000000000002ef7ed0000000000000000000000000000000000000000000000000000000000000000203135373137363731323138363430706959474f5a4a436f335134494233626430",
                        "owner_address": "410bb9d6a228547dd5056961dc6714975e0f9f4e69",
                        "contract_address": "4154458d3303622e755c3a5aa29b37e831941ffeff"
                        },
                        "type_url": "type.googleapis.com/protocol.TriggerSmartContract"
                    },
                    "type": "TriggerSmartContract"
                    }
                ],
                "ref_block_bytes": "54a7",
                "ref_block_hash": "d4037270a1694d6d",
                "expiration": 1571795988000,
                "fee_limit": 10000000,
                "timestamp": 1571795930660
                },
                "raw_data_hex": "0a0254a72208d4037270a1694d6d40a0dcddb2df2d5a9002081f128b020a31747970652e676f6f676c65617069732e636f6d2f70726f746f636f6c2e54726967676572536d617274436f6e747261637412d5010a15410bb9d6a228547dd5056961dc6714975e0f9f4e6912154154458d3303622e755c3a5aa29b37e831941ffeff22a401cad9acb50000000000000000000000000000000000000000000000000000000000000060000000000000000000000000bd3ae7330b91e8fe0c2702db7fe38535c01edb09000000000000000000000000000000000000000000000000000000002ef7ed0000000000000000000000000000000000000000000000000000000000000000203135373137363731323138363430706959474f5a4a436f33513449423362643070a49cdab2df2d900180ade204"
            }
            ]
        }
    }

getBlockByNum
```````````
通过高度查询块

定义::

    GET /trx/getBlockByNum?num={int}
    
请求示例::

    GET /trx/getNowBlock?num=1234

返回:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": {
            "blockID": "0000000000d354bbd46b43ba64897698e9d727fd16e7730ecf2612bca32195f3",
            "block_header": {
            "raw_data": {
                "number": 13849787,
                "txTrieRoot": "630b68ed807d398e3c79d88466376b7f04b7b0ae74526fd3590c0251607463d0",
                "witness_address": "41d25855804e4e65de904faf3ac74b0bdfc53fac76",
                "parentHash": "0000000000d354ba4e12c69b9e76022dfbe2b170ec33499905615145a6772431",
                "version": 9,
                "timestamp": 1571795934000
            }
            },
            "transactions": [
            {
                "ret": [
                {
                    "contractRet": "SUCCESS"
                }
                ],
                "signature": [
                "096c70f3b73fce5d8bcac0a8e886e729d70f3e659040448da73980da5a0bdd4b25092f9348caac4dcb246a434e69a4bc263135b10328f2b1defe365486dcd4a500"
                ],
                "txID": "ebd1ce89f031964e1a0620e3d2d38cf76eb0949615643eac8ec3bb0e1bfdde22",
                "raw_data": {
                "contract": [
                    {
                    "parameter": {
                        "value": {
                        "data": "a3082be900000000000000000000000000000000000000000000000000000000000000310000000000000000000000000000000000000000000000000000000000000000",
                        "owner_address": "41e78f6df1d536b0bfb2c4a8d71dd7a892b65179f5",
                        "contract_address": "41e42d76d15b7ecd27a92cc9551738c2635c63b71c",
                        "call_value": 10000000
                        },
                        "type_url": "type.googleapis.com/protocol.TriggerSmartContract"
                    },
                    "type": "TriggerSmartContract"
                    }
                ],
                "ref_block_bytes": "54a7",
                "ref_block_hash": "d4037270a1694d6d",
                "expiration": 1571795988000,
                "fee_limit": 6000000,
                "timestamp": 1571795931057
                },
                "raw_data_hex": "0a0254a72208d4037270a1694d6d40a0dcddb2df2d5ab301081f12ae010a31747970652e676f6f676c65617069732e636f6d2f70726f746f636f6c2e54726967676572536d617274436f6e747261637412790a1541e78f6df1d536b0bfb2c4a8d71dd7a892b65179f5121541e42d76d15b7ecd27a92cc9551738c2635c63b71c1880ade2042244a3082be90000000000000000000000000000000000000000000000000000000000000031000000000000000000000000000000000000000000000000000000000000000070b19fdab2df2d9001809bee02"
            },
            {
                "ret": [
                {
                    "contractRet": "SUCCESS"
                }
                ],
                "signature": [
                "d96553310e242db28f0288223e29148a2260d19683325905a35cabc97ad5edfe3e4e57c8a4d3eaac4756f324b7d70be91166acf00751605d81e962294c82b2d600"
                ],
                "txID": "9e55e7d6e25da0458b9928ccff8ff3c988e1f8dd5a65e02c1da86d635af8632b",
                "raw_data": {
                "contract": [
                    {
                    "parameter": {
                        "value": {
                        "data": "cad9acb50000000000000000000000000000000000000000000000000000000000000060000000000000000000000000bd3ae7330b91e8fe0c2702db7fe38535c01edb09000000000000000000000000000000000000000000000000000000002ef7ed0000000000000000000000000000000000000000000000000000000000000000203135373137363731323138363430706959474f5a4a436f335134494233626430",
                        "owner_address": "410bb9d6a228547dd5056961dc6714975e0f9f4e69",
                        "contract_address": "4154458d3303622e755c3a5aa29b37e831941ffeff"
                        },
                        "type_url": "type.googleapis.com/protocol.TriggerSmartContract"
                    },
                    "type": "TriggerSmartContract"
                    }
                ],
                "ref_block_bytes": "54a7",
                "ref_block_hash": "d4037270a1694d6d",
                "expiration": 1571795988000,
                "fee_limit": 10000000,
                "timestamp": 1571795930660
                },
                "raw_data_hex": "0a0254a72208d4037270a1694d6d40a0dcddb2df2d5a9002081f128b020a31747970652e676f6f676c65617069732e636f6d2f70726f746f636f6c2e54726967676572536d617274436f6e747261637412d5010a15410bb9d6a228547dd5056961dc6714975e0f9f4e6912154154458d3303622e755c3a5aa29b37e831941ffeff22a401cad9acb50000000000000000000000000000000000000000000000000000000000000060000000000000000000000000bd3ae7330b91e8fe0c2702db7fe38535c01edb09000000000000000000000000000000000000000000000000000000002ef7ed0000000000000000000000000000000000000000000000000000000000000000203135373137363731323138363430706959474f5a4a436f33513449423362643070a49cdab2df2d900180ade204"
            }
            ]
         }
        }

getBlockById
```````````
通过ID(Hash)查询块

定义::

    GET /trx/getBlockById?id={hash}
    
请求示例::

    GET /trx/getBlockById?id=0000000000d355af382b789f7870b0504206fb212cd6bac078b8d89e2ede0ee5 

返回:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": {
            "blockID": "0000000000d354bbd46b43ba64897698e9d727fd16e7730ecf2612bca32195f3",
            "block_header": {
            "raw_data": {
                "number": 13849787,
                "txTrieRoot": "630b68ed807d398e3c79d88466376b7f04b7b0ae74526fd3590c0251607463d0",
                "witness_address": "41d25855804e4e65de904faf3ac74b0bdfc53fac76",
                "parentHash": "0000000000d354ba4e12c69b9e76022dfbe2b170ec33499905615145a6772431",
                "version": 9,
                "timestamp": 1571795934000
            }
            },
            "transactions": [
            {
                "ret": [
                {
                    "contractRet": "SUCCESS"
                }
                ],
                "signature": [
                "096c70f3b73fce5d8bcac0a8e886e729d70f3e659040448da73980da5a0bdd4b25092f9348caac4dcb246a434e69a4bc263135b10328f2b1defe365486dcd4a500"
                ],
                "txID": "ebd1ce89f031964e1a0620e3d2d38cf76eb0949615643eac8ec3bb0e1bfdde22",
                "raw_data": {
                "contract": [
                    {
                    "parameter": {
                        "value": {
                        "data": "a3082be900000000000000000000000000000000000000000000000000000000000000310000000000000000000000000000000000000000000000000000000000000000",
                        "owner_address": "41e78f6df1d536b0bfb2c4a8d71dd7a892b65179f5",
                        "contract_address": "41e42d76d15b7ecd27a92cc9551738c2635c63b71c",
                        "call_value": 10000000
                        },
                        "type_url": "type.googleapis.com/protocol.TriggerSmartContract"
                    },
                    "type": "TriggerSmartContract"
                    }
                ],
                "ref_block_bytes": "54a7",
                "ref_block_hash": "d4037270a1694d6d",
                "expiration": 1571795988000,
                "fee_limit": 6000000,
                "timestamp": 1571795931057
                },
                "raw_data_hex": "0a0254a72208d4037270a1694d6d40a0dcddb2df2d5ab301081f12ae010a31747970652e676f6f676c65617069732e636f6d2f70726f746f636f6c2e54726967676572536d617274436f6e747261637412790a1541e78f6df1d536b0bfb2c4a8d71dd7a892b65179f5121541e42d76d15b7ecd27a92cc9551738c2635c63b71c1880ade2042244a3082be90000000000000000000000000000000000000000000000000000000000000031000000000000000000000000000000000000000000000000000000000000000070b19fdab2df2d9001809bee02"
            },
            {
                "ret": [
                {
                    "contractRet": "SUCCESS"
                }
                ],
                "signature": [
                "d96553310e242db28f0288223e29148a2260d19683325905a35cabc97ad5edfe3e4e57c8a4d3eaac4756f324b7d70be91166acf00751605d81e962294c82b2d600"
                ],
                "txID": "9e55e7d6e25da0458b9928ccff8ff3c988e1f8dd5a65e02c1da86d635af8632b",
                "raw_data": {
                "contract": [
                    {
                    "parameter": {
                        "value": {
                        "data": "cad9acb50000000000000000000000000000000000000000000000000000000000000060000000000000000000000000bd3ae7330b91e8fe0c2702db7fe38535c01edb09000000000000000000000000000000000000000000000000000000002ef7ed0000000000000000000000000000000000000000000000000000000000000000203135373137363731323138363430706959474f5a4a436f335134494233626430",
                        "owner_address": "410bb9d6a228547dd5056961dc6714975e0f9f4e69",
                        "contract_address": "4154458d3303622e755c3a5aa29b37e831941ffeff"
                        },
                        "type_url": "type.googleapis.com/protocol.TriggerSmartContract"
                    },
                    "type": "TriggerSmartContract"
                    }
                ],
                "ref_block_bytes": "54a7",
                "ref_block_hash": "d4037270a1694d6d",
                "expiration": 1571795988000,
                "fee_limit": 10000000,
                "timestamp": 1571795930660
                },
                "raw_data_hex": "0a0254a72208d4037270a1694d6d40a0dcddb2df2d5a9002081f128b020a31747970652e676f6f676c65617069732e636f6d2f70726f746f636f6c2e54726967676572536d617274436f6e747261637412d5010a15410bb9d6a228547dd5056961dc6714975e0f9f4e6912154154458d3303622e755c3a5aa29b37e831941ffeff22a401cad9acb50000000000000000000000000000000000000000000000000000000000000060000000000000000000000000bd3ae7330b91e8fe0c2702db7fe38535c01edb09000000000000000000000000000000000000000000000000000000002ef7ed0000000000000000000000000000000000000000000000000000000000000000203135373137363731323138363430706959474f5a4a436f33513449423362643070a49cdab2df2d900180ade204"
            }
            ]
        }
    }

queryTransactionByTxHash
```````````
通过ID(Hash)查询交易

定义::

    GET /trx/queryTransactionByTxHash?hash={hash}
    
请求示例::

    GET /trx/queryTransactionByTxHash?hash=92fb8d12daf58b30d1bb32b40549ea81484fca4f8b9f18f5f77888766b32d92b 

返回:

.. code-block:: json

   {
        "status": 0,
        "message": "success",
        "data": {
            "status": "confirmed",
            "ret": [
            {
                "contractRet": "SUCCESS"
            }
            ],
            "signature": [
            "4d167c45dfed989d9c51762d1378987b6cf229d5d2f9cca86d10df6f584f0a0c1127dca96a1b8adf7bda2551468958cbb16f43ea58b875179eb2e33adb730cb101"
            ],
            "txID": "aa9d1388ad95a4508fefa5455d749e224b9b8ec756198f65b76d0804dbd438f8",
            "raw_data": {
            "contract": [
                {
                "parameter": {
                    "value": {
                    "owner_address": "410583a68a3bcd86c25ab1bee482bac04a216b0261"
                    },
                    "type_url": "type.googleapis.com/protocol.TransferContract"
                },
                "type": "TransferContract"
                }
            ],
            "ref_block_bytes": "55fb",
            "ref_block_hash": "98eef46887044dfa",
            "expiration": 1571796954000,
            "timestamp": 1571796897478
            },
            "raw_data_hex": "0a0255fb220898eef46887044dfa4090d798b3df2d5a69080112650a2d747970652e676f6f676c65617069732e636f6d2f70726f746f636f6c2e5472616e73666572436f6e747261637412340a15410583a68a3bcd86c25ab1bee482bac04a216b02611215418ce5dcf6496a66b356bdefee325b33a42ff60b0e188889cad22370c69d95b3df2d"
        }
    }

queryTransactioninfoByHash
```````````
根据ID(Hash)查询交易的fee，所在的block

定义::

    GET /trx/queryTransactioninfoByHash?hash={hash}
    
请求示例::

    GET /trx/queryTransactioninfoByHash?hash=92fb8d12daf58b30d1bb32b40549ea81484fca4f8b9f18f5f77888766b32d92b 

返回:

.. code-block:: json

   {
        "status": 0,
        "message": "success",
        "data": {
            "id": "aa9d1388ad95a4508fefa5455d749e224b9b8ec756198f65b76d0804dbd438f8",
            "fee": 2690,
            "blockNumber": 13850109,
            "blockTimeStamp": 1571796900000,
            "contractResult": [
              "SUCCESS"
            ],
            "receipt": {
            "net_fee": 2690
            }
        }
    }

validateAddress
```````````
检查地址是否正确

定义::

    GET /trx/validateAddress?address={address}
    
请求示例::

    GET /trx/validateAddress?address=TAUN6FwrnwwmaEqYcckffC7wYmbaS6cBiX 

返回:

.. code-block:: json

   {
        "status": 0,
        "message": "success",
        "data": true
    }

getAccount
```````````
查询一个账号的信息

定义::

    GET /trx/getAccount?address={address}
    
请求示例::

    GET /trx/getAccount?address=TAUN6FwrnwwmaEqYcckffC7wYmbaS6cBiX 

返回:

.. code-block:: json

   {
        "status": 0,
        "message": "success",
        "data": {
            "address": "410583a68a3bcd86c25ab1bee482bac04a216b0261",
            "balance": 44373254448638,
            "create_time": 1530265827000,
            "latest_opration_time": 1571799060000,
            "free_net_usage": 4783,
            "latest_consume_free_time": 1571795661000,
            "account_resource": {
            "latest_consume_time_for_energy": 1571799060000
            },
            "assetV2": [
            {
                "key": "1000025",
                "value": 100000
            },
            {
                "key": "1000542",
                "value": 1552
            }
            ],
            "free_asset_net_usageV2": [
            {
                "key": "1000025",
                "value": 0
            },
            {
                "key": "1000542",
                "value": 0
            }
            ]
        }
    }

getAccountNet
```````````
查询账户的资源信息

定义::

    GET /trx/getAccountNet?address={address}
    
请求示例::

    GET /trx/getAccountNet?address=TAUN6FwrnwwmaEqYcckffC7wYmbaS6cBiX 

返回:

.. code-block:: json

   {
        "status": 0,
        "message": "success",
        "data": {
            "freeNetUsed": 4772,
            "freeNetLimit": 5000,
            "assetNetUsed": [
            {
                "key": "1000025",
                "value": 0
            },
            {
                "key": "1000542",
                "value": 0
            }
            ],
            "TotalNetLimit": 43200000000,
            "TotalNetWeight": 20303370221
        }
    }

getAssetIssueById
```````````
根据id查询token信息

定义::

    GET /trx/getAssetIssueById?id={id}
    
请求示例::

    GET /trx/getAssetIssueById?id=1000025 

返回:

.. code-block:: json

   {
        "status": 0,
        "message": "success",
        "data": {
            "owner_address": "41375c15b10f9b2bb01a62522201629b29704f8e62",
            "name": "65546f6c6172",
            "abbr": "45544c",
            "total_supply": 8000000000,
            "trx_num": 1000000,
            "num": 10000000,
            "start_time": 1531058283000,
            "end_time": 1538315940000,
            "description": "65546f6c6172202d206e65772067656e65726174696f6e20746f6b656e20666f7220736f6369616c206d6564696120776865726520656e746875736961737473206265636f6d652070726f66657373696f6e616c732e204f6e652068696e743a20536f6369616c206d65646961206561726e202434302042696c6c696f6e2066726f6d2061647665727469736572732e2049434f20737461727473204a756c792031362c20323031382e",
            "url": "687474703a2f2f7777772e65546f6c61722e6f7267",
            "id": "1000025"
        }
    }
