---
title: Global Admin Consoleでのユーザーグループの管理
description: Global Admin Consoleでユーザーグループを作成、共有、編集、削除して、組織全体のユーザー管理を効率化する方法について説明します。
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: f81a20fd6d9d64443f4708b3fc17de7240d1bc61
workflow-type: tm+mt
source-wordcount: '1330'
ht-degree: 0%

---


# Global Admin Consoleでのユーザーグループの管理

Global Admin Consoleでユーザーグループを作成、管理、共有し、同じ権限を持つユーザーをグループ化することで、ユーザー管理を効率化し、時間を節約し、一貫性を確保します。

[Global Admin Console](https://helpx.adobe.com/enterprise/global-admin-console/adopt-global-administration.html) で、組織を選択し、**[!UICONTROL ユーザーグループ]** に移動します。 単一のユーザー管理ソースを使用して複数の組織間でグループを共有し、ユーザーとグループを同期します。

[Global Admin Consoleへのログイン &#x200B;](https://global-admin-console.adobe.com)



## ユーザーグループの作成

[&#x200B; ユーザーグループを個別に作成 &#x200B;](https://helpx.adobe.com/jp/enterprise/using/user-groups.html) するか、一括で作成するか、[&#x200B; 確立されたAzure AD からAdobe Admin Consoleのフェデレーティッドディレクトリに直接同期 &#x200B;](https://helpx.adobe.com/enterprise/using/add-azure-sync.html) することができます。 Global Admin Consoleでは、関連する製品プロファイルが割り当てられたユーザーグループを定義でき、ユーザーグループ管理者は後でAdmin Consoleを使用してユーザーを追加できます。

1. [Global Admin Console](https://global-admin-console.adobe.com/) にサインインし、編集する組織を選択して、「**[!UICONTROL ユーザーグループ]**」タブに移動します。

2. 「**[!UICONTROL ユーザーグループを追加]**」を選択します。

   ![Global Admin Consoleの「組織」タブで、「ユーザーグループ」タブが選択されています。](assets/add-user-group.png " ユーザーグループを追加 ")

   _組織にユーザーグループを追加して、ユーザー管理を効率化する_

3. 表示される **[!UICONTROL ユーザーグループを追加]** ダイアログボックスに以下を入力します。
   - **[!UICONTROL 名前]**：ユーザーグループの名前を指定します。
   - **[!UICONTROL 製品プロファイル]**：ユーザーグループの現在または将来のメンバーに製品へのアクセスを付与する場合は、ドロップダウン矢印をクリックしてリストから製品プロファイルを選択するか、製品プロファイル名を入力して表示されるドロップダウンリストから選択します。 まだ作成されていない製品プロファイルを追加する場合は、まず「[&#x200B; 製品プロファイル &#x200B;](https://helpx.adobe.com/enterprise/using/global-admin-edit-organizations.html#profiles) タブを使用する必要があります。
   - **[!UICONTROL 管理者]**：ドロップダウン矢印をクリックしてリストから管理者を選択するか、管理者のメールアドレスを入力して表示されるドロップダウンリストから選択します。 まだ作成されていない新しい管理者を追加する場合は、まず「[&#x200B; 管理者 &#x200B;](#share-user-groups) タブを使用してその管理者を作成する必要があります。

   指定した製品プロファイルはユーザーグループに割り当てられ、指定した管理者はグループのユーザーグループ管理者になります。 ユーザーグループ管理者は、関連する組織のAdobe Admin Consoleを使用してグループを管理できます。

4. 「**[!UICONTROL 保存]**」を選択します。

5. 「**[!UICONTROL 保留中の変更を確認]**」を選択して、更新を確認します。 次に、「変更を送信 **&#x200B;**&#x200B;を選択して [&#x200B; 実行 &#x200B;](https://helpx.adobe.com/enterprise/global-admin-console/set-up-organizations.html#execute-jobs) します。

   >[!NOTE]
   >
   >グローバル管理者は、Global Admin Consoleを使用して、ユーザーグループに [&#x200B; 製品プロファイルとユーザーグループ管理者の割り当て &#x200B;](#review-user-groups) を割り当てることができます。 Adobe Admin Consoleを使用すると、システム管理者とユーザーグループ管理者は [&#x200B; ユーザーの追加と、管理者と製品プロファイルの割り当て &#x200B;](https://helpx.adobe.com/jp/enterprise/using/user-groups.html) ユーザーグループに対して行うことができます。



## ユーザーグループの共有

グループ投影を使用すると、ユーザーグループとそれに関連するユーザーを、単一の管理ソースから複数の Admin Console に同期できます。 グローバル管理者は、上位や並列ではなく下位で動作するソース組織の階層の子孫を持つユーザーグループを共有できます。

1. [Global Admin Console](https://global-admin-console.adobe.com/) にログインし、組織を選択して、「**[!UICONTROL ユーザーグループ]**」タブに移動します。

2. 共有するユーザーグループのチェックボックスを選択します。

   グループの共有が無効になるのは、次の場合です。
   - ユーザーグループは別の組織で共有されています。 グループを共有または編集するには、グループを所有する組織を組織階層から選択します。
   - 組織は [Adobe storage for business](https://helpx.adobe.com/in/enterprise/using/storage-for-business.html) を使用していません。このストレージは段階的にグローバルに展開されています。
   - 組織ポリシーが無効です。 「**[!UICONTROL ポリシー]**」タブに移動して、**[!UICONTROL 共有ユーザーグループの管理]** ポリシーを有効にします。
   - この組織には、ユーザーグループを共有する子組織がありません。

3. **[!UICONTROL ユーザーグループを共有]** を選択します。

4. <a id="review-user-groups"></a> ユーザーグループを確認して、他の組織と共有します。 選択した組織のシステム管理者でもある場合は、「**[!UICONTROL Admin Consoleで開く]**」を選択します Adobe Admin Console内のユーザーグループのメンバーのリストを確認する場合は、「」アイコンを <img src="assets/icon-open-in-admin-console.png" alt="Admin Consoleで開くアイコン" width="14" height="14"> リックします。

   >[!NOTE]
   >
   >競合を防ぐには、ユーザーグループを共有する組織に、同じ名前のグループがまだ存在しないことを確認します。

5. 「**[!UICONTROL 次へ]**」を選択します。

6. ユーザーグループを共有する組織を選択し、「**[!UICONTROL 次へ]**」を選択します。

7. 競合がない場合は、「**[!UICONTROL ユーザーグループを共有]**」を選択します。

   競合がある場合（ターゲット組織に同じ名前のユーザーグループが存在する場合）は、次のいずれかのオプションを選択してから **[!UICONTROL ユーザーグループを共有]** を選択します。
   - **[!UICONTROL 無視（デフォルト）]**：同じ名前のターゲット組織内のグループをスキップします。
   - **[!UICONTROL 追加のみ]**：ユーザーを削除せずに既存のユーザーグループに新しいユーザーを追加して、ユーザーグループを結合します。
   - **[!UICONTROL ミラーグループ]**：ユーザーを追加または削除して、ターゲット組織のグループを共有グループに一致するように調整します。

8. 「**[!UICONTROL 保留中の変更を確認]**」を選択して、更新を確認します。 次に、「変更を送信 **&#x200B;**&#x200B;を選択して [&#x200B; 実行 &#x200B;](https://helpx.adobe.com/enterprise/global-admin-console/set-up-organizations.html#execute-jobs) します。

   グループ投影イベントは、参照用にログに記録されます。 詳細情報 [&#x200B; 監査ログの表示とダウンロード &#x200B;](https://helpx.adobe.com/enterprise/global-admin-console/insights.html)。


ユーザーグループを共有すると、そのグループとそのユーザーがターゲット組織に追加されます。 ただし、*ソースユーザーグループが制御します* 共有ユーザーグループとそのユーザー。 管理者と製品プロファイルの割り当ては、組織間で *同期されません*。

見込みユーザーグループの名前またはソースユーザーグループに関連付けられたユーザーを変更すると、その変更内容がターゲット組織で自動的に更新されます。 共有ユーザーグループは直接管理できませんが、ターゲット組織内の管理者は製品プロファイルを共有グループに割り当てて、グループのユーザーにライセンスアクセスを付与できます。



## 共有グループへのアクセスの取り消し

1. [Global Admin Console](https://global-admin-console.adobe.com/) にログインし、組織を選択して、「**[!UICONTROL ユーザーグループ]**」タブに移動します。

2. 関連するユーザーグループの **[!UICONTROL 共有アクセスを管理]** を選択します。

3. アクセスを取り消す組織を選択します。

4. 「**[!UICONTROL アクセスの失効]**」を選択します。

5. アクセス権限の取り消し時に、ユーザー・グループとユーザーを削除するか、ターゲット組織にコピーを残すかを選択できます。
   - を削除すると、ユーザーグループがターゲット組織から削除されます。 他の共有グループのメンバーでないユーザーは、ターゲット組織から削除され、すべての製品、サービスおよびアセットへのアクセス権が失われます。
   - コピーを作成した後も、ユーザーグループとユーザーはターゲット組織に残り、すべての割り当てはそのまま維持されます。 ただし、ユーザーグループは同期されなくなり、ターゲット組織の管理者が管理できます。

6. 「**[!UICONTROL アクセスの失効]**」を選択します。

7. 「**[!UICONTROL 保留中の変更を確認]**」を選択して、更新を確認します。 次に、「変更を送信 **&#x200B;**&#x200B;を選択して [&#x200B; 実行 &#x200B;](https://helpx.adobe.com/enterprise/global-admin-console/set-up-organizations.html#execute-jobs) します。



## ユーザーグループの編集

1. [Global Admin Console](https://global-admin-console.adobe.com/) にログインし、組織を選択して、「**[!UICONTROL ユーザーグループ]**」タブに移動します。

2. **[!UICONTROL その他のオプション]** を選択します。 関連 <img src="assets/icon-more-options.png" alt="その他のオプション アイコン" width="14" height="14" style="vertical-align:middle"> るユーザーグループのアイコンをクリックし、「**[!UICONTROL ユーザーグループを編集]**」を選択します。

   >[!NOTE]
   >
   >選択した組織が所有していないユーザーグループは編集できません。

   ![&#x200B; 「ユーザーグループ」タブで「ユーザーグループを編集」オプションがハイライト表示されている組織](assets/edit-user-group.png " ユーザーグループを編集 ")

   _ユーザーグループを編集して、ユーザーグループ名、製品プロファイルまたは管理者を更新します。_

3. ユーザーグループ名、製品プロファイルまたは管理者を更新します。 次に、「**[!UICONTROL 保存]**」を選択します。

   >[!NOTE]
   >
   >**[!UICONTROL ユーザーグループを編集]** ウィザードでは、この組織に既に管理者ロールが割り当てられているユーザーにのみ管理者ロールを割り当てることができます。 詳細情報 [&#x200B; 新規管理者の追加 &#x200B;](https://helpx.adobe.com/enterprise/global-admin-console/manage-admins.html)

4. 「**[!UICONTROL 保留中の変更を確認]**」を選択して、更新を確認します。 次に、「変更を送信 **&#x200B;**&#x200B;を選択して [&#x200B; 実行 &#x200B;](https://helpx.adobe.com/enterprise/using/global-admin-set-up-organizations.html#execute-jobs) します。

   >[!NOTE]
   >
   >共有ユーザーグループの名前を変更すると、その変更内容がターゲット組織で自動的に更新されます。



## ユーザーグループの削除

1. [Global Admin Console](https://global-admin-console.adobe.com/) にログインし、組織を選択して、「**[!UICONTROL ユーザーグループ]**」タブに移動します。

2. **[!UICONTROL その他のオプション]** を選択します。 関連 <img src="assets/icon-more-options.png" alt="その他のオプション アイコン" width="14" height="14" style="vertical-align:middle"> るユーザーグループのアイコンをクリックし、「**[!UICONTROL ユーザーグループを削除]**」を選択します。

   >[!NOTE]
   >
   >選択した組織が所有していないユーザーグループを削除することはできません。

3. 表示されるダイアログボックスで「**[!UICONTROL OK]**」を選択します。

   >[!CAUTION]
   >
   >ユーザーグループを削除すると、ユーザーに影響を与える可能性があります。 ユーザーグループを削除した場合に、アクセスや情報が失われないことを確認します。

4. 組織を編集したら、「**[!UICONTROL 保留中の変更をレビュー]**」を選択して確認します。 次に、「変更を送信 **&#x200B;**&#x200B;を選択して [&#x200B; 実行 &#x200B;](https://helpx.adobe.com/enterprise/using/global-admin-set-up-organizations.html#execute-jobs) します。
