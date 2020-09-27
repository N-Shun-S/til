# Git個人運用  
個人開発時の手順を記載  
※現職場ではSVNでのバージョン管理である
※チーム開発を意識する

* 手順 *
  
- GitHub上のリポジトリからローカルにcloneする  
`$git clone [URL]`  
  
- 開発ブランチを作成  
※個人開発では*develop*で統一  
`$git checkout -b develop`
  
- 開発  
```
$git add .
$git commit -m 'メッセージ(コミットメッセージのフォーマットに従う)'
```
  
- ローカルからリモートへ
```
$git pull origin master
$git push origin develop
```
  
- GitHub
GitHub上でpull request  
GitHub上でmerge  
  
- ローカルのmasterブランチを最新化
```
$git checkout master
$git pull origin master
```
  
- 不要になったローカルの開発ブランチ(develop)を削除する  
`git branch --delete develop`  
マージしたかにどうかに関わらず強制的に削除  
`git branch -D dev`
