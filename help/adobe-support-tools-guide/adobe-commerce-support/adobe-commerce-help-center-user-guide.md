---
title: Adobe CommerceのExperience League サポートユーザーガイド
description: Experience League サポートにサポートチケットを送信する方法、アカウントへの共有アクセスを提供する方法、Adobe Commerce ナレッジベースを操作する方法について説明します。
feature: Support, Roles/Permissions, Tools and External Services, Admin Workspace, Iaas, Marketing Tools
feature-set: Commerce
solution: Commerce
source-git-commit: 7c09a33efee7a2e62b47758ab1af37e663776374
workflow-type: tm+mt
source-wordcount: '3275'
ht-degree: 0%

---

# Adobe CommerceのExperience League サポートユーザーガイド

このガイドでは、[Experience League サポートにサポートチケットを送信し &#x200B;](https://experienceleague.adobe.com/home#support)Adobe Commerce アカウントへの共有アクセスを提供する方法について説明します。

>[!NOTE]
>
>Adobe Commerceのサポートは、Adobe Commerce ヘルプセンターからExperience Leagueに移行されました。 [&#x200B; こちら &#x200B;](#what-is-experience-support) で説明しているExperience League ケースフォームフローを使用して、サポートケースを送信します。

>[!NOTE]
>
>この時点で、以前にAdobe Commerce ヘルプセンターで送信したケースを表示するには、https://support.magento.com/hc/en-us/requestsに移動する必要があります。これらのケースは新しいサポートチケットシステムに移行されていないからです。 ヘルプセンターは読み取り専用になりました。元の問題に対するサポートを引き続き受けるには、[Experience League サポート &#x200B;](https://experienceleague.adobe.com/home#support) にフォローアップチケットを送信する必要があります。

>[!NOTE]
>
>Adobe Commerce ヘルプセンターのナレッジベースの部分は、Adobe Experience League ポータルに移行されました。 サポートチケットを作成すると、関連するナレッジベース記事が、Adobe Experience League からの関連するその他のAdobe Commerce ドキュメントと共に提案されます。

**主要更新：** 2024 年 7 月 29 日

**[EXPERIENCE LEAGUEのサポートとは](#what-is-experience-support)**

**[サポートケース](#support-cases)**

* [Experience League サポートへのログイン](#sign-in-experience-support)
* [サポートケースの送信](#support-case)

   * [Adobe Experience League スタートページ](#experience-league-start-page)
   * [Adobe Commerce アカウントページ](#submit-case-adobe-commerce-account-page)
   * [*メールアドレスを確認してください*](#verify-email-address-error)

* [サポートケースのトラッキング](#track-support-cases)
* [あなたのケースのコメント](#comments-in-your-case)
* [ケースを閉じる](#close-case)
* [ケースを再度開きます](#reopen-case)
* [Cloud Console を使用してチケットを送信](#cloud-console)
* [Adobe Commerce P1 ホットライン](#P1-hotline)
* [Adobe Commerceの共通責任運用モデル](#shared-responsibility-operational-model)

**[共有アクセス：自分のアカウントにアクセスするための権限を他のユーザーに付与します](#shared-access)**

* [共有アクセスを提供できるユーザー](#who-can-provide-shared-access)
* [共有アクセスを提供](#provide-shared-access)
* [共有アクセスの失効（削除）](#revoke-shared-access)

   * [クラウドプロジェクトを介して共有アクセス権を付与されたユーザーを削除する方法を教えてください。](#remove-cloud-shared-access-users)

* [共有アカウントへのアクセス （アカウントの切り替え）](#switch-accounts)
* [共有アクセスのトラブルシューティング](#troubleshooting-shared-access)

**[ADOBE COMMERCEの請求に関する FAQ](#billing-faq)**


## Experience League サポートとは {#what-is-experience-support}

Experience League サポートは、Adobeのサポート ポータルで、Adobe Commerceの正規のお客様がサポートチケットを送信および管理できます。 また、トラブルシューティング記事を確認することもできます。

## サポートケース {#support-cases}

Adobe Experience League サポートケース管理を使用すると、サポート事例を通じてサポートを活用し、Adobe Commerceを含むAdobe製品を使用中に発生した特定の問題を、契約中のすべてのAdobe Commerce製品に対して解決できます。

## Experience League サポートへのログイン {#sign-in-experience-support}

ログインすると、サポートチケットに関するエージェントからの質問を送信、更新、回答できます。

Adobe Experience League サポートにログインするには、次の手順に従います。

1. [experienceleague.adobe.com](https://experienceleague.adobe.com/?lang=ja) に移動します。
1. Adobe ログイン資格情報を使用してログインします。

![experience-league へのログイン &#x200B;](/help/adobe-support-tools-guide/assets/experience_league_sign_in.png)

### サポートケースの送信 {#support-case}

アカウントオーナーまたは Shared Access ユーザーとして正常にログインしたら、Adobe Experience League のホームページ、Adobe Commerceのアカウントページ、Adobe Commerce Cloud のアカウントページを使用して、サポートケースを送信できます。

>[!NOTE]
>
>Adobe Commerce Marketplace チームのサポートリクエストは、Experience Leagueを通じて送信することはできません。サポートシステムが、Experience Leagueと統合されていない別のプラットフォームで動作するからです。
>
>次のステートメントが当てはまる場合、サポートケースを送信することができます。
>
>* 問題の組織の名前が左の列で、（Commerce）で終わります。 イシューは、その組織または関連付けられたアカウントに関連しています。
>* お客様の問題は、Marketplace アカウントにログインできないこと、または拡張機能のデプロイに関して質問があることです。
>* 問題は、Marketplace での購入に対する払い戻しのリクエストだけではありません。
>
>拡張機能の公開、[Adobe Commerce Marketplace](https://commercemarketplace.adobe.com/) での購入、払い戻しの請求に関する問題については、https://commercemarketplace.adobe.com/に直接 [!DNL Commerce Marketplace] チームにお問い合わせください。 ページの下部に移動し、**[!UICONTROL お問い合わせ]** をクリックすると、Marketplace サポートチケットを送信するためのフォームが開きます。

#### Adobe Experience League スタートページ {#experience-league-start-page}

Adobe Experience League のスタートページを使用して新しいサポートケースを送信するには、[Experience Leagueでサポートチケットを作成する &#x200B;](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-customer-support-experience#create-a-support-ticket-with-experience-league) を参照してください。

>[!INFO]
>
>1. ケースを提出するには、適切な商品（Adobe Commerce、Adobe Commerce Intelligence、Adobe Commerce Payment Services、Experience Platformなど）のサポートを受ける資格を付与されている必要があります。 サポートを受ける資格がない場合は、組織内でサポートを受ける資格のあるユーザーではないことを示すバーがページ上部に表示されます。
>1. 複数の組織に属している場合、または類似した名前を持つ複数の組織がある場合は（それぞれが、組織が購読している他のAdobe製品を表します）、最初に、左の列で「*[!DNL (Commerce)]*」で終わるドロップダウンから適切な組織を選択する必要があります。
>1. ケースを送信する際に **[!UICONTROL 商品を選択]** ドロップダウンが空の場合は、Adobe Commerce パートナーアカウントを使用している可能性があります。 サポート資格を持つマーチャントからの [&#x200B; 共有アクセス &#x200B;](#shared-access) を持つユーザーのみがチケットを送信できます。 マーチャントの問題については、共有アクセスをリクエストします。 パートナーに関する問題については、spphelp@adobe.comにお問い合わせください。

>[!NOTE]
>
>ケースを送信する前に正しい組織を選択していること、および選択した組織が、サポートをリクエストする製品に適した資格を持っていることを確認します。 例えば、イシューがAdobe Commerceに関連しているが、商品としてAdobe Commerce IntelligenceまたはAdobe Experience Platformを選択していて、ケースが正常に送信された場合、ケースのルーティング間違いや応答時間の遅延につながる可能性があります。
>
>また、ケースの送信時に間違った組織が選択された場合、チームは適切または適切な組織の **[!UICONTROL マイケース]** でケースを表示できません。 Adobe Commerce サポートチームには、ケースに関連付けられた組織を変更する機能はありません。この問題に対処するには、既存のケースをクローズし、提供/選択された適切な詳細で新しいケースを送信する必要があります。

>[!NOTE]
>
>製品として「**[!DNL Commerce]on cloud infrastructure**」が選択されたチケットを送信しており、組織に複数のプロジェクトがリストされている場合は、適切な **[!UICONTROL プロジェクト ID]** を選択するように求められます。 目的の **[!UICONTROL プロジェクト ID]** が見つからない場合は、別の「プロジェクト X」でサポートが必要なメモをチケットに追加してください。<br> クラウドインフラストラクチャで **[!DNL Commerce]を使用していて、「Managed Services上で**&#x200B;**[!DNL Commerce]」チケットを送信しようとしているが** クラウドインフラストラクチャで **[!DNL Commerce]を表示しない場合** 利用可能な商品として以下を行います。<br>1 **[!UICONTROL ケースのタイトル]** にイシューの件名を入力します。<br>2. **[!UICONTROL ケースの説明]** にイシューの説明を入力します。<br>3. これらの項目を両方とも入力すると、以下の「**[!UICONTROL クラウドプロジェクト URL]**」フィールドが表示されます。

>[!IMPORTANT]
>
>experienceleague.adobe.comにログインしたときに、組織のドロップダウンメニューに組織が表示されない場合は、サポートをリクエストする前または既存のサポートケースを管理する前に、プロファイルをaccounts.magento.comと同期する必要がある場合があります。
>
>1. accounts.magento.comに移動し、Adobe Experience League でのサポートケースの管理に使用するプロファイル（企業、学校、個人）と同じプロファイルでログインします。
>1. accounts.magento.com プロファイルに正常にログインしたら、experienceleague.adobe.comに戻ってログインします。
>1. 組織ドロップダウンメニューから組織を選択します。
>1. それでも組織が表示されない場合は、Commerce管理者に問い合わせて、サポート委任権限を取得してください。 詳しくは、[Commerce アカウント共有 &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-share) のヘルプ記事を参照してください。

>[!NOTE]
>
>組織/製品が重要な理由
>
>**例 A**：共有アクセス権を持つ会社は 1 つだけで、その会社が 2 つのAdobe製品（Product1 および Product2）の使用権限を持っています。
>
>1. 各組織は 1 つの製品を表すので、ドロップダウンには「OrgA-Product1」と「OrgB-Product2」という 2 つの組織が表示されます。
>1. Product = Product1 を選択した場合、問題が Product2 に関係しているときは、ケースは Product2 サポートにルーティングされ、ケースを Product1 サポートに転送する際に遅延が生じます。
>1. OrgA-Product1 のケースを発行し、今後その組織の **[!UICONTROL My Cases]** をレビューする場合、組織として OrgA-Product2 を選択しても表示されません（例 B と比較して、その他の組織を選択する必要があります）。
>
>**例 B**:2 つの会社に対して共有アクセス権があり、各会社はAdobe Commerceの使用権限のみを持っています。
>
>1. 組織 A に対してケースを送信したが、問題が実際に組織 B に影響を与えている場合、組織 B のメンバーは、今後、「マイケース **[!UICONTROL にこのケースを表示できなくな]** ます。
>1. さらに、組織 A のメンバーは、実際には組織 B 向けのケースである **[!UICONTROL マイケース]** の下のケースを確認できるようになり、プライバシーの問題が発生する可能性があります。

>[!NOTE]
>
> 最速で最も正確なサポートを受けるには、サポートリクエストを作成する際に、正しい詳細を選択します。 正確な選択は、ケースを正しいチームに直接ルーティングし、応答時間を短縮するのに役立ちます。
>
>組織がAdobe Commerce Intelligence/Commerce レポート（MBI）の権限を持っているが、詳細レポートに関するサポートが必要な場合は、**Commerce レポート** を商品として選択しないでください。 Commerce レポートチームは、高度なレポートの問題をサポートしていません。
>
>別の製品を選択できない場合（例えば、「**[!UICONTROL 製品を選択]**」ドロップダウンが空または表示されていない場合）、通常は、次のいずれかの理由が原因です。
>
>* Commerceの使用権限が期限切れになっているか、非アクティブです（未払いの請求やライセンスの問題など）。
>* クラウドインフラストラクチャ（PaaS）上のAdobe Commerceでホストされるインスタンスの場合、クラウドプロジェクトに追加されていません。
>
>クラウドプロジェクトのAdobe Commerceの場合は、アカウントオーナーに連絡して、適切なクラウドプロジェクトに追加されるようにリクエストします。 詳しくは、クラウドインフラストラクチャー上のAdobe Commerceの [&#x200B; ユーザーアクセスの管理 &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/project/user-access) を参照してください。
>
>共有アクセス権が付与され、クラウドプロジェクトに追加されたら、次の操作を行います。
>
>1. [Adobe サポート &#x200B;](https://experienceleague.adobe.com/home?lang=en#support) ページに移動します。
>1. 左側の組織ドロップダウンで、名前が「**（Commerce）**」で終わる組織を選択します。
>1. 適切な商品のチケットを送信し、詳細レポートに特別に関連する問題については、**Commerce レポート** を選択しないでください。

Experience Leagueにログインしてサポートケースを送信するには、https://account.adobe.comとhttps://account.magento.comの両方にアカウントがある必要があります。 サインインするまでサポート ケースを送信できません。

既にhttps://account.magento.comにアカウントを持っているがログインできない場合、2022 年 8 月からhttps://account.adobe.comにアカウントを登録する必要が生じている可能性があります。

これを解決するには、以下を行います。

1. MAG ID と同じメールアドレスを使用して、https://account.adobe.comでアカウントを作成します。
1. https://account.magento.comに移動して、Adobe IDと MAG ID をリンクします。

#### Adobe Commerce アカウントページ {#submit-case-adobe-commerce-account-page}

Adobe Commerce アカウントのページを使用して新しいサポートチケットを送信するには、次の手順に従います。

1. Adobe Commerce アカウントにログインします。 ユーザーガイドの [&#x200B; 詳細な手順 &#x200B;](https://experienceleague.adobe.com/docs/commerce-admin/start/commerce-account/commerce-account-create.html?lang=en#create-a-commerce-account) を参照してください。
1. 「**サポート**」タブをクリックします。

   ![magento_account_support_tab](/help/adobe-support-tools-guide/assets/magento_account_support_tab.png){width="800"}

1. Adobe Experience League サポートページが読み込まれます。
1. 左側のメニューから **[!UICONTROL チケットを開く]** を選択します。
1. [fields](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-support-ticket-contact-reason-descriptions) を入力します。
1. 「**送信**」をクリックします。

#### *メールアドレスを確認してください* エラーが発生しました（Adobe Commerce アカウントページ） {#verify-email-address-error}

[Adobe Commerce アカウント &#x200B;](https://account.magento.com/) ページの以下に示すような「メールアドレスを確認してください」エラーが発生した場合は、サポートチケットを送信できません。

![Verify_Email_Address_Error](/help/adobe-support-tools-guide/assets/Verify_Email_Address_Error.png)


### Commerce サポートケースのトラッキング {#track-support-case}

サポートケースは、次のような場合です。

* 直接提出しています。
* は、CC （カーボンコピー）を通じて監視者としてに追加されました。

>[!NOTE]
>
>Commerce以外のAdobe製品で送信されたサポートケースがある場合、それらのチケットを同じ画面から追跡することはできません。最初に、製品使用権限に関連付けられた組織に切り替える必要があります。
>例えば、以前に「（Commerce）」で終わる組織を選択して、Commerceの事例をトラッキングしたのに対して、AEPのサポートケースも持っている場合、それらの事例はここでは表示されません。

#### ケースを表示

左側のメニューで **[!UICONTROL マイケース]** をクリックすると、個人的に送信したCommerce ケースを確認できます。 「（Commerce）」で終わる正しい組織を選択していることを確認してください。

![view-support-cases](/help/adobe-support-tools-guide/assets/view_support_cases.png)

#### Adobe Commerce ヘルプセンターで過去の事例を確認する

Adobe Commerce ナレッジベースにあるAdobe Commerce ヘルプセンター **Adobe Commerce ヘルプセンターの廃止措置** から [&#x200B; 過去のケースを表示 &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-knowledge-base/kb/announcements/news/decommissioning-of-adobe-commerce-help-center) する方法について詳しく説明します。

#### 監視ケースの表示

*ウォッチャーとして追加* されたCommerce ケースを確認するには、左側のメニューで **[!UICONTROL 組織のケース]** をクリックします。

<!-- TODO: Add image here -->


#### ケースの検索

ケースを検索するには、「*[!UICONTROL 検索]*」フィールドに検索クエリを入力し、キーボードの *Enter* キーを押します。

![&#x200B; 検索ケース &#x200B;](/help/adobe-support-tools-guide/assets/search_cases.png)

#### ケースのエスカレーション

さらに注意が必要で、最初の応答時間が経過したと感じた場合は、ケースをエスカレーションできます。 これを行うには、

1. 画面右側の **[!UICONTROL ケースの詳細]** パネルの右下にある *[!UICONTROL 管理にエスカレート]* をクリックします。

   ![&#x200B; エスカレートから管理へ &#x200B;](/help/adobe-support-tools-guide/assets/escalate_to_management.png)

1. クリックすると、ポップアップフォームが表示されます。 フォームに入力して、「**[!UICONTROL エスカレート]**」をクリックします。

   ![confirm-escalation](/help/adobe-support-tools-guide/assets/confirm_escalation.png)

   *エスカレーションの理由には、エージェントのコミュニケーションスキル、エージェントの技術的知識、コールバック/更新待ち、イシューの緊急性の変化、解決が期待に応えなかったこと、解決までの時間などが含まれます*。

#### サポートケースに対するウォッチャーの追加

ウォッチャーを追加すると、組織のメンバーから送信されたケースをサポートできます。 新しいケースが送信されたとき、または既存のケースが更新されたときに、ウォッチャーにメール通知が届きます。

1. 既存のケースにウォッチャーを追加するには、ケースを開き、画面の右側にあるケースの詳細パネルの「ウォッチャー」の横にある鉛筆アイコンをクリックします。

   ![add-watchers](/help/adobe-support-tools-guide/assets/add_watchers.png)

1. 鉛筆をクリックすると、リストからウォッチャーを追加または削除できます。

   ![update-watchers](/help/adobe-support-tools-guide/assets/update_watchers.png)

>[!NOTE]
>
>ケースのウォッチャーの追加および削除方法について詳しくは、[&#x200B; ウォッチャーの追加と削除、チケットのクローズと再オープン &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-learn/tutorials/help-and-support/add-remove-watchers-close-reopen-support-ticket) のビデオを参照してください。

### あなたのケースのコメント {#comments-in-your-case}

ケースのコメントには、お客様またはAdobe Commerce サポートチームが作成したすべてのコメントが含まれています。 コメントは、最新（上）から最も古い（下）順に表示されます。
コメントを追加するには、次の手順に従います。

1. チケットの一番下までスクロールします。
1. 「**[!UICONTROL コメント]**」フィールドにコメントを書き込み、「**[!UICONTROL コメントを追加]**」をクリックします。

![add-comments](/help/adobe-support-tools-guide/assets/add_comments.png)

### ケースを閉じる {#close-case}

ケースを閉じるには、**[!UICONTROL ケースの詳細]** パネルの右下にある *[!UICONTROL ケースを閉じる]* をクリックします。

![&#x200B; クローズケース &#x200B;](/help/adobe-support-tools-guide/assets/close_case.png)

>[!NOTE]
>
>ケースをクローズする方法について詳しくは、[&#x200B; ウォッチャーの追加と削除、チケットのクローズと再オープン &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-learn/tutorials/help-and-support/add-remove-watchers-close-reopen-support-ticket) のビデオを参照してください。

### ケースを再度開きます {#reopen-case}

>[!NOTE]
>
>**クローズ後 14 日以内に限り、ケースを再オープンすることができます。** ケースをクローズしてから 14 日を超えても、問題に関するヘルプをリクエストしたい場合は、新しいケースをオープンする必要があります。<br> ケースのクローズと再オープンについて詳しくは、[&#x200B; ウォッチャーの追加と削除、チケットのクローズと再オープン &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-learn/tutorials/help-and-support/add-remove-watchers-close-reopen-support-ticket) のビデオを参照してください。

>[!NOTE]
>
>クローズ済みチケットからのメール通知に応答してケースを再オープンすることはできません。 ケースを再度開くには、アカウント所有者から [&#x200B; 共有アクセス &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-cloud-kcs/kbarticles/ka-26164) が付与されていることを確認してください。

### Cloud Console を使用してチケットを送信 {#cloud-console}

Cloud Console を使用して新しいサポートチケットを送信するには、次の手順に従います。

1. [Cloud Console](https://console.adobecommerce.com) にログインします。
1. ユーザーメニューで **[!UICONTROL サポート]** を選択します。
1. **[!UICONTROL マイチケット]** ページが読み込まれます。
1. 右上隅の **[!UICONTROL チケットを送信]** をクリックします。
1. [fields](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-support-ticket-contact-reason-descriptions) を入力します。
1. 「**[!UICONTROL 送信]**」をクリックします。

### Adobe Commerce P1 ホットライン {#P1-hotline}

[Adobe Commerce P1 ホットライン &#x200B;](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/how-to/adobe-commerce-p1-notification-hotline.html) の記事には、P1 インシデント発生時のAdobe Commerceの P1 ホットライン番号と、提供する情報が記載されています。

### Adobe Commerceの共通責任運用モデル {#shared-responsibility-operational-model}

[Adobe Commerceの共有責任運用モデル &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-operations/security-and-compliance/shared-responsibility#operational-responsibilities-summary) の記事を参照してください。
これは、当社の Pro インフラストラクチャ製品のみの運用上の責任を明確にすることを目的としています。

### フォローアップチケットを開く {#follow-up}

フォローアップチケットを開くと、元のイシューが継続性のためにフォローアップチケットにリンクされます。

フォローアップチケットを開くには、フォローアップチケットを作成するチケットの下部にある「*フォローアップを作成*」リンクをクリックします。

## 共有アクセス：自分のアカウントにアクセスするための権限を他のユーザーに付与します {#shared-access}

お客様は、お客様のアカウントに対し、他のAdobe Commerce アカウント所有者による限定的なアクセスを許可することができます。 特に、**共有アクセス** 機能を使用すると、信頼できる従業員とサービスプロバイダーにヘルプセンターアカウントを使用するための権限を付与して、サポートチケットを操作できるようにすることができます。

[https://account.magento.com](https://account.magento.com/) のAdobe Commerce アカウントページを使用して、共有アクセスを提供および管理できます。

### 共有アクセスを提供できるユーザー {#who-can-provide-shared-access}

従った権限を持つアカウント所有者（プライマリアカウント所有者）のみが、他のユーザーに共有アクセスを提供できます。

ユーザーとそのアクセスの管理は、特に共有アクセスの観点から、顧客の責任です。 そのため、Adobe Commerce サポートチームは、お客様の代わりにAdobe Commerce アカウントに共有アクセスを提供することはできません。 お客様は、[Adobe Commerce アカウントのページ &#x200B;](https://account.magento.com/) を使用して、自身が共有アクセスを持つユーザーを追加することをお勧めします。

共有アクセス権が付与されたユーザーは、そのアクセス権を他のユーザーに転送または付与することはできません。

### 共有アクセスを提供 {#provide-shared-access}

共有アカウントの設定手順について詳しくは、『Adobe Commerce入門ガイド』の [Commerce アカウントの共有 &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-share) の節を参照してください。

>[!NOTE]
>
>共有アクセスを付与するには、既存のアカウントが必要です。詳しくは [Commerce アカウントの作成 &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create#create-a-commerce-account) を参照してください。

新しいユーザーに共有アクセスを提供すると、Adobe Commerce アカウントページの **共有アクセス**/**権限の管理** で関連情報を利用できます。

>[!NOTE]
>
>Shared Access は、Commerce Cloudコンソールへのアクセスを自動的に付与しません。 [&#x200B; クラウドプロジェクトにユーザーを個別に追加する &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/project/user-access#add-a-user-to-the-project) 必要があります。

![magento-account-shared-manage-permissions](/help/adobe-support-tools-guide/assets/magento_account_shared_manage_permissions.png)

### 共有アクセスの失効（削除） {#revoke-shared-access}

1. Adobe Commerce アカウント（[https://account.magento.com](https://account.magento.com/)）にログインします。
1. 左側のパネルの「共有アクセス」で、「**権限の管理**」を選択します。
1. 共有アクセスを取り消すユーザーを見つけ、ユーザーの行（![&#x200B; アクション &#x200B;](/help/adobe-support-tools-guide/assets/remove_icon.png){width="25"} 列）にある **削除アイコン** をクリックします。
1. **ユーザーを削除** をクリックしてアクセスを取り消すか、左上隅の「X」をクリックして取り消しをキャンセルします。

   ![revoke_shared_access](/help/adobe-support-tools-guide/assets/revoke_shared_access.png){width="800"}

   **編集** メニューを使用して共有アクセスを取り消すこともできます。

1. Adobe Commerce アカウント（[https://account.magento.com](https://account.magento.com/)）にログインします。
1. 左側のパネルの「共有アクセス」で、「**権限の管理**」を選択します。
1. 共有アクセスを取り消すユーザーを見つけ、ユーザーの行（**アクション** 列）の「**編集**」をクリックします。
1. ページ下部の **このユーザーを削除** をクリックします。
1. 確認のポップアップで、「**ユーザーを削除**」をクリックしてアクセスを取り消すか、左上隅の「X」をクリックして取り消しをキャンセルします。

### クラウドプロジェクトを介して共有アクセス権を付与されたユーザーを削除する方法を教えてください。 {#remove-cloud-shared-access-users}

<u> 影響を受ける製品とバージョン </u>

* Adobe Commerce Cloud （すべてのバージョン）

<u>原因</u>：

Adobe Commerce Cloud プロジェクトがあり、プロジェクトにユーザーを追加していた場合、プロジェクト所有者の画像 ID に対する共有アクセスが自動的に付与されていた可能性があります。 これは通常、**[!UICONTROL Share Name]** 列に示され、*MAG[XYZ からのクラウド共有アクセス]* を示します。

>[!NOTE]
>
>DELETE リンクが見つからない場合は、Commerce Cloudを通じて共有アクセスが自動的に付与されていました。

<u>ソリューション</u>

共有アクセスが追加/付与されていない場合、共有名が *Cloud Shared Access である共有アクセスユーザーのリストを MAG[XYZ]* から削除することはできません [&#x200B; このページ &#x200B;](https://account.magento.com/grantor/manage/)。 これらは、情報/監査目的で保持されます。

ただし、それらの共有アクセスユーザーに対する権限を取り消すと、そのユーザーはアクセスできなくなります。

1. Adobe Commerce アカウント（[https://account.magento.com](https://account.magento.com/)）にログインします。
1. 左側のパネルの *[!UICONTROL 共有アクセス]* で「**[!UICONTROL 権限の管理]**」を選択します。
1. 共有アクセスを取り消すユーザーを見つけ、ユーザーの行（**[!UICONTROL アクション]** 列）の「*[!UICONTROL 編集]*」をクリックします。
1. 「*[!UICONTROL アカウント権限の付与]*」ですべてのリソースをオフにします。

![grant-account-permissions-image](/help/adobe-support-tools-guide/assets/help-center-user-guide-grant-account-permissions-image.png){width="800"}

詳しくは、Cloud Infrastructure ガイドのCommerceにある [&#x200B; ユーザーアクセスの管理 &#x200B;](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html#manage-users-from-the-project-web-interface) ドキュメントを参照してください。

### 共有アカウントへのアクセス （アカウントの切り替え） {#switch-accounts}

>[!NOTE]
>
>この手順は、Adobe Commerceのチケットを送信する場合には必要ありません。
>Adobe Commerce チケットの送信に関するデモについては、[&#x200B; このビデオを参照してください &#x200B;](https://experienceleague.adobe.com/en/playlists/support-requests)。

提供された共有アクセスを使用するには、次の手順に従います。

1. Adobe Commerce アカウント（[https://account.magento.com](https://account.magento.com/)）にログインします。
1. **アカウントを切り替え** メニューをクリックし、アカウントを選択します。

   ![magento-account-shared-switch](/help/adobe-support-tools-guide/assets/magento_account_shared_switch.png){width="800"}

現在使用しているアカウント（独自のネイティブアカウントまたは共有アクセス）を確認するには、**アカウントの切り替え** メニューを参照してください。このメニューには、アクティブなアカウントが表示されます。

### 共有アクセスのトラブルシューティング {#troubleshooting-shared-access}

サポートナレッジベースの [&#x200B; 共有アクセスのトラブルシューティングの記事 &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/shared-access-troubleshooting) を参照してください。


