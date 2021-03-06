# Git 個人運用

個人開発時の手順を記載  
※現職場では SVN でのバージョン管理である  
※チーム開発を意識する

## 手順

1. GitHub 上のリポジトリからローカルに clone する

```
$git clone [URL]
```

2. 開発ブランチを作成  
   ※個人開発では*develop*で統一/単語繋げる場合はハイフン（-）

```
$git checkout -b develop
```

3. 開発 Working directory 　 → 　 Staging area 　 → 　 Repository

```
$git add .
$git commit -m 'メッセージ(コミットメッセージのフォーマットに従う)'
```

4. ローカルからリモートへ

```
$git pull origin main
$git push origin develop
```

5. GitHub

GitHub 上で pull request  
GitHub 上で merge

6. ローカルの master ブランチを最新化

```
$git checkout main
$git pull origin main
```

7. 不要になったローカルの開発ブランチ(develop)を削除する

```
$git branch --delete develop
```

マージしたかにどうかに関わらず強制的に削除

```
$git branch -D dev
```

8. その他

現在の状態確認  
※HEAD→ 今いるブランチを指す

```
$git status
```

コミット履歴確認  
※q で終了

```
$git log
```

コミットログの先頭７桁のコミット ID を表示する/コミットログを縦グラフで表示する

```
$git log --oneline
$git log --graph
```

作業のキャンセル  
Staging area に add した作業をキャンセル  
※git status で確認できる

```
$git reset HEAD <filename>
```

Working directory での作業をキャンセル  
※track 済みのファイルのみ可能/注意して行うこと

```
$git checkout --<filename>
```

ファイル名の変更を Git で管理

```
$git mv <filename1> <filename2>
```

or

```
mvコマンド <filename1> <filename2>
$git add -A
```

マージについて  
Fast Forward マージされるブランチの HEAD をマージするブランチの先端にそのまま移動
Automatic merge 各コミットが異なる箇所を変更している場合  
Conflict 各コミットが同じ箇所を変更している → 手動 or ツールで対処

マージする前に差分（diff）を確認する
※compare が新しい変更などした方

```
$git diff <base> <compare>
```

```
$git merge <branchname>
```

# コミットメッセージのフォーマット

[Prefix] チケット番号 要約  
空行  
変更した理由の詳細

-例  
[Fix] refs #01 ○○ の不具合の修正

- [Fix]　修正（ミス・バグ）
- [Add]　追加（ファイル・機能）
- [Remove]　削除（コード・ファイル）
- [Change]　仕様変更（コード・ファイル）
- [Update]　修正・改善（Fix ではない場合）
- [Upgrade]　更新（パッケージ・ドキュメント）
- [Revert]　変更取り消し
- [Study]  
  ※ 個人学習用 教材名番号記載
