# Git個人運用  
個人開発時の手順を記載  
※現職場ではSVNでのバージョン管理である  
※チーム開発を意識する  

## 手順
  
1. GitHub上のリポジトリからローカルにcloneする  
```
$git clone [URL]
```  

2. 開発ブランチを作成  
※個人開発では*develop*で統一  
```
$git checkout -b develop
```  
  
3. 開発  
```
$git add .
$git commit -m 'メッセージ(コミットメッセージのフォーマットに従う)'
```  
  
4. ローカルからリモートへ
```
$git pull origin master
$git push origin develop
```  
  
5. GitHub  
GitHub上でpull request   
GitHub上でmerge    
  
6. ローカルのmasterブランチを最新化
```
$git checkout master
$git pull origin master
```  
  
7. 不要になったローカルの開発ブランチ(develop)を削除する  
```
git branch --delete develop
```
マージしたかにどうかに関わらず強制的に削除   
```
git branch -D dev
```  

# コミットメッセージのフォーマット
[Prefix] チケット番号 要約  
空行  
変更した理由の詳細  

-例
[Fix] refs #01 ○○の不具合の修正

- [Fix]　修正（ミス・バグ）
- [Add]　追加（ファイル・機能）
- [Remove]　削除（コード・ファイル）
- [Change]　仕様変更（コード・ファイル）
- [Update]　修正・改善（Fixではない場合）
- [Upgrade]　更新（パッケージ・ドキュメント）
- [Revert]　変更取り消し  
  
- [Study]  
※ 個人学習用 教材名番号記載  