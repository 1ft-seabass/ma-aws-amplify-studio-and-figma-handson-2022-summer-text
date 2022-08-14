# Figma の準備

Figma で Amplify からデータを入れるひな形をつくります。

## ズームの調整

今後の作業をしやすいようにズームを調整します。

![image](https://i.gyazo.com/48f778e041148b9367d7374faf2e568a.png)

Ctrl + マウススクロール で、デフォルトで入っている Frame 群がこれくらいの大きさで収まるように、調整します。

![image](https://i.gyazo.com/a0aa7db72840a479c764eedef8b904c6.png)

右上のズーム設定をクリックして 25 % くらいに設定しても良いでしょう。

## Frame の作成と調整

![image](https://i.gyazo.com/c6fc729932010da1f330154508966ca4.png)

ヘッダーの＃ボタンをクリックし Frame になっているかを確認します。

![image](https://i.gyazo.com/df1dfcdc3d07ff70dccf11bf0afb5b6a.png)

画面上の空いているスペースにクリックして 100 x 100 の大きさの Frame をつくります。

この Frame をクリックして選択した状態にします。通常、作成した瞬間は選択されています。

![image](https://i.gyazo.com/829981d84b88e7bab456731756b70644.png)

右側の Design 設定の画面で Frame の項目の W 100 H 100 となっているところを注目します。

![image](https://i.gyazo.com/4e48a5bd26c4f5ab894463b9a23219ac.png)

100 の値をクリックすると編集できるので W 300 H 200 と設定します。

![image](https://i.gyazo.com/1af3b81d13232cc3a53fb55d1156db23.png)

Frame の見た目も 300 x 200 に大きさが反映されました。

## Zoom to selection 

![image](https://i.gyazo.com/91aa004963c01eed84b557a8575c3c68.png)

このあと Frame 内の作業をするので Frame を選択した状態で Shift + 2 をするか、右上のメニューから View > Zoom to selection して Frame に対してズームします。

![image](https://i.gyazo.com/0b44ae6c881b31e794025e9aeddbc149.png)

このようにズームされます。

## Image の作成と調整

![image](https://i.gyazo.com/e648d2086f38867104cd172e8ebef1bf.jpg)

今回使う画像です。こちらの画像を Chrome ブラウザで右クリックして `画像をコピー` を行っておきます。クリップボードに画像が記録されました。

![image](https://i.gyazo.com/e3759d827c63470b76a3321e9fb5b6d4.png)

Frame 外のこのあたりを右クリックして Paste here をクリックします。

![image](https://i.gyazo.com/3392263f8a681048a241ba9350b699e5.png)

初回ですとクリップボードからのデータのペーストは許可が必要なので許可しましょう。

![image](https://i.gyazo.com/ebb557f3dc7d0ccc6d9fca0ded135dd0.png)

初回許可した時に、ペーストが不発になる場合があります。

![image](https://i.gyazo.com/807c4d8ba8e1b6768ee40ddd9d6d62bd.png)

そのときはブラウザをリロードして、

![image](https://i.gyazo.com/1af3b81d13232cc3a53fb55d1156db23.png)

今回の Frame を選択したあと、再度 Shift + 2 で Frame にズームします。

![image](https://i.gyazo.com/e3759d827c63470b76a3321e9fb5b6d4.png)

もう一度 Frame 外のこのあたりを右クリックして Paste here をクリックします。

![image](https://i.gyazo.com/77e90ca5a63b9c0fb755880ee78c44d5.jpg)

このようにペーストされれば OK です。

![image](https://i.gyazo.com/1c512635464f622fbe8150e1a9899789.jpg)

画像をクリックして選択し、マウスで動かして、Frame の左上に持っていくと吸着するのでマウスを離して配置します。

## Text の作成と調整

### Title

![image](https://i.gyazo.com/39451ea4478ecad1adcc218d722a3236.png)

ヘッダーの T ボタンをクリックします。

![image](https://i.gyazo.com/dbb749cac287b24e676ae74f308e9634.jpg)

画像の左下からマウスをドラッグして 300 x 50 になるまで引っ張ってマウスを離します。

![image](https://i.gyazo.com/7c90020866ca108ccede2bedf3e2e1dd.jpg)

入力を半角英数モードにして Title と入力して Frame 外をクリックして入力を終わります。

![image](https://i.gyazo.com/3a1fd1d6aab65626e414b461f0dea759.jpg)

このように Text オブジェクトが Title をいう文字が入力されて 300 x 50 の大きさで画像のすぐ下に密着した形で配置していれば OK です。

### Description

![image](https://i.gyazo.com/e5c74cfa8e89d30bdda5b5582ee318d7.jpg)

同じ操作で、Title の下に Description という Text オブジェクトを作成します。

コツとしては、最初の作成時には Title 直下に密着するかは気にせずに、まず 300 x 50 の大きさで Description のオブジェクトを作った後に、吸着機能を利用して、再度マウスで移動して Title の下に密着配置させるのがよいでしょう。

## コンポーネント化

Image ・ Title ・ Description をまとめてコンポーネント化します。

![image](https://i.gyazo.com/74c176055144054cc0fefb37ea4edd79.jpg)

Shift キーを押しながら Image ・ Title ・ Description をクリックして複数選択します。左側のレイヤーでも Image ・ Title ・ Description が選択させていることを確認しましょう。

![image](https://i.gyazo.com/05739bccf237703a418e7af378b7ba55.jpg)

選択した 3 オブジェクトの上で右クリックをして Create component クリックします。

![image](https://i.gyazo.com/5ce8979a8a021a029cdc3b754bdc4b71.jpg)

コンポーネントになりました。

## コンポーネントの名前を HomeCard にする

![image](https://i.gyazo.com/bd337e24d809395e3f2d78f6781e704f.jpg)

コンポーネントの名前を示す右上テキストはダブルクリックで編集できます。

![image](https://i.gyazo.com/3c6539ea55d1a9fe159a0d1016d43f8d.jpg)

ダブルクリックして編集状態にします。

![image](https://i.gyazo.com/3dfc02a40add4f9648333995bf390171.png)

入力を半角英数入力にして `HomeCard` と入力して Enter キーを押します。

![image](https://i.gyazo.com/56138a4297948eba99c630998b52fc09.jpg)

右上のコンポーネント名が変更出来たことと、Layers の部分でもちゃんと変更できているか確認しましょう。

