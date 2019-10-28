Ripple API Docs
==================

account_info
`````````````````
The account_info command retrieves information about an account, its activity, and its XRP balance. All information retrieved is relative to a particular version of the ledger.

定义::

    POST /xrp/account_info
    
请求示例::

    curl -X POST --header 'Content-Type: application/json' --header 'Accept: application/json' -d '{ \ 
        "account": "r9cZA1mLK5R5Am25ArfXFmqgNwjZgnfk59", \ 
        "strict": true, \ 
        "ledger_index": "current", \ 
        "queue": true \ 
        }' 'http://localhost:8080/xrp/account_info'

返回:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": {
            "result": {
            "ledger_current_index": 50897665,
            "validated": false,
            "account_data": {
                "Account": "r9cZA1mLK5R5Am25ArfXFmqgNwjZgnfk59",
                "OwnerCount": 17,
                "PreviousTxnLgrSeq": 46220792,
                "LedgerEntryType": "AccountRoot",
                "index": "4F83A2CF7E70F77F79A307E6A472BFC2585B806A70833CCD1C26105BAE0D6E05",
                "PreviousTxnID": "81CF63F4039FCCF33105407D8F23566F91ED5A768C95E730BF759CD1B4397E75",
                "Flags": 0,
                "Sequence": 1406,
                "Balance": "13315611787"
            },
            "queue_data": {
                "txn_count": 0
            },
            "status": "success"
            }
        }
    }

account_currencies
`````````````````
The account_currencies command retrieves a list of currencies that an account can send or receive, based on its trust lines. (This is not a thoroughly confirmed list, but it can be used to populate user interfaces.)

定义::

    POST /xrp/account_currencies
    
请求示例::

    curl -X POST --header 'Content-Type: application/json' --header 'Accept: application/json' -d '{ \ 
             "account": "r9cZA1mLK5R5Am25ArfXFmqgNwjZgnfk59", \ 
             "account_index": 0, \ 
             "ledger_index": "validated", \ 
             "strict": true \ 
         }' 'http://localhost:8080/xrp/account_currencies'

返回:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": {
            "result": {
            "validated": true,
            "ledger_index": 50897632,
            "ledger_hash": "6C9D5CC114729BA4A1F21E0FAE9DF7A706E29D15F35AC1DAABE0F4BC0C087CD6",
            "send_currencies": [
                "ASP",
                "BTC",
                "CHF",
                "CNY",
                "DYM",
                "EUR",
                "JOE",
                "JPY",
                "MXN",
                "USD"
            ],
            "receive_currencies": [
                "BTC",
                "CNY",
                "DYM",
                "EUR",
                "JOE",
                "MXN",
                "USD",
                "015841551A748AD2C1F76FF6ECB0CCCD00000000"
            ],
            "status": "success"
            }
        }
    }

