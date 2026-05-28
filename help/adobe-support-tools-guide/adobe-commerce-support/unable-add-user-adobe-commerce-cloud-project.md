---
title: Adobe Commerce クラウドプロジェクトにユーザーを追加できません
description: この記事では、Adobe Commerce クラウドプロジェクトにユーザーを追加できない場合の解決策を紹介します。
feature: Cloud, Paas
solution: Commerce
feature-set: Commerce
role: Developer
exl-id: 2dc52d5e-0930-48c4-986e-ce3f9f6f8221
source-git-commit: 755c6dc9cff041b9ca9183fbecde21f90fbaee1a
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---

# Adobe Commerce クラウドプロジェクトにユーザーを追加できません

この記事では、ユーザーをクラウドプロジェクトに追加しようとしたが、エラーが発生して失敗した場合の解決策を示します。*ユーザーXXXが存在しません*。

## 影響を受ける製品とバージョン

* クラウドインフラストラクチャ上のAdobe Commerce、[&#x200B; サポートされているすべてのバージョン &#x200B;](https://magento.com/sites/default/files/magento-software-lifecycle-policy.pdf)

## 問題

この記事では、Adobe Commerce クラウドプロジェクトにユーザーを追加できない場合の解決策を紹介します。

## 原因

ユーザーのアカウントは、プロジェクトにユーザーとして追加する前に、最初に[https://accounts.magento.cloud](https://accounts.magento.cloud)に作成し、Adobe SSOにリンクする必要があります。 ユーザーがAdobe アカウントを持っているが、Commerce（magento.com）アカウントを持っていない場合は、最初にアカウントを作成する必要があります。

## ソリューション

1. [https://accounts.magento.cloud](https://accounts.magento.cloud)でログインするようにユーザーに依頼します。 ユーザーは、同じメールアドレスを使用してAdobeに既に登録されている必要があります。
   >[!NOTE]
   >[https://account.adobe.com](https://account.adobe.com)にアカウントを作成または持っているということは、ユーザーが[https://accounts.magento.cloud](https://accounts.magento.cloud)にアカウントを持っているとは限りません。 ユーザーは最初に[Commerce アカウントを作成する必要があります](https://experienceleague.adobe.com/ja/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account)。

1. ユーザーが既にAdobe アカウントを持っているがログインできない場合は、[!UICONTROL 問題理由]が&#x200B;*User Management*&#x200B;に設定された[&#x200B; サポートリクエスト &#x200B;](https://experienceleague.adobe.com/home?lang=ja#support)を送信するように依頼します。

1. ユーザーが[https://accounts.magento.cloud](https://accounts.magento.cloud)に正常にサインインしたら、ユーザーをプロジェクトに追加できます。 詳細な手順については、「Commerce on Cloud Infrastructure ガイド」の「[&#x200B; ユーザーの追加とアクセスの管理](https://experienceleague.adobe.com/ja/docs/commerce-cloud-service/user-guide/project/user-access#add-users-and-manage-access)」を参照してください。

## 関連トピックス：

* Commerce on Cloud Infrastructure ガイドの[&#x200B; ユーザーアクセスの管理](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html?lang=ja)。
* [Adobe Commerce サポートまたはクラウドアカウントにログインできない](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/unable-to-log-in-to-support-or-cloud-project.html?lang=ja)
