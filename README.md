# mypkgについて
![test.bash](https://github.com/MYOYOSHINYA/mypkg/actions/workflows/test.yml/badge.svg)
* このレポジトリは未来ロボティクス学科のロボットシステム学で作成したものです。
* このレポジトリを使用するにはROS2をダウウンロードする必要があります。
## talkerコマンド
パブリッシャを持つノードであり、0.5秒おきに0から数字をカウントして"countup"というトピックを通じてlistener.pyに送信する

## listenerコマンド
サブリスクライバを持つノードであり、"countup"というトピックを通じてtalker.pyでカウントした数字を出力する
## launchファイル
複数のノードを一度に立ち上げる
## トピック
### countup
"talker.py"が生成した情報を"listene.py"が受け取りそれを出力するための通信経路
## インストール方法
ubuntu上で以下のコマンドを入力してクローンを作成する
```bash
$ git clone https://github.com/MYOYOSHINYA/mypkg.git
```
## 実行例

talker.pyとlistener.pyを異なる端末で実行する。実行方法は以下の通りです。
```bash
* 端末１
$ ros2 run mypkg talker
```

```bash
*　端末２
$ ros2 run mypkg listener
[INFO] [1703920876.273478009] [listener]: Listen: 61
[INFO] [1703920876.757911380] [listener]: Listen: 62
[INFO] [1703920877.282844039] [listener]: Listen: 63
[INFO] [1703920877.749514393] [listener]: Listen: 64
[INFO] [1703920878.283442294] [listener]: Listen: 65
[INFO] [1703920878.749288237] [listener]: Listen: 66
[INFO] [1703920879.283219975] [listener]: Listen: 67
[INFO] [1703920879.748667952] [listener]: Listen: 68
[INFO] [1703920880.283489270] [listener]: Listen: 69
[INFO] [1703920880.745031100] [listener]: Listen: 70
[INFO] [1703920881.267867858] [listener]: Listen: 71
[INFO] [1703920881.742683038] [listener]: Listen: 72
[INFO] [1703920882.283734854] [listener]: Listen: 73
[INFO] [1703920882.744839248] [listener]: Listen: 74
[INFO] [1703920883.280033841] [listener]: Listen: 75
[INFO] [1703920883.742604446] [listener]: Listen: 76
[INFO] [1703920884.276677364] [listener]: Listen: 77
[INFO] [1703920884.745594595] [listener]: Listen: 78
[INFO] [1703920885.260071152] [listener]: Listen: 79
```
端末１、端末２ともに　Ctrl + C で終了

* launchファイルを利用して一つの端末で出力する
```bash
$ ros2 launch mypkg talk_listen.launch.py

[INFO] [launch]: All log files can be found below /home/shinya1107/.ros/log/2023-12-30-16-28-50-500195-DESKTOP-CJ9LDDI-8973
[INFO] [launch]: Default logging verbosity is set to INFO
[INFO] [talker-1]: process started with pid [8975]
[INFO] [listener-2]: process started with pid [8977]
[listener-2] [INFO] [1703921331.492500182] [listener]: Listen: 0
[listener-2] [INFO] [1703921331.963793190] [listener]: Listen: 1
[listener-2] [INFO] [1703921332.502857296] [listener]: Listen: 2
[listener-2] [INFO] [1703921332.961785490] [listener]: Listen: 3
[listener-2] [INFO] [1703921333.503023787] [listener]: Listen: 4
[listener-2] [INFO] [1703921333.993283792] [listener]: Listen: 5
[listener-2] [INFO] [1703921334.480305007] [listener]: Listen: 6
[listener-2] [INFO] [1703921334.971440899] [listener]: Listen: 7
[listener-2] [INFO] [1703921335.477816414] [listener]: Listen: 8
[listener-2] [INFO] [1703921335.970084333] [listener]: Listen: 9
[listener-2] [INFO] [1703921336.475078227] [listener]: Listen: 10
[listener-2] [INFO] [1703921336.965353794] [listener]: Listen: 11
[listener-2] [INFO] [1703921337.470195437] [listener]: Listen: 12
[listener-2] [INFO] [1703921337.973702076] [listener]: Listen: 13
[listener-2] [INFO] [1703921338.467032233] [listener]: Listen: 14
[listener-2] [INFO] [1703921338.968677827] [listener]: Listen: 15
[listener-2] [INFO] [1703921339.463813074] [listener]: Listen: 16
[listener-2] [INFO] [1703921339.963982319] [listener]: Listen: 17
```
Ctrl + C で終了

## 必要なソフトウェア
* ROS2 foxy
* Python

## テスト環境
* ubuntu20.04
## ライセンス
* BSD-3-Clause License
* このパッケージのコードは、下記のスライド(CC-BY-SA 4.0 by Ryuichi Ueda)のものを、本人の許可を得て使用したものである。
* [ryuichiueda/mypkg](https://github.com/ryuichiueda/mypkg)
* © 2023 Shinya Myoyo
