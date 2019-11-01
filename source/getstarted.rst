开始
===========
本文档指导开发者如何使用iBlockAPI。

基本URL
`````````````````
本文中所有接口的基本URL为：

.. code-block:: bash

    https://api.iblockapi.com/

认证
``````````````````````

本文所有请求，都受API Key 保护。用户可以在网站中申请，得到一个API Key，使用示例：

.. code-block:: bash

    curl  https://api.iblockapi.com?apiKey='你的 APIKey' "https://api.iblockapi.com/btc/queryTransactionInfo?txId=6f54fcaec5553af2284da5917f52be3a82295531508886a254ff767a36ae73cd"

OR

.. code-block:: bash

    curl "https://api.iblockapi.com/btc/queryTransactionInfo?txId=6f54fcaec5553af2284da5917f52be3a82295531508886a254ff767a36ae73cd&apiKey=你的 APIKey"