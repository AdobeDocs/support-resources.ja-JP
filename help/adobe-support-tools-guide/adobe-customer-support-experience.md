---
keywords: Experience Platformのサポート；platform サポート；インテリジェントサービスのサポート；顧客 ai のサポート；アトリビューション ai のサポート；rtcdp のサポート；サポートチケットの送信；カスタマーサポート
title: Adobe Experience Cloud Customer One for Enterprise
description: Adobe カスタマーサポートエクスペリエンス
seo-description: Adobe Customer Support Experience
exl-id: 276e0862-6f7e-491e-b63e-10a50b7238c2
source-git-commit: 47bba3af6d3c2dde1c2e9a3123be7ea7037185d1
workflow-type: tm+mt
source-wordcount: '941'
ht-degree: 0%

---

# Adobe カスタマーサポートエクスペリエンス

## Experience League サポートチケット

サポートチケットが [Experience League](https://experienceleague.adobe.com/home?lang=ja#support) 経由で送信されるようになりました。 サポートチケットの送信方法については、[&#x200B; サポートチケットの送信 &#x200B;](#create-a-support-ticket-with-experience-league) の節を参照してください。

アドビでは、Adobe カスタマーサポートとのやり取りの改善に取り組んでいます。 Experience Leagueを使用して 1 つのエントリポイントに移行することで、サポートエクスペリエンスを合理化することが私たちのビジョンです。 サービスを開始すると、Adobe カスタマーサポートに簡単にアクセスでき、複数の商品をまたいだ共通システムを通じてサービス履歴をより明確に把握でき、電話、web、チャットなどを通じて 1 つのポータルでヘルプをリクエストできるようになります。

Adobe Commerce ユーザーの場合は、Adobe CommerceのExperience League サポートユーザーガイドの [&#x200B; サポートケースの送信 &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case) を参照してください。

## サポート・リクエストの提出に必要な役割 {#submit-ticket}

[Experience League](https://experienceleague.adobe.com/home?lang=ja#support) でサポートチケットを送信するには、システム管理者によってサポート管理者の役割が割り当てられている必要があります。 この役割を割り当てることができるのは、組織内のシステム管理者のみです。 製品、製品プロファイル、その他の管理者の役割は、サポート管理者の役割を割り当てることができず、サポートチケットの送信に使用される **[!UICONTROL ケースを作成]** オプションを表示することができません。 様々なタイプの管理者ロールとその使用権限について詳しくは、[&#x200B; 管理者ロール &#x200B;](admin-roles.md) を参照してください。

Commerceを使用している場合、サポートケースの操作へのアクセスを共有するプロセスは異なります。 詳しくは、Adobe CommerceのExperience League サポートユーザーガイドの [&#x200B; 共有アクセス：自分のアカウントにアクセスするための他のユーザーへの権限の付与 &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#shared-access) を参照してください。

### サポートエンティティを追加すると、組織に役割を割り当てることができます

サポート管理者ロールは、サポート関連情報にアクセスできる非管理者ロールです。 サポート管理者は、イシューレポートを表示、作成、管理できます。

管理者を追加または招待するには：

1. Admin Consoleで、**[!UICONTROL ユーザー]**/**[!UICONTROL 管理者]** を選択します。
1. **[!UICONTROL 管理者を追加]** をクリックします。
1. 名前またはメールアドレスを入力します。

   既存のユーザーを検索したり、新しいユーザーを追加したりするには、有効なメールアドレスを指定して、画面に表示される情報を入力します。

   ![&#x200B; 管理者を追加 &#x200B;](assets/admin-console-add-admin.png)

1. **[!UICONTROL 次へ]** をクリックします。 管理者ロールのリストが表示されます。

ユーザーにサポート管理者の役割を割り当てる（ユーザーがサポートに連絡できるようにする）:

1. 「**[!UICONTROL サポート管理者]**」オプションを選択します。

   ![&#x200B; 管理者権限を編集 &#x200B;](assets/edit-admin-rights.png)

1. 次の 2 つのオプションのいずれかを選択します。

   * オプション 1:**[!UICONTROL 基本サポート管理者]**。 すべてのソリューション（Marketo Engageを除く）に対してサポートへのアクセス権をユーザーに付与する場合は、このオプションを選択します。
   * オプション 2:**[!UICONTROL 製品サポート管理者]**:Marketo Engage サポートの場合は、このオプションを選択します。 サポートへのアクセスを許可するMarketo Engage インスタンスを選択します。

   ![&#x200B; 管理者権限の編集：Marketo](assets/edit-admin-rights-advanced.png)

1. 選択が完了したら、「**[!UICONTROL 保存]**」をクリックします。

ユーザーは、新しい管理者権限に関する招待状を `message@adobe.com` から受信します。

ユーザーが組織に参加するには、メールの **開始** をクリックする必要があります。 新しい管理者がメールの招待状に含まれている **開始** リンクを使用しない場合、Admin Consoleにログインすることはできません。

ログインプロセスの一環として、Adobe プロファイルをまだ持っていない場合は、設定するように求められる場合があります。 ユーザーがメールアドレスに複数のプロファイルを関連付けている場合、ユーザーは **チームに参加** を選択し（プロンプトが表示された場合）、新しい組織に関連付けられているプロファイルを選択する必要があります。

![&#x200B; 管理者権限の確認 &#x200B;](assets/admin-rights-confirmation.png)

詳しくは、管理ロールに関するドキュメントの [&#x200B; エンタープライズ管理者ロールを編集 &#x200B;](admin-roles.md#add-enterprise-role) 手順に従ってください。 この役割を割り当てることができるのは、組織のシステム管理者のみです。 管理階層について詳しくは、[&#x200B; 管理者の役割 &#x200B;](admin-roles.md) ドキュメントを参照してください。

### Experience Leagueでサポートチケットを作成します

>[!NOTE]
>
> サポートチケットを送信する前に、[Adobe ステータス &#x200B;](https://status.adobe.com/ja) サイトでAdobe システムのパフォーマンス、可用性、ソリューションの問題を確認することを検討してください。

サポートケースを送信するプロセスは、Experience League サポートプラットフォームと直接統合されるようになりました。 これは、資格のある顧客に対してより多くのパーソナライゼーションと使いやすさを提供するように最近再設計されたセルフサービスポータルです。

1. [Experience League](https://experienceleague.adobe.com/home?lang=ja#support) を使用してチケットを作成するには、上部ナビゲーションにある「**[!UICONTROL サポート]**」タブを選択します。
   ![&#x200B; 「Experience League サポート」タブ &#x200B;](./assets/experience-league-support-tab.png)
1. サポートホームページから、開いているサポートケースに簡単に移動したり、新しいケースをログに記録したり、上位のサポート記事を表示したり、追加の学習ソースにアクセスしたりできます。
   ![Experience League サポートリソース &#x200B;](./assets/experience-league-support-resources.png)
1. ケースを送信するには、「**[!UICONTROL サポートチケットを開く]**」を選択します。 また、サイドバーメニューの **[!UICONTROL チケットを開く]** オプションを選択します。


### サポートチケットを入力

1. **[!UICONTROL サポートチケットを開く]** を選択すると、ケース作成ページに移動します。このページで、商品名（Audience Manager、Campaign、Target など）、**[!UICONTROL ケースのタイトル]**、および **[!UICONTROL ケースの説明]** を入力できます。

   ![Experience League オープンチケット &#x200B;](./assets/experience-league-open-ticket.png)

   トラブルシューティングプロセスを迅速に進めるには、「**[!UICONTROL ケースの説明]**」フィールドに次の情報を追加します。

   * 問題の説明をクリア
   * 再現手順
   * ビジネス上の影響に関する声明
   * これは新しい実装/機能/開発ですか？
   * プロセスが機能したのはいつですか？
   * 実行したトラブルシューティング手順
   * 関連するログデータ
   * バージョン番号
   * ビルド情報（該当する場合）
   * 重要な識別子


1. ソリューションを選択する際には、次の質問が表示され、一部のソリューションには追加のフィールドがあります。

   * サポート・リクエストの優先度（低、Medium、高、重大）
   * ビジネスへの影響
   * お客様のタイムゾーン （アメリカ、EMEA、APAC）

   ケースの優先度とビジネスへの影響がサポートの応答時間にどのように影響するかについて詳しくは、成功計画リソースに関するドキュメントの [&#x200B; サポートの初期応答時間のターゲット &#x200B;](https://experienceleague.adobe.com/ja/docs/support-resources/data-sheets/overview#targeted-initial-response-times-for-support) を参照してください。

![Experience League チケットの優先度 &#x200B;](./assets/experience-league-ticket-priority.png)

>[!TIP]
>
> **[!UICONTROL ケースを作成]** オプションまたは **[!UICONTROL サポート]** タブが表示されない場合は、システム管理者に連絡してサポート管理者の役割を割り当てる必要があります。








>[!NOTE]
>
> 問題が原因で実稼動システムが停止したり重大な中断が発生した場合は、すぐにサポートを受けるための電話番号が提供されます。




<!--

## What About the Legacy Systems?

New Tickets/Cases will no longer be able to be submitted in legacy systems as of May 11th.  The [Admin Console](https://adminconsole.adobe.com/) will be used to submit new tickets/cases.

### Existing Tickets/Cases

* Between May 11th and May 20th the legacy systems will remain available to work existing tickets/cases to completion.
* Beginning May 20th the support team will migrate remaining open cases from the legacy systems to the new support experience.  You will receive an email notification regarding how to contact support to continue to work these cases.
-->
