.. BlockChainApi-docs-en documentation master file, created by
   sphinx-quickstart on Tue Oct 22 13:49:09 2019.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Rest API
========================

基本URL
`````````````````
本文中所有接口的基本URL为：

.. code-block:: bash

    https://api.iblockapi.com/swagger-ui.html

认证
``````````````````````

本文所有请求，都受API Key 保护。用户可以在网站中申请，得到一个API Key，使用示例：

.. code-block:: bash

    curl  https://api.iblockapi.com?apiKey='你的 APIKey' "https://api.iblockapi.com/btc/queryTransactionInfo?txId=6f54fcaec5553af2284da5917f52be3a82295531508886a254ff767a36ae73cd"

OR

.. code-block:: bash

    curl "https://api.iblockapi.com/btc/queryTransactionInfo?txId=6f54fcaec5553af2284da5917f52be3a82295531508886a254ff767a36ae73cd&apiKey=你的 APIKey"

.. toctree::
   :maxdepth: 2

   getstarted
   bitcoin
   bitcoinabc
   cardano
   dash
   eos
   ethereum
   ethereumclassic
   libra
   litecoin
   monero
   neo
   stellar
   telegram
   tron
   zcash
   ripple