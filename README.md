# mypkgについて
![test.bash](https://github.com/MYOYOSHINYA/mypkg/actions/workflows/test.yml/badge.svg)
* このレポジトリは未来ロボティクス学科のロボットシステム学で作成したものです。

## talkerコマンド
パブリッシャを持つノードであり、0から数字をカウントして"countup"というトピックを通じてlistener.pyに送信します

## listenerコマンド
パブリッシャを持つノードであり、"countup"というトピックを通じてtalker.pyでカウントした数字を出力する
## launchファイル
複数のノードを一度に立ち上げる
## トピック
"talker.py"が生成した情報を"listene.py"が受け取りそれを出力するための通信経路
## インストール方法
* github、Python、ROS2が利用できる環境で、以下のコマンドを入力する
'$ mkdir -p ros2_ws/src'
'$ cd ~/ros2_ws/src'
* 以下のコマンドで環境をコピーする
* $ git clone git@github.com:MYOYOSHINYA/mypkg.git
* 以下のコマンドでダウンロードされていることを確認する
* $ ls
* 最後に以下のコマンドを入力してビルドする
* $ cd ~/ros_ws

* $ colcon build
* $ source ~/.bashrc


## 実行例


## 必要なソフトウェア
* ROS2
* Python

## テスト環境
* Ubuntu 20.04

## ライセンス
* BSD-3-Clause License
* © 2023 Shinya Myoyo
