---
title: Global Admin Consoleでのユーザーグループの管理
description: Global Admin Consoleでユーザーグループを作成、共有、編集、削除し、組織全体でユーザー管理を効率化する方法について説明します。
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: 1e20362a-0974-4b83-a083-9edaab04c255
source-git-commit: 265c341935b3257e5731a129c42411151645ae89
workflow-type: tm+mt
source-wordcount: '1330'
ht-degree: 0%

---

# Global Admin Consoleでのユーザーグループの管理

Global Admin Consoleでユーザーグループを作成、管理、共有し、同じ権限を持つユーザーをグループ化してユーザー管理を合理化し、時間を節約して、一貫性を確保します。

[Global Admin Console](https://helpx.adobe.com/jp/enterprise/global-admin-console/adopt-global-administration.html)で、組織を選択し、**[!UICONTROL ユーザーグループ]**&#x200B;に移動します。 単一のユーザー管理ソースを使用して、ユーザーとグループを同期し、複数の組織をまたいでグループを共有します。

[Global Admin Consoleにログイン &#x200B;](https://global-admin-console.adobe.com)



## ユーザーグループの作成

[&#x200B; ユーザーグループ &#x200B;](https://helpx.adobe.com/jp/enterprise/using/user-groups.html)を個別に、一括で作成するか、または[確立されたAzure AD](https://helpx.adobe.com/jp/enterprise/using/add-azure-sync.html)からAdobe Admin Consoleのフェデレーションディレクトリに直接同期できます。 Global Admin Consoleでは、関連する製品プロファイルが割り当てられたユーザーグループを定義できます。このユーザーグループに対して、後でAdmin Consoleを使用してユーザーを追加できます。

1. [Global Admin Console](https://global-admin-console.adobe.com/)にログインし、編集する組織を選択してから、**[!UICONTROL ユーザーグループ]** タブに移動します。

2. 「**[!UICONTROL ユーザーグループを追加]**」を選択します。

   「ユーザーのグループ」タブが選択されたGlobal Admin Consoleの「![組織」タブ。](assets/add-user-group.png " ユーザーグループを追加")

   _組織にユーザーグループを追加して、ユーザー管理を効率化します。_

3. 表示される「**[!UICONTROL ユーザーグループを追加]**」ダイアログボックスに、次の情報を入力します。
   - **[!UICONTROL 名前]**: ユーザーグループの名前を指定します。
   - **[!UICONTROL 製品プロファイル]**: ユーザーグループの現在または将来のメンバーに製品アクセス権を付与する場合は、ドロップダウン矢印をクリックしてリストから製品プロファイルを選択するか、製品プロファイル名を入力して表示されるドロップダウンリストから製品プロファイルを選択します。 まだ作成されていない製品プロファイルを追加する場合は、まず「[製品プロファイル &#x200B;](https://helpx.adobe.com/jp/enterprise/using/global-admin-edit-organizations.html#profiles)」タブを使用して追加する必要があります。
   - **[!UICONTROL 管理者]**: ドロップダウン矢印をクリックして、リストから管理者を選択するか、管理者のメールアドレスを入力して、表示されるドロップダウンリストから選択します。 まだ作成されていない新しい管理者を追加する場合は、まず「[管理者](#share-user-groups)」タブを使用してその管理者を作成する必要があります。

   指定した製品プロファイルはユーザーグループに割り当てられ、指定した管理者がグループのユーザーグループ管理者になります。 ユーザーグループ管理者は、関連する組織のAdobe Admin Consoleを使用して、グループを管理できます。

4. 「**[!UICONTROL 保存]**」を選択します。

5. 「**[!UICONTROL 保留中の変更を確認]**」を選択して、更新を確認します。 次に、**[!UICONTROL 変更を送信]**&#x200B;から[実行](https://helpx.adobe.com/jp/enterprise/global-admin-console/set-up-organizations.html#execute-jobs)を選択します。

   >[!NOTE]
   >
   >グローバル管理者は、[Global Admin Consoleを使用して、製品プロファイルとユーザーグループ管理者](#review-user-groups)をユーザーグループに割り当てることができます。 Adobe Admin Consoleを使用すると、システム管理者とユーザーグループ管理者は[&#x200B; ユーザーを追加し、管理者と製品プロファイル &#x200B;](https://helpx.adobe.com/jp/enterprise/using/user-groups.html)をユーザーグループに割り当てることができます。



## ユーザーグループの共有

グループ投影を使用すると、ユーザーグループとその関連ユーザーを1つの管理ソースから複数のAdmin Consoleに同期できます。 グローバル管理者は、ソース組織の階層的な子孫とユーザーグループを共有でき、上向きまたは横向きではなく、下向きに作業できます。

1. [Global Admin Console](https://global-admin-console.adobe.com/)にログインし、組織を選択して、**[!UICONTROL ユーザーグループ]** タブに移動します。

2. 共有するユーザーグループのチェックボックスをオンにします。

   次の場合、グループの共有が無効になる可能性があります。
   - ユーザーグループは別の組織から共有されています。 グループを共有または編集するには、グループを所有する組織を組織階層から選択します。
   - 組織は、グローバルに段階的に展開されている[Adobe ストレージをビジネス &#x200B;](https://helpx.adobe.com/in/enterprise/using/storage-for-business.html)に使用していません。
   - 組織ポリシーが無効になっています。 「**[!UICONTROL ポリシー]**」タブに移動して、**[!UICONTROL 共有ユーザーグループの管理]** ポリシーを有効にします。
   - 組織には、ユーザーグループを共有する子組織がありません。

3. 「**[!UICONTROL ユーザーグループを共有]**」を選択します。

4. <a id="review-user-groups"></a> ユーザーグループを確認して、他の組織と共有します。 選択した組織のシステム管理者でもある場合は、**[!UICONTROL Admin Consoleで開く]**&#x200B;を選択します <img src="assets/icon-open-in-admin-console.png" alt="Admin Consoleで開くアイコン" width="14" height="14"> アイコンをクリックして、Adobe Admin Consoleのユーザーグループメンバーのリストを確認します。

   >[!NOTE]
   >
   >競合を防ぐには、ユーザーグループを共有する組織に、同じ名前のグループが既にないことを確認します。

5. 「**[!UICONTROL 次へ]**」を選択します。

6. ユーザーグループを共有する組織を選択し、**[!UICONTROL 次へ]**&#x200B;を選択します。

7. 競合がない場合は、**[!UICONTROL ユーザーグループを共有]**&#x200B;を選択します。

   競合がある場合（ターゲット組織に同じ名前のユーザーグループが存在する場合）、次のいずれかのオプションを選択し、**[!UICONTROL ユーザーグループを共有]**&#x200B;を選択します。
   - **[!UICONTROL 無視（デフォルト）]**：同じ名前のターゲット組織内のグループをスキップします。
   - **[!UICONTROL 追加のみ]**: ユーザーを削除せずに既存のユーザーグループに新しいユーザーを追加して、ユーザーグループを統合します。
   - **[!UICONTROL ミラーグループ]**: ユーザーを追加または削除して、共有グループに合わせてターゲット組織のグループを調整します。

8. 「**[!UICONTROL 保留中の変更を確認]**」を選択して、更新を確認します。 次に、**[!UICONTROL 変更を送信]**&#x200B;から[実行](https://helpx.adobe.com/jp/enterprise/global-admin-console/set-up-organizations.html#execute-jobs)を選択します。

   グループ投影イベントは、参照用にログに記録されます。 [監査ログの表示とダウンロード &#x200B;](https://helpx.adobe.com/jp/enterprise/global-admin-console/insights.html)について説明します。


ユーザーグループを共有すると、グループとそのユーザーがターゲット組織に追加されます。 ただし、*ソースユーザーグループは*&#x200B;共有ユーザーグループとそのユーザーを制御します。 管理者と製品プロファイルの割り当ては、組織間で&#x200B;*not*&#x200B;同期されています。

予測されるユーザーグループの名前またはソースユーザーグループ内の関連ユーザーの変更は、ターゲット組織で自動的に更新されます。 共有ユーザーグループを直接管理することはできませんが、ターゲット組織内の管理者は製品プロファイルを共有グループに割り当てることができ、グループのユーザーにライセンスへのアクセス権を付与できます。



## 共有グループへのアクセス権の取り消し

1. [Global Admin Console](https://global-admin-console.adobe.com/)にログインし、組織を選択して、**[!UICONTROL ユーザーグループ]** タブに移動します。

2. 関連するユーザーグループの&#x200B;**[!UICONTROL 共有アクセスの管理]**&#x200B;を選択します。

3. アクセス権を取り消す組織を選択します。

4. 「**[!UICONTROL アクセスを取り消す]**」を選択します。

5. アクセス権を取り消す際に、ユーザーグループとユーザーを削除するか、コピーをターゲット組織に残すかを選択できます。
   - 削除時に、ユーザーグループがターゲット組織から削除されます。 他の共有グループのメンバーではないユーザーは、ターゲット組織から削除され、すべての製品、サービス、アセットにアクセスできなくなります。
   - コピーを残すと、ユーザーグループとユーザーはすべての割り当てを維持しながら、ターゲット組織に残ります。 ただし、ユーザーグループは同期されなくなり、ターゲット組織の管理者が管理できるようになります。

6. 「**[!UICONTROL アクセスを取り消す]**」を選択します。

7. 「**[!UICONTROL 保留中の変更を確認]**」を選択して、更新を確認します。 次に、**[!UICONTROL 変更を送信]**&#x200B;から[実行](https://helpx.adobe.com/jp/enterprise/global-admin-console/set-up-organizations.html#execute-jobs)を選択します。



## ユーザーグループの編集

1. [Global Admin Console](https://global-admin-console.adobe.com/)にログインし、組織を選択して、**[!UICONTROL ユーザーグループ]** タブに移動します。

2. **[!UICONTROL 詳細オプション]**&#x200B;を選択 関連するユーザーグループの<img src="assets/icon-more-options.png" alt="その他のオプション アイコン" width="14" height="14" style="vertical-align:middle"> アイコンを選択し、**[!UICONTROL ユーザーグループを編集]**&#x200B;を選択します。

   >[!NOTE]
   >
   >選択した組織が所有していないユーザーグループを編集することはできません。

   ![&#x200B; ユーザーグループを編集オプションが「ユーザーグループ」タブでハイライト表示された状態で選択された組織。](assets/edit-user-group.png " ユーザーグループの編集")

   _ユーザーグループを編集して、ユーザーグループ名、製品プロファイル、または管理者を更新します。_

3. ユーザーグループ名、製品プロファイル、または管理者を更新します。 次に、**[!UICONTROL 保存]**&#x200B;を選択します。

   >[!NOTE]
   >
   >**[!UICONTROL ユーザーグループを編集]** ウィザードでは、この組織で既に管理者ロールが割り当てられているユーザーにのみ管理者ロールを割り当てることができます。 [新しい管理者を追加する方法](https://experienceleague.adobe.com/ja/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators)について説明します。

4. 「**[!UICONTROL 保留中の変更を確認]**」を選択して、更新を確認します。 次に、**[!UICONTROL 変更を送信]**&#x200B;から[実行](https://helpx.adobe.com/jp/enterprise/using/global-admin-set-up-organizations.html#execute-jobs)を選択します。

   >[!NOTE]
   >
   >共有ユーザーグループの名前を変更すると、変更はターゲット組織で自動的に更新されます。



## ユーザーグループの削除

1. [Global Admin Console](https://global-admin-console.adobe.com/)にログインし、組織を選択して、**[!UICONTROL ユーザーグループ]** タブに移動します。

2. **[!UICONTROL 詳細オプション]**&#x200B;を選択 関連するユーザーグループの<img src="assets/icon-more-options.png" alt="その他のオプション アイコン" width="14" height="14" style="vertical-align:middle"> アイコンを選択し、**[!UICONTROL ユーザーグループの削除]**&#x200B;を選択します。

   >[!NOTE]
   >
   >選択した組織が所有していないユーザーグループを削除することはできません。

3. 表示されるダイアログボックスで「**[!UICONTROL Ok]**」を選択します。

   >[!CAUTION]
   >
   >ユーザーグループを削除すると、ユーザーに影響を与える可能性があります。 ユーザーグループが削除されたときに失われるアクセスまたは情報がないことを確認します。

4. 組織を編集したら、**[!UICONTROL 保留中の変更をレビュー]**&#x200B;を選択してレビューします。 次に、**[!UICONTROL 変更を送信]**&#x200B;から[実行](https://helpx.adobe.com/jp/enterprise/using/global-admin-set-up-organizations.html#execute-jobs)を選択します。
