# React

Node.js  
JavaScriptをRubyやPythonと同じようにPCのターミナル
上で動かすことができるようにするためのソフトウェア

フロントエンド開発にNode.jsが必要  
npm  
パッケージのインストールと整合性の管理

他にも色々（バンドルなど）これらを実現するためのツールは全てNode.js上で動く

バージョンマネージャーを使ってNode.jsをインストール
※プロジェクトごとに異なるバージョンの環境を共存させるのが必要になる  
今回はこれ　→　nodenv
<BR>
<BR>
# 環境構築
インストール  
anyenv  
nodenv  
node.js  
設定したことで新しくターミナルを立ち上げた時に設定することなく、  
nodeなど実行できる


※ macOS High Sierra バージョン10.13.6  
 ~/.zshrcではなく~/bash_profileに設定

node REPL .exit
<BR>
<BR>
# React

Create React App

React で作られるアプリケーションは、すべて『コンポーネント（Component）』の組み合わせで構成される。コンポーネ
ントというのは、今の段階では『任意の UI を表現するパーツの単位』

Reactではコンポーネントの実装は、関数または、クラスで定義することになっている

JSX...HTMLに見えて実はJavaScript→最終的にJavaScriptにコンパイルされる

___  
***メモ***<BR>
gitignore作成参考<BR>
[gitignore.io](https://www.toptal.com/developers/gitignore)<BR><BR>

任意のディレクトリ配下(プロジェクトフォルダ配下)<BR>

​```
nodenv local <バージョン番号>
​```

バージョン管理に含める

___

<BR>
<BR>

# 参考　　
[macの.bash_profileと.bashrc](https://qiita.com/Yuuki557/items/bda36910605b308122d2)  
[anyenv + macOS環境構築](https://qiita.com/rinpa/items/81766cd6a7b23dea9f3c)  
[PATHを通すについて](https://qiita.com/HANYA/items/1bf072343ef12deeb974)  



