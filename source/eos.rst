EOS API Docs
===========

get_info
`````````````````
调用返回区块链总体信息。

定义::

    GET /eos/get_info
    
请求示例::

    GET /eos/get_info

返回:

.. code-block:: json

  {
    "status": 0,
    "message": "success",
    "data": {
      "netCpuLimit": "1048576",
      "server_version": "greymass-v1.8.4-hl-dirty",
      "chain_id": "aca376f206b8fc25a6ed44dbdc66547c36c6c33e3a119ffbeaef943642f0e906",
      "head_block_num": "86883544",
      "last_irreversible_block_num": "86883208",
      "last_irreversible_block_id": "052dbb8890d3f7bd23a49645cbc893da2af07f254fdb3a817a8b70696c2d2040",
      "head_block_id": "052dbcd891f8ca9ced365ff7eeebec01154f54709519bfa8d47db46c3a668036",
      "head_block_time": "2019-10-28T07:35:41.500",
      "head_block_producer": "eoshuobipool",
      "virtual_block_cpu_limit": "3258136",
      "virtual_block_net_limit": "1048576000",
      "block_cpu_limit": "200000"
    }
  }

get_block
`````````````````
调用返回指定区块的详细数据。

定义::

    GET /eos/get_block?block_num_or_id={block_num_or_id}
    
请求示例::

    GET /eos/get_block?block_num_or_id=1

返回:

.. code-block:: json

  {
    "status": 0,
    "message": "success",
    "data": {
      "confirmed": true,
      "transactions": [],
      "previous": "0000000000000000000000000000000000000000000000000000000000000000",
      "timestamp": "2018-06-08T08:08:08.500",
      "transaction_mroot": "0000000000000000000000000000000000000000000000000000000000000000",
      "action_mroot": "aca376f206b8fc25a6ed44dbdc66547c36c6c33e3a119ffbeaef943642f0e906",
      "block_mroot": null,
      "producer": "",
      "schedule_version": "0",
      "new_producers": null,
      "producer_signature": "SIG_K1_111111111111111111111111111111111111111111111111111111111111111116uk5ne",
      "id": "00000001405147477ab2f5f51cda427b638191c66d2c59aa392d5c2c98076cb0",
      "block_num": 1,
      "ref_block_prefix": 4126519930,
      "header_extensions": [],
      "block_extensions": []
    }
  }

get_account
`````````````````
调用返回指定账号的描述信息。

定义::

    GET /eos/get_account?account_name={account_name}
    
请求示例::

    GET /eos/get_account?account_name=binancecold1

返回:

.. code-block:: json

  {
    "status": 0,
    "message": "success",
    "data": {
      "account_name": "binancecold1",
      "head_block_num": 86885749,
      "head_block_time": "2019-10-28T07:54:04.500",
      "privileged": false,
      "last_code_update": "1970-01-01T00:00:00.000",
      "created": "2018-11-14T06:58:00.000",
      "core_liquid_balance": "36701484.9626 EOS",
      "ram_quota": 20683,
      "net_weight": 10000000500,
      "cpu_weight": 10000001500,
      "net_limit": {
        "used": 129,
        "available": 762598416469,
        "max": 762598416598
      },
      "cpu_limit": {
        "used": 358,
        "available": 3181931201,
        "max": 3181931559
      },
      "ram_usage": 3686,
      "total_resources": {
        "owner": "binancecold1",
        "net_weight": "1000000.0500 EOS",
        "cpu_weight": "1000000.1500 EOS",
        "ram_bytes": 19283
      },
      "permissions": [
        {
          "name": null,
          "parent": "owner",
          "perm_name": "active",
          "required_auth": {
            "accounts": [],
            "keys": [
              {
                "key": "EOS5GZ7R4BsApfxKcSbHeBEeFavsu9b75ooXM6pf5fo5G4ZbSWBMX",
                "weight": 1
              }
            ],
            "threshold": "1",
            "waits": []
          }
        },
        {
          "name": null,
          "parent": "",
          "perm_name": "owner",
          "required_auth": {
            "accounts": [],
            "keys": [
              {
                "key": "EOS5GZ7R4BsApfxKcSbHeBEeFavsu9b75ooXM6pf5fo5G4ZbSWBMX",
                "weight": 1
              }
            ],
            "threshold": "1",
            "waits": []
          }
        }
      ]
    }
  }

get_transaction
`````````````````
调用返回指定的交易数据。

定义::

    GET /eos/get_transaction?id={id}
    
请求示例::

    GET /eos/get_transaction?id=4B26B91CDF86777655D50129772472D211ACD752508036843FB52AC028B2CB1C

返回:

