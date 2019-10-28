Zcash API Docs
===========
Zcash is a privacy-protecting, digital currency built on strong science. `Official website`_.

.. _Official website: https://z.cash/


getbestblockhash
`````````````````
Returns the hash of the best (tip) block in the longest block chain.

Definition::

    GET /zec/getbestblockhash/
    
Example Request::

    GET /zec/getbestblockhash/

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": "00000000003049e7ed2ecff4de3819f2fa3dd53cde6983f8775ead5c0b4bf2d8" // (string) the block hash hex encoded
    }

getBlockByBlockHeight
``````````````````````
getblock "height"

Definition::

    GET /zec/getBlockByBlockHeight?height=12800
    
Example Request::

    GET /zec/getBlockByBlockHeight?height=12800

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": {
            "m": {
            "hash": "00000000febc373a1da2bd9f887b105ad79ddc26ac26c2b28652d64e5207c5b5",
            "confirmations": 612213,
            "size": 748771,
            "height": 12800,
            "version": 4,
            "merkleroot": "a2725bef50de57c71ede8d15f769ea5272ab7ad56bdb94ca8a73b12a469e7632",
            "finalsaplingroot": "0000000000000000000000000000000000000000000000000000000000000000",
            "tx": [
                "008440c3cec370670be6a83f6ff7f2518eb47de9257373f31b1e9640ae9e6986",
                "f1d6098b1b076a8f0b5036126bea8bf32eabc42453007ccd89814bb5030e2f59",
                "c94f6dfcfe60acf27c2dde44a8b38694896a6674b5dcf255c63b54ba8162cdc9",
                "2a438db7e3f95f9c74fa691a04763ecc34cf66383ffd8356ed0d405582083eb9",
                "bb4110cb9718f939a260a39826849300942151fb3c9f16e09cffe5a79b0e20fb",
                "c0ea223eeb4024de5fb3e94bb4be927221d17b5b3df6fce12ed43ec3d4fe7493",
                "4d9d4b1a133f5d3abb88a461f0fa669e0aa088b2d93235c3040bc776a6ab8fd9",
                "487f4ceece179a753cc6ba8136e19b2869e0602dda99d5f300e7a8ac58b45f27",
                "cc9095719f7bad03c64afa29e52b32487e2003952e0fb1bcec4273a11ab82a78",
                "2363a19c4b57636d14fc9ad8bc6b2c2609f309ff4b895b21ea6ee7c0908ab2d2",
                "b6819292057f8aa0f2bd1716fbecf53b3d2a591a3ca55b164468e26b26e86fc3",
                "d782054e50408745927b3fef8b813701e76d9c3af79e5ce49be16c112b93a23d",
                "0d8332217aefdfd34a594b28dea40e92be4682fc4d4f331124e6b3930d690379",
                "d85246dad6d0addc4a7ecac125d89a6586857f917fc59c896d8b257dfd7db447",
                "748271801ffc8296f69319f2f4b447774bfbefcad447bb91735433c115c0ad0a",
                "074d91d4c1dec867583fb661ab997e1f4e52a995ae9b97e6afa37ed1e39c8780",
                "3edef316394815b6608afed481c214497f78f93ba4aa3722a1c986c45d4557e6",
                "1d6fb748d2169149ffc61750eb0ddcdfe31ab7bede16b892a1968f701abc6bb0",
                "9d9080562542ce92d6df2c52a580a008f73e73d32ea7c0b389b6b4f8b8b0d36b",
                "51201e1867e8476e8a89c36b13bc07ae587aa00fd1b6d011e0c93d7bbc9995ea",
                "67b166ea599c253eff45edda8e6d73943c1db165bc72516dca9286ab1c354656",
                "2d73db2f76b7a6590f131d9b31f78e453904f352dc9605274f163402fa11091b",
                "92ec55dc7220c0d036383847c79d597b15e1aa18664fa5e995d16642c7733d5d",
                "4577bb320dfe33aa96814c5932f5d1dde847ef5bff2e63e261b463996b86beb3",
                "fc5ccfbfaa901bdf28c4673f3a6dab4e27fbda310676055ac1ba4a2b639468f4"
            ],
            "time": 1479519154,
            "nonce": "0000000000000000000000000000000000000000000000000014117519b7c6db",
            "solution": "0076568fbc8ac5c33d60148fc74c28a19becd044e850593f470862db3dc582d54e13ce679b0a9a5aacc0014d8e917b9f5f1fb235028e90ab9245952a96eb8f339f6dc70bf28139d9e20853b05c2c16e53439f9140354ba7dffca181b20bb31986763f3813609501a3005e42351f122bb9ddbf3a0b0ad05fa186be54ebf951fe432d63faa01cf6ccbb20ffb650c024a4456130340713bbabcd5b9dd35f7c76e5dfb7af5ed70d2552802db77648812d9f2ff58d1c99dc348122605dcf25d06943a730162c3194fab435e402f7dc5d6e2354d6a1dca0ec7b708f444dfe31b5b815c77c382443c3d4e6cadb3f5eee1b829d36019388ce712a6d8d5b858b3137efa12040d5937dbef6665e373604e331c3cec891aedbafd0451162debfff1c25ae37cb8a1daf1d7ce17acc7068998301d614572150eba0b6974ef105bec20a89e6ec94b846b010ab36f88deb9591ff979f3e905689094be513fc509f4121dd4fbddce669b38a8950833addd359b48551b2a816918aad66ce6e039e45906e70af93953c3e9bb9142a02ce63bfd34837c32c0191013dd4bc7f1cff41594ccdab9ce495100dbf1b8143594182f544acafa3a2756085215d63b4a9e6d1d1c44017bc25a2ceb5800850a24cfebb59bdf5848a620a46ff4a308ff29ff92324390f06609fb39b3257727c33aad290af7ab842b0a13d37081cf34b03e5b580820d05453c6233c6051710e48aa67e2f4d39f83872eff3f3d49aba2259994356046e84eb9968179d43615712c9c1fd9e4657a17b5db05ecb50b4e631f7374166fc368990cc29560d954e5063cb596f4bd7e92740a672cea0347e0c8cb1341f124ca727c9ad3d12946189846719813a1ff487212bcb998cf2132cdd8fcb111ce10c12e2152ef5bcaf4f9b0b177be4e3352a261162bb2df58d4d74cd88e72027af6d52acc85b69f240209ffaa3b55ed5510b1e044e328a898f528779b715577151c9065b59543f40820a9e12dcfafab7e991421b03ce11c2bf131c2238454c72c68c51b1b7bb3f33ec08422dceb782785b49831d6e3fd569aad3f0bed0e717a0888da3d37b856f1a55844a6e4f31b75854d23d69384dd1cf36dafcc6943f3eaf34aa4041ec33e125f7cca77796c59df85941265c52d79e2347084a5392e97fc442b6c7379eab6752a505cc3ad747da80f0bbf05d24cf31667adce75a13ac488f5e44d1008ce1f1eaf5431122f88c444d57a3ef0477f69e3ff297e0bcf6778515d4b353a8ed3deb8ae38d523d86ab0a310939cdae9d085a5509bc162c9ba381211f2bb3a9e0e28c6fc108a9acde67d67b80a615597628f5b3446686dd4c149df2ac5cc74e6b04fc8e2a6849a3e90421e82934d2351509ab54f168cdce1c5f3a20afe0cf552e0dfa905564109597535b4eab35b26325ff9b2a3025a63f61dc6718d31dee8c607e1d2a739e25a86de0d85ddac8d09bc79628ca2b8a6d348253ea977dcd21355671ee254cded9bfee136f5d4c3fd9dc55f9de2208d77de01d57fd788812352121d65790da29e61f00d4a37ad5d17ab8bb98293b783e7fb3f6163de1060118f4117038b99d46111d5cfb9e390e7659efea11c1814f624595856fecb67a9227b7aefef85e31f9de14676bfb094672d5bed1bf65bdbf7e26b03677cc72003446471e60d75cce36cb1c2c1984b30a342b2b06139256d5f5f5fa8c538b45428b447e78dbb993a8d0808d98c5c39042a4f2b9a81a5089b6f6d6ec0b19f5e574b1da2b9d6fa08f49c672c88e00302cc9e77789314c59be0ca4f6bb38b67571e0d549f95ec9ff697c73899a6e6f0eede59c6a8678b86bebc178a07dc5fd82bea7a0fe0d7fd60da4a44ae756eb4b182b0906ace3f5d1eb9932b356b63ebd54639d653621ee55311fe",
            "bits": "1d0181f2",
            "difficulty": 347762.928199834,
            "chainwork": "000000000000000000000000000000000000000000000000000012024f06e9d8",
            "anchor": "47442189f27d5c2ac3e24dcfd6d227aef5c41548f25f806c603964ec011a7627",
            "valuePools": [
                {
                "id": "sprout",
                "monitored": true,
                "chainValue": 422.1280921,
                "chainValueZat": 42212809210,
                "valueDelta": 0,
                "valueDeltaZat": 0
                },
                {
                "id": "sapling",
                "monitored": true,
                "chainValue": 0,
                "chainValueZat": 0,
                "valueDelta": 0,
                "valueDeltaZat": 0
                }
            ],
            "previousblockhash": "000000014e765bbaa1aec886d6b7b784e1e367e2700d54df163e8a07496f1935",
            "nextblockhash": "0000000078548f474d22ebdf90081935f32f8feafdf0f47de55acbc45504271f"
            }
        }
    }
    
getBlockByBlockHash
`````````````````
getblock "hash"

