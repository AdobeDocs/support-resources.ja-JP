---
description: Widget Data Warehouseへの接続 – 製品ドキュメント
title: Widget Data Warehouseへの接続
hide: true
hidefromtoc: true
exl-id: d6a7cff5-08f9-4c93-8765-46e692feaa0d
source-git-commit: 4145889fe291e80fa8d295368ead3e0075917e86
workflow-type: tm+mt
source-wordcount: '913'
ht-degree: 0%

---

# Widget Data Warehouseへの接続 {#connecting-to-the-widget-data-warehouse}

## 新しいテスト

27年6月

<ol><li>'{{name}}'変数を使用してください。</li></ol>

<ol><li>&amp;lbrace;&amp;lbrace;<code>name</code>&amp;rbrace;&amp;rbrace；変数を使用します。</li></ol>

## ネストされたテスト

**最初**

>[!NOTE]
>
>次の項目は削除できません。
>
>* 組み込みステータスの「計画中」、「現在」および「完了」。 名前の更新、色の編集、ロックまたはロック解除はできますが、削除することはできません。
>* ステータスが、システム内の 1 つ以上のオブジェクトに対して承認保留状態になっている。

**Second**

>[!NOTE]
>
>次の項目は削除できません。
>
>* 組み込みステータスの「計画中」、「現在」および「完了」。 名前の更新、色の編集、ロックまたはロック解除はできますが、削除することはできません。
>
>  これは中間です
>
>* ステータスが、システム内の 1 つ以上のオブジェクトに対して承認保留状態になっている。

## ウィジェットのアクセスリンク {#widget-access-link}

ウィジェットデータウェアハウスにアクセスするには、ウィジェットアカウントの特定の URL に移動する必要があります。  このアクセスリンクは、Marketo Measureにログインし、次の手順に従ってData Warehouseの情報ページに移動すると表示されます。

