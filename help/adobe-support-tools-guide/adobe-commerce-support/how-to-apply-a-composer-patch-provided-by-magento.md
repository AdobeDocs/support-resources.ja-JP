---
title: Adobeが提供するコンポーザーパッチの適用方法
description: この記事では、Adobe Commerce オンプレミス、Adobe Commerce オンクラウドインフラストラクチャ、およびMagento Open Sourceにコンポーザーパッチを適用する方法について説明します。
feature: Best Practices, Compliance, Console
solution: Commerce
feature-set: Commerce
source-git-commit: fa46bb7187c55a0c7d75930868c74bf8ba072c41
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---

# Adobeが提供するコンポーザーパッチの適用方法

この記事では、Adobe Commerce オンプレミス、Adobe Commerce オンクラウドインフラストラクチャ、およびMagento Open Sourceにコンポーザーパッチを適用する方法について説明します。

>[!WARNING]
>
>ステージング/統合環境にパッチを適用してテストしてから、実稼動環境に適用することを強くお勧めします。 また、操作の前に最新のバックアップを作成することをお勧めします。

## Adobe Commerce on cloud infrastructureにコンポーザーパッチを適用する方法 {#cloud}

1. プロジェクト ルートに`m2-hotfixes`という名前のディレクトリがない場合は、ディレクトリを作成してください。
1. `%patch_name%.composer.patch` ファイルを`m2-hotfixes` ディレクトリにコピーします。
1. コードの変更を追加、コミット、プッシュします。

   ```git
   git add -A
   ```

   ```git
   git commit -m "Apply %patch_name%.composer.patch patch"
   ```

   ```git
   git push origin
   ```

Cloud プロジェクトへのパッチの適用について詳しくは、開発者ドキュメントの「[ パッチを適用](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/upgrade/apply-patches)」を参照してください。

## Adobe Commerce オンプレミスおよびMagento Open Sourceにコンポーザーパッチを適用する方法 {#commerce}

1. パッチをAdobe Commerce オンプレミスまたはMagento Open Source ルートディレクトリにアップロードします。
1. 次のSSH コマンドを実行します。

   ```bash
   patch -p1 < %patch_name%.composer.patch
   ```

   （上記のコマンドが機能しない場合は、`-p2`ではなく`-p1`を使用してみてください）

1. 変更を反映するには、**[!UICONTROL システム]**/**[!UICONTROL キャッシュ管理]**&#x200B;の下の管理者のキャッシュを更新します。