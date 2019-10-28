Cardano API Docs
===========
validateAddress
```````````
Verifies that the address is a correct ADA address

定义::

    GET /ada/validateAddress?address={adderess}
    
请求示例::

    GET /ada/validateAddress?address=12312312312

返回:

.. code-block:: json

   {
        "status": 0,
        "message": "success",
        "data": false
    }

getAddressInfo
```````````
Get summary information about an address.

定义::

    GET /ada/getAddressInfo?address={adderess}
    
请求示例::

    GET /ada/getAddressInfo?address=DdzFFzCqrhsvB8v761AotebjeczMDkBEqk5p8u7jvoyxgdMdnem7qS58A2vtoU66uHCmFa1QbXCoQ5yDp5mCsnmJ3qUYPvrSw4LNrs2i

返回:

.. code-block:: json

   {
        "status": 0,
        "message": "success",
        "data": {
            "caAddress": "DdzFFzCqrhsvB8v761AotebjeczMDkBEqk5p8u7jvoyxgdMdnem7qS58A2vtoU66uHCmFa1QbXCoQ5yDp5mCsnmJ3qUYPvrSw4LNrs2i",
            "caType": "CPubKeyAddress",
            "caTxNum": 2,
            "caBalance": {
            "getCoin": "0"
            },
            "caTxList": [
            {
                "inputs": [
                {
                    "address": "DdzFFzCqrhsvB8v761AotebjeczMDkBEqk5p8u7jvoyxgdMdnem7qS58A2vtoU66uHCmFa1QbXCoQ5yDp5mCsnmJ3qUYPvrSw4LNrs2i",
                    "amount": 88988.637231
                }
                ],
                "outputs": [
                {
                    "address": "DdzFFzCqrhsoZZ3Nmzrs7saK1wyBWHcjeJk6HgxuckWMRZcfVjrHaX3V8dTf2szJuS1CE8n3KbBC3jJrDMtBu6K1SdWWKJ9nCRX6QDej",
                    "amount": 43648
                }
                ],
                "inputSum": 88988.637231,
                "outputSum": 88988.464798,
                "ctbId": "bf4b6f68e8eb0264b78e44efb567228f0d869de8a6f1326cd14614d3977b336a",
                "ctbTimeIssued": 1571800431,
                "ctbInputs": [
                [
                    "DdzFFzCqrhsvB8v761AotebjeczMDkBEqk5p8u7jvoyxgdMdnem7qS58A2vtoU66uHCmFa1QbXCoQ5yDp5mCsnmJ3qUYPvrSw4LNrs2i",
                    {
                    "getCoin": "88988637231"
                    }
                ]
                ],
                "ctbOutputs": [
                [
                    "DdzFFzCqrhsoZZ3Nmzrs7saK1wyBWHcjeJk6HgxuckWMRZcfVjrHaX3V8dTf2szJuS1CE8n3KbBC3jJrDMtBu6K1SdWWKJ9nCRX6QDej",
                    {
                    "getCoin": "43648000000"
                    }
                ]
                ],
                "ctbInputSum": {
                "getCoin": "88988637231"
                },
                "ctbOutputSum": {
                "getCoin": "88988464798"
                }
            }
            ]
        }
    }

getBlockByHash
```````````
Get block's summary information by HASH.

定义::

    GET /ada/getBlockByHash?hash={hash}
    
请求示例::

    GET /ada/getBlockByHash?hash=a50f856c4ac7a3955bccc3b08cfb8ba8c82883b4264d430b75eeb21395ff47d4

返回:

.. code-block:: json

   {
        "status": 0,
        "message": "success",
        "data": {
            "cbsEntry": {
            "totalSend": 0,
            "fees": 0,
            "cbeEpoch": 151,
            "cbeSlot": 9,
            "cbeBlkHeight": 3260070,
            "cbeBlkHash": "a50f856c4ac7a3955bccc3b08cfb8ba8c82883b4264d430b75eeb21395ff47d4",
            "cbeTimeIssued": 1571435271,
            "cbeTxNum": 0,
            "cbeTotalSent": {
                "getCoin": "0"
            },
            "cbeSize": 670,
            "cbeBlockLead": "af2800c124e599d6dec188a75f8bfde397ebb778163a18240371f2d1",
            "cbeFees": {
                "getCoin": "0"
            }
            },
            "cbsPrevHash": "2dc60d1feb3ebe08fa770115a4336be7ce53b2f0f9341024cbdc364a177f8d03",
            "cbsNextHash": "92b981a87db51dbdb7cf3718f0a23f89922993badaaecdea07123bcc4e0e35fd",
            "cbsMerkleRoot": "0e5751c026e543b2e8ab2eb06099daa1d1e5df47778f7787faab45cdf12fe3a8"
        }
    }

getBlockByEpochAndSlot
```````````
Get block's summary information by epoch and slot.