account_tx
`````````````````
Retrieves a list of transactions that affected the specified account.

定义::

    POST /xrp/account_tx
    
请求示例::

    curl -X POST --header 'Content-Type: application/json' --header 'Accept: application/json' -d '{"account": "rQ3fNyLjbvcDaPNS4EAJY8aT9zR3uGk17c", \ 
        "ledger_index_min": -100, \ 
        "ledger_index_max": -1, \ 
        "binary": false, \ 
        "limit": 2, \ 
        "forward": false \ 
    }' 'http://localhost:8080/xrp/account_tx'

返回:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": {
            "result": {
            "marker": {
                "ledger": 50897835,
                "seq": 12
            },
            "ledger_index_max": 50897835,
            "limit": 2,
            "ledger_index_min": 50774373,
            "transactions": [
                {
                "tx": {
                    "date": 625126592,
                    "Account": "rQ3fNyLjbvcDaPNS4EAJY8aT9zR3uGk17c",
                    "TransactionType": "OfferCreate",
                    "ledger_index": 50897835,
                    "SigningPubKey": "039451ECAC6D4EB75E3C926E7DC7BA7721719A1521502F99EC7EB2FE87CEE9E824",
                    "Fee": "12",
                    "OfferSequence": 15355908,
                    "TakerGets": "9921368056",
                    "Flags": 0,
                    "Sequence": 15355912,
                    "LastLedgerSequence": 50897837,
                    "TakerPays": {
                    "currency": "CNY",
                    "value": "21822.24746697112",
                    "issuer": "rJ1adrpGS3xsnQMb9Cw54tWJVFPuSdZHK"
                    },
                    "TxnSignature": "3045022100E7D62765390C549B5DAFDBEFF6B6FDFC04359D62522FA1F53A850E7D0E2135F0022007CE5273A767D70CCB23F82233F022406949F769A46A27B4874F32ABC60B11C2",
                    "inLedger": 50897835,
                    "hash": "4E334855C132F97E7A0962395CA53ACC88B2D811614B44D1BC45129515508B25"
                },
                "validated": true,
                "meta": {
                    "AffectedNodes": [
                    {
                        "ModifiedNode": {
                        "LedgerIndex": "07CE63F6E62E095CAF97BC77572A203D75ECB68219F97505AC5DF2DB061C9D96",
                        "FinalFields": {
                            "Owner": "rQ3fNyLjbvcDaPNS4EAJY8aT9zR3uGk17c",
                            "IndexNext": "0000000000000000",
                            "IndexPrevious": "0000000000000000",
                            "Flags": 0,
                            "RootIndex": "07CE63F6E62E095CAF97BC77572A203D75ECB68219F97505AC5DF2DB061C9D96"
                        },
                        "LedgerEntryType": "DirectoryNode"
                        }
                    },
                    {
                        "DeletedNode": {
                        "LedgerIndex": "3E3AE66D1C3C8B65DE5EAF5BBEC520DB7BE109B5A61B18C7034833402F7F5FF8",
                        "FinalFields": {
                            "TakerPays": {
                            "currency": "CNY",
                            "value": "5609.10794821284",
                            "issuer": "rJ1adrpGS3xsnQMb9Cw54tWJVFPuSdZHK"
                            },
                            "Account": "rQ3fNyLjbvcDaPNS4EAJY8aT9zR3uGk17c",
                            "PreviousTxnLgrSeq": 50897834,
                            "BookDirectory": "623C4C4AD65873DA787AC85A0A1385FE6233B6DE100799474F07CF8D27B6A335",
                            "OwnerNode": "0000000000000000",
                            "PreviousTxnID": "C925A52010E17A84CD112FBDD2F260CFADCDDE1229289D5AF53A376004D3D3CC",
                            "TakerGets": "2551299253",
                            "Flags": 0,
                            "Sequence": 15355908,
                            "BookNode": "0000000000000000"
                        },
                        "LedgerEntryType": "Offer"
                        }
                    },
                    {
                        "ModifiedNode": {
                        "LedgerIndex": "47FE64F9223D604034486F4DA7A175D5DA7F8A096952261CF8F3D77B74DC4AFA",
                        "FinalFields": {
                            "Account": "rQ3fNyLjbvcDaPNS4EAJY8aT9zR3uGk17c",
                            "OwnerCount": 5,
                            "Flags": 0,
                            "Sequence": 15355913,
                            "Balance": "25275244638"
                        },
                        "PreviousFields": {
                            "Sequence": 15355912,
                            "Balance": "25275244650"
                        },
                        "PreviousTxnLgrSeq": 50897835,
                        "LedgerEntryType": "AccountRoot",
                        "PreviousTxnID": "51920F104B6BEC784F3FAD289BDA5566FDE1B71343308684D3A5DAB1CF94A5EF"
                        }
                    },
                    {
                        "DeletedNode": {
                        "LedgerIndex": "623C4C4AD65873DA787AC85A0A1385FE6233B6DE100799474F07CF8D27B6A335",
                        "FinalFields": {
                            "TakerPaysCurrency": "000000000000000000000000434E590000000000",
                            "ExchangeRate": "4F07CF8D27B6A335",
                            "TakerGetsCurrency": "0000000000000000000000000000000000000000",
                            "TakerGetsIssuer": "0000000000000000000000000000000000000000",
                            "Flags": 0,
                            "RootIndex": "623C4C4AD65873DA787AC85A0A1385FE6233B6DE100799474F07CF8D27B6A335",
                            "TakerPaysIssuer": "0360E3E0751BD9A566CD03FA6CAFC78118B82BA0"
                        },
                        "LedgerEntryType": "DirectoryNode"
                        }
                    },
                    {
                        "CreatedNode": {
                        "LedgerIndex": "623C4C4AD65873DA787AC85A0A1385FE6233B6DE100799474F07D073A8476C73",
                        "LedgerEntryType": "DirectoryNode",
                        "NewFields": {
                            "TakerPaysCurrency": "000000000000000000000000434E590000000000",
                            "ExchangeRate": "4F07D073A8476C73",
                            "RootIndex": "623C4C4AD65873DA787AC85A0A1385FE6233B6DE100799474F07D073A8476C73",
                            "TakerPaysIssuer": "0360E3E0751BD9A566CD03FA6CAFC78118B82BA0"
                        }
                        }
                    },
                    {
                        "CreatedNode": {
                        "LedgerIndex": "B5A6FCAC273C9F79ADA41832364F8DBB5EAAA711E0D9948A107703868F8DF129",
                        "LedgerEntryType": "Offer",
                        "NewFields": {
                            "TakerPays": {
                            "currency": "CNY",
                            "value": "21822.24746697112",
                            "issuer": "rJ1adrpGS3xsnQMb9Cw54tWJVFPuSdZHK"
                            },
                            "Account": "rQ3fNyLjbvcDaPNS4EAJY8aT9zR3uGk17c",
                            "BookDirectory": "623C4C4AD65873DA787AC85A0A1385FE6233B6DE100799474F07D073A8476C73",
                            "TakerGets": "9921368056",
                            "Sequence": 15355912
                        }
                        }
                    }
                    ],
                    "TransactionResult": "tesSUCCESS",
                    "TransactionIndex": 14
                }
                },
                {
                "tx": {
                    "date": 625126592,
                    "Account": "rQ3fNyLjbvcDaPNS4EAJY8aT9zR3uGk17c",
                    "TransactionType": "OfferCreate",
                    "ledger_index": 50897835,
                    "SigningPubKey": "039451ECAC6D4EB75E3C926E7DC7BA7721719A1521502F99EC7EB2FE87CEE9E824",
                    "Fee": "12",
                    "OfferSequence": 15355907,
                    "TakerGets": "5269844095",
                    "Flags": 0,
                    "Sequence": 15355911,
                    "LastLedgerSequence": 50897837,
                    "TakerPays": {
                    "currency": "CNY",
                    "value": "11375.06387618575",
                    "issuer": "rJ1adrpGS3xsnQMb9Cw54tWJVFPuSdZHK"
                    },
                    "TxnSignature": "30440220322FB7A3C1FD3D44E188A0EA7A1E81D55DBFBC9268AFF1373BDE0820B7309753022016C61DF5DF6F5CE565BDF9551A92004B27FF5B99140A5821DE6322C996960088",
                    "inLedger": 50897835,
                    "hash": "51920F104B6BEC784F3FAD289BDA5566FDE1B71343308684D3A5DAB1CF94A5EF"
                },
                "validated": true,
                "meta": {
                    "AffectedNodes": [
                    {
                        "ModifiedNode": {
                        "LedgerIndex": "07CE63F6E62E095CAF97BC77572A203D75ECB68219F97505AC5DF2DB061C9D96",
                        "FinalFields": {
                            "Owner": "rQ3fNyLjbvcDaPNS4EAJY8aT9zR3uGk17c",
                            "IndexNext": "0000000000000000",
                            "IndexPrevious": "0000000000000000",
                            "Flags": 0,
                            "RootIndex": "07CE63F6E62E095CAF97BC77572A203D75ECB68219F97505AC5DF2DB061C9D96"
                        },
                        "LedgerEntryType": "DirectoryNode"
                        }
                    },
                    {
                        "ModifiedNode": {
                        "LedgerIndex": "47FE64F9223D604034486F4DA7A175D5DA7F8A096952261CF8F3D77B74DC4AFA",
                        "FinalFields": {
                            "Account": "rQ3fNyLjbvcDaPNS4EAJY8aT9zR3uGk17c",
                            "OwnerCount": 5,
                            "Flags": 0,
                            "Sequence": 15355912,
                            "Balance": "25275244650"
                        },
                        "PreviousFields": {
                            "Sequence": 15355911,
                            "Balance": "25275244662"
                        },
                        "PreviousTxnLgrSeq": 50897835,
                        "LedgerEntryType": "AccountRoot",
                        "PreviousTxnID": "689A62337923B7BA2B6C733E252FFE719C2578DCB69FC362473C62E8977C321F"
                        }
                    },
                    {
                        "DeletedNode": {
                        "LedgerIndex": "623C4C4AD65873DA787AC85A0A1385FE6233B6DE100799474F07AA431940A49E",
                        "FinalFields": {
                            "TakerPaysCurrency": "000000000000000000000000434E590000000000",
                            "ExchangeRate": "4F07AA431940A49E",
                            "TakerGetsCurrency": "0000000000000000000000000000000000000000",
                            "TakerGetsIssuer": "0000000000000000000000000000000000000000",
                            "Flags": 0,
                            "RootIndex": "623C4C4AD65873DA787AC85A0A1385FE6233B6DE100799474F07AA431940A49E",
                            "TakerPaysIssuer": "0360E3E0751BD9A566CD03FA6CAFC78118B82BA0"
                        },
                        "LedgerEntryType": "DirectoryNode"
                        }
                    },
                    {
                        "CreatedNode": {
                        "LedgerIndex": "623C4C4AD65873DA787AC85A0A1385FE6233B6DE100799474F07AB2999D7E69B",
                        "LedgerEntryType": "DirectoryNode",
                        "NewFields": {
                            "TakerPaysCurrency": "000000000000000000000000434E590000000000",
                            "ExchangeRate": "4F07AB2999D7E69B",
                            "RootIndex": "623C4C4AD65873DA787AC85A0A1385FE6233B6DE100799474F07AB2999D7E69B",
                            "TakerPaysIssuer": "0360E3E0751BD9A566CD03FA6CAFC78118B82BA0"
                        }
                        }
                    },
                    {
                        "CreatedNode": {
                        "LedgerIndex": "A0328677B30BC3664703B86F8D809946DFFDE952F6898FAF7FD46681D4BDFA1C",
                        "LedgerEntryType": "Offer",
                        "NewFields": {
                            "TakerPays": {
                            "currency": "CNY",
                            "value": "11375.06387618575",
                            "issuer": "rJ1adrpGS3xsnQMb9Cw54tWJVFPuSdZHK"
                            },
                            "Account": "rQ3fNyLjbvcDaPNS4EAJY8aT9zR3uGk17c",
                            "BookDirectory": "623C4C4AD65873DA787AC85A0A1385FE6233B6DE100799474F07AB2999D7E69B",
                            "TakerGets": "5269844095",
                            "Sequence": 15355911
                        }
                        }
                    },
                    {
                        "DeletedNode": {
                        "LedgerIndex": "D83A7D78385F85EE88363D8806CFADEA1E468436D75DC0BDF501A2F93A29D802",
                        "FinalFields": {
                            "TakerPays": {
                            "currency": "CNY",
                            "value": "18419.25685844518",
                            "issuer": "rJ1adrpGS3xsnQMb9Cw54tWJVFPuSdZHK"
                            },
                            "Account": "rQ3fNyLjbvcDaPNS4EAJY8aT9zR3uGk17c",
                            "PreviousTxnLgrSeq": 50897834,
                            "BookDirectory": "623C4C4AD65873DA787AC85A0A1385FE6233B6DE100799474F07AA431940A49E",
                            "OwnerNode": "0000000000000000",
                            "PreviousTxnID": "0E5B9C486D5E31EF502B69E4ED238E2FD0563A81115C23078383D31BE681F219",
                            "TakerGets": "8537196172",
                            "Flags": 0,
                            "Sequence": 15355907,
                            "BookNode": "0000000000000000"
                        },
                        "LedgerEntryType": "Offer"
                        }
                    }
                    ],
                    "TransactionResult": "tesSUCCESS",
                    "TransactionIndex": 13
                }
                }
            ],
            "account": "rQ3fNyLjbvcDaPNS4EAJY8aT9zR3uGk17c",
            "status": "success"
            }
        }
    }

ledger
`````````````````
Retrieve information about the public ledger.

