---
title: 管理者の管理
description: Adobeのお客様がGlobal Admin Consoleで管理者を設定および管理し、ユーザーアクセス、製品ライセンス、および組織リソースを制御する方法。
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: 41c00379-98ee-4922-8eba-cc373c23a019
source-git-commit: 8860538190e99e171abc6273adda321443e41fed
workflow-type: tm+mt
source-wordcount: '1159'
ht-degree: 2%

---

# 管理者の管理

*エンタープライズに適用されます。*

グローバル管理者機能を確認し、ユーザー、製品ライセンス、グループの管理を個々の組織の管理者に委任して配布する方法を説明します。

Global Admin Consoleで、組織を選択し、「**[!UICONTROL 管理者]**」タブに移動して、管理者権限を追加、編集、または削除できます。 詳しくは、[&#x200B; グローバル管理の導入](https://helpx.adobe.com/jp/enterprise/global-admin-console/adopt-global-administration.html)を参照してください。 [Global Admin Console](https://global-admin-console.adobe.com/)に移動してログインします。


Global Admin Consoleは、グローバル管理者という役割を導入します。 この役割はシステム管理者とは異なり、次の操作を実行できます。

- Global Admin Console階層に追加されたすべての管理コンソールでのAdobeの総投資額の全体像を表示します。
- 複数の管理コンソールをまたいで、Adobe ライセンスとリソースの割り当てと使用状況をモニタリングします。
- Admin Consoleまたは組織を作成します。
- ルートまたは親Admin Consoleの製品ライセンスを、階層内の下にある子管理コンソールに割り当てます。
- システム管理者が独自のAdmin Consoleを引き続き管理しながら、日常業務を維持します。 例えば、グローバル管理者は商品を子Admin Consoleに割り当てることができますが、ユーザーに割り当てることはできません。 システム管理者は、Admin Console内でシートを受け取り、製品をユーザーに割り当てます。
- 必要に応じて、階層内の任意の管理コンソールに組織ポリシーを適用します。

## 基本的な管理作業

Global Admin Consoleは、複数の組織とAdmin Consoleで動作するように設計されています。 Admin ConsoleとGlobal Admin Consoleの各機能と、それらの機能の完了場所を次の表に示します。

<table>
  <tr>
    <th colspan="2">タスク</th>
    <th>Global Admin Console</th>
    <th>Admin Console</th>
  </tr>

<tr>
    <td colspan="2">子組織の作成、再親、および削除</td>
    <td align="center">○</td>
    <td align="center">×</td>
  </tr>

<tr>
    <td colspan="2">複数の組織との連携</td>
    <td align="center">○</td>
    <td align="center">×</td>
  </tr>

<tr>
    <td rowspan="2" valign="middle">管理者の管理</td>
    <td>1つ以上の組織の場合</td>
    <td align="center">○</td>
    <td align="center">×</td>
  </tr>

<tr>
    <td>1つの組織に対して</td>
    <td align="center">○</td>
    <td align="center">○</td>
  </tr>

<tr>
    <td colspan="2">製品プロファイルとユーザーグループの管理</td>
    <td align="center">○</td>
    <td align="center">○</td>
  </tr>

<tr>
    <td colspan="2">ポリシーの定義と管理</td>
    <td align="center">○</td>
    <td align="center">×</td>
  </tr>

<tr>
    <td colspan="2">組織をまたいだプロダクトの割り当て</td>
    <td align="center">○</td>
    <td align="center">×</td>
  </tr>

<tr>
    <td colspan="2">製品のユーザーへの割り当て</td>
    <td align="center">×</td>
    <td align="center">○</td>
  </tr>

<tr>
    <td colspan="2">ユーザーの管理</td>
    <td align="center">×</td>
    <td align="center">○</td>
  </tr>

<tr>
    <td colspan="2">パッケージの管理</td>
    <td align="center">×</td>
    <td align="center">○</td>
  </tr>

<tr>
    <td colspan="2">ドメインとディレクトリの設定</td>
    <td align="center">×</td>
    <td align="center">○</td>
  </tr>

<tr>
    <td colspan="2">エンタープライズストレージと暗号化の管理</td>
    <td align="center">×</td>
    <td align="center">○</td>
  </tr>
</table>

## 管理者の管理

Adobe製品へのアクセスと使用を詳細に管理できる、柔軟な管理階層を構築できます。 Adobe Admin Consoleと同様に、Global Admin Consoleでは、システム管理者、製品管理者、製品プロファイル管理者、ユーザーグループ管理者、デプロイメント管理者、サポート管理者、ストレージ管理者を追加できます。 これらの管理者は、管理者である組織でそれぞれの管理タスクを実行できます。 これらの役割とは別に、グローバル管理には、グローバル管理者とグローバルビューアの2つの新しい役割があります。

グローバル管理者は一時的な役割です。 ユーザーを組織のグローバル管理者にすると、そのユーザーはその組織のすべての子のグローバル管理者になります（直接または間接的）。 また、組織階層に新しい組織が作成された場合、その組織の親のすべてのグローバル管理者は、新しく作成された組織のグローバル管理者になります。

グローバル管理者ロールの機能を次に示します。

- 子組織の作成と削除
- ポリシーの設定と編集
- 管理者ロールの設定と変更
- 子組織での製品の追加と削除
- 子組織のリソース割り当ての設定または変更
- 製品プロファイルとユーザーグループの管理

Global Viewer ロールの機能を次に示します。

- 組織内および子組織内のユーザーグループ、製品、製品プロファイル、管理者、ポリシーセット、リソースのリストを表示します。

## 分散管理

管理者を管理することで、グローバル管理者は、ユーザー、製品ライセンス、グループの管理を個々の組織の管理者に委任して配布できます。 グローバル管理者が組織に追加した管理者には、他の組織の管理を可視化することなく、組織を柔軟に管理できます。 そのため、グローバル管理者は、リソースとユーザーに関するデータを隔離したまま、リソースとユーザーの管理を委任できます。

グローバル管理者は、組織を作成し、製品やストレージなどのリソースをそれらの組織に配布し、ID設定を管理し、組織ポリシーテンプレートを作成して適用できます。 グローバル管理者が組織に追加したシステム管理者は、ユーザーへの製品の割り当て、ユーザーのオンボーディング、製品プロファイルの作成と管理、その組織内での他の管理タスクを実行できます。

## 管理者を追加

1. [Global Admin Console](https://global-admin-console.adobe.com/)で、編集する組織を選択し、**[!UICONTROL 管理者]** タブに移動します。

1. 「**[!UICONTROL 管理者を追加]**」を選択します。

   ![Global Admin Console add admin](../assets/global-admin-console-add-admin.png)

1. **[!UICONTROL 管理者を追加]** ダイアログボックスで、**[!UICONTROL ユーザーの詳細]**：電子メール、名、姓、アカウントタイプ、および国コードを入力します。

   既存のユーザーを管理者として追加する場合は、既存のユーザーと同じアカウントタイプを選択します。そうしないと、追加操作が失敗します。

   >[!NOTE]
   >
   > 組織は、どのアカウントタイプを追加できるかについて制限を設定できます。 これらは、[policies](https://helpx.adobe.com/jp/enterprise/global-admin-console/update-policies.html)または組織の他の設定パラメーターに基づいている場合があります。 組織では、AdobeID ユーザーとBusinessID ユーザーの両方を同時に追加することはできません。 一般に、組織内に両方のタイプのユーザーはいませんが、ルールが設定される順序に応じて、ポリシーまたはルールの適用前に特定のアカウントタイプのユーザーが存在する場合があります。

1. 「**[!UICONTROL 管理者権限]**」セクションから1つ以上の管理者ロールを選択します。

   製品管理者、製品プロファイル管理者、ユーザーグループ管理者などの役割については、それぞれ特定の製品、プロファイル、グループを選択します。

   ![Global Admin Console add admin](../assets/global-admin-console-add-admin-detail.png)

1. 「**[!UICONTROL 保存]**」を選択します。

1. 組織を編集した後、「**[!UICONTROL 保留中の変更を確認]**」を選択し、「**[!UICONTROL 変更を送信]**」から「[実行](https://helpx.adobe.com/jp/enterprise/global-admin-console/execute-jobs.html)」を選択します。

管理者の役割が追加されると、ユーザーは役割の変更を通知するメール通知を受け取ります。

管理者が追加されると、その管理者に役割を引き受けるよう促す電子メールメッセージが届き、Admin Consoleへのリンクが表示されます。 グローバル管理者と他のロールの両方として追加された場合、1つはGlobal Admin Consoleに、もう1つはAdmin Consoleに招待されます。

## 管理者の編集

1. 編集する組織を選択し、**[!UICONTROL 管理者]** タブに移動します。

1. 関連する管理者の&#x200B;**[!UICONTROL 詳細オプション]** （⋮） アイコンを選択し、**[!UICONTROL 管理者を編集]**&#x200B;を選択します。

   ![Global Admin Console管理者権限の編集](../assets/global-admin-console-edit-admin-right.png)

1. 管理者の詳細を更新し、**[!UICONTROL 保存]**&#x200B;を選択します。

1. 組織の編集が完了したら、「**[!UICONTROL 保留中の変更を確認]**」を選択します。

追加または削除された管理者の役割ごとに、保留中の変更リストに個別のコマンドが表示されます。 レビュー後、**[!UICONTROL 変更を送信]**&#x200B;から[実行](https://helpx.adobe.com/jp/enterprise/global-admin-console/execute-jobs.html)を選択します。

## 管理者権限の削除

1. 編集する組織を選択し、**[!UICONTROL 管理者]** タブに移動します。

1. 関連する管理者の&#x200B;**[!UICONTROL 詳細オプション]** （⋮） アイコンを選択し、**[!UICONTROL 管理者権限の削除]**&#x200B;を選択します。

   ![Global Admin Consoleで管理者権限を削除](../assets/global-admin-console-remove-admin-right.png)

1. 確認ダイアログで「**[!UICONTROL OK]**」を選択します。

1. 組織の編集が完了したら、「**[!UICONTROL 保留中の変更を確認]**」を選択します。 レビュー後、**[!UICONTROL 変更を送信]**&#x200B;から[実行](https://helpx.adobe.com/jp/enterprise/global-admin-console/execute-jobs.html)を選択します。

管理者を削除すると、その組織の管理コンソールへのアクセス権が失われたことを通知するメール通知がユーザーに届きます。
