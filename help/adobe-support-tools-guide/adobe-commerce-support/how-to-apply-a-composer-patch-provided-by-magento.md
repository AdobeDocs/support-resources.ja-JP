---
title: Adobeが提供するコンポーザーパッチの適用方法
description: この記事では、Adobe Commerce オンプレミス、Adobe Commerce オンクラウドインフラストラクチャ、およびMagento Open Sourceにコンポーザーパッチを適用する方法について説明します。
feature: Best Practices, Compliance, Console
solution: Commerce
feature-set: Commerce
exl-id: 66d8df60-4c4a-49ef-8107-986e10d6e289
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: cdfd3bc1-dc23-5cf0-b965-d3c0c55cde67
    internal-label: Best Practices
  - id: b5f00040-57a0-4a6d-a39e-383b1936c2c9
    internal-label: Compliance
  - id: 125c1f49-aefd-5f34-a252-288937f95f6b
    internal-label: Marketing Tools
subfeature_v2:
  - id: c4af0798-d497-5e6b-8380-19812c26d00a
    internal-label: Console
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
source-git-commit: a4ba265c36bd4ba6c7c563879834f2c59fdc58a4
workflow-type: tm+mt
source-wordcount: '225'
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

Cloud プロジェクトへのパッチの適用について詳しくは、開発者ドキュメントの「[&#x200B; パッチを適用](https://experienceleague.adobe.com/ja/docs/commerce-cloud-service/user-guide/develop/upgrade/apply-patches)」を参照してください。

## Adobe Commerce オンプレミスおよびMagento Open Sourceにコンポーザーパッチを適用する方法 {#commerce}

1. パッチをAdobe Commerce オンプレミスまたはMagento Open Source ルートディレクトリにアップロードします。
1. 次のSSH コマンドを実行します。

   ```bash
   patch -p1 < %patch_name%.composer.patch
   ```

   （上記のコマンドが機能しない場合は、`-p1`ではなく`-p2`を使用してみてください）

1. 変更を反映するには、**[!UICONTROL システム]**/**[!UICONTROL キャッシュ管理]**&#x200B;の下の管理者のキャッシュを更新します。
