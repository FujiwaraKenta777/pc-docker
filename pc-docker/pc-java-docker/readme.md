# Name

プログラミングコンテスト用実行環境
Java11版

# 使い方

構成はこれ
https://qiita.com/jhorikawa_err/items/fb9c03c0982c29c5b6d5
内容はこれ
https://qiita.com/A-Kira/items/0dda255e00771f556e2a

* 前準備
  * 実行したいファイルをoptに配置

* Dockerビルド(初回のみ)
  ```
  docker compose up -d --build
  docker image ls
  docker container ls
  ```

  * docker image ls で pc-java-docker-java が存在することを確認
  * docker container ls で pc-java-docker-java が存在することを確認

* コンテナ起動(2回目から)
  ```
  docker compose up -d
  ```

* コンテナ接続
  ```
  docker-compose exec java bash
  ```

* Javaプログラムコンパイル
  ```
  cd opt/
  python sample.py 180.0
  ```

* Javaプログラム実行
  ```
  java Main
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