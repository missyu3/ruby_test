## Docker コマンド

- image 作成
  - docker pull ruby:3.0.0-preview1-alpine
- コンテナ作成
  - docker run -d -it IMAGE ID
    - docker images で表示される ID を run コマンドの後に入力する。
    ```
    docker run -d -it e9ca01973428
    ```
- コンテナ実行
  - docker exec -it NAMES sh
- bash のインストール

  - apk add bash

- 削除
  - コンテナ一括削除
    - docker rm -f `docker ps -a -q`
  - image 一括削除
    - docker rmi `docker images -q`
