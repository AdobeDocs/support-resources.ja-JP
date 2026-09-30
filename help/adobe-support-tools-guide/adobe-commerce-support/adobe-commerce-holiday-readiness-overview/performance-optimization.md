---
title: パフォーマンスの最適化
description: パフォーマンスの最適化に関する推奨事項：Adobe Commerceを利用するマーチャントは、ホリデーシーズンなどの交通量の多いイベントに備えて環境を整えることができます。
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: cdfd3bc1-dc23-5cf0-b965-d3c0c55cde67
    internal-label: Best Practices
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
    internal-label: Architecture
subfeature_v2:
  - id: f8ddfd3b-6194-46e8-a176-0e918039be56
    internal-label: Cloud architecture
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 8b0e99848d1e5798cce52e21f9052b2b57c73b38
workflow-type: tm+mt
source-wordcount: '1698'
ht-degree: 0%
---

# パフォーマンスの最適化

このセクションでは、ホリデーシーズンなどのトラフィックの多いイベント用に、Commerce on cloud インフラストラクチャとオンプレミスの両方のAdobe Commerce環境を準備するための技術的な推奨事項について説明します。

>[!NOTE]
>
>**（クラウドのみ）**&#x200B;とマークされた手順は、クラウドインフラストラクチャ上のCommerceに適用されます。 その他のほとんどの推奨事項は、オンプレミスのデプロイメントにも適用されます。

## Fastly リクエストキャッシュの最適化（クラウドのみ） {#optimize-fastly-request-caching}