.. code-block:: json

  {
    "status": 0,
    "message": "success",
    "data": {
      "status": null,
      "id": "4b26b91cdf86777655d50129772472d211acd752508036843fb52ac028b2cb1c",
      "trx": {
        "receipt": {
          "status": "executed",
          "cpu_usage_us": 291,
          "net_usage_words": 25,
          "trx": [
            1,
            {
              "signatures": [
                "SIG_K1_KdhEauhS3aHNZMGr4koAYpNCQjF9ZAobA5wJn7bDx7K3vyRqXVVBxvSiMb3jNVcmVGHB7V1WHMVyLx2vYGBNEBMqdxoWdB"
              ],
              "compression": "none",
              "packed_context_free_data": "",
              "packed_trx": "a69eb65dc7c364bc856a0000000001a09866fd489c8665000000572d3ccdcd01c068f4924d97cccd00000000a8ed323266c068f4924d97cccd1052a448a169a63b010000000000000004494e4445580000454254433e454f533e4554483e555344542c312e30363036314254432c31303031302e3831353839555344542c323937392e3233393735454f532c35342e363939383845544800"
            }
          ]
        },
        "trx": {
          "expiration": "2019-10-28T07:54:14",
          "ref_block_num": 50119,
          "ref_block_prefix": 1787149412,
          "max_net_usage_words": 0,
          "max_cpu_usage_ms": 0,
          "delay_sec": 0,
          "context_free_actions": [],
          "actions": [
            {
              "account": "gq3dsmbxguge",
              "name": "transfer",
              "authorization": [
                {
                  "actor": "tradingmylog",
                  "permission": "active"
                }
              ],
              "data": {
                "from": "tradingmylog",
                "to": "binancecold1",
                "quantity": "0.0001 INDEX",
                "memo": "BTC>EOS>ETH>USDT,1.06061BTC,10010.81589USDT,2979.23975EOS,54.69988ETH"
              },
              "hex_data": "c068f4924d97cccd1052a448a169a63b010000000000000004494e4445580000454254433e454f533e4554483e555344542c312e30363036314254432c31303031302e3831353839555344542c323937392e3233393735454f532c35342e3639393838455448"
            }
          ],
          "transaction_extensions": [],
          "signatures": [
            "SIG_K1_KdhEauhS3aHNZMGr4koAYpNCQjF9ZAobA5wJn7bDx7K3vyRqXVVBxvSiMb3jNVcmVGHB7V1WHMVyLx2vYGBNEBMqdxoWdB"
          ],
          "context_free_data": []
        }
      },
      "block_time": "2019-10-28T07:53:15.500",
      "block_num": 86885651,
      "last_irreversible_block": 86885679,
      "traces": [
        {
          "act": {
            "account": "gq3dsmbxguge",
            "authorization": [
              {
                "actor": "tradingmylog",
                "permission": "active"
              }
            ],
            "data": {
              "from": "tradingmylog",
              "to": "binancecold1",
              "quantity": "0.0001 INDEX",
              "memo": "BTC>EOS>ETH>USDT,1.06061BTC,10010.81589USDT,2979.23975EOS,54.69988ETH"
            },
            "hex_data": "c068f4924d97cccd1052a448a169a63b010000000000000004494e4445580000454254433e454f533e4554483e555344542c312e30363036314254432c31303031302e3831353839555344542c323937392e3233393735454f532c35342e3639393838455448",
            "name": "transfer"
          },
          "console": "",
          "cpu_usage": null,
          "elapsed": 292,
          "inline_traces": null,
          "receipt": {
            "abi_sequence": 21,
            "act_digest": "a2af6b88e98b204a049288d9b32c36ff963d7d71ed38842111c91ae6ae49eb72",
            "auth_sequence": [
              [
                "tradingmylog",
                "363888"
              ]
            ],
            "code_sequence": 1,
            "global_sequence": 9733904895,
            "receiver": "gq3dsmbxguge",
            "recv_sequence": 122612
          },
          "total_cpu_usage": null,
          "trx_id": "4b26b91cdf86777655d50129772472d211acd752508036843fb52ac028b2cb1c",
          "context_free": false,
          "block_num": 86885651,
          "block_time": "2019-10-28T07:53:15.500",
          "producer_block_id": "052dc51333605af21721d34c2bb71293a99741df3a0cfc588404c77035e45478",
          "account_ram_deltas": [],
          "trx_status": null,
          "createdAt": null
        },
        {
          "act": {
            "account": "gq3dsmbxguge",
            "authorization": [
              {
                "actor": "tradingmylog",
                "permission": "active"
              }
            ],
            "data": {
              "from": "tradingmylog",
              "to": "binancecold1",
              "quantity": "0.0001 INDEX",
              "memo": "BTC>EOS>ETH>USDT,1.06061BTC,10010.81589USDT,2979.23975EOS,54.69988ETH"
            },
            "hex_data": "c068f4924d97cccd1052a448a169a63b010000000000000004494e4445580000454254433e454f533e4554483e555344542c312e30363036314254432c31303031302e3831353839555344542c323937392e3233393735454f532c35342e3639393838455448",
            "name": "transfer"
          },
          "console": "",
          "cpu_usage": null,
          "elapsed": 6,
          "inline_traces": null,
          "receipt": {
            "abi_sequence": 21,
            "act_digest": "a2af6b88e98b204a049288d9b32c36ff963d7d71ed38842111c91ae6ae49eb72",
            "auth_sequence": [
              [
                "tradingmylog",
                "363889"
              ]
            ],
            "code_sequence": 1,
            "global_sequence": 9733904896,
            "receiver": "tradingmylog",
            "recv_sequence": 121298
          },
          "total_cpu_usage": null,
          "trx_id": "4b26b91cdf86777655d50129772472d211acd752508036843fb52ac028b2cb1c",
          "context_free": false,
          "block_num": 86885651,
          "block_time": "2019-10-28T07:53:15.500",
          "producer_block_id": "052dc51333605af21721d34c2bb71293a99741df3a0cfc588404c77035e45478",
          "account_ram_deltas": [],
          "trx_status": null,
          "createdAt": null
        },
        {
          "act": {
            "account": "gq3dsmbxguge",
            "authorization": [
              {
                "actor": "tradingmylog",
                "permission": "active"
              }
            ],
            "data": {
              "from": "tradingmylog",
              "to": "binancecold1",
              "quantity": "0.0001 INDEX",
              "memo": "BTC>EOS>ETH>USDT,1.06061BTC,10010.81589USDT,2979.23975EOS,54.69988ETH"
            },
            "hex_data": "c068f4924d97cccd1052a448a169a63b010000000000000004494e4445580000454254433e454f533e4554483e555344542c312e30363036314254432c31303031302e3831353839555344542c323937392e3233393735454f532c35342e3639393838455448",
            "name": "transfer"
          },
          "console": "",
          "cpu_usage": null,
          "elapsed": 10,
          "inline_traces": null,
          "receipt": {
            "abi_sequence": 21,
            "act_digest": "a2af6b88e98b204a049288d9b32c36ff963d7d71ed38842111c91ae6ae49eb72",
            "auth_sequence": [
              [
                "tradingmylog",
                "363890"
              ]
            ],
            "code_sequence": 1,
            "global_sequence": 9733904897,
            "receiver": "binancecold1",
            "recv_sequence": 12648
          },
          "total_cpu_usage": null,
          "trx_id": "4b26b91cdf86777655d50129772472d211acd752508036843fb52ac028b2cb1c",
          "context_free": false,
          "block_num": 86885651,
          "block_time": "2019-10-28T07:53:15.500",
          "producer_block_id": "052dc51333605af21721d34c2bb71293a99741df3a0cfc588404c77035e45478",
          "account_ram_deltas": [],
          "trx_status": null,
          "createdAt": null
        }
      ],
      "cpu_usage_us": null,
      "net_usage_words": null
    }
  }

