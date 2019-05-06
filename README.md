# kaggle-titanic
以下のコンペのためのリポジトリです。
https://www.kaggle.com/c/titanic


## Setup

### データのセットアップ
下記のページからデータをすべてダウンロードして、input/ フォルダに配置します。
https://www.kaggle.com/c/titanic/data

### docker-compose のセットアップ
1. 下記の手順を参考に Docker CE、Docker Compose をインストールします。
- https://docs.docker.com/install/
- https://docs.docker.com/compose/install/

2. 下記のコマンドで、jupyter notebook が開始します。
```shell
cd docker
docker-compose up
```

3. jupyter notebook 開始時にコンソールに下記のような URL が表示されます。表示された URL にアクセスします。
- http://localhost:8888/?token=<起動ごとに異なる値>

    あとは、通常の jupyter notebook と同様に操作してください。

4. jupyter notebook を終了する場合は下記のコマンドを実行してください。
```shell
cd docker
docker-compose down
```


**補足**  
GPU 付きのマシンかつ、[NVIDIA Docker](https://nvidia.github.io/nvidia-docker/) がインストールされている場合は、上記のコマンドではなく下記のコマンドを使うことで GPU 対応の  Docker image を使用できます。

```shell
cd docker

# jupyter notebook 開始
docker-compose -f docker-compose.gpu.yml up

# jupyter notebook 終了
docker-compose -f docker-compose.gpu.yml down
```

