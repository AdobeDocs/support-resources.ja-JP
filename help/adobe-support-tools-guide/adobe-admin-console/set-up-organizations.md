---
title: 組織階層の管理
description: グローバル管理者がGlobal Admin Consoleで組織の階層を管理する方法について説明します。
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
source-git-commit: 3b3b2711887f0db086e4eb8281344cc7356accf7
workflow-type: tm+mt
source-wordcount: '1626'
ht-degree: 0%

---

# 組織階層の管理

エンタープライズに適用します。

グローバル管理者がGlobal Admin Consoleで組織の階層を管理する方法について説明します。

[&#x200B; へのアクセス  [!DNL Global Admin Console]](https://helpx.adobe.com/jp/enterprise/global-admin-console/adopt-global-administration.html#request-access) を取得したら、新しい組織の作成、既存の組織の階層への追加、組織の削除、親組織の変更を行うことができます。
[Global Admin Consoleへのログイン &#x200B;](https://global-admin-console.adobe.com/)

組織は、Adobeの製品とユーザーの管理に使用される構造です。 [[!DNL Adobe Admin Console]](https://helpx.adobe.com/jp/enterprise/using/admin-console.html) を使用すると、管理者は組織内の製品とユーザーのデプロイメントおよび設定を管理できます。 [[!DNL Global Admin Console]](https://helpx.adobe.com/jp/enterprise/global-admin-console/overview.html) を使用すると、グローバル管理者が複数の組織を作成、管理および削除できます。

## 子組織の作成

[&#x200B; グローバル管理者 &#x200B;](https://helpx.adobe.com/jp/enterprise/global-admin-console/manage-administrators.html) は、階層内の任意の組織の子組織を作成し、名前、国、ユーザーグループ、製品、製品プロファイル、管理者およびポリシーを設定できます。

新しい子組織が作成されると、以下が直近の親から自動的に継承されます。

- 組織の [&#x200B; ポリシー &#x200B;](https://helpx.adobe.com/jp/enterprise/global-admin-console/update-policies.html) 設定（ある場合はロックを含む）。
- システム管理者のリスト （**[!UICONTROL 作成時にシステム管理者を継承]**&#x200B;[&#x200B; ポリシー &#x200B;](https://helpx.adobe.com/jp/enterprise/global-admin-console/update-policies.html) で制御）。
次の場合、システム管理者が継承されない可能性があります。
   - [&#x200B; ドメインの信頼 &#x200B;](https://helpx.adobe.com/jp/enterprise/using/directory-trust.html) がない。
   - ユーザータイプの制限（Adobe ID/Enterprise ID/Federated ID ユーザーポリシーを追加）。 [&#x200B; ポリシー詳細 &#x200B;](https://helpx.adobe.com/jp/enterprise/global-admin-console/update-policies.html) について説明します。
- 親組織がアクセス権を持つドメインの [[!DNL Federated ID]] または [[!DNL Enterprise ID]] ユーザーにアクセスします。 これにより、親組織のドメインユーザーが子組織で使用できるようになります。 ユーザーアクセスの継承は、**親組織が管理するディレクトリからユーザーを継承** ポリシー [&#x200B; によって制御 &#x200B;](https://helpx.adobe.com/jp/enterprise/global-admin-console/update-policies.html) されます。
- 共有ポリシー、パスワードポリシー、およびセキュリティの連絡先（**子組織の作成時にアセット共有設定を継承**&#x200B;[&#x200B; ポリシー &#x200B;](https://helpx.adobe.com/jp/enterprise/global-admin-console/update-policies.html) で制御）。

1. [Global Admin Console](https://global-admin-console.adobe.com/) にサインインします。 「**[!UICONTROL 組織]**」タブで、子組織を追加する組織を選択します。
2. **[!UICONTROL 追加+]** アイコンを選択します。
   ![&#x200B; 組織を追加 &#x200B;](/help/adobe-support-tools-guide/assets/add-an-organization-1.png)
3. 組織の **名前** と **国** を指定します。\
   組織のシンプルな名前は 4 ～ 100 文字にする必要があります。パス名の最大長は 255 文字です。
   ![&#x200B; 子組織を追加 &#x200B;](/help/adobe-support-tools-guide/assets/add-an-child-organization.png)
4. 「**[!UICONTROL 保存]**」を選択します。
5. 組織の編集が完了したら、「**[!UICONTROL 保留中の変更をレビュー]**」を選択します。 レビュー後、「**[!UICONTROL 変更を送信]**」を選択して [&#x200B; 実行 &#x200B;](https://helpx.adobe.com/jp/enterprise/global-admin-console/execute-jobs.html) します。

## 子組織の削除

[&#x200B; グローバル管理者 &#x200B;](https://helpx.adobe.com/jp/enterprise/global-admin-console/manage-administrators.html) は、子組織を削除できます。 削除操作は元に戻すことができず、ルート組織は削除できません。 削除した組織に割り当てられたリソースは、その親組織に返されます。 組織が削除される前に、その親は自動的に任意の子組織の親になります。

組織は、次の条件を満たした場合にのみ削除できます。

- 組織内に Sign アカウント、Adobe Stock購入またはストレージリポジトリはありません。
- 組織内に要求されたドメインはありません。
- 組織にインスタンス化された製品がありません。
- インスタンス化を組み込むことができるExperience Cloud製品が組織にありません。

>[!WARNING]
>
>組織を削除すると、ユーザーに影響が及びます。 組織を削除してもアクセス権や情報が失われないことを確認します。

1. [[!DNL Global Admin Console]](https://global-admin-console.adobe.com/) にログインします。 「**[!UICONTROL 組織]**」タブに移動し、削除する組織を選択します。
1. **[!UICONTROL 削除]** アイコンを選択します。
   ![&#x200B; 組織を削除 &#x200B;](/help/adobe-support-tools-guide/assets/delete-organization.png)
1. **[!UICONTROL 組織を削除]** ダイアログボックスで「**[!UICONTROL OK]**」を選択します。
1. 組織の編集が完了したら、「**[!UICONTROL 保留中の変更をレビュー]**」を選択します。 レビュー後、「**[!UICONTROL 変更を送信]**」を選択して [&#x200B; 実行 &#x200B;](https://helpx.adobe.com/jp/enterprise/global-admin-console/execute-jobs.html) します。

## 組織名の変更

組織名は、購入時に設定された、会社または機関の正式名称です。 この名前は、ログイン時にプロファイルを選択するときに表示されます。特に、複数の組織のAdobe製品にアクセスできる場合や、ビジネスプロファイルと個人プロファイルのどちらかを選択する必要がある場合に表示されます。

[&#x200B; グローバル管理者 &#x200B;](https://helpx.adobe.com/jp/enterprise/global-admin-console/manage-administrators.html) は、ユーザーが [[!DNL Creative Cloud]] 製品およびサービスにサインインする際に正しいプロファイルを識別できるように、親または子組織の名前を編集できます。

1. [Global Admin Console](https://global-admin-console.adobe.com/) にサインインします。 「**[!UICONTROL 組織]**」タブで、名前を変更する組織を選択します。
1. **[!UICONTROL 編集]** アイコンを選択します。
   ![&#x200B; 組織名を変更 &#x200B;](/help/adobe-support-tools-guide/assets/rename-organization.png)
1. 組織名を更新し、「**[!UICONTROL 保存]**」を選択します。

>[!TIP]
>
>ユーザーが正しいプロファイルを選択できるように、明確でわかりやすい組織名（最大 255 文字）を使用します。 特殊文字の使用を避け、地域、部門、使用権限を含めることを検討してください。 また、組織の階層全体で一般的でない頭字語や、あいまいな名前や類似した名前は使用しないでください。
>ユーザーが正しいプロファイルを選択できるように、明確でわかりやすい組織名（最大 255 文字）を使用します。 特殊文字の使用を避け、地域、部門、使用権限を含めることを検討してください。 また、組織の階層全体で一般的でない頭字語や、あいまいな名前や類似した名前は使用しないでください。

変更は監査ログに記録され、すべてのユーザーにメールで通知され、名前は 24 時間更新できません。 [&#x200B; 監査ログの表示方法とダウンロード方法を説明します &#x200B;](https://helpx.adobe.com/jp/enterprise/global-admin-console/insights.html)。

## 組織の親の変更

一 [[!DNL Global Administrator]](https://helpx.adobe.com/jp/enterprise/global-admin-console/manage-administrators.html)、「階層を変更 **[!UICONTROL ボタンを使用して、組織階層内の組織の親を変更でき]** す。

組織の親を変更すると、次のような影響があります。

- 組織の親を変更すると、その親を変更した組織をルートとするサブツリー全体が移動します。 親が変更された組織とその子のパス名が、新しい場所を反映するように更新されます。
- 移動した組織の組織 [&#x200B; ポリシー &#x200B;](https://helpx.adobe.com/jp/enterprise/global-admin-console/update-policies.html) が更新され、新しい階層内の組織でポリシーのロックが保持されます。
- 階層内の組織の位置を変更すると、その組織のグローバル管理者が変更される場合があります。 グローバル管理の役割は階層の下位に継承されるので、新しい親組織のグローバル管理者は移動した組織のグローバル管理者になります。 同様に、グローバル管理者が古い親のグローバル管理者になることで、移動した組織での役割を失う可能性があります。 継承されたグローバル管理の役割は、組織の管理者ウィンドウに表示されません。
- 再ペアレント化は、移動した組織内の使用可能な製品にも影響します。 可能な場合は、[&#x200B; 製品割り当て &#x200B;](https://helpx.adobe.com/jp/enterprise/global-admin-console/allocate-products.html) が更新され、新しい親の場所から取得されます。
- 製品の割り当てを新しい親から取得するように更新できない場合、製品は、それらの製品の製品プロファイルと共に削除されます。 この操作の結果、ユーザーはアクセス権を失う可能性があります。 新しい場所で製品を使用できるようにするには、古い場所と新しい場所の最も近い共通の上位にある製品が使用可能である必要があります。

>[!WARNING]
>
>再ペアレント化の結果として製品が削除されると、ユーザーはそれらの製品にアクセスできなくなります。

1. [Global Admin Console](https://global-admin-console.adobe.com/) にサインインします。 「**[!UICONTROL 組織]**」タブで、「**[!UICONTROL 階層を変更]**」を選択して組織の再ペアレント化を有効にします。
2. 表示され **[!UICONTROL ポップアップ画面で「OK]**」を選択します。
3. 親を変更するには、子組織を目的の組織の上にドラッグします。
4. 組織の親の変更が完了したら、「**[!UICONTROL 保存]**」を選択します。
5. 組織の編集が完了したら、「**[!UICONTROL 保留中の変更をレビュー]**」を選択します。 レビュー後、「**[!UICONTROL 変更を送信]**」を選択して [&#x200B; 実行 &#x200B;](https://helpx.adobe.com/jp/enterprise/global-admin-console/execute-jobs.html) します。

ジョブが完了したら、「製品割当」にナビゲートして [&#x200B; 付与値を変更 &#x200B;](https://helpx.adobe.com/jp/enterprise/global-admin-console/allocate-products.html) し、製品リソースの割当の変更を反映できます。

## 組織マッパーを使用した既存の組織の追加

[&#x200B; グローバル管理者 &#x200B;](https://helpx.adobe.com/jp/enterprise/global-admin-console/manage-administrators.html) の場合、現在Global Admin Consoleの階層に含まれていない既存の組織を組織階層に追加できます。

組織階層にチーム組織を追加することもできます。 チーム組織は、製品配分や製品使用状況のロールアップには関与せず、Global Admin Consoleでのチーム組織の管理は制限されます。 これらを組織階層に追加して追跡し、購入した製品を可視化できます。 チーム組織は、その下に子組織を持つことができず、企業組織の機能の多くを持っていません。

詳しくは、[&#x200B; 製品配分の制限 &#x200B;](https://helpx.adobe.com/jp/enterprise/global-admin-console/allocate-products.html#limitations) を参照してください。

>[!WARNING]
>
> 子組織は、同じストレージモデルに基づくルート組織にのみ追加できます。 したがって、ユーザーストレージモデルに基づく子組織は、ユーザーストレージモデルに基づくルート組織にのみ追加できます。 また、エンタープライズストレージモデルに基づく子組織は、エンタープライズストレージモデルに基づくルート組織にのみ追加できます。
>子組織は、同じストレージモデルに基づくルート組織にのみ追加できます。 したがって、ユーザーストレージモデルに基づく子組織は、ユーザーストレージモデルに基づくルート組織にのみ追加できます。 また、エンタープライズストレージモデルに基づく子組織は、エンタープライズストレージモデルに基づくルート組織にのみ追加できます。

**[!UICONTROL 組織マッパー]** タブには、次の情報が表示されます。

1. 子組織を追加できる、可能な親組織のリストを含むドロップダウン。 これらは、グローバル管理者が対象となる組織です。
1. 手順 1 で選択した親の下に追加できる子組織のリスト。 自分がシステム管理者であり、まだ別の組織の子ではない組織です。

組織がグローバル管理に追加されると、組織マッパーを使用して追加された組織内の製品は購入として残ります。[&#x200B; 製品配分 &#x200B;](https://helpx.adobe.com/jp/enterprise/global-admin-console/allocate-products.html) の数値は、これらの組織でのロールアップを停止します。

1. [Global Admin Console](https://global-admin-console.adobe.com/) にサインインし、**[!UICONTROL Organization Mapper]** に移動します。
2. ドロップダウンリストから親組織を選択します。\
   これらは、グローバル管理者として直接追加される組織です。 ドロップダウンリストに、親として使用する組織が表示されていない場合は、階層の上位の組織を選択します。 組織マッパーの操作が完了したら、[&#x200B; 階層を変更 &#x200B;](https://helpx.adobe.com/jp/enterprise/global-admin-console/set-up-organizations.html#change-the-parent-of-an-organization) を使用して、新しい組織をツリー内で下に移動し、親を使用できるようにします。
3. 前の手順で選択した組織の子として追加する組織を選択します。
4. 「**[!UICONTROL 保留中の変更を確認]**」を選択します。 次に、「変更を送信 **[!UICONTROL を選択して]** 実行 [&#x200B; し &#x200B;](https://helpx.adobe.com/jp/enterprise/global-admin-console/execute-jobs.html) す。
5. 変更を実行した後、上記の手順を繰り返して、組織階層に子組織を追加できます。

組織が階層に入ったら、「**[!UICONTROL 組織]**」タブに移動して、組織のポリシー、管理者、その他の設定を調整できます。