定义::

    POST /xrp/ledger
    
请求示例::

    curl -X POST --header 'Content-Type: application/json' --header 'Accept: application/json' -d '{"ledger_index": "validated", \ 
        "full": false, \ 
        "accounts": false, \ 
        "transactions": false, \ 
        "expand": false, \ 
        "owner_funds": false \ 
    }' 'http://localhost:8080/xrp/ledger'

返回:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": {
            "result": {
            "ledger": {
                "close_flags": 0,
                "ledger_index": "50897930",
                "seqNum": "50897930",
                "account_hash": "944A9641AD68864E2AE1A0C55CCD9ADF368F1D0C705F724EC09FE2EA9D0A26FF",
                "close_time_resolution": 10,
                "accepted": true,
                "close_time": 625126970,
                "close_time_human": "2019-Oct-23 06:22:50.000000000",
                "ledger_hash": "B1ECFBF713A011B18622A653A695DDE343B8FC5FFA62CD9A2A0BF859C247DE45",
                "total_coins": "99991315287644195",
                "closed": true,
                "totalCoins": "99991315287644195",
                "parent_close_time": 625126961,
                "hash": "B1ECFBF713A011B18622A653A695DDE343B8FC5FFA62CD9A2A0BF859C247DE45",
                "parent_hash": "8D5F65E85585BBEDD6523F4C692E93C47EF408EC1B07E10A15C1DA56A024CABB",
                "transaction_hash": "49C882DFAEED23815615FDC3DB76A598644C9C0C72ACB56ACCE72A148A27F1F9"
            },
            "validated": true,
            "ledger_index": 50897930,
            "ledger_hash": "B1ECFBF713A011B18622A653A695DDE343B8FC5FFA62CD9A2A0BF859C247DE45",
            "status": "success"
            }
        }
    }