定义::

    GET /ada/getBlockByEpochAndSlot?epoch={epoch}&slot={slot}
    
请求示例::

    GET /ada/getBlockByEpochAndSlot?epoch=151&slot=9

返回:

.. code-block:: json

   {
        "status": 0,
        "message": "success",
        "data": [
            {
            "totalSend": 0,
            "fees": 0,
            "cbeEpoch": 151,
            "cbeSlot": 9,
            "cbeBlkHeight": 3260070,
            "cbeBlkHash": "a50f856c4ac7a3955bccc3b08cfb8ba8c82883b4264d430b75eeb21395ff47d4",
            "cbeTimeIssued": 1571435271,
            "cbeTxNum": 0,
            "cbeTotalSent": {
                "getCoin": "0"
            },
            "cbeSize": 670,
            "cbeBlockLead": "af2800c124e599d6dec188a75f8bfde397ebb778163a18240371f2d1",
            "cbeFees": {
                "getCoin": "0"
            }
            }
        ]
    }

getBlockTxsByHash
```````````
Get block's brief information about transactions.

定义::

    GET /ada/getBlockTxsByHash?hash={hash}

请求示例::

    GET /ada/getBlockTxsByHash?hash=48ade3faf23f887c67d7277e5430122b86844f3308bb35dd44a3898500da0e78

返回:

.. code-block:: json

   {
        "status": 0,
        "message": "success",
        "data": [
            {
            "inputs": [
                {
                "address": "DdzFFzCqrhsruKX97Vm7WxzS5DRw2Dnwxn3ZyxpsfhPWK8ieeTo9KBRwFuMByZdpHLr9dCvqnnbrADGhdjShsNrxkC7JNGD5MJG8q1s7",
                "amount": 1000
                }
            ],
            "outputs": [
                {
                "address": "DdzFFzCqrht44o9pshsCmnmQ7CEgFm9uhqoQzJHsmE9wHopMcThez91cAf7WCMY7C9qMYRBdVkdFY4ttqXBCrTorGdGrhk3az2LnK4Ts",
                "amount": 476.275229
                },
                {
                "address": "DdzFFzCqrhstphy8cETDW9wvPJ4dAoBKHZ9jSrxkDvYzCFHDDYCKHC2yjfcpqKUe2yTintwRTYvK8zZApbUvcvMeX5dfoC8SRZh3XrD8",
                "amount": 523.55269
                }
            ],
            "inputSum": 1000,
            "outputSum": 999.827919,
            "ctbId": "3b7affecdae60c6a4ec96439d68c709c55871424c1aa94edc9dc25a95bb0bd9a",
            "ctbTimeIssued": 1571435091,
            "ctbInputs": [
                [
                "DdzFFzCqrhsruKX97Vm7WxzS5DRw2Dnwxn3ZyxpsfhPWK8ieeTo9KBRwFuMByZdpHLr9dCvqnnbrADGhdjShsNrxkC7JNGD5MJG8q1s7",
                {
                    "getCoin": "1000000000"
                }
                ]
            ],
            "ctbOutputs": [
                [
                "DdzFFzCqrht44o9pshsCmnmQ7CEgFm9uhqoQzJHsmE9wHopMcThez91cAf7WCMY7C9qMYRBdVkdFY4ttqXBCrTorGdGrhk3az2LnK4Ts",
                {
                    "getCoin": "476275229"
                }
                ],
                [
                "DdzFFzCqrhstphy8cETDW9wvPJ4dAoBKHZ9jSrxkDvYzCFHDDYCKHC2yjfcpqKUe2yTintwRTYvK8zZApbUvcvMeX5dfoC8SRZh3XrD8",
                {
                    "getCoin": "523552690"
                }
                ]
            ],
            "ctbInputSum": {
                "getCoin": "1000000000"
            },
            "ctbOutputSum": {
                "getCoin": "999827919"
            }
            },
            {
            "inputs": [
                {
                "address": "DdzFFzCqrht2caAG7wF3DEfHEQd8y4Vutv8E3AxKQYgf1XeSzWNMzf5EC8ssiTuyrkNJ9URSvZxK3Gq4cYgJ82SwPUE63cARsnnNqrai",
                "amount": 400000
                },
                {
                "address": "DdzFFzCqrhssUiC44EBAwFu8ThnF2sz32zsL4KKyK36ba2hVVYmepTJvX2c2HScNWM8PqAtSyd5CQPQei4mhArv3ETBWz597uehQcDC3",
                "amount": 2
                },
                {
                "address": "DdzFFzCqrhtCLtKQASqhP1WD2zZ4gLjxFnbh5tw4dQ3pm4cy2wxMUG5gv4XN92rAnLGrZQVEQFecX2ksuhu89VT854RTU2tA5vtCGCou",
                "amount": 298.7
                }
            ],
            "outputs": [
                {
                "address": "DdzFFzCqrht5ieFWEyAcULVTfr8YPdgoMiGReHT2xH3N3GZHpcPYVTZZCeEEH33ARTqotTzVLyixuF2QAYpjTSd8UDNhvihFRvCtXZz7",
                "amount": 295056.205187
                },
                {
                "address": "DdzFFzCqrhtAfDZtxCsQqnuanAfPHaNxZG4KgbbZJ7FEfydMWGdXcVuWQjwUYT7X7UoXakDiHXHohfG9gnmpRnEtxGivmtMgnSPUdWqx",
                "amount": 105244.30612
                }
            ],
            "inputSum": 400300.7,
            "outputSum": 400300.511307,
            "ctbId": "77bae5a06b96ea81fd3beb59022092aaea0f7535709987dcc2114109a2bc0446",
            "ctbTimeIssued": 1571435091,
            "ctbInputs": [
                [
                "DdzFFzCqrht2caAG7wF3DEfHEQd8y4Vutv8E3AxKQYgf1XeSzWNMzf5EC8ssiTuyrkNJ9URSvZxK3Gq4cYgJ82SwPUE63cARsnnNqrai",
                {
                    "getCoin": "400000000000"
                }
                ],
                [
                "DdzFFzCqrhssUiC44EBAwFu8ThnF2sz32zsL4KKyK36ba2hVVYmepTJvX2c2HScNWM8PqAtSyd5CQPQei4mhArv3ETBWz597uehQcDC3",
                {
                    "getCoin": "2000000"
                }
                ],
                [
                "DdzFFzCqrhtCLtKQASqhP1WD2zZ4gLjxFnbh5tw4dQ3pm4cy2wxMUG5gv4XN92rAnLGrZQVEQFecX2ksuhu89VT854RTU2tA5vtCGCou",
                {
                    "getCoin": "298700000"
                }
                ]
            ],
            "ctbOutputs": [
                [
                "DdzFFzCqrht5ieFWEyAcULVTfr8YPdgoMiGReHT2xH3N3GZHpcPYVTZZCeEEH33ARTqotTzVLyixuF2QAYpjTSd8UDNhvihFRvCtXZz7",
                {
                    "getCoin": "295056205187"
                }
                ],
                [
                "DdzFFzCqrhtAfDZtxCsQqnuanAfPHaNxZG4KgbbZJ7FEfydMWGdXcVuWQjwUYT7X7UoXakDiHXHohfG9gnmpRnEtxGivmtMgnSPUdWqx",
                {
                    "getCoin": "105244306120"
                }
                ]
            ],
            "ctbInputSum": {
                "getCoin": "400300700000"
            },
            "ctbOutputSum": {
                "getCoin": "400300511307"
            }
            }
        ]
    }

getLastTransactions
```````````
Get information about the N latest transactions.

