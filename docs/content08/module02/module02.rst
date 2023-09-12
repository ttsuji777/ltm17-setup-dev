コンフィグの初期化
======================================

一旦、UCSを取得したBIG-IP (big50.f5jp.local) の全設定を消去し、デフォルト状態に戻します。

- TMSHへの移行

  
SSH等でBIG-IPのLinux OS Shellにアクセスした状態で以下のコマンドを実行します。

.. code-block:: bash

   [root@big40:Active:Standalone] config # tmsh
   root@(big40)(cfg-sync Standalone)(Active)(/Common)(tmos)# 


- デフォルトコンフィグの流し込み


| 以下のコマンドを実行します。
| (コンフィグをリセットしてよいか (y/n)をきかれるので、yとインプットします。)
| 実行すると、コンフィグレーションが初期化されます。

.. code-block:: bash

   (tmos)# load sys config default


- 保存


このデフォルトコンフィグを流し込んだ状態を保存します。

.. code-block:: bash

   (tmos)# save sys config

