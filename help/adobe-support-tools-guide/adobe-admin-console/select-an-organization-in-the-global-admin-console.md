---
title: Global Admin Consoleで組織を選択する
description: Global Admin Console内で編集する組織を選択する方法について説明します。
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: 6a94922a-3343-433d-96e7-0af0f26581a1
source-git-commit: d5f0473b100cda574b4980e6c871a9c275f9f95a
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 2%

---

# Global Admin Consoleで組織を選択する

Global Admin Console内で編集する組織を選択する方法について説明します。

>[!NOTE]
>
>[Global Admin Console](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration#request-access-to-the-global-admin-console)にアクセスできたら、最初に組織を選択して、組織の名前、ユーザーグループ、製品プロファイル、管理者、および組織ポリシーを表示および管理します。 ログインするには、[Global Admin Console](https://global-admin-console.adobe.com/)に移動します。

Global Admin Consoleは、Adobeのリソースを一元管理する組織のハブとして機能します。 グローバル管理者は次のことが可能です。

- 組織の下に子組織を作成する
- システム管理者を割り当てて管理する
- 管理および割り当てのためのリソースをそれらの組織のユーザーに配布

>[!NOTE]
>
> 組織内のユーザーと管理者は、組織外のユーザー、ストレージ、その他のリソースを表示できません。

## 組織の選択

「**[!UICONTROL 組織セレクター]**」ドロップダウンリストにリストされている組織は、明示的にグローバル管理者である組織、つまり、グローバル管理者またはグローバルビューアの役割を持つ組織の管理者リストに追加された組織です。 階層内のそのポイントより下にあるすべての組織のグローバル管理者（またはグローバルビューア）は暗黙的に指定されますが、それらの組織は[!UICONTROL 組織ピッカー]にリストされません。

![組織ピッカー](/help/adobe-support-tools-guide/assets/org-picker.png)

リストを作成する場合は、リストを作成する組織にグローバル管理者として追加します。 [!UICONTROL 組織セレクター]で組織を選択する場合、管理権限は、選択した組織のグローバル管理者であることに基づきます。 また、ツリーの上位にある親組織のグローバル管理者として表示される場合もあり、より多くの権限を付与できます。 追加の権限を取得するには、その上位レベルの組織を選択する必要があります。

Global Admin Consoleでは、[!UICONTROL 階層ツリー]から組織を選択した後、特定の組織の情報の編集を開始できます。

**編集は次の影響を与える可能性があります：**

- 組織名
- ユーザーグループ
- 製品プロファイル
- 管理者
- 組織ポリシー

**編集は：**&#x200B;に影響しません

- ユーザー（グループまたは製品プロファイルの削除を除く）
- ユーザーの追加（管理者を除く）

階層ツリーから組織を選択すると、次の情報が表示されます。

- 組織名
- 領域
- ユーザー数
- 製品リスト
- 製品プロファイル
- ユーザーグループ
- 管理者
- 要求されたドメイン
- 組織のポリシー値

製品、ユーザーグループ、管理者、ドメイン、ポリシー、またはポリシーテンプレートを表示または編集するには、適切なタブを選択します。 ほとんどの場合、[!UICONTROL 検索] フィールドを使用して、タブ内の特定の項目を見つけることができます。

![組織の編集](/help/adobe-support-tools-guide/assets/edit-an-organization.png)

組織に追加または組織から削除された管理者には、メール通知が送信されます。 組織に対する特定のポリシーの変更は、その組織のAdmin Consoleに通知を送信します。

## 制約と必要な条件について説明します

- ネスト組織の最大深度は5です。 したがって、a/b/c/d/eは許可されますが、a/b/c/d/e/fはエラーです。 例えば、Acme Corp/ International Region/ Acme Europe/ Acme UK/ Acme Londonは許可されますが、Acme Corp/ International Region/ Acme Europe/ Acme UK/ Acme London/ Acme Mayfairはエラーです。

- パス名の最大長（すべての組織を含む）は255文字です（「/」を含む）。 1つの組織名の最大長は4 ～ 100文字です。

- 組織のパス名は一意ですが、単純な名前は兄弟の間でのみ一意です。 組織階層の他の場所に、同じ単純な名前を持つ組織が存在する場合があります。

- Global Admin Consoleを使用して、選択した組織にリンクされているドメインのリストのみを表示できます。 選択した組織のシステム管理者である場合は、「**[!UICONTROL Admin Consoleで開く]**」から「[ ドメインを管理する](https://helpx.adobe.com/enterprise/using/manage-domains-directories.html)」を選択します。 「ドメイン」タブに表示される情報については、[ スキーマの書き出しと読み込み](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/export-or-import-organization-structure-and-product-allocations#export-and-import-schemas)を参照してください。

- IE 11は、グローバル管理アクセスではサポートされていません。 別のブラウザーまたは新しいバージョンのIE ブラウザーを使用します。