定义::

    GET /ada/getLastTransactions

请求示例::

    GET /ada/getLastTransactions

返回:

.. code-block:: json

   {
        "status": 0,
        "message": "success",
        "data": [
            {
                "amount": 750750.747525,
                "cteId": "35f8770e76ad7f243a3440eaefe7826737383ef8c8326e2f97a9b1379fac4cf2",
                "cteTimeIssued": 1571801191,
                "cteAmount": {
                "getCoin": "750750747525"
                }
            },
            {
                "amount": 18958.131096,
                "cteId": "5ae4577f80614b9b23d8d1003b83a86e610b9c71730ada776a791c8b3b91a972",
                "cteTimeIssued": 1571800751,
                "cteAmount": {
                "getCoin": "18958131096"
                }
            },
            {
                "amount": 3506.749836,
                "cteId": "688744786a8878dce91c8005fbed9b01bcf1d82e15f59ff073c19b318732e4da",
                "cteTimeIssued": 1571800591,
                "cteAmount": {
                "getCoin": "3506749836"
                }
            },
            {
                "amount": 83453.756236,
                "cteId": "c85da1bd8ea5403c037859601d0eff3fb7c4fb62e55dc7e540d848048fc4fb18",
                "cteTimeIssued": 1571799031,
                "cteAmount": {
                "getCoin": "83453756236"
                }
            }
        ]
    }