ledger_closed
`````````````````
Returns the unique identifiers of the most recently closed ledger. (This ledger is not necessarily validated and immutable yet.)

定义::

    POST /xrp/ledger_closed
    
请求示例::

    curl -X POST --header 'Content-Type: application/json' --header 'Accept: application/json' 'http://localhost:8080/xrp/ledger_closed'

返回:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": {
            "result": {
            "ledger_index": 50898103,
            "ledger_hash": "4D65A1C7B09FB1D4D33CA10B01C3E6C1F1C79D6F50D6D787933B0C8FC4B97388",
            "status": "success"
            }
        }
    }

ledger_current
`````````````````
The ledger_current method returns the unique identifiers of the current in-progress ledger. This command is mostly useful for testing, because the ledger returned is still in flux.

定义::

    POST /xrp/ledger_current
    
请求示例::

    curl -X POST --header 'Content-Type: application/json' --header 'Accept: application/json' 'http://localhost:8080/xrp/ledger_current'

返回:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": {
            "result": {
            "ledger_current_index": 50898248,
            "status": "success"
            }
        }
    }

ledger_data
`````````````````
The ledger_data method retrieves contents of the specified ledger. You can iterate through several calls to retrieve the entire contents of a single ledger version.

定义::

    POST /xrp/ledger_data
    
请求示例::

    curl -X POST --header 'Content-Type: application/json' --header 'Accept: application/json' -d '{ \ 
             "binary": true, \ 
             "ledger_hash": "93F0F35AB8657DA25B11DA00BA39EE1A26C8B85F64DAB687E846AECB21D2A715", \ 
             "limit": 5 \ 
         }' 'http://localhost:8080/xrp/ledger_data'

返回:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": {
            "result": {
            "ledger": {
                "ledger_data": "0308A57D01633D924BB676A307292316D7587E9CB6194D11114BEA8AC308ABC5DEB132F26B2D17564E7BD3D01C5E1A69AC9F7CB34395A324AC566228D3E1FE6149ED812EE30F3E31971BFCA4BCA530BF992FF0377C7348AB3F76D38179EC048B84FE660A269627D6F2B1EAC32542B3D22542B3DA0A00",
                "closed": true
            },
            "validated": true,
            "ledger_index": 50898301,
            "ledger_hash": "93F0F35AB8657DA25B11DA00BA39EE1A26C8B85F64DAB687E846AECB21D2A715",
            "marker": "0000139EDA03EF58CE7176F1402035B5EB6AEE49724555DDB0EBA01432B009A7",
            "state": [
                {
                "data": "110061220000000024000000032502F729932D00000000555F39A60CE98875C0350EBD6F03D28878D694E9360D7C4431C122BD3E5D46421D6240000000066BB8958114E376654FF7B1F656D56462FB43E77E9776EE7396",
                "index": "000003E6AFED1AADCC39AAE0727B354C2286F1503274F345FE661748F24366CF"
                },
                {
                "data": "1100722200210000250178D1CA37000000000000000038000000000000028355C0C37CE200B509E0A529880634F7841A9EF4CB65F03C12E6004CFAD9718D66946280000000000000000000000000000000000000004743420000000000000000000000000000000000000000000000000166D6071AFD498D000000000000000000000000000047434200000000002599D1D255BCA61189CA64C84528F2FCBE4BFC3867800000000000000000000000000000000000000047434200000000006EEBB1D1852CE667876A0B3630861FB6C6AB358E",
                "index": "0000041EFD027808D3F78C8352F97E324CB816318E00B977C74ECDDC7CD975B2"
                },
                {
                "data": "110061220000000024000000022502DA163B2D00000000557540CE04B966D67DBD39F3AA832274902B79AF4782F5AC9D4DC7CD18B1D9AE0D624000000001312D008114B6B047F1FE00A59289D45CDDB0FE81F6BD07A267",
                "index": "000004D417A9CE049C9A71A62B004659B5F1AAAB1BEA1EFDE4E01EB3497FD999"
                },
                {
                "data": "110061220000000024000000022502418FCE2D0000000155E4BE6307E377590FF56BBF2F26DCBC4BA9682A4C141269352E4E2D4E53C1116E624000000001312CF48114D774EA776552E07F863D6BE94ADFD8735A28D82E",
                "index": "00000FB78838CA2CFA82E7438B4F54794A6783327326D58C46B4EF137C059038"
                },
                {
                "data": "1100612200000000240000000125024951D62D0000000055C0D950DF1A7FA968975598C261DEEB7AEC40E367266BEBC91D471F39C1DE040D62400000012A0507A081147A762D01DEFA26F7EE16BFAD723468A366E8F4F0",
                "index": "000012F60C3F1E226D03F974AE8E77250B2BEA91C38AB4146B6055A048C7D540"
                }
            ],
            "status": "success"
            }
        }
    }

ledger_entry
`````````````````
The ledger_data method retrieves contents of the specified ledger. You can iterate through several calls to retrieve the entire contents of a single ledger version.

