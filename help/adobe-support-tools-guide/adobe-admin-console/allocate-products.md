---
title: Global Admin Consoleを使用して製品を子組織に割り当てる
description: グローバル管理者がリソースを子組織に配布し、各組織内で効果的なリソース管理とユーザー割り当てを可能にする方法について説明します。
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: de6e785d-8965-40d5-ac78-7fbb2cd7afc7
source-git-commit: d5f0473b100cda574b4980e6c871a9c275f9f95a
workflow-type: tm+mt
source-wordcount: '1050'
ht-degree: 0%

---

# Global Admin Consoleを使用して製品を子組織に割り当てる

エンタープライズ版に適用されます。

グローバル管理者がリソースを子組織に配布し、各組織内で効果的なリソース管理とユーザー割り当てを可能にする方法について説明します。

[Global Admin Console](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration)で、**[!UICONTROL Product Allocation]** タブに移動し、子組織に割り当てる商品を選択します。

[Global Admin Console](https://global-admin-console.adobe.com)にログインします。

>[!NOTE]
>
>**[!UICONTROL 製品割り当て]**&#x200B;は、エンタープライズ期間使用許諾契約（ETLA）契約でのみ使用できます。

Adobe製品を組織全体で配布および管理する一環として、購入したリソースを組織全体のリソース割り当てに分割して管理します。 リソースの全部または一部を割り当てることで、製品リソースの管理を他の組織に配布できます。 すべての製品のすべてのリソースを割り当てることができるわけではありません。一部の製品は他の組織に配布できません。 このような製品は、**[!UICONTROL 製品割り当て]** タブに表示されますが、他の組織に追加するための管理機能はありません。

>[!WARNING]
>
>**期限切れ**&#x200B;の契約、または&#x200B;**非アクティブ**&#x200B;状態の契約から、子組織に製品を割り当てることはできません。 [契約の有効期限](https://helpx.adobe.com/enterprise/using/contract-expiry.html)の詳細を確認するか、会社の管理者に問い合わせて、子組織内のユーザーがAdobe アプリやサービスにアクセスできなくなる問題を回避するためのサポートを受けてください。

## プールされたストレージ

これは、Admin Consoleに「ストレージ」タブがあるお客様に適用されます。 「ストレージ」タブが表示されない場合、Admin Consoleはまだエンタープライズストレージモデルに更新されていません。 組織を移行すると、次の変更が表示されます。

- グローバル管理者は、階層全体でストレージの割り当てと使用状況にアクセスでき、**[!UICONTROL Global Admin Console]**&#x200B;の「[製品割り当て](https://adminconsole.adobe.com/)」タブを使用して組織にストレージを割り当てることができます。
- システム管理者とストレージ管理者は、組織全体でストレージを完全に制御し、可視化できます。 **[!UICONTROL Adobe Admin Console]**&#x200B;の「[Storage](https://adminconsole.adobe.com/)」タブを使用して、ストレージを追跡および管理できます。

Adobe Creative Cloud ストレージのアップデートにより、エンドユーザーは、組織が購入するストレージの量まで、ストレージの割り当てが柔軟になります。 [詳細情報](https://helpx.adobe.com/enterprise/using/manage-adobe-storage.html)

## 製品の割り当て

Global Admin Consoleの「**[!UICONTROL 製品割り当て]**」タブには、組織階層で購入された製品の割り当て単位が表示されます。 [&#x200B; グローバル管理者](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators#admins)として、これらの製品リソースを組織ツリー内の別の組織に割り当て、割り当て量を指定できます。 [&#x200B; グローバルビューア &#x200B;](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators#admins)として、データを表示および書き出すことができますが、更新はできません。

製品を組織に割り当てるには、次の手順に従います。

1. [Global Admin Console](https://global-admin-console.adobe.com)にログインし、**[!UICONTROL Product Allocation]**&#x200B;に移動します。
1. ドロップダウンリストから製品を選択して、様々な組織に割り当てられている製品を確認します。\
   組織に製品がない場合は、**[!UICONTROL 追加+]** アイコンが表示されます。

   >[ !N注意]
   >
   >子組織に既に購入契約がある場合、親からその子組織への製品割り当てが制限される場合があります。 [詳細情報](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html#limited-product-allocation)

1. 製品を割り当てるには、関連する組織の「**[!UICONTROL 追加+]**」アイコンを選択します。\
   一部の製品には、複数の割り当て可能なリソースが含まれています。この場合、ダイアログボックスに複数のリソースが一覧表示され、それぞれに値を指定する必要があります。 例えば、Adobe Stockには、Adobe Stock画像クレジットとプレミアムクレジットを含めることができます。
   ![Adobe Stock Images](/help/adobe-support-tools-guide/assets/adobe-stock-images.png)
1. 表示されるダイアログボックスで、製品数量を指定します。
1. 「**[!UICONTROL 保存]**」を選択します。
1. リソースの割り当て超過を許可または禁止するには、関連する切り替えスイッチを選択します。
   ![割り当て超過](/help/adobe-support-tools-guide/assets/overallocation.png)
1. リソースの割り当てが完了したら、「**[!UICONTROL 保留中の変更を確認]**」を選択します。 レビュー後、**[!UICONTROL 変更を送信]**&#x200B;から[実行](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)を選択します。

## Adobe Acrobat Sign ユーザーライセンスまたはトランザクションの割り当てと配布

Global Admin Consoleでは、Acrobat Sign ユーザーライセンスまたはトランザクションを組織階層に割り当てて配布できます。 Acrobat Sign ライセンスまたはトランザクションが割り当てられている階層内の各組織は、独自の個別のAcrobat Sign アカウントを作成します。

- Acrobat Signのアカウントは、それぞれ独立しており、管理やコンテンツの面で分断されています。
- 各Acrobat Sign アカウントは、他のAcrobat Sign アカウント（例えば、親組織や姉妹組織）を認識しません。

Admin Consoleでの[Adobe Acrobat Signの管理について詳しくは、](https://helpx.adobe.com/enterprise/using/adobe-sign-for-enterprise.html)を参照してください。

ナレッジベース認証（KBA）や電話認証（PA）などの認証アドオンを管理するには、Adobe担当者またはカスタマーサクセスマネージャーにお問い合わせください。


## 製品割り当ての制限

親組織から子組織への割り当ては、次の場合に制限されます。

- 両方の組織が異なる契約を持っていて、割り当てようとしている製品が両方に存在する場合、契約間で同じオファーを混在させることはできません。
- 両方の組織が同じ契約を結んでいる場合は、Adobeの担当者に連絡するか、[Global Admin Consoleの](https://helpx.adobe.com/enterprise/using/support-for-enterprise.html)製品割り当て&#x200B;**[!UICONTROL がブロックされていることを示すサポート]** ケースを送信することで、製品の割り当て権限をリクエストできます。

## 過剰配分

[&#x200B; グローバル管理者](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators#admins)として、リソースの割り当て超過を許可できます。

製品と組織に関連付けられた配分[&#x200B; ポリシー](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html#update-policies)は、過剰配分が許可されているかどうかを示します。

割り当て超過を使用すると、親組織で使用できる以上の製品リソースを子組織に付与できます。 割り当てが近似値で、リソース割り当てを追加したまま管理者に負担をかけたくない場合に便利です。
組織内の製品リソースに対して割り当て超過が無効になっている場合、子付与の合計は親付与を超えることはできません。 割り当て超過が無効になっているリソースを割り当て超過するリクエストは実行されません。
割り当て超過トグルが「有効」から「無効」に切り替わった場合、リソースの割り当て超過量に割り当て超過状況が存在する場合、割り当て更新を実行する前に、割り当て超過を排除するために割り当て値を調整する必要があります。

![割り当て超過](/help/adobe-support-tools-guide/assets/overallocation.png)

## 階層内の期限切れ契約

期限切れのETLA コントラクトから子組織に製品を割り当てることはできません。 **[!UICONTROL 概要]**&#x200B;および&#x200B;**[!UICONTROL 製品割り当て]** ページのアプリ内バナーと通知は、1つ以上の子組織の契約が期限切れになるか、期限切れになるか、非アクティブになるかを明確に示します。

![製品の割り当て](/help/adobe-support-tools-guide/assets/product-allocation.png)

>[ !I重要]
>
>階層の一部であるETLA コントラクトが非アクティブになると、製品は&#x200B;**[!UICONTROL 概要]**&#x200B;および&#x200B;**[!UICONTROL 製品割り当て]** ページから削除されます。

[契約の有効期限](https://helpx.adobe.com/enterprise/using/contract-expiry.html)について詳しくは、会社の管理者にお問い合わせいただくか、子組織内のユーザーがAdobe アプリやサービスにアクセスできなくなる問題についてサポートを受けてください。
