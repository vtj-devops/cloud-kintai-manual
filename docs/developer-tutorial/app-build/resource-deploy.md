---
sidebar_position: 5
---

# リソースのデプロイ

Amplifyプロジェクトの初期化が完了したら、次に必要なリソースをデプロイします。以下のコマンドを実行して、リソースをデプロイします。

```bash
amplify push
```

コマンドを実行すると、`garakuSendMail`で使用する環境変数の値を入力するように求められます。

`garakuSendMail`は、メール送信機能を提供するためのLambda関数であり、AWS SES（Simple Email Service）を使用してメールを送信します。この関数を正しく動作させるため設定する必要があります。

後から、Amplifyの設定画面からも設定できますが、何らかの値を設定しておかないと、デプロイが完了しません。プロンプトの回答例は、以下の通りです。

```bash
? Enter the missing environment variable value of REGION in garakuSendMail: › ap-northeast-1
? Enter the missing environment variable value of EMAIL_FROM in garakuSendMail: › noreply@example.com
```

## Enter the missing environment variable value of REGION in garakuSendMail

`garakuSendMail`関数で使用するリージョンを入力します。ここでは、`ap-northeast-1`（東京リージョン）を入力します。

## Enter the missing environment variable value of EMAIL_FROM in garakuSendMail

`garakuSendMail`関数で使用するメールアドレスを入力します。所属する組織や団体でルールがない場合は、通常は`noreply@xxxx`の形式で入力します。

上記以外にも追加でプロンプトが表示されますが、特に変更する必要はありません。デフォルトのままでエンターキーを押してください。

```bash
? Are you sure you want to continue? (Y/n) › 
? Do you want to update code for your updated GraphQL API (Y/n)
? Do you want to generate GraphQL statements (queries, mutations and subscription) based on your schema types?
This will overwrite your current graphql queries, mutations and subscriptions (Y/n)
```