定义::

    POST /xrp/ledger_entry
    
请求示例::

    curl -X POST --header 'Content-Type: application/json' --header 'Accept: application/json' -d '{ \ 
                "account_root": "r9cZA1mLK5R5Am25ArfXFmqgNwjZgnfk59", \ 
                "ledger_index": "validated", \ 
                "type": "account_root" \ 
            }' 'http://localhost:8080/xrp/ledger_entry'

返回:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": {
            "result": {
            "node": {
                "Account": "r9cZA1mLK5R5Am25ArfXFmqgNwjZgnfk59",
                "OwnerCount": 17,
                "PreviousTxnLgrSeq": 46220792,
                "LedgerEntryType": "AccountRoot",
                "index": "4F83A2CF7E70F77F79A307E6A472BFC2585B806A70833CCD1C26105BAE0D6E05",
                "PreviousTxnID": "81CF63F4039FCCF33105407D8F23566F91ED5A768C95E730BF759CD1B4397E75",
                "Flags": 0,
                "Sequence": 1406,
                "Balance": "13315611787"
            },
            "validated": true,
            "ledger_index": 50898378,
            "ledger_hash": "115DE5F31FBBE2A7D8479584C3D1E36D56690BC53922F48AB2019540FD54A0FD",
            "index": "4F83A2CF7E70F77F79A307E6A472BFC2585B806A70833CCD1C26105BAE0D6E05",
            "status": "success"
            }
        }
    }

