---
title: グローバルな経営体制の導入
description: Global Admin Consoleの概要とアクセスをリクエストする方法について説明します。
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
exl-id: 4da055a9-7cdc-4411-8895-016e24eabb2e
source-git-commit: f8d59d1d855ed2c564d9a86286e799ab428d8680
workflow-type: tm+mt
source-wordcount: '810'
ht-degree: 0%

---

# グローバルな経営体制の導入

エンタープライズ版に適用されます。

Global Admin Consoleを利用するメリットと、アクセス方法をご紹介します。 [詳細情報](#request-access-to-the-global-admin-console)

Adobe Admin Consoleでサポートケースを作成して、Global Admin Consoleへのアクセスをリクエストします。 [Global Admin Console](https://global-admin-console.adobe.com)にログインします。

## はじめに

[Global Admin Console](https://global-admin-console.adobe.com)は、多くのAdmin Consoleを持っているか、メインのAdmin Consoleを複数のコンソールに分割したい複雑な組織構造を持つお客様向けです。 たとえば、多国籍企業、教育コンソーシアム、大規模な学区、大規模な政府機関などです。 既存の管理コンソールを組織チャートのような階層構造にネストし、分散型エンタープライズ全体に透明性を提供します。

Global Admin Consoleは、既存のAdmin Consoleの機能を置き換えたり、変更したりすることはありません。 ルート組織を最上位に配置し、そのルート組織の下にネストされたすべてのコンソールを持つ階層として機能します。 Admin Consoleがルートコンソールとして動作する階層構造の購入と作成に焦点を当てた選択基準があります。

Global Admin Consoleの機能と利点について詳しくは、Global Admin Console[に関する](https://community.adobe.com/questions-624/new-white-paper-for-the-adobe-global-admin-console-678929#M35625) ホワイトペーパーを参照し、次の[&#x200B; ビデオ &#x200B;](https://youtu.be/FLBWR78wpok)をご覧ください。

このビデオのコンテンツとボイスオーバーは現在英語でのみ利用できます。

## 主な利点

[!DNL Global Admin Console]の主な利点を次に示します。

- Adobe製品の使用状況とクラウドストレージの管理を、部門、部署、現場のオフィスに任せることで、一元管理の必要性を減らすことができます。
- 各エンティティの組織を作成し、階層構造で管理します。 組織も削除できます。
- 組織をまたいでリソースと製品ライセンスを配布する。
- 組織間の表示を制限し、管理者が割り当てられたスコープ内のユーザーとリソースのみを表示できるようにします。
- 組織のディレクトリ構造に合わせて、Admin Consoleの組織構造をセルフサービス方式で管理できます。
- 特定の組織またはプロジェクトのAdobe リソースを管理する指定された管理者を割り当てることで、管理センターを作成します。
- 組織レベルでポリシーを定義して適用できます。
- 製品プロファイルとユーザーグループを作成、編集、削除します。
- レポート用に組織情報をエクスポートしたり、他のプロセスで使用したりできます。
- 組織の更新と組織階層の変更を読み込みます。
- 今後の有効期限、期限切れ、非アクティブな契約など、子組織のETLA契約ステータスに関する通知を受け取ります。 詳しくは、[契約の有効期限](https://helpx.adobe.com/jp/enterprise/using/contract-expiry.html)のドキュメントを参照してください。

## 実施要件

Adobeでは、次の条件の1つ以上を満たしている場合は、グローバル管理をお勧めします。

- 複数の管理コンソールを管理し、一元的に表示および制御する必要があります。
- 管理コンソールを個別に管理する場合。
- 複数の契約を管理します。
- ID設定を複数の子組織に分散または一元化する必要があります。
- 購入したリソースを企業の別の部分に割り当て、別の管理者を割り当てます。
- 特定のAdobe製品、地域、または組織の管理者が存在し、重複や干渉を防ぐ必要があります。

## Global Admin Consoleへのアクセスをリクエスト

[Global Admin Console](https://adminconsole.adobe.com/support/)へのアクセスをリクエストするには、Adobe担当者にお問い合わせください。

1. [Admin Console](https://adminconsole.adobe.com/support/)で、**[!UICONTROL サポート]** > **[!UICONTROL サポートの概要]**&#x200B;に移動します。

   >[!NOTE]
   >
   > サポート ケースをメイン組織（グローバル管理階層のルート組織）を通じて送信します。

1. 「**[!UICONTROL ケースを作成]**」を選択して、**[!UICONTROL ケースを作成]** ウィンドウを開きます。

1. フォームで、次の詳細を指定します。

   - 問題の優先度：P4 – 軽微
   - 問題の影響：Medium
   - 問題の概要：&lt;お客様の組織名>がGlobal Admin Consoleへのアクセスを要求しています

1. 「**[!UICONTROL お客様が直面している問題の性質を説明する]**」に、お客様の組織がGlobal Admin Consoleへのアクセスを要求していることを明記し、次の詳細を記載します。

   - **名前とコンソール ID** （「@AdobeOrg」の前の数字と文字のシリーズとしてURLに含まれる）をAdmin Consoleの&#x200B;*ルート（上）*組織として指定するか、新しいコンソールをリクエストして目的の名前を指定します。
 – 場合によっては、新しいコンソールが推奨されるオプションです。 Adobeの担当者がサポートします。 後で変更が困難なため、*root*&#x200B;組織を慎重に選択してください。
   - 少なくとも1人の現在のシステム管理者をグローバル管理者ロールに割り当てます。 後で追加の管理者を追加できます。
   - Adobe担当者またはCustomer Success Managerの名前とメールアドレス。

   ![問題の説明](/help/adobe-support-tools-guide/assets/describe.png)

1. 「**[!UICONTROL 次へ]**」を選択し、次の情報を入力します。

   | 入力する詳細 | 説明 |
   | ------------------ | ----------- |
   | **通知するユーザーをリスト** | 最大10個のメールアドレスを追加して、Adobe カスタマーケアからケースアップデートを受け取ります。 |
   | **タイムゾーン** | Adobe カスタマーケアでは、電話が必要な場合にタイムゾーンを使用します。 このフィールドは、システム設定に基づいて自動的に入力されます。 |
   | **営業時間** | Adobeカスタマーケアでは、電話が必要な場合、勤務時間と通常の勤務時間を考慮します。 時間スライダーを使用して、リーチに最適な時間を指定します。 |
   | **電話番号** | トラブルシューティングまたは明確化について、Adobe カスタマーサポート担当者から問い合わせできるように、連絡先番号を指定します。 |

1. **[!UICONTROL 送信]**&#x200B;を選択します。
