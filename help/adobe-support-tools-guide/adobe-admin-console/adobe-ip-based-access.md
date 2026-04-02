---
title: IP アドレスによる製品アクセスの制限
description: IP ベースのアクセス権を使用して、Adobe製品へのユーザーアクセスを制御し、承認済みのパブリック IP範囲に使用を制限できます。
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: 879a936ea110084c03df6003494f88831561d3c2
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 1%

---


# IP アドレスによる製品アクセスの制限

エンタープライズ版に適用されます。

IP ベースのアクセス権を使用して、ユーザーによるAdobe製品へのアクセスを制御し、リストにないパブリック IP アドレスからの不正使用を防ぎます。

[Admin Console](https://adminconsole.adobe.com/settings/identity)に移動して、信頼できるパブリック IP アドレスを&#x200B;**IP ベースのアクセス**&#x200B;に追加し、Adobe アプリとサービスを安全に利用できるようにします。

## IP ベースのアクセスの利点

IP ベースのアクセス制御では、IP アドレスのAdobeを使用して、ランダムなパブリック IP アドレスからの許可リストに加える製品の使用を制限します。 IP ベースのアクセスは、Adobe Admin Console内のすべてのディレクトリと関連する製品に適用されます。

信頼できるパブリック IPを&#x200B;**許可IP アドレス** リストに追加すると、ユーザーを次の場所から停止できます。

- 許可されたIP範囲外のパブリック IPからの製品へのアクセス
- 許可されたIP範囲外のパブリック IPからAdobe [&#x200B; ユーザープロファイル &#x200B;](https://helpx.adobe.com/jp/enterprise/using/manage-adobe-profiles.html)にログインします
- 許可されたIP範囲外のweb アプリでのユーザープロファイルの切り替え

  ![組織構造の書き出し](./assets/ip-based-access.avif)

## IP ベースのアクセスを有効にする

### 重要な検討事項

>[ !I重要な考慮事項]
>
>- 管理者は、自分のパブリック IP アドレスを追加してから、他のIP範囲を追加する必要があります。 エラーが発生する可能性があります。
>- IP ベースのアクセスは、プライベート IP アドレスには適用されません。

CIDR形式でのみ、最大150の異なるパブリック IP範囲を追加できます。

Adobe Admin ConsoleでIP ベースのアクセスを有効にするには、次の手順に従います。

1. **[[!UICONTROL Adobe Admin Console Settings]](https://adminconsole.adobe.com/settings/identity)** セクションに移動します。
2. 選択メニューで「**[!UICONTROL プライバシーとセキュリティ]**」を選択して展開し、次に「**[!UICONTROL 認証設定]**」を選択します。
3. 「**[!UICONTROL IP ベースのアクセス]**」セクションで、「**[!UICONTROL IP アドレスを追加]**」ボタンを選択します。
4. **[!UICONTROL IP アドレスを追加]** ウィンドウで：
   - パブリック IP アドレスまたはCIDR ブロックを入力して、このアドレスを契約許可リストに追加します。
   - コンマを使用して複数のIP アドレスを区切ります。
   - 「**[!UICONTROL 保存]**」を選択します。

   現在はIPv4形式のみをサポートしています。 以下に、いくつかの例を示します。
   - IP v4 アドレス：1.3.4.6
   - IP v4 サブネット アドレス：1.2.0.0/24

IP アドレスは数分以内に追加されます。 関連するユーザーは、次回ログインするか、許可されたパブリック IP アドレスの外でプロファイルを切り替えようとするときに、制限が表示されます。 この変更の前に、ユーザーに通知することをお勧めします。

各エントリの横にある「編集」または「削除」オプションを選択すると、リストされているIP アドレスを編集または削除できます。

>[!NOTE]
>
>- IP ベースのアクセスが有効になっている場合、**強制ログアウトは発生しません**。 ユーザーが影響を受けるのは、webでログインまたはプロファイルを切り替える際に、制限されたプロファイルを選択しようとしたときだけです。
>- セキュリティで保護されたweb ゲートウェイを使用している場合は、すべてのトラフィックがそのゲートウェイを通じてルーティングされていることを確認します。 Adobe アプリとサービスが正しく機能するために許可されるドメインの[&#x200B; リスト &#x200B;](https://helpx.adobe.com/jp/enterprise/kb/network-endpoints.html)を表示します。
>- 無効なIP アドレスを入力したためにAdmin Consoleからロックされている場合は、[Adobe カスタマーケア &#x200B;](https://helpx.adobe.com/jp/enterprise/using/support-for-enterprise.html)にお問い合わせください。

## 会話に参加

共同作業、質問、他の管理者とのチャットを行うには、[&#x200B; エンタープライズ版およびグループ版コミュニティ &#x200B;](https://www.adobe.com/go/entcom_jp)にアクセスしてください。
