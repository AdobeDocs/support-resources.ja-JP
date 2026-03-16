---
title: グローバルな管理を採用する
description: Global Admin Consoleとは何か、およびアクセスをリクエストする方法を説明します。
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
source-git-commit: ae2a50b6ebab1ba46fdcad0e8aa2921b4728ed42
workflow-type: tm+mt
source-wordcount: '805'
ht-degree: 0%

---

# グローバルな管理を採用する

エンタープライズに適用します。

Global Admin Consoleを使用するメリットとアクセス方法について説明します。 [詳細情報](#request-access-to-the-global-admin-console)

Adobe Admin Consoleでサポートケースを作成して、Global Admin Consoleへのアクセスをリクエストします。
[Global Admin Console](https://adminconsole.adobe.com/support) にサインインします。

## はじめに

[0}Global Admin Console} は、多くの Admin Console を持つ、または主要なAdmin Consoleを複数のコンソールに分割する必要がある、複雑な組織構造を持つお客様向けです。 ](https://adminconsole.adobe.com/support)例えば、多国籍企業、教育機関のコンソーシアム、大規模な学区、大規模な政府機関などです。 分散した企業全体に透明性を提供するために、既存の Admin Console を組織図のような階層構造にネストします。

Global Admin Consoleは、既存の Admin Console の機能に取って代わるものでも、変更するものでもありません。 最上位にルート組織があり、そのルート組織の下にネストされたすべてのコンソールを持つ階層として機能します。 Admin Consoleがルートコンソールとして機能する階層構造の購入と作成に重点を置いた選択基準があります。

Global Admin Consoleの機能とメリットについて詳しくは、[Global Admin Consoleに関するホワイトペーパー ](https://community.adobe.com/questions-624/new-white-paper-for-the-adobe-global-admin-console-678929#M35625) を参照してください。

[!VIDEO](https://youtu.be/FLBWR78wpok)

このビデオのコンテンツとボイスオーバーは、現在、英語でのみ利用できます。

## 主なメリット

[!DNL Global Admin Console] の主なメリットを次に示します。

- Adobe製品の使用状況とクラウドストレージの管理を部門、部門、フィールドオフィスに委任することで、一元管理の必要性を軽減します。
- エンティティごとに組織を作成し、階層構造で管理します。 組織は削除することもできます。
- 複数の組織にリソースと製品ライセンスを配布します。
- 組織間の表示を制限して、管理者が割り当てられた範囲内のユーザーとリソースのみを表示できるようにします。
- 組織のディレクトリ構造に合わせて、セルフサービス方式でAdmin Consoleの組織構造を管理します。
- 特定の組織やプロジェクトのAdobe リソースを管理する指定管理者を割り当てることで、管理センターを構築します。
- 組織レベルでポリシーを定義し、適用します。
- 製品プロファイルおよびユーザーグループを作成、編集および削除します。
- レポート用または他のプロセスで使用するための組織情報をエクスポートします。
- 組織の更新および組織階層の変更をインポートします。
- 今後の契約期限切れ、期限切れ、非アクティブな契約など、子組織のETLAの契約ステータスに関する通知を受信します。 詳しくは、[ 契約の有効期限 ](https://helpx.adobe.com/enterprise/using/contract-expiry.html) ドキュメントを参照してください。

## 実施要件条件

Adobeでは、組織が次の 1 つ以上の条件を満たしている場合、グローバル管理をお勧めします。

- 複数の Admin Console を管理し、一元的な表示と制御を行う必要があります。
- Admin Console を分離し、個別に管理する必要がある場合。
- 複数の契約を管理します。
- 複数の子組織にわたって ID 設定を配布または一元化する必要があります。
- 購入したリソースを企業の様々な部分に割り当て、別々の管理者を割り当てる場合。
- 特定のAdobe製品、リージョンまたは組織の管理者がいて、重複や干渉を防ぎたい場合。

## Global Admin Consoleへのアクセスをリクエスト

[Global Admin Console](https://adminconsole.adobe.com/support/) へのアクセスをリクエストするには、Adobe担当者に問い合わせた後、次の手順に従います。

1. [Admin Console](https://adminconsole.adobe.com/support/) で、**[!UICONTROL サポート]**/**[!UICONTROL サポートの概要]** に移動します。

   >[!NOTE]
   >
   > メイン組織（グローバル管理階層のルート組織として機能）を通じてサポートケースを送信します。

1. 「**[!UICONTROL ケースを作成]**」を選択して、「**[!UICONTROL ケースを作成]**」ウィンドウを開きます。

1. フォームで、次の詳細を指定します。

   - 問題の優先度：P4 - マイナー
   - この問題の影響：Medium
   - 問題の概要：&lt; 所属する組織の名前 > がGlobal Admin Consoleへのアクセスを要求しています

1. **[!UICONTROL 発生している問題の性質を説明]** で、組織がGlobal Admin Consoleへのアクセスをリクエストしていることを示し、次の詳細を含めます。

   - Admin Consoleの **名前とコンソール ID** （URL では「@AdobeOrg」の前にある一連の数字と文字で検出されます）を *ルート（トップ）* 組織として指定するか、新しいコンソールをリクエストして目的の名前を指定します。
 – 場合によっては、新しいコンソールが推奨されるオプションです。 Adobe担当者がガイドします。 *root* 組織は後で変更するのが難しいので、慎重に選択してください。
   - 現在の 1 人以上のシステム管理者をグローバル管理者の役割に割り当てます。 後で管理者を追加できます。
   - Adobe担当者またはカスタマーサクセスマネージャーの名前とメールアドレス。

   ![ 問題の説明 ](/help/adobe-support-tools-guide/assets/describe.png)

1. 「**[!UICONTROL 次へ]**」を選択し、次の情報を入力します。

   | 入力する詳細 | 説明 |
   | ------------------ | ----------- |
   | **通知するユーザーのリスト** | 最大 10 個のメールアドレスを追加して、Adobe カスタマーケアからケースのアップデートを受け取ります。 |
   | **タイムゾーン** | Adobe カスタマーケアは、電話が必要な場合にタイムゾーンを使用します。 このフィールドは、システム設定に基づいて自動的に入力されます。 |
   | **労働時間** | Adobe カスタマーケアは、お客様からの連絡が必要な場合に、営業時間と通常の営業時間を考慮します。 タイム スライダを使用して、到達するのに最適な時間を指定します。 |
   | **電話番号** | トラブルシューティングや明確な説明のためにAdobe カスタマーケア担当者から連絡を差し上げることができるように、連絡先の電話番号を指定します。 |

1. **[!UICONTROL 送信]** を選択します。
