# React の準備と Amplify デプロイ

さきほどの Figma のコンポーネントを React に準備して Amplify デプロイを行います。

![image](https://i.gyazo.com/c7f10c1770ec6d51680c999f837c2557.png)

こちらの手順を進めていきます。

![image](https://i.gyazo.com/fb4e7349d345849648d070b817912711.png)

今回の Cloud9 を開きましょう。

```
cd amplify-homes-handson-sample-202208
```

ターミナルでこちらのコマンドを入力して、React や Amplify の設定した対象のフォルダへ移動します。

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

## Amplify に publish

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