sign
`````````````````
The sign method takes a transaction in JSON format and a seed value, and returns a signed binary representation of the transaction. To contribute one signature to a multi-signed transaction, use the sign_for method instead.

定义::

    POST /xrp/sign
    
请求示例::

    curl -X POST --header 'Content-Type: application/json' --header 'Accept: application/json' -d '{ \ 
                "offline": false, \ 
                "secret": "s████████████████████████████", \ 
                "tx_json": { \ 
                    "Account": "rf1BiGeXwwQoi8Z2ueFYTEXSwuJYfV2Jpn", \ 
                    "Amount": { \ 
                        "currency": "USD", \ 
                        "issuer": "rf1BiGeXwwQoi8Z2ueFYTEXSwuJYfV2Jpn", \ 
                        "value": "1" \ 
                    }, \ 
                    "Destination": "ra5nK24KXen9AHvsdFTKHSANinZseWnPcX", \ 
                    "TransactionType": "Payment" \ 
                }, \ 
                "fee_mult_max": 1000 \ 
            }' 'http://localhost:8080/xrp/sign'

返回:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": {
            "result": {
                "status": "success",
                "tx_blob": "1200002280000000240000016861D4838D7EA4C6800000000000000000000000000055534400000000004B4E9C06F24296074F7BC48F92A97916C6DC5EA9684000000000002710732103AB40A0490F9B7ED8DF29D246BF2D6269820A0EE7742ACDD457BEA7C7D0931EDB7446304402200E5C2DD81FDF0BE9AB2A8D797885ED49E804DBF28E806604D878756410CA98B102203349581946B0DDA06B36B35DBC20EDA27552C1F167BCF5C6ECFF49C6A46F858081144B4E9C06F24296074F7BC48F92A97916C6DC5EA983143E9D4A2B8AA0780F682D136F7A56D6724EF53754",
                "tx_json": {
                    "Account": "rf1BiGeXwwQoi8Z2ueFYTEXSwuJYfV2Jpn",
                    "Amount": {
                        "currency": "USD",
                        "issuer": "rf1BiGeXwwQoi8Z2ueFYTEXSwuJYfV2Jpn",
                        "value": "1"
                    },
                    "Destination": "ra5nK24KXen9AHvsdFTKHSANinZseWnPcX",
                    "Fee": "10000",
                    "Flags": 2147483648,
                    "Sequence": 360,
                    "SigningPubKey": "03AB40A0490F9B7ED8DF29D246BF2D6269820A0EE7742ACDD457BEA7C7D0931EDB",
                    "TransactionType": "Payment",
                    "TxnSignature": "304402200E5C2DD81FDF0BE9AB2A8D797885ED49E804DBF28E806604D878756410CA98B102203349581946B0DDA06B36B35DBC20EDA27552C1F167BCF5C6ECFF49C6A46F8580",
                    "hash": "4D5D90890F8D49519E4151938601EF3D0B30B16CD6A519D9C99102C9FA77F7E0"
                }
            }
        }
    }

sign_for
`````````````````
The sign_for command provides one signature for a multi-signed transaction.

定义::

    POST /xrp/sign_for
    
请求示例::

    curl -X POST --header 'Content-Type: application/json' --header 'Accept: application/json' -d '{ \ 
            "account": "rLFd1FzHMScFhLsXeaxStzv3UC97QHGAbM", \ 
            "seed": "s████████████████████████████", \ 
            "key_type": "ed25519", \ 
            "tx_json": { \ 
                "TransactionType": "TrustSet", \ 
                "Account": "rEuLyBCvcw4CFmzv8RepSiAoNgF8tTGJQC", \ 
                "Flags": 262144, \ 
                "LimitAmount": { \ 
                    "currency": "USD", \ 
                    "issuer": "rHb9CJAWyB4rj91VRWn96DkukG4bwdtyTh", \ 
                    "value": "100" \ 
                }, \ 
                "Sequence": 2, \ 
                "SigningPubKey": "", \ 
                "Fee": "30000" \ 
            } \ 
        }' 'http://localhost:8080/xrp/sign_for'

返回:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": {
            "result": {
                "status": "success",
                "tx_blob": "1200142200040000240000000263D5038D7EA4C680000000000000000000000000005553440000000000B5F762798A53D543A014CAF8B297CFF8F2F937E868400000000000753073008114A3780F5CB5A44D366520FC44055E8ED44D9A2270F3E010732102B3EC4E5DD96029A647CFA20DA07FE1F85296505552CCAC114087E66B46BD77DF744730450221009C195DBBF7967E223D8626CA19CF02073667F2B22E206727BFE848FF42BEAC8A022048C323B0BED19A988BDBEFA974B6DE8AA9DCAE250AA82BBD1221787032A864E58114204288D2E47F8EF6C99BCC457966320D12409711E1F1",
                "tx_json": {
                    "Account": "rEuLyBCvcw4CFmzv8RepSiAoNgF8tTGJQC",
                    "Fee": "30000",
                    "Flags": 262144,
                    "LimitAmount": {
                        "currency": "USD",
                        "issuer": "rHb9CJAWyB4rj91VRWn96DkukG4bwdtyTh",
                        "value": "100"
                    },
                    "Sequence": 2,
                    "Signers": [{
                            "Signer": {
                                "Account": "rsA2LpzuawewSBQXkiju3YQTMzW13pAAdW",
                                "SigningPubKey": "02B3EC4E5DD96029A647CFA20DA07FE1F85296505552CCAC114087E66B46BD77DF",
                                "TxnSignature": "30450221009C195DBBF7967E223D8626CA19CF02073667F2B22E206727BFE848FF42BEAC8A022048C323B0BED19A988BDBEFA974B6DE8AA9DCAE250AA82BBD1221787032A864E5"
                            }
                        }
                    ],
                    "SigningPubKey": "",
                    "TransactionType": "TrustSet",
                    "hash": "A94A6417D1A7AAB059822B894E13D322ED3712F7212CE9257801F96DE6C3F6AE"
                }
            }
        }
    }

