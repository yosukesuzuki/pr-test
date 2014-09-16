pr-test
=======

pull request の実験用

説明すること
# git/githubのメリット
- 分散型のアーキテクチャー
- pull-request型開発
- 他サービスとの連携が可能
  - テスト自動化（circle ciとか）
  - deploy自動化（capistranoとか）

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
## 1. コード変更の際にmasterブランチから新しいブランチを切る
```
# git checkout -b newpr01
```
## 2. 空でコミットする
```
# git commit --allow-empty
```
## 3. 何か変更を加えてコミット
```
# git add 対象のファイル
# git commit -m "コミットのメッセージ"
```
もしくは以下にすると変更した管理下のファイルをすべてコミットできる
```
# git commit -a
```
## 4. push
```
# git push origin newpr01
```
## 5. 新しいpull-requestを作る
githubの画面からpull-requestを出すもしくはhub(brew install hub)コマンドから
```
# hub pull-request
```
## 6. pull-requestにタスクを書く
```
- [ ] スクリーンショットを追加
- [ ] テストコードを書く
```
## 7. コミット→pushの繰り返し
必要であれば、他の開発者とやり取りしながら

## 8. マージする

  
# ドキュメントはどうする？
- wikiとかREADME.mdに書く
- もしくはbacklogとかでファイル管理
