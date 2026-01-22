---
keywords: Experience Platformのサポート；platform サポート；インテリジェントサービスのサポート；顧客 ai のサポート；アトリビューション ai のサポート；rtcdp のサポート；サポートチケットの送信；カスタマーサポート
title: Adobe Experience Cloud Customer One for Enterprise
description: Adobe カスタマーサポートエクスペリエンス
seo-description: Adobe Customer Support Experience
exl-id: 276e0862-6f7e-491e-b63e-10a50b7238c2
source-git-commit: 361a370c64197b77ef5437efecfc41f5bd72a16e
workflow-type: tm+mt
source-wordcount: '1163'
ht-degree: 0%

---

# Adobe カスタマーサポートエクスペリエンス

## Experience League サポートチケット

サポートチケットが [Experience League](https://experienceleague.adobe.com/home#support) 経由で送信されるようになりました。 サポートチケットの送信方法については、[&#x200B; サポートチケットの送信 &#x200B;](#create-a-support-ticket-with-experience-league) の節を参照してください。

アドビでは、Adobe カスタマーサポートとのやり取りの改善に取り組んでいます。 Experience Leagueを使用して 1 つのエントリポイントに移行することで、サポートエクスペリエンスを合理化することが私たちのビジョンです。 サービスを開始すると、Adobe カスタマーサポートに簡単にアクセスでき、複数の商品をまたいだ共通システムを通じてサービス履歴をより明確に把握でき、電話、web、チャットなどを通じて 1 つのポータルでヘルプをリクエストできるようになります。

Adobe Commerce ユーザーの場合は、Adobe CommerceのExperience League サポートユーザーガイドの [&#x200B; サポートケースの送信 &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case) を参照してください。

## サポート・リクエストの提出に必要な役割 {#submit-ticket}

[Experience League](https://experienceleague.adobe.com/home#support) でサポートチケットを送信するには、システム管理者によってサポート管理者の役割が割り当てられている必要があります。 この役割を割り当てることができるのは、組織内のシステム管理者のみです。 製品、製品プロファイル、その他の管理者の役割は、サポート管理者の役割を割り当てることができず、サポートチケットの送信に使用される **[!UICONTROL ケースを作成]** オプションを表示することができません。 様々なタイプの管理者ロールとその使用権限について詳しくは、[&#x200B; 管理者ロール &#x200B;](admin-roles.md) を参照してください。

Commerceを使用している場合、サポートケースの操作へのアクセスを共有するプロセスは異なります。 詳しくは、Adobe CommerceのExperience League サポートユーザーガイドの [&#x200B; 共有アクセス：自分のアカウントにアクセスするための他のユーザーへの権限の付与 &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#shared-access) を参照してください。

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
> サポートチケットを送信する前に、[Adobe ステータス &#x200B;](https://status.adobe.com/ja) サイトでAdobe システムのパフォーマンス、可用性および既知の問題を確認してください。

Experience Leagueは、資格のあるお客様にパーソナライズされたサポートと使いやすいエクスペリエンスを提供するように設計されたセルフサービスサポートポータルです。

1. [Experience League](https://experienceleague.adobe.com/home#support) でチケットを作成するには、上部ナビゲーションで「**[!UICONTROL サポート]**」タブを選択します。

   ![&#x200B; 「Experience League サポート」タブ &#x200B;](./assets/experience-league-support-tab.png)

1. **[!UICONTROL ホーム]** メニューから **[!UICONTROL サポートチケットを開く]**、**[!UICONTROL ケースを表示して管理する]**、**[!UICONTROL コールバックをリクエスト]**、または追加の学習リソースにアクセスできます。

   ![Experience League ホームメニュー &#x200B;](./assets/home-menu.png)

1. ケースを送信するには、「**[!UICONTROL サポートチケットを開く]**」を選択します。 サイドバーメニューで **[!UICONTROL チケットを開く]** を選択することもできます。

   ![Experience League がチケットをオープンする &#x200B;](./assets/open-support-ticket.png)

### サポートチケットを入力

**[!UICONTROL サポートチケットを開く]** または **[!UICONTROL チケットを開く]** を選択すると、ケース作成ページが表示されます。

フォームでは、ガイド付きの複数ステップのワークフローを使用します。

* 該当するAdobe製品を選択します。
* 問題の説明
* システムと環境の詳細を入力
* 影響と緊急度を示す
* 連絡先情報の確認
* 詳細を確認して送信します。

次の手順に従って、サポートチケットを作成します。

1. 製品名をクリックして該当する製品を選択し、&lbrack; 次へ **[!UICONTROL をクリックし]** す。

   ![Experience League 製品の選択 &#x200B;](./assets/select-product.png)

1. 「**[!UICONTROL イシューの詳細]**」セクションでは、ケースのタイトルを入力し、イシューを説明し、再現手順を指定します。

   ![Experience League 問題の詳細 &#x200B;](./assets/issue-details.png)

   次のような詳細を含めます。

   * 何をしようとしているか
   * 期待どおりに動作していない項目
   * 最近の環境の変更
   * 既に実行した手順

   イシューの詳細を入力すると、Experience Leagueのフォームの横のパネルに AI を利用したレコメンデーションが表示されます。 推奨事項は次のとおりです。

   * 関連するドキュメントまたは既知のソリューションを提案
   * 問題が既に対処されているかどうかを確認するのに役立ちます
   * よくある問題に関してケースを送信する必要性を軽減

   ケース作成プロセスを中断することなく、パネルが表示されます。 レコメンデーションはいつでも確認でき、必要に応じてケースの送信を続行できます。

   ![Experience League 問題の詳細 &#x200B;](./assets/ai-recommendations.png)

1. **[!UICONTROL 次へ]** をクリックします。

1. 「**[!UICONTROL システム情報]**」セクションで、環境を選択して「**[!UICONTROL 次へ]**」をクリックします。

   >[!NOTE]
   >
   > 選択した製品に応じて、追加のフィールドが表示される場合があります。 これらのフィールドには、イシューが発生する環境に関する詳細が含まれています。

   ![Experience League システム情報 &#x200B;](./assets/system-information.png)

1. 「**[!UICONTROL 影響]**」セクションで、以下を選択します。
   * サポート案件の優先度（P4 - マイナー、P3 – 重要、P2 – 緊急、P1 – 重大）
   * ビジネス・インパクト（小規模、Medium、大規模）

   ![Experience League の影響の詳細 &#x200B;](./assets/impact.png)

   ケースの優先度とビジネスへの影響がサポートの応答時間にどのように影響するかについて詳しくは、成功プランリソースに関するドキュメントの [&#x200B; サポートのターゲット化された初期応答時間 &#x200B;](https://experienceleague.adobe.com/en/docs/support-resources/data-sheets/overview#targeted-initial-response-times-for-support) を参照してください。

1. 「**[!UICONTROL 次へ]**」をクリックします。

1. **[!UICONTROL 連絡先情報]** セクションで、タイムゾーンを選択し、電話番号を入力し、ウォッチャーを追加し、必要に応じてファイルを添付して、**[!UICONTROL 次へ]** をクリックします。

   ![Experience League の連絡先情報 &#x200B;](./assets/contact-information.png)

1. 「**[!UICONTROL レビューして送信]**」セクションで、ケースの詳細をレビューし、「**[!UICONTROL 送信]**」をクリックします。

   ![Experience League のレビューと送信 &#x200B;](./assets/review-and-submit.png)

   **[!UICONTROL レビューと送信]** 手順では、入力したすべての情報の概要を示し、次の操作を行うことができます。

   * すべてのケースの詳細を 1 か所でレビュー
   * 前のステップに戻って編集します
   * 進行状況を失わずにレビューの概要に戻る

送信後：

* ケースはExperience Leagueに記録されます
* 更新を追跡し、ポータルを通じてサポートと通信できます
* Adobe サポートは、提供された優先度と影響に基づいて対応します

>[!TIP]
>
> 「**[!UICONTROL チケットを開く]**」オプションや「**[!UICONTROL サポート]** タブが表示されない場合は、システム管理者に連絡してサポート管理者の役割を割り当ててください。

>[!NOTE]
>
> この問題が原因で実稼動システムが停止したり重大な中断が発生した場合は、すぐにサポートを受けるための電話番号が提供されます。