get_currency_balance
`````````````````
调用返回指定账户的代币余额信息。

定义::

    GET /eos/get_currency_balance?code={code}&account_name={account_name}&symbol={symbol}
    
请求示例::

    GET /eos/get_currency_balance?code=eosio.token&account_name=binancecold1&symbol=EOS

返回:

.. code-block:: json

  {
    "status": 0,
    "message": "success",
    "data": [
      "2.9626 EOS"
    ]
  }

hasContract
`````````````````
检测地址是否是合约账户

定义::

    GET /eos/hasContract?address={address}
    
请求示例::

    GET /eos/hasContract?address=test11111111

返回:

.. code-block:: json

  {
    "status": 0,
    "message": "success",
    "data": false
  }

eosSign
`````````````````
使用传入的秘钥对数据进行签名

定义::

    GET /eos/eosSign?data={data}&privateKey={privateKey}
    
请求示例::

    GET /eos/eosSign?data=123123123123123&privateKey=5J3yf2qU69i2CX8JQaPwM5PtvJ41bB1Dc7rRqFafzxjrW2wxvV6

返回:

.. code-block:: json

  {
    "status": 0,
    "message": "success",
    "data": "SIG_K1_K9NP9aggyTJexCvr6Jz3bDvPC1kjyLb9AhU79nP4XLqHdX9Ep7xfZFNEMCj1y1DU8z3qqQUmRUkeYErXmhHN9bNNTpS5of"
  }

eosVerifySign
`````````````````
使用公钥对已经签名的数据进行验证

定义::

    GET /eos/eosVerifySign?data={data}&signature={signature}&publicKey={publicKey}
    
请求示例::

    GET /eos/eosVerifySign?data=123123123123123&signature=SIG_K1_K9NP9aggyTJexCvr6Jz3bDvPC1kjyLb9AhU79nP4XLqHdX9Ep7xfZFNEMCj1y1DU8z3qqQUmRUkeYErXmhHN9bNNTpS5of&publicKey=EOS8Q84bT1Luyk32z6NKrnpjwstN9DKmNvo8gt9om4X15Ky2p2Bik

返回:

.. code-block:: json

  {
    "status": 0,
    "message": "success",
    "data": true
  }