---
description: WidgetData Warehouseへの接続 — 製品ドキュメント
title: ウィジェットへのData Warehouse
hide: true
hidefromtoc: true
source-git-commit: fcf5fb8f9728dd27a81de21241a71ce49dd015f8
workflow-type: tm+mt
source-wordcount: '911'
ht-degree: 0%

---

# ウィジェットへのData Warehouse {#connecting-to-the-widget-data-warehouse}

## 新規テスト

<ol><li>「 」を使用します。{{name}}'変数。</li></ol>

<ol><li>&amp;lbrace;&amp;lbrace；を使用<code>name</code>&amp;rbrace;&amp;rbrace；変数。</li></ol>

## ネストされたテスト

**最初**

>[!NOTE]
>
>次の項目は削除できません。
>
>* 組み込みステータスの「計画」、「現在」、「完了」。 名前の更新、色の編集、ロックまたはロック解除は可能ですが、削除することはできません。
>* システム内の 1 つ以上のオブジェクトに対して承認待ち状態のステータス。

**Second**

>[!NOTE]
>
>次の項目は削除できません。
>
>* 組み込みステータスの「計画」、「現在」、「完了」。 名前の更新、色の編集、ロックまたはロック解除は可能ですが、削除することはできません。
>
>  これは、次の間にあります。
>
>* システム内の 1 つ以上のオブジェクトに対して承認待ち状態のステータス。

## ウィジェットアクセスリンク {#widget-access-link}

ウィジェットデータウェアハウスにアクセスするには、ウィジェットアカウントの特定の URL に移動する必要があります。  このアクセスリンクを見つけるには、Marketo Measureにログインし、次の手順に従って、Data Warehouse情報ページに移動します。

1. Marketo Measureのページ上部で、「 **マイアカウント** > **設定**.

   ![](assets/adobe-logo-old.png)

1. 左側のメニューの [ セキュリティ ] で、[ **Data Warehouse**.

   ![](assets/adobe-logo-old.png)

1. このページには、ウィジェットデータウェアハウスへのリンクとユーザー名が表示されます。

   ![](assets/adobe-logo-old.png)

   >[!NOTE]
   >
   >これは、個々のユーザーだけでなく、組織で使用できる読み取り専用アカウントです。 Marketo Measureにアクセスできる組織内のユーザーは、このアカウントを使用して WidgetData Warehouseリーダーアカウントにログインできます。

1. ウィジェット URL に含まれるリンクをクリックすると、ウィジェットのログインページが開き、ユーザー名とパスワードを入力できます。 _パスワードをお持ちでない場合は、以下の手順を参照してリセットしてください。_.

   ![](assets/adobe-logo-old.png)

1. ログインしたら、「 **ワークシート** をクリックします。

   ![](assets/adobe-logo-old.png)

1. BIZIBLE_ROI_V3 データベースオブジェクトは画面の左側に表示されます。  クエリー・ウィンドウの上部にあるドロップダウン・オプションから「ウェアハウス」、「データベース」および「スキーマ」を入力します。  それぞれに 1 つのオプションのみを指定します。  これで、ウィジェットクエリエディター内でクエリを実行する準備が整いました。

   ![](assets/adobe-logo-old.png)

## パスワードをリセット {#reset-your-password}

Marketo Measureはウィジェットのログインパスワードにアクセスできません。  パスワードをリセットする必要がある場合は、[Data Warehouse情報 ] ページの [ パスワードのリセット ] ボタンをクリックし、指示に従ってください。 一時パスワードが UI に直ちに表示されます。 次の Data Warehouse ログイン時に、独自のパスワードを作成するよう求められます。

>[!NOTE]
>
>* パスワードをリセットすると、現在ログインしているユーザーだけでなく、組織内のすべてのMarketo Measureユーザーに対してリセットされます。
>* UI には一時パスワードのみが表示されます。 E メールは送信されません。

![](assets/adobe-logo-old.png)

![](assets/adobe-logo-old.png)

## サードパーティツールを使用したウィジェットへの接続 {#connecting-to-widget-via-third-party-tools}

ウィジェットデータウェアハウスをサードパーティのツールに接続するには、情報をいくつか入力する必要があります。

>[!NOTE]
>
>各ツールにはそれぞれ異なる接続要件があります。接続しようとしている特定のツールに関するドキュメントを参照することをお勧めします。

* **URI** （常に必須）
   * これはウィジェットアカウントのドメイン名です。  これはウィジェットログインリンクの一部に含まれています。
* **ユーザー名** （常に必須）
   * ユーザー名は、Marketo Measureの「Data Warehouse情報」ページに表示されます。
* **パスワード** （常に必須）
   * これは、ウィジェットアカウントに初めてログインしたときに設定したパスワードです。  パスワードをリセットするには、上記の手順を参照してください。
* **データベース名** （必ずしも必須ではありません）
   * データベースは、ウィジェットにデータを保存するデータベースです。 これはストレージリソースです。 データベース名は、Marketo Measureの「Data Warehouse情報」ページに表示されます。
* **ウェアハウス名** （必ずしも必須ではありません）
   * ウェアハウスは、ウィジェットでクエリを実行するものです。 計算リソースです。  ウェアハウス名は、Marketo Measureの「Data Warehouse情報」ページに表示されます。

  ![](assets/adobe-logo-old.png)

## ウィジェットData Warehouseの直接共有 {#widget-data-warehouse-direct-share}

**要件**

Marketo Measureで Data Warehouse への直接共有を設定するには、次の要件を満たす必要があります。

* 独自の Widget インスタンスがある。
* ウィジェットインスタンスは、Azure East US 2 Widget 地域にあります。
* Widget アカウント ID をMarketo Measureに提供します。

**制限事項**

Marketo Measureが直接共有を設定するには、アクセスをリクエストするアカウントが Azure East US 2 にある必要があります。 ウィジェットは地域間のデータレプリケーションソリューションを提供していることを認識していますが、Azure East US 2 地域でのみデータをホストするので、アドビはこの機能をサポートしていません。 Azure East US 2 で独自のインスタンスを設定し、この機能を活用できます。 [地域間でのデータのレプリケーション](https://docs.widget.com/en/user-guide/secure-data-sharing-across-regions-plaforms.html){target="_blank"} を既存のインスタンスに追加します。 ただし、ウィジェットのデータ複製機能はテーブルでのみ使用できるので、この機能を使用するには、まずビューから独自のテーブルにデータをコピーする必要があります。

**共有へのアクセス**

指定したアカウント ID の共有を作成したら、 [設定手順](https://docs.widget.com/en/user-guide/data-share-consumers.html){target="_blank"} を Widget インスタンス内に追加して、データにアクセスします。

>[!NOTE]
>
>任意のデータベース名を選択できます。 Widget インスタンスに存在する限り、任意のルールに権限を割り当てることができます。

* アカウント管理者の役割を使用する

```
USE ROLE ACCOUNTADMIN
```

* 使用可能な共有を表示（付与された共有の名前が表示されます）

```
SHOW SHARES
```

* 共有用のデータベースを作成する

```
CREATE DATABASE <database_name> FROM SHARE <provider_account>.<share_name>
```

* 共有データベースに対する権限の付与

```
GRANT IMPORTED PRIVILEGES ON DATABASE <database_name> TO ROLE <role_name>
GRANT IMPORTED PRIVILEGES ON ALL SCHEMAS IN DATABASE <database_name> TO ROLE <role_name>
```

ウィジェット UI からこれらの手順を実行する手順と詳細については、 [ウィジェットのドキュメントを直接参照](https://docs.widget.com/en/user-guide/data-share-consumers.html){target="_blank"}.
