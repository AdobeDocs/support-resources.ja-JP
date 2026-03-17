---
title: Global Admin Consoleを使用した子組織への製品の割り当て
description: グローバル管理者がリソースを子組織に配布し、各組織内で効果的なリソース管理とユーザー割り当てを可能にする方法を説明します。
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
source-git-commit: 943ddbe1e049e77d502e2da393f7588b10a7a58b
workflow-type: tm+mt
source-wordcount: '1050'
ht-degree: 0%

---

# Global Admin Consoleを使用した子組織への製品の割り当て

エンタープライズに適用します。

グローバル管理者がリソースを子組織に配布し、各組織内で効果的なリソース管理とユーザー割り当てを可能にする方法を説明します。

[Global Admin Console](https://helpx.adobe.com/jp/enterprise/global-admin-console/adopt-global-administration.html) で、「製品割り当て **[!UICONTROL 」タブに移動し、子組織に割り当てる製品を選択します]**

[Global Admin Console](https://adminconsole.adobe.com/support) にサインインします。

>[!NOTE]
>
>**[!UICONTROL 製品の割り当て]** は、エンタープライズ期間ライセンス契約（ETLA）でのみ使用できます。

複数の組織間でAdobe製品を配布および管理する一環として、購入したリソースを複数の管理対象組織間でのリソース割り当てに分割する方法があります。 製品リソースの管理は、リソースの全部または一部を提供することで、他の組織に配布できます。 すべての製品のすべてのリソースを割り当てることができるわけではありません。一部の製品は他の組織に配布できません。 このような製品は「**[!UICONTROL 製品配分]**」タブに表示されますが、他の組織に追加するコントロールはありません。

>[!WARNING]
>
>**期限切れ** または組織が **非アクティブ** 状態の契約から子組織に製品を割り当てることはできません。 [&#x200B; 契約の有効期限 &#x200B;](https://helpx.adobe.com/jp/enterprise/using/contract-expiry.html) の詳細を確認するか、会社の管理者に問い合わせて、子組織のユーザーがAdobeのアプリやサービスにアクセスできなくなるのを防ぎます。

## プールされたストレージ

これは、Admin Consoleに「ストレージ」タブがあるお客様が対象となります。 「ストレージ」タブが表示されない場合は、Admin Consoleがまだエンタープライズストレージモデルに更新されていません。 組織が移行されると、次の変更が表示されます。

- グローバル管理者は、**[!UICONTROL Global Admin Console]** の「Product Allocation[&#x200B; タブを使用して、階層全体のストレージ割り当てと使用状況にアクセスでき &#x200B;](https://adminconsole.adobe.com/) す。
- システム管理者とストレージ管理者は、組織全体のストレージを完全に制御および表示できます。 **[!UICONTROL Adobe Admin Console]** の「[&#x200B; ストレージ &#x200B;](https://adminconsole.adobe.com/)」タブを使用して、ストレージをトラッキングおよび管理できます。

Adobe Creative Cloud ストレージの更新に伴い、組織が購入するストレージ容量を上限として、エンドユーザーに対するストレージの割り当て制限は柔軟に行えます。 [詳細情報](https://helpx.adobe.com/jp/enterprise/using/manage-adobe-storage.html)

## 製品の割り当て

Global Admin Consoleの **[!UICONTROL 商品配分]** タブには、組織階層全体で購入された商品の配分単位が表示されます。 [&#x200B; グローバル管理者 &#x200B;](https://helpx.adobe.com/jp/enterprise/global-admin-console/manage-administrators.html#admins) は、これらの製品リソースを組織ツリー内の別の組織に割り当て、割り当てる数量を指定できます。 [&#x200B; グローバルビューア &#x200B;](https://helpx.adobe.com/jp/enterprise/global-admin-console/manage-administrators.html#admins) の場合は、データの表示と書き出しは可能ですが、更新は行えません。

組織に製品を割り当てるには、次の手順に従います。

1. [Global Admin Console](https://global-admin-console.adobe.com) にサインインし、**[!UICONTROL 製品配分]** に移動します。
1. ドロップダウンリストから製品を選択して、様々な組織への割り当て方法を確認します。\
   組織に現在製品がない場合は、「**[!UICONTROL 追加+]**」アイコンが表示されます。

   >[ !N注意]
   >
   >子組織が既に購入契約を持っている場合、親からその子組織への製品の割り当てが制限される場合があります。 [詳細情報](https://helpx.adobe.com/jp/enterprise/global-admin-console/allocate-products.html#limited-product-allocation)

1. 製品を割り当てるには、関連する組織の **[!UICONTROL 追加+]** アイコンを選択します。\
   一部のプロダクトには複数の割り当て可能リソースが含まれます。この場合、ダイアログボックスには複数のリソースがリストされるので、それぞれのリソースに値を指定する必要があります。 例えば、Adobe Stockには、Adobe Stock画像クレジットとプレミアムクレジットを含めることができます。
   ![Adobe Stock画像 &#x200B;](/help/adobe-support-tools-guide/assets/adobe-stock-images.png)
1. 表示されるダイアログボックスで、製品数量を指定します。
1. 「**[!UICONTROL 保存]**」を選択します。
1. リソースの割り当て超過を許可または禁止するには、関連する切り替えスイッチを選択します。
   ![&#x200B; 割り当て超過 &#x200B;](/help/adobe-support-tools-guide/assets/overallocation.png)
1. リソースの割り当てが完了したら、「**[!UICONTROL 保留中の変更をレビュー]**」を選択します。 レビュー後、「**[!UICONTROL 変更を送信]**」を選択して [&#x200B; 実行 &#x200B;](https://helpx.adobe.com/jp/enterprise/global-admin-console/execute-jobs.html) します。

## Adobe Acrobat Sign ユーザーライセンスまたはトランザクションの割り当てと配布

Global Admin Consoleを使用すると、Acrobat Signのユーザーライセンスやトランザクションを組織全体に割り当てて配布できます。 Acrobat Sign ライセンスまたはトランザクションが割り当てられた階層内の各組織は、それぞれ別のAcrobat Sign アカウントを作成します。

- 作成される各Acrobat Sign アカウントは独立しており、管理とコンテンツの点でサイロ化されています。
- 各Acrobat Sign アカウントは、他のAcrobat Sign アカウント（親組織や姉妹組織など）を認識しません。

詳しくは、[Admin ConsoleでのAdobe Acrobat Signの管理 &#x200B;](https://helpx.adobe.com/jp/enterprise/using/adobe-sign-for-enterprise.html) を参照してください。

Knowledge-based Authentication （KBA）や Phone Authentication （PA）などの認証アドオンを管理するには、Adobe担当者またはカスタマーサクセスマネージャーにお問い合わせください。


## 製品割り当ての制限

次の場合、親組織から子組織への割当ては制限されます。

- 両方の組織の契約が異なり、割り当てようとしている製品が両方に存在する場合、契約間で同じオファーを混在させることはできません。
- 両方の組織で同じ契約がある場合は、Adobeの担当者に問い合わせるか、Global Admin Consoleで [&#x200B; 製品割り当て &#x200B;](https://helpx.adobe.com/jp/enterprise/using/support-for-enterprise.html) がブロックされていると指定して **[!UICONTROL サポートを送信]** して、製品を割り当てる権限をリクエストできます。

## 配分超過

[&#x200B; グローバル管理者 &#x200B;](https://helpx.adobe.com/jp/enterprise/global-admin-console/manage-administrators.html#admins) は、リソースの割り当て超過を許可できます。

製品および組織に関連付けられた配分 [&#x200B; ポリシー &#x200B;](https://helpx.adobe.com/jp/enterprise/global-admin-console/update-policies.html#update-policies) は、割り当て超過が許可されているかどうかを示します。

割り当て超過を使用すると、親組織で使用可能な製品リソースよりも多くの製品リソースを子組織に付与できます。 これは、割り当てが概算であり、管理者がリソース割り当ての合計を維持することに負担をかけたくない場合に役立ちます。
組織内の製品リソースで割り当て超過が無効になっている場合は、子の付与の合計が親の付与を超えることはできません。 割り当て超過が無効になっているリソースを割り当て超過にするリクエストは実行されません。
割り当て超過トグルが有効から無効に切り替えられた場合、リソースの割り当て量内に割り当て超過状況が存在する場合に、割り当て超過アップデートを実行する前に、割り当て超過を解消するように割り当て値を調整する必要があります。

![&#x200B; 割り当て超過 &#x200B;](/help/adobe-support-tools-guide/assets/overallocation.png)

## 階層内の有効期限切れの契約

期限切れのETLA契約から子組織に製品を割り当てることはできません。 次に示すアプリ内バナーおよび通知は、「概要」ページおよび **[!UICONTROL 製品配分]**&#x200B;**&#x200B;** ページに、1 つ以上の子組織の契約がいつ期限切れになるか、期限切れになるか、または非アクティブになるかを示します。

![&#x200B; 製品配分 &#x200B;](/help/adobe-support-tools-guide/assets/product-allocation.png)

>[ !I重要]
>
>階層の一部であるETLA コントラクトが非アクティブになると、その商品は **[!UICONTROL 概要]** ページと **[!UICONTROL 商品配分]** ページから削除されます。

[&#x200B; 契約の有効期限について詳しくは、こちらを参照 &#x200B;](https://helpx.adobe.com/jp/enterprise/using/contract-expiry.html) するか、会社の管理者に問い合わせて、子組織のユーザーがAdobeのアプリやサービスへのアクセス権を失わないようにしてください。
