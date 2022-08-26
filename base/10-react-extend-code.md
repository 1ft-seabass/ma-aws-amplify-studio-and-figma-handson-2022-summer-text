# React のコードによる拡張

![image](https://i.gyazo.com/5ea818fa97baf3734abdce39c0c2b523.jpg)

React のコードによる拡張で、コンポーネントにページングと幅変更でコンテンツが調整される仕組みを追加してみます。

## 参考記事

- [UI development (React) - Extend via code - AWS Amplify Docs](https://docs.amplify.aws/console/uibuilder/override/)
    - 英語ですが、このあたりの詳しい拡張が載っています

## src/App.jsの修正

src/App.js を変更します。

```
import './App.css';
import { NewHomes, NavBar, MarketingFooter } from './ui-components'

function App() {
  return (
    <div className="App">
    <NavBar width={"100vw"}/>
    <NewHomes isPaginated itemsPerPage={3}/>
    <MarketingFooter width={"100vw"}/>
    </div>
  );
}

export default App;
```

こちらのソースコードに差し替えます。

具体的には、元のソースから以下を行っています。

- NavBar や MarketingFooter が横幅に合うように `width={"100vw"}` を追加
- NewHomes にページング機能を追加するために `isPaginated itemsPerPage={3}` を追加

Amplify に publish

```js
amplify publish
```

こちらのコマンドで Amplify に反映します。


```
Do you still want to publish the frontend?
```

は、Yesで進みます。

```
✔ Zipping artifacts completed.
✔ Deployment complete!
https://**********.*****************.amplifyapp.com
```

と出れば反映成功です。

## 表示確認

ターミナルでデプロイされた URL を Open で開きます。

![image](https://i.gyazo.com/5ea818fa97baf3734abdce39c0c2b523.jpg)

ページングと幅変更でコンテンツが調整される表示が確認できるはずです！

React のコードによる拡張、これでひとまずの流れはできました。

最後に環境の削除方法を学びましょう。