---
title: テストページをリダイレクト（非表示）
description: 内部テスト用のテストページ
hide: true
hidefromtoc: true
source-git-commit: ed472a699d30b12f3632cf658ae05ac420f931d3
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 0%

---

# テストページをリダイレクト（非表示）

リダイレクトを含む非表示のテストページ

## 標準の 1:1 リダイレクト

EXL: <https://experienceleague.adobe.com/docs/platform-learn/tutorials/rtcdp/b2b-overview.html>

EDS: <https://eds-stage.experienceleague.adobe.com/en/docs/platform-learn/tutorials/rtcdp/b2b-overview>

EXL: <https://experienceleague.adobe.com/docs/workfront/using/review-and-approve-work/proofing/create-proofs/create-proofs--in-wf.html>

EDS: https://eds-stage.experienceleague.adobe.com/en/docs/workfront/using/review-and-approve-work/proofing/create-proofs/create-proofs—in-wf

EXL: <https://experienceleague.adobe.com/docs/workfront/using/product-announcements/product-releases/quarterly-release/release-20-2/2020.2-release-overview.html>

EDS: <https://eds-stage.experienceleague.adobe.com/en/docs/workfront/using/product-announcements/product-releases/quarterly-release/release-20-2/2020.2-release-overview>

## ワイルドカードリダイレクト

（多対 1） `https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/*`

* EXL: <https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/bubba.html>
* EDS: <https://eds-stage.experienceleague.adobe.com/en/docs/analytics/analyze/reports-analytics/bubba>

(1:1) `https://experienceleague.adobe.com/docs/primetime/aiq-help/(*)`

* EXL: <https://experienceleague.adobe.com/docs/primetime/aiq-help/account-iq-components/segments-timeframe.html>
* EDS: <https://eds-stage.experienceleague.adobe.com/en/docs/primetime/aiq-help/account-iq-components/segments-timeframe>

(1:1) `https://experienceleague.adobe.com/docs/adobe-campaign-insider-events/events/(*)`

* EXL: <https://experienceleague.adobe.com/docs/adobe-campaign-insider-events/events/2022/microsoft.html>
* EDS: <https://eds-stage.experienceleague.adobe.com/en/docs/adobe-campaign-insider-events/events/2022/microsoft>

## その他のリダイレクト

ランディングページ、その他のドメイン、nginx 設定

<https://one.workfront.com/s/managed-content-videos/welcome-to-workfront-MCFSRY5DWNL5EENJI3JD6XIB3TOM>

<https://experienceleague.adobe.com/docs/events.html>