[!DNL Fastly]は、オリジン サーバーの負荷を軽減するために、エッジに応答をキャッシュします。 特に、トラッキングパラメーターやヘッドレスストアフロントを使用してプロモーションを実施している場合、繁忙期には、いくつかの設定チェックがそのキャッシュを最大限に活用するのに役立ちます。 完全な構成リファレンスについては、[&#x200B; キャッシュ構成のカスタマイズ &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/cdn/setup-fastly/fastly-custom-cache-configuration)を参照してください。

* トラッキングパラメーターを正規化する：ホリデーシーズンには、Google Ads、Facebook、Xなどのソーシャルおよび有料キャンペーンを実行する可能性が高く、すべてのURLに一意のトラッキング文字列を追加します。 一意の文字列ごとに、同じページのキャッシュエントリが個別に作成されるため、キャッシュヒット率が低下します。 これらのパラメーターをAdobe Commerce管理者の[!DNL Fastly]設定の&#x200B;**[!UICONTROL 無視URL パラメーター]** リストに追加して、[!DNL Fastly]が同等のパラメーターとして扱えるようにします。
* ランディングページがキャッシュ可能であることを確認します。各プロモーションランディングページの`x-cache`応答ヘッダーを確認します。 キャッシュ可能なページは、後続の読み込みに対して`HIT`または`HIT`/`MISS` ペアを返します。 ヘッダーが`MISS, MISS`を返す場合、ページはキャッシュされていないため、調査が必要です。
* GraphQL クエリにGET リクエストを使用する：PWAまたはヘッドレスストアフロントを実行する場合、GraphQL クエリを`POST` リクエストではなく、URLに含まれる`GET` リクエストとして送信します。 [!DNL Fastly]は、クエリがURLの一部である`GET`件のリクエストのみをキャッシュします。 本文で送信されたクエリを含む`GET` リクエストはキャッシュされません。

>[!NOTE]
>
>[!DNL Fastly] オリジンのシールドは、キャッシュのパフォーマンスにも影響します。 設定の詳細については、[Fastly オリジンシールド &#x200B;](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/scalability-capacity-planning.md#fastly-origin-shielding)を参照してください。

## Fastly IOを有効にする（クラウドのみ） {#enable-fastly-io}

[!DNL Fastly] IOは、画像のサイズ変更とフォーマット変換を、Adobe Commerce オリジンではなく[!DNL Fastly] エッジネットワークにオフロードします。 これにより、トラフィックの多い販売期間中に一般的なボトルネックとなる、画像量の多いストアフロントのサーバー負荷を軽減し、ページのレンダリング速度を向上できます。 設定オプションについては、[Fastlyの画像最適化](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/cdn/fastly-image-optimization)を参照してください。

開始する前に、オリジンのシールドが設定されていることを確認します。[!DNL Fastly] IOでは、前提条件としてオリジンのシールドが必要です。 設定の詳細については、[Fastly オリジンシールド &#x200B;](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/scalability-capacity-planning.md#fastly-origin-shielding)を参照してください。

[!DNL Fastly] IOを有効にするには：

1. 管理者で、**[!UICONTROL Fastly設定]** ページに移動し、**[!UICONTROL デフォルト IO設定オプション]**&#x200B;の横にある&#x200B;**[!UICONTROL 設定]**&#x200B;を選択します。
1. [!DNL Fastly] IO スニペットが有効になっていることを確認します。
1. **[!UICONTROL 画像の最適化]**&#x200B;設定で、**[!UICONTROL 詳細な画像の最適化を有効にする]**&#x200B;を&#x200B;*[!UICONTROL はい]*&#x200B;に設定します。 この設定は、Adobe Commerceの組み込み画像サイズ変更を無効にし、タスクを[!DNL Fastly]に転送します。
1. シールドの場所が正しく設定されていることを確認します。 設定の詳細については、[Fastly オリジンシールド &#x200B;](#fastly-origin-shielding)を参照してください。

>[!NOTE]
>
>ディープ画像最適化では、商品画像のみのサイズに変更されます。 バナーやコンテンツブロックなどのCMS画像は影響を受けず、Adobe Commerceの組み込みのサイズ変更を引き続き使用します。

[!DNL Fastly] IOが機能していることを確認するには、製品画像リクエストの応答ヘッダーを確認します。

* `x-cache` ヘッダーは`HIT`を返します。
* `fastly-io-info`と`fastly-stats`のヘッダーが入力されています。
* 画像URLに`/cache/` ディレクトリがパスに含まれていません。

## Redis L2 キャッシュの実装 {#implement-redis-l2-cache}

効果的なキャッシュ方法を実装し、トラフィックのピーク時にストアが確実に機能するようにします。[!DNL Redis] L2 キャッシュは、各web ノードにキャッシュ データをローカルに保存することで、ネットワーク帯域幅を[!DNL Redis]に削減します。 L2 キャッシュの仕組みについて詳しくは、[&#x200B; レベル 2 キャッシュ &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/cache/level-two-cache)を参照してください。

クラウドインフラストラクチャ上のCommerceで、`REDIS_BACKEND` デプロイ変数を設定して、これを有効にします。 設定手順については、『Commerce on Cloud Infrastructure Guide 』の[REDIS_BACKEND](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/configure/env/stage/variables-deploy#redis_backend)を参照してください。 オンプレミスでは、`app/etc/env.php`で直接設定します。

>[!NOTE]
>
>[!DNL Redis]は、Adobe Commerce 2.4.9以降、または2.4.5-p16、2.4.6-p14、2.4.7-p9、または2.4.8-p4以降のパッチリリースでは、L2 キャッシュバックエンドとしてサポートされていません。 これらのバージョンでは、代わりに`VALKEY_BACKEND`を使用してください。

## MySQLおよびRedis スレーブ接続を有効にする（クラウドのみ） {#enable-mysql-and-redis-slave-connections}

[!DNL Redis]および[!DNL MySQL] スレーブ接続は、読み取りトラフィックをレプリカノードにオフロードし、トラフィックが多い期間におけるマスター接続の負荷を軽減します。 設定手順については、Adobe Commerceのバージョンに応じて、[MYSQL_USE_SLAVE_CONNECTION](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/configure/env/stage/variables-deploy#mysql_use_slave_connection)および[REDIS_USE_SLAVE_CONNECTION](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/configure/env/stage/variables-deploy#redis_use_slave_connection)または[VALKEY_USE_SLAVE_CONNECTION](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/configure/env/stage/variables-deploy#valkey_use_slave_connection)を参照してください。

### Redis スレーブ接続

[!DNL Redis] スレーブ接続は、[!DNL Redis] インスタンスへの読み取り専用接続であり、読み取りトラフィックを非マスターノードから提供できるようにします。 これを有効にしないと、[!DNL MySQL]は高負荷のボトルネックに陥る可能性があります。 [!DNL New Relic]のAPM概要チャートで、応答時間が増加していることを早期署名として確認してから、**[!UICONTROL データベース]** タブで、最も時間のかかるトランザクションで並べ替えて、遅い[!DNL MySQL] `SELECT` クエリを特定します。 デプロイ変数`REDIS_USE_SLAVE_CONNECTION`を`true`に設定して、これを有効にします。

>[!NOTE]
>
>`REDIS_USE_SLAVE_CONNECTION`は、ステージング環境およびProduction Pro クラスター環境でのみサポートされています。 スタータープロジェクトまたはスケール化（分割）されたアーキテクチャプロジェクトではサポートされていません。 拡張アーキテクチャで有効にすると、[!DNL Redis]接続エラーが発生します。代わりに、そのアーキテクチャで[!DNL Redis]個のL2 キャッシュを使用してください。 上記の[Redis L2 キャッシュの実装](#implement-redis-l2-cache-implement-redis-l2-cache)を参照してください。

### MySQL スレーブ接続

Pro クラスター環境の`MYSQL_USE_SLAVE_CONNECTION` フラグを有効にして、特定の読み取り専用データベースクエリをスレーブ接続に直接送信し、マスター接続からクエリ実行をオフロードします。

>[!CAUTION]
>
>本番環境でいずれかの設定を有効にする前に、ロード テストを実行します。 通常の負荷の環境では、スレーブ接続によってパフォーマンスが10～15%低下する可能性があります。 負荷が大きく持続的な環境では、同様のマージンでパフォーマンスを向上させることができます。 有効化する前に、予想されるピークシーズンのトラフィックの下で評価します。

## 非同期注文とメール処理を有効にする {#enable-asynchronous-order-and-email-processing}

非同期処理を使用して、大量の注文関連の操作をバックグラウンドでキューに入れて実行し、ピーク時のトラフィック中のフロントエンドの遅延を低減します。 ここでは、関連する3つの異なる設定について説明します。概要については、[設定のベストプラクティス &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/configuration)を参照してください。

* 非同期注文プレースメント：非同期注文モジュールは、注文を受信した状態としてマークし、キューに入れ、注文をファーストインファーストアウト処理します。 デフォルトでは無効になっています。 コマンドラインから有効にします。

  ```
  bin/magento setup:config:set --checkout-async 1
  ```

  有効にすると、注文の詳細はすぐに使用できなくなります。注文は、`placeOrderProcess`の消費者が在庫と照合して検証し（デフォルトで有効）、更新されるまでキューに入ったままになります。 このモジュールを無効にする前に、すべての実行中の非同期注文が処理を完了したことを確認してください。 詳しくは、[&#x200B; チェックアウトパフォーマンスのベストプラクティス &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/high-throughput-order-processing)を参照してください。

* 非同期注文データ処理：集中的なストアフロント販売と集中的な注文処理は、データベースレベルで競合する可能性があります。 この設定を有効にすると、2つのトラフィックパターンが区別されるので、注文は一時的なストレージに配置され、衝突することなくOrder Managementグリッドに一括で移動されます。 これにより、注文、請求書、出荷、クレジットメモのグリッドがクローズごとに更新されるため、ロックが回避され、処理時間が短縮されます。 最良の結果を得るには、cronを1分に1回実行するように設定します。

>[!NOTE]
>
>これを有効にする方法は、デプロイメントモードによって異なります。 クラウドインフラストラクチャ上のAdobe Commerce ステージング環境と実稼動環境は、デフォルトで実稼動モードで実行されます。この設定は、管理者を通じて使用することはできません。 実稼動モードでは、代わりに`bin/magento config:set dev/grid/async_indexing 1`を実行します。 デフォルトモードで、**[!UICONTROL Stores]** > **[!UICONTROL Configuration]** > **[!UICONTROL Advanced]** > **[!UICONTROL Developer]** > **[!UICONTROL Grid Settings]**&#x200B;に移動し、**[!UICONTROL 非同期インデックス]**&#x200B;を&#x200B;*[!UICONTROL Enable]*&#x200B;に設定します。

詳しくは、[&#x200B; スケジュールされた注文操作](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/order-management/orders/order-scheduled-operations)を参照してください。

* 非同期メール通知：この設定は、チェックアウトと注文処理メール通知をバックグラウンドに移動します。 **[!UICONTROL 店舗]** > **[!UICONTROL 設定]** > **[!UICONTROL 営業]** > **[!UICONTROL 営業メール]** > **[!UICONTROL 一般設定]** > **[!UICONTROL 非同期送信]**&#x200B;で有効にします。

## スケジュール時に更新するインデクサーを設定する {#configure-indexers-for-update-on-schedule}

インデクサーをスケジュールモードで実行するように設定することで、データベースのロックを回避し、カタログの頻繁な更新中の応答性を向上させます。 詳しくは、[&#x200B; インデクサー設定に関するベストプラクティス &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-operations/implementation-playbook/best-practices/maintenance/indexer-configuration)を参照してください。

インデクサーは、**[!UICONTROL 保存]**&#x200B;の更新または&#x200B;**[!UICONTROL スケジュール]**&#x200B;の更新モードで実行できます。

* **[!UICONTROL カタログやその他のデータが変更されるたびに、保存]** インデックスを直ちに更新します。 更新とブラウジングの強度が低いことを前提としており、高負荷時に大幅な遅延やデータの利用不能が発生する可能性があります。
* 実稼動用には、**[!UICONTROL スケジュール]**&#x200B;の更新をお勧めします。 専用のcron ジョブを通じて、データの更新やインデックス再作成に関する情報をバックグラウンドで保存します。

各インデクサーの更新モードを個別に&#x200B;**[!UICONTROL システム]** > **[!UICONTROL ツール]** > **[!UICONTROL インデックス管理]**&#x200B;に設定します。

>[!IMPORTANT]
>
>`customer_grid` インデクサーでサポートされているモードは、Adobe Commerceのバージョンによって異なります。 2.4.8より前のバージョンでは、Customer Gridは&#x200B;**[!UICONTROL 保存時の更新]**&#x200B;のみをサポートしています。スケジュール時の更新&#x200B;**[!UICONTROL に設定しないでください]**。 Adobe Commerce 2.4.8以降では、Customer Gridは両方のモードをサポートし、デフォルトで&#x200B;**[!UICONTROL スケジュールに従って更新]**&#x200B;するようになりました。

## カタログフラットテーブルの無効化と評価 {#disable-and-evaluate-catalog-flat-table}

製品とカテゴリにフラットテーブルを使用することは推奨されません。 この非推奨の機能は、パフォーマンスの低下とインデックス作成の問題を引き起こす可能性があります。 詳しくは、[&#x200B; フラットカタログ &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/catalog/catalog-flat)を参照してください。

フラットカタログを無効にするには、**[!UICONTROL Stores]** > **[!UICONTROL Configuration]** > **[!UICONTROL Catalog]** > **[!UICONTROL Catalog]** > **[!UICONTROL Storefront]**&#x200B;に移動し、**[!UICONTROL Use Flat Catalog Category]**&#x200B;を&#x200B;*[!UICONTROL No]*&#x200B;に設定し、**[!UICONTROL Use Flat Catalog Product]**&#x200B;を&#x200B;*[!UICONTROL No]*&#x200B;に設定してから、**[!UICONTROL Save Config]**&#x200B;をクリックします。

一部のサードパーティモジュールやカスタマイズでは、正しく機能するためにフラットテーブルが必要です。 フラットテーブルを無効にする前に、これらの拡張機能を使用し続ける影響とリスクを評価します。

## 拡張（分割）アーキテクチャを検討する（クラウドのみ） {#consider-scaled-split-architecture}

上記の設定とコードレベルの最適化を適用した後でも、負荷テストまたはライブインフラストラクチャのパフォーマンスにCPUやその他のリソースが引き続き表示される場合は、スケーリングされた（分割）アーキテクチャへの移行を検討してください。 詳しくは、[拡張アーキテクチャ &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/architecture/scaled-architecture)を参照してください。

>[!NOTE]
>
>拡張アーキテクチャは、Pro 48 クラスター以上を持つアカウントでのみ使用できます。

分割層アーキテクチャでは、最低6つのノードを使用します。[!DNL OpenSearch]または[!DNL Elasticsearch]、[!DNL MariaDB]、[!DNL Redis]または[!DNL Valkey]を実行している3つのサービスノードと、`php-fpm`および`NGINX`を実行している3つのweb ノードです。

* サービスノードは、サーバーサイズ（CPUとメモリ）を増やすことによって、垂直方向にのみ拡張できます。 データベースクラスターは高可用性のために構築されているため、サービスノードは信頼性の高い方法で水平方向に拡張できません。
* web ノードは垂直方向と水平方向の両方に拡張でき、web サーバーを追加してリクエスト量の増加に対応できます。

これにより、負荷の高い期間に必要に応じてインフラストラクチャを拡張し、各層を個別に拡張できます。 予想される負荷の高い時期に先立ってスプリットティアのアーキテクチャに切り替えるには、Adobeのアカウントチームにお問い合わせください。