Definition::

    GET /zec/getBlockByBlockHash?blockHash=00000000febc373a1da2bd9f887b105ad79ddc26ac26c2b28652d64e5207c5b5
    
Example Request::

    GET /zec/getBlockByBlockHash?blockHash=00000000febc373a1da2bd9f887b105ad79ddc26ac26c2b28652d64e5207c5b5

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": {
            "m": {
            "hash": "00000000febc373a1da2bd9f887b105ad79ddc26ac26c2b28652d64e5207c5b5",
            "confirmations": 612218,
            "size": 748771,
            "height": 12800,
            "version": 4,
            "merkleroot": "a2725bef50de57c71ede8d15f769ea5272ab7ad56bdb94ca8a73b12a469e7632",
            "finalsaplingroot": "0000000000000000000000000000000000000000000000000000000000000000",
            "tx": [
                "008440c3cec370670be6a83f6ff7f2518eb47de9257373f31b1e9640ae9e6986",
                "f1d6098b1b076a8f0b5036126bea8bf32eabc42453007ccd89814bb5030e2f59",
                "c94f6dfcfe60acf27c2dde44a8b38694896a6674b5dcf255c63b54ba8162cdc9",
                "2a438db7e3f95f9c74fa691a04763ecc34cf66383ffd8356ed0d405582083eb9",
                "bb4110cb9718f939a260a39826849300942151fb3c9f16e09cffe5a79b0e20fb",
                "c0ea223eeb4024de5fb3e94bb4be927221d17b5b3df6fce12ed43ec3d4fe7493",
                "4d9d4b1a133f5d3abb88a461f0fa669e0aa088b2d93235c3040bc776a6ab8fd9",
                "487f4ceece179a753cc6ba8136e19b2869e0602dda99d5f300e7a8ac58b45f27",
                "cc9095719f7bad03c64afa29e52b32487e2003952e0fb1bcec4273a11ab82a78",
                "2363a19c4b57636d14fc9ad8bc6b2c2609f309ff4b895b21ea6ee7c0908ab2d2",
                "b6819292057f8aa0f2bd1716fbecf53b3d2a591a3ca55b164468e26b26e86fc3",
                "d782054e50408745927b3fef8b813701e76d9c3af79e5ce49be16c112b93a23d",
                "0d8332217aefdfd34a594b28dea40e92be4682fc4d4f331124e6b3930d690379",
                "d85246dad6d0addc4a7ecac125d89a6586857f917fc59c896d8b257dfd7db447",
                "748271801ffc8296f69319f2f4b447774bfbefcad447bb91735433c115c0ad0a",
                "074d91d4c1dec867583fb661ab997e1f4e52a995ae9b97e6afa37ed1e39c8780",
                "3edef316394815b6608afed481c214497f78f93ba4aa3722a1c986c45d4557e6",
                "1d6fb748d2169149ffc61750eb0ddcdfe31ab7bede16b892a1968f701abc6bb0",
                "9d9080562542ce92d6df2c52a580a008f73e73d32ea7c0b389b6b4f8b8b0d36b",
                "51201e1867e8476e8a89c36b13bc07ae587aa00fd1b6d011e0c93d7bbc9995ea",
                "67b166ea599c253eff45edda8e6d73943c1db165bc72516dca9286ab1c354656",
                "2d73db2f76b7a6590f131d9b31f78e453904f352dc9605274f163402fa11091b",
                "92ec55dc7220c0d036383847c79d597b15e1aa18664fa5e995d16642c7733d5d",
                "4577bb320dfe33aa96814c5932f5d1dde847ef5bff2e63e261b463996b86beb3",
                "fc5ccfbfaa901bdf28c4673f3a6dab4e27fbda310676055ac1ba4a2b639468f4"
            ],
            "time": 1479519154,
            "nonce": "0000000000000000000000000000000000000000000000000014117519b7c6db",
            "solution": "0076568fbc8ac5c33d60148fc74c28a19becd044e850593f470862db3dc582d54e13ce679b0a9a5aacc0014d8e917b9f5f1fb235028e90ab9245952a96eb8f339f6dc70bf28139d9e20853b05c2c16e53439f9140354ba7dffca181b20bb31986763f3813609501a3005e42351f122bb9ddbf3a0b0ad05fa186be54ebf951fe432d63faa01cf6ccbb20ffb650c024a4456130340713bbabcd5b9dd35f7c76e5dfb7af5ed70d2552802db77648812d9f2ff58d1c99dc348122605dcf25d06943a730162c3194fab435e402f7dc5d6e2354d6a1dca0ec7b708f444dfe31b5b815c77c382443c3d4e6cadb3f5eee1b829d36019388ce712a6d8d5b858b3137efa12040d5937dbef6665e373604e331c3cec891aedbafd0451162debfff1c25ae37cb8a1daf1d7ce17acc7068998301d614572150eba0b6974ef105bec20a89e6ec94b846b010ab36f88deb9591ff979f3e905689094be513fc509f4121dd4fbddce669b38a8950833addd359b48551b2a816918aad66ce6e039e45906e70af93953c3e9bb9142a02ce63bfd34837c32c0191013dd4bc7f1cff41594ccdab9ce495100dbf1b8143594182f544acafa3a2756085215d63b4a9e6d1d1c44017bc25a2ceb5800850a24cfebb59bdf5848a620a46ff4a308ff29ff92324390f06609fb39b3257727c33aad290af7ab842b0a13d37081cf34b03e5b580820d05453c6233c6051710e48aa67e2f4d39f83872eff3f3d49aba2259994356046e84eb9968179d43615712c9c1fd9e4657a17b5db05ecb50b4e631f7374166fc368990cc29560d954e5063cb596f4bd7e92740a672cea0347e0c8cb1341f124ca727c9ad3d12946189846719813a1ff487212bcb998cf2132cdd8fcb111ce10c12e2152ef5bcaf4f9b0b177be4e3352a261162bb2df58d4d74cd88e72027af6d52acc85b69f240209ffaa3b55ed5510b1e044e328a898f528779b715577151c9065b59543f40820a9e12dcfafab7e991421b03ce11c2bf131c2238454c72c68c51b1b7bb3f33ec08422dceb782785b49831d6e3fd569aad3f0bed0e717a0888da3d37b856f1a55844a6e4f31b75854d23d69384dd1cf36dafcc6943f3eaf34aa4041ec33e125f7cca77796c59df85941265c52d79e2347084a5392e97fc442b6c7379eab6752a505cc3ad747da80f0bbf05d24cf31667adce75a13ac488f5e44d1008ce1f1eaf5431122f88c444d57a3ef0477f69e3ff297e0bcf6778515d4b353a8ed3deb8ae38d523d86ab0a310939cdae9d085a5509bc162c9ba381211f2bb3a9e0e28c6fc108a9acde67d67b80a615597628f5b3446686dd4c149df2ac5cc74e6b04fc8e2a6849a3e90421e82934d2351509ab54f168cdce1c5f3a20afe0cf552e0dfa905564109597535b4eab35b26325ff9b2a3025a63f61dc6718d31dee8c607e1d2a739e25a86de0d85ddac8d09bc79628ca2b8a6d348253ea977dcd21355671ee254cded9bfee136f5d4c3fd9dc55f9de2208d77de01d57fd788812352121d65790da29e61f00d4a37ad5d17ab8bb98293b783e7fb3f6163de1060118f4117038b99d46111d5cfb9e390e7659efea11c1814f624595856fecb67a9227b7aefef85e31f9de14676bfb094672d5bed1bf65bdbf7e26b03677cc72003446471e60d75cce36cb1c2c1984b30a342b2b06139256d5f5f5fa8c538b45428b447e78dbb993a8d0808d98c5c39042a4f2b9a81a5089b6f6d6ec0b19f5e574b1da2b9d6fa08f49c672c88e00302cc9e77789314c59be0ca4f6bb38b67571e0d549f95ec9ff697c73899a6e6f0eede59c6a8678b86bebc178a07dc5fd82bea7a0fe0d7fd60da4a44ae756eb4b182b0906ace3f5d1eb9932b356b63ebd54639d653621ee55311fe",
            "bits": "1d0181f2",
            "difficulty": 347762.928199834,
            "chainwork": "000000000000000000000000000000000000000000000000000012024f06e9d8",
            "anchor": "47442189f27d5c2ac3e24dcfd6d227aef5c41548f25f806c603964ec011a7627",
            "valuePools": [
                {
                "id": "sprout",
                "monitored": true,
                "chainValue": 422.1280921,
                "chainValueZat": 42212809210,
                "valueDelta": 0,
                "valueDeltaZat": 0
                },
                {
                "id": "sapling",
                "monitored": true,
                "chainValue": 0,
                "chainValueZat": 0,
                "valueDelta": 0,
                "valueDeltaZat": 0
                }
            ],
            "previousblockhash": "000000014e765bbaa1aec886d6b7b784e1e367e2700d54df163e8a07496f1935",
            "nextblockhash": "0000000078548f474d22ebdf90081935f32f8feafdf0f47de55acbc45504271f"
            }
        }
    }

