---
title: Global Admin Consoleで組織を選択します
description: Global Admin Console内で編集する組織を選択する方法について説明します。
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
source-git-commit: 0bc0dbd8c7040e0be7e7bd45945edb0fb24cb7cc
workflow-type: tm+mt
source-wordcount: '630'
ht-degree: 2%

---


# Global Admin Consoleで組織を選択します

Global Admin Console内で編集する組織を選択する方法について説明します。

>[!NOTE]
>
>[Global Admin Console](https://helpx.adobe.com/jp/enterprise/global-admin-console/adopt-global-administration.html#request-access) にアクセスできるようになったら、まず組織を選択し、その組織の名前、ユーザーグループ、製品プロファイル、管理者、および組織ポリシーを表示および管理できます。 Global Admin Consoleにログインするには、[&#x200B; ここをクリック &#x200B;](https://global-admin-console.adobe.com/) します。

Global Admin Consoleは、Adobe リソースに対する組織の中央管理ハブとして機能します。 グローバル管理者は次の操作を実行できます。

- 組織の下に子組織を作成する
- システム管理者への割り当てによる管理
- 子組織にリソースを配布して、それらの組織内のユーザーに管理および割り当てます

>[!NOTE]
>
> 組織内のユーザーと管理者は、組織外のユーザー、ストレージ、またはその他のリソースを表示できません。

## 組織を選択します

**[!UICONTROL 組織セレクター]** ドロップダウンリストに表示される組織は、明示的にグローバル管理者になっている組織です。つまり、グローバル管理者またはグローバルビューアのロールでその組織の管理者リストに追加された組織です。 その階層内を指すその下のすべての組織の暗黙的なグローバル管理者（またはグローバルビューア）ですが、これらの組織は [!UICONTROL &#x200B; 組織ピッカー &#x200B;] に表示されません。

![&#x200B; 組織ピッカー &#x200B;](/help/adobe-support-tools-guide/assets/org-picker.png)

リストに表示したい場合は、リストに表示したい組織に自分自身をグローバル管理者として追加します。 [!UICONTROL &#x200B; 組織セレクター &#x200B;] で組織を選択した場合、管理者権限は、選択した組織のグローバル管理者であるかどうかに基づきます。 また、ツリーの上位にある親組織のグローバル管理者として表示される場合もあり、より多くの権限を付与できます。 追加の権限を取得するには、その高レベル組織を選択する必要があります。

Global Admin Consoleでは、[!UICONTROL &#x200B; 階層ツリー &#x200B;] から組織を選択すると、特定の組織の情報の編集を開始できます。

**編集の影響：**

- 組織名
- ユーザーグループ
- 製品プロファイル
- 管理者
- 組織のポリシー

**編集の影響なし：**

- ユーザー（グループまたは製品プロファイルの削除を除く）
- ユーザーの追加（管理者を除く）

階層ツリーから組織を選択すると、次の情報が表示されます。

- 組織名
- 領域
- ユーザー数
- 製品のリスト
- 製品プロファイル
- ユーザーグループ
- 管理者
- 要求したドメイン
- 組織のポリシー値

製品、ユーザーグループ、管理者、ドメイン、ポリシー、ポリシーテンプレートを表示または編集するには、適切なタブを選択します。 ほとんどの場合、「[!UICONTROL &#x200B; 検索 &#x200B;]」フィールドを使用して、タブ内の特定の項目を検索できます。

![&#x200B; 組織の編集 &#x200B;](/help/adobe-support-tools-guide/assets/edit-an-organization.png)

組織に追加または組織から削除された管理者には、メール通知が届きます。 組織に対して特定のポリシーを変更すると、その組織の [!DNL Admin Console] に通知が届きます。

## 制約と必要な条件について説明します

- 組織のネストの最大深度は 5 です。 そのため、a/b/c/d/e は許可されますが、a/b/c/d/e/f はエラーです。 例えば、Acme Corp/国際地域/Acme Europe/Acme UK/Acme London は許可されていますが、Acme Corp/国際地域/Acme Europe/Acme UK/Acme London/Acme Mayfair はエラーです。

- パス名の最大長（すべての組織を含む）は 255 文字（「/」を含む）です。 1 つの組織名の最大長は 4 ～ 100 文字です。

- 組織のパス名は一意ですが、単純な名前は兄弟の間でのみ一意です。 組織階層内の他の場所に、同じシンプルな名前の組織が存在する場合があります。

- グローバル管理コンソールを使用して表示できるのは、選択した組織にリンクされているドメインのリストのみです。 選択した組織のシステム管理者の場合は、「**[!UICONTROL Admin Consoleで開く]**」を選択して [&#x200B; ドメインを管理 &#x200B;](https://helpx.adobe.com/jp/enterprise/using/manage-domains-directories.html) します。 「ドメイン」タブに表示される情報については、[&#x200B; スキーマのエクスポートとインポート &#x200B;](https://helpx.adobe.com/jp/enterprise/global-admin-console/export-and-import-data.html#export-and-import-schemas) を参照してください。

- IE 11 は、グローバル管理アクセスではサポートされていません。 別のブラウザーまたは新しいバージョンの IE ブラウザーを使用してください。