queryTransactionByTxHash
```````````
Query transaction based on hash

定义::

    GET /ada/queryTransactionByTxHash?hash={hash}

请求示例::

    GET /ada/queryTransactionByTxHash?hash=

返回:

.. code-block:: json

   {
        "status": 0,
        "message": "success",
        "data": {
            "totalInput": 999.827919,
            "totalOutput": 999.827919,
            "fee": 0.172081,
            "inputs": [
                {
                    "address": "DdzFFzCqrhsruKX97Vm7WxzS5DRw2Dnwxn3ZyxpsfhPWK8ieeTo9KBRwFuMByZdpHLr9dCvqnnbrADGhdjShsNrxkC7JNGD5MJG8q1s7",
                    "amount": 1000
                }
            ],
            "outputs": [
                {
                    "address": "DdzFFzCqrht44o9pshsCmnmQ7CEgFm9uhqoQzJHsmE9wHopMcThez91cAf7WCMY7C9qMYRBdVkdFY4ttqXBCrTorGdGrhk3az2LnK4Ts",
                    "amount": 476.275229
                },
                {
                    "address": "DdzFFzCqrhstphy8cETDW9wvPJ4dAoBKHZ9jSrxkDvYzCFHDDYCKHC2yjfcpqKUe2yTintwRTYvK8zZApbUvcvMeX5dfoC8SRZh3XrD8",
                    "amount": 523.55269
                }
            ],
            "ctsId": "3b7affecdae60c6a4ec96439d68c709c55871424c1aa94edc9dc25a95bb0bd9a",
            "ctsTxTimeIssued": 1571435091,
            "ctsBlockTimeIssued": 1571435091,
            "ctsBlockHeight": 3260061,
            "ctsBlockEpoch": 151,
            "ctsBlockSlot": 0,
            "ctsBlockHash": "48ade3faf23f887c67d7277e5430122b86844f3308bb35dd44a3898500da0e78",
            "ctsTotalInput": {
            "getCoin": "1000000000"
            },
            "ctsTotalOutput": {
            "getCoin": "999827919"
            },
            "ctsFees": {
            "getCoin": "172081"
            },
            "ctsInputs": [
                [
                    "DdzFFzCqrhsruKX97Vm7WxzS5DRw2Dnwxn3ZyxpsfhPWK8ieeTo9KBRwFuMByZdpHLr9dCvqnnbrADGhdjShsNrxkC7JNGD5MJG8q1s7",
                    {
                    "getCoin": "1000000000"
                    }
                ]
                ],
            "ctsOutputs": [
                [
                    "DdzFFzCqrht44o9pshsCmnmQ7CEgFm9uhqoQzJHsmE9wHopMcThez91cAf7WCMY7C9qMYRBdVkdFY4ttqXBCrTorGdGrhk3az2LnK4Ts",
                    {
                    "getCoin": "476275229"
                    }
                ],
                [
                    "DdzFFzCqrhstphy8cETDW9wvPJ4dAoBKHZ9jSrxkDvYzCFHDDYCKHC2yjfcpqKUe2yTintwRTYvK8zZApbUvcvMeX5dfoC8SRZh3XrD8",
                    {
                    "getCoin": "523552690"
                    }
                ]
            ]
        }
    }