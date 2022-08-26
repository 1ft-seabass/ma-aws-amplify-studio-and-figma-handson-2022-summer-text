# Amplify Studio の設定

![image](https://i.gyazo.com/6f3713ebb10fe3d725dc8a56398110ab.png)

Amplify Studio 側から Figma で Amplify UI テンプレートを元に Figma ファイルを作成します。また、Amplify Studio 側で Figma のデザインにデータが入れられるように Data （データの入れ物）を作成します。

Amplify Studio の設定を進めます。

## 別のタブで Figma にログイン

![image](https://i.gyazo.com/a7824e2fcbc836a4f8cbd510e6d8bb92.png)

ブラウザで別のタブを開きます。

![image](https://i.gyazo.com/7f6371ba74ad93065884809a2477873f.png)

右上の Login ボタンをクリックして、ログインします。

（UI Kit のコピー時にログインすると、ダッシュボードにもどって分かりにくくなるので、先にログインしてます。）

## Figma の言語設定が English かどうかを確認

[Figmaが日本版をリリース、英語以外の言語へのローカライズは初 | gihyo.jp](https://gihyo.jp/article/2022/07/figma220727)

最近、日本語もサポートされましたが、まだまだ文献が少なく、つまづいたときに解決しにくく、進めにくいところがあります。

![image](https://i.gyazo.com/58979aff0be4921eb350d4b3bcb5a66d.png)

今回が右上の言語設定から English を選択して英語で設定します。

## Data の設定

ブラウザで Amplify Studio のタブに戻ります。

![image](https://i.gyazo.com/56050a7f1df77b4d152a692210bd6c9c.png)

左のメニューから Data をクリックします。たまに Loading のままになる場合があるので、そのときはリロードします。

![image](https://i.gyazo.com/27987a8032239562df3e2f31280016d3.png)

今回の仕組みでは、すでにデータができています。（Git リポジトリで事前に設定されています。）

右上の Save and Deploy ボタンをクリックして設定を確定します。

![image](https://i.gyazo.com/2d0e712f7e832893ab74ce7a83a86bce.png)

デプロイするか聞かれるので Deploy ボタンをクリックします。

![image](https://i.gyazo.com/2029ef38d3602791267c79322dcf881f.png)

アニメーションしながらデプロイしています。

![image](https://i.gyazo.com/4d4dc865c8cc93d53a9804d80d736cac.png)

下部の Deployment logs をクリックすると開くので、UPDATE_COMPLETE になりまで待ちます。

## UI Library

![image](https://i.gyazo.com/d9c74635961e3ef9e374e2ed7bb63d76.png)

左のメニューから UI Library をクリックします。

![image](https://i.gyazo.com/d94ed8b58650bb6d82b5452563c2ada7.png)

Get started ボタンをクリックします。

![image](https://i.gyazo.com/e76447620321ce39787f55ca9d148bfb.png)

Use our Figma template to get started の Use our Figma template をクリックします。

![image](https://i.gyazo.com/bb57e7230dd536be884a5692f70d9dda.png)

Figma の AWS Amplify UI Kit のページに移動します。

## AWS Amplify UI Kit の取り込み

Get a copy ボタンをクリックします。

![image](https://i.gyazo.com/5747155663755067a29cb071063a66d9.png)

しばらくボタンがローディングでくるくる回って、このように Figma で AWS Amplify UI Kit が読み込まれたプロジェクトが表示されます。

これで Amplify Studio 用の Figma ファイルの準備ができました。設定していきましょう。

## 余談

![image](https://i.gyazo.com/28019e3e8be858cee99a708f5b1eb985.png)

右上の三角ボタンをクリックするとプレゼンテーションぽく再生されて、部品の作り方が表示される仕掛けです。

![image](https://i.gyazo.com/c78fcc631102717ad4b9e642b4217b46.png)

ただし、英語です。

## トラブルシューティング : Checking for running deployments のまま進まない 対応1

![image](https://i.gyazo.com/a2c7d615056e9b31377f155acc311d4d.png)

Data のときに Checking for running deployments の場合は待ちます。

- /amplify-homes-handson-sample-202208/amplify/backend/api/amplifyhomes/schema.graphql ファイルを開きます
- 1行だけ改行を増やして保存して amplify push します
- ? Do you want to update code for your updated GraphQL API
  - Yes
- ? Do you want to generate GraphQL statements (queries, mutations and subscription) based on your schema types?
This will overwrite your current graphql queries, mutations and subscriptions
  - Yes
- Deploy が終わったらもう一度 Amplify Studio を見に行く
- Data で Deploy 出来るはずです

## トラブルシューティング : Checking for running deployments のまま進まない 対応2

それでも進まない場合は、環境を作り直しますが、解決する確証がなく、あまりおすすめしないので、対応1で解消されることを祈っております。

- Cloud9 にもどります。
- amplify-homes-handson-sample-202208 フォルダに移動します
- amplify delete コマンドで今回の環境削除します
- ファイルツリーから amplify-homes-handson-sample-202208 フォルダを削除します
- 再度 Amplify ベースから作り直します。

参考

- Amplify studio data save and deploy is loading for ever · Issue #440 · aws-amplify/amplify-adminui
  - https://github.com/aws-amplify/amplify-adminui/issues/440
- UI - parse error blocks functions · Issue #431 · aws-amplify/amplify-adminui
  - https://github.com/aws-amplify/amplify-adminui/issues/431


