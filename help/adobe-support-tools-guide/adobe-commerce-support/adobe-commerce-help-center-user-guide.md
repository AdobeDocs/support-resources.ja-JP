---
title: Adobe CommerceのExperience League サポートユーザーガイド
description: Adobe Commerce サポートにサポートチケットを送信する方法、アカウントへの共有アクセスを提供する方法、Experience League ナレッジベースを操作する方法について説明します。
feature: Support, Roles/Permissions, Tools and External Services, Admin Workspace, Iaas, Marketing Tools
feature-set: Commerce
solution: Commerce
exl-id: a7833d47-1d4b-4c10-9d2e-42fa43f8513c
source-git-commit: 6ac712151b002370eb84a3e3deb5480921cc40a6
workflow-type: tm+mt
source-wordcount: '3602'
ht-degree: 0%

---

# Adobe CommerceのExperience League サポートユーザーガイド

このガイドでは、[Experience League サポート &#x200B;](https://experienceleague.adobe.com/home#support)にサポートチケットを送信し、Adobe Commerce アカウントへの共有アクセスを提供する方法について説明します。

>[!NOTE]
>
>Adobe Commerce サポートは、Adobe Commerce ヘルプセンターからExperience Leagueに移行されました。 サポートケースを送信するには、[ここ](#what-is-experience-support)で説明されているExperience League ケースフォームフローを使用します。

>[!NOTE]
>
>現時点では、Adobe Commerce ヘルプセンターで以前に提出されたケースを確認するには、https://support.magento.com/hc/en-us/requestsにアクセスする必要があります。これらのケースは新しいサポートチケットシステムに移行されていないためです。 ヘルプセンターは読み取り専用になりました。元の問題のサポートを受け取るには、[Experience League サポート &#x200B;](https://experienceleague.adobe.com/home#support)にフォローアップチケットを送信する必要があります。

>[!NOTE]
>
>Adobe Commerce ヘルプセンターのナレッジベース部分が、Adobe Experience League ポータルに移行されました。 サポートチケットを作成すると、関連するナレッジベース記事と、Adobe Experience Leagueの他の関連するAdobe Commerce ドキュメントが提案されます。

**メジャーアップデート：** 2024年7月29日（PT）

**[EXPERIENCE LEAGUE サポートとは何ですか？](#what-is-experience-support)**

**[サポートケース](#support-cases)**

* [Experience League サポートへのログイン](#sign-in-experience-support)
* [サポートケースを送信](#support-case)

  * [Adobe Experience Leagueのスタートページ](#experience-league-start-page)
  * [Adobe Commerce アカウントページ](#submit-case-adobe-commerce-account-page)
  * [*メールアドレスを確認してください* Adobe Commerce アカウント ページのエラー](#verify-email-address-error)

* [サポートケースの追跡](#track-support-cases)
* [あなたの場合のコメント](#comments-in-your-case)
* [ケースを閉じる](#close-case)
* [ケースを再度開く](#reopen-case)
* [Cloud Consoleを使用したチケットの送信](#cloud-console)
* [Adobe Commerce P1 ホットライン](#P1-hotline)
* [Adobe Commerceの共通責任運用モデル](#shared-responsibility-operational-model)

**[共有アクセス：他のユーザーがアカウントにアクセスするための権限を付与](#shared-access)**

* [共有アクセスを提供できるユーザー](#who-can-provide-shared-access)
* [共有アクセスの提供](#provide-shared-access)
* [共有アクセスの取り消し（削除）](#revoke-shared-access)

  * [クラウドプロジェクトを介して共有アクセスが許可されたユーザーを削除するにはどうすればよいですか？](#remove-cloud-shared-access-users)

* [共有アカウントへのアクセス（アカウントの切り替え）](#switch-accounts)
* [共有アクセスのトラブルシューティング](#troubleshooting-shared-access)

Adobe Commerceの&#x200B;**[請求に関するFAQ](#billing-faq)**


## EXPERIENCE LEAGUEサポートとは何ですか？ {#what-is-experience-support}

Experience League サポートは、Adobeのサポートポータルであり、対象となるAdobe Commerceのお客様がサポートチケットを送信および管理できます。 また、トラブルシューティング記事を確認することもできます。

## サポートケース {#support-cases}

Adobe Experience League サポートケース管理では、契約中のすべてのAdobe Commerce製品について、Adobe Commerceを含むAdobe製品を使用する際に発生した特定の問題に対処するために、サポートを通じてサポートを利用できます。

## EXPERIENCE LEAGUE サポートへのログイン {#sign-in-experience-support}

ログインすると、サポートチケットに関する担当者からの質問を送信、更新、応答できます。

Adobe Experience League サポートにログインするには、次の手順に従います。

1. [experienceleague.adobe.com](https://experienceleague.adobe.com/?lang=ja)に移動します。
1. Adobeのログイン資格情報を使用してログインします。

![sign-into-experience-league](/help/adobe-support-tools-guide/assets/experience_league_sign_in.png)

### サポートケースを送信 {#support-case}

アカウントオーナーまたはShared Access ユーザーとして正常にログインしたら、Adobe Experience League ホームページ、Adobe Commerce アカウントページ、Adobe Commerce Cloud アカウントページを使用してサポートケースを送信できます。

>[!NOTE]
>
>Adobe Commerce Marketplace チームのサポートリクエストは、Experience Leagueを通じて送信することはできません。サポートシステムは、Experience Leagueと統合されていない別のプラットフォーム上で動作するからです。
>
>次の条件に当てはまる場合は、サポートケースを送信できます。
>
>* 問題の組織は、左側の列に名前が付けられ、（Commerce）で終わります。 問題は、その組織または関連するアカウントに関連しています。
>* 問題は、Marketplace アカウントにログインできないか、拡張機能のデプロイについて質問があることです。
>* 問題は、Marketplaceで購入した商品の返金をリクエストすることだけではありません。
>
>[Adobe Commerce Marketplace](https://commercemarketplace.adobe.com/)での拡張機能の公開、購入の問題、返金のリクエストに関する問題については、https://commercemarketplace.adobe.com/にアクセスして[!DNL Commerce Marketplace] チームに直接お問い合わせください。 ページの下部に移動し、**[!UICONTROL お問い合わせ]**&#x200B;をクリックすると、Marketplace サポートチケットを送信するためのフォームが開きます。

#### Adobe Experience Leagueのスタートページ {#experience-league-start-page}

Adobe Experience Leagueのスタートページを使用して新しいサポートケースを送信するには、[Experience Leagueでサポートチケットを作成](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-customer-support-experience#create-a-support-ticket-with-experience-league)を参照してください。

>[!INFO]
>
>1. ケースを提出するには、適切な商品（例：Adobe Commerce、Adobe Commerce Intelligence、Adobe Commerce Payment Services、Experience Platformなど）をサポートする権利が必要です。 サポートの資格がない場合は、ページの上部にバーが表示され、組織内のサポート資格を持つユーザーではないことが通知されます。
>1. 複数の組織に属している場合、または類似した名前を持つ複数の組織がある場合（各組織がサブスクリプションを持つ他のAdobe製品のいずれかを表します）、最初に&#x200B;*[!DNL (Commerce)]*&#x200B;で終わる左側の列のドロップダウンから適切な組織を選択する必要があります。
>1. ケースの送信時に「**[!UICONTROL 製品を選択]**」ドロップダウンが空の場合は、Adobe Commerce パートナーアカウントを使用している可能性があります。 サポートの使用権限を持つ販売者から[共有アクセス &#x200B;](#shared-access)を持つユーザーのみがチケットを送信できます。 加盟店の問題がある場合は、共有アクセスをリクエストしてください。 パートナーの問題については、spphelp@adobe.comにお問い合わせください。

>[!NOTE]
>
>ケースを送信する前に正しい組織を選択し、選択した組織がサポートをリクエストする製品に適した使用権限を持っていることを確認します。 例えば、問題がAdobe Commerceに関連するものの、Adobe Commerce IntelligenceまたはAdobe Experience Platformを製品として選択し、ケースが正常に送信された場合、ケースのルーティングが間違い、応答時間が遅れる可能性があります。
>
>さらに、ケースが送信された時点で間違った組織が選択された場合、適切な組織または正しい組織について、**[!UICONTROL マイケース]**&#x200B;の下のケースを表示できません。 Adobe Commerce サポートチームには、ケースに関連付けられている組織を変更する機能がありません。この問題に対処するには、既存のケースをクローズし、適切な詳細が提供/選択された新しいケースを送信する必要があります。

>[!NOTE]
>
>製品として「**[!DNL Commerce]on cloud infrastructure**」を選択したチケットを送信し、組織に複数のプロジェクトがリストされている場合は、適切な&#x200B;**[!UICONTROL プロジェクト ID]**&#x200B;を選択するように求められます。 希望する&#x200B;**[!UICONTROL プロジェクト ID]**&#x200B;が見つからない場合は、チケットに別の「プロジェクト X」でサポートを求めている旨のメモを必ず追加してください。<br>Managed Services **の「**&#x200B;[!DNL Commerce]」チケットを送信する予定で、クラウドインフラストラクチャ **の**&#x200B;[!DNL Commerce]&#x200B;にいる場合、利用可能な商品としてクラウドインフラストラクチャ **の**&#x200B;[!DNL Commerce]&#x200B;が表示されません：<br>1。 問題の件名を&#x200B;**[!UICONTROL ケースのタイトル]**.<br>2に入力します。 問題の説明を&#x200B;**[!UICONTROL ケースの説明]**.<br>3に入力します。 これらの両方の項目を入力すると、以下の&#x200B;**[!UICONTROL クラウドプロジェクト URL]** フィールドが表示されます。

>[!IMPORTANT]
>
>experienceleague.adobe.comにログインしても組織ドロップダウンメニューに組織が表示されない場合は、サポートをリクエストしたり、既存のサポートケースを管理したりする前に、プロファイルをaccounts.magento.comと同期する必要がある場合があります。
>
>1. accounts.magento.comに移動し、Adobe Experience Leagueでサポートケースの管理に使用するのと同じプロファイル（企業、学校、または個人）でログインします。
>1. accounts.magento.com プロファイルに正常にログインしたら、experienceleague.adobe.comに戻ってログインします。
>1. 組織ドロップダウンメニューから組織を選択します。
>1. それでも組織が表示されない場合は、Commerce管理者に連絡して、サポート委任者権限を取得してください。 詳しくは、[Commerce Account Share](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-share)のヘルプ記事を参照してください。

>[!NOTE]
>
>組織や製品が重要な理由
>
>**例A**：共有アクセス権が1つの会社のみであり、その会社には2つのAdobe製品（Product1およびProduct2）の使用権限があります。
>
>1. 各組織は1つの製品を表しているので、ドロップダウンに2つの組織（OrgA-Product1やOrgB-Product2など）が表示されます。
>1. Product = Product1を選択したが、問題がProduct2に関連している場合、ケースはProduct2 サポートにルーティングされ、ケースをProduct1 サポートに転送する際に遅延が発生します。
>1. OrgA-Product1のケースを送信し、今後その組織の&#x200B;**[!UICONTROL My Cases]**&#x200B;を確認する場合、組織としてOrgA-Product2を選択するとケースが表示されません（例Bと比較すると、他の組織を選択する必要があります）。
>
>**例B**: 2つの会社に対する共有アクセスがあり、各会社にはAdobe Commerceの使用権限のみが付与されています。
>
>1. OrgAのケースを送信したが、問題が実際にOrgBに影響を与えている場合、OrgBのメンバーは今後&#x200B;**[!UICONTROL My Cases]**&#x200B;の下でこのケースを確認できません。
>1. さらに、組織Aのメンバーは、実際に組織B向けの&#x200B;**[!UICONTROL マイケース]**&#x200B;の下のケースを確認できるようになり、プライバシーの問題につながる可能性があります。

>[!NOTE]
>
> 最も迅速で正確なサポートを受けられるように、サポートリクエストを作成する際に正しい詳細を選択します。 正確な選択により、ケースを正しいチームに直接転送し、応答時間を短縮できます。
>
>組織がAdobe Commerce Intelligence / Commerce レポート （MBI）の使用権限を持っているが、高度なレポートに関するサポートが必要な場合は、**Commerce レポート**&#x200B;を製品として選択しないでください。 Commerce Reporting チームは、高度なレポートの問題に対するサポートを提供していません。
>
>問題が支払いに関連する場合は、デフォルトで支払いサービスを選択しないでください。 決済サービスとは、Adobeの決済サービスモジュールを指します。 一般的に、支払い上の問題のために選択すると、対象となる製品と適切な調査パスについて混乱が生じる可能性があります。
>
>別の製品を選択できない場合（例えば、**[!UICONTROL 製品を選択]** ドロップダウンが空であるか、表示されていない場合）は、通常、次のいずれかの理由が原因です。
>
>* Commerceの使用権限が期限切れになっているか、非アクティブです（請求やライセンスの問題が原因など）。
>* Adobe Commerce on cloud infrastructure （PaaS）でホストされているインスタンスの場合、Cloud プロジェクトに追加されていません。
>
>クラウドプロジェクト上のAdobe Commerceの場合は、アカウントオーナーに連絡して、適切なクラウドプロジェクトに追加するようにリクエストしてください。 詳しくは、「[&#x200B; クラウドインフラストラクチャ上のAdobe Commerceのユーザーアクセスを管理](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/project/user-access)」を参照してください。
>
>共有アクセスが付与され、Cloud プロジェクトに追加された後：
>
>1. [Adobe サポート &#x200B;](https://experienceleague.adobe.com/home?lang=en#support) ページに移動します。
>1. 左側の組織ドロップダウンで、名前が&#x200B;**（Commerce）**&#x200B;で終わる組織を選択します。
>1. 適切な製品のチケットを送信し、高度なレポートに特に関連する問題については&#x200B;**Commerce レポート**&#x200B;を選択しないでください。

サポートケースを送信するには、Experience Leagueにログインするには、https://account.adobe.comとhttps://account.magento.comの両方にアカウントが必要です。 ログインするまで、サポートケースを送信することはできません。

既にhttps://account.magento.comにアカウントをお持ちで、ログインできない場合は、2022年8月時点で必要なhttps://account.adobe.comにアカウントを登録していない可能性があります。

これを解決するには、以下を行います。

1. MAG IDの同じメールアドレスを使用して、https://account.adobe.comでアカウントを作成します。
1. https://account.magento.comに移動して、Adobe IDをMAG IDにリンクします。

#### Adobe Commerce アカウントページ {#submit-case-adobe-commerce-account-page}

Adobe Commerce アカウントページを使用して新しいサポートチケットを送信するには、次の手順に従います。

1. Adobe Commerce アカウントにログインします。 ユーザーガイドの[詳細な手順](https://experienceleague.adobe.com/docs/commerce-admin/start/commerce-account/commerce-account-create.html?lang=en#create-a-commerce-account)を参照してください。
1. 「**サポート**」タブをクリックします。

   ![magento_account_support_tab](/help/adobe-support-tools-guide/assets/magento_account_support_tab.png){width="800"}

1. Adobe Experience Leagueのサポートページが読み込まれます。
1. 左側のメニューから「**[!UICONTROL チケットを開く]**」を選択します。
1. [&#x200B; フィールド &#x200B;](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-support-ticket-contact-reason-descriptions)に入力します。
1. 「**送信**」をクリックします。

#### *メールアドレスを確認してください* Adobe Commerce アカウント ページのエラー {#verify-email-address-error}

「[Adobe Commerce アカウント &#x200B;](https://account.magento.com/)」ページで「メールアドレスを確認してください」というエラーが表示された場合、サポートチケットを送信することはできません。

![Verify_Email_Address_Error](/help/adobe-support-tools-guide/assets/Verify_Email_Address_Error.png)


### Commerceのサポートケースの追跡 {#track-support-case}

サポートケースは、次のとおりです。

* 個人向けに送信したものです。
* CC （カーボンコピー）を通じてウォッチャーとして追加されました。

>[!NOTE]
>
>Commerce以外の他のAdobe製品に送信されたサポートケースがある場合、それらのチケットを同じ画面から追跡することはできません。最初に、製品の使用権限に関連付けられている組織に切り替える必要があります。
>例えば、以前に「（Commerce）」で終わる組織を選択してCommerce ケースをトラッキングしていますが、AEP サポートケースもあります。これらのケースはここでは表示されません。

#### ユースケースの表示

左側のメニューで「**[!UICONTROL マイケース]**」をクリックすると、自分で送信したCommerceのケースを表示できます。 「（Commerce）」で終わる正しい組織を選択していることを確認してください。

![view-support-cases](/help/adobe-support-tools-guide/assets/view_support_cases.png)

#### 監視したケースの表示

左側のメニューで「**[!UICONTROL 自分の組織のケース]**」をクリックすると、ウォッチャー&#x200B;*として*&#x200B;追加されたCommerce ケースを表示できます。

<!-- TODO: Add image here -->


#### ケースの検索

ケースを検索するには、*[!UICONTROL 検索]* フィールドに検索クエリを入力し、キーボードの&#x200B;*enter*&#x200B;を押します。

![検索ケース &#x200B;](/help/adobe-support-tools-guide/assets/search_cases.png)

#### ユースケースを拡大

ケースにさらに注意を払う必要があり、最初の応答時間が経過したと感じた場合は、ケースをエスカレーションする可能性があります。 そのためには，

1. 画面の右側にある&#x200B;*[!UICONTROL ケースの詳細]* パネルの右下にある&#x200B;**[!UICONTROL 管理にエスカレーション]**&#x200B;をクリックします。

   ![管理にエスカレーション &#x200B;](/help/adobe-support-tools-guide/assets/escalate_to_management.png)

1. クリックすると、ポップアップフォームが表示されます。 フォームに入力し、**[!UICONTROL エスカレーション]**&#x200B;をクリックします。

   ![confirm-escalation](/help/adobe-support-tools-guide/assets/confirm_escalation.png)

   *エスカレーションの理由には、*&#x200B;が含まれる場合があります：エージェントのコミュニケーションスキル、エージェントの技術的な知識、コールバック/更新の待機中、問題の緊急性の変更、解決が期待に応じなかった、解決までの時間。

#### サポートケースにウォッチャーを追加する

組織のメンバーが送信したサポート事例にウォッチャーを追加できます。 新しいケースが提出されたり、既存のケースが更新されたりすると、視聴者にメール通知が届きます。

1. 既存のケースにウォッチャーを追加するには、ケースを開き、画面の右側にあるケース詳細パネルの「ウォッチャー」の横にある鉛筆アイコンをクリックします。

   ![&#x200B; アドウォッチャー](/help/adobe-support-tools-guide/assets/add_watchers.png)

1. 鉛筆をクリックした後、リストからウォッチャーを追加または削除できます。

   ![update-watchers](/help/adobe-support-tools-guide/assets/update_watchers.png)

>[!NOTE]
>
>ケースのウォッチャーを追加および削除する方法について詳しくは、[&#x200B; ウォッチャーの追加と削除、チケットのクローズと再開のビデオ &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-learn/tutorials/help-and-support/add-remove-watchers-close-reopen-support-ticket)を参照してください。

### あなたの場合のコメント {#comments-in-your-case}

お客様のケースのコメントには、お客様またはAdobe Commerce サポートチームが作成したすべてのコメントが含まれます。コメントは、最新（上）から最も早い（下）まで表示されます。
コメントを追加するには、次の手順に従います。

1. チケットの一番下までスクロールします。
1. 「**[!UICONTROL コメント]**」フィールドにコメントを入力し、「**[!UICONTROL コメントを追加]**」をクリックします。

![add-comments](/help/adobe-support-tools-guide/assets/add_comments.png)

### ケースを閉じる {#close-case}

ケースを閉じるには、*[!UICONTROL ケース詳細]* パネルの右下にある&#x200B;**[!UICONTROL ケースを閉じる]**&#x200B;をクリックします。

![&#x200B; クローズケース &#x200B;](/help/adobe-support-tools-guide/assets/close_case.png)

>[!NOTE]
>
>ケースをクローズする方法について詳しくは、[視聴者の追加と削除、チケットのクローズと再開のビデオ &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-learn/tutorials/help-and-support/add-remove-watchers-close-reopen-support-ticket)を参照してください。

### ケースを再度開く {#reopen-case}

>[!NOTE]
>
>**ケースは、クローズ後14日以内にのみ再開できます。** ケース閉鎖から14日を超えていても、問題についてヘルプを依頼したい場合は、新しいケースを開く必要があります。<br> ケースのクローズと再開について詳しくは、[視聴者の追加と削除、チケットのクローズと再開のビデオ &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-learn/tutorials/help-and-support/add-remove-watchers-close-reopen-support-ticket)を参照してください。

>[!NOTE]
>
>クローズしたチケットからのメール通知に応答して、ケースを再度開くことはできません。 ケースを再度開くには、アカウント所有者から[共有アクセス &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-cloud-kcs/kbarticles/ka-26164)が付与されていることを確認してください。

### Cloud Consoleを使用したチケットの送信 {#cloud-console}

Cloud Consoleを使用して新しいサポートチケットを送信するには、次の手順に従います。

1. [Cloud Console](https://console.adobecommerce.com)にログインします。
1. ユーザーメニューで「**[!UICONTROL サポート]**」を選択します。
1. **[!UICONTROL マイチケット]** ページが読み込まれます。
1. 右上隅の「**[!UICONTROL チケットを送信]**」をクリックします。
1. [&#x200B; フィールド &#x200B;](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-support-ticket-contact-reason-descriptions)に入力します。
1. 「**[!UICONTROL 送信]**」をクリックします。

### Adobe Commerce P1 ホットライン {#P1-hotline}

[Adobe Commerce P1 ホットライン &#x200B;](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/how-to/adobe-commerce-p1-notification-hotline.html)記事では、P1 インシデント中にヘルプを求める際にAdobe CommerceのP1 ホットライン番号を提供し、提供する情報について説明しています。

### Adobe Commerceの共通責任運用モデル {#shared-responsibility-operational-model}

[Adobe Commerce Shared Responsibility Operational Model](https://experienceleague.adobe.com/en/docs/commerce-operations/security-and-compliance/shared-responsibility#operational-responsibilities-summary)の記事を参照してください。
この目的は、Pro インフラストラクチャの提供のみに対する運用上の責任を明確にすることです。

### フォローアップチケットの発行 {#follow-up}

フォローアップチケットを開くと、元の問題がフォローアップチケットにリンクされ、継続できるようになります。

フォローアップチケットを開くには、フォローアップを作成するチケットの下部にある「*フォローアップを作成*」リンクをクリックします。

## 共有アクセス：他のユーザーがアカウントにアクセスするための権限を付与します {#shared-access}

他のAdobe Commerce アカウント所有者に対して、アカウントへの限定的なアクセス権を付与できます。 特に、**共有アクセス**&#x200B;機能を使用すると、信頼できる従業員およびサービスプロバイダーがヘルプセンターアカウントを使用してサポートチケットを操作できるように、権限を提供できます。

Adobe Commerce アカウントページ（[https://account.magento.com](https://account.magento.com/)）を使用して、共有アクセスを提供および管理できます。

### 共有アクセスを提供できるユーザー {#who-can-provide-shared-access}

他のユーザーに共有アクセスを提供できるのは、適切な権限を持つアカウント所有者（プライマリアカウント所有者）のみです。

ユーザーとそのアクセスの管理は、特に共有アクセスの観点から、顧客の責任です。 したがって、Adobe Commerce サポートチームは、お客様の代わりにAdobe Commerce アカウントへの共有アクセスを提供することはできません。 お客様は、[Adobe Commerce アカウントページ &#x200B;](https://account.magento.com/)を使用して、自身で共有アクセス権を持つユーザーを追加することをお勧めします。

共有アクセス権が付与されたユーザーは、他のユーザーにそのようなアクセス権を譲渡または付与することはできません。

### 共有アクセスの提供 {#provide-shared-access}

共有アカウントの設定に関する詳細な手順については、Adobe Commerce入門ガイドの「[Commerce アカウントの共有](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-share)」セクションを参照してください。

>[!NOTE]
>
>共有アクセスを許可するには、既存のアカウントが必要です。詳しくは、[Commerce アカウントの作成](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create#create-a-commerce-account)を参照してください。

新しいユーザーに共有アクセスを提供すると、関連する情報は、Adobe Commerce アカウントページの&#x200B;**共有アクセス** > **権限の管理**&#x200B;で利用できます。

>[!NOTE]
>
>Shared Accessは、Commerce Cloud Consoleへのアクセス権を自動的に付与しません。 ユーザーをクラウドプロジェクト [&#128279;](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/project/user-access#add-a-user-to-the-project)に個別に追加する必要があります。

![magento-account-shared-manage-permissions](/help/adobe-support-tools-guide/assets/magento_account_shared_manage_permissions.png)

### 共有アクセスの取り消し（削除） {#revoke-shared-access}

1. [https://account.magento.com](https://account.magento.com/)でAdobe Commerce アカウントにログインします。
1. 左側のパネルで、「共有アクセス」の下の「**権限を管理」を選択します。**
1. 共有アクセスを取り消すユーザーを見つけ、ユーザーの行（**アクション**&#x200B;列）の![削除アイコン &#x200B;](/help/adobe-support-tools-guide/assets/remove_icon.png){width="25"}をクリックします。
1. 「**ユーザーを削除**」をクリックしてアクセス権を取り消すか、上隅の「X」をクリックして取り消しをキャンセルします。

   ![revoke_shared_access](/help/adobe-support-tools-guide/assets/revoke_shared_access.png){width="800"}

   また、**編集** メニューを使用して、共有アクセスを取り消すこともできます。

1. [https://account.magento.com](https://account.magento.com/)でAdobe Commerce アカウントにログインします。
1. 左側のパネルで、「共有アクセス」の下の「**権限を管理」を選択します。**
1. 共有アクセスを取り消すユーザーを見つけ、ユーザーの行（**アクション**&#x200B;列）の&#x200B;**編集**&#x200B;をクリックします。
1. ページ下部の「**このユーザーを削除**」をクリックします。
1. 確認ポップアップで「**ユーザーを削除**」をクリックしてアクセス権を取り消すか、上隅の「X」をクリックして取り消しをキャンセルします。

### クラウドプロジェクトを介して共有アクセスが許可されたユーザーを削除するにはどうすればよいですか？ {#remove-cloud-shared-access-users}

<u>影響を受ける製品とバージョン </u>

* Adobe Commerce Cloud （全バージョン）

<u>原因</u>：

Adobe Commerce Cloud プロジェクトを所有しており、ユーザーをプロジェクトに追加した場合、プロジェクトオーナーのMAGE IDに対する共有アクセスが自動的に付与されている可能性があります。 これは通常、**[!UICONTROL Share Name]**&#x200B;列に表示され、MAG[XYZ ]*からの* クラウド共有アクセスを示します。

>[!NOTE]
>
>DELETE リンクが見つからない場合は、Commerce Cloudを通じてShared Accessが自動的に付与されたことを意味します。

<u>ソリューション</u>

共有アクセスがこのページ [&#128279;](https://account.magento.com/grantor/manage/)で追加/付与されなかった場合、共有名が&#x200B;*Cloud Shared Access from MAG[XYZ]*&#x200B;の共有アクセスユーザーのリストを削除することはできません。 これらは、情報/監査の目的で保持されます。

ただし、それらの共有アクセス ユーザーに対する権限を取り消すと、そのユーザーはそのアクセス権を持たなくなります。

1. [https://account.magento.com](https://account.magento.com/)でAdobe Commerce アカウントにログインします。
1. 左側のパネルの&#x200B;**[!UICONTROL 共有アクセス]**&#x200B;で、**[!UICONTROL 権限の管理]**&#x200B;を選択します。
1. 共有アクセスを取り消すユーザーを見つけ、ユーザーの行（*[!UICONTROL アクション]*&#x200B;列）の&#x200B;**[!UICONTROL 編集]**&#x200B;をクリックします。
1. **[!UICONTROL アカウント権限の付与]**&#x200B;の下にあるすべてのリソースのチェックを外します。
1. ユーザーがまだ&#x200B;**[!UICONTROL クラウド共有アクセス]**&#x200B;を使用しているかどうかに関する混乱を防ぐには、**[!UICONTROL 共有名]**&#x200B;を次のような名前に変更する必要があります。例：*クラウド共有アクセスが失効しました – 削除できません*、または類似の名前に変更します。

![grant-account-permissions-image](/help/adobe-support-tools-guide/assets/help-center-user-guide-grant-account-permissions-image.png){width="800"}

詳しくは、「Commerce on Cloud Infrastructure Guide」の[&#x200B; ユーザーアクセスの管理](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html#manage-users-from-the-project-web-interface) ドキュメントを参照してください。

### 共有アカウントへのアクセス（アカウントの切り替え） {#switch-accounts}

>[!NOTE]
>
>この手順は、Adobe Commerceのチケットを送信する場合には必要ありません。
>Adobe Commerce チケットの送信に関するデモについては、[このビデオを参照してください](https://experienceleague.adobe.com/en/playlists/support-requests)。

提供された共有アクセスを使用するには、次の手順に従います。

1. [https://account.magento.com](https://account.magento.com/)でAdobe Commerce アカウントにログインします。
1. 「**アカウントを切り替え**」メニューをクリックし、アカウントを選択します。

   ![magento-account-shared-switch](/help/adobe-support-tools-guide/assets/magento_account_shared_switch.png){width="800"}

現在使用しているアカウント（自分のネイティブアカウントまたは共有アクセス）を確認するには、**アカウントを切り替え** メニューを参照してください。アクティブなアカウントが表示されます。

### 共有アクセスのトラブルシューティング {#troubleshooting-shared-access}

サポート ナレッジベースの[共有アクセスのトラブルシューティング記事](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/shared-access-troubleshooting)を参照してください。
