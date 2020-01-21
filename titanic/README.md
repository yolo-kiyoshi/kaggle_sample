# 概要
Dockerコンテナにパッケージ管理ツール`poetry`を使って分析環境を構築します。

# 準備

- Dockerをインストールします
- [Kaggle](https://www.kaggle.com/c/titanic/data)から`train.csv`(学習データ)と`test.csv`(テストデータ)をダウンロードし、`data/raw/`に配置します

# 使い方
## ビルドとコンテナ起動
`docker-compose.yml`と同一ディレクトリにて、以下のコマンドによりDockerイメージのビルドとコンテナを起動できます。
```
docker-compose up -d
```

_※`Dockerfile`を変更しリビルドしたい場合は`docker-compose up -d --build`を実行する_

## jupyterへのアクセス
コンテナ実行後、以下にアクセスすることでJupyter labにアクセスできます。  
<a>http://localhost:8888/lab</a>

## パッケージの追加
以下のコマンドでPythonパッケージを追加できます。
```
poetry add <追加したいパッケージ>
```