# DTM
音楽的あるいは技術的な裏付けはほぼ皆無の作曲･編曲メモ。  



### <b>INDEX</b>
* [ドラムセット](#DrumSet): GM音源のドラムセットを利用する
* [レイテンシー](#Latency): ASIO4ALLを使ってレイテンシーを小さくする
* [クオンタイズ](#AutoQuantize): クオンタイズをグリッドに揃える
* [ベロシティ](#AutoVelocity): ベロシティをベタで揃える
* [ドラムパターン](#DrumPattern): XXXXXXX
* [コード進行](#ChordProgression): XXXXXXX
* [GrageBand](https://github.com/mubirou/DTM/tree/main/garageband): Apple GarageBandのサンプル（旧）

***



<a name="DrumSet"></a>
## ドラムセット

### 説明
GM（General MIDI）の「チャンネル10番」にはドラムセットなどパーカッション用（リズム音色）が予約されています。ここではドラムセットに含まれる主な音色をピックアップします。

### 使い方
1. "Insert MIDI Track"（MIDIトラックの挿入）
1. "Enable Inline MIDI Editing"（インラインMIDI編集を有効にする）
1. "MIDI Output"（MIDI出力）を"DLS Soft Synth"（DLSソフトシンセ）に設定
1. "MIDI Channel"（MIDIチャンネル）を"10"に設定
1. "Drum Kits"（ドラムキット）は"Standard"に設定

|通称|音階|音色名|概要|nanoKEY2|
|:--:|:--:|:--|:--|:--:|
|バスドラ|C|Bass Drum 1|大ダイコ（フットペダルで叩く）|-1 OCT|
|スネア|D|Acoustic Snare|小ダイコ|-1 OCT|
|ハイハット①|F#|Closed Hi-hat|2枚のシンバル（フットペダルで開閉）|-1 OCT|
|フロア|G|High Floor Tom|床に置くタムタム|-1 OCT|
|タムタム②|A|Low Tom|（使わない）|-1 OCT|
|ハイハット②|A#|Open Hi-hat|2枚のシンバル（フットペダルで開閉）|-1 OCT|
|タムタム①|D2|High Tom|リズムの切れ目に入れる|-1 OCT|
|クラッシュシンバル|C#2|Crash Cymbal 1|アクセント用（両サイドの小シンバル）|-1 OCT|
|ライドシンバル|D#2|Ride Cymbal 1|基本リズムを刻む（大きめのシンバル）|-1 OCT|

実行環境：ACID Xpress 7、ACID Pro 10、KORG nanoKEY2   
作成者：夢寐郎  
作成日：2020年10月21日  



<a name="Latency"></a>
## レイテンシー

### 説明
レイテンシーを小さくするためにASIOドライバ（ASIO4ALL）を使います。MIDIキーボード入力の遅れがなくなります。


### 設定方法
1. http://www.asio4all.org/ から「ASIO4ALL 2.14」をインストール
1. ACIDの[オプション]-[ユーザー設定]-[オーディオデバイス]の「オーディオデバイスの種類」から「ASIO4ALL v2」を選択し「適用」  
（Xpressの場合[Options]-[Preferences]-[Audio Device]-[Audio device]-[ASIO4ALL v2]）
1. 引き続き「詳細」（Advanced）を選択
1. 「オーディオの詳細設定」の「設定」（Configure）を選択
1. 「ASIO4ALL v2.14」設定画面で、利用したいオーディオインターフェイス（AKG C44-USB Microphone）を選択
1. Windowsの[設定]-[システム]-[サウンド]-[出力デバイスを選択してください]で上記のオーディオインターフェイスを選択

実行環境：ACID Pro 10、ACID Xpress 7、AKG Lyra、ASIO4ALL v.2.14  
作成者：夢寐郎  
作成日：2020年10月22日  
更新日：2020年10月24日



<a name="AutoQuantize"></a>
## クオンタイズ

### 説明
MIDIキーボードを使ってリアルタイムレコーディングしたものを、16分音符のグリッドにかっちり揃えます。

### 操作方法
1. グリッドに揃えたいMIDIトラックを選択。
1. [編集]-[MIDIプロセスとフィルタ]-[クオンタイズ]を選択。
1. 次の項目を選択して「適用」を押す。
    * クオンタイズスタート
    * クオンタイズリリース
    * 選択したトラックのすべての音符に適用

実行環境：ACID Pro 10、ACID Xpress 7  
作成者：夢寐郎  
作成日：2020年10月22日  



<a name="AutoVelocity"></a>
## ベロシティ

### 説明
MIDIキーボードを使ってリアルタイムレコーディングしたもののベロシティをベタで揃えます。

### 操作方法
1. ベロシティを揃えたいMIDIトラックを選択。  
    ベロシティが表示されていない場合、[表示]-[インラインMIDI編集の表示]-[ノートオンベロシティ]で表示。
1. [編集]-[MIDIプロセスとフィルタ]-[ベロシティ]を選択。  
 （Xpressの場合は[Edit]-[MIDI Processes Filters]-[Velocity]）
1. 次の項目を選択または設定して「適用」を押す。
    * スタート ベロシティ（Change Start Velocity）：✔
    * リリース ベロシティ（Change Release Velocity）：✔
    * 値の設定: 100（1～127／初期値64）
    * 選択したトラックのすべての音符に適用（Apply to all notes selected tracks）

実行環境：ACID Pro 10、ACID Xpress 7  
作成者：夢寐郎  
作成日：2020年10月22日  
更新日：2020年10月24日



<a name="DrumPattern"></a>
## ドラムパターン

|種類|概要|.mid|.mp3|
|:--:|:--|:--:|:--:|
|8beat|8分音符主体（Hi-hat版）ROCK･POPS|[●](https://mubirou.github.io/DTM/mid/8beat_Hi-hat.mid)|[●](https://mubirou.github.io/DTM/mp3/8beat_Hi-hat.mp3)|
|8beat|同上（Ride Cymbal版）|[●](https://mubirou.github.io/DTM/mid/8beat_RideCymbal.mid)|[●](https://mubirou.github.io/DTM/mp3/8beat_RideCymbal.mp3)|
|8beat|同上（Floor Tom版）|[●](https://mubirou.github.io/DTM/mid/8beat_FloorTom.mid)|[●](https://mubirou.github.io/DTM/mp3/8beat_FloorTom.mp3)|
|16beat|16分音符主体, FUNK･ROCK･J-POP|[●](https://mubirou.github.io/DTM/mid/16beat.mid)|[●](https://mubirou.github.io/DTM/mp3/16beat.mp3)|
|Swing|Shuffle,|[●]()|[●]()|

* 参考：https://www.youtube.com/watch?v=_YgCsGy_rHA

実行環境：ACID Pro 10、ACID Xpress 7  
作成者：夢寐郎  
作成日：2020年10月24日  
更新日：2020年10月25日  



<a name="ChordProgression"></a>
## コード進行

|種類|コード進行|.mid|.mp3|
|:--:|:--|:--:|:--:|
|王道進行|F-G-Em-Am|[●](https://mubirou.github.io/DTM/mid/chord01.mid)|[●](https://mubirou.github.io/DTM/mp3/chord01.mp3)|
|椎名林檎進行|FM7-E7-Am7-CM7|[●](https://mubirou.github.io/DTM/mid/chord01.mid)|[●](https://mubirou.github.io/DTM/mp3/chord01.mp3)|

* 参考：https://www.youtube.com/watch?v=tE-b4nvusB8

実行環境：ACID Pro 10、ACID Xpress 7  
作成者：夢寐郎  
作成日：2020年10月31日  