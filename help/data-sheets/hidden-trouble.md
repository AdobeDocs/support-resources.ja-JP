---
title: 非表示のトラブルシューティング
description: 隠されたトラブル
type: Troubleshooting
hide: true
hidefromtoc: true
exl-id: dfb54d2d-e4f4-420f-8e91-f1aba704cb31
source-git-commit: a9acc52cf5469ffeb9711ac6f4b52d54bb99086f
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 6%

---

# 非表示のトラブルシューティング

このページに適用される `type: Troubleshooting` はありません。 左ナビゲーションはありますか？

## コードテーブル

**テーブルの外側**

```json
PrimaryIdentities [
  {"id": "ccid-2", "namespace": "CCID"},
  {"id": "ecid-1", "namespace": "ECID"},
  {"id": "ecid-2", "namespace": "ECID"}
  ]
NonPrimaryIdentities [
  {"id": "ccid-1", "namespace": "CCID"},
  {"id": "ecid-3", "namespace": "ECID"}
  ]
  "id": "ccid-1",
    "namespace": "CCID"
```

**表内のストレートコード**

<table>
    <tr>
      <th>並べ替えられた ID リスト</th>
      <th>選択した ID</th>
    </tr>
    <tr>
      <td><code>PrimaryIdentities [<br/>&nbsp;&nbsp;{"id": "ccid-2", "namespace": "CCID"},<br/>&nbsp;&nbsp;{"id": "ecid-1", "namespace": "ECID"},<br/>&nbsp;&nbsp;{"id": "ecid-2", "namespace": "ECID"}<br/>&nbsp;]<br/>&nbsp;NonPrimaryIdentities [<br/>&nbsp;&nbsp;{"id": "ccid-1", "namespace": "CCID"},<br/>&nbsp;&nbsp;{"id": "ecid-3", "namespace": "ECID"}<br/>]</code> </td>
      <td><code>"id": "ccid-1",<br/>&nbsp;"namespace": "CCID"</code> </td>
    </tr>
  </table>

**テーブルでの前読みコードの使用**

<table>
    <tr>
      <th>並べ替えられた ID リスト</th>
      <th>選択した ID</th>
    </tr>
    <tr>
      <td><pre lang="json"><code>PrimaryIdentities [<br/>&nbsp;&nbsp;{"id": "ccid-2", "namespace": "CCID"},<br/>&nbsp;&nbsp;{"id": "ecid-1", "namespace": "ECID"},<br/>&nbsp;&nbsp;{"id": "ecid-2", "namespace": "ECID"}<br/>&nbsp;]<br/>&nbsp;NonPrimaryIdentities [<br/>&nbsp;&nbsp;{"id": "ccid-1", "namespace": "CCID"},<br/>&nbsp;&nbsp;{"id": "ecid-3", "namespace": "ECID"}<br/>]</pre></code> </td>
      <td><pre lang="json"><code>"id": "ccid-1",<br/>&nbsp;"namespace": "CCID"</pre></code> </td>
    </tr>
  </table>

## 新しいタブを含むディープリンク

ここをクリック：[ 新しいタブで開く記事への相対リンク ](hidden/bug-fixes.md#test-for-autoactivate){target=_blank}

```
Click here: [Relative link to article open in new tab](hidden/bug-fixes.md#test-for-autoactivate){target=_blank}
```
