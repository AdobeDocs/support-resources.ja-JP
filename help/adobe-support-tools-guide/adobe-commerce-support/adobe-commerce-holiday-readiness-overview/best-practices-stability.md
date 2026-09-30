---
title: ベストプラクティスと安定性
description: Adobe Commerceを利用するマーチャントが、ホリデーシーズンなどの交通量の多いイベントに備えるためのベストプラクティスと安定性に関する推奨事項。
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
TQID: 'https://experienceleague.adobe.com/iA6ioGYYgQSotPrPqujDBdRcjBLUQXMGXfwlcSMGjkM'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: cdfd3bc1-dc23-5cf0-b965-d3c0c55cde67
    internal-label: Best Practices
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
subfeature_v2:
  - id: 3c398179-d35a-51ba-b317-6c5b95feef5e
    internal-label: Logs
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 71589dd124714805fbf844540fb2d272433631ee
workflow-type: tm+mt
source-wordcount: '861'
ht-degree: 4%
---

# ベストプラクティスと安定性

このセクションでは、ホリデーシーズンなどのトラフィックの多いイベント用に、Commerce on cloud インフラストラクチャとオンプレミスの両方のAdobe Commerce環境を準備するための技術的な推奨事項について説明します。

>[!NOTE]
>
>**（クラウドのみ）**&#x200B;とマークされた手順は、クラウドインフラストラクチャ上のCommerceに適用されます。 その他のほとんどの推奨事項は、オンプレミスのデプロイメントにも適用されます。

## 最新バージョンのAdobe Commerceへのアップグレード {#upgrade-to-latest-version-of-adobe-commerce}

サイトがサポートされていないバージョンのAdobe Commerceになっていないことを確認します。これにより、サイトのパフォーマンスに影響を与え、セキュリティ問題に対する脆弱性が高まる可能性があります。 最新バージョンのAdobe Commerceにアップグレードして、安全でホリデーシーズンに備えることができます。

