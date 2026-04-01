---
title: Global Admin Consoleでの製品プロファイルの管理
description: グローバル管理者がGlobal Admin Consoleで製品プロファイルを追加、編集、削除する方法について説明します。
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
product_v2:
  - id: f7bdf6be-dd3b-4d2d-ac52-0e62ed0d3102
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
exl-id: 6a0b2d9f-9e02-428c-a2be-bc457230f7e0
source-git-commit: 74d2dd4eb999f91172eec4c3b5690e1e8b8bd293
workflow-type: tm+mt
source-wordcount: 580
ht-degree: 1%

---

# Global Admin Consoleでの製品プロファイルの管理

**適用先：** Enterprise


## 概要

グローバル管理者は、[Global Admin Console](https://global-admin-console.adobe.com/)で製品プロファイルを追加、編集、削除できます。

>[!NOTE]
>
>[Global Admin Console](https://helpx.adobe.com/jp/enterprise/global-admin-console/adopt-global-administration.html#request-access)で、組織を選択し、**[!UICONTROL 製品]**&#x200B;に移動します。 製品プロファイルを使用して、製品に対するすべてのサービスまたは選択したサービスをアクティブ化できます。

標準のAdmin Consoleと同様に、Product Profilesを使用すると、組織内の商品の使用状況を微調整できます。 また、管理者（**[!UICONTROL 製品プロファイル管理者]**）を製品プロファイルに割り当てることもできます。 これらの管理者は、管理する製品プロファイルにエンドユーザーを追加できます。

製品プロファイルを管理するには、製品を選択します。 製品プロファイルを追加、編集、削除するためのコントロールが表示されます。

>[!NOTE]
>
>一部の商品については、Global Admin Consoleで商品プロファイルを作成または編集することはできません。 そのような場合は、代わりに[Admin Console](https://helpx.adobe.com/jp/enterprise/using/admin-console.html)を使用してください。

## 製品プロファイルの追加

1. [Global Admin Console](https://global-admin-console.adobe.com/)で、編集する組織を選択し、**[!UICONTROL 製品]** タブに移動します。
1. 製品プロファイルを追加する製品を選択します。
1. 「**[!UICONTROL プロファイルを追加]**」を選択します。
1. **[!UICONTROL プロファイルを追加]** ダイアログボックスで、次の詳細を入力します。

   | フィールド | 説明 |
   |---|---|
   | **[!UICONTROL 名前]** | 組織内の製品プロファイルの一意の名前。他の製品プロファイルおよびユーザーグループとは異なります。 |
   | **[!UICONTROL 割り当て]** | このプロファイルに割り当てられたライセンスの目標数。 |
   | **[!UICONTROL ユーザーグループ]** | ドロップダウンから選択するか、ユーザーグループ名を入力します。 ユーザーグループがまだ存在しない場合は、最初に「[**[!UICONTROL &#x200B; ユーザーグループ &#x200B;]**](https://helpx.adobe.com/jp/enterprise/global-admin-console/manage-user-groups.html)」タブから作成します。 |
   | **[!UICONTROL 管理者]** | ドロップダウンから選択するか、管理者のメールアドレスを入力します。 管理者がまだ存在しない場合は、[**[!UICONTROL 管理者&#x200B;]**](https://helpx.adobe.com/jp/enterprise/global-admin-console/manage-administrators.html) タブを使用して最初に作成します。 |

   指定された[!UICONTROL &#x200B; ユーザーグループ &#x200B;]には、製品プロファイルが割り当てられます。 指定された管理者は&#x200B;**[!UICONTROL 製品プロファイル管理者]**&#x200B;になります。この管理者は、関連する組織のAdobe Admin Consoleを介してプロファイルを管理できます。

   ![&#x200B; プロファイルを追加](./assets/manage-product-profiles_add-profile.png)

1. **[!UICONTROL 通知]** トグルを使用して、メール通知を有効または無効にします。 有効にすると、プロファイルにユーザーが追加または削除されたときに、ユーザーにメールで通知されます。
1. 個々の&#x200B;**[!UICONTROL サービス]** トグルを使用して、製品プロファイルの特定のサービスを有効または無効にします。 詳しくは、[製品プロファイルのサービスの有効化/無効化](https://helpx.adobe.com/jp/enterprise/using/enable-disable-services.html)を参照してください。
1. 「**[!UICONTROL 保存]**」を選択します。
1. 組織の編集が完了したら、「**[!UICONTROL 保留中の変更を確認]**」を選択します。 レビュー後、**[!UICONTROL 変更を送信]**&#x200B;から[実行](https://helpx.adobe.com/jp/enterprise/global-admin-console/execute-jobs.html)を選択します。

## 製品プロファイルの編集

1. 編集する組織を選択し、**[!UICONTROL 製品]** タブに移動して、製品を選択します。
1. 関連する製品プロファイルの「**[!UICONTROL 詳細オプション]** ![詳細オプション &#x200B;](./assets/manage-product-profiles_more-options.png)」アイコンを選択し、「**[!UICONTROL プロファイルを編集]**」を選択します。
1. 必要に応じて製品プロファイルの詳細を更新し、**[!UICONTROL 保存]**&#x200B;を選択します。
1. 組織の編集が完了したら、「**[!UICONTROL 保留中の変更を確認]**」を選択します。 レビュー後、**[!UICONTROL 変更を送信]**&#x200B;から[実行](https://helpx.adobe.com/jp/enterprise/global-admin-console/execute-jobs.html)を選択します。

## 製品プロファイルの削除

>[!WARNING]
>
> 製品プロファイルを削除すると、そのプロファイルのメンバーであるか、そのプロファイルに添付されたユーザーグループに属しているすべてのユーザーの製品アクセスが削除されます。

1. 編集する組織を選択し、**[!UICONTROL 製品]** タブに移動して、製品を選択します。
1. 関連する製品プロファイルの「**[!UICONTROL 詳細オプション]** ![詳細オプション &#x200B;](./assets/manage-product-profiles_more-options.png)」アイコンを選択し、「**[!UICONTROL プロファイルを削除]**」を選択します。
1. 確認ダイアログボックスで「**[!UICONTROL OK]**」を選択します。
1. 組織の編集が完了したら、「**[!UICONTROL 保留中の変更を確認]**」を選択します。 レビュー後、**[!UICONTROL 変更を送信]**&#x200B;から[実行](https://helpx.adobe.com/jp/enterprise/global-admin-console/execute-jobs.html)を選択します。


## 関連トピックス

- [&#x200B; グローバル管理の導入](https://helpx.adobe.com/jp/enterprise/global-admin-console/adopt-global-administration.html)
- [管理者の管理](https://helpx.adobe.com/jp/enterprise/global-admin-console/manage-administrators.html)
- [&#x200B; ユーザーグループの管理](https://helpx.adobe.com/jp/enterprise/global-admin-console/manage-user-groups.html)
- [製品を子組織に割り当て](https://helpx.adobe.com/jp/enterprise/global-admin-console/allocate-products.html)
- [保留中のジョブの実行](https://helpx.adobe.com/jp/enterprise/global-admin-console/execute-jobs.html)
- [&#x200B; サービスを有効/無効にする](https://helpx.adobe.com/jp/enterprise/using/enable-disable-services.html)
- [Admin Consoleの概要](https://helpx.adobe.com/jp/enterprise/using/admin-console.html)
