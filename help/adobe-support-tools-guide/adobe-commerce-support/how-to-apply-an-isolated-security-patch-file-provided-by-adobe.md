---
title: Adobeが提供する分離パッチの適用方法
description: この記事では、Adobe Commerce オンプレミス、Adobe Commerce on Cloud インフラストラクチャ、およびMagento Open Sourceに個別パッチを適用する方法について説明します。
feature: Best Practices, Compliance, Console
solution: Commerce
feature-set: Commerce
autotag-review: '2026-08-19T13:22:21.768Z'
TQID: 'https://experienceleague.adobe.com/tmaNqB6uOX2ukmfxQvcqFvYwm2UyO6USzb7t8hFQM1A'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: b5f00040-57a0-4a6d-a39e-383b1936c2c9
source-git-commit: 45b00b9b0d2ceb422747c0a4a34f060f33ab127b
workflow-type: tm+mt
source-wordcount: 219
ht-degree: 0%

---

# Adobeが提供する分離パッチの適用方法

この記事では、Adobe Commerce オンプレミス、Adobe Commerce on Cloud インフラストラクチャ、およびMagento Open Sourceに個別パッチを適用する方法について説明します。

>[!WARNING]
>
>ステージング/統合環境にパッチを適用してテストしてから、実稼動環境に適用することを強くお勧めします。 また、操作の前に最新のバックアップを作成することをお勧めします。

## Adobe Commerce on Cloud インフラストラクチャに個別パッチを適用する方法 {#cloud}

1. プロジェクト ルートに`m2-hotfixes`という名前のディレクトリがない場合は、ディレクトリを作成してください。
1. `%patch_name%.patch` ファイルを`m2-hotfixes` ディレクトリにコピーします。
1. コードの変更を追加、コミット、プッシュします。

   ```git
   git add -A
   ```

   ```git
   git commit -m "Apply %patch_name%.patch patch"
   ```

   ```git
   git push origin
   ```

Cloud プロジェクトへのパッチの適用について詳しくは、[&#x200B; パッチの適用](https://experienceleague.adobe.com/ja/docs/commerce-on-cloud/user-guide/develop/upgrade/apply-patches)を参照してください。

## Adobe Commerce オンプレミスとMagento Open Sourceに個別パッチを適用する方法 {#commerce}

1. パッチをAdobe Commerce オンプレミスまたはMagento Open Source ルートディレクトリにアップロードします。
1. 次のSSH コマンドを実行します。

   ```bash
   patch -p1 < %patch_name%.patch
   ```

   （上記のコマンドが機能しない場合は、`-p1`ではなく`-p2`を使用してみてください）

1. 変更を反映するには、**[!UICONTROL システム]**/**[!UICONTROL キャッシュ管理]**&#x200B;の下の[!UICONTROL 管理者]のキャッシュを更新します。