Adobe Commerceの[最新リリース &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-operations/release/notes/overview)には、以前のバージョンからアップグレードする際にプロジェクトに役立つ機能強化や軽減された問題など、多くの[重要なセキュリティ修正](https://experienceleague.adobe.com/en/docs/commerce-operations/release/notes/security-patches/overview)が含まれています。

サポートされていないバージョンのAdobe Commerceについて詳しくは、[Adobe Commerceのライフサイクルポリシー](https://experienceleague.adobe.com/ja/docs/commerce-operations/release/planning/lifecycle-policy)を参照してください。

## 最新のECE-ToolsとQPT （Quality Patch Tool）をインストールする {#install-latest-ece-tools-and-quality-patch-tool-qpt}

`--with-dependencies` スイッチを使用して、最新の`ece-tools` モジュールとその依存モジュールがインストールされていることを確認し、お使いのAdobe Commerceのバージョンに必要なすべてのクラウドパッチが適切にインストールされるようにします。 手順については、[ECE-Tools パッケージの更新](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/dev-tools/ece-tools/update-package)を参照してください。

品質パッチツールで使用可能なパッチリストを確認し、Adobe Commerceのバージョンと互換性のあるパフォーマンスパッチが適用されていることを確認します。 「[品質パッチツール：パッチを検索](https://experienceleague.adobe.com/ja/docs/commerce-operations/tools/quality-patches-tool/patches-available-in-qpt/patches-available-in-qpt-tool-overview)」を参照してください。

>[!NOTE]
>
>QPTは、Adobe Commerce オンクラウドインフラストラクチャとオンプレミスの両方で使用できます。 インストールと使用のコマンドは2つの間で異なります。Cloudの場合、QPTはECE-Tools パッケージに含まれています。

## ログファイルの確認とクリーニング {#review-and-clean-log-files}

クラウド環境のログファイル（例えば、`~/var/log`以下のアプリケーションログファイル）を確認し、デフォルトまたはカスタムログファイルに書き込まれる頻繁に記録されるレコードを特定します。 詳しくは、[&#x200B; ログの表示と管理](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/develop/test/log-locations)を参照してください。

* 次の既定のログ ファイルを確認し、繰り返し発生するエラーを修正します：`~/var/log`、`~/var/log/exception.log`、`~/var/log/support_report.log`、`~/var/log/system.log`、`~/var/report`。
* 過去の問題のトラブルシューティング用に以前に追加したデバッグログを削除します。

これらのログは[!DNL New Relic]でも利用できます。[New Relic log management](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/monitor/new-relic/log-management)を参照してください。

## ディスクサイズの増加を監視する {#monitor-disk-size-growth}

Adobe Commerce on cloud インフラストラクチャには、2つのメインディスクボリュームがあります。 これらのボリュームを監視して、トラフィックが多い場合に十分な空き容量があることを確認します。 Adobe Commerceでは、いずれかのボリュームが使用率70%を超えた場合に警告が表示されます。

* `/mnt/shared` （ログとメディア ファイルを含む共有ファイル）
* `/data/mysql` （データベースボリューム）

詳しくは、[&#x200B; ディスク領域の管理](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/develop/storage/manage-disk-space)を参照してください。

## 最も遅いデータベース要求の確認 {#review-slowest-database-requests}

[!DNL New Relic]で最も時間がかかるデータベース トランザクションを定期的に監視および確認することが重要です。 大幅に遅いクエリとコンポーネントを調査します。

* **最も時間のかかるトランザクションを確認する：** **[!UICONTROL New Relic]** > **[!UICONTROL APM &amp; Services]** > select environment > **[!UICONTROL Databases]**&#x200B;に移動し、最も時間のかかるトランザクションで並べ替えます。

* **MySQLのスロークエリログを確認します。** システムによって記録されたスロークエリーについて、`mysql-slow.log`を確認します。 これらのログは[!DNL New Relic]でも利用できます。**[!UICONTROL New Relic]** > **[!UICONTROL ログ]**&#x200B;に移動し、`filePath:"/var/log/mysql/mysql-slow.log"`でフィルタリングします。

[!DNL MySQL]のスロークエリログを定期的に確認して、スロークエリーが頻繁に実行されていないことを確認します。 問題があると特定したクエリを解決する手順については、[&#x200B; データベースパフォーマンスの問題を解決する](https://experienceleague.adobe.com/en/docs/commerce-operations/implementation-playbook/best-practices/maintenance/resolve-database-performance-issues)を参照してください。

## cron ジョブの設定 {#configure-cron-jobs}

Commerceのすべての非同期処理は、Linux cron コマンドを使用して実行されます。

Commerceは、インデックス作成やキューのコンシューマーオペレーションなど、重要なシステム機能に対する適切なcron ジョブ設定に依存します。 適切に設定しないと、Commerceが期待どおりに機能しません。

Unix crontab ファイルで適切なUnix ユーザーを使用して、Commerce cronを正しく設定することが重要です。 各Unix ユーザーには独自のcrontab ファイルがあります。これは、そのユーザーのcron ジョブを実行するために使用される設定です。 手順については、[cron ジョブの設定と実行](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs)を参照してください。

スクリプト `dev/tools/cron.sh`は削除されたため、実行できなくなりました。

## クライアントサイド設定の最適化 {#optimize-client-side-settings}

Commerce インスタンスのストアフロントの応答性を向上させるには、**[!UICONTROL ストア]** > **[!UICONTROL 構成]** > **[!UICONTROL 詳細]** > **[!UICONTROL 開発者]**&#x200B;の下で次の設定を行います。この設定は、開発者モードでのみ使用できます。

* **[!UICONTROL グリッド設定]** > **[!UICONTROL 非同期インデックス]**: *[!UICONTROL 有効]*
* **[!UICONTROL CSS設定]** — **[!UICONTROL CSS ファイルを縮小]**: *[!UICONTROL はい]*
* **[!UICONTROL JavaScript Settings]** — **[!UICONTROL JavaScript ファイルを縮小]**: *[!UICONTROL はい]*
* **[!UICONTROL JavaScript Settings]** — **[!UICONTROL JavaScript バンドルを有効にする]**: *[!UICONTROL はい]* （デフォルトでは有効になっていません）
* **[!UICONTROL テンプレート設定]** — **[!UICONTROL HTMLを縮小]**: *[!UICONTROL はい]*

Cloud上のAdobe Commerceは常に実稼動モードで実行されるため、代わりにコマンドラインから各オプション（例：`bin/magento config:set --lock-config dev/css/minify_files 1`）を設定し、結果として生じる`app/etc/config.php`の変更を確定して再デプロイします。 CLI パスの完全なリストについては、[&#x200B; リソースファイルの最適化](https://experienceleague.adobe.com/en/docs/commerce-operations/implementation-playbook/best-practices/development/optimize-css-js-files)を参照してください。
