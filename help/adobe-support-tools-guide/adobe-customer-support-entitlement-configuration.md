---
title: Adobe カスタマーサポートの使用権限の設定
description: Adobeのお客様がAdmin Consoleでサポートエンタイトルメントを設定および管理して、サポートリソースにアクセスし、問題を送信し、ケースアクティビティを管理する方法。
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: 75b0e812-da38-46af-94b6-7b7db8954be3
source-git-commit: e6379bd22238091d6f6d26d2aa3e515ce7c61e5a
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%

---

# Adobe カスタマーサポートの使用権限の設定

組織のサポートエンタイトルメントを設定するには、まずAdmin Consoleを通じてユーザーを追加または招待します。

## 組織へのサポート使用権限の役割の追加

**[!UICONTROL サポート管理者]**&#x200B;の役割は、サポートに関する情報にアクセスできる管理者以外の役割です。 **[!UICONTROL サポート管理者]**&#x200B;は、問題レポートを表示、作成、管理できます。

管理者を追加または招待するには：

1. Admin Consoleで、**[!UICONTROL Users]** > **[!UICONTROL Administrators]**&#x200B;を選択します。
1. 「**[!UICONTROL 管理者を追加]**」をクリックします。
1. 名前または電子メールアドレスを入力します。

   有効なメールアドレスを指定し、画面に情報を入力することで、既存のユーザーを検索したり、新しいユーザーを追加したりできます。

   ![管理者を追加](assets/admin-console-add-admin.png)

1. 「**[!UICONTROL 次へ]**」をクリックします。 管理者の役割のリストが表示されます。

**[!UICONTROL サポート管理者]**&#x200B;の役割をユーザーに割り当てるには（ユーザーがサポートに問い合わせできるようにする）:

1. 「**[!UICONTROL サポート管理者]**」オプションを選択します。

   ![管理者権限の編集](assets/edit-admin-rights.png)

1. 次の2つのオプションのいずれかを選択します。

   * オプション 1: **[!UICONTROL 基本サポート管理者]**。 すべてのソリューション（Marketo Engageを除く）に対するユーザーサポートへのアクセス権を付与する場合は、このオプションを選択します。
   * オプション 2: **[!UICONTROL 製品サポート管理者]**: Marketo Engage サポートにこのオプションを選択します。 ユーザーサポートへのアクセス権を付与するMarketo Engage インスタンスを選択します。

   ![管理者権限の編集Marketo](assets/edit-admin-rights-advanced.png)

1. 選択したら、**[!UICONTROL 保存]**&#x200B;をクリックします。

ユーザーは、新しい管理者権限に関する招待メールを`message@adobe.com`から受け取ります。

ユーザーが組織に参加するには、メール内の&#x200B;**[!UICONTROL 開始]**&#x200B;をクリックする必要があります。 新しい管理者が電子メールの招待状に「**[!UICONTROL はじめに]**」リンクを使用しない場合、Admin Consoleにサインインできません。

サインインプロセスの一環として、Adobe プロファイルを既にお持ちでない場合は、設定するように求められる場合があります。 ユーザーがメールアドレスに複数のプロファイルを関連付けている場合、ユーザーは&#x200B;**[!UICONTROL チームに参加]** （プロンプトが表示された場合）を選択し、新しい組織に関連付けられているプロファイルを選択する必要があります。

![管理者権限の確認](assets/admin-rights-confirmation.png)

詳細については、管理者役割ドキュメントの「[ エンタープライズ管理者の役割を編集](adobe-admin-console/admin-roles.md#edit-enterprise-admin-role)手順」を参照してください。 この役割を割り当てることができるのは、組織のシステム管理者のみです。 管理階層について詳しくは、[管理ロール ](adobe-admin-console/admin-roles.md)のドキュメントを参照してください。