getblockcount
`````````````````
Returns the number of blocks in the best valid block chain.

Definition::

    GET /zec/getblockcount
    
Example Request::

    GET /zec/getblockcount

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": 625018
    }

getrawtransaction
`````````````````
By default this function only works sometimes. This is when the tx is in the mempool or there is an unspent output in the utxo for this transaction.

Definition::

    GET /zec/getrawtransaction?txId=05b6de3a91c6e79cd6b8037995ad207cceed5f62dea0fa3b5481f2c13689a168
    
Example Request::

    GET /zec/getrawtransaction?txId=05b6de3a91c6e79cd6b8037995ad207cceed5f62dea0fa3b5481f2c13689a168

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": {
            "m": {
            "hex": "0400008085202f8901975b2f530dab63fa900cefb12f281c9e9d75758fbaff750fd2912e1c23a14fd2000000006b4830450221009536954eda87c8630b1f8bea39b1c5fa8aa8860cfb24bd49a3575d95f1fc91d7022007d9fd1c4ff954f5543d388cae7fba8f346c195cf0743a54a050505783d7d5b20121037b88c957e150467797dadcad00ac9b8aa66a5b4014acaf26e8c0e685ee0c08a8feffffff02f60e0100000000001976a9149bcd2d68e506ac4ad900ae34cd91bf6d50cb8caf88ac50c30000000000001976a914d6f21003daed188c3b6c7d58cce644e3bf7051dc88ac62270900812709000000000000000000000000",
            "txid": "05b6de3a91c6e79cd6b8037995ad207cceed5f62dea0fa3b5481f2c13689a168",
            "overwintered": true,
            "version": 4,
            "versiongroupid": "892f2085",
            "locktime": 599906,
            "expiryheight": 599937,
            "vin": [
                {
                "txid": "d24fa1231c2e91d20f75ffba8f75759d9e1c282fb1ef0c90fa63ab0d532f5b97",
                "vout": 0,
                "scriptSig": {
                    "asm": "30450221009536954eda87c8630b1f8bea39b1c5fa8aa8860cfb24bd49a3575d95f1fc91d7022007d9fd1c4ff954f5543d388cae7fba8f346c195cf0743a54a050505783d7d5b2[ALL] 037b88c957e150467797dadcad00ac9b8aa66a5b4014acaf26e8c0e685ee0c08a8",
                    "hex": "4830450221009536954eda87c8630b1f8bea39b1c5fa8aa8860cfb24bd49a3575d95f1fc91d7022007d9fd1c4ff954f5543d388cae7fba8f346c195cf0743a54a050505783d7d5b20121037b88c957e150467797dadcad00ac9b8aa66a5b4014acaf26e8c0e685ee0c08a8"
                },
                "value": 0.00121642,
                "valueSat": 121642,
                "address": "t1cyajT8fwBqoFiuz3EWDAo9cFAfYfSrtHt",
                "sequence": 4294967294
                }
            ],
            "vout": [
                {
                "value": 0.00069366,
                "valueZat": 69366,
                "valueSat": 69366,
                "n": 0,
                "scriptPubKey": {
                    "asm": "OP_DUP OP_HASH160 9bcd2d68e506ac4ad900ae34cd91bf6d50cb8caf OP_EQUALVERIFY OP_CHECKSIG",
                    "hex": "76a9149bcd2d68e506ac4ad900ae34cd91bf6d50cb8caf88ac",
                    "reqSigs": 1,
                    "type": "pubkeyhash",
                    "addresses": [
                    "t1Y5QY3VHACJjeoFtJ65DQhCKxAhNNHXwjE"
                    ]
                },
                "spentTxId": "1c2f29006c314fdf5308ecc7d35bbbe3b7ae58c02eeda32338ffcfca0df2198a",
                "spentIndex": 0,
                "spentHeight": 600382
                },
                {
                "value": 0.0005,
                "valueZat": 50000,
                "valueSat": 50000,
                "n": 1,
                "scriptPubKey": {
                    "asm": "OP_DUP OP_HASH160 d6f21003daed188c3b6c7d58cce644e3bf7051dc OP_EQUALVERIFY OP_CHECKSIG",
                    "hex": "76a914d6f21003daed188c3b6c7d58cce644e3bf7051dc88ac",
                    "reqSigs": 1,
                    "type": "pubkeyhash",
                    "addresses": [
                    "t1dU8bBu8rFKvLcTZsMGXSbr3uCuyT9Uq84"
                    ]
                }
                }
            ],
            "vjoinsplit": [],
            "valueBalance": 0,
            "valueBalanceZat": 0,
            "vShieldedSpend": [],
            "vShieldedOutput": [],
            "blockhash": "000000000031fa1cdd94a4a13c7a4d6b2a8f1f1dfc3cfc14d8123f8af5ae2362",
            "height": 599917,
            "confirmations": 25102,
            "time": 1568012519,
            "blocktime": 1568012519
            }
        }
    }
    
