# deeplearning-env
Dockerでkeras+jupyterのディープラーニング環境を整えます。GPU必須。Ubuntu16.04推奨。
## Installation
### Docker
Refer to https://docs.docker.com/install/linux/docker-ce/ubuntu/
### Docker Compose
Refer to https://github.com/docker/compose/releases
### nvidia-docker
Refer to https://github.com/NVIDIA/nvidia-docker
## Usage
### プロジェクトフォルダ
リポジトリ直下のdataフォルダがコンテナとの共有フォルダになっています。ここにjupyter notebookで使う各種データを入れてください。
### Alias(推奨)
```
alias dco='docker-compose'
```
### 起動
初回起動時のみビルドが始まります。
```
dco up
```
localhost:8888にアクセスするとjupyter notebookが起動しています。
### 終了
```
dco down
```
イメージごと削除するなら
```
dco down --rmi all
```