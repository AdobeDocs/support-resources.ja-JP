---
title: クラウド基盤の一時的なAdobe Commerceのアップグレードをリクエストする方法
description: トラフィックが多いオンラインイベントを計画している場合、または突然サイトのトラフィックが多いイベントが発生した場合は、[ サポートチケット ] （https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html?lang=en#submit-ticket）を提出して、Adobe Commerce on cloud infrastructure ストアの一時的なクラウド容量を追加でリクエストできます。
solution: Commerce
exl-id: 203882c0-929a-4bb3-afff-738bc518b46b
TQID: https://experienceleague.adobe.com/9--JwGLuX01kXR569r1OjVrkiTd2BQa-j-gOTs9oKGY
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
subfeature_v2:
  - id: f8ddfd3b-6194-46e8-a176-0e918039be56
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: d1c3158bb425e7966ccc5e5d79457c6b33e00063
workflow-type: tm+mt
source-wordcount: 1136
ht-degree: 1%

---

# クラウド基盤の一時的なAdobe Commerceのアップグレードをリクエストする方法

トラフィックが多いオンラインイベントを計画している場合、または突然サイトのトラフィックが多いイベントが発生した場合は、[&#x200B; サポートチケット &#x200B;](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html?lang=en#submit-ticket)を提出して、Adobe Commerce on cloud infrastructure ストアの一時的なクラウド容量を追加できます。

>[!NOTE]
>
>緊急でないアップサイズリクエストには、48営業時間前の通知が必要です。 プロモーションキャンペーンのアップサイズは、サイトが完全に機能的でない場合、または予測よりもはるかに高いトラフィックを受け取り、パフォーマンスが大幅に低下した場合を除いて、緊急事態とは見なされません。

## 影響を受ける製品とバージョン

* クラウドインフラストラクチャ上のAdobe Commerce、すべての[&#x200B; サポートされているバージョン &#x200B;](https://www.adobe.com/content/dam/cc/en/legal/terms/enterprise/pdfs/Adobe-Commerce-Software-Lifecycle-Policy.pdf)。

## トラフィックイベントを特定する方法

New Relicアラートでは、ベースラインアラート条件を使用して、データのビヘイビアーに合わせたしきい値を定義できます。

ベースラインアラートは、次のようなアラート条件を作成するのに便利です。

* データが異常に動作している場合にのみ通知します。
* 日次または週次のトレンドなど、変化するデータやトレンドに動的に対応。

さらに、ベースラインアラートは、まだ既知の動作がない場合に、新しいアプリケーションで適切に機能します。

このリンクをクリックして、適用されたインテリジェンスによるNew Relic [異常値検出](https://docs.newrelic.com/docs/alerts-applied-intelligence/applied-intelligence/anomaly-detection/anomaly-detection-applied-intelligence/)の詳細をご確認ください。

トラフィックの多いイベントを示唆するアラート通知を受け取った場合は、追加の容量をリクエストする[&#x200B; サポートチケットの送信](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html?lang=en#submit-ticket)を検討する必要がある場合があります。 以下の手順に従います。

## サイトのパフォーマンスを監視する方法

Adobeでは、以下の主要なパフォーマンス指標を追跡するための、Adobe Commerce on cloud infrastructure Pro プランアーキテクチャとAdobe Commerce on cloud infrastructure Starter プランアーキテクチャの実稼動環境に対する一連のNew Relic アラートポリシーを提供しています。

* [Apdex スコア](https://docs.newrelic.com/docs/apm/new-relic-apm/apdex/apdex-measure-user-satisfaction)
* エラー率
* ディスク領域（Pro アーキテクチャの実稼動環境でのみ使用可能）

業界のベストプラクティスにもとづいて、これらのポリシーは、パフォーマンスに影響を与える警告と重大な条件のしきい値を設定します。 サイトでインフラストラクチャやアプリケーションの問題が発生し、アラートしきい値がトリガーされた場合、New Relicはアラート通知を送信します。これにより、問題に積極的に対処できます。 これらのポリシーを使用するには、通知チャネルを設定してアラートメッセージを受信する必要があります。

パフォーマンス ベースのアラートを[設定](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/monitor/new-relic/new-relic-service#monitor-performance-with-managed-alerts)する方法については、このリンクを参照してください。

## 一時的なアップサイズをリクエストする手順

クラウドの一時的な追加容量をリクエストするには、次の情報を記載した[&#x200B; サポートチケット &#x200B;](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html?lang=en#submit-ticket)をAdobe Commerce サポートセンターに送信します。

>[!NOTE]
>
>*ホリデーサージリクエスト*&#x200B;の選択肢は、10月から12月の間のオプションのみです。

1. サポートが必要な[!DNL Adobe Commerce]製品を選択してください：
   * [!DNL Commerce Cloud]
   * [!DNL Commerce on Managed Service]

1. 以下のフィールドに入力します。
   * **[!UICONTROL ケースタイトル]**
   * **[!UICONTROL ケースの説明]** *（問題とコンテキストを明確に説明してください）*

1. 「**[!UICONTROL 問題理由]**」ドロップダウンメニューから「*インフラストラクチャ変更リクエスト*」を選択します。

1. ドロップダウンメニューから「**[!UICONTROL 環境]**」を選択します。

1. ドロップダウンメニューから適切な&#x200B;**[!UICONTROL 製品バージョン]**&#x200B;を選択します。

1. 「**[!UICONTROL 今日どのインフラ変更を行うか]**」ドロップダウンメニューから「*クラウドプロジェクトのサイズ変更（vCPU）*」を選択します。

1. **[!UICONTROL &#x200B; アーキテクチャ]**&#x200B;を選択します。
   * *デフォルトのアーキテクチャ：* 「**サイズを選択**」ドロップダウンメニューから「*次に使用可能なサイズ*」を選択します。
   * *拡張アーキテクチャ：*&#x200B;選択すると、画面が変更され、次の2つの追加フィールドが表示されます。
      * Web ノードの&#x200B;*サイズ*
      * *サービスノードのサイズ* *（各ノードに必要なサイズを入力）*

1. **[!UICONTROL 開始日]**&#x200B;をUTC形式（日付と時刻）で入力します。

1. **[!UICONTROL 日付]**&#x200B;をUTC形式（日時）で入力します。

1. **[!UICONTROL プロジェクト URL]** *を指定します（https://accounts.magento.cloud/の下にあり、通常は`https://[REGION].magento.cloud/projects/PROJECT_ID`形式）*&#x200B;です

1. **[!UICONTROL プロジェクト ID]**&#x200B;を入力します。

1. **[!UICONTROL 影響を受けるURL]** *を指定してください（`http://`または`https://`で始める必要があります）*

1. **[!UICONTROL 優先度]**&#x200B;を選択します。

1. 「**[!UICONTROL ビジネスへの影響]**」を選択します。

1. **[!UICONTROL タイムゾーン]** *を確認（例：`(UTC-5:00) Indiana (East)`）*

1. **[!UICONTROL 電話番号]** *を入力してください（例：`+12015550123`）*

1. 「**[!UICONTROL 送信]**」をクリックして、サポートケースを確定します。

>[!NOTE]
>
>アップサイズがスケジュールされると、自動システムがクラウドインスタンスのサイズを調整します。 手続きが完了した時点でチケット通知が届かない場合があります。 Observation for Adobe Commerce ツールを使用して、AWSまたはAzure インスタンスの種類を表示し、[変更を確認できます](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/how-to/check-vcpu-using-observation-for-adobe-commerce)。

## アップサイズの履歴を表示

**CSM （カスタマーサクセスマネージャー）**&#x200B;から情報をリクエストすることで、要求されたサイズ変更の履歴を表示できます。
サイズ変更リクエストごとに、次の情報を利用できます。

* **サイズ開始日**: アップサイズリクエストの日付。
* **サイズ終了日**: クラスターが前のサイズに戻された日付。
* **vCPU サイズ**: アップサイズ後のクラスターのサイズ。
* **日間の使用状況**：クラスターがアップサイズを維持した日数。
* **期間vCPU**: vCPU サイズを、使用された日数で変更しました。 （例えば、vCPU サイズ 192 x 25日は4,800になります）。


## 関連トピックス

* サイトのパフォーマンスを測定、改善するためのインサイト、方法、例については、サポートナレッジベースの次の詳細な記事を参照してください。
   * [Adobe Commerce クラウド版のCPU割り当て計算](https://experienceleague.adobe.com/ja/docs/commerce-knowledge-base/kb/how-to/magento-commerce-cloud-cpu-allocation-calculation)
   * [Adobe Commerce on cloudでホストのインスタンスのアップサイズが必要かどうかを確認します](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/how-to/magento-commerce-cloud-check-if-upsize-for-hosts-instances-is-needed)
   * [Adobe Commerce on cloud用のホストのCPU設定を確認します](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/how-to/magento-commerce-cloud-check-hosts-cpu-configuration)
* 障害を特定する方法については、サポートナレッジベースの「[&#x200B; クラウド上のAdobe Commerceの障害を特定して測定する](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/how-to/how-to-identify-outages)」を参照してください。
* 容量の増加を利用する必要性を回避するためのサイトパフォーマンスの向上について詳しくは、以下の開発者向けドキュメントの記事を参照してください。
   * [画像のサイズ](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/products/digital-assets/product-image-config#product-image-resizing)
   * [フルページキャッシュ](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/tools/cache-management#full-page-caching)
   * [ECE-Tools](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/dev-tools/ece-tools/package-overview)
