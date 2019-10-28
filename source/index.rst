.. BlockChainApi-docs-en documentation master file, created by
   sphinx-quickstart on Tue Oct 22 13:49:09 2019.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Rest API
========================

- 概览
    
  本文档指导开发者如何使用iBlockAPI.

- Base URL

  本文中所有接口的基本URL为：

  .. code-block:: bash

    https://api.iblockapi.com/

- 认证

  本文所有请求，都受API Key 保护。用户可以在网站中创建应用，得到一个API Key，使用示例：

  .. code-block:: bash

    curl  https://api.iblockapi.com?apiKey="Your APIKey"

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