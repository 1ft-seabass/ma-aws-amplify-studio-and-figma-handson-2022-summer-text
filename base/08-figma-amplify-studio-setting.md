# Figma と Amplify Studio の連携

Figma と Amplify Studio の連携を進めます。

## Figma から Amplify へ設定の Share

![image](https://i.gyazo.com/80de300c1294e49ee645063374fdc756.jpg)

まず、現在開いている Figma ファイルの URL をブラウザのアドレスバーからコピーします。

![image](https://i.gyazo.com/c9344523e9cbb279187222c204482445.png)

Amplify の画面に戻ります。

![image](https://i.gyazo.com/478ecfe7b10d5b253b4383264f473b1e.png)

Paste your Figma file link に注目します。

![image](https://i.gyazo.com/70875b5e15370f5aa988fbe8c527e6d7.png)

こちらに、さきほどの Figma ファイルの URLをコピーアンドペーストして、Continue ボタンをクリックします。

![image](https://i.gyazo.com/84cec8ff5599ec4ac177569e2e07d8a6.png)

AWS と Figma の連携初回は、Amplify Atudio 側から Figma 側にアクセス許可が聞かれるので Allow access ボタンをクリックします。

![image](https://i.gyazo.com/70df26122c027990ba0e8b86140fdfbd.png)

Fetching from Figma と表示されてロードが開始します。

![image](https://i.gyazo.com/b6544a19764ac76d9bb33ac0149fed15.png)

このように Figma theme updates と出てきたら成功です。

![image](https://i.gyazo.com/06ffb828df72babe333841a1e5b73a0e.png)

Skip theme updates ボタンをクリックします。

## コンポーネントの受け入れ

コンポーネントは HomeCard ・ NavBar ・ MarketingFooter だけ受け入れます。ほかは Reject or Skip します。

![image](https://i.gyazo.com/b1884b94d49efad74c51db9b67da59d0.png)

すると HomeCard のコンポーネントの許可ページに移動するので Accept ボタンをクリックして受け入れます。

![image](https://i.gyazo.com/7e78de5a20a37a8d88e026325af9b460.png)

MarketingFooter も Accept ボタンをクリックして受け入れます。

![image](https://i.gyazo.com/ef86a5dadc445a46cf64ca0c6d7e1446.png)

NavBar も Accept ボタンをクリックして受け入れます。

![image](https://i.gyazo.com/e51076484dd30cca6099346af8523ecd.png)

コンポーネントの受け入れ設定が終わり Save Components ボタンをクリックします。

![image](https://i.gyazo.com/8d617a6f7f2d23e322e2ec59852d23d7.png)

取り込みが成功して、UI Library 画面が表示されて Components に HomeCard ・ NavBar ・ MarketingFooter がいます。

### 間違って Accept したものがあれば、あとでも削除できます

間違って Accept したものがあれば、この画面で Delete していきます。

![image](https://i.gyazo.com/db25ddf024977de45ff07eb87629da88.jpg)

とはいえ、削除するものは少ないほうがよいので、なるべく Reject or Skip で対応しておきましょう。

## Content

![image](https://i.gyazo.com/7d5c00fd904a8f111422886131cc8c47.png)

左メニューで Content をクリックします。

![image](https://i.gyazo.com/8c8c2c86d712d9a880d0b1f4cf4cd252.png)

### Auto-generate seed data

Content ページでしばらくロードを待っていると Auto-generate seed data ボタンが出てくるのでクリックします。

ロードの間は、Amplify 上のデータモデルを調べています。

![image](https://i.gyazo.com/265bc78544c2a75fabe8b7e1eaeaab3a.png)

自動生成するデータを 5 つ作成するので、How many rows of data do you want to generate? (1-100) のところを 5 として Generate data ボタンをクリックします。

![image](https://i.gyazo.com/5c5331fd07bd4541d5d80a49eef9845b.png)

データが自動作成されます。

### image_url を画像 URL に置き換える

データが自動作成されましたが image_url は画像 URL でないと動きません。image_url を画像 URL に置き換えます。

![image](https://i.gyazo.com/47ad33564efc095868facd27952b8d9b.png)

編集したい行をクリックします。

![image](https://i.gyazo.com/982de3dfec85d4d11488663cb1009299.png)

各行のデータ内容を編集します。今回は image_url を以下のサンプル画像 URL と入れ替えて、Save Home をクリックします。

### figma_test_image01.jpg

![figma_test_image01](https://raw.githubusercontent.com/1ft-seabass/ma-aws-amplify-studio-and-figma-handson-2022-summer-text/master/base/images/figma_test_image01.jpg)

https://raw.githubusercontent.com/1ft-seabass/ma-aws-amplify-studio-and-figma-handson-2022-summer-text/master/base/images/figma_test_image01.jpg

### figma_test_image01.jpg

![figma_test_image02](https://raw.githubusercontent.com/1ft-seabass/ma-aws-amplify-studio-and-figma-handson-2022-summer-text/master/base/images/figma_test_image02.jpg)

https://raw.githubusercontent.com/1ft-seabass/ma-aws-amplify-studio-and-figma-handson-2022-summer-text/master/base/images/figma_test_image02.jpg

### figma_test_image03.jpg

![figma_test_image01](https://raw.githubusercontent.com/1ft-seabass/ma-aws-amplify-studio-and-figma-handson-2022-summer-text/master/base/images/figma_test_image03.jpg)

https://raw.githubusercontent.com/1ft-seabass/ma-aws-amplify-studio-and-figma-handson-2022-summer-text/master/base/images/figma_test_image03.jpg

### figma_test_image04.jpg

![figma_test_image01](https://raw.githubusercontent.com/1ft-seabass/ma-aws-amplify-studio-and-figma-handson-2022-summer-text/master/base/images/figma_test_image04.jpg)

https://raw.githubusercontent.com/1ft-seabass/ma-aws-amplify-studio-and-figma-handson-2022-summer-text/master/base/images/figma_test_image04.jpg

### figma_test_image05.jpg

![figma_test_image05](https://raw.githubusercontent.com/1ft-seabass/ma-aws-amplify-studio-and-figma-handson-2022-summer-text/master/base/images/figma_test_image05.jpg)

https://raw.githubusercontent.com/1ft-seabass/ma-aws-amplify-studio-and-figma-handson-2022-summer-text/master/base/images/figma_test_image05.jpg

このように変更できていれば OK です。

![image](https://i.gyazo.com/29efe86cae70f7ad80f55f5ecd715767.png)

## UI コンポーネントと Content のデータを紐付ける

![image](https://i.gyazo.com/0f4dd5aed675a07f437011dc5f7a40dd.png)

左メニューから UI Library に移動します。

![image](https://i.gyazo.com/8efbdf99b992a28f40df91844c41c173.png)

Components から HomeCard をクリックして、HomeCard が表示されたら Configure ボタンをクリックします。

![image](https://i.gyazo.com/a85a46c7dea5e0fd6ccc8c5f683ab228.png)

HomeCard の設定が表示されました。

![image](https://i.gyazo.com/7d8afc925b588a36621bd14f209fce61.png)

Components properties のところにある Add prop をクリックします。

![image](https://i.gyazo.com/34139f72417f3c9e70f348246a920180.png)

- Name
    - home
- Type
    - Home

と設定します。

![image](https://i.gyazo.com/91d096f74e6bca4678a2449e373c8b68.png)

Elements tree で image をクリックします。

![image](https://i.gyazo.com/ca5ba5e6b7ee7d1aac185d48b0681391.png)

image を選択した状態で Child properties 項目で Set prop をクリックします。

![image](https://i.gyazo.com/ce0921f218f42d6b06c665ccc1c15a16.png)

内容は、

- Prop
    - src
- Value
    - home.image_url

と設定します。

つづいて Title を選択した状態で Set prop をクリックします。

![image](https://i.gyazo.com/ea35ff274ebe2dbc93d2a3402ce3be1d.png)

内容は、

- Prop
    - label
- Value
    - home.address

と設定します。

つづいて Description を選択した状態で Set prop をクリックします。

![image](https://i.gyazo.com/90732d5d289b0af11ee78096070b1704.png)

内容は、

- Prop
    - label
- Value
    - home.price

と設定します。

## コンポーネントをデータに応じて並べる NewHomes コレクションを作成する

![image](https://i.gyazo.com/8c85646974d193c805cb32303881987f.png)

右上にある Create collection をクリックします。

![image](https://i.gyazo.com/3521db5e1942e247390930a55345a6f0.png)

コレクションの名前を NewHomes にして、Create ボタンをクリックします。

![image](https://i.gyazo.com/00b638c562267e89134e2ca26ca739f5.png)

あたらしく NewHomes が作成されて先ほど Content で設定したデータがプレビューとして反映されています。

## コレクションのレイアウトの編集

![image](https://i.gyazo.com/32d46aef7ba06288e2f159ab3d0c1255.png)

 NewHomes を選択した状態で Configure をクリックして編集画面に移動します。

![image](https://i.gyazo.com/632e07c75b8bab1eec3f15f30dbfd08b.png)

Layout の Type を Grid に変更します。

![image](https://i.gyazo.com/69d9b46363014759bbad64cd9e624a38.png)

上下左右の余白を示す、こちらのエリアで各設定を 10 px にします。（これは上部の余白を設定する例です）

![image](https://i.gyazo.com/eddb1b4d7bcafc6df7c2c2ce8b8cdfed.png)

上下左右ともに 10 px に設定した状態です。

### レイアウトが崩れたら再度作り直します

![image](https://i.gyazo.com/919851d96cbc98b32aa9c3ff455782c9.png)

レイアウトの編集中にレイアウトが崩れてしまったら再度作り直しましょう。

![image](https://i.gyazo.com/5fa73e555c180ea686921372bd76b91d.png)

UI Library をクリックして編集画面から戻ります。

![image](https://i.gyazo.com/0b5af0806dbee49fffef5ab15d8d71ed.png)

 NewHomes を選択した状態で Delete ボタンをクリックします。

削除できたら「コンポーネントをデータに応じて並べる NewHomes コレクションを作成する」から再開します。

それでもうまく作られないときは、Grid 変更だけ行います。一度 React 反映後に余白調整します。

## コンポーネントコードの取得

![image](https://i.gyazo.com/1cb9f35fc517e26ddc4156bc59f728b3.png)

Get component code ボタンをクリックします。

![image](https://i.gyazo.com/c7f10c1770ec6d51680c999f837c2557.png)

NewHomes コンポーネントを Cloud9 に準備した React ソースコードに割り当てる手順が書いてあるので、この画面のまま、次の手順に進みます。

はじめての React の準備と Amplify デプロイがうまくいきました。では少し、次の章で内容を変更してみましょう。