decoderawtransaction
`````````````````
Return a JSON object representing the serialized, hex-encoded transaction.

Definition::

    GET /zec/decoderawtransaction?rawtransaction={rawtransaction}
    
Example Request::

    GET /zec/decoderawtransaction?rawtransaction={rawtransaction}

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": 
        {
            "txid" : "id",        (string) The transaction id
            "overwintered" : bool   (boolean) The Overwintered flag
            "version" : n,          (numeric) The version
            "versiongroupid": "hex"   (string, optional) The version group id (Overwintered txs)
            "locktime" : ttt,       (numeric) The lock time
            "expiryheight" : n,     (numeric, optional) Last valid block height for mining transaction (Overwintered txs)
            "vin" : [               (array of json objects)
                {
                "txid": "id",    (string) The transaction id
                "vout": n,         (numeric) The output number
                "scriptSig": {     (json object) The script
                    "asm": "asm",  (string) asm
                    "hex": "hex"   (string) hex
                },
                "sequence": n     (numeric) The script sequence number
                }
                ,...
            ],
            "vout" : [             (array of json objects)
                {
                "value" : x.xxx,            (numeric) The value in ZEC
                "n" : n,                    (numeric) index
                "scriptPubKey" : {          (json object)
                    "asm" : "asm",          (string) the asm
                    "hex" : "hex",          (string) the hex
                    "reqSigs" : n,            (numeric) The required sigs
                    "type" : "pubkeyhash",  (string) The type, eg 'pubkeyhash'
                    "addresses" : [           (json array of string)
                    "t12tvKAXCxZjSmdNbao16dKXC8tRWfcF5oc"   (string) zcash address
                    ,...
                    ]
                }
                }
                ,...
            ],
            "vjoinsplit" : [        (array of json objects, only for version >= 2)
                {
                "vpub_old" : x.xxx,         (numeric) public input value in ZEC
                "vpub_new" : x.xxx,         (numeric) public output value in ZEC
                "anchor" : "hex",         (string) the anchor
                "nullifiers" : [            (json array of string)
                    "hex"                     (string) input note nullifier
                    ,...
                ],
                "commitments" : [           (json array of string)
                    "hex"                     (string) output note commitment
                    ,...
                ],
                "onetimePubKey" : "hex",  (string) the onetime public key used to encrypt the ciphertexts
                "randomSeed" : "hex",     (string) the random seed
                "macs" : [                  (json array of string)
                    "hex"                     (string) input note MAC
                    ,...
                ],
                "proof" : "hex",          (string) the zero-knowledge proof
                "ciphertexts" : [           (json array of string)
                    "hex"                     (string) output note ciphertext
                    ,...
                ]
                }
            ],
        }

    }
    
sendRawTransaction
`````````````````
Submits raw transaction (serialized, hex-encoded) to local node and network.

Definition::

    GET /zec/sendRawTransaction?hexstring={rawtransaction}
    
Example Request::

    GET /zec/sendRawTransaction?hexstring={rawtransaction}

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": 'txId'
    }
    
validateaddress
`````````````````
Return information about the given Zcash address.

Definition::

    GET /zec/validateaddress?address={address}
    
Example Request::

    curl -X GET --header 'Accept: application/json' 'http://localhost:8080/zec/validateaddress?address=xxxxxxxx'

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": false
    }