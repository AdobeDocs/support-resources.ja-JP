---
title: 管理者の管理
description: Adobeのお客様がGlobal Admin Consoleで管理者を設定および管理して、ユーザーアクセス、製品ライセンス、組織のリソースを制御する方法。
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: 7e5c601a5edd2558d16bfb7b2d508bcf8f976f51
workflow-type: tm+mt
source-wordcount: '1160'
ht-degree: 2%

---


# 管理者の管理

*enterprise に適用。*

グローバル管理者機能を調べ、各組織の管理者にユーザー、製品ライセンス、グループの管理をデリゲートおよび配布する方法を学びます。

Global Admin Consoleでは、組織を選択し、「**[!UICONTROL 管理者]**」タブに移動して、管理者権限を追加、編集または削除できます。 詳しくは、[&#x200B; グローバル管理の採用 &#x200B;](https://helpx.adobe.com/jp/enterprise/global-admin-console/adopt-global-administration.html) を参照してください。 [Global Admin Console](https://global-admin-console.adobe.com/) に移動してサインインします。


Global Admin Consoleでは、グローバルアドミニストレータというロールが導入されています。 この役割はシステム管理者とは異なり、次の操作を実行できます。

- Global Admin Console階層に追加されたすべての Admin Console で、Adobeへの総投資の全体像を確認できます。
- 複数の Admin Console をまたいで、Adobeのライセンスとリソースの割り当ておよび使用状況を監視します。
- Admin Console または組織を作成します。
- ルートまたは親Admin Consoleから、階層内の下にある子 Admin Console に製品ライセンスを割り当てます。
- システム管理者が独自の Admin Console を引き続き管理しながら、日常業務を維持します。 例えば、グローバル管理者は、製品を子Admin Consoleに割り当てることはできますが、ユーザーに割り当てることはできません。 システム管理者は、Admin Console内の席を受け取り、商品をユーザーに割り当てます。
- オプションで、階層内の任意の Admin Console に組織ポリシーを適用できます。

## 基本的な管理タスク

Global Admin Consoleは、複数の組織や Admin Console で動作するように設計されています。 様々な機能と、それらを実行できる場所（Admin ConsoleまたはGlobal Admin Console）の概要を次の表に示します。

<table>
  <tr>
    <th colspan="2">タスク</th>
    <th>Global Admin Console</th>
    <th>Admin Console</th>
  </tr>

<tr>
    <td colspan="2">子組織を作成、親変更および削除</td>
    <td align="center">○</td>
    <td align="center">×</td>
  </tr>

<tr>
    <td colspan="2">複数の組織での作業</td>
    <td align="center">○</td>
    <td align="center">×</td>
  </tr>

<tr>
    <td rowspan="2" valign="middle">管理者の管理</td>
    <td>1 つ以上の組織の場合</td>
    <td align="center">○</td>
    <td align="center">×</td>
  </tr>

<tr>
    <td>1 つの組織の場合</td>
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
    <td colspan="2">組織間での製品の割り当て</td>
    <td align="center">○</td>
    <td align="center">×</td>
  </tr>

<tr>
    <td colspan="2">ユーザーへの製品の割り当て</td>
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

柔軟な管理階層を作成して、Adobe製品のアクセスと使用を詳細に管理できます。 Adobe Admin Consoleと同様に、Global Admin Consoleでは、システム管理者、製品管理者、製品プロファイル管理者、ユーザーグループ管理者、デプロイメント管理者、サポート管理者およびストレージ管理者を追加できます。 これらの管理者は、管理者となる組織でそれぞれの管理タスクを実行できます。 これらのロールとは別に、グローバル管理には、グローバル管理者とグローバルビューアの 2 つの新しいロールがあります。

グローバル管理者は移行的な役割です。 ユーザーを組織のグローバル管理者にすると、そのユーザーは、直接または間接的に、その組織のすべての子のグローバル管理者になります。 また、新しい組織が組織階層に作成された場合、その組織の親のすべてのグローバル管理者は、新しく作成された組織のグローバル管理者になります。

グローバル管理者ロールの機能は次のとおりです。

- 子組織の作成および削除
- ポリシーの設定と編集
- 管理者ロールの設定と変更
- 子組織での製品の追加と削除
- 子組織のリソース割り当ての設定または変更
- 製品プロファイルとユーザーグループの管理

グローバルビューアの役割の機能は次のとおりです。

- 組織および子組織のユーザーグループ、製品、製品プロファイル、管理者、ポリシーセットおよびリソースのリストを表示します。

## 分散管理

グローバル管理者は、管理者を管理することで、個々の組織の管理者にユーザー、製品ライセンス、グループの管理を委任および配布できます。 グローバル管理者によって組織に追加された管理者には、他の組織の管理を可視化せずに組織を柔軟に管理する権限が付与されます。 したがって、グローバル管理者は、リソースとユーザーの管理を委任し、それらのリソースとユーザーに関するデータを分離することができます。

グローバル管理者は、組織を作成したり、組織に製品やストレージなどのリソースを配布したり、ID 設定を管理したり、組織ポリシーテンプレートを作成および適用したりできます。 グローバル管理者によって組織に追加されたシステム管理者は、ユーザーへの製品の割り当て、ユーザーのオンボーディング、製品プロファイルの作成と管理およびその組織内のその他の管理タスクを実行できます。

## 管理者を追加

1. [Global Admin Console](https://global-admin-console.adobe.com/) で、編集する組織を選択し、「**[!UICONTROL 管理者]**」タブに移動します。

1. **[!UICONTROL 管理者を追加]** を選択します。

   ![&#x200B; グローバル admin console 管理者を追加 &#x200B;](../assets/global-admin-console-add-admin.png)

1. **[!UICONTROL 管理者を追加]** ダイアログボックスで、**[!UICONTROL ユーザーの詳細]** メール、名、姓、アカウントタイプ、国コード）を入力します。

   既存のユーザーを管理者として追加しようとする場合は、既存のユーザーと同じアカウントタイプを選択します。選択しない場合、追加操作が失敗します。

   > [ !N注意]
   > 
   > 組織には、アカウントタイプを追加できる制限を設けることができます。 これらは、[&#x200B; ポリシー &#x200B;](https://helpx.adobe.com/jp/enterprise/global-admin-console/update-policies.html) または組織のその他の設定パラメーターに基づいている場合があります。 組織では、AdobeID ユーザーと BusinessID ユーザーの両方を同時に追加することはできません。 一般に、組織内に両方のタイプのユーザーは存在しないはずですが、ルールが設定される順序によっては、ポリシーまたはルールの適用を事前に行う特定のアカウントタイプのユーザーが存在する場合があります。

1. 「**[!UICONTROL 管理者権限]**」セクションから 1 つ以上の管理者ロールを選択します。

   製品管理者、製品プロファイル管理者、ユーザーグループ管理者などの役割の場合、特定の製品、プロファイル、グループをそれぞれ選択します。

   ![&#x200B; グローバル admin console 管理者を追加 &#x200B;](../assets/global-admin-console-add-admin-detail.png)

1. 「**[!UICONTROL 保存]**」を選択します。

1. 組織の編集後、「**[!UICONTROL 保留中の変更のレビュー]**」を選択し、「**[!UICONTROL 変更の発行]**」を選択して変更を [&#x200B; 実行 &#x200B;](https://helpx.adobe.com/jp/enterprise/global-admin-console/execute-jobs.html) します。

管理者ロールが追加されると、そのロールの変更を知らせるメール通知がユーザーに届きます。

管理者が追加されると、自分の役割を引き受けるように招待するメールメッセージと、Admin Consoleへのリンクが送信されます。 グローバル管理者とその他のロールの両方として追加された場合は、1 つはグローバル管理コンソール、もう 1 つはAdmin Consoleの 2 つの招待状が届きます。

## 管理者を編集

1. 編集する組織を選択し、「**[!UICONTROL 管理者]**」タブに移動します。

1. 関連する管理者の **[!UICONTROL その他のオプション]** （⋮）アイコンを選択してから、「**[!UICONTROL 管理者を編集]**」を選択します。

   ![global admin console 管理者権限の編集 &#x200B;](../assets/global-admin-console-edit-admin-right.png)

1. 管理者の詳細を更新し、「**[!UICONTROL 保存]**」を選択します。

1. 組織の編集が完了したら、「**[!UICONTROL 保留中の変更をレビュー]**」を選択します。

追加または削除された管理者ロールごとに、保留中の変更リストに別のコマンドが表示されます。 レビュー後、「**[!UICONTROL 変更を送信]**」を選択して [&#x200B; 実行 &#x200B;](https://helpx.adobe.com/jp/enterprise/global-admin-console/execute-jobs.html) します。

## 管理者権限を削除

1. 編集する組織を選択し、「**[!UICONTROL 管理者]**」タブに移動します。

1. 関連する管理者の **[!UICONTROL その他のオプション]** （⋮）アイコンを選択し、「**[!UICONTROL 管理者権限を削除]**」を選択します。

   ![global admin console 管理者権限を削除 &#x200B;](../assets/global-admin-console-remove-admin-right.png)

1. 確認ダイアログで **[!UICONTROL OK]** を選択します。

1. 組織の編集が完了したら、「**[!UICONTROL 保留中の変更をレビュー]**」を選択します。 レビュー後、「**[!UICONTROL 変更を送信]**」を選択して [&#x200B; 実行 &#x200B;](https://helpx.adobe.com/jp/enterprise/global-admin-console/execute-jobs.html) します。

管理者を削除すると、その組織の Admin Console へのアクセス権が失われたことを知らせるメール通知がユーザーに届きます。

