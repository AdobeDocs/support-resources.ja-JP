---
title: 組織の階層の管理
description: グローバル管理者がGlobal Admin Consoleで組織の階層を管理する方法について説明します。
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: 6fcf16e3-0408-4961-9981-14d526e1ea28
source-git-commit: d5f0473b100cda574b4980e6c871a9c275f9f95a
workflow-type: tm+mt
source-wordcount: '1547'
ht-degree: 0%

---

# 組織の階層の管理

エンタープライズ版に適用されます。

グローバル管理者がGlobal Admin Consoleで組織の階層を管理する方法について説明します。

Global Admin Console[に](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration#request-access-to-the-global-admin-console) アクセスできるようになると、新しい組織を作成したり、既存の組織を階層に追加したり、組織を削除したり、親組織を変更したりできます。 [Global Admin Consoleにログインするには、こちらに移動します](https://global-admin-console.adobe.com/)。

組織とは、Adobe製品とユーザーを管理するために使用される構造です。 [Adobe Admin Console](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/admin-console-overview)を使用すると、管理者は組織内の製品とユーザーのデプロイメントと設定を管理できます。 [Global Admin Console](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration)を使用すると、グローバル管理者は複数の組織を作成、管理、削除できます。

## 子組織の作成

[&#x200B; グローバル管理者](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators)として、階層内の任意の組織の子組織を作成し、名前、国、ユーザーグループ、製品、製品プロファイル、管理者、ポリシーを設定できます。

新しい子組織が作成されると、次の要素が親から自動的に継承されます。

- 組織の[&#x200B; ポリシー](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html)設定（存在する場合はロックを含む）。
- システム管理者のリスト（**[!UICONTROL 作成時にシステム管理者を継承]** [&#x200B; ポリシー](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html)）。
次の手順を実行すると、システム管理者が継承されるのを防ぐことができます。
   - [&#x200B; ドメインの信頼](https://helpx.adobe.com/enterprise/using/directory-trust.html)がありません。
   - ユーザータイプの制限（Adobe ID / Enterprise ID / Federated ID ユーザーポリシーの追加）。 [&#x200B; ポリシーの詳細](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html)について説明します。
- 親組織がアクセスできるドメインからFederated IDまたはEnterprise ID ユーザーへのアクセス。 これにより、親内のドメインユーザーを子組織で使用できるようになります。 ユーザーアクセスの継承は、**親組織が管理するディレクトリからユーザーを継承** [&#x200B; ポリシー](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html)によって制御されます。
- 共有ポリシー、パスワードポリシー、およびセキュリティ連絡先（**によって管理）子組織の作成時にアセット共有設定を継承** [&#x200B; ポリシー](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html)）。

1. [Global Admin Console](https://global-admin-console.adobe.com/)にログインします。 「**[!UICONTROL 組織]**」タブで、子組織を追加する組織を選択します。
2. 「**[!UICONTROL 追加+]**」アイコンを選択します。
   ![組織を追加](/help/adobe-support-tools-guide/assets/add-an-organization-1.png)
3. 組織の&#x200B;**name**&#x200B;と&#x200B;**country**&#x200B;を指定します。\
   組織のシンプルな名前は4 ～ 100文字にする必要があります。パス名の最大長は255文字です。
   ![子組織を追加](/help/adobe-support-tools-guide/assets/add-a-child-organization.png)
4. 「**[!UICONTROL 保存]**」を選択します。
5. 組織の編集が完了したら、「**[!UICONTROL 保留中の変更を確認]**」を選択します。 レビュー後、**[!UICONTROL 変更を送信]**&#x200B;から[実行](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)を選択します。

## 子組織の削除

[&#x200B; グローバル管理者](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators)として、子組織を削除できます。 削除操作を元に戻すことはできず、ルート組織を削除することはできません。 削除された組織に割り当てられたリソースは、その親組織に返されます。 組織が削除される前に、その親は自動的にその子組織の親になります。

組織は、次の条件を満たす場合にのみ削除できます。

- 組織内にSign アカウント、Adobe Stockの購入、またはストレージリポジトリはありません。
- 組織内にクレームされたドメインはありません。
- 組織内にインスタンス化された製品はありません。
- 組織内にインスタンスを含めることができるExperience Cloud製品はありません。

>[!WARNING]
>
>組織を削除すると、ユーザーに影響が及びます。 組織が削除されたときに失われるアクセスまたは情報がないことを確認します。

1. [Global Admin Console](https://global-admin-console.adobe.com/)にログインします。 「**[!UICONTROL 組織]**」タブに移動し、削除する組織を選択します。
1. 「**[!UICONTROL 削除]**」アイコンを選択します。
   ![組織を削除](/help/adobe-support-tools-guide/assets/delete-organization.png)
1. **[!UICONTROL 組織を削除]** ダイアログボックスで、**[!UICONTROL OK]**&#x200B;を選択します。
1. 組織の編集が完了したら、「**[!UICONTROL 保留中の変更を確認]**」を選択します。 レビュー後、**[!UICONTROL 変更を送信]**&#x200B;から[実行](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)を選択します。

## 組織の名前の変更

組織名は、購入時に設定した会社または機関の正式な名前です。 ユーザーは、ログイン時にプロファイルを選択する際にこの名前を表示します。特に、複数の組織からAdobe製品にアクセスできる場合や、ビジネスプロファイルと個人プロファイルのどちらかを選択する必要がある場合に表示されます。

[&#x200B; グローバル管理者](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators)は、任意の親または子組織の名前を編集して、Creative Cloud製品およびサービスにログインする際に正しいプロファイルをユーザーが特定できるようにすることができます。

1. [Global Admin Console](https://global-admin-console.adobe.com/)にログインします。 「**[!UICONTROL 組織]**」タブで、名前を変更する組織を選択します。
1. 「**[!UICONTROL 編集]**」アイコンを選択します。
   ![組織の名前を変更](/help/adobe-support-tools-guide/assets/rename-organization.png)
1. 組織名を更新し、**[!UICONTROL 保存]**&#x200B;を選択します。

>[!TIP]
>
>ユーザーが適切なプロファイルを選択できるように、明確で認識可能な組織名を最大255文字まで使用します。 特殊文字を使用することは避け、地域、部署、または使用権限を含めることを検討してください。 また、組織の階層全体で、一般的ではない頭字語や、あいまいな名前や類似する名前を使用することは避けましょう。

変更は監査ログに記録され、すべてのユーザーに電子メールで通知され、名前を24時間更新することはできません。 [監査ログの表示およびダウンロード方法について説明します](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/download-audit-logs-and-export-reports)。

## 組織の親を変更

[&#x200B; グローバル管理者](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators)は、**[!UICONTROL 階層を変更]** ボタンを使用して、組織階層の組織を再ペアレント化できます。

組織の親を変更すると、次のような影響があります。

- 組織を再ペアレント化すると、その組織を持つサブツリー全体が再ペアレント化された組織にルート化されます。 親子関係にある組織とその子のパス名が、新しい場所を反映するように更新されます。
- 移動した組織の組織[&#x200B; ポリシー](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html)が更新され、ポリシーに対するロックが新しい階層の組織によって保持されるようになります。
- 階層内の組織の位置を変更すると、その組織のグローバル管理者を変更できます。 グローバル管理ロールは階層に継承されるため、新しい親組織のグローバル管理者は自動的に移動された組織のグローバル管理者になります。 同様に、グローバル管理者が古い親のグローバル管理者であることによってその役割を持っていた場合、移動された組織での役割を失う可能性があります。 継承されたグローバル管理の役割は、組織の管理者ペインには表示されません。
- リペアレンティングは、移動した組織で使用可能な製品にも影響します。 可能であれば、[製品割り当て](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html)が更新され、新しい親の場所を介して割り当てられます。
- 製品の割り当てを新しい親から更新できない場合、製品は、それらの製品の製品プロファイルと共に削除されます。 この操作の結果、ユーザーがアクセスを失う可能性があります。 製品を新しい場所で使用できるようにするには、古い場所と新しい場所の最も近い共通の祖先に製品が使用可能である必要があります。

>[!WARNING]
>
>親子関係の変更の結果として製品が削除された場合、ユーザーはそれらの製品にアクセスできなくなります。

1. [Global Admin Console](https://global-admin-console.adobe.com/)にログインします。 「**[!UICONTROL 組織]**」タブで、**[!UICONTROL 階層を変更]**&#x200B;を選択して、組織の親子変更を有効にします。
2. 表示されるポップアップ画面で「**[!UICONTROL OK]**」を選択します。
3. 再親にするには、目的の組織の上に子組織をドラッグします。
4. 組織の親子関係の変更が完了したら、**[!UICONTROL 保存]**&#x200B;を選択します。
5. 組織の編集が完了したら、「**[!UICONTROL 保留中の変更を確認]**」を選択します。 レビュー後、**[!UICONTROL 変更を送信]**&#x200B;から[実行](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)を選択します。

ジョブが完了したら、「製品割り当て」に移動し、[付与値](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html)を変更して、製品リソースの割り当ての変更を反映できます。

## 組織マッパーを使用した既存の組織の追加

[&#x200B; グローバル管理者](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators)は、現在Global Admin Console階層に含まれていない既存の組織を組織階層に追加できます。

組織階層にチーム組織を追加することもできます。 チーム組織は、製品の割り当てや製品の使用状況のロールアップには参加せず、Global Admin Consoleでのチーム組織の管理は限られています。 それらを組織階層に追加して追跡し、購入した製品を可視化することができます。 チーム組織では、その下に子の組織を配置することはできず、エンタープライズ組織の機能の多くはありません。

製品割り当ての[制限](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html#limitations)について詳しく説明します。

>[!WARNING]
>
> 同じストレージモデルに基づくルート組織にのみ、子組織を追加できます。 したがって、ユーザーストレージモデルに基づく子組織は、ユーザーストレージモデルに基づくルート組織にのみ追加できます。 また、エンタープライズストレージモデルに基づく子組織は、エンタープライズストレージモデルに基づくルート組織にのみ追加できます。

「**[!UICONTROL 組織マッパー]**」タブには、次の情報が表示されます。

1. 子組織を追加できる可能性のある親組織のリストを含むドロップダウン。 これらは、あなたがグローバル管理者である組織です。
1. 手順1で選択した親の下に追加できる子組織のリスト。 これらの組織は、システム管理者であり、まだ別の組織の子ではない組織です。

組織がグローバル管理に追加されると、組織マッパーを使用して追加された組織内の製品は購入として残ります。[製品割り当て](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html)番号は、これらの組織でロールアップを停止します。

1. [Global Admin Console](https://global-admin-console.adobe.com/)にログインし、**[!UICONTROL 組織マッパー]**&#x200B;に移動します。
2. ドロップダウンリストから親組織を選択します。\
   これらは、グローバル管理者として直接追加される組織です。 ドロップダウンリストで、親として使用する組織が表示されない場合は、階層内で上位の組織を1つ選択します。 組織マッパー操作が完了したら、[階層を変更](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/set-up-organizations#change-the-parent-of-an-organization)して、新しい組織をツリー内で下に移動し、使用する親を持たせることができます。
3. 前の手順で選択した組織の子として追加する組織を選択します。
4. 「**[!UICONTROL 保留中の変更を確認]**」を選択します。 次に、**[!UICONTROL 変更を送信]**&#x200B;から[実行](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)を選択します。
5. 変更を実行した後、上記の手順を繰り返して、組織の階層に子組織を追加できます。

組織が階層に属したら、「**[!UICONTROL 組織]**」タブに移動して、組織のポリシー、管理者、またはその他の設定を調整できます。