submit 
`````````````````
The submit method applies a transaction and sends it to the network to be confirmed and included in future ledgers.

定义::

    POST /xrp/submit
    
请求示例::

    curl -X POST --header 'Content-Type: application/json' --header 'Accept: application/json' -d '{ \ 
        "tx_blob": "1200002280000000240000000361D4838D7EA4C6800000000000000000000000000055534400000000004B4E9C06F24296074F7BC48F92A97916C6DC5EA968400000000000000A732103AB40A0490F9B7ED8DF29D246BF2D6269820A0EE7742ACDD457BEA7C7D0931EDB74473045022100D184EB4AE5956FF600E7536EE459345C7BBCF097A84CC61A93B9AF7197EDB98702201CEA8009B7BEEBAA2AACC0359B41C427C1C5B550A4CA4B80CF2174AF2D6D5DCE81144B4E9C06F24296074F7BC48F92A97916C6DC5EA983143E9D4A2B8AA0780F682D136F7A56D6724EF53754" \ 
        }' 'http://localhost:8080/xrp/submit'

返回:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": {
            "result": {
                "engine_result": "tesSUCCESS",
                "engine_result_code": 0,
                "engine_result_message": "The transaction was applied. Only final in a validated ledger.",
                "status": "success",
                "tx_blob": "1200002280000000240000016961D4838D7EA4C6800000000000000000000000000055534400000000004B4E9C06F24296074F7BC48F92A97916C6DC5EA9684000000000002710732103AB40A0490F9B7ED8DF29D246BF2D6269820A0EE7742ACDD457BEA7C7D0931EDB74473045022100A7CCD11455E47547FF617D5BFC15D120D9053DFD0536B044F10CA3631CD609E502203B61DEE4AC027C5743A1B56AF568D1E2B8E79BB9E9E14744AC87F38375C3C2F181144B4E9C06F24296074F7BC48F92A97916C6DC5EA983143E9D4A2B8AA0780F682D136F7A56D6724EF53754",
                "tx_json": {
                    "Account": "rf1BiGeXwwQoi8Z2ueFYTEXSwuJYfV2Jpn",
                    "Amount": {
                        "currency": "USD",
                        "issuer": "rf1BiGeXwwQoi8Z2ueFYTEXSwuJYfV2Jpn",
                        "value": "1"
                    },
                    "Destination": "ra5nK24KXen9AHvsdFTKHSANinZseWnPcX",
                    "Fee": "10000",
                    "Flags": 2147483648,
                    "Sequence": 361,
                    "SigningPubKey": "03AB40A0490F9B7ED8DF29D246BF2D6269820A0EE7742ACDD457BEA7C7D0931EDB",
                    "TransactionType": "Payment",
                    "TxnSignature": "3045022100A7CCD11455E47547FF617D5BFC15D120D9053DFD0536B044F10CA3631CD609E502203B61DEE4AC027C5743A1B56AF568D1E2B8E79BB9E9E14744AC87F38375C3C2F1",
                    "hash": "5B31A7518DC304D5327B4887CD1F7DC2C38D5F684170097020C7C9758B973847"
                }
            }
        }
    }

tx 
`````````````````
The tx method retrieves information on a single transaction.

定义::

    POST /xrp/tx
    
请求示例::

    curl -X POST --header 'Content-Type: application/json' --header 'Accept: application/json' -d '{ \ 
                "transaction": "2DFC42DAC340AF7ED089F4A325E574A2C521C8B9CB39356F899A33595F4DB7D4" \ 
            }' 'http://localhost:8080/xrp/tx'

