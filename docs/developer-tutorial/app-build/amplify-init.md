---
sidebar_position: 4
---

# Amplifyプロジェクトの初期化

Amplify CLIの設定が完了したら、次にAmplifyプロジェクトを初期化します。以下のコマンドを実行して、プロジェクトを初期化します。

```bash
amplify init
```

## 環境名の入力

コマンドを実行すると、以下のようなプロンプトが表示されます。プロンプトの回答例です。

```bash
? Enter a name for the environment (dev): main
? Choose your default editor: Visual Studio Code
? Select the authentication method you want to use: AWS profile
? Please choose the profile you want to use <profile-name>
```

### Enter a name for the environment

環境名を入力します。勤怠アプリを実行環境のみで使用する場合は、`main`と入力します。開発環境を分けたい場合は、`dev`や`staging`などの名前を付けることもできます。

### Choose your default editor

使用するエディタを選択します。ここでは、`Visual Studio Code`を選択していますが、他のエディタを使用している場合は適宜変更してください。勤怠アプリでは、Visual Studio Codeを使用することをお勧めします。

### Select the authentication method you want to use

認証方法を選択します。ここでは、`AWS profile`を選択します。これにより、先ほど設定したAWSプロファイルを使用してAmplify CLIがAWSにアクセスできるようになります。

### Please choose the profile you want to use

プロファイル名を入力します。先ほど設定したプロファイル名を入力してください。もし、プロファイル名を省略した場合は、`default`が使用されます。

## ステータスの確認

プロンプトの入力ができてコマンドの実行が完了したら、`amplify status`コマンドを実行して、現在の環境のステータスを確認します。

順調に進んでいれば、以下のような出力が表示されます。

```bash
    Current Environment: main
    
┌──────────┬────────────────────────┬───────────┬───────────────────┐
│ Category │ Resource name          │ Operation │ Provider plugin   │
├──────────┼────────────────────────┼───────────┼───────────────────┤
│ Api      │ AdminQueries           │ Create    │ awscloudformation │
├──────────┼────────────────────────┼───────────┼───────────────────┤
│ Api      │ garakufrontend         │ Create    │ awscloudformation │
├──────────┼────────────────────────┼───────────┼───────────────────┤
│ Auth     │ garakufrontendbabcd123 │ Create    │ awscloudformation │
├──────────┼────────────────────────┼───────────┼───────────────────┤
│ Custom   │ customResource1234abcd │ Create    │ awscloudformation │
├──────────┼────────────────────────┼───────────┼───────────────────┤
│ Function │ AdminQueriesf1234abc   │ Create    │ awscloudformation │
├──────────┼────────────────────────┼───────────┼───────────────────┤
│ Function │ garakuSendMail         │ Create    │ awscloudformation │
├──────────┼────────────────────────┼───────────┼───────────────────┤
│ Storage  │ s123456789             │ Create    │ awscloudformation │
├──────────┼────────────────────────┼───────────┼───────────────────┤
│ Hosting  │ amplifyhosting         │ Update    │                   │
└──────────┴────────────────────────┴───────────┴───────────────────┘
```
