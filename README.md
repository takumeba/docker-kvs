# 概要

Jenkinsでdocker-composeのCI/CDをおこなうための手順書。

# 構成

1. ローカルマシン
2. ビルドサーバー + Jenkins
3. 本番サーバー

ローカルサーバーは開発者のローカルマシン(PC)を想定。
ここで開発したものを、GitHubにPushする。

ビルドサーバー上にJenkinsはコンテナとして展開される。
JenkinsはGitHubに更新があると、パイプラインを開始し、自身がのるビルドサーバー上でdocker-composeを使ってビルドを行う。
作成されたイメージはレジストリに登録される。

ビルドに成功したら、本番環境にdocker-composeでサービスが展開される。
展開はレジストリ上のイメージからおこなわれる。

# セットアップ
続きは書籍にて