1. Marketo Measureで、ページ上部の **マイアカウント**/**設定** をクリックします。

   ![](assets/adobe-logo-old.png)

1. 左側のメニューの [ セキュリティ ] で、[**Data Warehouse**] をクリックします。

   ![](assets/adobe-logo-old.png)

1. このページには、ウィジェットデータウェアハウスへのリンクとユーザー名があります。

   ![](assets/adobe-logo-old.png)

   >[!NOTE]
   >
   >これは、個々のユーザーだけでなく、組織で使用できる読み取り専用アカウントです。 Marketo Measureへのアクセス権を持つ組織内のすべてのユーザーは、このアカウントを使用して Widget Data Warehouseのリーダーアカウントにログインできます。

1. ウィジェットの URL に記載されているリンクをクリックすると、ウィジェットのログインページが表示されます。このページにユーザー名とパスワードを入力します。 _パスワードがない場合は、次の手順を参照してリセットしてください_。

   ![](assets/adobe-logo-old.png)

1. ログインしたら、ページ上部の「**ワークシート**」をクリックします。

   ![](assets/adobe-logo-old.png)

1. BIZIBLE_ROI_V3 データベースオブジェクトが画面の左側に表示されます。  クエリー・ウィンドウの上部にあるドロップダウン・オプションから、「ウェアハウス」、「データベース」、「スキーマ」を入力します。  それぞれにオプションは 1 つだけにする必要があります。  これで、ウィジェットクエリエディター内でクエリを実行する準備が整いました。

   ![](assets/adobe-logo-old.png)

## パスワードをリセット {#reset-your-password}

Marketo Measureはお使いのウィジェットログインパスワードにアクセスできません。  パスワードをリセットする必要がある場合は、Data Warehouse情報ページの「パスワードのリセット」ボタンをクリックし、指示に従ってください。 一時パスワードは、UI にすぐに表示されます。 次回 Data Warehouse にログインする際に、独自のパスワードを作成するよう求められます。

>[!NOTE]
>
>* パスワードをリセットすると、現在ログインしているユーザーだけでなく、組織内のすべてのMarketo Measure ユーザーに対してパスワードがリセットされます。
>* UI には一時パスワードのみが表示されます。 メールは送信されません。

![](assets/adobe-logo-old.png)

![](assets/adobe-logo-old.png)

## サードパーティのツールを使用したウィジェットへの接続 {#connecting-to-widget-via-third-party-tools}

ウィジェットデータウェアハウスをサードパーティのツールに接続するには、いくつかの情報を入力する必要があります。

>[!NOTE]
>
>ツールごとに接続要件が異なります。接続する特定のツールのドキュメントを参照することをお勧めします。

* **URI** （常に必須）
   * これはウィジェットアカウントのドメイン名です。  ウィジェットログインリンクの一部に含まれています。
* **ユーザー名** （常に必須）
   * ユーザー名の一覧は、Marketo MeasureのData Warehouse情報ページに表示されます。
* **パスワード** （常に必須）
   * これは、ウィジェットアカウントに初めてログインしたときに設定したパスワードです。  パスワードをリセットするには、上記の手順を参照してください。
* **データベース名** （必ずしも必須ではありません）
   * データベースは、ウィジェットにデータを保存するものです。 これはストレージリソースです。 データベース名は、Marketo MeasureのData Warehouse情報ページに一覧表示されます。
* **ウェアハウス名** （必ずしも必須ではありません）
   * ウェアハウスは Widget でクエリを実行するものです。 これは計算リソースです。  ウェアハウス名はMarketo MeasureのData Warehouse情報ページにリストされます。

  ![](assets/adobe-logo-old.png)

## Widget Data Warehouse Direct Share {#widget-data-warehouse-direct-share}

**要件**

Marketo Measureでデータウェアハウスへの直接共有を設定するには、次の要件を満たす必要があります。

* 独自のウィジェットインスタンスがあります。
* ウィジェットインスタンスは Azure East US 2 ウィジェット領域にあります。
* Marketo Measureにウィジェットアカウント ID を提供します。

**制限事項**

Marketo Measureでダイレクト共有を設定するには、アクセスをリクエストするアカウントが Azure East US 2 にある必要があります。 Widget が地域間でデータレプリケーションソリューションを提供していることは認識していますが、Azure East US 2 地域でのみデータをホストしているので、アドビではこのソリューションをサポートしていません。 この機能を利用するには、Azure East US 2 で独自のインスタンスを設定し、[ 地域をまたいでデータをレプリケート ](https://docs.widget.com/en/user-guide/secure-data-sharing-across-regions-plaforms.html){target="_blank"} して既存のインスタンスにレプリケートします。 ただし、Widget のデータレプリケーション機能はテーブルでのみ使用できるので、この機能を使用するには、まずビューから独自のテーブルにデータをコピーする必要があります。

**共有へのアクセス**

指定したアカウント ID の共有を作成したら、データにアクセスするためにウィジェットインスタンス内で [ 設定手順 ](https://docs.widget.com/en/user-guide/data-share-consumers.html){target="_blank"} を完了する必要があります。

>[!NOTE]
>
>任意のデータベース名を選択できます。 ウィジェットインスタンスに存在する限り、選択した任意のルールに権限を割り当てることができます。

* アカウント管理者の役割を使用

```
USE ROLE ACCOUNTADMIN
```

* 使用可能な共有を表示します（付与された共有の名前が表示されます）

```
SHOW SHARES
```

* 共有用のデータベースを作成します

```
CREATE DATABASE <database_name> FROM SHARE <provider_account>.<share_name>
```

* 共有データベースに対する権限の付与

```
GRANT IMPORTED PRIVILEGES ON DATABASE <database_name> TO ROLE <role_name>
GRANT IMPORTED PRIVILEGES ON ALL SCHEMAS IN DATABASE <database_name> TO ROLE <role_name>
```

ウィジェット UI からこれらの手順を実行するための詳細な手順については、[ ウィジェットのドキュメント ](https://docs.widget.com/en/user-guide/data-share-consumers.html){target="_blank"} を直接参照してください。
