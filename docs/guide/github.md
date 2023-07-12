---
sidebar_position: 4
---

# ドキュメント管理について
本ドキュメントサイトはGitHubにて管理しています。

- https://github.com/KoushiKagawa/documentation-system

## ドキュメントの修正依頼について
ドキュメントに間違いがある場合は、issueを作成してください。

- https://github.com/KoushiKagawa/documentation-system/issues/new

## ドキュメントの修正について
### 1.issueをアサインする
issueをアサインします。

### 2. ブランチを作成する
#### ブランチの命名規則

|ブランチ名| 役割| 派生元 | マージ先 |
| --- | --- | --- | --- |
| main | 本番公開用のブランチ。 | - | - |
| feature/XXX | ドキュメント作成用のブランチ。<br/> 'XXX'にはissueのIDを記載してください | main | main |

#### ブランチの作成方法

ブランチを作成します。

```
git branch freature/XXX
```

ブランチが作成されているか確認します。

```
git branch
```

### 3. ブランチチェックアウト

```
git checkout feature/XXX
```

### 4. ファイル作成

```
vi sample.md
```

### 5. ファイルをステージング環境にアップ

#### git add

```
git add sample.md
```
#### git commit

```
git commit -m "コミットメッセージ"
```

#### git push

```
git push -u origin feature/XXX
```

### 6. プルリクエスト作成
GitHubよりプルリクエスト作成

### 7. レビュー
プルリクエストをレビューする。

- MUST:明らかな間違い
- IMO:緩やかな意見。私はこう思うけど
- NIT:軽微な修正
- Q:質問がある場合に利用

問題なければapproveする。


### 8. マージ
GitHubよりマージする。