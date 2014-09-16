pr-test
=======

pull request の実験用

説明すること
# git/githubのメリット
- 分散型のアーキテクチャー
- pull-request型開発

# ブランチ構成
- masterブランチ
  - 開発していく上でのメーンのブランチ
  - ここからブランチを切って新しい変更を加える
- deployment/staging
  - ステージングサーバーにあがっているソースコード
  - masterからpull-requestを送ってマージする
- deployment/production
  - 本番サーバーにあがっているコード
  - deployment/stagingからpull-requestを送ってマージする

# pull-request型開発
1. コード変更の際にmasterブランチから新しいブランチを切る
```
git checkout -b newpr01
```
2. 


  
- ドキュメントはどうする？
  - wikiとかREADME.mdに書く
  - もしくはbacklogとかでファイル管理
