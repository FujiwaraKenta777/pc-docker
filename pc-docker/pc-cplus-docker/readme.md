# Name

プログラミングコンテスト用実行環境
c++言語版

# 使い方

構成はこれ
https://qiita.com/jhorikawa_err/items/fb9c03c0982c29c5b6d5
内容はこれ
https://www.engilaboo.com/cpp-docker/

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
  docker-compose exec c-plus bash
  ```

* c++プログラムコンパイル
  ```
  cd opt/
  gcc g++ helloWorld.cpp -o helloWorld
  ```

* c++プログラム実行
  ```
  ./helloworld
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