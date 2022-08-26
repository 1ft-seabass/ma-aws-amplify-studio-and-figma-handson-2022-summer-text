# React の準備と Amplify デプロイ

さきほどの Figma のコンポーネントを React に準備して Amplify デプロイを行います。

![image](https://i.gyazo.com/c7f10c1770ec6d51680c999f837c2557.png)

こちらの手順を進めていきます。

## Cloud9 で作業

![image](https://i.gyazo.com/1eb071e98cf07c07678c6ab076eded13.png)

AWS コンソールの上部から Cloud9 を検索して呼び出しましょう。

![image](https://i.gyazo.com/73853d74f3041c9fd800d9c17addf619.png)

一覧から、今回の Cloud9 を選択して Open IDE ボタンをクリックします。

![image](https://i.gyazo.com/fb4e7349d345849648d070b817912711.png)

今回の Cloud9 を開きました。先ほど作業していたものがちゃんとあるはずです。

## ターミナルでフォルダの移動

![image](https://i.gyazo.com/2ba05cd3815d6018fd960cdbe74b7542.png)

Cloud9 に入った時にターミナルでの狙っているフォルダが作業フォルダになっていない場合は移動します。

```
cd amplify-homes-handson-sample-202208
```

ターミナルでこちらのコマンドを入力して、React や Amplify の設定した対象のフォルダへ移動します。

（対応してもらう前に、状況聞いてみる）

![image](https://i.gyazo.com/17f5f190cdb7486383a771b72b97c73f.png)

あらためて、作業フォルダが `~/environment/amplify-homes-handson-sample-202208` 担っているか確認して進めましょう。違う場所の場合、次の amplify pull でエラーやアラートが出ます。

## amplify pull コマンドをクリップボードにコピー

![image](https://i.gyazo.com/c7f10c1770ec6d51680c999f837c2557.png)

NewHomes コンポーネントを Cloud9 に準備した React ソースコードに割り当てる手順が書いてあるので 1. に書いてあるコマンドを、右側にあるコピーボタンでコピーします。

## src/App.jsの修正

![image](https://i.gyazo.com/fc5eb744994cc609ad766563f80fd976.png)

src/App.js を変更します。

```js
import './App.css';
import { NewHomes, NavBar, MarketingFooter } from './ui-components'

function App() {
  return (
    <div className="App">
    <NavBar />
    <NewHomes />
    <MarketingFooter />
    </div>
  );
}

export default App;
```

こちらのソースコードに差し替えます。

具体的には、元のソースから以下を行っています。

- `import { NewHomes, NavBar, MarketingFooter } from './ui-components'` という今回使うコンポーネントが呼び出されたり
- `<NavBar />` `<NewHomes />` `<MarketingFooter />` が表示部分 App に配置されています。

## Amplify に publish

この変更を、いよいよ Amplify のホストに反映してみましょう。

```
amplify publish
```

こちらのコマンドで Amplify に反映します。

```
Do you still want to publish the frontend?
```

は、Yesで進みます。

```
(node:7600) [DEP0148] DeprecationWarning: Use of deprecated folder mapping "./" in the "exports" field module resolution of the package at /home/ec2-user/environment/amplify-homes-handson-sample-202208/node_modules/postcss-safe-parser/node_modules/postcss/package.json.
Update this package.json to use a subpath pattern like "./*".
(Use `node --trace-deprecation ...` to show where the warning was created)
Creating an optimized production build...
```

と途中で止まっているように見えるかもですが、待っていれば OK です。

```
✔ Zipping artifacts completed.
✔ Deployment complete!
https://**********.*****************.amplifyapp.com
```

と出れば反映成功です。

## 表示確認

![image](https://i.gyazo.com/c4644e01f5145afa8e840801b0e12836.png)

ターミナルでデプロイされた URL を Open で開きます。

![image](https://i.gyazo.com/0b24edebd9ac697c24b55c3cca373883.jpg)

このように表示が確認できるはずです！