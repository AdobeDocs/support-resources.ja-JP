---
title: Global Admin Consoleでのポリシーテンプレートの管理
description: グローバル管理者が、Global Admin Consoleに保存されている組織から直接または間接的に、任意の子組織にポリシーテンプレートを適用する方法について説明します。
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
product_v2:
  - id: f7bdf6be-dd3b-4d2d-ac52-0e62ed0d3102
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: cf30f2a656ccb28b678ea6fcd8e4d56d7c8a8fb4
workflow-type: tm+mt
source-wordcount: 705
ht-degree: 0%

---

# Global Admin Consoleでのポリシーテンプレートの管理

**適用先：** Enterprise

グローバル管理者が、Global Admin Consoleに保存されている組織から直接または間接的に、任意の子組織にポリシーテンプレートを適用する方法について説明します。

>[!NOTE]
>
>[Global Admin Console](https://helpx.adobe.com/jp/enterprise/global-admin-console/adopt-global-administration.html)で、編集する組織を選択し、「**ポリシーテンプレート**」タブに移動して、セットアップを合理化し、組織全体で一貫性のあるポリシー管理を容易にします。
>
> [Global Admin Consoleにログイン &#x200B;](https://global-admin-console.adobe.com/)

## ポリシーテンプレートの機能

ポリシーテンプレートは、組織とともに保存され、その組織のすべてのグローバル管理者に表示されます。 適用すると、ポリシーテンプレートのエントリは各組織で個別に設定されます。 ポリシーテンプレートが組織に適用されると、ポリシーテンプレートの各エントリが組織のポリシーに適用され、既存のポリシー値が置き換えられます。

### ロックされたポリシー動作

ロックされたポリシーの更新は、更新を適用するユーザーが、更新中のポリシーの「**[!UICONTROL ロック済み]**」アイコンで示されている組織のグローバル管理者である場合にのみ実行されます。

テンプレートを適用するユーザーがポリシーのロックを解除する権限を持っている場合、ポリシーロックは適用されたテンプレートの値（ロック済みまたはロック解除）を取得します。 テンプレートがロックをそのまま残すことを示している場合、ポリシー内のロックの値は以前と同じままになります。

### 保存に関する重要なメモ

>[!NOTE]
>
>Global Admin Consoleで行われた他の変更とは異なり、ポリシーテンプレートの編集は、**[!UICONTROL 保留中の変更のレビュー –]**&#x200B;のプロセスを経ることなく、すぐに有効になります。 ただし、ポリシーテンプレートが適用されている組織で保留中の変更を実装するには、[送信](https://helpx.adobe.com/jp/enterprise/global-admin-console/execute-jobs.html)が必要です。

## ポリシーテンプレートの作成

1. [Global Admin Console](https://global-admin-console.adobe.com/)で、編集する組織を選択し、「**[!UICONTROL ポリシーテンプレート]**」タブに移動します。
1. 「**[!UICONTROL テンプレートを作成]**.<br>」を選択
   ![写真1](./assets/DXSKB-3209-1-ga_14.png)
   <br>
1. **[!UICONTROL ポリシーテンプレートを作成]** ダイアログボックスで、ポリシーテンプレートの&#x200B;**name**&#x200B;と&#x200B;**description**&#x200B;を入力します。<br> ポリシーテンプレートの名前は、最大100文字までです。
1. テンプレートに含めるポリシーを選択します。
1. 選択したポリシーの値を設定します（以下の[&#x200B; ポリシー値の設定](#setting-policy-values)を参照）。
1. 「**保存**」を選択します。

### ポリシー値の設定 {#setting-policy-values}

テンプレートに含まれる各ポリシーについて、次の2つの設定を行います。

* **許可/許可されていません：** スライダーを目的の値に設定します。 [&#x200B; ポリシーの詳細](https://helpx.adobe.com/jp/enterprise/global-admin-console/update-policies.html#policy-details)について説明します。
* **ロック値：**&#x200B;次のいずれかのオプションを使用して、ポリシーのロック状態を変更します。
   * **ロック** — テンプレートの適用後にポリシーがロックされます。
   * **ロック解除** — テンプレートを適用すると、ポリシーがロック解除されます。
   * **そのまま保持** — ポリシーのロック状態は、テンプレートが適用される前と同じままになります。<br>
     ![写真2](./assets/DXSKB-3209-2-policy-template.png)
<br>

## 組織へのテンプレートの適用

1. [Global Admin Console](https://global-admin-console.adobe.com/)で、編集する組織を選択し、「**[!UICONTROL ポリシーテンプレート]**」タブに移動します。
1. 関連するポリシーテンプレートの&#x200B;**[!UICONTROL 詳細オプション]** ![詳細オプション &#x200B;](./assets/manage-product-profiles_more-options.png) アイコンを選択し、**[!UICONTROL 組織にテンプレートを適用]**&#x200B;を選択します。<br>
   ![写真3](./assets/DXSKB-3209-3-ga_15.png)
   <br>
1. テンプレートを適用する組織を選択します。 複数の組織を選択できます。<br>
   ![写真4](./assets/DXSKB-3209-4-bulk-apply-template.png)
   <br>
1. 「**[!UICONTROL テンプレートを適用]**」を選択します。
1. ポリシーテンプレートが適用されている組織で保留中の変更を実装するには、**[!UICONTROL 保留中の変更を確認]**&#x200B;を選択します。 レビュー後、**[!UICONTROL 変更を送信]**&#x200B;から[実行](https://helpx.adobe.com/jp/enterprise/global-admin-console/execute-jobs.html)を選択します。

選択した組織のすべてのポリシー値が既にテンプレートの値と一致している場合、変更が行われなかったことを知らせるメッセージが表示されます。 また、他に保留中の編集がない場合、**[!UICONTROL 保留中の変更のレビュー]**&#x200B;は有効になっていません。

## テンプレートの編集

1. [Global Admin Console](https://global-admin-console.adobe.com/)で、編集する組織を選択し、「**[!UICONTROL ポリシーテンプレート]**」タブに移動します。
1. 関連するテンプレートの&#x200B;**[!UICONTROL 詳細オプション]** アイコン ![詳細オプション &#x200B;](./assets/manage-product-profiles_more-options.png)を選択し、**[!UICONTROL テンプレートを編集]**&#x200B;を選択します。<br>
   ![写真5](./assets/DXSKB-3209-5-ga_15-1.png)
   <br>
1. ポリシーテンプレートを更新し、**[!UICONTROL 今すぐ更新]**&#x200B;を選択します。
1. ポリシーテンプレートが適用されている組織で保留中の変更を実装するには、**[!UICONTROL 保留中の変更を確認]**&#x200B;を選択します。 レビュー後、**[!UICONTROL 変更を送信]**&#x200B;から[実行](https://helpx.adobe.com/jp/enterprise/global-admin-console/execute-jobs.html)を選択します。

## テンプレートの削除

1. [Global Admin Console](https://global-admin-console.adobe.com/)で、編集する組織を選択し、「**[!UICONTROL ポリシーテンプレート]**」タブに移動します。
1. 関連するテンプレートの&#x200B;**[!UICONTROL 詳細オプション]** ![詳細オプション &#x200B;](./assets/manage-product-profiles_more-options.png) アイコンを選択し、**[!UICONTROL テンプレートを削除]**.<br>を選択します
   ![写真6](./assets/DXSKB-3209-6-ga_15-2.png)
   <br>
1. 表示されるダイアログボックスで「*はい*」を選択します。