返回:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": {
            "result": {
                "date": 625028891,
                "Account": "rQ3fNyLjbvcDaPNS4EAJY8aT9zR3uGk17c",
                "Destination": "r4dgY6Mzob3NVq8CFYdEiPnXKboRScsXRu",
                "TransactionType": "Payment",
                "ledger_index": 50872679,
                "SigningPubKey": "039451ECAC6D4EB75E3C926E7DC7BA7721719A1521502F99EC7EB2FE87CEE9E824",
                "Amount": {
                    "currency": "CNY",
                    "value": "13550",
                    "issuer": "rJ1adrpGS3xsnQMb9Cw54tWJVFPuSdZHK"
                },
                "Fee": "10",
                "Flags": 2147483648,
                "Sequence": 15252046,
                "TxnSignature": "3045022100CFE35712AD1847092F2B2566EE5B5F7EC2A5D305B45744807470886D0DC499880220608C4AE2E80850909AAA78DE3AC68A70604722C3FFBB2263E8A0CDD9904E651E",
                "validated": true,
                "meta": {
                    "AffectedNodes": [{
                            "ModifiedNode": {
                                "LedgerIndex": "47FE64F9223D604034486F4DA7A175D5DA7F8A096952261CF8F3D77B74DC4AFA",
                                "FinalFields": {
                                    "Account": "rQ3fNyLjbvcDaPNS4EAJY8aT9zR3uGk17c",
                                    "OwnerCount": 5,
                                    "Flags": 0,
                                    "Sequence": 15252047,
                                    "Balance": "25276491030"
                                },
                                "PreviousFields": {
                                    "Sequence": 15252046,
                                    "Balance": "25276491040"
                                },
                                "PreviousTxnLgrSeq": 50872679,
                                "LedgerEntryType": "AccountRoot",
                                "PreviousTxnID": "6090785054AC237A492E2365A77ED1846AB4FA2990F3A6D4E35772EE4C0A1CF9"
                            }
                        }, {
                            "ModifiedNode": {
                                "LedgerIndex": "9C86539A6A24C8514308691D843FF3AEE9839EAFF931785FF879FBF0316B87CE",
                                "FinalFields": {
                                    "HighNode": "0000000000000000",
                                    "LowNode": "0000000000000000",
                                    "LowLimit": {
                                        "currency": "CNY",
                                        "value": "0",
                                        "issuer": "rJ1adrpGS3xsnQMb9Cw54tWJVFPuSdZHK"
                                    },
                                    "Flags": 2228224,
                                    "Balance": {
                                        "currency": "CNY",
                                        "value": "-445213.6119487387",
                                        "issuer": "rrrrrrrrrrrrrrrrrrrrBZbvji"
                                    },
                                    "HighLimit": {
                                        "currency": "CNY",
                                        "value": "1000000000",
                                        "issuer": "r4dgY6Mzob3NVq8CFYdEiPnXKboRScsXRu"
                                    }
                                },
                                "PreviousFields": {
                                    "Balance": {
                                        "currency": "CNY",
                                        "value": "-431663.6119487387",
                                        "issuer": "rrrrrrrrrrrrrrrrrrrrBZbvji"
                                    }
                                },
                                "PreviousTxnLgrSeq": 50872673,
                                "LedgerEntryType": "RippleState",
                                "PreviousTxnID": "0A583BE0EE337A59C6787EFC2C90748728AD94AFBDA6B8E0898FAD3998ED6FB8"
                            }
                        }, {
                            "ModifiedNode": {
                                "LedgerIndex": "A1DA8C3C97B3609E7FD8E662715F47B6EEF01BCA732809EFB12DC644F67F6AA8",
                                "FinalFields": {
                                    "HighNode": "0000000000000000",
                                    "LowNode": "0000000000000000",
                                    "LowLimit": {
                                        "currency": "CNY",
                                        "value": "0",
                                        "issuer": "rJ1adrpGS3xsnQMb9Cw54tWJVFPuSdZHK"
                                    },
                                    "Flags": 131072,
                                    "Balance": {
                                        "currency": "CNY",
                                        "value": "-0.15789331729",
                                        "issuer": "rrrrrrrrrrrrrrrrrrrrBZbvji"
                                    },
                                    "HighLimit": {
                                        "currency": "CNY",
                                        "value": "5",
                                        "issuer": "rQ3fNyLjbvcDaPNS4EAJY8aT9zR3uGk17c"
                                    }
                                },
                                "PreviousFields": {
                                    "Balance": {
                                        "currency": "CNY",
                                        "value": "-13550.15789331729",
                                        "issuer": "rrrrrrrrrrrrrrrrrrrrBZbvji"
                                    }
                                },
                                "PreviousTxnLgrSeq": 50872096,
                                "LedgerEntryType": "RippleState",
                                "PreviousTxnID": "FE2A3AA48A395700D1793E5E0D24F546E4DE386E0C1823C4BC01532AFD4C8116"
                            }
                        }
                    ],
                    "TransactionResult": "tesSUCCESS",
                    "TransactionIndex": 29,
                    "delivered_amount": {
                        "currency": "CNY",
                        "value": "13550",
                        "issuer": "rJ1adrpGS3xsnQMb9Cw54tWJVFPuSdZHK"
                    }
                },
                "inLedger": 50872679,
                "DestinationTag": 104398,
                "hash": "2DFC42DAC340AF7ED089F4A325E574A2C521C8B9CB39356F899A33595F4DB7D4",
                "status": "success"
            }
        }
    }
