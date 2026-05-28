---
title: サポート通知にチームメンバーを含める方法
description: この記事では、サポート通知にチームメンバーを含める方法について説明します。
feature: Cloud, Support, Admin Workspace
role: Admin, Developer
solution: Commerce
feature-set: Commerce
exl-id: 392ef795-f710-401f-8b0e-3c8dfec7bb3a
TQID: 'https://experienceleague.adobe.com/fWRfvDT8NCwPfzmAx1Zowo4T8KvKLKWqhDkZDfX8stU'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: e7dae43f-215c-4cdf-90d3-c5a461a6e669
subfeature_v2:
  - id: bb2df8be-afdd-4818-b6b5-95ca1dd3bc3a
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 9f1760d31cd80e0358aa341c3f6091b2a86b6d67
workflow-type: tm+mt
source-wordcount: 305
ht-degree: 12%

---


# サポート通知にチームメンバーを含める方法

この記事では、メール通知でサポートのアップデートを自動的に受信するために、チームメンバーを含める方法を説明します。

## 影響を受ける製品とバージョン

* クラウドインフラストラクチャ上のAdobe Commerce、すべての[&#x200B; サポートされているバージョン &#x200B;](https://www.adobe.com/content/dam/cc/en/legal/terms/enterprise/pdfs/Adobe-Commerce-Software-Lifecycle-Policy.pdf)。

## 原因

* 必要な権限を持つチームメンバーが[!DNL cloud project]に追加されていません。
* チームメンバーはサポートアカウントを持っていません。

## ソリューション

1. **[!DNL Cloud Project URL]**&#x200B;に移動します（例：`https://us-3.magento.cloud/projects/xxxxxx/edit`）。
1. チームメンバーがプロジェクトに追加され、[!DNL Project Admin]であるかどうかを確認します。

プロジェクトに追加されていない場合は、それらを[!DNL Project Admin]として追加し、[!DNL Shared Access]を付与する必要があります。

* ユーザーガイドの[&#x200B; ユーザーアクセスの管理](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html?lang=ja)。
* [Commerce ナレッジベースのAdobe Commerce クラウドプロジェクト &#x200B;](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/unable-add-user-adobe-commerce-cloud-project.html?lang=ja)にユーザーを追加できません。
* [Adobe Commerce ヘルプセンターユーザーガイド：共有アクセス &#x200B;](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html?lang=ja#shared-access) （Commerce ナレッジベース）

[!DNL cloud project]に追加されたが、[!DNL Project Admin role]を持っていない場合は、[&#x200B; ユーザーアクセスの管理](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html?lang=ja)で、それに応じて[!DNL role]を更新してください。

組織で開かれたすべてのケースでチームメンバーがウォッチャーになるようにしたい場合は、[&#x200B; サポートチケット &#x200B;](https://experienceleague.adobe.com/home?lang=ja&support-tab=home#support)を送信します。

## 関連トピックス

[以前のチームメンバーがAdobe Commerce cloud通知メールを受信する](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/former-teammembers-receive-cloud-notification-emails.html?lang=ja)
