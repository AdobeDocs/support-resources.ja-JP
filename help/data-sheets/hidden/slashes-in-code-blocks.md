---
title: コードブロックのスラッシュ UGP-11189
description: コードブロックのスラッシュ UGP-11189 テスト
hide: true
hidefromtoc: true
source-git-commit: 4fc9b739d18941d276b88f8799163523c8bd5f85
workflow-type: tm+mt
source-wordcount: '45'
ht-degree: 4%

---

# コードブロックのスラッシュ

1. 次のコマンドを実行します。

   ```bash
   vendor/bin/magento-patches -n status |grep "27015\|Status"
   ```

1. 次の手順

コードブロックにない

vendor/bin/magento-patches -n ステータス |grep &quot;27015\|状態&quot;

エスケープされたバックスラッシュ :

vendor/bin/magento-patches -n ステータス |grep &quot;27015&amp;bsol;|ステータス&quot;
