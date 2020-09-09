# Hands-on 1: 初めてのEC2インスタンスを起動する
- awsのアクセスキー設定
    1. awsのコンソール(https://console.aws.amazon.com)にログインし、「マイセキュリティ資格情報」から新しいアクセスキーを発行
    2. 下記のようにファイルに書き込む
        ```
        $ cat ~/.aws/credentials
        [default]
        aws_access_key_id = XXXXXXXXXXXXXXXXXX
        aws_secret_access_key = YYYYYYYYYYYYYYYYYYY

        $ cat ~/.aws/config
        [profile default]
        region = ap-northeast-1
        output = json
        ```
- プロジェクト用のコンテナ作成
    ```
    docker run --name myaws -it -v ~/.aws:~/.aws bash
    ```