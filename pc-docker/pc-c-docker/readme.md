# Name

プログラミングコンテスト用実行環境
c言語版

# 使い方

構成はこれ
https://qiita.com/jhorikawa_err/items/fb9c03c0982c29c5b6d5
内容はこれ
https://panda-program.com/posts/set-up-c-lang-with-docker

* 前準備
  * 実行したいファイルをoptに配置

* Dockerビルド(初回のみ)
  ```
  docker compose up -d --build
  docker image ls
  docker container ls
  ```

  * docker image ls で  pc-c-docker-c-lang が存在することを確認
  * docker container ls で  pc-c-docker-c-lang が存在することを確認

* コンテナ起動(2回目から)
  ```
  docker compose up -d
  ```

* コンテナ接続
  ```
  docker-compose exec c-lang bash
  ```

* cプログラムコンパイル
  ```
  cd opt/
  gcc hello.c
  ```

* cプログラム実行
  ```
  ./a.out
  ```

* 終了
  * コンテナから切断
    ```
    exit
    ```
  * コンテナを終了
    ```
    docker compose down
    ```
  * 確認
    ```
    docker container ls
    ```