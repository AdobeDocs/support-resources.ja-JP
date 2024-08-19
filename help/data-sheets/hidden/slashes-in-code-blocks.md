---
title: コードブロックのスラッシュ UGP-11189
description: コードブロックのスラッシュ UGP-11189 テスト
hide: true
hidefromtoc: true
source-git-commit: 2255dad674f1b4d456ffb50ebec9313bc4b3d7f5
workflow-type: tm+mt
source-wordcount: '46'
ht-degree: 0%

---

# コードブロックのスラッシュ

1. 次のコマンドを実行します。

   ```bash
   vendor/bin/magento-patches -n status |grep "27015\|Status"
   ```

1. コマンド（エスケープ）を実行します。

   ```bash
   vendor/bin/magento-patches -n status |grep "27015&bsol;|Status"
   ```

コードブロックにない

vendor/bin/magento-patches -n ステータス |grep &quot;27015\|状態&quot;

エスケープ：

vendor/bin/magento-patches -n ステータス |grep &quot;27015&amp;bsol;|ステータス&quot;

