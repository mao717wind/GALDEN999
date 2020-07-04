#  Adafruit  gemmaでNeoPixel LEDを光らせる!

#### 準備するもの
1. Adafruit gemma
2. NeoPixel LED
3. Micro USB

### 配線図

Adafruit gemmaとNeoPixelLEDを以下のように配線します。

[![Image from Gyazo](https://i.gyazo.com/2a20767b0a63c83195495d191eccc965.png)](https://gyazo.com/2a20767b0a63c83195495d191eccc965)

| gemma  |  NeoPixelLED |
|---|---|
| Vout  |  5V |   
| D1・A1 |　Din   |   
|  GND | GND  |   



### プログラミング環境セットアップ

「Arduino IDE」というソフトウェアを使ってプログラムを書いていきます。 [公式サイト](https://www.arduino.cc/en/Main/Software#)からソフトウェアをダウンロードしてください。

### Arduino IDEでLEDテープ用のライブラリを追加する

NeoPixelというLEDテープを光らせるために必要なライブラリーをインストールします。

* [Arduino]→[Preferences] をクリック
###### ※ Arduino IDEのバージョンによっては　[ファイル]→[環境設定]になります。

[![Image from Gyazo](https://i.gyazo.com/b96cb8bddfe6a7280b4691b7fa4b9fc0.gif)](https://gyazo.com/b96cb8bddfe6a7280b4691b7fa4b9fc0)

* 以下のAdafruitのURLをコピーして、追加のボードマネージャーのURLに貼り、OKをクリックしてください。

`https://www.adafruit.com/package_adafruit_index.json`

[![Image from Gyazo](https://i.gyazo.com/3ecc10f542ccb09d554e101c53af6d4d.png)](https://gyazo.com/3ecc10f542ccb09d554e101c53af6d4d)


* [スケッチ]→[ライブラリをインクルード]→[ライブラリを管理]をクリックしてください。

[![Image from Gyazo](https://i.gyazo.com/5ab321f971312021e5e3260a9ddb6f15.gif)](https://gyazo.com/5ab321f971312021e5e3260a9ddb6f15)


* すると以下のような画面になります。検索欄に「Neopixel」と入力します。Adafruit Neopixel by Adafruit を選択してインストールしてください。


[![Image from Gyazo](https://i.gyazo.com/eaf57ed9371763d70b8e544fd15b66ff.png)](https://gyazo.com/eaf57ed9371763d70b8e544fd15b66ff)


これで、ライブラリのインストール完了です！

### Adafruit Gemmaにプログラムを書き込む

##### Gemmaに書き込むための設定

まずは、ボードを選択するために[ツール]→[ボード]→[Arduino Gemma] をクリックしてください。

[![Image from Gyazo](https://i.gyazo.com/5cafc0b4f8f87cd8eeab9631ac62b599.png)](https://gyazo.com/5cafc0b4f8f87cd8eeab9631ac62b599)

次に書き込み装置を選択します。[ツール]→[書込装置]→[USBtinyISP]をクリックしてください。そして、以下のプログラムをスケッチにコピー&ペーストしてください。
[![Image from Gyazo](https://i.gyazo.com/b571d43b040071bc3da7fd49dddf46e1.png)](https://gyazo.com/b571d43b040071bc3da7fd49dddf46e1)

#####　書き込みたいプログラムを書く

今回LEDテープを光らせるプログラムはこちらから選べます。

https://github.com/mao717wind/gyaruden

プログラムを選び、コピー＆ペーストしてください。






##### プログラムを書き込む
[スケッチ]→[書込装置を使って書き込む] をクリックします。
[![Image from Gyazo](https://i.gyazo.com/9ab8f7993a9181d75d51f5badf182647.png)](https://gyazo.com/9ab8f7993a9181d75d51f5badf182647)


[書込装置を使って書き込む]をクリック後、Gemmaにある小さなボタンを押すと、こちらのように赤いLEDが10秒間点滅します。赤いLEDが点滅し終わると、プログラムの書き込みが終了になります。
[![Image from Gyazo](https://i.gyazo.com/a1920b51bc85df9a41beb97888945557.gif)](https://gyazo.com/a1920b51bc85df9a41beb97888945557)
