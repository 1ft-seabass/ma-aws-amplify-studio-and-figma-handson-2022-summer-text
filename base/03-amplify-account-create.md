# Amplify の初期設定

Cloud9 のターミナルで作業を進めます。

Amplify CLI をインストールします。

## Amplify CLI インストール

```
npm install -g @aws-amplify/cli
```

こちらのコマンドを実行して、インストールを待ちます。

## Amplify 初期設定をはじめる

```
amplify configure
```

こちらのコマンドを実行します。

```
Follow these steps to set up access to your AWS account:

Sign in to your AWS administrator account:
https://console.aws.amazon.com/
Press Enter to continue
```

このようなメッセージが出てくるので Enter キーを押します。

### Specify the AWS Region

![image](https://i.gyazo.com/d7403e2a37429e460c42a32bc41a62f3.png)

リージョンは ap-northeast-1 を選択して、Enter キーを押します。

### Specify the username of the new IAM user:

![image](https://i.gyazo.com/62110af7cd533317a1a629765e6bb302.png)

Amplify のための新しい IAM ユーザーの名前を決めます。

これは最初に提案される ランダムの名前（amplify-＜ランダム文字列＞）をそのままで OK です。

Enter キーを押します。

### Complete the user creation using the AWS console

リージョンと IAM ユーザの名前が決まったので、ブラウザ上の AWS コンソールで実際に作成する URL が案内されました。

![image](https://i.gyazo.com/968760e7cc5cae519c53185d46435e41.png)

緑色の URL の部分をクリックしましょう。

![image](https://i.gyazo.com/e36550baf6f4974a36bdd60900e160e5.png)

Open をクリックします。

![image](https://i.gyazo.com/d2be0dfa08d7f81bcab3de08eb31e3af.png)

ブラウザ上の AWS コンソールの IAM に移動します。さきほど決めたIAM ユーザーの名前が設定されています。

## AWS コンソール

![image](https://i.gyazo.com/af7680fbfa2d6a240e52b2bc617bae8c.png)

右下の 次のステップ : アクセス権限 ボタンをクリックします。

![image](https://i.gyazo.com/6e8b6dfc50b49e0c30e58b42f016ab95.png)

AdministratorAccess-Amplify がチェックされていることを確認して、右下の 次のステップ : タグ ボタンをクリックします。

![image](https://i.gyazo.com/a368e189c4c22825018ef29775fcb576.png)

タグの追加項目は何も設定せず、右下の 次のステップ : 確認 ボタンをクリックします。

![image](https://i.gyazo.com/a5326dab0c21713b4f937c491cc4891a.png)

確認画面で、ユーザー名やアクセス権限にAdministratorAccess-Amplifyがあることを確認して、ユーザの作成ボタンをクリックします。

![image](https://i.gyazo.com/6806637dcfdb3cb93267f36d5b4c9c8e.png)

作成成功画面に移動します。

## アクセスキー ID をテキストエディタにメモ

![image](https://i.gyazo.com/09def33c31917a707f288040e0122ee8.png)

アクセスキー ID をテキストエディタにメモします。しっかり全文字コピーアンドペーストしてメモできているかを確認しましょう。

## シークレットアクセスキーをテキストエディタにメモ

![image](https://i.gyazo.com/3bbd2feb8eba42656da510cf9faaf68c.png)

シークレットアクセスキーの表示をクリックします。

![image](https://i.gyazo.com/97029c8ab8c0e4122786e3869f1c13f0.png)

シークレットアクセスキーをテキストエディタにメモします。シークレットアクセスキーは、閉じるまでの間、ここでしかメモすることができません。

しっかり全文字コピーアンドペーストしてメモできているかを確認しましょう。

![image](https://i.gyazo.com/dcd26a267777fbab105df98c0f6f7a6e.png)

閉じるボタンをクリックします。

![image](https://i.gyazo.com/0743f735f8a8799d09600a6ae50f2e32.png)

IAM の一覧画面に戻って、作成されたことを確認します。

## Cloud9 に設定を反映

![image](https://i.gyazo.com/c317a339450ce78517b22db098a771a8.png)

Cloud9 のターミナルに戻り、先ほどの Amplify CLI の設定途中になっています。

入力できたら Enter キーを押します。

![image](https://i.gyazo.com/5f266f1e0eb94cfa90ab87b43c2d89cc.png)

Amplify のための新しい IAM ユーザーのアクセスキーを聞かれるので、メモしたものを入力します。コピーアンドペーストできます。

![image](https://i.gyazo.com/64a046c31ef147a2bab0c683f7ec0afa.png)

ペーストするとこのように＊＊＊＊＊となります。

Enter キーを押します。

![image](https://i.gyazo.com/636916da111dbba008e6606f0dfaca97.png)

Amplify のための新しい IAM ユーザーのシークレットアクセスキーを聞かれるので、メモしたものを入力します。コピーアンドペーストできます。

![image](https://i.gyazo.com/2b907045a97f075eb110962d4880edf0.png)

入力できたら Enter キーを押します。

## プロファイル名の設定

この Cloud9 のローカルのプロファイル名を指定が聞かれます。

デフォルトのままで OK なので、 Enter キーを押します。

![image](https://i.gyazo.com/731f1a2ec7aa061fc1a7b765703721ab.png)

Successfully set up the new user. とでて、この Cloud9 での Amplify 初期設定は完了です！

## どうなっているか

- Cloud9
- Amplify ユーザー